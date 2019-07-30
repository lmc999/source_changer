# source_changer
script to change source for linux

三、用法
wget  git.io/superupdate.sh

bash superupdate.sh

使用 wget -qO- git.io/superupdate.sh | bash 也可一键换源，如果第一步你出现错误或执行后无任何输出，请检查是否安装 wget 和 ca-certificates，请使用

apt-get install -y wget && apt-get install -y ca-certificates

或者

yum install -y wget && yum install -y ca-certificates

对于 Debian 默认换源为 Fastly CDN 的 mirror 这个源有 Fastly 的加持对境外主机都有不错的速度。 对于 Ubuntu 和 CentOS 系统都默认换为阿里云的 mirror 这个源有阿里云全球 CDN 的加持，全球都有不错的速度。

对于 Debian 系统还设置了四套其他的源，阿里云，CloudFront CDN，网易163，中科大的源，请根据需要使用参数一键设置如

bash superupdate.sh cn

bash superupdate.sh 163

bash superupdate.sh aliyun

bash superupdate.sh aws

如果配置的文件不满意，一键还原

bash superupdate.sh restore
