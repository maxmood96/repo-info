<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:6.8.23`](#elasticsearch6823)
-	[`elasticsearch:7.16.3`](#elasticsearch7163)

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

## `elasticsearch:7.16.3`

```console
$ docker pull elasticsearch@sha256:de5474d051409e8222eee30c82ef299f3f3c97bb339bbd19c314178db659f7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.16.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:809462292ed9395f7c67372ff30de136aed44b80dfa81f8142e399e51c05e973
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350148765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5e932847815e81e74ca6179f584f2af458867bfe5dd6fad2ebc2dab32a2121`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:54:27 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Fri, 07 Jan 2022 03:54:28 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Fri, 07 Jan 2022 03:54:28 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 07 Jan 2022 03:54:28 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 07 Jan 2022 03:54:35 GMT
COPY --chown=0:0dir:cd0f893a15c106f87e3ecf14d20f65d13b31b1b5eaa5201e4c1234d3ffbd01c4 in /usr/share/elasticsearch 
# Fri, 07 Jan 2022 03:54:39 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Fri, 07 Jan 2022 03:54:39 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 03:54:39 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 Jan 2022 03:54:40 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Fri, 07 Jan 2022 03:54:40 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Fri, 07 Jan 2022 03:54:40 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Fri, 07 Jan 2022 03:54:41 GMT
EXPOSE 9200 9300
# Fri, 07 Jan 2022 03:54:41 GMT
LABEL org.label-schema.build-date=2022-01-07T03:52:04.721256476Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4e6e4eab2297e949ec994e688dad46290d018022 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.16.3 org.opencontainers.image.created=2022-01-07T03:52:04.721256476Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4e6e4eab2297e949ec994e688dad46290d018022 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.16.3
# Fri, 07 Jan 2022 03:54:41 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:54:41 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccee306c4da35e7dac6b42ac95d46b44885b84528e4443543a36c8ba0c115df`  
		Last Modified: Thu, 13 Jan 2022 19:06:08 GMT  
		Size: 8.3 MB (8255224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28688537d02c2ed17870a9288ec4e85ccadf78c783474b043b7414ed938affb4`  
		Last Modified: Thu, 13 Jan 2022 19:06:06 GMT  
		Size: 4.4 KB (4356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5fb23d065d9374354067d1217f927b83769361514184723eba4a278d0698d8`  
		Last Modified: Thu, 13 Jan 2022 19:06:46 GMT  
		Size: 313.0 MB (313014856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f4c512861dddd667853cd7977eb94c92037141337d766fa7b65901536cb531`  
		Last Modified: Thu, 13 Jan 2022 19:06:04 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcc724c6288aae2814bec8dd49c4ad14cf15512e3dcd93f2632d91b974618f3`  
		Last Modified: Thu, 13 Jan 2022 19:06:03 GMT  
		Size: 2.0 KB (1980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb0ba51c947c56a5585a7fec988af3c2842497119e15d351292eaa326b9edc6`  
		Last Modified: Thu, 13 Jan 2022 19:06:02 GMT  
		Size: 192.1 KB (192123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53dd95410f1e3e10033e4881f03516836e523ce44331b2af09c49a93df4408`  
		Last Modified: Thu, 13 Jan 2022 19:06:01 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b38207512863c3f119d60f1437b56113eb56c646ee6b752e7499625109b6583`  
		Last Modified: Thu, 13 Jan 2022 19:05:59 GMT  
		Size: 103.9 KB (103866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.16.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:bc693247a6b0eb903238e3c06671db10b37f0fcb32a76b6cc9ae8a6b1755df64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345098623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ea011d26d28cc69b63b8c00795d284a72b37d985d9754e22c6a5cf92231c5f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:56:55 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip vim-tiny zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Fri, 07 Jan 2022 03:56:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Fri, 07 Jan 2022 03:56:56 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 07 Jan 2022 03:56:56 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 07 Jan 2022 03:57:01 GMT
COPY --chown=0:0dir:8ec7d81eb71c89c47308ad6a8162f0c05392df948e3b1bacb64b1643ac9c26d7 in /usr/share/elasticsearch 
# Fri, 07 Jan 2022 03:57:04 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Fri, 07 Jan 2022 03:57:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 03:57:05 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 Jan 2022 03:57:05 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Fri, 07 Jan 2022 03:57:05 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Fri, 07 Jan 2022 03:57:06 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Fri, 07 Jan 2022 03:57:06 GMT
EXPOSE 9200 9300
# Fri, 07 Jan 2022 03:57:06 GMT
LABEL org.label-schema.build-date=2022-01-07T03:54:46.953812332Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4e6e4eab2297e949ec994e688dad46290d018022 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.16.3 org.opencontainers.image.created=2022-01-07T03:54:46.953812332Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4e6e4eab2297e949ec994e688dad46290d018022 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.16.3
# Fri, 07 Jan 2022 03:57:06 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:57:06 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f773c1275a3333c4668ad8e6df45b4d09aea1758d2e334dbd4c795de33d2323e`  
		Last Modified: Fri, 14 Jan 2022 01:39:59 GMT  
		Size: 8.1 MB (8085323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136347f389ecd3a0d9ebcca526383719fa067a8f12918f2df1d074a4776fcbe4`  
		Last Modified: Fri, 14 Jan 2022 01:39:57 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d81ecd351b75a70cb6ebc60f74644583957037691b9e3b4add807d91c6c77e`  
		Last Modified: Fri, 14 Jan 2022 01:40:28 GMT  
		Size: 309.5 MB (309536366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9268443bd89dcd7feb63ed0dda88736477b5b1c5f387d5f59bf520a10d565565`  
		Last Modified: Fri, 14 Jan 2022 01:39:55 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2acd051ab30f24cf496448370a2ba0e8c4e1e43a5a150d36846fb4ab522ee7`  
		Last Modified: Fri, 14 Jan 2022 01:39:55 GMT  
		Size: 2.0 KB (1981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a0c2425d1d4881061f8aac9510165993c0f835476faad899c53d4f555b9727`  
		Last Modified: Fri, 14 Jan 2022 01:39:55 GMT  
		Size: 186.1 KB (186141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e949da5cd54937d29b9bcc320de86240b1faf0c423452020e093654a90a3bfe`  
		Last Modified: Fri, 14 Jan 2022 01:39:55 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4d52bc6ea7cd082b64c4239f71a7498f3595c604b13fc11f659b4ce09e2e60`  
		Last Modified: Fri, 14 Jan 2022 01:39:55 GMT  
		Size: 103.9 KB (103868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
