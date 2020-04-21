<div id="notebook" class="js-html">
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1>
<strong>Kombinasyon ve Karşılaşma Problemi</strong><a class="anchor-link" href="#Kombinasyon-ve-Kar%C5%9F%C4%B1la%C5%9Fma-Problemi"></a>
</h1>
<p><strong>Kombinasyon</strong>, bir nesne grubu içerisinden, sıra gözetmeksizin yapılan seçimlerdir. Örnek olarak mavi, sarı ve kırmızı topların bulunduğu torbadan çekilen topların seçilmesi olayının kaç farklı şekilde olabileceğinin hesaplanması kombinasyon ile hesaplanır.</p>
<p><strong>Kombinasyonun formülü</strong></p>
<p><img src="https://camo.githubusercontent.com/0585ef4abc0cdf78875b6047b25b559af1518a1d/68747470733a2f2f6769746875622e636f6d2f617964696e636167617461792f50726f626162696c6974792d666f722d64697363726574652d72616e646f6d2d7661726961626c652f626c6f622f6d61737465722f696d616765732f6b6f6d62696e6173796f6e2e6a70673f7261773d74727565" alt="alt text" data-canonical-src="https://github.com/aydincagatay/Probability-for-discrete-random-variable/blob/master/images/kombinasyon.jpg?raw=true"></p>
<p>Ayrıca kombinasyonu pythonda yazalım ve ilgi çekici bir karşılaşma problemini çözelim.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1>
<strong>Soru:</strong><a class="anchor-link" href="#Soru:"></a>
</h1>
<h1>Evlendiğiniz kişinin, evlenmek istediğiniz kişi olmasının olasılığı ne olabilir ?<a class="anchor-link" href="#Evlendi%C4%9Finiz-ki%C5%9Finin,-evlenmek-istedi%C4%9Finiz-ki%C5%9Fi-olmas%C4%B1n%C4%B1n-olas%C4%B1l%C4%B1%C4%9F%C4%B1-ne-olabilir-?"></a>
</h1>
<h1>
<strong>Çözüm:</strong><a class="anchor-link" href="#%C3%87%C3%B6z%C3%BCm:"></a>
</h1>
<p>Aslında başta uyarmam gereken birkaç durum var.</p>
<ul>
<li>Evlenmek istediğiniz kişi sayısı 1'den fazla ise bu bizim hesaplayacağımız olasılıktan daha yüksek çıkacaktır. Çünkü belli başlı kuralları kabul ettiğimiz zaman ortaya çıkan sonucu sizinle paylaşıyorum. Bu örneğin sorusuna ruh eşinizi bulma olasılığı da diyebilirsiniz.</li>
<li>Her kişi ile karşılaşma için eşit şans verilmektedir.</li>
<li>Bir insanın ömründe ortalama 80.000 insan ile karşılaştığını varsayalım.</li>
<li>Türkiye'de bulunan nüfus için değerlendirme yapalım. Türkiye nüfusunda örnekteki insanın ömrü boyunca aynı nüfus oranında olduğunu, kadın-erkek sayısının eşit ve ikisinin toplamının 80.000.000 olduğunu varsayalım. Yaş ile ilgili ise herkesin reşit yaşta olduğunu varsayalım.</li>
</ul>
<p>Eğer tüm durumlardan, bir insanın ömrü boyunca tanıştığı kişilerin dışında kalan nüfusun kombinasyonunun, tüm nüfusta karşılaşılanların nüfusunun kombinasyonunun 1'den çıkarılımı bir insanın evlendiği kişinin hayatındaki evlenmek istediği kişi olma olasılığının sonucunu verecektir.</p>
<p>Bu durumda belirlenmesi gerekenler şunlardır;</p>
<ol>
<li>Olay uzayı : Bu insanın ömrü boyunca tanıştığı kişilerin dışında kalan nüfusun seçilmesi</li>
<li>Örnek uzay :Tüm nüfustan karşılaşılanların nüfusunun seçilmesi</li>
</ol>
<p>Değişkenlerimizi tanımlamak gerekirse;</p>
<ul>
<li>P (Toplam nüfus) = 40.000.000 // Kadın-Erkek olarak ayrıldı</li>
<li>S (Toplam evlenilecek kişi sayısı) = 1</li>
<li>F (Bir insanın ömrü boyunca tanıştığı kişi sayısı) = 80.000</li>
</ul>
<p>Şimdi kodlamaya geçelim.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">math</span>
<span class="n">P</span> <span class="o">=</span> <span class="mi">40000000</span>
<span class="n">S</span> <span class="o">=</span> <span class="mi">1</span>
<span class="n">F</span> <span class="o">=</span> <span class="mi">80000</span>
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
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">kombinasyonHesapla</span><span class="p">(</span><span class="n">n</span><span class="p">,</span><span class="n">r</span><span class="p">):</span>
    
    <span class="k">if</span> <span class="n">r</span><span class="o">==</span><span class="mi">0</span> <span class="ow">or</span> <span class="n">n</span> <span class="o">==</span> <span class="n">r</span><span class="p">:</span>       
        <span class="k">return</span> <span class="mi">1</span>
    <span class="k">else</span><span class="p">:</span> 
        <span class="k">return</span> <span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">n</span><span class="p">)</span> <span class="o">/</span> <span class="p">(</span><span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">n</span> <span class="o">-</span> <span class="n">r</span><span class="p">)</span> <span class="o">*</span> <span class="n">faktoriyelHesapla</span><span class="p">(</span><span class="n">r</span><span class="p">))</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">karsilasmaProblemi</span><span class="p">(</span><span class="n">P</span><span class="p">,</span><span class="n">S</span><span class="p">,</span><span class="n">F</span><span class="p">):</span>
    
    <span class="k">return</span> <span class="mi">1</span><span class="o">-</span> <span class="p">(</span><span class="n">kombinasyonHesapla</span><span class="p">(</span><span class="n">P</span><span class="o">-</span><span class="n">F</span><span class="p">,</span><span class="n">S</span><span class="p">)</span><span class="o">/</span><span class="n">kombinasyonHesapla</span><span class="p">(</span><span class="n">P</span><span class="p">,</span><span class="n">S</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">karsilasmaProblemi</span><span class="p">(</span><span class="n">P</span><span class="p">,</span><span class="n">S</span><span class="p">,</span><span class="n">F</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>
<div class="output_subarea output_text output_error">
<pre><span class="ansi-red-fg">---------------------------------------------------------------------------</span>
<span class="ansi-red-fg">RecursionError</span>                            Traceback (most recent call last)
<span class="ansi-green-fg">&lt;ipython-input-5-8af97acc5d68&gt;</span> in <span class="ansi-cyan-fg">&lt;module&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-fg">----&gt; 1</span><span class="ansi-red-fg"> </span>karsilasmaProblemi<span class="ansi-blue-fg">(</span>P<span class="ansi-blue-fg">,</span>S<span class="ansi-blue-fg">,</span>F<span class="ansi-blue-fg">)</span>

<span class="ansi-green-fg">&lt;ipython-input-4-c6ebc030159b&gt;</span> in <span class="ansi-cyan-fg">karsilasmaProblemi</span><span class="ansi-blue-fg">(P, S, F)</span>
<span class="ansi-green-intense-fg ansi-bold">      1</span> <span class="ansi-green-fg">def</span> karsilasmaProblemi<span class="ansi-blue-fg">(</span>P<span class="ansi-blue-fg">,</span>S<span class="ansi-blue-fg">,</span>F<span class="ansi-blue-fg">)</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-intense-fg ansi-bold">      2</span> 
<span class="ansi-green-fg">----&gt; 3</span><span class="ansi-red-fg">     </span><span class="ansi-green-fg">return</span> <span class="ansi-cyan-fg">1</span><span class="ansi-blue-fg">-</span> <span class="ansi-blue-fg">(</span>kombinasyonHesapla<span class="ansi-blue-fg">(</span>P<span class="ansi-blue-fg">-</span>F<span class="ansi-blue-fg">,</span>S<span class="ansi-blue-fg">)</span><span class="ansi-blue-fg">/</span>kombinasyonHesapla<span class="ansi-blue-fg">(</span>P<span class="ansi-blue-fg">,</span>S<span class="ansi-blue-fg">)</span><span class="ansi-blue-fg">)</span>

<span class="ansi-green-fg">&lt;ipython-input-3-a89adc1add34&gt;</span> in <span class="ansi-cyan-fg">kombinasyonHesapla</span><span class="ansi-blue-fg">(n, r)</span>
<span class="ansi-green-intense-fg ansi-bold">      4</span>         <span class="ansi-green-fg">return</span> <span class="ansi-cyan-fg">1</span>
<span class="ansi-green-intense-fg ansi-bold">      5</span>     <span class="ansi-green-fg">else</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-fg">----&gt; 6</span><span class="ansi-red-fg">         </span><span class="ansi-green-fg">return</span> faktoriyelHesapla<span class="ansi-blue-fg">(</span>n<span class="ansi-blue-fg">)</span> <span class="ansi-blue-fg">/</span> <span class="ansi-blue-fg">(</span>faktoriyelHesapla<span class="ansi-blue-fg">(</span>n <span class="ansi-blue-fg">-</span> r<span class="ansi-blue-fg">)</span> <span class="ansi-blue-fg">*</span> faktoriyelHesapla<span class="ansi-blue-fg">(</span>r<span class="ansi-blue-fg">)</span><span class="ansi-blue-fg">)</span>

<span class="ansi-green-fg">&lt;ipython-input-2-915f446c5eaf&gt;</span> in <span class="ansi-cyan-fg">faktoriyelHesapla</span><span class="ansi-blue-fg">(i)</span>
<span class="ansi-green-intense-fg ansi-bold">      5</span> 
<span class="ansi-green-intense-fg ansi-bold">      6</span>     <span class="ansi-green-fg">else</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-fg">----&gt; 7</span><span class="ansi-red-fg">         </span><span class="ansi-green-fg">return</span> i <span class="ansi-blue-fg">*</span> faktoriyelHesapla<span class="ansi-blue-fg">(</span>i<span class="ansi-blue-fg">-</span><span class="ansi-cyan-fg">1</span><span class="ansi-blue-fg">)</span>

... last 1 frames repeated, from the frame below ...

<span class="ansi-green-fg">&lt;ipython-input-2-915f446c5eaf&gt;</span> in <span class="ansi-cyan-fg">faktoriyelHesapla</span><span class="ansi-blue-fg">(i)</span>
<span class="ansi-green-intense-fg ansi-bold">      5</span> 
<span class="ansi-green-intense-fg ansi-bold">      6</span>     <span class="ansi-green-fg">else</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-fg">----&gt; 7</span><span class="ansi-red-fg">         </span><span class="ansi-green-fg">return</span> i <span class="ansi-blue-fg">*</span> faktoriyelHesapla<span class="ansi-blue-fg">(</span>i<span class="ansi-blue-fg">-</span><span class="ansi-cyan-fg">1</span><span class="ansi-blue-fg">)</span>

<span class="ansi-red-fg">RecursionError</span>: maximum recursion depth exceeded in comparison</pre>
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
<p>Çok fazla rekürsif işlemi olduğu için optimize edilmiş kombinasyon hesaplama fonksiyonu yazmalıyız. O yüzden yeni bir fonksiyon oluşturuyorum.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[0]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">optimizedSolution</span><span class="p">(</span><span class="n">P</span><span class="p">,</span><span class="n">S</span><span class="p">,</span><span class="n">F</span><span class="p">):</span>
    
    <span class="k">return</span> <span class="mi">1</span> <span class="o">-</span> <span class="p">((</span><span class="n">P</span><span class="o">-</span><span class="n">F</span><span class="p">)</span> <span class="o">/</span> <span class="n">P</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Bu işlemin buna dönüşmesindeki neden şudur, kombinasyonu hesaplarken S=1 olduğu için işlemi sadeleştirerek yaptım bu normal şartlarda kombinasyon fonksiyonunu hesaplarken de eklenebilirdi.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">optimizedSolution</span><span class="p">(</span><span class="n">P</span><span class="p">,</span><span class="n">S</span><span class="p">,</span><span class="n">F</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt output_prompt">Out[7]:</div>


<div class="output_text output_subarea output_execute_result">
<pre>0.0020000000000000018</pre>
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
<p>Çıkan sonuç yaklaşık olarak %0,002 olmuş oldu. Oldukça küçük bir oran.</p>

</div>
</div>
</div>
 

</div>