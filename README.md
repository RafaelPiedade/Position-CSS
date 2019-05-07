# Display

## Inline

- Faz com que os elemento fiquem um do lado do outro;
- O elemento não aceita `width` e `height`;
- Seu tamanho é definido pelo contúdo que ele comtém.
- Ganha `comportamento de palavra`, isto é o enter que existe entre os elemento ganham empaçono browser;
- Já que seu comportamento é de palavra, o esilo `text-align` funciona para o alinhamento.

```
<ul>
    <li class="inline">Primeiro</li>
    <li class="inline">Segundo</li>
    <li class="inline">Terceiro</li>
</ul>
// Exibição
Primeiro Segundo Terceiro

Pode ser resolvido com comentario, ou tudo na mesma linha
<ul>
       <li class="inline">Primeiro</li><!-- 
    --><li class="inline">Segundo</li><!-- 
    --><li class="inline">Terceiro</li>
</ul>
//Exibição
PrimeiroSegundoTerceiro
```

## Block
- Os elemento aceitão `width` e `height`;
- O elemento ocupa a linha inteira, outros elementos são colocados abaixo;
- Para posicionar o elemento em sua linha usamos a propriedade `margin`
```
<ul>
    <li class="block first">Primeiro</li>
    <li class="block second">Segundo</li>
    <li class="block third">Terceiro</li>
</ul>
// inicialmente todos estão do lado esquerdo, um abaixo do outro

//Posicionar no máximo do lado direito
.first{margin-left:auto;}

//posiciona no máximo do lado esquerdo
.second{margin-rigth:auto;}

// posiciona no centro
.third{margin-left:auto; margin-rigth:auto}

// quando AUTO ele ira calcular o tamanho da margin independente se mudar o tamanho do elemento;
```

## Inline-Block
- O elemento aceitão `width` e `height`;
- Um elemento do lado do outro, mesma linha;
- ganha o `comportamento de palavra`;
    - `text-align:justify`, justifica as palavras da linha exeto a ultima linha;

```
No exemplo adicionamos um elemento vazio para que ele oculpasse a ultima linha e usamos justify apara alinha aa <li>
OBS: o justify estava na <ul>
```
