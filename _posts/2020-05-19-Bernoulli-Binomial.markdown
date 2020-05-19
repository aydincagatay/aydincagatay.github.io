<div id="notebook" class="js-html">
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="https://colab.research.google.com/github/aydincagatay/Probability-for-discrete-random-variable/blob/master/BernoulliBinomialRandomVariables.ipynb" target="_parent"><img src="https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667" alt="Open In Colab" data-canonical-src="https://colab.research.google.com/assets/colab-badge.svg"></a></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1>
<strong>Bernoulli dağılımı</strong><a class="anchor-link" href="#Bernoulli-da%C4%9F%C4%B1l%C4%B1m%C4%B1"></a>
</h1>
<p>Bernoulli dağılımı adını ünlü matematikçi Jakob Bernoulli'den(1654–1705) almıştır.</p>
<p>Formülü şöyle ortaya çıkmıştır.</p>
<p>x, P(x)</p>
<p>1, p</p>
<p>0, 1-p</p>
<p>x=1 olduğu durum başarı
x =0 olduğu durum başarısızlık
X Bernoulli rastgele değişkeni 
p ise olasılıktır.</p>
<p>P(1) =p P(0)=1-p</p>
<p>E[X]=p</p>
<p>V(X)=p(1-p).</p>
<h1>Bernoulli Deneyinin Varsayımları:<a class="anchor-link" href="#Bernoulli-Deneyinin-Varsay%C4%B1mlar%C4%B1:"></a>
</h1>
<p>1.Deneyler aynı koşullarda tekrarlanabilirlik özelliğine sahip olmalıdır.</p>
<p>2.Deneylerin yalnız iki mümkün sonucu olması gereklidir.</p>
<p>3.Başarı olasılığı ( p ), deneyden deneye değişmemelidir.(Başarısızlık</p>
<p>olasılığı q=1-p ile gösterilir)</p>
<p>4.Denemeler birbirinden bağımsız olmalıdır.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Örnek:Bir sporcunun yaptığı müsabakada kazanma olasılığı 0,8 kaybetme olasılığı ise 0,2 olarak verilmiştir.</p>
<p>Sporcunun beklenen(ortalama)kazanma olasılığı ve varyansını bulunuz.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">math</span>

<span class="c1">#definition</span>

<span class="n">p</span> <span class="o">=</span> <span class="mf">0.8</span> <span class="c1"># sporcunun kazanma olasılığı </span>

<span class="n">q</span> <span class="o">=</span> <span class="mf">0.2</span> <span class="c1"># sporcunun kaybetme olasılığı</span>

<span class="k">def</span> <span class="nf">variance</span><span class="p">(</span><span class="n">p</span><span class="p">):</span>
  <span class="k">return</span> <span class="n">p</span><span class="o">*</span><span class="p">(</span><span class="mi">1</span><span class="o">-</span><span class="n">p</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s1">'Sporcunun beklenen(ortalama) kazanma olasılığı ='</span><span class="p">,</span><span class="nb">round</span><span class="p">(</span><span class="n">variance</span><span class="p">(</span><span class="n">p</span><span class="p">),</span><span class="mi">2</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Sporcunun beklenen(ortalama) kazanma olasılığı = 0.16
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
<h1>
<strong>Binomial dağılımı</strong><a class="anchor-link" href="#Binomial-da%C4%9F%C4%B1l%C4%B1m%C4%B1"></a>
</h1>
<p>Bernoulli dağılımında deney bir kez yapılıyor ve olumlu veya başarılı sonuçla ilgileniyordu. Eğer deney bir defa değil, n defa peş peşe birbirinden bağımsız olmak üzere tekrarlandığında yine olumlu veya başarılı sonuçla ilgileniyorsa, Bernoulli dağılımının özel bir genel hali ilgileniyorsa, Bernoulli dağılımının özel bir genel hali ortaya çıkar ve bu dağılıma Binom dağılımı denir.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Örnek</p>
<p>Bir öğrencinin fen lisesine gitme olasılığı 0.3'tür. Eğer aynı ortaokuldan 5 öğrenci liseye kayıt yaptıracaksa en fazla 2'sinin fen lisesine girme olasılığı nedir?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">faktoriyelHesapla</span><span class="p">(</span><span class="n">i</span><span class="p">):</span>
    
    <span class="k">if</span> <span class="n">i</span><span class="o">==</span><span class="mi">1</span> <span class="ow">or</span> <span class="n">i</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>       
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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">binomial</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">n</span><span class="p">,</span><span class="n">P</span><span class="p">):</span>
  <span class="k">return</span> <span class="p">(</span><span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">n</span><span class="p">)</span> <span class="o">/</span> <span class="p">(</span><span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">x</span><span class="p">)</span> <span class="o">*</span> <span class="p">(</span><span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">n</span><span class="o">-</span><span class="n">x</span><span class="p">))))</span> <span class="o">*</span> <span class="nb">pow</span><span class="p">(</span><span class="n">P</span> <span class="p">,</span> <span class="n">x</span><span class="p">)</span> <span class="o">*</span> <span class="nb">pow</span><span class="p">((</span><span class="mi">1</span><span class="o">-</span><span class="n">P</span><span class="p">)</span> <span class="p">,</span> <span class="n">n</span><span class="o">-</span><span class="n">x</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[37]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#definition</span>
<span class="kn">import</span> <span class="nn">sys</span>
 
<span class="n">n</span> <span class="o">=</span> <span class="mi">5</span> <span class="c1">#tekrarlama sayısı</span>
<span class="n">P</span> <span class="o">=</span> <span class="mf">0.3</span> <span class="c1">#fen lisesine gitme olasılığı</span>
<span class="n">sonuc</span><span class="o">=</span><span class="mi">0</span>
<span class="k">for</span> <span class="n">x</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">3</span><span class="p">):</span>
      <span class="n">sonuc</span> <span class="o">=</span> <span class="n">sonuc</span> <span class="o">+</span><span class="p">(</span><span class="n">binomial</span><span class="p">(</span><span class="n">x</span> <span class="p">,</span> <span class="n">n</span><span class="p">,</span> <span class="n">P</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'Aynı ortaokuldan 5 öğrenciden en fazla 2 sinin fen lisesine girme olasılığı = '</span><span class="p">,</span><span class="nb">round</span><span class="p">(</span><span class="n">sonuc</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Aynı ortaokuldan 5 öğrenciden en fazla 2 sinin fen lisesine girme olasılığı =  0.8369
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
<p>Yapılan işlemler;</p>
<p>b(x &lt; 2; 5, 0.3) = b(x = 0; 5, 0.3) + b(x = 1; 5, 0.3) + b(x = 2; 5, 0.3)</p>
<p>b(x &lt; 2; 5, 0.3) = 0.1681 + 0.3601 + 0.3087</p>
<p>b(x &lt; 2; 5, 0.3) = 0.8369</p>

</div>
</div>
</div>
 

</div>