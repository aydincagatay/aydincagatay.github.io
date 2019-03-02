---
layout: post
title:  "Siteyi nasıl kurdum"
date:   2019-03-02 23:09:21
categories: jekyll update
---
Size olabildiğince kolay bir şekilde bu blog sitesini nasıl kurduğumu anlatıcam ki siz de bir an önce github.io uzantılı bir siteye sahip olun.

Öncelikle gerekli kurulumları yapmakla başlayalım sırasıyla şunlar kurulacak.
1) VS Code
2) Github Destkop ya da GitBash
3) Ruby devkit
4) Ubuntu ya da Windows kullanıcısıysanız Ubuntu destkop

Sonra ise gitbashi açın githuba kaydolduğunuz emaili aşağıdaki kod aralığına yazın.

$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

Ssh şifremizin nereye kaydedileceğini soracak bir yol belirleyin ve kaydedin.
Sonra ise güvenlik adımlarını izleyin ve ssh şifreniz kaydedilmiş olacaktır.

Daha sonra kendinize ücretli ya da ücretsiz bir jekyll template seçin ve indirin.
Template'inizi olduğu gibi github destkop veya gitbash ile github'a pushlayın.
(Unutmayın: Repository adı "kullanıcıadınız.github.io" şeklinde olmalı.)

Bu noktada pushlama yaparken gitbash kullanıcısı iseniz "everything up to date" hatası alabilirsiniz.
Ben o yüzden github destkop ile pushlama yapıyorum.

Gelelim başlangıçta yaptığımız ssh keyi, repositorye eklemeye.
Bu kısım çok kolay repository'den settings'e gelin.
Ardından Deploy key seçeneğine basın ve ssh keyi oraya ekleyin. 

Siteniz birkaç dakika gecikmeli olarak github sistemlerine eklenebilir ve aradaki zaman sizin için sorun olabilir. Bu olumsuz yönlerinden biri. Olumlu yönleri ise basit ve ücretsiz ayrıca statik bir siteyi developerin ellerine verirseniz zaten dinamikleşecektir...


