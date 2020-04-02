<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.8`](#elasticsearch688)
-	[`elasticsearch:7.6.2`](#elasticsearch762)

## `elasticsearch:6.8.8`

```console
$ docker pull elasticsearch@sha256:6606066f12f09efeaaee8c3e9445fc1d60df5e947d87688049f9443207d2ead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `elasticsearch:6.8.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:219f56a8e5f005502f7b2000d367c01acc9deeb28d6f7d38f47e85dcd93bd9ca
```

-	Docker Version: 19.03.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.0 MB (475029929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e42cf9a68e7f19a7adc010de54d835bb9e65f49501e31072d931ff6f208782`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2020 23:27:21 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Mar 2020 23:27:21 GMT
ENV JAVA_HOME=/opt/jdk-14+36
# Wed, 18 Mar 2020 23:27:28 GMT
COPY dir:6061569ae0b6636f61b4e31d0d997c709a1e75f2f341f687d97d963f1b799e38 in /opt/jdk-14+36 
# Wed, 18 Mar 2020 23:28:07 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Wed, 18 Mar 2020 23:28:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Wed, 18 Mar 2020 23:28:09 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 18 Mar 2020 23:28:15 GMT
COPY --chown=1000:0dir:c12fcc31394b3c4e13c04ac8ff649ec4c8da4d5381f626cecb571577df6e04b4 in /usr/share/elasticsearch 
# Wed, 18 Mar 2020 23:28:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Mar 2020 23:28:16 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 Mar 2020 23:28:19 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Wed, 18 Mar 2020 23:28:19 GMT
EXPOSE 9200 9300
# Wed, 18 Mar 2020 23:28:19 GMT
LABEL org.label-schema.build-date=2020-03-18T23:22:18.622755Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2f4c2240ecfc520baef4353a726f13fc59c12066 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.8 org.opencontainers.image.created=2020-03-18T23:22:18.622755Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=2f4c2240ecfc520baef4353a726f13fc59c12066 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.8
# Wed, 18 Mar 2020 23:28:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 18 Mar 2020 23:28:21 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a81d6dd6ebf480228be5c61f684ec558bc4a8a745706e05571824605a7351d`  
		Last Modified: Tue, 31 Mar 2020 16:05:25 GMT  
		Size: 217.3 MB (217331377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43be5038628e709fbc5c7f239af2ec1c3c9da64c711e59b0b8fe190700575f58`  
		Last Modified: Tue, 31 Mar 2020 16:05:05 GMT  
		Size: 31.0 MB (30958529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ceac5aa6ce1930c997c0f69ae3874bd0d4fb354e91fa098d8cb59cd54cfc587`  
		Last Modified: Tue, 31 Mar 2020 16:05:00 GMT  
		Size: 2.3 KB (2338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4250fdbb4420bb2f5b183212fc70a7a6824a3c97faf77dc08c676090ce60f13`  
		Last Modified: Tue, 31 Mar 2020 16:05:17 GMT  
		Size: 151.0 MB (150952483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55b9786922477de39391990f2205fad0e4ab9d03e63fd05b9b390cd98164345`  
		Last Modified: Tue, 31 Mar 2020 16:04:59 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81a885a18e119ef586a058cf1f824faf6f2d6533090ce51331d4d644505cb98`  
		Last Modified: Tue, 31 Mar 2020 16:05:00 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.6.2`

```console
$ docker pull elasticsearch@sha256:1b09dbd93085a1e7bca34830e77d2981521a7210e11f11eda997add1c12711fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `elasticsearch:7.6.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f29607b18ae0d086c444b93bae5b4a949a7f75dd8bec68b5b0e0f4be8c1ea3a7
```

-	Docker Version: 19.03.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.9 MB (404949314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29a1ee41030e3963026369105f3bee76d75fdecbeca07932ac054126be7bff9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2020 06:38:25 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Mar 2020 06:39:23 GMT
RUN for iter in {1..10}; do yum update --setopt=tsflags=nodocs -y &&     yum install --setopt=tsflags=nodocs -y nc shadow-utils zip unzip &&     yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Thu, 26 Mar 2020 06:39:24 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Thu, 26 Mar 2020 06:39:24 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 26 Mar 2020 06:39:36 GMT
COPY --chown=1000:0dir:e8f8183a81e4135d278437111a658f98e7bfe7f63e055cfaae5964ceb46e4659 in /usr/share/elasticsearch 
# Thu, 26 Mar 2020 06:39:37 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Thu, 26 Mar 2020 06:39:38 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Mar 2020 06:39:38 GMT
COPY --chown=1000:0file:4e194e0f53ce77fff91bb999402cbd943658f591ee80ee538c1d145b9e464be4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 26 Mar 2020 06:39:43 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Thu, 26 Mar 2020 06:39:43 GMT
EXPOSE 9200 9300
# Thu, 26 Mar 2020 06:39:43 GMT
LABEL org.label-schema.build-date=2020-03-26T06:34:37.794943Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ef48eb35cf30adf4db14086e8aabd07ef6fb113f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.6.2 org.opencontainers.image.created=2020-03-26T06:34:37.794943Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=ef48eb35cf30adf4db14086e8aabd07ef6fb113f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.6.2
# Thu, 26 Mar 2020 06:39:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 26 Mar 2020 06:39:43 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d1ca5c8a25c41dc4169dd133c048336d0255ef71bbd65c98ee283891a66a17`  
		Last Modified: Tue, 31 Mar 2020 16:18:21 GMT  
		Size: 31.0 MB (31004855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941a3cc8e7b8d3883247f290762d908c610e11d315a180ad44eb26213aa9cfd5`  
		Last Modified: Tue, 31 Mar 2020 16:18:12 GMT  
		Size: 2.3 KB (2330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ec483d961810df12510963c39ae0754a6a310712037d5a5518b14285c59113`  
		Last Modified: Tue, 31 Mar 2020 16:18:37 GMT  
		Size: 298.2 MB (298157546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c486fd2006842badb17f248d544360f8096f4fc7087b005fb6104330a536ed35`  
		Last Modified: Tue, 31 Mar 2020 16:18:12 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b960df074b20a43d8af8a7da16ee4db1f52fae67b3afaae5c500e75849eaf2d`  
		Last Modified: Tue, 31 Mar 2020 16:18:12 GMT  
		Size: 1.6 KB (1621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1719d48d682301da138fabbc8a2c6dc14a9361fbd427367ed54927e11031930b`  
		Last Modified: Tue, 31 Mar 2020 16:18:12 GMT  
		Size: 2.0 KB (1958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
