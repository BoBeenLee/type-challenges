<!--info-header-start--><h1>Number Range <img src="https://img.shields.io/badge/-medium-d9901a" alt="medium"/> </h1><blockquote><p>by AaronGuo <a href="https://github.com/HongxuanG" target="_blank">@HongxuanG</a></p></blockquote><p><a href="https://tsch.js.org/8640/play" target="_blank"><img src="https://img.shields.io/badge/-Take%20the%20Challenge-3178c6?logo=typescript&logoColor=white" alt="Take the Challenge"/></a> </p><!--info-header-end-->

Sometimes we want to limit the range of numbers...
For examples.
```
type result = NumberRange<2 , 9> //  | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 
```
answer

```ts
type NumberRange<L, H, A extends unknown[] = [], S extends boolean = false, E extends boolean = false, R extends number[] = []> = A["length"] extends L ? NumberRangeArr<L, H, [unknown,...A], true, false, [...R, A["length"]]> : 
  A["length"] extends H ? [...R, A["length"]][number] : 
  S extends true ? NumberRangeArr<L, H, [unknown,...A], S, E, [...R, A["length"]]> : E extends true ? R : NumberRangeArr<L, H, [unknown,...A], S, E, R>;

```
- 확인 필요

<!--info-footer-start--><br><a href="../../README.md" target="_blank"><img src="https://img.shields.io/badge/-Back-grey" alt="Back"/></a> <a href="https://tsch.js.org/8640/answer" target="_blank"><img src="https://img.shields.io/badge/-Share%20your%20Solutions-teal" alt="Share your Solutions"/></a> <a href="https://tsch.js.org/8640/solutions" target="_blank"><img src="https://img.shields.io/badge/-Check%20out%20Solutions-de5a77?logo=awesome-lists&logoColor=white" alt="Check out Solutions"/></a> <!--info-footer-end-->
