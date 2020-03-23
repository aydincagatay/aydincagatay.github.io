---
layout: post
title:  Güvercin Yasası Prensibi"
date:   2020-03-23 23:09:21
categories: jekyll update
---
{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "name": "Untitled1.ipynb",
      "provenance": [],
      "authorship_tag": "ABX9TyM60xLL6cPjnCbQdz81jP1H",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/aydincagatay/Probability-for-discrete-random-variable/blob/master/PigeonHole.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "colab_type": "text",
        "id": "BzsjNC2teQ4X"
      },
      "source": [
        "# **Güvercin Yuvası Prensibi**\n",
        "\n",
        "Eğer 4 güvercininiz ve onları yerleştirebileceğiniz 3 yuvanız varsa en az ikisi yuva arkadaşı olmak zorundadır. \n",
        "\n",
        "*Genel bir ifadeyle: Eğer k deliğe koymak için k + 1 tane objeniz varsa, o zaman en azından bir tane deliğin içinde 2 veya daha fazla obje olması zorunludur.*\n",
        "\n",
        "![alt text](https://github.com/aydincagatay/Probability-for-discrete-random-variable/blob/master/images/pigeon.png?raw=true)\n",
        "\n",
        "\n",
        "Güvercin yuvası prensibinin hikayesi\n",
        "\n",
        "Gauss 6 yaşındayken babası ile çok büyük bir ormana gezmeye gitmiş. bunlar ormanda yürürken \n",
        "\n",
        "Gauss babasına sormuş : \"Bu ormandaki ağaç sayısı mı daha çok, bir ağaçta olabilecek maksimum yaprak sayısı mı?\" \n",
        "\n",
        "Babası da \"ağaç sayısı\" demiş. \n",
        "\n",
        "Gauss da babasına demiş ki : \"o zaman bu ormanda birbiriyle aynı sayıda yaprağı olan iki ağaç vardır\". \n",
        "\n",
        "Babası da \"peki\" demiş tabi. Bugün biz bu prensibi, güvercin yuvası prensibi olarak biliyoruz.\n",
        "\n",
        "Güvercin yuvası prensibi hem matematiksel teorem ispatlarında hem de güvercin yerleştirmek gibi matematik ile direkt bağlantısı olmadığını sandığımız bir çok yerde karşımıza çıkmaktadır.\n",
        "\n",
        "## **Soru**\n",
        "\n",
        "1 den 12 ye kadar sayılar bir çemberin üzerine diziliyor. Bu işlem hangi sıralamayla yapılırsa yapılsın toplamları 20 veya daha fazla olan komşu 3 sayının muhakkak bulunacağını gösterme deneyini kodda gösterelim.\n",
        "\n",
        "\n",
        "\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "v7Ru1-OteMoa",
        "colab_type": "text"
      },
      "source": [
        "\n",
        "\n",
        "> \n",
        "## **Çözüm**\n",
        "\n",
        "> Sayılar saat yönünde a1,a2,...,a12 olsun.\n",
        "\n",
        "\n",
        "> b1=a1+a2+a3\n",
        "\n",
        "\n",
        "> b2=a2+a3+a4\n",
        "\n",
        "\n",
        "> .\n",
        "\n",
        "\n",
        "> .\n",
        "\n",
        "\n",
        "> b12=a12+a1+a2\n",
        "\n",
        "\n",
        "> olsun. bi'lerin toplamı 3(1+2+..+12)=234 yani bu sayılardan \n",
        "> biri 234/12=~20 ' den büyüktür.\n",
        "\n",
        "Kodda göstermek gerekirse ;\n",
        "\n",
        "\n",
        "\n",
        "\n"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "-J9c4abxf1rE",
        "colab_type": "code",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 433
        },
        "outputId": "937763c1-d58c-4ce3-b30e-480d9be3613b"
      },
      "source": [
        "toplam =0 \n",
        "for x in range(1, 12):\n",
        "    if(x+1 == 12):\n",
        "        toplam = toplam + x + 12 + 1\n",
        "        print(x, 12, 1,\" toplam =\",x + 12 + 1, \"\\n\")\n",
        "        toplam = toplam + 12 + 1 + 2\n",
        "        print(x+1, 1, 2,\" toplam =\",12 + 1 + 2, \"\\n\")\n",
        "    else:\n",
        "        toplam = toplam + 3*x + 3\n",
        "        print(x, x+1, x+2,\" toplam =\",3*x + 3, \"\\n\")\n",
        "        "
      ],
      "execution_count": 1,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "1 2 3  toplam = 6 \n",
            "\n",
            "2 3 4  toplam = 9 \n",
            "\n",
            "3 4 5  toplam = 12 \n",
            "\n",
            "4 5 6  toplam = 15 \n",
            "\n",
            "5 6 7  toplam = 18 \n",
            "\n",
            "6 7 8  toplam = 21 \n",
            "\n",
            "7 8 9  toplam = 24 \n",
            "\n",
            "8 9 10  toplam = 27 \n",
            "\n",
            "9 10 11  toplam = 30 \n",
            "\n",
            "10 11 12  toplam = 33 \n",
            "\n",
            "11 12 1  toplam = 24 \n",
            "\n",
            "12 1 2  toplam = 15 \n",
            "\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "q-Tvkeeigk1n",
        "colab_type": "text"
      },
      "source": [
        "**Eleman sayısı ve  grup sayısını belirleyelim.**\n",
        "\n",
        "**Eleman sayısının grup sayısına bölümünün bir üst sayıya yuvarlanması bize \n",
        "en az bir 3'lünün toplamının büyük olabileceği değeri verecektir.**"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "D3Fc2NSPma3T",
        "colab_type": "code",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 52
        },
        "outputId": "d5620134-d5ec-4df5-8e4f-710769628c7a"
      },
      "source": [
        "import math\n",
        "Eleman_sayisi= toplam\n",
        "Grup_sayisi=12\n",
        "en_az= math.ceil(Eleman_sayisi/Grup_sayisi)\n",
        "print(\"toplam =\",toplam)\n",
        "\n",
        "print(\"toplam / 12 =~\",en_az) "
      ],
      "execution_count": 4,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "toplam = 234\n",
            "toplam / 12 =~ 20\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "ypQgc7fCoLZU",
        "colab_type": "text"
      },
      "source": [
        "# **20'den büyük olan en az bir 3'lü grup vardır.**"
      ]
    }
  ]
}
