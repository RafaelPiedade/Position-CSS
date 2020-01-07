# Display

## Inline
//(texto para textar git pull em outro pojeto)
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


## Float

- Quando aplicado com valores `right` e `left`, o elemento recebe um novo contexto. Logo em seguida ele é posicionado nesse novo contexto o máximo que ele conseguir para o sentido que foi passado para a prorpriedade `float`;
- `novo contexto` - é uma nova camada que fica acima da camada de origem do elemento. Contudo, se você tiver 4 elementos utilizando a propriedade `float`, não é criado um novo contexto para cada um. Os 4 elementos utilizam o mesmo contexto.
- Toda vez que tivermos um `<img>` ou um elemento definido como `display:inline` ou `display:inline-block` após qualquer tag definida com a propriedade `float:left` ou `right`, esses elementos se encaixam ao lado do elemeneto que está flutuando. Se não couber ao lado, ele fica embaixo do elemento que contém a propriedade `float`.
- Apesar do display do `<p>` ser `block`, o `display` de qualquer texto é `inline`, portanto o texto não fica embaixo do elemento que está flutuando e sim ao lado.
- Quando o elemento ganha um novo contexto, não estando mais no contexto do pai, alterando o tamanho do pai;
### Overflow
- `overflow` com valor `hidden`, tem o poder de esconder qualquer elemento filho que ultrapasse o tamanho do pai. Mas  quando o pai não tem um largura ou altura definida, ele se preocupa em levar em consideração a altura e largura dos filho, ainda que estejam no novo contexto.

### Clear
- A propriedade `clear` é utilizada para limpar o contexto caso tenha um elemento flutuando ao lado esquerdo (`left`), direito (`right`) ou ambos (`both`).
