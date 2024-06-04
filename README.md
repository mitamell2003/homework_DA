# homework_DA
{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyMX4LpNlU4kGk1VkKDaG5yG",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
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
        "<a href=\"https://colab.research.google.com/github/mitamell2003/homework_DA/blob/main/homework10.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Bài tập 1: Viết một hàm kiem_tra_so_nguyen_to(n) nhận vào một số nguyên dương n và kiểm tra xem n có phải là số nguyên tố hay không. Sử dụng vòng lặp và kiểm tra các ước số của n để thực hiện tác vụ này."
      ],
      "metadata": {
        "id": "3JbOBXEolMPG"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "import math\n",
        "def kiem_tra_so_nguyen_to(n):\n",
        "  nth = int(n)\n",
        "  if nth < 2: return False\n",
        "  for i in range(2, math.ceil(math.sqrt(nth))):\n",
        "    if n % i == 0: return False\n",
        "  return True\n",
        "\n",
        "n = int(input(\"Input: \"))\n",
        "result = kiem_tra_so_nguyen_to(n)\n",
        "if result:\n",
        "  print(f\"{n} is Prime\")\n",
        "else:\n",
        "  print(f\"{n} is not prime\")"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "L-v2gbxzlOO9",
        "outputId": "f34ce52a-14a7-468f-e299-83ecfc07357d"
      },
      "execution_count": 1,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Input: 10\n",
            "10 is not prime\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Bài tập 2: Viết một hàm tinh_giai_thua(n) nhận vào một số nguyên dương n và tính giai thừa của n (n!)\n"
      ],
      "metadata": {
        "id": "srezod93l0Nf"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "def tinh_giai_thua(n):\n",
        "  giai_thua = int(n)\n",
        "  if giai_thua == 0 or giai_thua == 1:\n",
        "    print(\"gia thua la 1 \")\n",
        "    return giai_thua\n",
        "  for i in range(2, n+1):\n",
        "      giai_thua = giai_thua * i\n",
        "  return giai_thua\n",
        "n = int(input(\"nhap vao mot so \"))\n",
        "print(tinh_giai_thua(n))\n",
        "\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "lNZpRprhl3vL",
        "outputId": "655d5399-cf9f-4f42-c231-e15db4230c1a"
      },
      "execution_count": 10,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "nhap vao mot so 1\n",
            "gia thua la 1 \n",
            "1\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Bài tập 3: Viết một hàm tinh_tong(n) nhận vào một số nguyên dương n và tính tổng các chữ số của n. Ví dụ: n = 123, thì hiển thị kết quả là 6.\n"
      ],
      "metadata": {
        "id": "gkFzTd_zrLYq"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "def sum_digits(number):\n",
        "    sum = 0\n",
        "    while number != 0:\n",
        "      sum += number % 10\n",
        "      number = number // 10\n",
        "\n",
        "    return sum\n",
        "\n",
        "number = int(input(\"hãy nhập vào chữ số \"))\n",
        "\n",
        "print(sum_digits(number))\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "PUN7XHXirOXm",
        "outputId": "5a141cbd-b032-49d0-bdae-162f0ee5a04d"
      },
      "execution_count": 18,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "hãy nhập vào chữ số 123\n",
            "6\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Bài tập 4: Viết một hàm tinh_trung_binh(data) nhận vào một danh sách số và tính trung bình cộng của các số trong danh sách đó. Sử dụng vòng lặp để lặp qua từng số trong danh sách và tính tổng các số\n",
        "\n"
      ],
      "metadata": {
        "id": "DmH1lKKut_Vj"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# tổng các phần tử chia cho tổng số phần tử\n",
        "data = []\n",
        "def tinh_trung_binh(data):\n",
        "  return sum(data) / len(data)\n",
        "for i in range(1,11):\n",
        "  data.append(i)\n",
        "print(tinh_trung_binh(data))"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "0LFThiqtvKSy",
        "outputId": "f53f70bc-04fb-48aa-eec6-af54c43cebaa"
      },
      "execution_count": 22,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "5.5\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Bài tập 5: Viết một hàm dem_so_lan_xuat_hien(data) nhận vào một danh sách và đếm số lần xuất hiện của mỗi phần tử trong danh sách đó.\n"
      ],
      "metadata": {
        "id": "uTiEnxfaww9r"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "data = [1, 1, 3, 5, 3, 6, 7, 9, 10, 10, 7, 10, 1, 4]\n",
        "count = {}\n",
        "for i in data:\n",
        "    if i in count:\n",
        "      count[i] += 1\n",
        "    else:\n",
        "      count[i] = 1\n",
        "\n",
        "print(\"số lần xuất hiện của từng phần tử: \")\n",
        "for i, count in count.items():\n",
        "    print(f\"{i}: {count} lần\")"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "FLYSZxYmwy-5",
        "outputId": "bb835897-8b88-4f2d-952b-34bb1d636b35"
      },
      "execution_count": 27,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "số lần xuất hiện của từng phần tử: \n",
            "1: 3 lần\n",
            "3: 2 lần\n",
            "5: 1 lần\n",
            "6: 1 lần\n",
            "7: 2 lần\n",
            "9: 1 lần\n",
            "10: 3 lần\n",
            "4: 1 lần\n"
          ]
        }
      ]
    }
  ]
}
