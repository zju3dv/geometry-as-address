<div align="center">

<img src="assets/gear_icon.gif" alt="Geometry as Address" width="690">

<h2>Geometry as Address: Routing Attention to Visual Memory for Long-Horizon Camera-Controlled Video Generation</h2>

<h3>ARXIV 2026</h3>

<a href="https://yzszy.github.io/">Zesong Yang</a><sup>1</sup>,
<a href="https://chenweikai.github.io/">Weikai Chen</a><sup>2‡</sup>,
<a href="https://scholar.google.com/citations?user=WhwTrhcAAAAJ&hl=zh-CN">Liyuan Cui</a><sup>1</sup>,
<a href="https://lutao2021.github.io/">Lutao Jiang</a><sup>3</sup>,
Runze Zhang<sup>2</sup>,
Yingda Yin<sup>2</sup>,
Xiaoyang Huang<sup>2</sup>,
Kai Yan<sup>2</sup>,
Keyang Luo<sup>2</sup>,
Wangguandong Zheng,
Xin Wang<sup>2</sup>,
<a href="http://www.cad.zju.edu.cn/home/bao">Hujun Bao</a><sup>1</sup>,
<a href="https://zhpcui.github.io/">Zhaopeng Cui</a><sup>1†</sup>

<sup>1</sup>State Key Laboratory of CAD&amp;CG, Zhejiang University &nbsp;&nbsp;
<sup>2</sup>LIGHTSPEED &nbsp;&nbsp;
<sup>3</sup>HKUST(GZ)

<sup>‡</sup>Project Lead &nbsp;&nbsp; <sup>†</sup>Corresponding Author

[![Project Page](https://img.shields.io/badge/Project_Page-GEAR-2563eb?style=flat-square)](https://zju3dv.github.io/geometry-as-address/)
[![arXiv](https://img.shields.io/badge/arXiv-2609.34722-b31b1b?style=flat-square)](https://arxiv.org/abs/2609.34722)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-green?style=flat-square)](LICENSE)

</div>

## 📰 News

- **[2026-11-27]** Code will be released on **2026-12-16**. Stay tuned! 🚀
- **[2026-09-28]** Release project page and arxiv paper. 🌏

## ✨ Overview

![teaser](assets/teaser.png)

Long-horizon camera-controlled video generation requires recovering previously observed content from an ever-growing visual history. Existing approaches either search historical context implicitly or reconstruct it into persistent 3D memory, facing inefficient memory access or accumulated geometric errors. Our key insight is that geometry need not explain the scene -- it only needs to determine **where visual memory should be read from**, while attention decides **what should be recovered**. Based on this insight, we introduce GEAR, a Geometry-Enabled Attention Routing framework that uses geometry as an explicit token-level address for visual memory. Rather than fusing historical observations into a persistent global 3D representation, GEAR retains them as frame latents and uses per-frame geometry only to establish token-level correspondences with target views, thereby avoiding persistent error accumulation from global fusion. Guided by these correspondences, a proposed Geometric Correspondence Attention (GCA) selectively injects geometrically matched historical features into target noisy patches during denoising. We further introduce an Invisible Octree to accumulate visibility evidence and reject geometrically plausible but occluded correspondences. Extensive experiments demonstrate that GEAR achieves state-of-the-art visual quality, precise camera control, and revisit consistency, enabling minute-long video generation along challenging trajectories.

## 🔬 Method overview

![pipeline](assets/pipeline.png)

**System overview.** For each target chunk, GEAR constructs patch correspondences to retrieved history using per-frame geometry and filters occluded matches with the Invisible Octree. GCA then injects matched historical features into noisy target tokens during denoising, after which generated observations are appended to the history bank for continued rollout.

## 🙏 Acknowledgement

Some codes are modified from [VideoX-Fun](https://github.com/aigc-apps/VideoX-Fun), thanks to the authors for their valuable works.

## 📄 License

Original code is licensed under [Apache 2.0](LICENSE).
Third-party components retain their respective licenses.

## 📝 Citation

If you find this work useful for your research, please consider citing:

```bibtex
@article{yang2026geometry,
    title={Geometry as Address: Routing Attention to Visual Memory for Long-Horizon Camera-Controlled Video Generation},
    author={Yang, Zesong and Chen, Weikai and Cui, Liyuan and Jiang, Lutao and Zhang, Runze and Yin, Yingda and Huang, Xiaoyang and Yan, Kai and Luo, Keyang and Zheng, Wangguandong and Wang, Xin and Bao, Hujun and Cui, Zhaopeng},
    journal={arXiv preprint arXiv:2609.34722},
    year={2026}
}
```
