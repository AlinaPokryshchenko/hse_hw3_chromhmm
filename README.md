# Домашнее задание 3
## Часть 1
Клеточная линия, рассмотренная в ДЗ2 (DOHH2), не содержит ChIP-seq эксперименты в рассматриваемых гистоновых метках, 
поэтому я буду работать с клеточной линией Monocytes-CD14+_RO01746.
### Список гистоновых меток
Метка|Ссылка на файл
-----|--------------
H2az|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H2azAlnRep1.bam
H3k79me2|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H3k79me2AlnRep1.bam
H4k20me1|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H4k20me1AlnRep1.bam  
H3k04me2|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H3k04me2AlnRep1.bam  
H3k04me3|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H3k04me3AlnRep1.bam  
H3k09ac|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H3k09acAlnRep1.bam
H3k09me3|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H3k09me3AlnRep1.bam 
H3k27ac|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H3k27acAlnRep1.bam 
H3k27me3|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H3k27me3AlnRep1.bam  
H3k36me3|http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746H3k36me3AlnRep1.bam 

Ссылка на контроль: http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneMonocd14ro1746ControlAlnRep1.bam

### Выдача ChromHMM

![transitions](/results_10/transitions_10.png)|![emissions](/results_10/emissions_10.png)|![fold1](/results_10/Monocytes-CD14+_RO01746_10_overlap.png)|![fold2](/results_10/Monocytes-CD14+_RO01746_10_RefSeqTES_neighborhood.png)|![fold3](/results_10/Monocytes-CD14+_RO01746_10_RefSeqTSS_neighborhood.png)
 -|-|-|-|-

### Из геномного браузера
![1_genome](/images/1_genome.png)
![2_genome](/images/2_genome.png)
![3_genome](/images/3_genome.png)

### Итог
Состояние|1|2|3|4|5|6|7|8|9|10
Наиболее часто встречающиеся гистоновые метки|1|2|3|4|5|6|7|8|9|10
Области генома, в которых чаще встречаются|1|2|3|4|5|6|7|8|9|10
Как расположены относительно старта транскрипции|1|2|3|4|5|6|7|8|9|10
Как расположены относительно конца транскрипции|1|2|3|4|5|6|7|8|9|10
Состояния, которые часто расположены рядом|1|2|3|4|5|6|7|8|9|10
Итоговое название|1|2|3|4|5|6|7|8|9|10
