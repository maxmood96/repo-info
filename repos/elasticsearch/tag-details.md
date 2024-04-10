<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.20`](#elasticsearch71720)
-	[`elasticsearch:8.13.0`](#elasticsearch8130)

## `elasticsearch:7.17.20`

```console
$ docker pull elasticsearch@sha256:2e416b50d43e55973e52f27bcaa6fe014b48794de0b62082cc8e6077cb22b4fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.20` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2edb381ac7247e649f3deba2f3072c984d1614ad5be886663125c1e4248db8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366676300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1deeb34cb9a0ab2474c16cd03b96b188a32f0082904898d2eeffb2072ddbaf`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 09 Apr 2024 08:24:48 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.build-date=2024-04-08T08:34:31.070382898Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b26557f585b7d95c71a5549e571a6bcd2667697d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.20 org.opencontainers.image.created=2024-04-08T08:34:31.070382898Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b26557f585b7d95c71a5549e571a6bcd2667697d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.20
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3e15586cb96bd5f0fbaea3a3a62208010ed3661e844e69b81ffce032767b09`  
		Last Modified: Tue, 09 Apr 2024 18:50:55 GMT  
		Size: 10.0 MB (9996801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1d54d71cf68aa804f549d3569eb7f3847cc085b11f65d6c8be7e3eb4e1fb04`  
		Last Modified: Tue, 09 Apr 2024 18:50:54 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e612b7661354d578fac5fa67734126be5771cdc697b7e506923e664c5f5c7f`  
		Last Modified: Tue, 09 Apr 2024 18:51:02 GMT  
		Size: 328.8 MB (328847527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe820ffc60b4615c03780997022d3a3df81e8e24bf230a904ce9f819ae7149b5`  
		Last Modified: Tue, 09 Apr 2024 18:50:55 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b4574f0cab6fe29f637165367f970bc6616850782dc594fe563619c04cffe4`  
		Last Modified: Tue, 09 Apr 2024 18:50:55 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e59fd32f36b3c538aba11c2b412cab763e6db5c9eeba55c44c226da8df4494`  
		Last Modified: Tue, 09 Apr 2024 18:50:56 GMT  
		Size: 192.2 KB (192163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630aeeb83a4eab64e8278fc980ef0400396d2493c57fa139d2fc9fb1f73fbd5f`  
		Last Modified: Tue, 09 Apr 2024 18:50:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e262332d270678e1ca292aa40a3ff40dc4d8447a2090f9250fd1f7a0f644f48`  
		Last Modified: Tue, 09 Apr 2024 18:50:57 GMT  
		Size: 109.2 KB (109246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.20` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:578c1b3c788ff60c6194b75e6a6fb29c0ca534247a466486c85288d84aa30666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c4ccd2a97dbcfc21c940b47fd652f24d9848cd8ae43c23de0581e95900e48e`

```dockerfile
```

-	Layers:
	-	`sha256:3e69e756c831254afed42537297418df063bec5a7e5f1660cb23948925b9e724`  
		Last Modified: Tue, 09 Apr 2024 18:50:55 GMT  
		Size: 2.3 MB (2311485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d96710f16d89b543c48a52206e603a618e6333fb10fe6abccea39e2e56aa9978`  
		Last Modified: Tue, 09 Apr 2024 18:50:54 GMT  
		Size: 37.7 KB (37742 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.20` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:6c56f6ae7059ee5ff236e928e4d0c9006e06fdbe47d480d13733fc74645d9148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360370187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc12e42703118f2b4a628cfe300347d3b7dd6695894086ad393fbaada856e429`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 09 Apr 2024 08:24:48 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.build-date=2024-04-08T08:34:31.070382898Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b26557f585b7d95c71a5549e571a6bcd2667697d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.20 org.opencontainers.image.created=2024-04-08T08:34:31.070382898Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b26557f585b7d95c71a5549e571a6bcd2667697d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.20
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c50df22b286b32751200d045cfb4487c468d64927726c21ab4dcaa274ec8db9`  
		Last Modified: Tue, 26 Mar 2024 18:57:22 GMT  
		Size: 7.3 MB (7331876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57048565a15c1497df0d5d8c6297e5593193b7faeafbfae200beb93d72e946`  
		Last Modified: Tue, 26 Mar 2024 18:57:20 GMT  
		Size: 4.3 KB (4324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66d3d016007d4289658a2a3e2b667d69bef75d4019e48594af1d8d6c9008fc`  
		Last Modified: Tue, 09 Apr 2024 18:53:00 GMT  
		Size: 326.8 MB (326752626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f843ab59bfaddf93e1ed9b2cea65cd240bfb5b5c92ffa14912440d6ddb213075`  
		Last Modified: Tue, 09 Apr 2024 18:52:53 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f273646ecc5d5ecdfa78f1c31abc012b26424c512d38daec370235db31bd1d`  
		Last Modified: Tue, 09 Apr 2024 18:52:53 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b663d030d33a2b9ad9351b38e0ded6c30819a009a26defa96d3dd8532d0921`  
		Last Modified: Tue, 09 Apr 2024 18:52:53 GMT  
		Size: 186.2 KB (186195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542c215b65d54a795958ca974882267dfc295c132a76229fac9bce6bf75ded73`  
		Last Modified: Tue, 09 Apr 2024 18:52:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3ea880c5527c5f69ee0c76c62fce51c1c64e91d91dae73f7a1e20c38256ac8`  
		Last Modified: Tue, 09 Apr 2024 18:52:54 GMT  
		Size: 109.2 KB (109249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.20` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:946da7e64523200d9b666dab270ed655a885ba4b81cc3ecb999e825d83432623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42b154fd6ce4d19d9fcd4fc2ae86cebb3e6f9ab8ec3aa7e274178fafc0ba45b`

```dockerfile
```

-	Layers:
	-	`sha256:45c15a7d5d6d7e4e5963e023aba225d339cb338c2dfc6af263934255fd7d3a56`  
		Last Modified: Tue, 09 Apr 2024 18:52:53 GMT  
		Size: 2.3 MB (2311702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8a530594519d42657e7e58ec91e4b259b49ff22235f5678330c6bb26d44c273`  
		Last Modified: Tue, 09 Apr 2024 18:52:53 GMT  
		Size: 37.7 KB (37745 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.13.0`

```console
$ docker pull elasticsearch@sha256:e70e2bc1f88987edac86e0b0a95f18e0e5b0b6e34eaf37074aa4aa5f6919b603
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.13.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2e06e0c83c551485faf8d49c354dbcbe5757f66fa82f27e753b36e2d3aa4b746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615312389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba1a371c8e771b1af9dc46432534d20c7d630e67e27c3a7ba4924c99454fa38`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T03:35:46.757803203Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=09df99393193b2c53d92899662a8b8b3c55b45cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T03:35:46.757803203Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=09df99393193b2c53d92899662a8b8b3c55b45cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["eswrapper"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b190db87e221cc1308d2e688ea9a83e09dda1b55ec50e9972f3dc260f0154f7`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 7.5 MB (7512513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa109031a696acdb26e523b807153d6070daaa043d16fc00fbf2bf4defab3d9d`  
		Last Modified: Tue, 26 Mar 2024 18:50:50 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08466127fcdb52493482da50e03efa0d702e3ae1a7c5d2823ae6513b9a9edd5f`  
		Last Modified: Tue, 26 Mar 2024 18:51:01 GMT  
		Size: 580.0 MB (579968400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5861b544bdb8bb365de4f07eb5ae84053d4f11ad0e955f4d7c72c9e3186d8ba1`  
		Last Modified: Tue, 26 Mar 2024 18:50:50 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d6b772957a38409db17e87e372cc3e107a3c53b7f2061c5692ab5bbd2ca838`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8288a7b93c5b6b6c37d89cebdbfad8082d65fad0dae864f472ec32b6ea7d9c`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 191.9 KB (191906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b4d3945e0f22a1f0150a19f73c269d35767c45d686dadc31a5c74763e05bbb`  
		Last Modified: Tue, 26 Mar 2024 18:50:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0122d88049315688a64c2a92b4b767e4dab2f3d874a3809f2f3db32c8549ec52`  
		Last Modified: Tue, 26 Mar 2024 18:50:52 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a2d8ae470c19a09fbd4c542d256ea179fe7644f08eb810aeb74e19aa4c582fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2eb6512b147ac967b87700dcaf456d1e8faf1f678ba6d2590a2452d082f5c69`

```dockerfile
```

-	Layers:
	-	`sha256:be8677b7c6276cb489c32d8da09c93c7ac927be31371fff2551d27cbf6f0c6fa`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 2.6 MB (2590070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff309f0a22fe7d63df20b866644a34b82455e672f37ea622c1b72f69cadedc9`  
		Last Modified: Tue, 26 Mar 2024 18:50:50 GMT  
		Size: 37.8 KB (37757 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.13.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:223e8fa0331a01364ba1ee7d5a4ec219d047ebadc8231d570ff87fca0b1da6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.4 MB (459420510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bfb2697483e0bdc9d3c0208a4fb9f579455a75403c7be9d5945bfbad904848`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T03:35:46.757803203Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=09df99393193b2c53d92899662a8b8b3c55b45cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T03:35:46.757803203Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=09df99393193b2c53d92899662a8b8b3c55b45cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["eswrapper"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14e5e1b762bfecd88ab86a4faf77d6a3199d588e85e7407913816371679657a`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 7.3 MB (7331903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf899c8d88bb7608d07eda424716015466893306895ab7e5d094900f153bdb26`  
		Last Modified: Tue, 26 Mar 2024 18:56:00 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b9969e4f4e4faabe36f710e31bbca65b235109f03bc43a6e7dd94c9b5f5dbe`  
		Last Modified: Tue, 26 Mar 2024 18:56:11 GMT  
		Size: 425.8 MB (425803447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1079e422fd69fed0509b31ce2fc1f3693607fec5e6f46e8c15ae5cdf4e55ee2e`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46279a912b6b1e38401f4b7d596a076a4e67bbf6b313878c66c6cc9ca52942e8`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb703192bdef9a2b254da889a3c1524adce873cda1f5f1a6f63352820d2a8e2`  
		Last Modified: Tue, 26 Mar 2024 18:56:02 GMT  
		Size: 185.9 KB (185932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b83a0c8d826e0a6159aa7233c85c9ebc232b80fe0c9479fef82752e5f16b1f7`  
		Last Modified: Tue, 26 Mar 2024 18:56:02 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81667493e1e6af1edbc07bcf742326013af80e6a6824930665c5a0b14ae65150`  
		Last Modified: Tue, 26 Mar 2024 18:56:03 GMT  
		Size: 109.3 KB (109259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d7b8e95a5f259c766897378b2c2028350bf9cb3ca132445f3b2523ffe2d50008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b2569b2880376d1da7828aa0f2a8e4ab1ce781dc8f5f410b83733f391091e2`

```dockerfile
```

-	Layers:
	-	`sha256:40eb042c66842dd8ee05f2eb974a7139247f1be77e74cc218dfa24b658a5767f`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 2.6 MB (2590303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c56700f68e57448d8b6376e76f982da10345b8301993c12963c4d32ea5e65d`  
		Last Modified: Tue, 26 Mar 2024 18:56:00 GMT  
		Size: 37.8 KB (37762 bytes)  
		MIME: application/vnd.in-toto+json
