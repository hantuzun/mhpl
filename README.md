# mhpl

MHPL is an experimental programming language written in Cuneiform and transpiled to Clojure.

## Examples

### Hello World
```clojure
(𒍑 "Hello, world!")
```

#### Transpiled Clojure Code
```clojure
(println "Hello, world!")
```

#### Output
```
Hello, world!
```

### Counting the Characters of a String
```clojure

(𒂋 s "Hello, World!")

(𒍑 (𒁺 "The string '" s "' has " (𒁺 (𒌨 s)) " characters!")
```

#### Transpiled Clojure Code
```clojure
(def s "Hello, World!")

(println (str "The string '" s "' has " (str (count s)) " characters!")
```

#### Output
```
The string 'Hello, World!' has 13 characters!
```

## How Is It Developed?

We've just replaced the English keywords in Clojure with Cuneiform counterparts. The following design decisions are made:
 * Cuneiforms are picked based on their legibility and unique looks rather than their meanings.
 * The Clojure characters such as parantheses and dashs are kept.
 * Arabic numerals are kept.

### mhpl.js
```clojure
(use 'clojure.contrib.def)

(defalias 𒊓 ns)
(defalias 𒂋 def)
(defalias 𒂊 defn)
(defalias 𒂊- defn-)
(defalias 𒈪 fn)
(defalias 𒈪? fn?)
(defalias 𒈬 print)
(defalias 𒈭 printf)
(defalias 𒍑 println)
(defalias 𒁺 str)
(defalias 𒌨 count)
```

The latest version could be found at: [mhpl.clj](mhpl.clj).

### Clojure Keywords
Clojure 1.11 has 648 keywords: [clojure_core_keywords.txt](clojure_core_keywords.txt). These have 454 unique words: [clojure_core_unique_words.txt](clojure_core_unique_words.txt).

Source: https://clojure.github.io/clojure/clojure.core-api.html#clojure.core/defmacro

### Unicode Cuneiform Characters
There're 922 Sumero-Akkadian Cuneiform script characters in Unicode version 15.0. The list is available on: [cuneiform_unicode_characters.txt](cuneiform_unicode_characters.txt).

## Version
This alpha version is transpiled to Clojure 1.11. This language should not be used for mission critical software, especially for fighter jets.

## The MIT License (MIT)
Copyright © 2023 Han Tuzun

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
