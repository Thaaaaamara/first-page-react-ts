# first-page-react-ts

- Instalar NVM: curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash

- Reiniciar o terminal: source /home/gio/.bashrc

- Listar versões em Node disponíveis: nvm ls-remote

- Instalar uma versão específica do Node: nvm install v22.11.0

- Instalar Vite com React e Typescript: npm create vite@latest . -- --template react-ts

- Todo projeto de NodeJS contém um arquivo chamado package.json





# Conceitos de Typescript:

```typescript

type UserAddressType = {
    rua: string;
    numero: number;
    complemento: string;
    bairro: string;
    cep: string;
    ibge: number;
}

type UserDataType = {
    id: number;
    userName: string;
    userAge: number;
    userEmail: string;
    address: UserAddressType;
    telefones: Array<string>;
}

const userData: UserDataType = {
    id: 1,
    userName: "Thamara",
    userAge: 31,
    userEmail: "thamara@gmail.com",
    address: {
        rua: "Alice Vieira",
        numero: 120,
        complemento: "apartamento 504",
        bairro: "São Vicente",
        cep: "88309-214",
        ibge: 25,
    },
    telefones: ["(47) 99666-6745", "(47) 99928-7400", "(47) 99925-3012"],
}

// Criar um modelo de dados que represente um carro e a marca a qual pertence o carro.
// A marca do carro deve ter nome, país e id.
// O carro deve ter modelo, ano, marca e id.

type Marca = {
    id: number;
    nome: string;
    pais: string;
}

type Carro = {
    id: number;
    modelo: string;
    ano: number;
    marca: Marca;
}

const carro1: Carro = {
    id: 1,
    modelo: "HB20",
    ano: 2020,
    marca: {
        id: 2,
        nome: "Hyundai",
        pais: "Coréia do Sul",
    }
}

const carro2: Carro = {
    id: 2,
    modelo: "GOL",
    ano: 2021,
    marca: {
        id: 3,
        nome: "Volkswagen",
        pais: "Alemanha",
    }
}

const carrosList: Array<Carro> = [carro1, carro2];

console.log(carrosList[1].marca.pais)
```

