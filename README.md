scheduler-research
==================

计算科学研究实践笔记
import time
import linecache
import os
while 1:
    tf = open('/Users/ctj12/Music/muluwenjian.txt','r')
    #    tf.readlines=tf.readlines.strip('\n')
    for line1 in tf.readlines():
        line1 = line1[:-1]
        i = open(line1,'r')
        for line in  i.readlines()[len(i.readlines())-2:len(i.readlines())-1]:
            print(line)
    
        time.sleep(1)
    
        output = open('/Users/ctj12/Music/dushu.txt','r')
        output.write(line1)
        output.write(str(line))
        output.close()
#
从表中读出每个sensor温度所在的路径，然后把温度倒数第二个读出来写进一个txt文档中，不读倒数第一个的原因是因为有可能有个raspberry pi还没读倒数第一个数 有的已经读取了 这样会使得时间上参差不齐
然后比较大小，找出最大的跟最小的
