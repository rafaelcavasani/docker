# SonarQube

## Como rodar
`docker-compose up -d`

## Como Rodar
O sonarqube irá subir um servidor na porta 9090 da sua maquina.


### Maven
* Fazer login em `http://localhost:9000` com username `admin` e senha `admin`;
* Criar um projeto e gerar o token do projeto;
* Rodar: `mvn sonar:sonar -Dsonar.projectKey=<NOME_DO_PROJETO> -Dsonar.host.url=http://localhost:9000 -Dsonar.login=<TOKEN_DO_PROJETO>`;


### Gradle
Plugins:
```
plugins {
    id "jacoco"
    id "java"
    id "application"
    id "org.sonarqube" version "3.0"
}

sonarqube {

    properties {

        property 'sonar.projectName', 'Example of SonarQube Scanner for Gradle Usage'

    }

}
```
* Executar: `./gradlew -Dsonar.login=5b2034e871ec685ce42a1399ba6b2080b2c2490d -Dsonar.host.url=http://myhost:9000 sonarqube`