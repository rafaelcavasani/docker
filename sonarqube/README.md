# SonarQube

## Como rodar
`docker-compose up -d`

## Como Rodar
O sonarqube irá subir um servidor na porta 9090 da sua maquina.


* Fazer login em `http://localhost:9000` com username `admin` e senha `admin`;
* Criar um projeto e gerar o token do projeto;

### Maven
* Rodar: `mvn sonar:sonar -Dsonar.projectKey=<NOME_DO_PROJETO> -Dsonar.host.url=http://localhost:9000 -Dsonar.login=<TOKEN_DO_PROJETO>`;


### Gradle
* Executar: `./gradlew sonarqube -Dsonar.projectKey=<NOME_PROJETO_AQUI> -Dsonar.host.url=http://localhost:9000 -Dsonar.login=<SEU_TOKEN_AQUI>`

Add Plugin:
```
plugins {
    id "org.sonarqube" version "3.4.0.2513"
}
```
