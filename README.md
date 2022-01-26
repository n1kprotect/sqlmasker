

# SqlMasker v. 1.0 [BETTA 2022]

**_установка_**

_Клонируем репозиторий_: `git clone https://github.com/n1kprotect/sqlmasker`
_Достаем файл sqlmasker.py и переносим в основную папку. Готово! _

**_инициализация движка_**

```
from sqlmasker import Sql

sql = Sql("my_database.db")
```

**_использование_**

```
from sqlmasker import Sql

sql = Sql("my_database.db")

sql.createTable(
  tableName='firstTable',
  values='(myname TEXT, myage BIGINT)',
  ifnotexists=True
  )
> {'created': True, 'ifNotExist': True}

def mydata(name=None, age=None):
  insert = sql.insertBlue(table='firstTable', values=['Nikita', '19'], count_=2)
  retutn insert

if __name__ == '__main__':
  mydata(name=input('Имя: '), age=input('Возраст: ))


```
