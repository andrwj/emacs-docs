---
slug: Lisp-Data-Types
---

Lisp *객체*는 Lisp 프로그램에서 사용하고 조작하는 데이터 일부분입니다. 여기서 말하는 *유형(type)* 또는 *데이터 유형(data type)*은 가능한 객체의 집합을 뜻합니다.

모든 객체는 적어도 하나의 유형에 속합니다. 같은 유형의 객체는 구조가 비슷하며 일반적으로 같은 컨텍스트에서 사용될 수 있습니다. 유형은 겹칠 수 있으며 객체는 두 개 이상의 유형에 속할 수 있습니다. 따라서 객체가 특정 타입에 속하는지는 질의할 수 있지만 객체 *자체*의 유형에 대해서는 질의할 수 없습니다.

이맥스에는 몇 가지 기본적인 객체 유형이 내장되어 있습니다. 다른 모든 유형을 구성하는 이러한 타입을 *기본 유형(primitive types)*이라고 합니다. 각 객체는 단 하나의 기본 유형에만 속합니다. 이러한 유형에는 *정수(integer)*, *부동 소수점(float)*, *cons*, *기호(symbol)*, *문자열(string)*, *벡터(vector)*, *해시 테이블(hash-table)*, *subr*, *바이트 코드 함수(byte-code function)* 및 *레코드(record)*와 편집과 관련된 *버퍼(buffer)*와 같은 몇 가지 특수 유형이 포함됩니다. ([편집 유형](/docs/elisp/Editing-Types) 참조).

각 기본 타입에는 객체가 해당 타입의 멤버인지 여부를 확인하는 특정 Lisp 함수가 있습니다.

Lisp는 다른 많은 언어와 달리 객체가 *스스로 유형을 결정한다 (self-typing)* 라는 점에서 다릅니다. 각 객체의 기본 유형은 객체 자체에 암시되어 있습니다. 예를 들어, 객체가 벡터인 경우 그 어떤 것도 이를 숫자로 취급할 수 없으며 Lisp는 이를 숫자가 아닌 벡터라는 것을 알고 있습니다.

대부분의 언어에서 프로그래머는 각 변수의 데이터 유형을 선언해야 하며, 컴파일러는 해당 유형을 알고 있지만 데이터에는 표시되지 않습니다. 이러한 유형 선언은 Emacs Lisp에는 존재하지 않습니다. Lisp 변수는 모든 유형의 값을 가질 수 있으며 변수에 저장하는 모든 값, 유형 등을 기억합니다. (사실, 소수의 Emacs Lisp 변수는 특정 유형의 값만 사용할 수 있습니다. [제한된 값을 가진 변수](/docs/elisp/Variables-with-Restricted-Values) 참조).

이 장에서는 GNU Emacs Lisp의 각 표준 유형의 목적, 인쇄된 표현 및 읽기 구문에 대해 설명합니다. 이러한 형을 사용하는 방법에 대한 자세한 내용은 이후 장에서 확인할 수 있습니다.

|                                                                |    |                                            |
| :------------------------------------------------------------- | -- | :----------------------------------------- |
| • [Printed Representation](/docs/elisp/Printed-Representation) |    | How Lisp objects are represented as text.  |
| • [Special Read Syntax](/docs/elisp/Special-Read-Syntax)       |    | An overview of all the special sequences.  |
| • [Comments](/docs/elisp/Comments)                             |    | Comments and their formatting conventions. |
| • [Programming Types](/docs/elisp/Programming-Types)           |    | Types found in all Lisp systems.           |
| • [Editing Types](/docs/elisp/Editing-Types)                   |    | Types specific to Emacs.                   |
| • [Circular Objects](/docs/elisp/Circular-Objects)             |    | Read syntax for circular structure.        |
| • [Type Predicates](/docs/elisp/Type-Predicates)               |    | Tests related to types.                    |
| • [Equality Predicates](/docs/elisp/Equality-Predicates)       |    | Tests of equality between any two objects. |
| • [Mutability](/docs/elisp/Mutability)                         |    | Some objects should not be modified.       |
