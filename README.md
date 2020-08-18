# 75.06 - Página de la materia

## Sobre el sitio
El sitio junta toda la información relativa a la materia. Links, calendario, info de cursada, etc

## Jekyll
Para levantar el sitio estático, estamos usando el tema [Prologue](https://github.com/chrisbobbe/jekyll-theme-prologue) de [Jekyll](https://jekyllrb.com).

### Levantarlo localmente
Si usás Linux, lo mas probable es que tengas Ruby instalado, pero es una buena idea usar [rvm](https://rvm.io) para manejar tus entornos de Ruby.

```bash
curl -sSL https://rvm.io/mpapis.asc | gpg2 --import -
curl -sSL https://rvm.io/pkuczynski.asc | gpg2 --import -
curl -L get.rvm.io | bash -s stable
echo 'source ~/.rvm/scripts/rvm' >> ~/.bashrc
source ~/.bashrc
rvm install 2.7.0
rvm --default use 2.7.0
```

Luego de eso, podés instalar las gemas.

```bash
gem install bundler
bundle install
```

Y finalmente para levantar el sitio:

```bash
bundle exec jekyll build
bundle exec jekyll serve --incremental
```

### En github pages
Se despliega solo desde el branch principal.
