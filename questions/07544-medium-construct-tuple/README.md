<!--info-header-start--><h1>Construct Tuple <img src="https://img.shields.io/badge/-medium-d9901a" alt="medium"/> <img src="https://img.shields.io/badge/-%23tuple-999" alt="#tuple"/></h1><blockquote><p>by Lo <a href="https://github.com/LoTwT" target="_blank">@LoTwT</a></p></blockquote><p><a href="https://tsch.js.org/7544/play" target="_blank"><img src="https://img.shields.io/badge/-Take%20the%20Challenge-3178c6?logo=typescript&logoColor=white" alt="Take the Challenge"/></a> </p><!--info-header-end-->

Construct a tuple with a given length.

For example

```ts
type result = ConstructTuple<2> // expect to be [unknown, unkonwn]
```


<!--info-footer-start--><br><a href="../../README.md" target="_blank"><img src="https://img.shields.io/badge/-Back-grey" alt="Back"/></a> <a href="https://tsch.js.org/7544/answer" target="_blank"><img src="https://img.shields.io/badge/-Share%20your%20Solutions-teal" alt="Share your Solutions"/></a> <a href="https://tsch.js.org/7544/solutions" target="_blank"><img src="https://img.shields.io/badge/-Check%20out%20Solutions-de5a77?logo=awesome-lists&logoColor=white" alt="Check out Solutions"/></a> <!--info-footer-end-->

answer
```ts
type ConstructTuple<L extends number, A extends unknown[] = []> = A["length"] extends L ? A : ConstructTuple<L, [unknown, ...A]>;
```
