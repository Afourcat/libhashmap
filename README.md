## Lib HashMap

It's a multi purpose lightweig hasmap libray written in C, for C developers.

Feel free to contribute, star and fork.

---

### Installation

To install the lib on linux, clone the repo and make the project or use the binary given in the release section.

---

### Changelog

* v1.0

  Initial release

* v1.1

  Removed hashmap_hash from exposed functions.

  Added hashmap_free to functions.

---

### Usage

This library has, (at the v1.0) 4 functions :

```
int hashmap_has(struct hashmap *map, const char *key);
int hashmap_del(struct hashmap **map, const char *key, void (*fr)(void *));
int hashmap_add(struct hashmap **map, const char *key, void *data);
void *hashmap_get(struct hashmap *map, const char *key);
void hashmap_free(struct hashmap *map, void (*free_it)(void *));
```

This functions helps you manage your Hashmap all way along.

---

##### HASHMAP_HAS

This simple function takes in a map and a key in parameter.

it will search for the occurence of the key in the hashmap and return 1 if it exists, 0 ortherwise.

---

##### HASHMAP_DEL

This simple function takes in a map and a key in parameter.

it will destroy the element specified by key in the hashmap and return 0 in case of success, 1 ortherwise.

---

##### HASHMAP_ADD

This simple function takes in a map, a key and a data in parameter.

It will save the data using the key as the way to get it with the next function.

---

### HASHMAP_GET

This simple function takes in a map and a key in parameter.

it will get the (void *) pointer on the data given the key it was added before with.

---

### HASHMAP_FREE

This simple function takes in a map and a function pointer in parameter.

it will free the hashmap using the function pointer on data.

---


### Credits

Thomas "nwmqpa" Nicollet for authoring the library.
Alexandre "afourcat" Fourcat for authoring the Makefile
