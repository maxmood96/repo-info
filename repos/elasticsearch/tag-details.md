<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.20`](#elasticsearch71720)
-	[`elasticsearch:8.13.0`](#elasticsearch8130)

## `elasticsearch:7.17.20`

```console
$ docker pull elasticsearch@sha256:69749ba67d997b6011cf05bb785151ac53c57a88467f65796ad123bd59e78d79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.20` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f4b58041708b48b82c92b91e5c7a6f4e6e10a8464a68070fe2fa31ce16704d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.8 MB (370778234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece573fa477b50ebdab906575711de1c2bc5c056ab0fae34698f23b930adae5d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Tue, 09 Apr 2024 08:24:48 GMT
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
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
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
	-	`sha256:4477f8fe99ebfd23fa06d28a2fa42eaa05d726926afc0a055e1ff2b612b7a293`  
		Last Modified: Wed, 17 Apr 2024 18:54:17 GMT  
		Size: 27.5 MB (27511740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09f09f9d1fe4c94bf32d080bc79e2f248c46b3fddff551705ad2cec73d2c4bc`  
		Last Modified: Thu, 25 Apr 2024 21:51:55 GMT  
		Size: 14.1 MB (14101294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73867ac551969a5b7ca3f9cb50f451ce20df9a3623e42b133ee673ff20d9fa4`  
		Last Modified: Thu, 25 Apr 2024 21:51:54 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb90e4e24227a8c74ef1ab17a4762ef8d5f1e20a1781955fc4b4198181bb635`  
		Last Modified: Thu, 25 Apr 2024 21:52:00 GMT  
		Size: 328.8 MB (328847527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7d2dd784fea481efe8da18f234dace6d1f1e950d51fe34b604a1a8621fe875`  
		Last Modified: Thu, 25 Apr 2024 21:51:55 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2747988c6aea4f2f43c7334ceff59c44ee690542c201169d3faed29d36066fc`  
		Last Modified: Thu, 25 Apr 2024 21:51:56 GMT  
		Size: 2.0 KB (1980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97cd51b0d01a38f738bf92c6de1efc7364d983ae0761381c06d3c10bd7ea948`  
		Last Modified: Thu, 25 Apr 2024 21:51:56 GMT  
		Size: 192.2 KB (192164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e722d67a11a9fbb86d325a5a2cfdbe2e62a9ea1c3dfd70e8d459d46aa267dc`  
		Last Modified: Thu, 25 Apr 2024 21:51:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fe60574680884e04490d481a9d19d4693c79493422ad8bd21dd833cc649835`  
		Last Modified: Thu, 25 Apr 2024 21:51:57 GMT  
		Size: 109.3 KB (109253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.20` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5d7e4369d94d8228bae9e8bba3af3a9883d2e7890adf3d20b8fce462311f661e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2350277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aad2cd2073d9efc998495c655209cf36ae40db866417310f5b905a5a9ed044b`

```dockerfile
```

-	Layers:
	-	`sha256:d5f7a3b525d127ee9e88d862f20fdf74716b09626faab4d8cfb2926719d2c9c5`  
		Last Modified: Thu, 25 Apr 2024 21:51:54 GMT  
		Size: 2.3 MB (2312522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2314b432464431a1369211ffd839e84ca4c6691343a8d0a9a29c6fd3b6c9093`  
		Last Modified: Thu, 25 Apr 2024 21:51:54 GMT  
		Size: 37.8 KB (37755 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.20` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:94c5dab6731be597da552565e6c9c7ad4f4a848f250cc0410171cd1b38fea4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361214631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36a53e9899b79e3d57dde001414fe0270f2c7c3989c8f39b195feaee48304ad`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Tue, 09 Apr 2024 08:24:48 GMT
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
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
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
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebfd7633338ad259a85ab2d6f891ec4673354f10af7ccd5ef0d546999d8b458`  
		Last Modified: Tue, 16 Apr 2024 09:50:12 GMT  
		Size: 8.2 MB (8175863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc9ac907ae0425f033bbd86560f6399d84d06755af08480b6d8b5caaba2a3a5`  
		Last Modified: Tue, 16 Apr 2024 09:50:11 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6700897d1eff0f459668a132b4daca875053ead95e84cf5f313e0429661a255`  
		Last Modified: Tue, 16 Apr 2024 09:50:18 GMT  
		Size: 326.8 MB (326752622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888b8cf6a7293f95a124b1e35de06e6b350acdfe954b115fdf3fab07880d23fc`  
		Last Modified: Tue, 16 Apr 2024 09:50:11 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58264cea9eacd1c5681c285605c675da394fc270486c9e17ca36b8ba4b6dc8`  
		Last Modified: Tue, 16 Apr 2024 09:50:12 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af432a9bfd21030048a8e98e59719332a5bec7e193a71fd9c1c6c6582139899b`  
		Last Modified: Tue, 16 Apr 2024 09:50:13 GMT  
		Size: 186.2 KB (186173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf89f8815abecf0e76167b99b041c0cf936a3f9578d6947f7a7d9cf02c9a11df`  
		Last Modified: Tue, 16 Apr 2024 09:50:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ca00094032082c3c563388043466ddccba7423575c6056908d2a371ea0f414`  
		Last Modified: Tue, 16 Apr 2024 09:50:13 GMT  
		Size: 109.3 KB (109253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.20` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b4db7e251f50718aa9439db041496015be0aa217766d035d8de83e6bc3044c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2fe56f13712abf0f3eff77195b2265dc82c44f790d88fd84ce4f43ce6488ab`

```dockerfile
```

-	Layers:
	-	`sha256:4e89483641cb2d88b2f7acc877fcd8a135d739aca084e37347db639290fc498a`  
		Last Modified: Tue, 16 Apr 2024 09:50:11 GMT  
		Size: 2.3 MB (2311702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68e0553e9e057be9ac3830efd9d5abc5d5a66124f02a8baf008051c4ae73332`  
		Last Modified: Tue, 16 Apr 2024 09:50:11 GMT  
		Size: 37.7 KB (37746 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.13.0`

```console
$ docker pull elasticsearch@sha256:f5b202a4934a3d44b6521d83970d7c604861ed9ac6d1b2abfac8ade2748fa02f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.13.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2b79ab456238e1331d99aed56c0a70810c677f45f8fb050e7db4594365cc3364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.9 MB (621898544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a9b5f8609f5f37a7c702424a3555094b90caeae6164bebce65b1af78e9c8d8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Tue, 26 Mar 2024 13:49:26 GMT
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
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
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
	-	`sha256:4477f8fe99ebfd23fa06d28a2fa42eaa05d726926afc0a055e1ff2b612b7a293`  
		Last Modified: Wed, 17 Apr 2024 18:54:17 GMT  
		Size: 27.5 MB (27511740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee18bf6d37c583265e90cd39a0305b983942430441cff7fe9128ededfa1aa015`  
		Last Modified: Thu, 25 Apr 2024 21:52:13 GMT  
		Size: 14.1 MB (14101262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bceb331b91a2e9dd239ef2eddd9154a8cea719b0bec019a74539125ac107fa`  
		Last Modified: Thu, 25 Apr 2024 21:52:13 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad262b52003c19cbb78cd4688e2c88e09696dd1ed9e2f6343efbb3d4b777d02f`  
		Last Modified: Thu, 25 Apr 2024 21:52:20 GMT  
		Size: 580.0 MB (579968372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19485f8ea70f247cd40f7b6deeb39cd9030e597fe691d33e91b64c856c4a762b`  
		Last Modified: Thu, 25 Apr 2024 21:52:13 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5e360733cb9731dd44b93c7cfb36ba539e2634f589c6782bd22cebd074003`  
		Last Modified: Thu, 25 Apr 2024 21:52:13 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb731a7c4fa15b98ba6c2685d7edc27891dab3ad1dc103090e081ead3630d4e`  
		Last Modified: Thu, 25 Apr 2024 21:52:14 GMT  
		Size: 191.9 KB (191907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783f4eec344adc7235e4ce13d57a9e7d92928aaa0367cd0ac8070e6a9f9672b3`  
		Last Modified: Thu, 25 Apr 2024 21:52:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626d3b6641385e1d2ed84cdc3c012c0d31dfe1f6abe7e3bd5e366bcb4deb6243`  
		Last Modified: Thu, 25 Apr 2024 21:52:14 GMT  
		Size: 109.3 KB (109254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:88b595eae55f6dcbf632411e163d76961b1c45799453114a9f657b9d30772806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c30699510880f93753ef710ac66be3494ba27eec964243e290b9ae4763ee795`

```dockerfile
```

-	Layers:
	-	`sha256:7165ebd220fd921d221cd2dd7d8658f2231c76025b702b37e8248172ca48795b`  
		Last Modified: Thu, 25 Apr 2024 21:52:13 GMT  
		Size: 2.6 MB (2590153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f188b8c39dd457367bada9242d119c4341a86a0accfabfcadcbef15985c432b`  
		Last Modified: Thu, 25 Apr 2024 21:52:13 GMT  
		Size: 37.8 KB (37770 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.13.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:ea06e220003d622101f0c419e214536bda98317d616add638d466e1441015b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460264839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9a1115a4c445a92e405796c2dd1c95e5425167dbaf62a7cf233a2ac7e81b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Tue, 26 Mar 2024 13:49:26 GMT
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
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
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
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0af4f133a7dfab3e2ccaf3e71c8c7a943586cf4ace4284e34938697aa12f49c`  
		Last Modified: Tue, 16 Apr 2024 04:57:15 GMT  
		Size: 8.2 MB (8175929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b620d53e57c5ec1c6367541886f747488b632ed164e94788bfe78b1c6255f9`  
		Last Modified: Tue, 16 Apr 2024 04:57:14 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0c7c530e762565f80e350895ba0eced106ec7d8b052396cfe9df94e3c4faaf`  
		Last Modified: Tue, 16 Apr 2024 04:57:27 GMT  
		Size: 425.8 MB (425803280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fe6980a74f34f75550e0dc6806dc0ad8a9b4e6fc7da09f207955a90381ee91`  
		Last Modified: Tue, 16 Apr 2024 04:57:15 GMT  
		Size: 9.1 KB (9093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4774a55de2261cdf056fd5199fe0addf6baa06f4e7eb8d5357bb10f641dd53b3`  
		Last Modified: Tue, 16 Apr 2024 04:57:16 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d40c3b91e67562788ddc28edfd1c811c3cf63f64366e8bc6d1ae5c1b81ff0`  
		Last Modified: Tue, 16 Apr 2024 04:57:16 GMT  
		Size: 185.9 KB (185914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75d69d4c0e6eda518c93e00df0542a8c54af53258eb1aaa62b88d69693e4b8a`  
		Last Modified: Tue, 16 Apr 2024 04:57:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb11e34dfb358ecccb1607ad4f262d5e02a64dba6eaadd99f8407357e99b96c`  
		Last Modified: Tue, 16 Apr 2024 04:57:17 GMT  
		Size: 109.3 KB (109254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:552bd26ae1d1322f789c170a10119fffda66b12aa9da4cd60f29718cd6ac4a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94aeea1f471180a4ec6251b4ef19cca59330a618c7caf517e455fc3649e29f`

```dockerfile
```

-	Layers:
	-	`sha256:2264e61e2fab13b3d1fd3732aca76d094c969a8ef201a5192f41236d03836fc9`  
		Last Modified: Tue, 16 Apr 2024 04:57:15 GMT  
		Size: 2.6 MB (2590287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb44e6c1fc01cbc10d0b3f0fcc5524a49d676d02768478ac8f450cfedc34b43c`  
		Last Modified: Tue, 16 Apr 2024 04:57:14 GMT  
		Size: 37.8 KB (37762 bytes)  
		MIME: application/vnd.in-toto+json
