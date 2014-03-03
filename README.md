# Critical Glossary Translation Project

This project is a translation for the [critical gaming
glossary](http://critical-gaming.com/critical-glossary/). It consists of
several parts: The language file that contains the structured
translation data, and the generator which is a small app that creates
output based on that structure. (Output can be html, epub, w/e)

## Current status

Translation: About ~2% (11/626) `HIGHLY UNSTABLE`

Output: No output yet.

## Translating

The current base document is being written in spanish. If you wish to
translate to your own language: fork, write your language file by
placing it in languages and calling it according to the [IETF
language](https://www.iana.org/assignments/language-subtag-registry/language-subtag-registry)
tag of your language.(eg. languages/fr.json or languages/sv.json), 
export, publish. Let us know so we can document all languages currently
being translated. An english port to the json format would also be welcome,
to make uniform output in several formats easy for any language.

Translation is open to everyone! :)

If you want to work in the spanish translation, please submit a pull
request. Try to work on words that aren't yet translated, unless you
feel one of the existing translations is lacking or misleading, in which
case you must justify the modifications.

The idea is to get a uniform and standard language to work with, so
constantly changing it is a big red light. However, many words that
may get lost in translation can be revised during the initial
translation, and this is OK. To help with this, the project will be
divided in these phases:

1. Highly Unstable (0-50% of translation): The body of work is changing a lot,
   all changes to translated words must be reviewed, but it's not a big
   deal.

2. Unstable (50%-75%): The body of work should still change, as
   discussions about its final shape are being held. However, changes to
   words, in particular those that are referenced most, should be
   justified more heavily

3. Stabilizing (75%-99%): The body of work is almost done, and we should
   strive for a stabilized language soon. Any changes to existing
   definitions should have very significant value to be approved.

4. Stable (100%): The glossary has been compiled fully, we don't expect
   existing words to change, and any change must be of highest value to
   justify a change.

Note that any words translated in the last 30 days are open for debate.
Once they have been in the dictionary for at least 30 days, they must be
reviewed more closely depending on the current state of the project (see
above.)

The date of addition is calculated by the time they are commited to the
project.

## The output generator

This isn't currently defined. Though something based on
[Cadmium](https://github.com/escusado/cadmium) is highly appealing. When
the project is `Highly Unstable`, this is very low priority, and it is
not recommended to approach this until we reach at least the `unstable`
level.

## The glossary file

The glosary file is a JSON object. For each entry in the glossary it has
one key, this key is the "slugified" version of the name in the original
glossary. This slug must be used when x-referencing from elsewhere. The
value of this key is an object with the following fields (Optional fields
are marked with †).

* term: The name of the term in the target language.
* definition: The definition in the target language. Use {{}}
* articles†: An array of articles. Articles are objects that have a
  `url` key, a `language` key, and a `title` key. The language key is to
  specify foreign language resources when relevant (eg. keep all english
  articles linked in the spanish version, but mark all non-spanish
  sources with [en] on export)
* source: A string with the textual source of definition. Not
  referenced (that's what articles is for).

## A project by SUTV

<div style="text-align: center">![U u
U](https://s3-us-west-2.amazonaws.com/droplr.storage/files/acc_94039/itv9?AWSAccessKeyId=AKIAJSVQN3Z4K7MT5U2A&Expires=1393877797&Signature=EZbG6zDSb2pWwgJJSUGxdr9J5kE%3D&response-content-disposition=inline%3B%20filename%3Dsutv.png%3B)
</div>

[El Sindicato](http://twitter.com/sndct_org)
