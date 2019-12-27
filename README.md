# clover
A Simple and Easy-to-Use Automated Testing Platform

# deploy
1. copy all the files in ./front/dist to nginx
2. start clover use `python3 clover.py runserver`
3. start nginx use `nginx -c nginx.conf`

# Development Plan
1. keyword support
2. test report
3. hook & fixture
4. use mysql replace mongodb
5. async-validator

# 关注公众号，学习更多测试知识。
![大猫聊测试][wechat]
[wechat]:data:image/jpg;base64,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

