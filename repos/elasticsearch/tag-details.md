<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.23`](#elasticsearch6823)
-	[`elasticsearch:7.17.0`](#elasticsearch7170)
-	[`elasticsearch:8.0.0`](#elasticsearch800)

## `elasticsearch:6.8.23`

```console
$ docker pull elasticsearch@sha256:deda76957c8cacc5dbf0d535fd14fe365f37d839813099bc32f26390a5e232dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `elasticsearch:6.8.23` - linux; amd64

```console
$ docker pull elasticsearch@sha256:71d4f7d890b90d277a1677d53f100139dcb39a34e9aac1138bfbf272c878a9cf
```

-	Docker Version: 20.10.10
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 MB (492666994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2652c5f453b2f21ac32f841a6ed1897097741d69a1a4cc1947f58fae0d04b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Jan 2022 21:35:20 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 06 Jan 2022 21:35:21 GMT
ENV JAVA_HOME=/opt/jdk-15.0.1+9
# Thu, 06 Jan 2022 21:35:26 GMT
COPY dir:8d79ae5f21bb18379c0d92b3d252f4730fec22a4509252ec794212b8f72bd7af in /opt/jdk-15.0.1+9 
# Thu, 06 Jan 2022 21:36:34 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Thu, 06 Jan 2022 21:36:38 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Thu, 06 Jan 2022 21:36:38 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 06 Jan 2022 21:36:42 GMT
COPY --chown=1000:0dir:b97ce01feda46ea896b080aa40faf3a7efc9341727b688e691ee0eac86058c3a in /usr/share/elasticsearch 
# Thu, 06 Jan 2022 21:36:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 21:36:44 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 06 Jan 2022 21:36:45 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Thu, 06 Jan 2022 21:36:46 GMT
EXPOSE 9200 9300
# Thu, 06 Jan 2022 21:36:46 GMT
LABEL org.label-schema.build-date=2022-01-06T21:30:50.087716Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4f67856884ff580d8b48a858411b8c17cb0f8cdb org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.23 org.opencontainers.image.created=2022-01-06T21:30:50.087716Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=4f67856884ff580d8b48a858411b8c17cb0f8cdb org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.23
# Thu, 06 Jan 2022 21:36:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 06 Jan 2022 21:36:46 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d2262411d0f2af035c2e0f0c62814960b3e7d77eecab02eba9f97819d00d2e`  
		Last Modified: Thu, 13 Jan 2022 16:11:26 GMT  
		Size: 207.7 MB (207657716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa3bfe04943870deba40892398c3fc9d08da9825ea7953984632c74e4994bd`  
		Last Modified: Thu, 13 Jan 2022 16:11:18 GMT  
		Size: 58.2 MB (58240591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e780d91c9f56dc0a05ae8916a4e8d6738cf94ed5cf924534d41236da5fb38f`  
		Last Modified: Thu, 13 Jan 2022 16:11:06 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2471af457050139c5057c781433abadb769786df91ecbe6ed2a59b5f85e50369`  
		Last Modified: Thu, 13 Jan 2022 16:11:20 GMT  
		Size: 150.7 MB (150664745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca890dfc68d05cdbdd9a7f528fbe8707c05d71e8c0c985307da6797ad204eb49`  
		Last Modified: Thu, 13 Jan 2022 16:11:05 GMT  
		Size: 2.1 KB (2065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85b0b895822b5794063d98df42deeb3f0110f505b79fff7abc26f54f70a9c5`  
		Last Modified: Thu, 13 Jan 2022 16:11:05 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.17.0`

```console
$ docker pull elasticsearch@sha256:332c6d416808f6e9a2cbcbe0170d9a9bb14bfe772180d37de5084c223dd8948b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.17.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:fa7141154a7e14df214e42f08c333702403eb88c02ba44e79322a1f42d733013
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350591762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe993d6e7ed5e00a18f9b146d867b77559bf9948e6596bbf880ddbefeec46f7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 28 Jan 2022 12:05:21 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Fri, 28 Jan 2022 12:05:22 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Fri, 28 Jan 2022 12:05:22 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 28 Jan 2022 12:05:22 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 28 Jan 2022 12:05:29 GMT
COPY --chown=0:0dir:cc54df79fe8a5e928e5ca064c25f72a822150f206c4c478c96d7b75ca58b37ef in /usr/share/elasticsearch 
# Fri, 28 Jan 2022 12:05:32 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Fri, 28 Jan 2022 12:05:32 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jan 2022 12:05:33 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Jan 2022 12:05:33 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Fri, 28 Jan 2022 12:05:33 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Fri, 28 Jan 2022 12:05:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Fri, 28 Jan 2022 12:05:34 GMT
EXPOSE 9200 9300
# Fri, 28 Jan 2022 12:05:34 GMT
LABEL org.label-schema.build-date=2022-01-28T12:02:58.245119914Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=bee86328705acaa9a6daede7140defd4d9ec56bd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.0 org.opencontainers.image.created=2022-01-28T12:02:58.245119914Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=bee86328705acaa9a6daede7140defd4d9ec56bd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.0
# Fri, 28 Jan 2022 12:05:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 28 Jan 2022 12:05:35 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49618e7bd315f1c1a942faac0e070e06f4df20e20619e69a2ef020f551db6a23`  
		Last Modified: Tue, 01 Feb 2022 20:10:45 GMT  
		Size: 8.7 MB (8651520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2c6f1952450c8b924d4b59ac6c6fa1603ebc6a836fb4792f003a19af278c38`  
		Last Modified: Tue, 01 Feb 2022 20:10:42 GMT  
		Size: 4.4 KB (4370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32ac7edc3c3a90c1e3061d077709c06a2f26e6cbaf1935f5380b4b0a6a511ec`  
		Last Modified: Tue, 01 Feb 2022 20:11:23 GMT  
		Size: 313.1 MB (313061525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e392fc2cc0c9ad8b617ab3fb061abfcd0c452348b1115bdfb36668fa4708e6`  
		Last Modified: Tue, 01 Feb 2022 20:10:40 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aff618a926422f798f4d10876441d3bb83de6ded15f6c4759ca080361e70d98`  
		Last Modified: Tue, 01 Feb 2022 20:10:39 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795bd33f4eb3201c206d795d375144555b25171925938b36139c62d421c311fb`  
		Last Modified: Tue, 01 Feb 2022 20:10:40 GMT  
		Size: 192.1 KB (192132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1c10cef7663c14ce9d4be2d9887d4659655647ad55fa4eaab3d06cf9593454`  
		Last Modified: Tue, 01 Feb 2022 20:10:38 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf47933dd3496f80ea3a0066f1954fd2db182f0cfe2b3717f6feb557d26d995`  
		Last Modified: Tue, 01 Feb 2022 20:10:36 GMT  
		Size: 103.9 KB (103867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.17.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:65eb4626069e48af12a04cf4644bd91232e4b632c975ca8f66ea5a109fa2fc20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.5 MB (345542948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc21d367dc945eb5f7050e2ceb3ff9f433243f44bb1f2da509954bb8c86cd04`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 28 Jan 2022 12:07:44 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Fri, 28 Jan 2022 12:07:45 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Fri, 28 Jan 2022 12:07:45 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 28 Jan 2022 12:07:45 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 28 Jan 2022 12:07:49 GMT
COPY --chown=0:0dir:88ef2d6995d2dc58aa6387f34871bc9a41b3d78c938672db39fa7b3d1004a980 in /usr/share/elasticsearch 
# Fri, 28 Jan 2022 12:07:53 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Fri, 28 Jan 2022 12:07:53 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jan 2022 12:07:53 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Jan 2022 12:07:54 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Fri, 28 Jan 2022 12:07:54 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Fri, 28 Jan 2022 12:07:55 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Fri, 28 Jan 2022 12:07:55 GMT
EXPOSE 9200 9300
# Fri, 28 Jan 2022 12:07:55 GMT
LABEL org.label-schema.build-date=2022-01-28T12:05:44.004252578Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=bee86328705acaa9a6daede7140defd4d9ec56bd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.0 org.opencontainers.image.created=2022-01-28T12:05:44.004252578Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=bee86328705acaa9a6daede7140defd4d9ec56bd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.0
# Fri, 28 Jan 2022 12:07:55 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 28 Jan 2022 12:07:55 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67ee43c98e6c0e746367e01ba7482b48882c682c03e3198dd514a0218e675d8`  
		Last Modified: Fri, 04 Feb 2022 03:16:03 GMT  
		Size: 8.5 MB (8478175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7998ff34fd1545aac17a2ef81907070cfdfd677d8c23fdd8e6d4e9437574ac1`  
		Last Modified: Fri, 04 Feb 2022 03:16:01 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1614b74e2b87bd9ec48179f944b9b4cba325cdd001ae94bdb01db10f1519f004`  
		Last Modified: Fri, 04 Feb 2022 03:16:29 GMT  
		Size: 309.6 MB (309587837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b8b9424b560ea9e82126e4ae4b9004d375fab159d30b17ee66bef41fa13d18`  
		Last Modified: Fri, 04 Feb 2022 03:15:58 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126098657dccc046a323a7bc5370c52048647ba9eb09d477df051e3ba30c5763`  
		Last Modified: Fri, 04 Feb 2022 03:15:58 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91169c979fed03df5aa95831ce1ef65fa14a4a6f2a8f7022694ff522e868a42`  
		Last Modified: Fri, 04 Feb 2022 03:15:58 GMT  
		Size: 186.1 KB (186142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfccbacadc114eeca5ed428e03c96b63d1c330539f3c49ded5c23a614a1b3e2a`  
		Last Modified: Fri, 04 Feb 2022 03:15:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9a039049ffe70d17b39fe59ca8117e9cb531f02a6a1dbd6cd93a21e58b4481`  
		Last Modified: Fri, 04 Feb 2022 03:15:59 GMT  
		Size: 103.9 KB (103867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.0.0`

```console
$ docker pull elasticsearch@sha256:19f79b36495507ec53867ab40acaae448a9baa7820fb843be8cb5ede670bac5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.0.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:959a17340492d563dfd09745a9b13fd58cd2857b2475b2affaac310ff03d7090
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.9 MB (558902869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef75c42834fe3e0ddec4be2a6f929bbe5b1d7a8d41230c05e1485545f8d9433`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Thu, 03 Feb 2022 22:55:19 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 03 Feb 2022 22:55:19 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 03 Feb 2022 22:55:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 03 Feb 2022 22:55:20 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 03 Feb 2022 22:55:33 GMT
COPY --chown=0:0dir:efc5ac24d0086aaea7de0ed5f9bdcbcffad9249e504b481fc39e29555afea12d in /usr/share/elasticsearch 
# Thu, 03 Feb 2022 22:55:37 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Thu, 03 Feb 2022 22:55:37 GMT
COPY --chown=0:0dir:b581b730e5b7ee3ec0eabb697a9ee0c5d9c3c7f14aa330f554a9bb2db8474887 in /usr/local/cloudflare-zlib 
# Thu, 03 Feb 2022 22:55:37 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 22:55:37 GMT
ENV ES_ZLIB_PATH=/usr/local/cloudflare-zlib/lib
# Thu, 03 Feb 2022 22:55:37 GMT
COPY file:bd241387dbc1b05c0872607dd207d3a5b10dfd812f1441a5b215a7e5436fca23 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 03 Feb 2022 22:55:38 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 03 Feb 2022 22:55:38 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 03 Feb 2022 22:55:39 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 03 Feb 2022 22:55:39 GMT
EXPOSE 9200 9300
# Thu, 03 Feb 2022 22:55:39 GMT
LABEL org.label-schema.build-date=2022-02-03T22:52:11.916594404Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1b6a7ece17463df5ff54a3e1302d825889aa1161 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.0.0 org.opencontainers.image.created=2022-02-03T22:52:11.916594404Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1b6a7ece17463df5ff54a3e1302d825889aa1161 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.0.0
# Thu, 03 Feb 2022 22:55:39 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 03 Feb 2022 22:55:39 GMT
CMD ["eswrapper"]
# Thu, 03 Feb 2022 22:55:39 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e05ed2996f33f43984062b4364926ada8e374b635945b53b77114ff43c7732`  
		Last Modified: Fri, 11 Feb 2022 00:06:10 GMT  
		Size: 8.2 MB (8235042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b224114dffc05f7908ec1b7a2be02be34abccf6138042c0802d008755b03dae`  
		Last Modified: Fri, 11 Feb 2022 00:06:03 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cea41c41579d57421484d486681cdd96ab99627a055f93110e130435ad5663`  
		Last Modified: Fri, 11 Feb 2022 00:12:58 GMT  
		Size: 521.6 MB (521644766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b9aaf2174b4a84a256c89b6d9fcc8b9267a68e76b4a1a66f25393cb2a22a70`  
		Last Modified: Fri, 11 Feb 2022 00:06:03 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1679a442dce4631d50263d98aedb31a556d962c2e970b5efed03fa8cd659a3`  
		Last Modified: Fri, 11 Feb 2022 00:06:04 GMT  
		Size: 147.2 KB (147242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc605bce0f66cf85cfb0ceab6e15041f0af22e01f8a8a59e6e4a3ca9783569c8`  
		Last Modified: Fri, 11 Feb 2022 00:05:56 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b56a738e2fc2c8726ac24170590b5893d3f3042c39329e8c9a575f34e928c1`  
		Last Modified: Fri, 11 Feb 2022 00:05:57 GMT  
		Size: 191.8 KB (191842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8103eda51ee3c47083c241c36d643ec1f760fe4fba56c8dee250a6f7486bc`  
		Last Modified: Fri, 11 Feb 2022 00:05:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d3a89ee02dd73a05758523b9840b9b44deaa52238550f33eefc2064e75189b`  
		Last Modified: Fri, 11 Feb 2022 00:05:57 GMT  
		Size: 103.9 KB (103866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.0.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:3705c346942351bfc73d6d9e4786f1ca3f07c7f8721aff8840fb0400f78b7e46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.1 MB (365080704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53497d8c2a63c9b247839d8cb0f80974221efcde684833430682b57b1020f0a1`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Thu, 03 Feb 2022 22:57:40 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 03 Feb 2022 22:57:41 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 03 Feb 2022 22:57:41 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 03 Feb 2022 22:57:41 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 03 Feb 2022 22:57:46 GMT
COPY --chown=0:0dir:973e829905c8362abf43d0153c368ef1e6a11b0a09d9a588bcb5898bc0318f17 in /usr/share/elasticsearch 
# Thu, 03 Feb 2022 22:57:50 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Thu, 03 Feb 2022 22:57:50 GMT
COPY --chown=0:0dir:dc66ad287e412767e7bc0881fa0de8bd5a657165824323af7b04dd18841bea5d in /usr/local/cloudflare-zlib 
# Thu, 03 Feb 2022 22:57:51 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 22:57:51 GMT
ENV ES_ZLIB_PATH=/usr/local/cloudflare-zlib/lib
# Thu, 03 Feb 2022 22:57:51 GMT
COPY file:bd241387dbc1b05c0872607dd207d3a5b10dfd812f1441a5b215a7e5436fca23 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 03 Feb 2022 22:57:51 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 03 Feb 2022 22:57:52 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 03 Feb 2022 22:57:52 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 03 Feb 2022 22:57:52 GMT
EXPOSE 9200 9300
# Thu, 03 Feb 2022 22:57:52 GMT
LABEL org.label-schema.build-date=2022-02-03T22:55:04.924703384Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1b6a7ece17463df5ff54a3e1302d825889aa1161 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.0.0 org.opencontainers.image.created=2022-02-03T22:55:04.924703384Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1b6a7ece17463df5ff54a3e1302d825889aa1161 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.0.0
# Thu, 03 Feb 2022 22:57:53 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 03 Feb 2022 22:57:53 GMT
CMD ["eswrapper"]
# Thu, 03 Feb 2022 22:57:53 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4c3a3a86a59418eb86cf6d5b9146774deea48519016e7c938860ee07ea1f08`  
		Last Modified: Fri, 11 Feb 2022 23:45:37 GMT  
		Size: 8.1 MB (8069082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2db2cee55f75bf043e97546693326118458a99c8693cef4573b45ae1dc0ddfd`  
		Last Modified: Fri, 11 Feb 2022 23:45:35 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8aad1865af14a05e06fe89197a4715aa84b784445852ac807a3b71c1f0fed4`  
		Last Modified: Fri, 11 Feb 2022 23:46:04 GMT  
		Size: 329.4 MB (329386757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c166f55a92ce67123be51ecff49f053ac7f15a0c06c21924393def634a002c4`  
		Last Modified: Fri, 11 Feb 2022 23:45:35 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55d054d831c359556ddaa4200244b2f3ca53d628af6486755d994a20d6c905c`  
		Last Modified: Fri, 11 Feb 2022 23:45:33 GMT  
		Size: 149.9 KB (149910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d00c8549483effc47db5cf1951c7c76646f9da48d649efc1d12acf5a8a9052`  
		Last Modified: Fri, 11 Feb 2022 23:45:32 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fe1fade6565d7278fb5587f035aa95e3ca54e013ae477ceaca05bdfc9377d9`  
		Last Modified: Fri, 11 Feb 2022 23:45:33 GMT  
		Size: 185.9 KB (185864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8167f3c87592b07a0c0ed8bd7bb98e0fde370e499036c2e72788d901c4ad6f`  
		Last Modified: Fri, 11 Feb 2022 23:45:33 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0343e9fce798ed70da31be2e702346e2c87bf3ce2299a0bb525f58d07ea01823`  
		Last Modified: Fri, 11 Feb 2022 23:45:33 GMT  
		Size: 103.9 KB (103866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
