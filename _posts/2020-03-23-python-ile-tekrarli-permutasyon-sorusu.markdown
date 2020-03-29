<div id="notebook" class="js-html">
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="https://colab.research.google.com/github/aydincagatay/Probability-for-discrete-random-variable/blob/master/TekrarliPermutasyon.ipynb" target="_parent"><img src="https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667" alt="Open In Colab" data-canonical-src="https://colab.research.google.com/assets/colab-badge.svg"></a></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1>
<strong>PYTHON İLE TEKRARLI PERMÜTASYON ÖRNEĞİ</strong><a class="anchor-link" href="#PYTHON-%C4%B0LE-TEKRARLI-PERM%C3%9CTASYON-%C3%96RNE%C4%9E%C4%B0">¶</a>
</h1>
<p>Soru:</p>
<p><img src="https://camo.githubusercontent.com/859175ebfda7fa4bdb85a957d30280336176aadf/68747470733a2f2f6769746875622e636f6d2f617964696e636167617461792f50726f626162696c6974792d666f722d64697363726574652d72616e646f6d2d7661726961626c652f626c6f622f6d61737465722f696d616765732f7470312e706e673f7261773d74727565" alt="alt text" data-canonical-src="https://github.com/aydincagatay/Probability-for-discrete-random-variable/blob/master/images/tp1.png?raw=true"></p>
<p>A'dan B'ye gidilebilecek en kısa kaç yol vardır?</p>
<p>Çözüm:
Bu soruda A noktasından başlayacaksak en kısa yol için bütün yolları şu şekilde düşünebiliriz: Sağa ve sağ alta. Zaten sola alta gitmeye gerek yoktur.</p>
<p>4 kere sağ alta 2 kere sağa gitmeyi A'dan B'ye giderkenki en kısa mesafe olarak tanımlayabiliriz.
Örneğin sağa alta gitmek için X'i, sağa gitmek için Y değişkenlerini tayin edelim.</p>
<p>Yollar şu şekilde sıralabilir.
XXXXYY
XXXYYX
.
.
.
YYXXXX</p>
<p>Tekrarlı permütasyon olmasını sağlayan kısıtın X ve Y'lerin tekrar etmesi olduğunu görmekteyiz.</p>
<p>O zaman cevap şu şekilde olur. (4+2)! / (4!.2!) = 15</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">faktoriyelHesapla</span><span class="p">(</span><span class="n">i</span><span class="p">):</span>
    
    <span class="k">if</span> <span class="n">i</span><span class="o">==</span><span class="mi">1</span><span class="p">:</span>       
        <span class="k">return</span> <span class="mi">1</span>
    
    <span class="k">else</span><span class="p">:</span> 
        <span class="k">return</span> <span class="n">i</span> <span class="o">*</span> <span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">i</span><span class="o">-</span><span class="mi">1</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">X</span> <span class="o">=</span> <span class="mi">4</span>
<span class="n">Y</span> <span class="o">=</span> <span class="mi">2</span>

<span class="n">sonuc</span> <span class="o">=</span> <span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">X</span> <span class="o">+</span> <span class="n">Y</span><span class="p">)</span> <span class="o">/</span> <span class="p">(</span><span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">X</span><span class="p">)</span> <span class="o">*</span> <span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">Y</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"Gidilebilecek en kısa yolların sayısı = "</span><span class="p">,</span><span class="n">sonuc</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Gidilebilecek en kısa yolların sayısı =  15.0
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Soruda şöyle bir değişiklik yaparsak;</p>
<p><img src="https://camo.githubusercontent.com/90d4b86137e3002689aa861078d8cc72d0935ece/68747470733a2f2f6769746875622e636f6d2f617964696e636167617461792f50726f626162696c6974792d666f722d64697363726574652d72616e646f6d2d7661726961626c652f626c6f622f6d61737465722f696d616765732f7470322e706e673f7261773d74727565" alt="alt text" data-canonical-src="https://github.com/aydincagatay/Probability-for-discrete-random-variable/blob/master/images/tp2.png?raw=true"></p>
<p>Eğer işaretlenen  yerden geçiş yapmak kısıtlanırsa o zaman geçilebilecek en kısa yol sayısı ne olur ?</p>
<p>Çözüm:</p>
<p><img src="https://camo.githubusercontent.com/9c63cd796c8bf7ed55f666b3e4dc2a497d6b1596/68747470733a2f2f6769746875622e636f6d2f617964696e636167617461792f50726f626162696c6974792d666f722d64697363726574652d72616e646f6d2d7661726961626c652f626c6f622f6d61737465722f696d616765732f7470332e706e673f7261773d74727565" alt="alt text" data-canonical-src="https://github.com/aydincagatay/Probability-for-discrete-random-variable/blob/master/images/tp3.png?raw=true"></p>
<p>Eğer Tüm durumlardan;</p>
<p>A'dan C'ye gidilen yollar ve D'den B'ye gidilen yollar çıkarılırsa çözüm elde edilir.</p>
<p>Tüm durumları zaten bulmuştuk (15)</p>
<p>O zaman</p>
<p>A'dan C'ye (1 + 1)! / (1! * 1!)</p>
<p>ile</p>
<p>D'den B'ye (2 + 1)! / (2! <em> 1</em>)</p>
<p>sonuçlarını çarpıp tüm durumlardan çıkarırsak sonucu elde etmiş oluruz.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">XAC</span> <span class="o">=</span> <span class="mi">1</span>
<span class="n">YAC</span> <span class="o">=</span> <span class="mi">1</span>

<span class="n">XDB</span> <span class="o">=</span> <span class="mi">1</span>
<span class="n">YDB</span> <span class="o">=</span> <span class="mi">2</span>

<span class="n">AC</span> <span class="o">=</span> <span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">XAC</span> <span class="o">+</span> <span class="n">YAC</span><span class="p">)</span> <span class="o">/</span> <span class="p">(</span><span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">XAC</span><span class="p">)</span> <span class="o">*</span> <span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">YAC</span><span class="p">))</span>
<span class="n">DB</span> <span class="o">=</span><span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">XDB</span> <span class="o">+</span> <span class="n">YDB</span><span class="p">)</span> <span class="o">/</span> <span class="p">(</span><span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">XDB</span><span class="p">)</span> <span class="o">*</span> <span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">YDB</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"Gidilebilecek en kısa yolların sayısı = "</span><span class="p">,</span><span class="n">sonuc</span> <span class="o">-</span> <span class="p">(</span><span class="n">AC</span> <span class="o">*</span> <span class="n">DB</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Gidilebilecek en kısa yolların sayısı =  9.0
</pre>
</div>
</div>

</div>
</div>

</div>
 

</div>