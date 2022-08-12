Caesars Cipher

One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.

A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus A ↔ N, B ↔ O and so on.

```js
function rot13(str) {
 let strAm = "ABCDEFGHIJKLMNOPQRSTUVWXYZ -_.&?!@ #/";
let strNz = "NOPQRSTUVWXYZABCDEFGHIJKLM -_.&?!@ #/";
  let rot13 = '';
  for (let i = 0; i < str.length; i++){
    if (strAm.includes(str.charAt(i))){
      rot13 += str.charAt(i).replace(str.charAt(i), strNz[strAm.indexOf(str.charAt(i))]);
    }
  }
  return rot13;
}
```

```js
rot13("SERR PBQR PNZC");
```
