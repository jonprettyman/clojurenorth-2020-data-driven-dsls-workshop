# grilles

`grilles` is a Clojure(script) library for defining a song in terms of its
structure and chords and generating different output representations including:
 * iRealPro style URLs for display or sharing with other musicians
 * generating an image
 * generating an ascii "grilles" chart

## Quick Start

```clojure

> (def minor-swing {
 :title "Minor Swing"
 :chorus [
   { :key 'A-'
     :measures ['A-' '%' 'D-' '%' 
                'E7' '%' 'A-' '%' 
                'D-' '%' 'A-' '%' 
                'Bb7' 'E7' 'A-' 'E7' }
 ]
})

> (grilles.ascii (minor-swing) )

Title: Minor Swing

Chorus: 
| A-  | %  | D- | % |
| E7  | %  | A- | % |
| D-  | %  | A- | % |
| Bb7 | E7 | A- | E7 |

```

## References

* [iRealPro URL Format](https://irealpro.com/ireal-pro-file-format/)
  Example: `{C |A- |D- |G7 }[C |A- |D- |G7 Z`
  As URL: `<a href="irealbook://Song Title=LastName FirstName=Style=Ab=n=T44*A{C^7 |A-7 |D-9 |G7#5 }">Song Title</a>`



## Limitations / Future Work

- A simple structure seemed to map quite simply over, not sure about a more
complex song.
- I think it would be a good approach to the problem.


