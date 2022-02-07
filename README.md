# regular-boric
_A RegEx exercise on replacing every name of every Chilean president to "Gabriel Boric Font" and its variations_

## wtf is this project even

IDK I got bored so I just thought of a prank on myself where all names of all Chilean presidents get replaced with the name of the incoming president [Gabriel Boric Font](https://en.wikipedia.org/wiki/Gabriel_Boric). This makes for an excruciatingly funny (or annoying) time reading about topics related to 🇨🇱 Chile. To illustrate the use of this project, consider this excerpt from the Wikipedia article on former president [Jorge Alessandri](https://en.wikipedia.org/wiki/Jorge_Alessandri): 

> Jorge Eduardo Alessandri Rodríguez (19 May 1896 – 31 August 1986) was the 27th President of Chile from 1958 to 1964, and was the candidate of the Chilean right in the crucial presidential election of 1970, which he lost to Salvador Allende. He was the son of Arturo Alessandri, who was president from 1920 to 1925 and again from 1932 to 1938. 

With this project, this whole quote turns into:

> Gabriel Boric Font (19 May 1896 – 31 August 1986) was the 27th President of Chile from 1958 to 1964, and was the candidate of the Chilean right in the crucial presidential election of 1970, which he lost to Gabriel Boric. He was the son of Gabriel Boric, who was president from 1920 to 1925 and again from 1932 to 1938. 

I had to learn RegEx for my job, so I thought this would be the perfect opportunity to pull off this prank on myself.

See my s\*\*tposts about this project on [my Twitter thread](https://twitter.com/olg6328/status/1486333775042977794).

## A primer on Spanish names

In order to understand what this project is trying to achieve, I need to explain first how Spanish names work.

People from most Spanish-speaking countries including Chile have two surnames. The first one comes from the father and the second one comes from the mother. If a couple named _Luis `Boric` Scarpa_ (father) and _María Soledad `Font` Aguilera_ (mother) would have a child named Gabriel, then Gabriel's complete name would be _Gabriel `Boric` `Font`_. 

This is an overview of how to refer to people whose names follow this naming convention: 

👍 Good: _Gabriel `Boric` `Font`_ 
* Usually used in formal contexts and official communication. 
* Some people are widely referred to by their first and second surnames, like [_Pedro `Aguirre` `Cerda`_](https://en.wikipedia.org/wiki/Pedro_Aguirre_Cerda). Some people call others by their first and second surnames as a matter of differentiating them from other people who share the same given name and first surname; an example is [_Eduardo `Frei` `Ruiz-Tagle`_](https://en.wikipedia.org/wiki/Eduardo_Frei_Ruiz-Tagle) and his father [_Eduardo `Frei` `Montalva`_](https://en.wikipedia.org/wiki/Eduardo_Frei_Montalva).

👍 Good: _Gabriel `Boric`_ 
* Used most often as a common name to match the Western naming convention of `GivenName Surname` and to make names more concise. 

👍 Good: _`Boric`_, _President `Boric`_ 
* In general, you can refer to people by their first surnames.

👎 Not Good: _Gabriel `Font`_, _`Font`_, _President `Font`_ 
* The second surname is not used alone to refer to people. This is a common mistake done by people who are unfamiliar with Spanish names upon reading full names like `Gabriel Boric Font`. 

## How it works

I set up a bunch of regular expressions (RegEx) that looks for name patterns. I used [RegExr](https://regexr.com/) to train myself and test my expressions.

I used the list of presidents of Chile from the website of the [Library of the Chilean National Congress (BCN)](https://www.bcn.cl/historiapolitica/presidentes_de_la_republica/index.html) as reference for the names the RegEx is replacing. I also looked up the full names of every president on [English](https://en.wikipedia.org/wiki/List_of_presidents_of_Chile) and [Spanish Wikipedia](https://es.wikipedia.org/wiki/Anexo:Presidentes_de_Chile).

The RegEx setup has five name patterns: 
1. G1S2S - given name + 1st surname + 2nd surname
   - Replaces the name with `Gabriel Boric Font` 
   - Intended for full names, including those with extra given names 
   - _Example:_ `Salvador Guillermo Allende Gossens` was a Chilean physician and politician.
   - _Replacement:_ `Gabriel Boric Font` was a Chilean physician and politician.
   - _Example:_ A statue dedicated to `Salvador Allende Gossens` can be found in Santiago.
   - _Replacement:_ A statue dedicated to `Gabriel Boric Font` can be found in Santiago.
2. G1S - given name + 1st surname
   - Replaces the name with `Gabriel Boric`
   - Intended for common names 
   - _Example:_ `Salvador Allende` ran for the presidency four times.
   - _Replacement:_ `Gabriel Boric` ran for the presidency four times.
3. 1S2S - 1st surname + 2nd surname
   - Replaces the name with `Boric Font`
   - Intended for some presidents who are known by their first and second surnames, without referring to their first name 
   - _Example:_ President `Barros Luco` has a sandwich named after him, the [`Barros Luco`](https://en.wikipedia.org/wiki/Barros_Luco).
   - _Replacement:_ President `Boric Font` has a sandwich named after him, the `Boric Font`.
4. 1S - 1st surname
   - Replaces the name with `Boric`
   - Intended when the president is referred to by their first surname 
   - _Example:_ After losing his previous three elections, `Allende` finally was elected president in 1970.
   - _Replacement:_ After losing his previous three elections, `Boric` finally was elected president in 1970.
5. 2S - 2nd surname
   - Replaces the name with `Font`
   - Intended for isolated instances of the second surname
   - _Example:_ In this Spanish name, the first or paternal surname is Allende and the second or maternal family name is `Gossens`.
   - _Replacement:_ In this Spanish name, the first or paternal surname is Boric and the second or maternal family name is `Font`.

## How to use

1. Install the Word Replacer II extension in your [Firefox](https://addons.mozilla.org/en-US/firefox/addon/word_replacer/) or [Chrome](https://chrome.google.com/webstore/detail/word-replacer-ii/djakfbefalbkkdgnhkkdiihelkjdpbfh) browser.
   - This is the only extension I know that supports RegEx statements. If you know of other extensions, please let me know!  
2. Once installed, click on the extension icon and open "Settings". 
   - You can enable and disable the extension (hence all replacements, including your existing ones) in this icon as well.
   - ![image](https://user-images.githubusercontent.com/99108307/152749830-80907c78-2930-402c-98cb-d9840c102d90.png)
3. Copy the contents of [regular-boric.json](/regular-boric.json) into the text box on the right side.
4. Click "Import". This will fill the left side with the replacement entries. Don't worry, these entries will add themselves after your existing replacement entries, so nothing will be overrided. 
   - ![image](https://user-images.githubusercontent.com/99108307/152755824-8f2cc93a-ed36-421e-9f17-d5600c1a93d4.png)
5. If the extension is enabled and all names of all presidents in the [BCN list](https://www.bcn.cl/historiapolitica/presidentes_de_la_republica/index.html) appear as `Gabriel Boric Font`, then congrats! The ~~chaotic~~ replacement entries are now ready.

## Known issues

### Pronouns

My replacement entries don't check for pronouns, so you will read something like "Her Excellency `Gabriel Boric`" when reading about Her Excellency [`Michelle Bachelet`](https://en.wikipedia.org/wiki/Michelle_Bachelet), the first (and so far only) Chilean president who uses she/her pronouns. 

### Pinochet and other questionable Chilean presidents

You will find some statements like "`Boric` dictatorship" when the webpage talks about the "[`Pinochet` dictatorship](https://en.wikipedia.org/wiki/Military_dictatorship_of_Chile_(1973%E2%80%931990))", which in my opinion is an offense against Boric. If you don't want this effect, you can disable or remove the replacement entries that check for [Augusto (José Ramón) Pinochet Ugarte](https://en.wikipedia.org/wiki/Augusto_Pinochet) and other questionable Chilean presidents. 

### Unintended replacements

1S and 2S patterns will replace any instance of a surname to `Boric` or `Font`, regardless of context, so it results to unintended replacements like "Puerto `Boric`" when referring to the city of "[Puerto `Montt`](https://en.wikipedia.org/wiki/Puerto_Montt)". If you're not reading about Chilean stuff, you might want to disable the replacement entries or Word Replacer II so that surnames don't get replaced.

### Testing limitations

I almost entirely tested my replacement entries on English Wikipedia, and I made these replacements with that website in mind. I haven't seen how the replacements integrate into Spanish texts.

### Word Replacer II limitations

Word Replacer II works across all active tabs. Currently, it doesn't support disabling or enabling it per website or per tab. 

⚠️ **If you want to remove my statements from your replacements list, it's a good idea to create a backup of your existing settings so that you don't lose your personal replacement entries!**

## Disclaimer

I'd be lying if I said I don't have any biases. Any explicit or implied views and opinions expressed in this project are strictly my own. 

I also admit that I created this project as someone who doesn't come from Chile, doesn't live in Chile, doesn't have any familial or non-familial relation with Chile, and only understands a bit of Spanish. I am just an outsider who got interested in Chilean stuff from my previous encounters in my previous job. I don't know a lot about Chile, including which of the presidents aside from Pinochet is questionable.

If the word replacements cause any unintended negative consequences, including insensitive text, please passive aggressively @ me here, on Discord (olg#6328) or on Twitter ([@olg6328](https://twitter.com/olg6328)), teach me a piece of Chilean history or culture, and I'll try my best to correct my project.

## This is too much text for what you call a "glorified s\*\*tpost"! Olg, do you really have that much time in your hands?! 

If I like whatever I'm doing, and more importantly if it makes me _learn_ something, then I tend to do a lot for it. This one is an example. 😉
