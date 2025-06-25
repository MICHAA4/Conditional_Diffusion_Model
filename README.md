<h1 align='center'>Conditional Diffusion 모델을 이용한 2D Brain MRI 생성 및 평가 🧠</h1>

## 개요

전 세계 AI 의료 시장은 급성장 중이며, AI 기반 의료 영상 분석이 혁신적인 발전을 이루고 있다. 특히 조기 진단과 빠른 치료가 중요한 뇌 질환 분야에서 AI는 딥러닝 기술을 기반으로 CT, MRI와 같은 뇌 영상 분석을 통해 최적의 치료 방법을 찾는 데 도움을 주고 있다. 하지만 의료 정보 데이터의 제한된 공개성과 개인정보 보호 문제, 그리고 데이터 획득에 따른 높은 비용 등이 주요한 제약 요인으로 작용하고 있다.<br/>이를 해결하기 위해 생성형 AI를 활용한다. 생성형 AI를 통해 의료 데이터를 생성함으로써, 데이터 부족과 제한성을 극복하고 개인정보 보호 문제를 해결할 수 있다. 생성된 데이터는 실제 환자의 정보가 아니므로 개인정보 보호 우려가 줄어들어, 의료 데이터의 공개와 공유를 촉진할 수 있는 긍정적인 요소로 작용할 것으로 기대된다.<br/><br/>본 프로젝트에서는 Diffusion Model을 사용하여 의료 이미지를 생성했다. Diffusion Model은 데이터를 완전한 노이즈로 만드는 Forward Process와 그 노이즈를 다시 데이터로 복원하는 Reverse Process를 통해 새로운 이미지를 샘플링한다. 이 과정에서 이미지의 노이즈를 효과적으로 제거하고 세부 사항을 잘 복원할 수 있는 UNet 구조를 사용했다.<br/>Diffusion Model UNet에는 Classifier-Free Guidance 기법을 적용하여 다양한 조건을 줄 수 있다. 이 기법은 별도의 Classifier 학습 없이 조건부 이미지를 생성할 수 있게 한다. 조건 정보 반영 정도를 결정하는 하이퍼파라미터인 Guidance Scale 값이 샘플링 이미지의 품질과 다양성에 매우 중요하다. Guidance Scale 값이 클수록 조건 정보의 반영 정도는 증가하지만, 이미지 품질이 떨어지거나 왜곡이 발생할 수 있다. 따라서, Guidance Scale 값을 적절히 조절하여 FID와 SSIM 평가 지표를 사용해 최적의 값을 찾고자 한다.


## Development Period
2024.03 ~ 2024.06

## 👩🏻‍💻Member
<ul>
  <li><a href="https://github.com/ChaSeongYeon">차성연</a> @Cha SeongYeon</li>
</ul>

## Professor
<ul>
 <li><a href="https://wonhee-lee.github.io/">이원희</a> @Lee WonHee</li>
</ul>

## 📌Objectives
<ul>
 <li>Generate Realistic Brain 2D MRI</li>
 <li>Find The Optimal Guidance Scale Value</li>
</ul>

## Data
<ul>
  <li><a href="https://camcan-archive.mrc-cbu.cam.ac.uk/dataaccess/">Cam-CAN Dataset</a></li>
</ul>

## Result
|Age|Sex|Slice Number|Sampling Process|
|:-:|:-:|:----------:|----------------|
|48|2(Male)|25|![그림25](https://github.com/MICHAA4/Conditional_Diffusion_Model/assets/172036158/4a73accd-655d-4e7e-939e-e08014da5e9c)|
|48|2|35|![그림35](https://github.com/MICHAA4/Conditional_Diffusion_Model/assets/172036158/cce583ad-5081-4349-a8e4-469995d31809)|
|48|2|45|![그림45](https://github.com/MICHAA4/Conditional_Diffusion_Model/assets/172036158/85939030-7bfc-4f93-8527-544937e2b8b2)|
|48|2|55|![그림55](https://github.com/MICHAA4/Conditional_Diffusion_Model/assets/172036158/bc72a406-c928-460c-8a10-b8059c24682a)|

## How to Run
1. Clone MONAI repository
```
git clone https://github.com/Project-MONAI/MONAI
```
2. Clone this repository
```
git clone https://github.com/MICHAA4/capstone-conditional-diffusion-mri
```
3. Go to src folder
4. Execute the .ipynb files!

## Helpful Repositories
<ul>
  <li><a href="https://github.com/Project-MONAI/GenerativeModels">Project MONAI Generative Models</a> @Project-MONAI</li>
</ul>
