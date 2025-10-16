# 通用
1. 每个方法下有loop类的，即一次性循环处理，一般需要修改的搜索 MARK和TODO
2. 跑代码之前检查，token/API key是否替换，文件保存路径是否替换，
3. 可以把之前生成的文件全部添加_backup后缀，注意不是删除
4. 根据/data2/cy/0_MM_Lombard_Deepfake/assets/speakers/test.json可以小批量测试是否读取正确（可以将这个文件改的更少，免得浪费额度）
5. 要修改运行文件时，新建文件，添加后缀 _v{id}，不要在原始文件修改
6. 下列方法没说到的文件或者文件夹不需要管（也可能有遗漏，有问题问我就行）
7. 之前的loop的逻辑结构是手敲的 需要自己读取文件来获得，后续更新，或者自己修改
8. API方法有时候loop会出错，不行就单个请求

# API
## loopy
/data2/cy/0_MM_Lombard_Deepfake/5_loopy

./response/ 存放过程文件的目录，存放时改为自己的名字最好

./videos/ demo时生成文件的地址，测试时可以用这个地址

./batch_request.py 批量提交任务

/data2/cy/0_MM_Lombard_Deepfake/5_loopy/request.py -> 1个speaker对应1个utterance（wav文件）的请求

./query.py  ->  指定单独1个task_id查询结果

./loop_body 自动下载不可用 容易出错 不推荐




 