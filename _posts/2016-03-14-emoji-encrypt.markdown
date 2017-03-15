---
layout: post
title:  "Emoji Shifting Cipher"
subtitle:  "Javascript text to Emoji Encryption"
desc:  "Encryption/Decryption of Emoji strings."
date:   2015-03-14 18:26:33 +0000
categories: project html js
---
Whilst speaking to a group of friends we discussed the idea of sending encrypted messages in the form of Emojis. This lead to me implementing a basic encryption/decryption Javascript driven page using one of the simplest form of encryption, the cipher shift.

![]({{ site.url }}/assets/images/emoji_cipher.png)

```
<input id="input" />

<button onclick="encrypt()">Encrypt</button>
<button onclick="decrypt()">Decrypt</button>

<p id="demo"></p>

<script>
  function encrypt() {
    input = document.getElementById("input").value;
    if (input[0].toLowerCase() == "e") {
      var add = Math.floor((Math.random() * 90) + 10);
      input = input.substring(2);
      output = "E" + add + " ";
      for (i = 0; i < input.length; i++) {
        output += emoji[alphabet.indexOf(input[i]) + add] + " ";
      }
    }
    document.getElementById("demo").innerHTML = output;
  }

  function decrypt() {
    input = document.getElementById("input").value;
    if (input[0].toLowerCase() == "e") {
      var add = parseInt(input[1] + input[2]);
      input = input.substring(4);
      output = "E" + add + " ";
      var emote = input.split(" ");
      for (i = 0; i < emote.length; i++) {
        output += alphabet[emoji.indexOf(emote[i]) - add];
      }
    }
    document.getElementById("demo").innerHTML = output;
  }

  var alphabet = ["A", "B", "C", "D", "E", "F", "G", ... etc .. ];

  var emoji = [":egg:", ":earth_africa:", ":cd:", ":koko:", ":rage1:", ... etc ... ];

</script>

```
