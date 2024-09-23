# YAML

- https://yaml.org/
- YAML(short for "YAML Ain't Markup Language") is a human-readable data serialization format. it's often used for configuration files, data exchange, and other applications where data needs to be represented in a structured way.

# YAML SYNTAX

- the basic structure of YAML is based on the use of indentation to indicate structure. This means that each level of structure is indented by a fixed number of spaces (usually 2 or 4). Here's an example of a YAML file that represents a simple shopping list:

```yaml
- Milk
- Bread
- Eggs
```

the hyphen symbol(-) is used to indicate a list item

```yaml
name: John Smith
age: 35
isMarried: true
favoriteFoods:
  - Pizza
  - Tacos
  - Sushi
birthdates: 1987-05-12
```

- the colon symbol(:) is used to seperate the key (the name of the data item) from the value (the data itself). The data types include a string (name), a number (age), a boolean (isMarried), a list (favoriteFoods), and a date (birthdate)

### Example

```yaml
person:
  name: John Smith
  age: 35
  isMarried: true
  favoriteFoods:
    - Pizza
    - Tacos
    - Sushi
  birthdates: 1987-05-12
```

=>

```json
{
  "person": {
    "name": "John Smith",
    "age": 35,
    "isMarried": true,
    "favoriteFoods": ["Pizza", "Tacos", "Sushi"],
    "birthdate": "1987-05-12"
  }
}
```
