# Longest Common Prefix

A simple Java program that finds the longest common prefix shared by an array of strings.

## Description

The `longestcommonprefix(String[] words)` function takes an array of strings and returns the longest prefix that every string in the array starts with. If there is no common prefix, it returns an empty string.

The algorithm works as follows:

- start with the first word as the candidate prefix,
- for each following word, shorten the prefix one character at a time until the word starts with it,
- if the prefix becomes empty, return `""` immediately,
- after all words are checked, return the remaining prefix.

## Requirements

- Java 25 or newer (the program uses unnamed classes, instance main methods, and `IO.println`)

## Usage

```bash
java Main.java
```

## Example

```java
String[] some_words = {"flower", "flow", "flight"};
IO.println(longestcommonprefix(some_words));
```

Output:

```
fl
```

Other cases:

| Input                          | Output   |
|--------------------------------|----------|
| `{"flower", "flow", "flight"}` | `"fl"`   |
| `{"dog", "racecar", "car"}`    | `""`     |
| `{"test"}`                     | `"test"` |
| `{}`                           | `""`     |

## Complexity

- Time: **O(S)**, where *S* is the total number of characters across all strings
- Space: **O(1)** extra space (besides the returned prefix)

## Limitations

- The array must not contain `null` elements (this would cause a `NullPointerException`).
- Matching is case-sensitive.

## License

This project is provided for educational purposes.
