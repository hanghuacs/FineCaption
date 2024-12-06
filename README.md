# FINECAPTION: Compositional Image Captioning Focusing on Wherever You Want at Any Granularity
<p align="center">
  <a href="https://arxiv.org/pdf/2411.15411"><img src="https://img.shields.io/badge/Paper-arXiv-b31b1b.svg"></a>
  &nbsp;
  <a href="https://hanghuacs.github.io/FineCaption/"><img src="https://img.shields.io/badge/Website-ProjectPage-A55D35"></a>
  &nbsp;
  <a href="https://huggingface.co/hhua2/finecaption"><img src="https://img.shields.io/badge/Resource-Dataset-EFBF6A.svg"></a>
</p>

---

![](/static/images/teaser-1.svg)
FINECAPTION is  a novel Vision-Language model with the improved capabilities of Attribute-Aware Regional
Captioning, Regional Dense Captioning, and Comprehensive Global Image Captioning. FINECAPTION can recognize arbitrary masks
as referential inputs and process high-resolution images.

---
<section class="section">
  <div class="container is-max-desktop">
    <div class="columns is-centered">
      <div class="column is-full-width">
        <h2 class="title is-3">Comparison of Models</h2>
        <div class="table-container">
          <table class="table is-bordered is-striped is-narrow is-hoverable is-fullwidth">
            <thead>
              <tr>
                <th rowspan="2">Model</th>
                <th colspan="3">Region Referral</th>
                <th colspan="5">Semantic Evaluation</th>
              </tr>
              <tr>
                <th>Visual Prompt</th>
                <th>Resolution</th>
                <th># Image Token</th>
                <th>ROUGE-L ↑</th>
                <th>BLEU-4 ↑</th>
                <th>METEOR ↑</th>
                <th>CIDEr ↑</th>
                <th>BERT Score ↑</th>
              </tr>
            </thead>
            <tbody>
              <!-- Zero-shot learning -->
              <tr style="background-color:#e9edf6;">
                <td colspan="9" style="text-align:center; font-weight:bold;"><i>Zero-Shot Learning</i></td>
              </tr>
              <tr>
                <td>Kosmos-2</td><td>Bbox</td><td>224</td><td>256</td><td>9.21</td><td>0.14</td><td>1.98</td><td>1.07</td><td>37.69</td>
              </tr>
              <tr>
                <td>Alpha-CLIP-13B</td><td>Mask</td><td>336</td><td>576</td><td>13.89</td><td>0.51</td><td>5.94</td><td>2.68</td><td>42.01</td>
              </tr>
              <tr>
                <td>Qwen2-VL-7B</td><td>Bbox</td><td>AnyRes</td><td>-</td><td>14.12</td><td>0.57</td><td>6.18</td><td>2.74</td><td>42.97</td>
              </tr>
              <tr style="background-color:#FFF9E3;">
                <td>GPT-4o</td><td>Bbox</td><td>-</td><td>-</td><td>17.87</td><td>3.21</td><td>12.87</td><td>6.49</td><td>49.85</td>
              </tr>
              <!-- Supervised learning -->
              <tr style="background-color:#e9edf6;">
                <td colspan="9" style="text-align:center; font-weight:bold;"><i>Supervised Learning</i></td>
              </tr>
              <tr>
                <td>Qwen2-VL-7B</td><td>Bbox</td><td>AnyRes</td><td>-</td><td>31.59</td><td>9.11</td><td>13.56</td><td>90.32</td><td>75.86</td>
              </tr>
              <tr style="background-color:#DAE8FC;">
                <td><b>FINECAPTION-8B (ours)</b></td><td>Mask</td><td>1024</td><td>1024</td>
                <td><b>41.05</b></td><td><b>14.46</b></td><td><b>22.01</b></td><td><b>127.95</b></td><td><b>80.97</b></td>
              </tr>
            </tbody>
          </table>
          <p class="is-bold">Table 2. Comparison of the capabilities of FINECAPTION and other related VLMs.</p>
        </div>
      </div>
    </div>
  </div>
</section>

---

## Install
Please following the guide here to prepare the environment on **Linux OS**.
<!-- currently does not support windows and MacOS -->

1. Clone this repository
```bash
https://github.com/hanghuacs/FineCaption.git
cd FineCaption
```

2. Create environment and install package
```Shell
. init.sh
```




## ✏️ Citation
```bibtex
@article{hua2024finecaption,
  title={FINECAPTION: Compositional Image Captioning Focusing on Wherever You Want at Any Granularity},
  author={Hua, Hang and Liu, Qing and Zhang, Lingzhi and Shi, Jing and Zhang, Zhifei and Wang, Yilin and Zhang, Jianming and Luo, Jiebo},
  journal={arXiv preprint arXiv:2411.15411},
  year={2024}
}
```
