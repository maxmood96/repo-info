<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.18`](#elasticsearch6818)
-	[`elasticsearch:7.14.0`](#elasticsearch7140)

## `elasticsearch:6.8.18`

```console
$ docker pull elasticsearch@sha256:a676c5eadeaff21fb0ed9b7f6be7dcb559dc25dcc017940197dd5ced0f90dbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `elasticsearch:6.8.18` - linux; amd64

```console
$ docker pull elasticsearch@sha256:0f16a358b58c4d233258c87fe2dd9762d02eb0561ff9e72aa9814e03f2e2dd15
```

-	Docker Version: 20.10.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.2 MB (482221730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b226f5ba29f397cac809b642d7f9f9bc7e865c4e248ccb65e6b9cee09bea2d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Wed, 28 Jul 2021 16:10:35 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 28 Jul 2021 16:10:36 GMT
ENV JAVA_HOME=/opt/jdk-15.0.1+9
# Wed, 28 Jul 2021 16:10:41 GMT
COPY dir:8d79ae5f21bb18379c0d92b3d252f4730fec22a4509252ec794212b8f72bd7af in /opt/jdk-15.0.1+9 
# Wed, 28 Jul 2021 16:11:23 GMT
RUN for iter in {1..10}; do yum update  --setopt=tsflags=nodocs -y &&     yum install -y  --setopt=tsflags=nodocs nc unzip wget which &&     yum clean all && exit_code=0 && break || exit_code=\$? && echo "yum error: retry $iter in 10s" && sleep 10; done;     (exit $exit_code)
# Wed, 28 Jul 2021 16:11:25 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chgrp 0 /usr/share/elasticsearch
# Wed, 28 Jul 2021 16:11:25 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 28 Jul 2021 16:11:28 GMT
COPY --chown=1000:0dir:2b0d1a24665560d0012df6c5f68f16ea5e598782bfc6749adbf0f56f745fdcf3 in /usr/share/elasticsearch 
# Wed, 28 Jul 2021 16:11:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 16:11:29 GMT
COPY --chown=1000:0file:08193f849fc25f29db1438eff6d5c9fe1d63237aeb07a3e0009e8ba554f97c31 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 28 Jul 2021 16:11:30 GMT
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh &&     chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh
# Wed, 28 Jul 2021 16:11:30 GMT
EXPOSE 9200 9300
# Wed, 28 Jul 2021 16:11:31 GMT
LABEL org.label-schema.build-date=2021-07-28T16:06:05.232873Z org.label-schema.license=Elastic-License org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aca23296a2422a5abea96a1b6b590f6566e9c02f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=6.8.18 org.opencontainers.image.created=2021-07-28T16:06:05.232873Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License org.opencontainers.image.revision=aca23296a2422a5abea96a1b6b590f6566e9c02f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=6.8.18
# Wed, 28 Jul 2021 16:11:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 28 Jul 2021 16:11:31 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0128b25cc806662d7fe5ee6828f183c810828baa43cf452ddb469980ae5c4ff3`  
		Last Modified: Tue, 03 Aug 2021 12:57:47 GMT  
		Size: 207.7 MB (207657662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e926b4f11fd8c1a1adffe67a9c0803a29698dba31660155078e0b337de05753`  
		Last Modified: Tue, 03 Aug 2021 12:57:27 GMT  
		Size: 48.3 MB (48319743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01aa6e6c3b0500fe4d3d1bc5e21b20db804d517a6f48bc911b001e0577b3544`  
		Last Modified: Tue, 03 Aug 2021 12:57:16 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f53e5ee82cadd34edd16d8d5f9354aa1615988ba5c57670bb2b7dce330df0f3`  
		Last Modified: Tue, 03 Aug 2021 12:57:34 GMT  
		Size: 150.1 MB (150140389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6045fa98c98d76b32e4a3f9ea1ab9f8e56b0efb02a13451db236b413feec67e7`  
		Last Modified: Tue, 03 Aug 2021 12:57:16 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec43e9f984f6fc2ffe54f846e2ca96c37af763371f2333fb82c3e54bb3468b1`  
		Last Modified: Tue, 03 Aug 2021 12:57:16 GMT  
		Size: 2.4 KB (2402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:7.14.0`

```console
$ docker pull elasticsearch@sha256:81c126e4eddbc5576285670cb3e23d7ef7892ee5e757d6d9ba870b6fe99f1219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.14.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:0a99d5540785efefc59c90001667494612eabb2b51badd8f8479c06d73fdee37
```

-	Docker Version: 20.10.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.9 MB (512909189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e347b2b2d6c139e00250755db2a77c993176bdbbc5daecc5c0c3a3b04004b186`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Thu, 29 Jul 2021 20:57:41 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y       nc shadow-utils zip unzip  &&       yum clean all &&       exit_code=0 && break ||         exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 29 Jul 2021 20:57:44 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chown -R 1000:0 /usr/share/elasticsearch
# Thu, 29 Jul 2021 20:57:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 29 Jul 2021 20:57:45 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 29 Jul 2021 20:57:57 GMT
COPY --chown=1000:0dir:fffa8e52a3084396da7b31aa8f4668af4f973d6ae6d63bc6addd5ce9c9446f3d in /usr/share/elasticsearch 
# Thu, 29 Jul 2021 20:57:58 GMT
COPY --chown=0:0file:cbfbfe828617d3c65a10427a333f66d6d0b1b1aaea532739bba4696579b6cb19 in /bin/tini 
# Thu, 29 Jul 2021 20:57:58 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 20:57:59 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Thu, 29 Jul 2021 20:58:01 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Thu, 29 Jul 2021 20:58:01 GMT
EXPOSE 9200 9300
# Thu, 29 Jul 2021 20:58:02 GMT
LABEL org.label-schema.build-date=2021-07-29T20:49:32.864135063Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dd5a0a2acaa2045ff9624f3729fc8a6f40835aa1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.14.0 org.opencontainers.image.created=2021-07-29T20:49:32.864135063Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dd5a0a2acaa2045ff9624f3729fc8a6f40835aa1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.14.0
# Thu, 29 Jul 2021 20:58:02 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 29 Jul 2021 20:58:02 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7718d2f58c471b94b4a903dd6a3c5dd2ebb81fbee56b303183faa1f69c0e8503`  
		Last Modified: Tue, 03 Aug 2021 13:53:51 GMT  
		Size: 91.8 MB (91788076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5c16bd8bb9053720f793e9ae887fe19e6d24b29e68b22c378feeddd386eea9`  
		Last Modified: Tue, 03 Aug 2021 13:53:07 GMT  
		Size: 2.4 KB (2391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d829b4b297d870405c4702449817546225fa190a081fddcb7fb31d5872b26f`  
		Last Modified: Tue, 03 Aug 2021 13:53:54 GMT  
		Size: 345.7 MB (345725509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad944c92c790eba2b7fa8d4110a944c30104f501858f7a032244687e2e2248b`  
		Last Modified: Tue, 03 Aug 2021 13:53:03 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373fb8fbaf74db6083b3eba23a0b8d3da7e26b308903a1ce40f4db27234e115a`  
		Last Modified: Tue, 03 Aug 2021 13:53:02 GMT  
		Size: 2.0 KB (1981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5908d3eb2989f37769070d80ebe75124a5e8f8891805e2ee69d9b983b0700e60`  
		Last Modified: Tue, 03 Aug 2021 13:52:59 GMT  
		Size: 199.7 KB (199696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.14.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:cd85f6539015b9ea355cf33ce845a6505606ed36ecd6f1e6c586b27fc9f7bf1c
```

-	Docker Version: 20.10.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.6 MB (510584883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c4063337413961ad39a3f214646c4ba5910e694d183b3a936b796f8c172e80`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 07 Dec 2020 23:42:06 GMT
ADD file:edd6e1253ec7bbb67b5a28d40c7d28b34a443c2cfa327bebf55c8b0b19484bf9 in / 
# Mon, 07 Dec 2020 23:42:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Mon, 07 Dec 2020 23:42:10 GMT
CMD ["/bin/bash"]
# Thu, 29 Jul 2021 21:51:41 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y       nc shadow-utils zip unzip  &&       yum clean all &&       exit_code=0 && break ||         exit_code=$? && echo "yum error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 29 Jul 2021 21:51:43 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chmod 0775 /usr/share/elasticsearch &&     chown -R 1000:0 /usr/share/elasticsearch
# Thu, 29 Jul 2021 21:51:43 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 29 Jul 2021 21:51:43 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 29 Jul 2021 21:51:52 GMT
COPY --chown=1000:0dir:84c243b2f9def98b6584f99f61bc7b6c48389e489f7dd1eef3051d5e55594c3e in /usr/share/elasticsearch 
# Thu, 29 Jul 2021 21:51:55 GMT
COPY --chown=0:0file:1d48586bd42e8cf29bed9d4feee798b5c536660cc7b115750f0cd4f7bd33c311 in /bin/tini 
# Thu, 29 Jul 2021 21:51:55 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 21:51:56 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Thu, 29 Jul 2021 21:51:58 GMT
RUN chmod g=u /etc/passwd &&     chmod 0775 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     ln -sf /etc/pki/ca-trust/extracted/java/cacerts /usr/share/elasticsearch/jdk/lib/security/cacerts
# Thu, 29 Jul 2021 21:51:58 GMT
EXPOSE 9200 9300
# Thu, 29 Jul 2021 21:51:58 GMT
LABEL org.label-schema.build-date=2021-07-29T21:47:05.916196581Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dd5a0a2acaa2045ff9624f3729fc8a6f40835aa1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.14.0 org.opencontainers.image.created=2021-07-29T21:47:05.916196581Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dd5a0a2acaa2045ff9624f3729fc8a6f40835aa1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.14.0
# Thu, 29 Jul 2021 21:51:58 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 29 Jul 2021 21:51:58 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:333cbcae3fb80b9a46084ae4caea81a84aafda9700fb646ab89206d0cfe213fd`  
		Last Modified: Mon, 07 Dec 2020 23:42:49 GMT  
		Size: 75.6 MB (75613064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1157305657a12ada26b59798f33b0be9849433053e47f63434067afc799b81`  
		Last Modified: Tue, 03 Aug 2021 23:59:41 GMT  
		Size: 91.8 MB (91760924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ccdd9b3f224dbc678815eb1b43572580472d2970846df6735c24a04c599728`  
		Last Modified: Tue, 03 Aug 2021 23:59:23 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db0e54bc8bb584dd1903e6f070e82bc430fa898e49202c58f64f3c497b0d4f8`  
		Last Modified: Tue, 03 Aug 2021 23:59:54 GMT  
		Size: 343.0 MB (342997077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f19cde676a47993b8fa99416e114263d17df6ccf0484c4b77f5c1c606b820cf`  
		Last Modified: Tue, 03 Aug 2021 23:59:23 GMT  
		Size: 9.1 KB (9109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6157fa8382415c94366da101b7373dde523dd93dac854d2f4e2b1267cd0604ba`  
		Last Modified: Tue, 03 Aug 2021 23:59:23 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036230b4b1873776e096e468aecc5d505b716b1b0a96b63849257c355698fb83`  
		Last Modified: Tue, 03 Aug 2021 23:59:25 GMT  
		Size: 200.3 KB (200340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
