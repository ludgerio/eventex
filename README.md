# Eventex

Sistema de Eventos encomendado pela Morena.

## Como desenvolver?

1. Clone o repositorio.
2. Crie um virtualenv com Python 3.6.5
3. Ative o virtualenv.
4. Instale as dependencias.
5. Configure a instancia com o .env
6. Execute os testes.

```console
git clone git@github.com:ludgerioneto/eventex.git wttd
cd wttd
python -m env .wttd
source .wttd/bin/activate
pip install -r requirements.txt
cp contrib/env-sample .env
python manage.py test
```

## Como fazer o deploy?

1. Crie uma instancia no heroku.
2. Envie as configuracoes para o heroku.
3. Define uma SECRET_KEY segura para a instancia.
4. Defina DEBUG=False
5. Configure o servidor de email.
6. Envie o codigo para o heroku.

```console
heroku create minha instancia
heroku config:push
heroku congig:set SECRET_KEY=`python contrib/secret_gen.py`
heroku config:set DEBUG=False
#configuro o emial
git push heroku master --force
```
