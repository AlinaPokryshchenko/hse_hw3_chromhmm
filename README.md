# Домашнее задание 3
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

Для более удобного определения какому состоянию соответствует тот или иной элемент генома, была создана таблица, в которой указаны места, где чаще всего располагаются гистоновые метки. Данные были взяты из статьи Ernst J, et al. Mapping and analysis of chromatin state dynamics in nine human cell types. Nature. 2011 и других статей, которые будут указаны далее

Источники:

H2az: (https://pubmed.ncbi.nlm.nih.gov/34643712/)

H3K79me2: (https://pubmed.ncbi.nlm.nih.gov/29665865/)

H3k09me3:(https://pubmed.ncbi.nlm.nih.gov/26675384/)

Гистоновая метка|H2az|H3k79me2|H4k20me1|H3k04me2|H3k04me3|H3k09ac|H3k09me3|H3k27ac|H3k27me3|H3k36me3	
-|-|-|-|-|-|-|-|-|-|-
Где чаще всего расположена|в транскрибируемых областях рядом с TSS усиляет экспрессию гена|участвует в альтернативном сплайсинге, поэтому располагается в активно транскрибируемых районах| в повторяющихся последовательностях и транскрибируемых районах|в сильных энхансерах и промоторах|в сильных промоторах и энхансерах|в сильных промоторах и энхансерах|супрессор в гетерохроматине|в сильных энхансерах и промоторах|в неактивных промоторах, повторяющихся областях, иногда в факультативном хроматине|в повторяющихся областях, в транскрибируемых областях

### Итог
Состояние|1|2|3|4|5|6|7|8|9|10
-|-|-|-|-|-|-|-|-|-|-
Наиболее часто встречающиеся гистоновые метки|H3K4me3, H3K4me2|H3K27ac|H3K79me2,H4K20me1,H3K27ac|H3K79me2, H4K20me1|H3K36me3|H3K9ac|H3K36me3|H3K9me3|-|H3K27me3 
Области генома, в которых чаще встречаются|CpG-островки, экзоны, старт транскрипции|ядерная ламина, TES|гены, расположение в 2kb от старта транскрипции|гены, ядерная ламина, расположение в 2kb от старта транскрипции, рядом с TES|экзоны, гены, рядом с TES|экзоны, гены, TES, ламина|экзоны, гены, TES|экзоны, ламина, TES|ламина (+занимает основную часть генома)|распределено равномерно
Как расположены относительно старта транскрипции|больше сконцентрированы перед, на и после TSS|располагаются до TSS|1000 нуклеотидов после TSS|1400 нуклеотидов после TSS|редко встречаются|редко встречаются|-|-|-|распределены равномерно
Как расположены относительно конца транскрипции|в основном до TES|распределены равномерно|-|встречаются редко после TES|сосредоточены до TES|чаще встречаются после TES|сосредоточены до TES|распределены равномерно|-|распределены равномерно
Состояния, которые часто расположены рядом|2,10|1,6,9|1,4|3,5|4,7|2,7|6|9|-|9
Итоговое название|сильный промотор|сильный энхансер|повторяющиеся последовательности в генах (возможно, какой-то регуляторный элемент, можно заметить на 1 скриншоте из геномного браузера, что данные последовательности расположены перед областями, с которых транскрибируются малые ядрышковые РНК (обозначены SNORD). Есть предположение, что данные области состояния 3 нужны для связывания РНК-полимеразы II типа, поскольку именно она транскрибирует мякРНК с интронов генов)|регуляторные последовательности|транскрибируемая область (transcriptional transition)|возможно, слабый промотор|транскрибируемая область (transcriptional elongation)|гетерохроматин|конститутивный гетерохроматин|факультативный гетерохроматин (Polycomb repressed)


