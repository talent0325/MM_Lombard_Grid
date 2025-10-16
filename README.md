# 通用
1. 每个方法下有loop类的，即一次性循环处理，一般需要修改的搜索 MARK和TODO
2. 跑代码之前检查，token/API key是否替换，文件保存路径是否替换，
3. 可以把之前生成的文件全部添加_backup后缀，注意不是删除
4. 根据/data2/cy/0_MM_Lombard_Deepfake/assets/speakers/test.json可以小批量测试是否读取正确（可以将这个文件改的更少，免得浪费额度）
5. 要修改运行文件时，新建文件，添加后缀 _v{id}，不要在原始文件修改
6. 下列方法没说到的文件或者文件夹不需要管（也可能有遗漏，有问题问我就行）
7. 之前的loop的逻辑结构是手敲的 需要自己读取文件来获得，后续更新，或者自己修改
8. API方法有时候loop会出错，不行就单个请求
9. 修改所有需要url（github）访问的资源父路径，与之前的相比有变化
10. 命名要修改 形如 "speaker_utterance_method" （之前的代码实现没有加method） 可以不修改源代码的基础上在自己的路径得到vidoes， 再用脚本批量修改


# API
## loopy
网址：[loopy(即梦人)] (https://www.volcengine.com/docs/85621/1810468#g3wIHs7A) 注册
> 1. 在[即梦AI - 一站式AI创作平台](https://jimeng.jianying.com/ai-tool/home/?utm_medium=aitools&utm_source=aibot&utm_campaign=null&utm_content=hw_jm_aibot)登录，左侧下方有个API点击进入
> 2. 跳转后登录开通数字人快速模型（免费版，需要实名认证）
> 3. 获取密钥和ID等（右上角头像悬停后点击API访问密钥）

/data2/cy/0_MM_Lombard_Deepfake/5_loopy

./response/ 存放过程文件的目录，存放时改为自己的名字最好

./videos/ demo时生成文件的地址，测试时可以用这个地址

./batch_request.py 批量提交任务

/data2/cy/0_MM_Lombard_Deepfake/5_loopy/request.py -> 1个speaker对应1个utterance（wav文件）的请求

./query.py  ->  指定单独1个task_id查询结果

./loop_body 自动下载不可用 容易出错 不推荐

## SyncLabs
环境： conda activate syncsdk
[官网](https://sync.so/projects)
[说明文档](https://docs.sync.so/introduction)

使用 lipsync-1.9.0-beta 便宜一半 视频要模糊一点

免费的有水印 开通19美元的才没有水印, 可以再看看官方文档研究下，运行代码已写好，看怎么开通 或者怎么处理水印

./batch 是并发执行，具体可参考说明文档

./demo.py 指定一对speaker和utterance得到生成视频的下载地址

## 




 