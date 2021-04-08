# Padrões Emergentes

## Component Pattern

<p style="text-indent: 20px; text-align: justify">
O padrão de componentes no React.js baseia-se em utilizar diversos componentes potencialmente reutilizáveis para compor o código de uma interface gráfica, dessa forma é possível obter um baixo acoplamento e uma alta coesão no código da interface. Visto que toda a estrutura será separada em pedaços menores a reusabilidade será alta, porém como consequência pode acabar se tornando mais complexo.
</p>

### Exemplo de código do projeto

<p style="text-indent: 20px; text-align: justify">
No exemplo abaixo, temos o componente TextInput sendo reutilizado diversas vezes e os dados que diferem em cada chamada são passados como <em>props</em> (dados que um componente pai passa para um filho). É possível ver que há outros componentes sendo utilizados.
</p>

``` typescript
import React, { useState } from 'react';

import {
  SubmitBtn,
  Container,
  ProfileImage,
  FormContainer,
  ProfileImageContainer,
} from './styles';

import TextInput from '../../components/TextInput';

const Signup: React.FC = () => {
  const history = useHistory();
  const dispatch = useDispatch();

  const [name, setName] = useState('');
  const [email, setEmail] = useState('');
  const [phone, setPhone] = useState('');
  const [nickname, setNickname] = useState('');
  const [password, setPassword] = useState('');
  const [loading, setLoading] = useState(false);
  const [passwordConfirmation, setPasswordConfirmation] = useState('');

  return (
    <Container>
      <ProfileImageContainer>
        <ProfileImage>{(name && name[0].toUpperCase()) || 'A'}</ProfileImage>

        <MdAddAPhoto size="32" color="var(--white)" />
      </ProfileImageContainer>

      <FormContainer>
        <TextInput
          value={name}
          disabled={loading}
          variant="outlined"
          label="Nome Completo"
          placeholder="Digite o nome"
          onChange={(e: React.ChangeEvent<HTMLInputElement>) =>
            setName(e.target.value)
          }
        />

        <TextInput
          value={nickname}
          disabled={loading}
          variant="outlined"
          label="Nome de usuário (Apelido)"
          placeholder="Digite o nome de usuário"
          onChange={(e: React.ChangeEvent<HTMLInputElement>) =>
            setNickname(e.target.value)
          }
        />

        <TextInput
          label="Email"
          value={email}
          disabled={loading}
          variant="outlined"
          placeholder="Digite o email"
          onChange={(e: React.ChangeEvent<HTMLInputElement>) =>
            setEmail(e.target.value)
          }
        />

        <TextInput
          value={phone}
          label="Telefone"
          disabled={loading}
          variant="outlined"
          placeholder="Digite o telefone"
          onChange={(e: React.ChangeEvent<HTMLInputElement>) =>
            setPhone(e.target.value)
          }
        />

        <TextInput
          label="Senha"
          type="password"
          value={password}
          variant="outlined"
          disabled={loading}
          placeholder="Digite uma senha"
          onChange={(e: React.ChangeEvent<HTMLInputElement>) =>
            setPassword(e.target.value)
          }
        />

        <TextInput
          type="password"
          variant="outlined"
          disabled={loading}
          label="Senha repetida"
          value={passwordConfirmation}
          placeholder="Confirme sua senha"
          onChange={(e: React.ChangeEvent<HTMLInputElement>) =>
            setPasswordConfirmation(e.target.value)
          }
        />

        <SubmitBtn onClick={send}>CADASTRAR</SubmitBtn>
      </FormContainer>
    </Container>
  );
};

export default Signup;
```

## Active Record

<p style="text-indent: 20px; text-align: justify">
Um objeto que carrega consigo, dados e comportamentos. Muitos desses dados precisam ser armazenados em um banco de dados. A Active Record propõe a abordagem de utilizar a lógica de acesso de dados no próprio objeto. Isso permite a nós todos sabermos como ler e escrever os dados do objeto no Banco de dados.
</p>

<p style="text-indent: 20px; text-align: justify">
O Django, assim como outros frameworks Back-end, faz uso desse padrão de arquitetura. No caso, as Django Models carregam consigo todo o domínio lógico e também as lógicas de manipulamento do banco de dados. Nesse padrão as classes são convenientes, mas eles não escondem o fato que os bancos relacionais estão presentes. Como resultado, é comumente visto outros padrões de ORM (object-relational mapping) presentes quando se está usando Active Record.
</p>

<p style="text-indent: 20px; text-align: justify">
Para o nosso contexto, optamos por uma abordagem a partir da modelagem de banco de dados, podendo a mesma ser vista <a href="../../iniciativa/modelagem_bd">aqui</a>
</p>

Exemplo com modelagem:

![Modelagem exemplo](../../../../assets/padroes_emergentes/active_record.png)

<p style="text-indent: 20px; text-align: justify">
Toda a lógica de acesso ao banco é fornecida por meio de polimorfismo. E é evidente os métodos básicos para persistir o dado, apagar o dado persistido, criar uma nova instância.
</p>


``` python
class Person(AbstractBaseUser):
    name = models.CharField(max_length=256)
    email = models.EmailField(max_length=256, primary_key=True)
    nickname = models.CharField(max_length=256, unique=True)
    picture = models.BinaryField()
    USERNAME_FIELD = "nickname"
    REQUIRED_FIELDS = [
        "name",
        "email",
        "password",
    ]


class Phone(models.Model):
    email = models.ForeignKey(Person, on_delete=models.CASCADE)
    phone_number = models.IntegerField()

# métodos de criação de instância
person = Person.create({ # atributos de pessoa
})
# métodos de criação de instância
phone = Phone.create(email=person ...) # Restante do atributos
# salvar os dados no banco
person.save()
phone.save()
```

## Referências

> FOWLER, Martin. "Patterns of Enterprise Application Architecture". Addison-Wesley Signature Series. 2002.

> "Components and Props". React. Disponível em: https://reactjs.org/docs/components-and-props.html. Acesso em: 07 abr. 2021

> "Design Patterns In React Native: Component Patterns". mohit199thd. Disponível em: https://dev.to/mohit199thd/design-patterns-in-react-native-component-patterns-352f. Acesso em: 07 abr. 2021

> "Filosofias de projeto". . Disponível em: https://docs.djangoproject.com/pt-br/2.2/misc/design-philosophies/#models. Acesso em: 07 abr. 2021

## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
|  1.0   | 07/04/2021 | Criação do documento | - | Todos os integrantes |
