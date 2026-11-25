# 帮我按照如下要求优化代码的README文件
* 帮我置顶按照如下要求准备一个动态 icon
    * 将 https://zju3dv.github.io/geometry-as-address/ 顶部的动态标题，将其动态效果导出为 gif, 保存到 @assets/gear_icon.gif, 然后将其置顶于 README 的顶部

* 然后为对应的论文名字: Geometry as Address: Routing Attention to Visual Memory for Long-Horizon Camera-Controlled Video Generation
* 紧跟投稿会议: ARXIV 2026
* 然后是作者信息及其链接:
    * Zesong Yang^1, link: https://yzszy.github.io/
    * Weikai Chen^2‡, link: https://chenweikai.github.io/
    * Liyuan Cui^1, link: https://scholar.google.com/citations?user=WhwTrhcAAAAJ&hl=zh-CN
    * Lutao Jiang^3, link: https://lutao2021.github.io/
    * Runze Zhang^2, 
    * Yingda Yin^2, 
    * Xiaoyang Huang^2, 
    * Kai Yan^2, 
    * Keyang Luo^2, 
    * Wangguandong Zheng
    * Xin WANG^2, 
    * Hujun Bao^1, link: http://www.cad.zju.edu.cn/home/bao
    * Zhaopeng Cui^1†, link: https://zhpcui.github.io/
    1: State Key Laboratory of CAD&CG, Zhejiang University
    2: LIGHTSPEED
    3: HKUST(GZ)
    ‡ denotes Project Lead
    † denotes Corresponding Author
* 然后放置如下的图标:
    [![Project Page](https://img.shields.io/badge/Project_Page-GEAR-2563eb?style=flat-square)](https://zju3dv.github.io/geometry-as-address/)
    [![arXiv](https://img.shields.io/badge/arXiv-2609.34722-b31b1b?style=flat-square)](https://arxiv.org/abs/2609.34722)
    [![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-green?style=flat-square)](LICENSE)

* 然后放置 News

## 📰 News

- **[2026-09-28]** Release project page and arxiv paper. 🌏

* 然后是 Overview 部分
## ✨ Overview

* 先插入图像 @assets/teaser.png

Long-horizon camera-controlled video generation requires recovering previously observed content from an ever-growing visual history. Existing approaches either search historical context implicitly or reconstruct it into persistent 3D memory, facing inefficient memory access or accumulated geometric errors. Our key insight is that geometry need not explain the scene -- it only needs to determine **where visual memory should be read from**, while attention decides **what should be recovered**. Based on this insight, we introduce GEAR, a Geometry-Enabled Attention Routing framework that uses geometry as an explicit token-level address for visual memory. Rather than fusing historical observations into a persistent global 3D representation, GEAR retains them as frame latents and uses per-frame geometry only to establish token-level correspondences with target views, thereby avoiding persistent error accumulation from global fusion. Guided by these correspondences, a proposed Geometric Correspondence Attention (GCA) selectively injects geometrically matched historical features into target noisy patches during denoising. We further introduce an Invisible Octree to accumulate visibility evidence and reject geometrically plausible but occluded correspondences. Extensive experiments demonstrate that GEAR achieves state-of-the-art visual quality, precise camera control, and revisit consistency, enabling minute-long video generation along challenging trajectories.

* 然后是 Method Overview 部分
## 🔬 Method overview
* 先插入图像 @assets/pipeline.png

**System overview.** For each target chunk, GEAR constructs patch correspondences to retrieved history using per-frame geometry and filters occluded matches with the Invisible Octree. GCA then injects matched historical features into noisy target tokens during denoising, after which generated observations are appended to the history bank for continued rollout.

* 然后是如下部分
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