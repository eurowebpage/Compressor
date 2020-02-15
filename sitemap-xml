<?php
/*---------------------------------------------------------------------------------------*/
/*
   Compresse et décompresse un fichier sitemap.xml ou autre fichier extension  
   Exemple ici avec une extension .xml
*/
/*---------------------------------------------------------------------------------------*/

    function uncompress($srcName, $dstName) {
    $string = implode("", gzfile($srcName));
    $fp = fopen($dstName, "w");
    fwrite($fp, $string, strlen($string));
    fclose($fp);
    } 

    function compress($srcName, $dstName)
    {
    $fp = fopen($srcName, "r");
    $data = fread ($fp, filesize($srcName));
    fclose($fp);

    $zp = gzopen($dstName, "w9");
    gzwrite($zp, $data);
    gzclose($zp);
    }
?>
<?php

    // Compress Avec un fichier sitemap.xml pour l'exemple
    compress("sitemap.xml","sitemap.xml.gz");
     // uncompress Avec un fichier sitemap.xml.gz pour l'exemple
    // uncompress("sitemap.xml.gz","sitemap.xml");
?>
