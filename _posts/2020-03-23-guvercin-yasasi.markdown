<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="https://colab.research.google.com/github/aydincagatay/Probability-for-discrete-random-variable/blob/master/PigeonHole.ipynb" target="_parent"><img src="https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667" alt="Open In Colab" data-canonical-src="https://colab.research.google.com/assets/colab-badge.svg"></a></p>
</div> 

<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<a href ="https://github.com/aydincagatay/Probability-for-discrete-random-variable/blob/master/PigeonHole.ipynb">İsterseniz burdan Github linkine de gidebilirsiniz.</a>
<h1>
<strong>Güvercin Yuvası Prensibi</strong><a class="anchor-link" href="#G%C3%BCvercin-Yuvas%C4%B1-Prensibi"></a>
</h1>
<p>Eğer 4 güvercininiz ve onları yerleştirebileceğiniz 3 yuvanız varsa en az ikisi yuva arkadaşı olmak zorundadır.</p>
<p><em>Genel bir ifadeyle: Eğer k deliğe koymak için k + 1 tane objeniz varsa, o zaman en azından bir tane deliğin içinde 2 veya daha fazla obje olması zorunludur.</em></p>
<p><img src="https://camo.githubusercontent.com/f9faacf1a53a2234fa158f21886c7b7889641286/68747470733a2f2f6769746875622e636f6d2f617964696e636167617461792f50726f626162696c6974792d666f722d64697363726574652d72616e646f6d2d7661726961626c652f626c6f622f6d61737465722f696d616765732f706967656f6e2e706e673f7261773d74727565" alt="alt text" data-canonical-src="https://github.com/aydincagatay/Probability-for-discrete-random-variable/blob/master/images/pigeon.png?raw=true"></p>
<p>Güvercin yuvası prensibinin hikayesi</p>
<p>Gauss 6 yaşındayken babası ile çok büyük bir ormana gezmeye gitmiş. bunlar ormanda yürürken</p>
<p>Gauss babasına sormuş : "Bu ormandaki ağaç sayısı mı daha çok, bir ağaçta olabilecek maksimum yaprak sayısı mı?"</p>
<p>Babası da "ağaç sayısı" demiş.</p>
<p>Gauss da babasına demiş ki : "o zaman bu ormanda birbiriyle aynı sayıda yaprağı olan iki ağaç vardır".</p>
<p>Babası da "peki" demiş tabi. Bugün biz bu prensibi, güvercin yuvası prensibi olarak biliyoruz.</p>
<p>Güvercin yuvası prensibi hem matematiksel teorem ispatlarında hem de güvercin yerleştirmek gibi matematik ile direkt bağlantısı olmadığını sandığımız bir çok yerde karşımıza çıkmaktadır. Şimdi ise başka bir güvercin yuvası problemine bakalım.</p>
<h2>
<strong>Soru</strong><a class="anchor-link" href="#Soru"></a>
</h2>
<p>1 den 12 ye kadar sayılar bir çemberin üzerine diziliyor. Bu işlem hangi sıralamayla yapılırsa yapılsın toplamları 20 veya daha fazla olan komşu 3 sayının muhakkak bulunacağını gösterme deneyini kodda gösterelim.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2>
<strong>Çözüm</strong><a class="anchor-link" href="#Soru"></a>
</h2>
 <blockquote>   
<p>Sayılar saat yönünde a1,a2,...,a12 olsun.</p>
<p>b1=a1+a2+a3</p>
<p>b2=a2+a3+a4</p>
<p>.</p>
<p>.</p>
<p>b12=a12+a1+a2</p>
<p>olsun. bi'lerin toplamı 3(1+2+..+12)=234 yani bu sayılardan 
biri 234/12=~20 ' den büyüktür.</p>
</blockquote>
<p>Kodda göstermek gerekirse ;</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">toplam</span> <span class="o">=</span><span class="mi">0</span> 
<span class="k">for</span> <span class="n">x</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">12</span><span class="p">):</span>
    <span class="k">if</span><span class="p">(</span><span class="n">x</span><span class="o">+</span><span class="mi">1</span> <span class="o">==</span> <span class="mi">12</span><span class="p">):</span>
        <span class="n">toplam</span> <span class="o">=</span> <span class="n">toplam</span> <span class="o">+</span> <span class="n">x</span> <span class="o">+</span> <span class="mi">12</span> <span class="o">+</span> <span class="mi">1</span>
        <span class="nb">print</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="mi">12</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span><span class="s2">" toplam ="</span><span class="p">,</span><span class="n">x</span> <span class="o">+</span> <span class="mi">12</span> <span class="o">+</span> <span class="mi">1</span><span class="p">,</span> <span class="s2">"</span><span class="se">\n</span><span class="s2">"</span><span class="p">)</span>
        <span class="n">toplam</span> <span class="o">=</span> <span class="n">toplam</span> <span class="o">+</span> <span class="mi">12</span> <span class="o">+</span> <span class="mi">1</span> <span class="o">+</span> <span class="mi">2</span>
        <span class="nb">print</span><span class="p">(</span><span class="n">x</span><span class="o">+</span><span class="mi">1</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span><span class="s2">" toplam ="</span><span class="p">,</span><span class="mi">12</span> <span class="o">+</span> <span class="mi">1</span> <span class="o">+</span> <span class="mi">2</span><span class="p">,</span> <span class="s2">"</span><span class="se">\n</span><span class="s2">"</span><span class="p">)</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="n">toplam</span> <span class="o">=</span> <span class="n">toplam</span> <span class="o">+</span> <span class="mi">3</span><span class="o">*</span><span class="n">x</span> <span class="o">+</span> <span class="mi">3</span>
        <span class="nb">print</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">x</span><span class="o">+</span><span class="mi">1</span><span class="p">,</span> <span class="n">x</span><span class="o">+</span><span class="mi">2</span><span class="p">,</span><span class="s2">" toplam ="</span><span class="p">,</span><span class="mi">3</span><span class="o">*</span><span class="n">x</span> <span class="o">+</span> <span class="mi">3</span><span class="p">,</span> <span class="s2">"</span><span class="se">\n</span><span class="s2">"</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>1 2 3  toplam = 6 

2 3 4  toplam = 9 

3 4 5  toplam = 12 

4 5 6  toplam = 15 

5 6 7  toplam = 18 

6 7 8  toplam = 21 

7 8 9  toplam = 24 

8 9 10  toplam = 27 

9 10 11  toplam = 30 

10 11 12  toplam = 33 

11 12 1  toplam = 24 

12 1 2  toplam = 15 

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
<p><strong>Eleman sayısı ve  grup sayısını belirleyelim.</strong></p>
<p><strong>Eleman sayısının grup sayısına bölümünün bir üst sayıya yuvarlanması bize 
en az bir 3'lünün toplamının büyük olabileceği değeri verecektir.</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">math</span>
<span class="n">Eleman_sayisi</span><span class="o">=</span> <span class="n">toplam</span>
<span class="n">Grup_sayisi</span><span class="o">=</span><span class="mi">12</span>
<span class="n">en_az</span><span class="o">=</span> <span class="n">math</span><span class="o">.</span><span class="n">ceil</span><span class="p">(</span><span class="n">Eleman_sayisi</span><span class="o">/</span><span class="n">Grup_sayisi</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"toplam ="</span><span class="p">,</span><span class="n">toplam</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"toplam / 12 =~"</span><span class="p">,</span><span class="n">en_az</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>toplam = 234
toplam / 12 =~ 20
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
<strong>20'den büyük olan en az bir 3'lü grup vardır.</strong><a class="anchor-link" href="#20'den-b%C3%BCy%C3%BCk-olan-en-az-bir-3'l%C3%BC-grup-vard%C4%B1r."></a>
</h1>
</div>
</div>
</div>
 

