<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.15`](#elasticsearch6815)
-	[`elasticsearch:7.12.1`](#elasticsearch7121)

## `elasticsearch:6.8.15`

```console
$ docker pull elasticsearch@sha256:fa7433fcb125b5c89e2db80918f460e4097cdcfcf1694e268a114270d70ec23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `elasticsearch:6.8.15` - linux; amd64

```console
$ docker pull elasticsearch@sha256:a4a020e64f64a12262aced394a20153b21b307ae7985f73c6b869e6cdcbe6131
```

-	Docker Version: 20.10.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.8 MB (479849192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71dbc55f668dad4f27786066060ffde16f347dc7c8345ab90b09e1157bf7b6e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Thu, 18 Mar 2021 06:38:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Mar 2021 06:38:48 GMT
ENV JAVA_HOME=/opt/jdk-15.0.1+9
# Thu, 18 Mar 2021 06:38:56 GMT
COPY dir:8d79ae5f21bb18379c0d92b3d252f4730fec22a4509252ec794212b8f72bd7af in /opt/jdk-15.0.1+9 
# Thu, 18 Mar 2021 06:39:58 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Thu, 18 Mar 2021 06:40:00 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Thu, 18 Mar 2021 06:40:01 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Mar 2021 06:40:06 GMT
COPY --chown=1000:0dir:bb53662b52f576e56386260cb35c528866996ddd5f87ba1d0573eff4bd6ad3c1 in /usr/share/elasticsearch 
# Thu, 18 Mar 2021 06:40:06 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Mar 2021 06:40:07 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 18 Mar 2021 06:40:09 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Thu, 18 Mar 2021 06:40:09 GMT
EXPOSE 9200 9300
# Thu, 18 Mar 2021 06:40:10 GMT
LABEL org.label-schema.build-date=2021-03-18T06:33:32.588487Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c9a8c60f59a902dfa018abda97b195f7ba9f29aa org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.15 org.opencontainers.image.created=2021-03-18T06:33:32.588487Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=c9a8c60f59a902dfa018abda97b195f7ba9f29aa org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.15
# Thu, 18 Mar 2021 06:40:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Mar 2021 06:40:11 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d2a6bc4529ec41290eade86ead2e35adfe70d2fc4d9e7daa0705c289268094`  
		Last Modified: Tue, 23 Mar 2021 13:50:07 GMT  
		Size: 207.7 MB (207657697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1e7ca20d705bc564bbc887c37719377ca2e97b30463f55a4555c88636eda2f`  
		Last Modified: Tue, 23 Mar 2021 13:50:02 GMT  
		Size: 46.0 MB (45959281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e358dab17355c3301934ef365a5c8e709e8802c91387858a26d7c8b15858e996`  
		Last Modified: Tue, 23 Mar 2021 13:49:47 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f67e30bb9fdd10fc4c310217f041d893d7f28adf748f28bda4880b93b12f21`  
		Last Modified: Tue, 23 Mar 2021 13:50:01 GMT  
		Size: 150.1 MB (150128276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29090ccafdcace322e29724fb1d373a3a0bc0a0e5d0bd64406b0db09bc194d63`  
		Last Modified: Tue, 23 Mar 2021 13:49:46 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6764b4f35508eb86b0b503e3c8526ce38e2fbd8990beaf14c2bc249bc57c20c7`  
		Last Modified: Tue, 23 Mar 2021 13:49:46 GMT  
		Size: 2.4 KB (2402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.12.1`

```console
$ docker pull elasticsearch@sha256:622f854572780281bc85b5fde33be27e99670941ed8b7eea5ba4aaf533fa64ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.12.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:c3a165c618a19a4a8da009698eab0ac4951b3f54f07866c77981f013233ec23b
```

-	Docker Version: 20.10.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.4 MB (433376263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dc8ea0f13974958c4abc07b9d2ac20ac56793834c216633db012be18899f67`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 20 Apr 2021 21:04:55 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y       nc shadow-utils zip unzip  &&       yum clean all &&       exit_code=0 && break ||         exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Tue, 20 Apr 2021 21:04:58 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chown -R 1000:0 /usr/share/elasticsearch
# Tue, 20 Apr 2021 21:04:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Apr 2021 21:04:58 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 20 Apr 2021 21:05:14 GMT
COPY --chown=1000:0dir:b8af2fe966f9f55fab0f0623ac9c70b7e8959fb427604ffafdfb0c862a43671b in /usr/share/elasticsearch 
# Tue, 20 Apr 2021 21:05:15 GMT
COPY --chown=0:0file:cbfbfe828617d3c65a10427a333f66d6d0b1b1aaea532739bba4696579b6cb19 in /bin/tini 
# Tue, 20 Apr 2021 21:05:15 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Apr 2021 21:05:16 GMT
COPY file:b60644ac0fe4cb4e2bab5fb75a5f9b33fa1cb8276d88703c138a52af6bd8ea5b in /usr/local/bin/docker-entrypoint.sh 
# Tue, 20 Apr 2021 21:05:18 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Tue, 20 Apr 2021 21:05:18 GMT
EXPOSE 9200 9300
# Tue, 20 Apr 2021 21:05:19 GMT
LABEL org.label-schema.build-date=2021-04-20T20:56:39.040728659Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3186837139b9c6b6d23c3200870651f10d3343b7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.12.1 org.opencontainers.image.created=2021-04-20T20:56:39.040728659Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3186837139b9c6b6d23c3200870651f10d3343b7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.12.1
# Tue, 20 Apr 2021 21:05:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 20 Apr 2021 21:05:21 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4a47ec20b2314bf85e36b8b116b965324eb4eb348fbcd846bdd8a57cb9225d`  
		Last Modified: Tue, 27 Apr 2021 17:26:56 GMT  
		Size: 30.8 MB (30761223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e4f4b7e738b9c1aff5f12c625295296195b8dba607eeaf6538f05fef4bc2db`  
		Last Modified: Tue, 27 Apr 2021 17:26:49 GMT  
		Size: 2.4 KB (2363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2a2418a5f4ec6a516f920081e6d05f54db7a9551d64d9e3d03086d35668372`  
		Last Modified: Tue, 27 Apr 2021 17:27:17 GMT  
		Size: 327.2 MB (327219842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646dbf47f74708f05a209254afe301c42374acf8838a5e01848d3c63c265efb8`  
		Last Modified: Tue, 27 Apr 2021 17:26:45 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbf21442fcebfcc9520c594030721c131d038cfd19cd224b07898c61cfd6fb`  
		Last Modified: Tue, 27 Apr 2021 17:26:45 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04f00c0d46462c469efe18824eab76fd330be4c2381e2824075ea32077ca5a2`  
		Last Modified: Tue, 27 Apr 2021 17:26:46 GMT  
		Size: 199.4 KB (199355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.12.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:0f15ce59a1c8256462c6c1be49724122eda3489c7cd43c1e6133c3464bb5b641
```

-	Docker Version: 20.10.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430205175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d090d5af83cac5a69e3992c25547b39232e72acd13fe596f7f1fad39e086a6ad`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 07 Dec 2020 23:42:06 GMT
ADD file:edd6e1253ec7bbb67b5a28d40c7d28b34a443c2cfa327bebf55c8b0b19484bf9 in / 
# Mon, 07 Dec 2020 23:42:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Mon, 07 Dec 2020 23:42:10 GMT
CMD ["/bin/bash"]
# Tue, 20 Apr 2021 21:48:33 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y       nc shadow-utils zip unzip  &&       yum clean all &&       exit_code=0 && break ||         exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Tue, 20 Apr 2021 21:48:34 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chown -R 1000:0 /usr/share/elasticsearch
# Tue, 20 Apr 2021 21:48:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Apr 2021 21:48:35 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 20 Apr 2021 21:48:40 GMT
COPY --chown=1000:0dir:2feeffb76c1bf724495b93d969a63b7bca8345f103eefc1d89261dca56a646c1 in /usr/share/elasticsearch 
# Tue, 20 Apr 2021 21:48:43 GMT
COPY --chown=0:0file:1d48586bd42e8cf29bed9d4feee798b5c536660cc7b115750f0cd4f7bd33c311 in /bin/tini 
# Tue, 20 Apr 2021 21:48:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Apr 2021 21:48:43 GMT
COPY file:b60644ac0fe4cb4e2bab5fb75a5f9b33fa1cb8276d88703c138a52af6bd8ea5b in /usr/local/bin/docker-entrypoint.sh 
# Tue, 20 Apr 2021 21:48:45 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Tue, 20 Apr 2021 21:48:45 GMT
EXPOSE 9200 9300
# Tue, 20 Apr 2021 21:48:45 GMT
LABEL org.label-schema.build-date=2021-04-20T21:46:04.451368164Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3186837139b9c6b6d23c3200870651f10d3343b7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.12.1 org.opencontainers.image.created=2021-04-20T21:46:04.451368164Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3186837139b9c6b6d23c3200870651f10d3343b7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.12.1
# Tue, 20 Apr 2021 21:48:45 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 20 Apr 2021 21:48:46 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:333cbcae3fb80b9a46084ae4caea81a84aafda9700fb646ab89206d0cfe213fd`  
		Last Modified: Mon, 07 Dec 2020 23:42:49 GMT  
		Size: 75.6 MB (75613064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef004a5c90526cca2ca090ce215b2c3069f1efb1bc5ef73e565613c9dd2e4f73`  
		Last Modified: Wed, 28 Apr 2021 17:40:41 GMT  
		Size: 29.9 MB (29883248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487f31dc597e3043e740f9f4048131676e3d6df8781fa10e117dcbed36f85e34`  
		Last Modified: Wed, 28 Apr 2021 17:40:31 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12818fcf0ef3bf781f8b7793227852fd3f233aefb56cc0bfad827e4ce2141ab1`  
		Last Modified: Wed, 28 Apr 2021 17:41:15 GMT  
		Size: 324.5 MB (324495317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e300b462771b7c77946457bfe8d80f9eaeaf5e95cc37929c98c90db2deff0a`  
		Last Modified: Wed, 28 Apr 2021 17:40:31 GMT  
		Size: 9.1 KB (9110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd15fa8dce95a58ae520a52ed2fbec4eb17ade06e0402791ee89eff0bde5b3`  
		Last Modified: Wed, 28 Apr 2021 17:40:31 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fa2410cff09aef3b53d36b75c187c1bf1235d90e5d9cd8529d46f01eaf3f57`  
		Last Modified: Wed, 28 Apr 2021 17:40:36 GMT  
		Size: 200.1 KB (200121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
