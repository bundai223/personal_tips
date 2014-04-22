shellのtips
============

## sed
()でパターンをグループ化  
グループ化されたものは\1・\2などで置換文字列に使用できる

    ex.)
        filename="test.txt"
        echo $filename | sed -e "s/^\([^.]*\)\..*$/\1/g"
        test
        
        echo $filename | sed -e "s/^\([^.]*\)\..\(.*\)$/\1/g"
        test
        echo $filename | sed -e "s/^\([^.]*\)\..\(.*\)$/\2/g"
        txt

