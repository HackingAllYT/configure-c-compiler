# C Compiler
## _Tutorial definitivo para crear a túa primeira aplicación_

<p align="center"> <img width="200" height="200" src="https://avatars.githubusercontent.com/u/87182741?v=4"> </p>

C é unha das linguaxes máis extendidas e unha das máis populares debido á súa 
potencia e velocidade. Neste caso empregarase para comezar a apaixonte andaina 
da programación.

- Instalar o compilador
- Primeiros pasos no mundo da programación
- Compilar e...
- ✨Magic ✨

## Requisitos

- PC ou ordenador con conexión a Internet
- Ganas de aprender
- Seguir este tutorial

## Contidos explicados

Este tutorial vaise dividir en dúas partes, unha primeira orientada a instalar Ubuntu en 
Windows e unha segunda orientada a xerar o noso primeiro arquivo en C, compilalo e executalo.
Esta última vai ser conxunta, xa que van ser exactamente os mesmos pasos para ámbolos dous casos.

No caso de estar empregando unha distribución Linux podes saltar a parte na que se explica como se instala
Ubuntu en Windows, xa que a parte común e realmente importante é a final, onde se explica como programar un
pequeno programa moi básico, como se compila e como se executa.

## Windows 10

O primeiro paso é instalar a versión de Ubuntu escollida, no meu caso, e a día de hoxe, a última versión é a 
20.04. Para conseguila hai que ir a tenda de Windows, 'Microsoft Store' para descargar e instalar esta aplicación:

<!-- // Foto de Ubuntu na tenda -->
<p align="center"> <img src="https://raw.githubusercontent.com/HackingAllYT/configure-c-compiler/main/Imaxes/Ubuntu_2004_store.png"> </p>

A continuación recomendo instalar tamén a aplicación de 'Windows Terminal', tamén dispoñible na tenda de 
Microsoft.

<!-- // Foto de Windows Terminal na Tenda -->
<p align="center"> <img src="https://raw.githubusercontent.com/HackingAllYT/configure-c-compiler/main/Imaxes/Windows_Terminal_store.png"> </p>

O seguinte paso é activar WSL, é dicir, a plataforma de Microsoft Windows Subsystem for Linux, que ven sendo
paravirtualización do Sistema Operativo para integrar Windows con Ubuntu, permitindo entrar en tódolos arquivos
de Windows dende Linux e poder empregar ferramentas propias de Ubuntu.

Para activar o WSL é preciso abrir unha PowerShell con permisos de Administrador para executar o seguinte 
comando:

```sh
 Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

Unha vez executado este comando xa podemos abrir a aplicación de Ubuntu 20.04 para probar que todo funciona
correctamente e que non nos da erro ao abrir o programa. Se esto ocorre deberíamos obter unha saída parecida a esta:

<!-- // Foto de Ubuntu pedindo introducir o nome polo que queremos ser coñecidos -->
<p align="center"> <img src="https://raw.githubusercontent.com/HackingAllYT/configure-c-compiler/main/Imaxes/Ubuntu_installed.png"> </p>

É posible que teñamos que reiniciar o equipo para que estes cambios teñan efecto.

Neste momento temos que introducir o noso nome de usuario, un calquera, non ten porque ser o mesmo que o que temos
en Windows. Tamén temos que introducir o noso contrasinal, para executar certos comandos con certos privilexios. 
Como no caso do noso usuario o contrasinal pode ser calquera, non ten porque ser o mesmo que temos na nosa conta
de Outlook nin o PIN que podemos ter en Windows.

## Primeiros pasos 

Como comentei anteriormente C é unha linguaxe de programación moi importante e moi interesante. Nós ímolo a empregar
para achegarnos a este fermosos mundo da programación e poder ter unha idea de como se crean, compilan e executan 
os nosos programas, para esto imos empregar un dos editores de texto por excelencia de Ubuntu, Vi ou Vim, hai 
ambas versións, tamén se pode empregar nano.

Agora é o momento de iniciar a aplicación de Windows Terminal, darlle a flechiña para abaixo (ao lado do máis) e 
seleccionar Ubuntu, con esto abrirase unha terminal, exactamente igual que se abrimos unha nova instancia da aplicación
pero é mais sinxelo abrir novas e podemos empregar os atallos de teclado Ctrl + C e Ctrl + V para copiar e pegar
texto respectivamente.

Para movernos polos directorios (carpetas), emprégase o comando ```cd <carpeta>```, cambiando carpeta pola carpeta á
cal queremos entrar ou ```cd ..``` para regresar ao directorio anterior. Neste primeiro exemplo imos crear un novo
directorio co comando ```mkdir NovaCarpeta```, podedes cambiarlle o nome e poñer o que queirades. Unha vez creado
entramos no directorio deste xeito ```cd NovaCarpeta```.

Agora é o momento de crear o noso arquivo en C, para eso executamos o seguinte comando, que serve para crear un arquivo
en branco ```touch OlaMundo.c```. Se executades o comando ```cat OlaMundo.c```, comando que serve para mostrar por pantalla
o contido dun arquivo, non vos vai imprimir nada xa que está baleiro.

### Programación

Tendo o arquivo creado imos a acceder a el executando ```nano OlaMundo.c```, poderíamos escribir calquera cousa que quixéramos
e empregar o arquivo coma un ```.txt``` normal, pero esta non é a finalidade do tutorial, polo que imos a programar
o noso programita jejeje.

O noso programa vai ter dúas partes, a primeira de importación de librerías, e a segunda unha función denominada ```main```,
base de calquera aplicación desenvolta nesta linguaxe. Hai dous tipos de librerías principalmente, as creadas polo propio
programador e as que veñen ca linguaxe, para este primer tutorial imos empregar o segundo tipo.

As librerías impórtanse nas primeiras liñas de código do xeito seguinte ```#include <nomeLibreria.h>```, todas as librerías
teñen como extensión ```.h```, no noso caso imos importar a librería ```#include <studio.h>``` xa que para o noso caso é
máis que suficiente.

A seguinte parte do noso código é a función ```main```, única función do noso código que vai a conter todo o código para 
este primer tutorial. O código vai ser o máis sinxelo posible, polo que imos empregar unha das funcións que contén a 
librería que importamos previamente, a función ```printf```, esta serve para imprimir datos por pantalla dun xeito
bastante sinxelo e sin moitas complicacións.

## Código final

Xuntando os pequenos trazos explicados anteriormente chegamos a obter este pequeno trozo de código que ten unha única 
librería e unha única función con tres liñas de código, realmente son dúas xa que a liña que comeza por ```//``` é un
comentario, é dicir, non se executa e podemos escribir o que queiramos sen problemas. A primeira liña de código é unha
chamada á función encargada de imprimir por pantalla o texto que poñamos entre ```""```. A última liña é o fin do noso 
código, por convenio devólvese un ```0``` para indicar que non houbo erros durante a execución.

```c
#include <stdio.h>

int main() {
   // printf() displays the string inside quotation
   printf("Ola Mundo!\n");
   return 0;
}
```

## Compilar

Unha vez que programamos o noso código temos que compilalo para poder executalo e ver que tal funciona e que fai o noso
código, para esto o que hai que facer e acceder á carpeta na que temos o noso código, que se seguimos os pasos en orde
non faría falta xa que xa estaríamos no directorio onde se atopa o noso código. Ben é certo que esto non é extrictamente
preciso, pero para este tutorial é o máis apropiado.

Para a compilación imos a empregar o compilador por excelencia de linux, é dicir, o ```gcc```, GNU Compiler Collection,
que como ben di o seu nome realmente é un conxunto de compiladores, pero para o noso uso podémolo definir perfectamente
coma un só compilador. Para compilar tan só é preciso executar o seguinte comando:

```sh
gcc olaMundo.c -o olaMundo
```

Este comando o que vai facer é compilar o noso programa, ```olaMundo.c``` e gardalo nun arquivo executable ```olaMundo```,
o nome deste executable pode ser calquera que queirades, como se non o queredes poñer, tede en conta que se non especificades
un nome por defecto vai asignarlle ```a.out```.

## Executar

Chegados a este punto a execución é o máis sinxelo que imos facer, xa que só é preciso escribir un comando e xa poderíamos
ver por pantalla o noso saludo.

Se compilamos empregando o comando indicado previamente só tendes que escribir ```./olaMundo``` para que se execute, se pola
contra non lle puxéchedes nome ao executable tendes que poñer ```./a.out``` para executar, deberíades obter unha saída 
parecida a esta:

<!-- // Foto do código executado -->
<p align="center"> <img src=""> </p>

# Conclusións finais

Como puidéchedes ver a programación é un mundo moi completo e fermoso onde cada cousa encárgase dunha pequena tarefa
para que todo funcione á perfección.

Espero que quedárades con ganas de seguir aprendendo, calquera dúbida non dudedes en contactar conmigo.
Vémonos pronto!
