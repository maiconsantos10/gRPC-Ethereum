 <div align="center">
   <img src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/005b9413-c5f5-4266-b295-673624b84ee1/dejsa57-04ca2134-b770-4e2b-a09f-a1b5b7c27928.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzAwNWI5NDEzLWM1ZjUtNDI2Ni1iMjk1LTY3MzYyNGI4NGVlMVwvZGVqc2E1Ny0wNGNhMjEzNC1iNzcwLTRlMmItYTA5Zi1hMWI1YjdjMjc5MjguZ2lmIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.yGAX8LUod_AWRCu986KvR1EYi6LivFEed85DjlhKQyc">
 </div>
 
<h1><i> Ⅰ - Sejam bem vindos ao futuro. II - É recomendado e indispensável que todos apertem os cintos, pois todo o conhecimento necessário será passado durante a leitura deste documento. III - Para aqueles que ainda não estão prontos para a verdade, caiam de joelhos e entendam que todos devem servir ao verdadeiro Senhor, dos vivos e dos mortos. </i> </h1>
<br> <br> 
 
 # ✏️ Módulo gRPC 
 ```
 É uma arquitetura e um sistema de API de código aberto controlados pela Cloud Native Computing Foundation.
 A proposta é que o cliente interaja com o servidor por meio de chamadas de funções simples, ou seja, de interface de códigos geradas pelo próprio gRPC. 
 ```
 # ✏️ Vantagem na arquitetura de microsserviços 
 ```
 Fácil o contrato entre cliente e servidor.
 Melhor desempenho dos serviços.
 Features nativas do HTTP/2, como streaming de dados, load balance, monitoramento etc.
```
# ✏️ O que incluirá na funcionalidade? 
 ```
Criação de carteira, consulta de saldo, envio transacional e assinatura de mensagens.
```
# Iniciando a task:
Iniciando o Maven
1) Criar o projeto Maven (Terminal VSCode)
Crie uma pasta onde quiser e abra no VSCode. Depois no terminal:
```
mvn -B archetype:generate \
 -DgroupId=com.maicon.wallet \
 -DartifactId=wallet-grpc-service \
 -DarchetypeArtifactId=maven-archetype-quickstart \
 -DarchetypeVersion=1.4 \
 -DinteractiveMode=false
```
2) Ajustar o pom.xml para gRPC + web3j
Logo abaixo de <version>1.0-SNAPSHOT</version>, adicione as propriedades:
```
<properties>
    <maven.compiler.source>17</maven.compiler.source>
    <maven.compiler.target>17</maven.compiler.target>
    <grpc.version>1.62.2</grpc.version>
    <protobuf.version>3.25.3</protobuf.version>
    <web3j.version>4.10.0</web3j.version>
</properties>
```
3) Dentro de *dependencies - /dependencies*..., adicione essas dependências (você pode deixar a de junit que já veio, não precisa apagar):    
```
<!-- gRPC -->
<dependency>
    <groupId>io.grpc</groupId>
    <artifactId>grpc-netty-shaded</artifactId>
    <version>${grpc.version}</version>
</dependency>
<dependency>
    <groupId>io.grpc</groupId>
    <artifactId>grpc-protobuf</artifactId>
    <version>${grpc.version}</version>
</dependency>
<dependency>
    <groupId>io.grpc</groupId>
    <artifactId>grpc-stub</artifactId>
    <version>${grpc.version}</version>
</dependency>

<!-- Protobuf runtime -->
<dependency>
    <groupId>com.google.protobuf</groupId>
    <artifactId>protobuf-java</artifactId>
    <version>${protobuf.version}</version>
</dependency>

<!-- Web3j para integração Ethereum -->
<dependency>
    <groupId>org.web3j</groupId>
    <artifactId>core</artifactId>
    <version>${web3j.version}</version>
</dependency>
```  
4) Salve o pom.xml e teste se o Maven consegue compilar:
```
mvn clean compile
```

> Se aparecer algo como "BUILD SUCCESS", quer dizer que o projeto já está pronto para receber o .proto e gerar o código gRPC.





<i>
 > ✨ A única forma dos homens chegarem a algum lugar é deixando algo para trás.
 </i>
