## ProseMirror

- About ProseMirror

[ProseMirror 사용기](https://leo.works/2004050)

- docs

[ProseMirror Docs](https://prosemirror.net/docs/)

### First Article - Quill VS ProseMirror

[두 에디터 이야기](https://jheo.io/blog/a-tales-of-two-editor/)

- Quill

에디터 내의 문서는 기본적으로 DOM 객체 형태로 다루어지면서도 조작이 필요할 때는 각 글자의 인덱스를 기준으로 글자를 추가하거나, 삭제하거나, 스타일을 변경하는 등의 동작을 수행.

장점 : API 명세가 깨끗하고 단순하게 정리됨. 일반적인 용도로 권장.

단점 : 확장하기 어렵다. 추가 기능, 커스텀이 쉽지않다.

- ProseMirror

장점 : 가장 상세한 문서 모델을 가지고 있었으며, 풍부한 생태계와 API를 보유

단점 : 문서 모델이나 UI의 처리에 DOM을 너무 적극적으로 활용 ⇒ 리액트, 캔버스와 통합이 어려울 수 있다.

- How to use in React?
1. react-prosemirror 와 같이 클래스 형태로 제공되는 컴포넌트를 사용하는 방식
2. Remirror나 Atalskit과 같이 ProseMirror를 이용하여 개발된 다른 에디터를 사용하는 방법

⇒ use-prosemirror

[use-prosemirror](https://www.npmjs.com/package/use-prosemirror)

### Second Article - 공식 문서 번역본

[](https://velog.io/@arais/ProseMirror-Guide-1)

- prosemirror-model

content를 묘사하는 자료구조

- prosemirror-state

state를 묘사하는 자료구조. selection 또는 transaction 시스템 포함.

- prosemirror-view

UI 컴포넌트를 구현. 유저와의 상호작용 핸들링

- prosemirror-transform

문서를 수정하는 기능. state 모듈의 transaction의 기반.

- transactions

사용자가 view와 상호작용시 state transactions 발생. 이는 document를 즉시 수정하는 것이 아니라 암시적으로 state를 업데이트한다. typing or interaction → transaction → change state → update view

- plugins

에디터 확장. keymap, history 등 다양하게 있음.

- commands

특별한 편집 행동을 지시한다.

prosemirror-commands 패키지는 enter와 delete와 같은 몇몇 기본 편집 단축키와 편집 command를 제공

- structure

Prosemirror에서 document는 트리의 노드 형태이다. 브라우저 DOM과 유사한 구조를 가지고 있다.

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d2c16fc5-a8b5-4515-9a47-0ef0dfa98e12/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221213%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221213T073955Z&X-Amz-Expires=86400&X-Amz-Signature=84d57d39d997c539e509c47cd9a931134074ece408ee5aed71dd99d8471ccfd6&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

## Prosemirror in React

[react prosemirror](https://codesandbox.io/s/t3num)

## Mdx

- Static Site Generator - Docusaurus

[개요 | Docusaurus](https://docusaurus.io/ko/docs)

- mdx docs

[Docs | MDX](https://mdxjs.com/docs/)

- CKeditor

[WYSIWYG HTML Editor with Collaborative Rich Text Editing](https://ckeditor.com/)