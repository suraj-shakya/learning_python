# JSON in Python
---
- JavaScript Object Notation (JSON)
- JSON is a syntax for storing and exchanging data.
- is text, written with JavaScript object notation.  

JSON supports mainly 6 data types:

- string
- number
- boolean
- null
- object
- array

## JSON in Python
---
Python has a built-in package called ```json```, which can be used to work with JSON data.

```
# import json package
import json
```



### Convert JSON to Python
---
```json.loads()``` method allow us to convert JSON String to python object( Python dictionary ).



```python
import json 
# same JSON:

json_data = '''{
                "name": "Falano",
                "age" : 20,
                "gender": "Male",
                "address": "Manang"
}'''

print("json_data type : ",type(json_data))

# parse json
python_object = json.loads(json_data)
print("python_object type : ",type(python_object))
print(python_object)
print(python_object["name"])
```

    json_data type :  <class 'str'>
    python_object type :  <class 'dict'>
    {'name': 'Falano', 'age': 20, 'gender': 'Male', 'address': 'Manang'}
    Falano
    

### Convert from Python Object to JSON
```json.dumps()``` can be used to convert Python Object to JSON



```python
json_dump = json.dumps(python_object)
print(json_dump)
print(type(json_dump))
```

    {"name": "Falano", "age": 20, "gender": "Male", "address": "Manang"}
    <class 'str'>
    


```python
str = '[{"a":"b"},{"b":[1,2,3,4,4]},{"c":true}]'
pyt = json.loads(str)
type(pyt)
```




    list



Following type of python object can be converted into JSON Strings:
- dict
- list
- tuple
- string
- int
- float
- True
- False
- None


```python
#Example:
import json

# json file downloaded from https://raw.githubusercontent.com/matthewreagan/WebstersEnglishDictionary/master/dictionary.json
# load the json data into python object
json_dictionary = dict()
with open("dictionary.json") as dictionary_file:
    json_dictionary = json.load(dictionary_file)
    
# get input from the user    
in_word = input("Search meaning of word : ")
print(json_dictionary[in_word.lower()])

#difflib-> get_close_matches

```

    Search meaning of word : bottle
    1. A hollow vessel, usually of glass or earthenware (but formerly of leather), with a narrow neck or mouth, for holding liquids. 2. The contents of a bottle; as much as a bottle contains; as, to drink a bottle of wine. 3. Fig.: Intoxicating liquor; as, to drown one's reason in the bottle. Note: Bottle is much used adjectively, or as the first part of a compound. Bottle ale, bottled ale. [Obs.] Shak. -- Bottle brush, a cylindrical brush for cleansing the interior of bottles. -- Bottle fish (ZoÃ¶l.), a kind of deep-sea eel (Saccopharynx ampullaceus), remarkable for its baglike gullet, which enables it to swallow fishes two or three times its won size. -- Bottle flower. (Bot.) Same as Bluebottle. -- Bottle glass, a coarse, green glass, used in the manufacture of bottles. Ure. -- Bottle gourd (Bot.), the common gourd or calabash (Lagenaria Vulgaris), whose shell is used for bottles, dippers, etc. -- Bottle grass (Bot.), a nutritious fodder grass (Setaria glauca and S. viridis); -- called also foxtail, and green foxtail. -- Bottle tit (ZoÃ¶l.), the European long-tailed titmouse; -- so called from the shape of its nest. -- Bottle tree (Bot.), an Australian tree (Sterculia rupestris), with a bottle-shaped, or greatly swollen, trunk. -- Feeding bottle, Nursing bottle, a bottle with a rubber nipple (generally with an intervening tubve), used in feeding infants.
    
    To put into bottles; to inclose in, or as in, a bottle or bottles; to keep or restrain as in a bottle; as, to bottle wine or porter; to bottle up one's wrath.
    
    A bundle, esp. of hay. [Obs. or Prov. Eng.] Chaucer. Shak.
    


```python

```
