<div id="notebook" class="js-html">
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="https://colab.research.google.com/github/aydincagatay/Probability-for-discrete-random-variable/blob/master/BayesTeoremiv2.ipynb" target="_parent"><img src="https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667" alt="Open In Colab" data-canonical-src="https://colab.research.google.com/assets/colab-badge.svg"></a></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1>Bayes' Teoremi<a class="anchor-link" href="#Bayes'-Teoremi"></a>
</h1>
<h2>Giriş<a class="anchor-link" href="#Giri%C5%9F"></a>
</h2>
<p>Bayes teoremi, bilinmeyen olasılıkları tümdengelimsel olarak ölçmenizi sağlayan  olasılık yasasıdır. Bayes Teoremi, koşullu olasılık üzerine kuruludur.</p>
<h2>Thomas Bayes<a class="anchor-link" href="#Thomas-Bayes"></a>
</h2>
<p>Bayes teoremi adını 1700'lü yıllarda doğmuş olan İngiliz olasılıkçı Thomas Bayes'ten almaktadır. Bayes'in ailesi İngiltere'nin önemli Presbiteryen ailelerinden biriydi. 1719 yılında değişim kilisesine mensup olanların gidebildiği, Cambridge ve Oxford o dönemde Presbiteryenlere açık olmadığından, Edinburgh Üniversitesi'nde presbiteryen vaizliği eğitimi almaya başlamıştır.  Edinburgh Üniversitesi'nde okumuştur. Hayatta iken yazdığı notlar ölümünden sonra Richard Price tarafından derlenerek yayınlanmıştır.</p>
<h2>Amaç<a class="anchor-link" href="#Ama%C3%A7"></a>
</h2>
<p>Bu makalenin içerdikleri:</p>
<ul>
<li>Bayes teoremini koşullu olasılıklarla ilişkili olarak tanımı </li>
<li>Bayes teoremini uygulamalı örnekleri</li>
</ul>
<h2>Bayes' Formülü<a class="anchor-link" href="#Bayes'-Form%C3%BCl%C3%BC"></a>
</h2>
<h1>
<img class="math math-inline" alt="$P(A|B) = \dfrac{P(B|A)P(A)}{P(B)}$" src="https://render.githubusercontent.com/render/math?math=P%28A%7CB%29%20%3D%20%5Cdfrac%7BP%28B%7CA%29P%28A%29%7D%7BP%28B%29%7D&amp;mode=inline"><a class="anchor-link" href="#%24P(A%7CB)-=-%5Cdfrac%7BP(B%7CA)P(A)%7D%7BP(B)%7D%24"></a>
</h1>
<p>Bayes teoremi oldukça sezgiseldir ve her iki olayın da gerçekleşme olasılığı açısından A'ya bağlı B'nin koşullu olasılığı ayrıştırılarak B'nin doğru olma olasılığına bölünür. Bayes teoremi, bu doğal fikri bir adım ileriye taşıyarak, her iki olayın koşulun kendisiyle çarpımının koşullu bir olasılık olarak doğru olma olasılığını ifade eder.</p>
<p>Özetlemek gerekirse:</p>
<p>Bayes Teoremi, koşullu olasılıktan gelir.</p>
<h3>
<img class="math math-inline" alt="$P(A|B) = \dfrac{P(A \cap B)}{P(B)}$" src="https://render.githubusercontent.com/render/math?math=P%28A%7CB%29%20%3D%20%5Cdfrac%7BP%28A%20%5Ccap%20B%29%7D%7BP%28B%29%7D&amp;mode=inline"><a class="anchor-link" href="#%24P(A%7CB)-=-%5Cdfrac%7BP(A-%5Ccap-B)%7D%7BP(B)%7D%24"></a>
</h3>
<p><img class="math math-inline" alt="$P(A \cap B)$" src="https://render.githubusercontent.com/render/math?math=P%28A%20%5Ccap%20B%29&amp;mode=inline"> ' yi</p>
<p><img class="math math-inline" alt="$P(B|A)P(A)$" src="https://render.githubusercontent.com/render/math?math=P%28B%7CA%29P%28A%29&amp;mode=inline">,</p>
<p>olarak yazarsak formülümüz şuna dönüşür;</p>
<h3>
<img class="math math-inline" alt="$P(A|B) = \dfrac{P(B|A)P(A)}{P(B)}$" src="https://render.githubusercontent.com/render/math?math=P%28A%7CB%29%20%3D%20%5Cdfrac%7BP%28B%7CA%29P%28A%29%7D%7BP%28B%29%7D&amp;mode=inline"><a class="anchor-link" href="#%24P(A%7CB)-=-%5Cdfrac%7BP(B%7CA)P(A)%7D%7BP(B)%7D%24"></a>
</h3>
<h2>Basit bir örnek<a class="anchor-link" href="#Basit-bir-%C3%B6rnek"></a>
</h2>
<p>İki tane akvaryum olduğunu varsayalım. Küçük akvaryumda, 10 tane palyaço balığı sahip olsun. Büyük akvaryumda ise 200 japon balığı ve 35 palyaço balığı olsun. Verilen bilgiler dahilinde seçilen bir palyaço balığının küçük akvaryumdan seçilmesi olasılığı nedir?</p>
<p>Aslında büyük akvaryum hem kapasite olarak daha hem de balık sayısı olarak küçük akvaryumdan fazla olduğu için balığın büyük olandan seçilmiş olma olasılığı daha fazladır.</p>
<p>Bayes teoremi kullanıldığında, bir balığın küçük akvaryumdan gelen bir balık olmas olasılığını,</p>
<p><img class="math math-inline" alt="$P(\text{kucuk_akvaryum | palyaco_baligi}) = \dfrac{P(\text{palyaco_baligi | kucuk_akvaryum})P(\text{kucuk_akvaryum})}{P(\text{palyaco_baligi})}$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7Bkucuk_akvaryum%20%7C%20palyaco_baligi%7D%29%20%3D%20%5Cdfrac%7BP%28%5Ctext%7Bpalyaco_baligi%20%7C%20kucuk_akvaryum%7D%29P%28%5Ctext%7Bkucuk_akvaryum%7D%29%7D%7BP%28%5Ctext%7Bpalyaco_baligi%7D%29%7D&amp;mode=inline"></p>
<p><img class="math math-inline" alt="$P(\text{palyaco_baligi | kucuk_akvaryum}) = 1$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7Bpalyaco_baligi%20%7C%20kucuk_akvaryum%7D%29%20%3D%201&amp;mode=inline"><br>
<img class="math math-inline" alt="$P(\text{kucuk_akvaryum}) = \dfrac{\text{kucuk akvaryumdaki balik sayisi}}{\text{butun baliklarin sayisi}} = \dfrac{10}{245}$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7Bkucuk_akvaryum%7D%29%20%3D%20%5Cdfrac%7B%5Ctext%7Bkucuk%20akvaryumdaki%20balik%20sayisi%7D%7D%7B%5Ctext%7Bbutun%20baliklarin%20sayisi%7D%7D%20%3D%20%5Cdfrac%7B10%7D%7B245%7D&amp;mode=inline"><br>
<img class="math math-inline" alt="$P(\text{palyaco_baligi}) = \dfrac{45}{245}$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7Bpalyaco_baligi%7D%29%20%3D%20%5Cdfrac%7B45%7D%7B245%7D&amp;mode=inline"></p>
<p>Bayes Teoremi uygulandığı zaman:</p>
<p><img class="math math-inline" alt="$P(\text{kucuk_akvaryum | palyaco_baligi}) = \dfrac{1 \cdot \dfrac{10}{245}}{\dfrac{45}{245}}$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7Bkucuk_akvaryum%20%7C%20palyaco_baligi%7D%29%20%3D%20%5Cdfrac%7B1%20%5Ccdot%20%5Cdfrac%7B10%7D%7B245%7D%7D%7B%5Cdfrac%7B45%7D%7B245%7D%7D&amp;mode=inline"></p>
<p><img class="math math-inline" alt="$ P(\text{kucuk_akvaryum | palyaco_baligi}) = \dfrac{10}{45}$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7Bkucuk_akvaryum%20%7C%20palyaco_baligi%7D%29%20%3D%20%5Cdfrac%7B10%7D%7B45%7D&amp;mode=inline"></p>
<p>Bu örnek, tüm temel bilgilere sahip olduğunuzdan Bayes teoremi uygulanmadan da çözülebilir. Küçük tanktaki palyaço balıklarının sayısına karşı genel olarak palyaço balıklarının sayısına bakmak yine aynı sonuca götürecektir:</p>
<p><img class="math math-inline" alt="$\dfrac{10}{45}$" src="https://render.githubusercontent.com/render/math?math=%5Cdfrac%7B10%7D%7B45%7D&amp;mode=inline"></p>
<h2>Başka bir örnek: NLP Örneği<a class="anchor-link" href="#Ba%C5%9Fka-bir-%C3%B6rnek:-NLP-%C3%96rne%C4%9Fi"></a>
</h2>
<p>Bayes teoremi spam mesajların sınıflandırılmasında doğal bir metod olarak kullanılabilir. Mesela "teklif" kelimesini ele alalım örneğin: (Size özel teklifimiz, Size bir teklifimiz var, Bu teklifi kaçırmayın!). Bu şekilde ulaşmış mesajların %73'ü spam etiketli olsun. %10 'u ise almak istediğimiz türden "teklif" kelimesini içeren mailler olsun. Eğer aldığımız tüm maillerin %20'si spam ise, yeni gelen bir mailin "teklif" kelimesini içerdiğinde spam olma olasılığı nedir?</p>
<p><img class="math math-inline" alt="$P(\text{Spam | Teklif}) = \dfrac{P(\text{Teklif | Spam})P(\text{Spam})}{P(\text{Teklif})}$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7BSpam%20%7C%20Teklif%7D%29%20%3D%20%5Cdfrac%7BP%28%5Ctext%7BTeklif%20%7C%20Spam%7D%29P%28%5Ctext%7BSpam%7D%29%7D%7BP%28%5Ctext%7BTeklif%7D%29%7D&amp;mode=inline"></p>
<p><img class="math math-inline" alt="$P(\text{Spam | Teklif}) = \dfrac{0.73 \cdot 0.20}{P(\text{Teklif})}$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7BSpam%20%7C%20Teklif%7D%29%20%3D%20%5Cdfrac%7B0.73%20%5Ccdot%200.20%7D%7BP%28%5Ctext%7BTeklif%7D%29%7D&amp;mode=inline"><br>
<img class="math math-inline" alt="$P(\text{Teklif}) = P(\text{Spam})\cdot P(\text{Teklif | Spam}) + P(\text{Spam')} \cdot P(\text{Teklif | Spam'})$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7BTeklif%7D%29%20%3D%20P%28%5Ctext%7BSpam%7D%29%5Ccdot%20P%28%5Ctext%7BTeklif%20%7C%20Spam%7D%29%20%2B%20P%28%5Ctext%7BSpam%27%29%7D%20%5Ccdot%20P%28%5Ctext%7BTeklif%20%7C%20Spam%27%7D%29&amp;mode=inline"><br>
<img class="math math-inline" alt="$P(\text{Teklif}) = 0.20 \cdot 0.73 + 0.8 \cdot 0.10$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7BTeklif%7D%29%20%3D%200.20%20%5Ccdot%200.73%20%2B%200.8%20%5Ccdot%200.10&amp;mode=inline"><br>
<img class="math math-inline" alt="$P(\text{Teklif}) = 0.146 + 0.08$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7BTeklif%7D%29%20%3D%200.146%20%2B%200.08&amp;mode=inline"><br>
<img class="math math-inline" alt="$P(\text{Teklif}) = 0.226$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7BTeklif%7D%29%20%3D%200.226&amp;mode=inline"></p>
<p>Son olarak bulduğumuz değerleri yerine yazarsak;</p>
<p><img class="math math-inline" alt="$P(\text{Spam | Teklif}) = \dfrac{0.73 \cdot 0.20}{0.226}$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7BSpam%20%7C%20Teklif%7D%29%20%3D%20%5Cdfrac%7B0.73%20%5Ccdot%200.20%7D%7B0.226%7D&amp;mode=inline"><br>
<img class="math math-inline" alt="$P(\text{Spam | Teklif}) = 0.6460$" src="https://render.githubusercontent.com/render/math?math=P%28%5Ctext%7BSpam%20%7C%20Teklif%7D%29%20%3D%200.6460&amp;mode=inline"></p>
<p>Görüldüğü gibi "Teklif" kelimesinin geçtiği bir mailin spam olma olasılığı %64.6 çıkmış olur. Yukarda problemin aksine bu problemin çözümü için Bayes teoremini kullanmak işimizi kolaylaştırmıştır.</p>
<p>Eğer bu problem için Bayes Teoreminin kodunu yazacak olsaydık:</p>
<p>Öncelikle verilen olasılıksal değerlerin ilk değer atamalarını yapacak olursak:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">math</span>
<span class="n">Pteklif_spam</span> <span class="o">=</span> <span class="mf">0.73</span>
<span class="n">Pspam</span> <span class="o">=</span> <span class="mf">0.2</span>
<span class="n">Pteklif_notspam</span> <span class="o">=</span> <span class="mf">0.1</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">CalculateBayes</span><span class="p">(</span><span class="n">P1</span><span class="p">,</span><span class="n">P2</span><span class="p">,</span><span class="n">P3</span><span class="p">):</span>
    <span class="k">return</span> <span class="p">(</span><span class="n">P1</span> <span class="o">*</span> <span class="n">P2</span><span class="p">)</span> <span class="o">/</span> <span class="p">((</span><span class="n">P1</span> <span class="o">*</span> <span class="n">P2</span><span class="p">)</span> <span class="o">+</span> <span class="p">((</span><span class="mi">1</span><span class="o">-</span><span class="n">P2</span><span class="p">)</span><span class="o">*</span> <span class="n">P3</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">CalculateBayes</span><span class="p">(</span><span class="n">Pteklif_spam</span><span class="p">,</span><span class="n">Pspam</span><span class="p">,</span><span class="n">Pteklif_notspam</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>0.6460176991150441
</pre>
</div>
</div>

</div>
</div>

</div>
 

</div>