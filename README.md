# Smart Contracts workshop at Nerdear.la

Contratos ejemplo para [nerdear.la 2017](https://nerdear.la)

## Requerimientos
[nodo parity](https://github.com/paritytech/parity)

## Correr Partity en modo DEV

Correr parity desde el Docker Compose file incluido:

`docker-compose up -d`

Si instalamos Parity localmente, ejecutarlo con los siguientes parametros

`parity --chain dev`

## Crear un usuario etherllonario

Una vez que estamos corriendo Parity, entrar en su [interface grafica](http://127.0.0.1:8180) local,
aceptar la licencia y crear una cuenta inicial que tendrá saldo 0.

Vamos a Accounts, creamos una cuenta nueva, seleccionamos 'Recovery Passphase', y en el paso siguiente
dejamos el recovery passphase vacio, ponemos un nombre y un password para la cuenta, y listo:
tenemos una cuenta con 1,606,938,044,258,990,275,541,962,092,341,162,602,522,202.994 Ether

Finalmente en la parte de accounts borrar la cuenta inicial con 0 Ether

## Contratos basicos:

*hello_word.sol*   : Autodescriptivo

*mortal_hello.sol* : Creamos un contrato base que nos permite borrar (kill) el contrato del blockchain, y el hello_world hereda del mismo. Tambien introducimos `Event` para ver los cambios en la variable de string

*users.sol*     : Introducimos varios tipos de datos: struct, mapping, arrays.

*nerdearla.sol* : Ejemplo de creacion de un token con symbol *NERD*. Es un [ERC20](https://theethereum.wiki/w/index.php/ERC20_Token_Standard) reducido

*nerdearla.v2*  : El token ahora puede cambiar de dueño y podemos emitir mas NERDS (minting)


## Resources
[solidity](https://solidity.readthedocs.io/en/latest/index.html)

[truffle framework](http://truffleframework.com/)

[testrpc](https://github.com/ethereumjs/testrpc)

[openzeppelin](https://github.com/OpenZeppelin/zeppelin-solidity)
