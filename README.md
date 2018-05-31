mongoladdu
----------

## How to install

* use `pip`

    ```bash
    $ pip install mongoladdu
    ```

* from source code

    ```bash
    $ python setup.py install
    ```

## How to use it

1. create folder named `migrations`
2. create `config.yml` file with in `migrations` folder and place your environment specific configurations

```yml
dev:
  host: localhost
  port: 27017
  db_name: dev_db
```

3. create migration scripts with in `migrations` folder. file names should follow patter `<index>_<description>.py`

```python
def run(db):
    db.Test.insert({'name': 'value'})
```

4. run migrate `mongoladdu <env> run`

```console
mongoladdu dev run
```


