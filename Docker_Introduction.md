Docker Introduction
================

``` r
library()
search()
```

    ## [1] ".GlobalEnv"        "package:stats"     "package:graphics" 
    ## [4] "package:grDevices" "package:utils"     "package:datasets" 
    ## [7] "package:methods"   "Autoloads"         "package:base"

``` r
install.packages("seqinr",repos="https://cran.rstudio.com/") 
```

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

``` r
library(help="seqinr") 
library(seqinr)

#List all functions
ls("package:seqinr")
```

    ##   [1] "a"                       "aaa"                    
    ##   [3] "AAstat"                  "acnucclose"             
    ##   [5] "acnucopen"               "al2bp"                  
    ##   [7] "alllistranks"            "alr"                    
    ##   [9] "amb"                     "as.alignment"           
    ##  [11] "as.matrix.alignment"     "as.SeqAcnucWeb"         
    ##  [13] "as.SeqFastaAA"           "as.SeqFastadna"         
    ##  [15] "as.SeqFrag"              "autosocket"             
    ##  [17] "baselineabif"            "bma"                    
    ##  [19] "c2s"                     "cai"                    
    ##  [21] "cfl"                     "choosebank"             
    ##  [23] "circle"                  "clfcd"                  
    ##  [25] "clientid"                "closebank"              
    ##  [27] "col2alpha"               "comp"                   
    ##  [29] "computePI"               "con"                    
    ##  [31] "consensus"               "count"                  
    ##  [33] "countfreelists"          "countsubseqs"           
    ##  [35] "crelistfromclientdata"   "css"                    
    ##  [37] "dia.bactgensize"         "dia.db.growth"          
    ##  [39] "dist.alignment"          "dotchart.uco"           
    ##  [41] "dotPlot"                 "draw.oriloc"            
    ##  [43] "draw.rearranged.oriloc"  "draw.recstat"           
    ##  [45] "exseq"                   "extract.breakpoints"    
    ##  [47] "extractseqs"             "fastacc"                
    ##  [49] "gb2fasta"                "gbk2g2"                 
    ##  [51] "gbk2g2.euk"              "GC"                     
    ##  [53] "GC1"                     "GC2"                    
    ##  [55] "GC3"                     "GCpos"                  
    ##  [57] "get.db.growth"           "getAnnot"               
    ##  [59] "getAnnot.default"        "getAnnot.list"          
    ##  [61] "getAnnot.logical"        "getAnnot.qaw"           
    ##  [63] "getAnnot.SeqAcnucWeb"    "getAnnot.SeqFastaAA"    
    ##  [65] "getAnnot.SeqFastadna"    "getAttributsocket"      
    ##  [67] "getFrag"                 "getFrag.character"      
    ##  [69] "getFrag.default"         "getFrag.list"           
    ##  [71] "getFrag.logical"         "getFrag.qaw"            
    ##  [73] "getFrag.SeqAcnucWeb"     "getFrag.SeqFastaAA"     
    ##  [75] "getFrag.SeqFastadna"     "getFrag.SeqFrag"        
    ##  [77] "getKeyword"              "getKeyword.default"     
    ##  [79] "getKeyword.list"         "getKeyword.logical"     
    ##  [81] "getKeyword.qaw"          "getKeyword.SeqAcnucWeb" 
    ##  [83] "getLength"               "getLength.character"    
    ##  [85] "getLength.default"       "getLength.list"         
    ##  [87] "getLength.logical"       "getLength.qaw"          
    ##  [89] "getLength.SeqAcnucWeb"   "getLength.SeqFastaAA"   
    ##  [91] "getLength.SeqFastadna"   "getLength.SeqFrag"      
    ##  [93] "getlistrank"             "getliststate"           
    ##  [95] "getLocation"             "getLocation.default"    
    ##  [97] "getLocation.list"        "getLocation.logical"    
    ##  [99] "getLocation.qaw"         "getLocation.SeqAcnucWeb"
    ## [101] "getName"                 "getName.default"        
    ## [103] "getName.list"            "getName.logical"        
    ## [105] "getName.qaw"             "getName.SeqAcnucWeb"    
    ## [107] "getName.SeqFastaAA"      "getName.SeqFastadna"    
    ## [109] "getName.SeqFrag"         "getNumber.socket"       
    ## [111] "getSequence"             "getSequence.character"  
    ## [113] "getSequence.default"     "getSequence.list"       
    ## [115] "getSequence.logical"     "getSequence.qaw"        
    ## [117] "getSequence.SeqAcnucWeb" "getSequence.SeqFastaAA" 
    ## [119] "getSequence.SeqFastadna" "getSequence.SeqFrag"    
    ## [121] "getTrans"                "getTrans.character"     
    ## [123] "getTrans.default"        "getTrans.list"          
    ## [125] "getTrans.logical"        "getTrans.qaw"           
    ## [127] "getTrans.SeqAcnucWeb"    "getTrans.SeqFastadna"   
    ## [129] "getTrans.SeqFrag"        "getType"                
    ## [131] "gfrag"                   "ghelp"                  
    ## [133] "gln"                     "glr"                    
    ## [135] "gls"                     "is.SeqAcnucWeb"         
    ## [137] "is.SeqFastaAA"           "is.SeqFastadna"         
    ## [139] "is.SeqFrag"              "isenum"                 
    ## [141] "isn"                     "kaks"                   
    ## [143] "kdb"                     "knowndbs"               
    ## [145] "lseqinr"                 "modifylist"             
    ## [147] "move"                    "mv"                     
    ## [149] "n2s"                     "oriloc"                 
    ## [151] "parser.socket"           "peakabif"               
    ## [153] "permutation"             "pga"                    
    ## [155] "plot.SeqAcnucWeb"        "plotabif"               
    ## [157] "plotladder"              "plotPanels"             
    ## [159] "pmw"                     "prepgetannots"          
    ## [161] "prettyseq"               "print.qaw"              
    ## [163] "print.SeqAcnucWeb"       "query"                  
    ## [165] "quitacnuc"               "read.abif"              
    ## [167] "read.alignment"          "read.fasta"             
    ## [169] "readBins"                "readfirstrec"           
    ## [171] "readPanels"              "readsmj"                
    ## [173] "rearranged.oriloc"       "recstat"                
    ## [175] "residuecount"            "reverse.align"          
    ## [177] "rho"                     "rot13"                  
    ## [179] "s2c"                     "s2n"                    
    ## [181] "savelist"                "SEQINR.UTIL"            
    ## [183] "setlistname"             "splitseq"               
    ## [185] "stresc"                  "stutterabif"            
    ## [187] "summary.SeqFastaAA"      "summary.SeqFastadna"    
    ## [189] "swap"                    "syncodons"              
    ## [191] "synsequence"             "tablecode"              
    ## [193] "test.co.recstat"         "test.li.recstat"        
    ## [195] "translate"               "trimSpace"              
    ## [197] "uco"                     "ucoweight"              
    ## [199] "where.is.this.acc"       "words"                  
    ## [201] "words.pos"               "write.fasta"            
    ## [203] "zscore"

``` r
#List available datasets
data(package="seqinr")

#Load dataset aaindex
data(aaindex, package="seqinr") 
?aaindex #It is a list of 544 physicochemical and biological properties for the 20 amino-acids
```

``` r
#Use data to plot AA by hydrophobicity and volume
plot(aaindex$FASG890101$I,
     aaindex$PONJ960101$I,
     xlab="hydrophobicity", ylab="volume", type="n")
text(aaindex$FASG890101$I,
     aaindex$PONJ960101$I,
     labels=a(names(aaindex$FASG890101$I)))
```

![](Docker_Introduction_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

``` r
#Barplot exercise
seqinr::choosebank("swissprot")
mySeq <- seqinr::query("mySeq", "N=MBP1_YEAST")
mbp1 <- seqinr::getSequence(mySeq)
seqinr::closebank()
x <- seqinr::AAstat(mbp1[[1]])
```

![](Docker_Introduction_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

``` r
barplot(sort(x$Compo), cex.names = 0.6)
```

![](Docker_Introduction_files/figure-gfm/unnamed-chunk-3-2.png)<!-- -->
