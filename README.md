# hse_hw3_chromhmm
 Ссылка на колаб: https://colab.research.google.com/drive/1l4EM_ofKS7mZGYGwGKCzaliN-A1a3Y6F?usp=sharing
 
 В прошлом дз я использовала клеточнуую линию H1, так как её я не нашла, в этом дз будет проанализирована клеточная линия H1-hESC
 
 ## Таблица гистоновых меток
Name | File
--- | ---
H3k09me3 | wgEncodeBroadHistoneH1hescH3k09me3StdAlnRep1.bam
H3k4me1 | wgEncodeBroadHistoneH1hescH3k4me1StdAlnRep1.bam
H3k4me2 | wgEncodeBroadHistoneH1hescH3k4me2StdAlnRep1.bam
H3k4me3 | wgEncodeBroadHistoneH1hescH3k4me3StdAlnRep1.bam
H3k9ac | wgEncodeBroadHistoneH1hescH3k9acStdAlnRep1.bam
H3k27ac | wgEncodeBroadHistoneH1hescH3k27acStdAlnRep1.bam
H3k36me3 | wgEncodeBroadHistoneH1hescH3k36me3StdAlnRep1.bam
H3k79me2 | wgEncodeBroadHistoneH1hescH3k79me2StdAlnRep1.bam
H4k20me1 | wgEncodeBroadHistoneH1hescH4k20me1StdAlnRep1.bam
H3K27me3 | wgEncodeBroadHistoneH1hescH3k27me3StdAlnRep1.bam

## Файл cellmarkfiletable.txt
Клеточная линия | Гистоновая метка | Файл с гистоновой меткой | Файл с контролем
--- | --- | --- | ---
H1-hESC | H3K09me3 | H3K09me3.bam | Control.bam
H1-hESC | H3k4me1 | H3k4me1.bam | Control.bam
H1-hESC | H3k4me2 | H3k4me2.bam | Control.bam
H1-hESC | H3k4me3 | H3k4me3.bam | Control.bam
H1-hESC | H3k9ac | H3k9ac.bam | Control.bam
H1-hESC | H3k27ac | H3k27ac.bam | Control.bam
H1-hESC | H3k36me3 | H3k36me3.bam | Control.bam
H1-hESC | H3k79me2 | H3k79me2.bam | Control.bam
H1-hESC | H4k20me1 | H4k20me1.bam | Control.bam
H1-hESC | H3K27me3 | H3K27me3.bam | Control.bam

## Таблица ChromHMM

Emission | Overlap | Transition 
 --- | --- | ---
![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/emissions_15.png) | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/H1-hESC_15_overlap.png) | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/transitions_15.png)

RefSeqTSS | RefSeqTES 
 --- | --- 
![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/H1-hESC_15_RefSeqTSS_neighborhood.png) | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/H1-hESC_15_RefSeqTES_neighborhood.png)

## Эпигенетические типы
№ | Название | Описание | Картинка
 --- | --- | ---| ---
1 | Active Promoter | <ul><li> выражен в H3K27me3 </li><li> Чаще всего находятся на RefSeqTES, RefSeqExon, RefSeqGene, RefSeqTSS2Kb, а также на ядерной ламине </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/1.png)
2 | Weak enhancer/Weak transcribed | <ul><li> выражен в H3K27me3, H3K4me2, H3K4me1 </li><li> Чаще всего находятся на RefSeqTES, RefSeqExon, CpGIslands </li><li> Попадает на интрон или экзон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/2.png)
3 | Strong enhancer/Transcriptional elogation | <ul><li> выражен в H3K27me3, H3K4me2, H3K4me3, H3K4me1 </li><li> Чаще всего находятся на RefSeqTES и RefSeqTSS2Kb, а также на ядерной ламине </li><li> Попадает на интрон или экзон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/3.png)
4 | Active Promoter | <ul><li> выражен в H3K4me3, H3K4me2, H3K9ac </li><li> Чаще всего находятся на CpGIslands, RefSeqTES, RefSeqExon и RefSeqTSS2Kb </li><li> Попадает на интрон или экзон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/4.png)
5 | Active Promoter | <ul><li> выражен в H3K9ac, H3K27ac, H3K4me3, H3K4me2, H3K79me2 </li><li> Чаще всего находятся на RefSeqTES и RefSeqTSS2Kb, а также на RefSeqExon, CpGIslands, и RefSeqGene </li><li> Попадает на интрон или экзон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/5.png)
6 | Weak enhancer | <ul><li> выражен в H3K4me2, H3K4me1 </li><li> Чаще всего находятся на RefSeqGene и RefSeqTES, а также RefSeqExon, но реже </li><li> Попадает на интрон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/6.png)
7 | Weak enhancer | <ul><li> выражен в  H3K79me2, H3K4me2, H3K4me3 </li><li> Чаще всего находятся на RefSeqTES </li><li> Попадает на интрон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/7.png)
8 | Weak enhancer | <ul><li> выражен в  H3K79me2 </li><li> Чаще всего находятся на RefSeqTES, а также на ядерной ламине, но реже </li><li> Попадает на интрон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/8.png)
9 | Weak enhancer | <ul><li> выражен в  H3K79me2 </li><li> Чаще всего находятся на RefSeqGene, а также RefSeqTES и RefSeqExon, но реже </li><li> Попадает на интрон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/9.png)
10 | Weak transcribed | <ul><li> нигде не выражен </li><li> Чаще всего находятся на RefSeqGene </li><li> Попадает на экзон или интрон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/10.png)
11 | Weak transcribed | <ul><li> выражен в H3K36me3 </li><li> Чаще всего находятся на RefSeqGene, а также на RefSeqTES и RefSeqExon, но реже </li><li> Попадает на экзон или интрон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/11.png)
12 | Weak transcribed | <ul><li> выражен в H3K36me3, H3K09me3 </li><li> Чаще всего находятся на RefSeqGene, а также на RefSeqTES и RefSeqExon, но реже </li><li> Попадает на экзон или интрон </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/12.png)
13 | Repressed | <ul><li> выражен в H3K09me3 </li><li> Чаще всего находятся на ядерной ламине, то есть попадает на участок репрессированного гетерохроматима </li><li> Не попадает на ген </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/13.png)
14 | Heterochromatin | <ul><li> нигде не выражен  </li><li> Чаще всего находятся на ядерной ламине, то есть попадает на участок репрессированного гетерохроматима </li><li> Не попадает на ген </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/14.png)
15 | Heterochromatin | <ul><li> выражен в H3K4me1 </li><li> Чаще всего находятся на ядерной ламине, то есть попадает на участок репрессированного гетерохроматима </li> | ![Image](https://github.com/Lenassskuh/hse_hw3_chromhmm/blob/main/data/15.png)

