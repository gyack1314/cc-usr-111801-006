# 长距离纯氢管道材料试验资料版本采集

现有项目保存管材报告与试验页的冻结响应。transport 核对请求与字节来源，domain 提取资料身份，ledger 原子保存原文与版本，view 呈现已接收资料及缺口。合成样例不访问真实站点；业务关联和完整性判断尚未实现。

Python 3.11 以上，在项目根目录执行：

    python -m unittest discover -s tests -v
    python -m compileall -q capture_service tests
    python -m capture_service.cli inspect data/normal.json

Docker 构建和运行：docker build -t hydrogen-collection-006 .；docker run --rm hydrogen-collection-006。
