# _Teste com Imagens_

Nesse módulo foi testado como as imagens se comportam na aplicação.

## Logos e Icons:

Para a localização das imagens foi necessário criar um caminho relativo para a imagem em nosso `mkdocs.yml`, dessa forma:

```
theme:
    favicon: images/favicon.png
```

E para a logo o mesmo esquema:

```
theme:
    favicon: images/favicon.png
    logo: images/image_logo.svg
```

> Importante: ele não identifica imagens do tipo **".ico"**. A aplicação é renderizada porém a imagem é retornada como 404 (Not Found.)

## Imagens adicionais:

Para adicionar imagens a documentação, é utilizado as seguintes linhas:

```
    ![Texto "alt" da img](caminho/para/imagem.jpg)
```

Resultado:

![Minha imagem](images/teste_img1.png)

## Atributos para imagens:

No seu `mkdocs.yml`, você precisa adicionar um `attr_list` ao seu `markdown_extensions` explicitamente e o caminho para o seu arquivo css:

```
markdown_extensions:
  - attr_list

extra_css:
  - caminho/para/arquivo.css
```

No `Markdown` adicione a imagem e referencie uma tag para a imagem:

```
    ![Texto "alt" da img](caminho/para/imagem.jpg){ .tag-para-estilização-da-imagem }
```

No seu `css` adicione seus atributos a tag que você criou:

```
.tag-para-estilização-da-imagem {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 300px;
  border-radius: 18px;
}
```

Resultado:

![Minha imagem](images/teste_img1.png){ .img-estilizada }
