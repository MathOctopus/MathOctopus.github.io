---
layout: default
---

<!-- Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project. -->
# **Introduction**
<p style="color: black; text-align:justify; text-justify:inter-ideograph;">
This work pioneers exploring and building powerful Multilingual Math Reasoning (xMR) LLMs. To accomplish this, we make the following works:
</p>
*   <p style="color: black; text-align:justify; text-justify:inter-ideograph;">
    <strong>MGSM8KInstruct</strong>, the first multilingual math reasoning instruction dataset, encompassing ten distinct languages, thus addressing the issue of training data scarcity in xMR tasks.</p>
*   <p style="color: black; text-align:justify; text-justify:inter-ideograph;">
    <strong>MSVAMP</strong>, an out-of-domain xMR test dataset, to conduct a more exhaustive and comprehensive evaluation of the model’s multilingual mathematical capabilities.</p>
*   <p style="color: black; text-align:justify; text-justify:inter-ideograph;">
    <strong>MathOctopus</strong>, our effective Multilingual Math Reasoning LLMs, training with different strategies, which notably outperform conventional open-source LLMs and exhibit superiority over ChatGPT in few-shot scenarios.</p>


![xmath](/XMATH_MODEL_00.jpg)
## **MGSM8KInstruct**

| Training Dataset      | En      | Sw      | Zh      | Bn      | De      | Es      | Fr      | Ja      | Ru      | Th      | Overall |
|:----------------------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|
| MGSM8KInstruct        | 7473    | 7472    | 7466    | 6539    | 7466    | 7470    | 7469    | 7471    | 7361    | 7473    | **73.6K**   |

## **MSVAMP**

| Test Dataset      | En      | Sw      | Zh      | Bn      | De      | Es      | Fr      | Ja      | Ru      | Th      | Overall |
|:----------------------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|
| MSVAMP                | 1000    | 1000    | 1000    | 1000    | 1000    | 1000    | 1000    | 1000    | 1000    | 1000    | **10K**   |


## **Overall Results on MGSM**

| 7B Model                        | En      | Sw      | Zh      | Bn      | De      | Es      | Fr      | Ja      | Ru      | Th      | Overall |
|:--------------------------------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|
| MathOctupos<sup>C</sup>         | 52.0    | 23.6    | 31.6    | 18.8    | 38.0    | 39.2    | 36.4    | 27.2    | 33.6    | 21.6    | 32.2    |
| **xRFT**-MathOctupos<sup>C</sup>| 51.2    | 24.0    | 33.2    | 18.8    | 36.0    | 41.2    | 37.6    | 29.6    | 36.4    | 25.2    | 33.3    |
| MathOctupos<sup>P</sup>-LoRA    | 30.4    | 15.2    | 23.6    | 10.4    | 22.8    | 24.8    | 26.4    | 18.0    | 22.0    | 14.8    | 20.8    |
| MathOctupos<sup>P</sup>         | 52.4    | 39.2    | 38.4    | 28.8    | 44.8    | 42.4    | 43.6    | 36.0    | 39.6    | 34.4    | 40.0    |
| **xRFT**-MathOctupos<sup>P</sup>| 54.8    | 38.4    | 45.2    | 33.2    | 43.6    | 45.2    | 38.0    | 35.6    | 48.4    | 36.4    | 41.9    |

<p></p>

| 13B Model                       | En      | Sw      | Zh      | Bn      | De      | Es      | Fr      | Ja      | Ru      | Th      | Overall |
|:--------------------------------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|
| MathOctupos<sup>C</sup>         | 56.4    | 27.2    | 39.2    | 24.0    | 47.6    | 49.6    | 47.6    | 40.4    | 42.0    | 24.8    | 39.9    |
| **xRFT**-MathOctupos<sup>C</sup>| 53.6    | 28.0    | 45.2    | 21.2    | 48.0    | 46.4    | 46.0    | 35.2    | 45.6    | 28.8    | 39.8    |
| MathOctupos<sup>P</sup>         | 53.2    | 42.8    | 48.8    | 35.2    | 44.4    | 48.0    | 48.4    | 43.2    | 47.6    | 46.8    | 45.8    |
| **xRFT**-MathOctupos<sup>P</sup>| 51.6    | 46.0    | 51.2    | 42.0    | 49.2    | 53.2    | 49.6    | 39.6    | 47.6    | 46.0    | 47.6    |

<p></p>

| 30-34B Model                    | En      | Sw      | Zh      | Bn      | De      | Es      | Fr      | Ja      | Ru      | Th      | Overall |
|:--------------------------------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|
| MathOctupos<sup>C</sup>         | 55.6    | 24.4    | 36.0    | 19.2    | 40.4    | 51.2    | 44.4    | 27.2    | 37.2    | 21.6    | 35.7    |
| **xRFT**-MathOctupos<sup>C</sup>| 53.6    | 27.6    | 34.4    | 19.2    | 47.2    | 47.6    | 44.8    | 30.8    | 38.8    | 22.8    | 36.7    |
| MathOctupos<sup>P</sup>         | 56.4    | 46.8    | 52.0    | 35.2    | 47.2    | 53.2    | 48.0    | 39.2    | 45.6    | 41.2    | 46.5    |
| **xRFT**-MathOctupos<sup>P</sup>| 51.6    | 47.2    | 52.4    | 37.6    | 51.2    | 52.8    | 44.4    | 41.6    | 50.0    | 47.6    | 47.6    |

## **Overall Results on MSVAMP**

| 7B Model                        | En      | Sw      | Zh      | Bn      | De      | Es      | Fr      | Ja      | Ru      | Th      | Overall |
|:--------------------------------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|
| MathOctupos<sup>C</sup>         | 49.2    | 36.6    | 43.6    | 30.2    | 48.6    | 46.8    | 46.4    | 42.5    | 46.7    | 34.0    | 42.5    |
| **xRFT**-MathOctupos<sup>C</sup>| 49.9    | 37.7    | 43.3    | 32.9    | 46.5    | 47.6    | 47.3    | 42.7    | 46.6    | 36.2    | 43.1    |
| MathOctupos<sup>P</sup>-LoRA    | 30.4    | 15.2    | 23.6    | 10.4    | 22.8    | 24.8    | 26.4    | 18.0    | 22.0    | 14.8    | 20.8    |
| MathOctupos<sup>P</sup>         | 46.5    | 40.1    | 42.5    | 29.1    | 43.5    | 45.4    | 46.0    | 42.5    | 45.4    | 35.7    | 41.7    |
| **xRFT**-MathOctupos<sup>P</sup>| 46.8    | 42.3    | 43.2    | 32.8    | 43.1    | 44.5    | 45.3    | 43.2    | 42.1    | 40.5    | 42.4    |

<p></p>

| 13B Model                       | En      | Sw      | Zh      | Bn      | De      | Es      | Fr      | Ja      | Ru      | Th      | Overall |
|:--------------------------------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|
| MathOctupos<sup>C</sup>         | 56.6    | 40.4    | 49.0    | 30.3    | 50.9    | 54.2    | 54.7    | 46.3    | 52.4    | 35.7    | 47.1    |
| **xRFT**-MathOctupos<sup>C</sup>| 52.9    | 41.9    | 49.2    | 34.1    | 50.5    | 52.8    | 51.5    | 45.8    | 50.2    | 35.7    | 46.5    |
| MathOctupos<sup>P</sup>         | 50.7    | 43.4    | 42.6    | 31.8    | 48.4    | 49.4    | 50.6    | 41.1    | 46.9    | 39.3    | 44.4    |
| **xRFT**-MathOctupos<sup>P</sup>| 44.6    | 43.4    | 46.4    | 34.2    | 47.7    | 48.2    | 49.9    | 43.1    | 48.2    | 39.5    | 44.5    |

<p></p>

| 30-34B Model                    | En      | Sw      | Zh      | Bn      | De      | Es      | Fr      | Ja      | Ru      | Th      | Overall |
|:--------------------------------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|:--------|
| MathOctupos<sup>C</sup>         | 51.5    | 42.1    | 46.2    | 23.2    | 50.5    | 52.1    | 52.9    | 42.2    | 50.5    | 33.4    | 44.5    |
| **xRFT**-MathOctupos<sup>C</sup>| 48.1    | 42.8    | 43.6    | 23.3    | 48.7    | 50.0    | 48.9    | 43.4    | 44.6    | 35.5    | 42.9    |
| MathOctupos<sup>P</sup>         | 56.4    | 46.8    | 52.0    | 35.2    | 47.2    | 53.2    | 48.0    | 39.2    | 45.6    | 41.2    | 46.5    |
| **xRFT**-MathOctupos<sup>P</sup>| 48.0    | 42.3    | 46.1    | 36.2    | 47.5    | 48.5    | 48.3    | 45.8    | 47.2    | 41.2    | 45.1    |

## **MathOctupos in English**

| Models                          | GSM8K   | SVAMP   |
|:--------------------------------|:--------|:--------|
| LLaMA 2-7B                      | 42.4    | 38.3    |
| MathOctupos<sup>P</sup>-7B      | 49.3    | 46.8    |
| MathOctupos<sup>C</sup>-7B      | 50.8    | 49.3    |
| LLaMA 2-13B                     | 51.0    | 50.9    |
| MathOctupos<sup>P</sup>-13B     | 55.5    | 52.1    |
| MathOctupos<sup>C</sup>-13B     | 56.6    | 56.6    |
| LLaMA 1-33B                     | 50.0    | 49.0    |
| MathOctupos<sup>P</sup>-33B     | 56.0    | 52.5    |
| MathOctupos<sup>C</sup>-33B     | 53.7    | 51.5    |

## **Multilingual SFT can generally benefit Monolingual SFT**

<div style="text-align: center;">
  <img src="/rq4.png" alt="rq4" width="60%">
</div>

<div style="display: flex; justify-content: center;">
  <p style="color: black; text-align:justify; text-justify:inter-ideograph; max-width: 700px;">
  Above figure separately illustrates the test results of several models in their respective training languages. We ob-
  serve that our model still surpasses the results of the monolingual SFT models in their native
  training languages. This suggests that, at least in the task of math reasoning, multilingual
  SFT can be considered a superior training strategy to monolingual SFT, effortlessly
  elevating the model’s performance in its native language.
  </p>
</div>


<footer class="site-footer">
  <span class="site-footer-owner" style="text-align: center;"><a href="http://localhost:4000">MathOctopus</a> is maintained by <a href="https://nuochenpku.github.io/">Nuo Chen</a> and Zinan Zheng.</span>
  <!-- <span class="site-footer-credits">This page was generated by <a href="https://pages.github.com">GitHub Pages</a>.</span> -->
  <dev style="display: flex; flex-direction:row; justify-content:center">
    <img src="/hkust.png" style="margin: 2em;" width="60%" height="30%">
    <img src="/microsoft.png" style="margin: 3.5em 0 0;" width="30%" height="3%">
  </dev>
</footer>



<!-- ### Header 3

<!-- ```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header. --> 

<!-- ###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item -->

<!-- ### Small image -->

<!-- ![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png) -->


<!-- ### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
``` -->
