### Creating Dummy List
- `List<Integer> integerList = List.of(1, 2, 3, 4);` fixed sized list.
- `List<String> stringList = Arrays.asList("a", "b", "c");` fixed sized list.
- `List<String> test = new ArrayList<>();` and `Collections.addAll(test,"Salih","Veli","Ahmet");` **not fixed sized** list.
- `List<String> test = new ArrayList<>();` and `test.addAll(List.of("Salih","Veli","Ahmet"));` **not fixed sized** list.
- `test.set(2,"sait");` --> **Replaces** the element at **the specified position** in this list with the specified element (optional operation).
- `test.removeIf(item->item.equals("sait"));` **-->** Removes all of the elements of this collection that **satisfy the given predicate.**
- `private final String id;` **and** `UUID.randomUUID().toString()` **-->** Generate random ID.
- Introduce local variable in IntelliJ Idea `alt + Enter`


