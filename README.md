# Whole exome sequencing data analysis (WES data analysis)

## Курсовой проект по анализу NGS-данных.

### Описание проекта.

Репозиторий содержит материалы курсового проекта, выполняемого в 2025 году при обучении на программе Бластим "Анализ NGS-данных".

Тема проекта: Анализ экзома.

Куратор: Зарубин Алексей 

Самостоятельная работа “Анализ экзома”:

1.	Обработать экзомные данные согласно протоколу.
2.	Аннотировать варианты.
3.	Описать один потенциально самый патогенный вариант для каждого образца.
4.	Установить Y и MT гаплогруппы.

Папка с fastq данными: /home/prep01/data/fastq/Exome/fastq

Расположение bed файла с координатами для анализа: /home/prep01/data/reference/output_renamed.bed

Расположение референса: /home/prep01/data/reference/Full_genome

### Расположение исходных данных:

Папка reference: https://disk.yandex.ru/d/HbTFRsRMEf-ABw

Папка fastq: https://disk.yandex.ru/d/s-4c-c6zLxZ4rA

### Структура папок и файлов проекта:

* out - папка с результатами работы программ
  * fastqc - отчеты fastqc
  * gvcf - отчеты bcftools stats
  * multiqc_data - данные для отчета multiqc
  * qualimap - отчеты qualimap
  * * chr_all.wgs.genome
    * chr_all.wgs.log        - результаты работы plink (проверка на родство)
    * chr_all.wgs.nosex
  * * chr_all_final_renamed.avinput
    * chr_all_final_renamed.hg38_multianno.txt   - результаты работы annovar (аннотация)
    * chr_all_final_renamed.hg38_multianno.vcf
  * chr_all_final_renamed.vcf.gz - финальный файл .vcf с вариантами
  * * classify_Y.ClassificationLog.log
    * classify_Y.hapresult.hg           - результаты работы LineageTracker classify (определение гаплогрупп по Y-хромосоме)
    * classify_Y.lineageresult.txt
  * haplogroups.txt - результат работы haplogrep classify (определение гапрогруппы по митохондриальному геному)
  * multiqc_report.html - отчет multiqc
* .gitattributes - технический файл с обозначением больших файлов (LFS)
* Annovar.xlsx - результаты работы annovar в формате .xlsx
* SpirovaVV_WES_data_analysis_report.pdf - полный отчет по результатам проекта
* open_cravat.sqlite - результаты аннотации итогового .vcf в Open Cravat


### Дополнительные ресурсы:

Haplogrep 3: https://haplogrep.i-med.ac.at/

Open CRAVAT: https://run.opencravat.org/submit/nocache/index.html
