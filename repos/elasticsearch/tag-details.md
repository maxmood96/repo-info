<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.23`](#elasticsearch6823)
-	[`elasticsearch:7.17.4`](#elasticsearch7174)
-	[`elasticsearch:8.2.3`](#elasticsearch823)

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

## `elasticsearch:7.17.4`

```console
$ docker pull elasticsearch@sha256:529b3cfec4354beda158c6c7f2f8015cbdc9432a48c1d63e824d6fd728f30db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.17.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9396036d141a2bc50bfb74cba320483ade8c1d62f850faa4d41b4461e0a8fe48
```

-	Docker Version: 20.10.16
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.8 MB (356782272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64cccab426e007ea19962deb2910114c25bb4e945ceb09c27926ff1c34a6dca`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Wed, 18 May 2022 20:14:01 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Wed, 18 May 2022 20:14:02 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Wed, 18 May 2022 20:14:02 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 May 2022 20:14:02 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 18 May 2022 20:14:09 GMT
COPY --chown=0:0dir:549be6b9d73a27c351f455baa31dc1ee6178243ba7007fa8dee8e3f73969de9b in /usr/share/elasticsearch 
# Wed, 18 May 2022 20:14:13 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Wed, 18 May 2022 20:14:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 May 2022 20:14:13 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 May 2022 20:14:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Wed, 18 May 2022 20:14:14 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Wed, 18 May 2022 20:14:15 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Wed, 18 May 2022 20:14:15 GMT
EXPOSE 9200 9300
# Wed, 18 May 2022 20:14:15 GMT
LABEL org.label-schema.build-date=2022-05-18T20:11:36.585918371Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=79878662c54c886ae89206c685d9f1051a9d6411 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.4 org.opencontainers.image.created=2022-05-18T20:11:36.585918371Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=79878662c54c886ae89206c685d9f1051a9d6411 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.4
# Wed, 18 May 2022 20:14:15 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 18 May 2022 20:14:15 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aceae0816c1b49cb7f63d9aa49e1f53fd5ccedf70454dfd9d9217e0ddf01829`  
		Last Modified: Wed, 25 May 2022 05:41:42 GMT  
		Size: 18.1 MB (18081009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f282e391d7d7f1c42a92085425c737a0b4ab56d57633b0257f6ec9fecb5c218`  
		Last Modified: Wed, 25 May 2022 05:41:39 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1c86ab271c86978c55c9a189af4eb3bd0088ff0a80d95381689fcc7eff6a8`  
		Last Modified: Wed, 25 May 2022 05:42:03 GMT  
		Size: 309.8 MB (309822759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2d02571b2b6619cfc5e3ffd5afa77e69a5b6c7e086a9a4700e89aa5a34a966`  
		Last Modified: Wed, 25 May 2022 05:41:39 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fb4b01f643c5b7787c878b813f5e912417d715cd41b201ab28ebbd2734965e`  
		Last Modified: Wed, 25 May 2022 05:41:37 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606786004049189a662f6c51433fe32773329f2fb4ba176d748cd175be0a2c0e`  
		Last Modified: Wed, 25 May 2022 05:41:37 GMT  
		Size: 192.1 KB (192132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ec7712324b21e55297cba4c0624cc6535e11b5309dae6212dab6b36505249f`  
		Last Modified: Wed, 25 May 2022 05:41:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5976c5411619b618cc8e6b0a1d46d2f3b5845535ecbcf9443770f6c51e8614`  
		Last Modified: Wed, 25 May 2022 05:41:37 GMT  
		Size: 103.9 KB (103864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.17.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:310afb0b900b01b1b09f2bca48f0b7eb7f7e62ef6ed1d9b08f25a7a868158bc4
```

-	Docker Version: 20.10.16
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352575853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ac99164e4b7ab458a8d3543382b5385747531ccf32848617b2b26684ac2b58`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Wed, 18 May 2022 20:16:15 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Wed, 18 May 2022 20:16:16 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Wed, 18 May 2022 20:16:16 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 May 2022 20:16:16 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 18 May 2022 20:16:20 GMT
COPY --chown=0:0dir:73295c4ff64e88fda921ca45a9ec688267643b9c6d62f3af207bcabbcc95a809 in /usr/share/elasticsearch 
# Wed, 18 May 2022 20:16:24 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Wed, 18 May 2022 20:16:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 May 2022 20:16:24 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 May 2022 20:16:25 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Wed, 18 May 2022 20:16:25 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Wed, 18 May 2022 20:16:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Wed, 18 May 2022 20:16:26 GMT
EXPOSE 9200 9300
# Wed, 18 May 2022 20:16:26 GMT
LABEL org.label-schema.build-date=2022-05-18T20:13:54.577348181Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=79878662c54c886ae89206c685d9f1051a9d6411 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.4 org.opencontainers.image.created=2022-05-18T20:13:54.577348181Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=79878662c54c886ae89206c685d9f1051a9d6411 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.4
# Wed, 18 May 2022 20:16:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 18 May 2022 20:16:26 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfeca47b2583f728bc6074e8af984467a9e890d8ff2e2cc54569fe53745f7a1`  
		Last Modified: Wed, 25 May 2022 17:40:56 GMT  
		Size: 16.7 MB (16731258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc138a45fc96942a2eee3aa460ed184765fa1ae9471e1ba6b4b50538d33c12e`  
		Last Modified: Wed, 25 May 2022 17:40:54 GMT  
		Size: 4.4 KB (4371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770aba879c1a2d17504e1bac9d5fe38d86c294a0bab0920d44da83bbaff72cb`  
		Last Modified: Wed, 25 May 2022 17:41:20 GMT  
		Size: 308.4 MB (308369316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec2d6215148c5ecc813ab122741c8daaae09fdcd2f5b6446ed622ca9c961657`  
		Last Modified: Wed, 25 May 2022 17:40:51 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a9b212c684ffe79573e749dac7569a7b951b8fcb7ab956dac815cb69ebf937`  
		Last Modified: Wed, 25 May 2022 17:40:51 GMT  
		Size: 2.0 KB (1981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0077c1fe93adcd113fb488696828dc20331f82bb452c5cd88d8c6ff705a2ecd`  
		Last Modified: Wed, 25 May 2022 17:40:51 GMT  
		Size: 186.2 KB (186162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a9cfa22bef167240fc89d77533d745561cfc6d7e8d461793e6fc1f6a79220`  
		Last Modified: Wed, 25 May 2022 17:40:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddc033588d2c34315404a643898ad686b4f22f11d7f44b4720a810a5b639f89`  
		Last Modified: Wed, 25 May 2022 17:40:51 GMT  
		Size: 103.9 KB (103872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.2.3`

```console
$ docker pull elasticsearch@sha256:f1363868e19aa721355f387a8e79a33496c56fb525d37bc27e032a5c1e540b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.2.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:454e5ff645c6d291ef982a808433169b7f9970f79c6bc14f50f91982adb2de21
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570331745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59306705ed62914a42734f3c12b2dfab9fc8e9f26b32ea72c74ab94c000cf0e3`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Thu, 09 Jun 2022 01:07:45 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 09 Jun 2022 01:07:46 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 09 Jun 2022 01:07:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 Jun 2022 01:07:46 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 09 Jun 2022 01:08:00 GMT
COPY --chown=0:0dir:5341396f87fa2c23b4406cb94068d0a8a5933de08e3583a8667af9fa1305bf65 in /usr/share/elasticsearch 
# Thu, 09 Jun 2022 01:08:04 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Thu, 09 Jun 2022 01:08:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jun 2022 01:08:04 GMT
COPY file:bd241387dbc1b05c0872607dd207d3a5b10dfd812f1441a5b215a7e5436fca23 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 09 Jun 2022 01:08:05 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 09 Jun 2022 01:08:05 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 09 Jun 2022 01:08:06 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 09 Jun 2022 01:08:06 GMT
EXPOSE 9200 9300
# Thu, 09 Jun 2022 01:08:06 GMT
LABEL org.label-schema.build-date=2022-06-09T01:05:12.056328351Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=9905bfb62a3f0b044948376b4f607f70a8a151b4 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.2.3 org.opencontainers.image.created=2022-06-09T01:05:12.056328351Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=9905bfb62a3f0b044948376b4f607f70a8a151b4 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.2.3
# Thu, 09 Jun 2022 01:08:06 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 09 Jun 2022 01:08:06 GMT
CMD ["eswrapper"]
# Thu, 09 Jun 2022 01:08:06 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3c26aec5815b0c9b38cbf5bcd042bc4fd857297be2d2c7337302f619c5e377`  
		Last Modified: Wed, 15 Jun 2022 05:01:49 GMT  
		Size: 9.0 MB (8968696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b693cfe8119f254b24c3b68965f7dea78269f365995f30e573f0e38364c1ab`  
		Last Modified: Wed, 15 Jun 2022 05:01:46 GMT  
		Size: 4.4 KB (4363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25a07e1368a506f3e1cfa6c8f6ff478f6654bea6d5fa3ea78d514311a25cc1`  
		Last Modified: Wed, 15 Jun 2022 05:02:40 GMT  
		Size: 532.5 MB (532480112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272721e0bba39173f2397ca1ffe3020b9970f81aa814e0ea8f752273aa6f7173`  
		Last Modified: Wed, 15 Jun 2022 05:01:46 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cfc83305a2eb0e5697d8296a97a655357e10197502a6dc5eeb0a0d4861b571`  
		Last Modified: Wed, 15 Jun 2022 05:01:43 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30fddfc9ef3fbdcdf04b600e4c40ad35e57a018ee28a00af202bd1be756fcd1`  
		Last Modified: Wed, 15 Jun 2022 05:01:43 GMT  
		Size: 191.9 KB (191860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb649e5598f26609f7eec7007f33e1e0cc5df3a3f10b97aba78b8b7b7bdbac7`  
		Last Modified: Wed, 15 Jun 2022 05:01:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e1f4f44c160e4fef87ad25b91f52e5ee505294897405791415c0433b532149`  
		Last Modified: Wed, 15 Jun 2022 05:01:43 GMT  
		Size: 102.4 KB (102422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.2.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:af6d49f92b93317939fcba39fba1ea05ff9435099c8dfa84d8738a043a95727c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378519820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872a2feba802b050e6b78075dd5fa72ee179ae242f94f7b1b2124e1b052cbe65`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Thu, 09 Jun 2022 01:10:20 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 09 Jun 2022 01:10:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 09 Jun 2022 01:10:21 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 Jun 2022 01:10:21 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 09 Jun 2022 01:10:26 GMT
COPY --chown=0:0dir:bda8079a155c94840a5e1c07f35574604f3e42a5959ad1f541b7978e4e21e29d in /usr/share/elasticsearch 
# Thu, 09 Jun 2022 01:10:30 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Thu, 09 Jun 2022 01:10:30 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Jun 2022 01:10:30 GMT
COPY file:bd241387dbc1b05c0872607dd207d3a5b10dfd812f1441a5b215a7e5436fca23 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 09 Jun 2022 01:10:31 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 09 Jun 2022 01:10:31 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 09 Jun 2022 01:10:32 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 09 Jun 2022 01:10:32 GMT
EXPOSE 9200 9300
# Thu, 09 Jun 2022 01:10:32 GMT
LABEL org.label-schema.build-date=2022-06-09T01:08:04.317363568Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=9905bfb62a3f0b044948376b4f607f70a8a151b4 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.2.3 org.opencontainers.image.created=2022-06-09T01:08:04.317363568Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=9905bfb62a3f0b044948376b4f607f70a8a151b4 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.2.3
# Thu, 09 Jun 2022 01:10:32 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 09 Jun 2022 01:10:32 GMT
CMD ["eswrapper"]
# Thu, 09 Jun 2022 01:10:32 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df448df8c8b9e3eb2f4470cb7fb7d552aa84c2acc0e615db7a721c60ec497821`  
		Last Modified: Thu, 16 Jun 2022 00:44:54 GMT  
		Size: 8.8 MB (8794995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb63d9b854309a223d9733edd8a2e766fa5dfbce135b3aafaa0113a9ff2c7d24`  
		Last Modified: Thu, 16 Jun 2022 00:44:52 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca42f25926ba917565f905d3df120ce390aad54352f63f46e64434042d1661b7`  
		Last Modified: Thu, 16 Jun 2022 00:45:26 GMT  
		Size: 342.2 MB (342229710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c010be679258ed84c0326e1c0a4306b719076b967da913bcb88024dab7b4693`  
		Last Modified: Thu, 16 Jun 2022 00:44:50 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0238caf7ca620f6d53c431237127071bb142acdde831814247a36f82da0b79cd`  
		Last Modified: Thu, 16 Jun 2022 00:44:50 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c017558a5d656ee86b04072294421b6a12f06eb8d18957377d8eddce3e636436`  
		Last Modified: Thu, 16 Jun 2022 00:44:50 GMT  
		Size: 185.9 KB (185888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4466dca44a23575bad0f1fd991ea7231fb6e90ad6d6c06d89472da9d0eac4e8`  
		Last Modified: Thu, 16 Jun 2022 00:44:50 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df14e179730f187568346204f9dd383421fe8d1069cc70b3b51d420464edfa2e`  
		Last Modified: Thu, 16 Jun 2022 00:44:50 GMT  
		Size: 102.4 KB (102418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
