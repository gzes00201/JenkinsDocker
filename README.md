# 给脚本授权
chmod u+x *.sh
# 创建Jenkins数据目录（用作持久卷）
sudo ./pre_install_jenkins.sh
# 启动Jenkins容器
docker-compose up -d
# 進入Jenkins容器
docker exec -it 容器編號 /bin/bash
# 取的Jenkins金鑰
cat /var/jenkins_home/secrets/initialAdminPassword
# 初始化動作
1.開啟 http://localhost:8081/ 並貼上
2.Install suggested plugins
3.依畫面指示完成
4.進入後如果畫面為白頁,請重啟container