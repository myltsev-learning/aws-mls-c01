SSML stands for Speech Synthesis Markup Language. Think of SSML tags as special instructions you mix in with your text to tell [[entities/aws/Amazon Polly|Amazon Polly]] how to handle different parts of your text. Here's one of the most useful tags for pronunciation:

```xml
<speak>
	I <phoneme alphabet="ipa" ph="rɛd">read</phoneme>
	a great book yesterday.
</speak>
```

SSML offers many other tags for controlling aspects like emphasis, pauses, and more.

#entity 