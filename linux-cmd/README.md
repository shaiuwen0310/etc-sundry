# linux指令記錄

1. 查看容量
    ```
    sudo du -smc . ; echo "---"; sudo du -shc . ; echo "---"; date +%Y-%m-%d
    ```

2. iotop: 監看每支程式讀寫硬碟的情形
    ```
    顯示成累計讀寫硬碟的資料量: sudo iotop -a
    只會顯示正在讀寫硬碟的程式: sudo iotop -o

    設定 iotop 更新的頻率，預設是 1 秒鐘: sudo iotop -d 10

    針對某一支正在執行中的程式來監看: sudo iotop -p 3093

    批次方式產出三次資料到 io.log 檔案，然後，只產出正在讀取硬碟中的程式: sudo iotop -bot -n 10 > io.log

    ```

3. top sort by memory
    ```
    top -b -o +%MEM | head -n 13 > test.log
    ```

4. linux上錄影：Kazam
    ```sh
    # 安裝kazam
    sudo apt-get install kazam

    # 使用fmpeg轉檔給windows播放
    sudo apt install ffmpeg
    # 轉檔：無音源
    ffmpeg -i test.mp4 -pix_fmt yuv420p -c:a copy -movflags +faststart output.mp4
    # 轉檔：有音源
    ffmpeg -i test.mp4 -c:a copy -movflags +faststart output.mp4
    ```
