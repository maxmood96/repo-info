<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.20`](#elasticsearch71720)
-	[`elasticsearch:8.13.0`](#elasticsearch8130)

## `elasticsearch:7.17.20`

```console
$ docker pull elasticsearch@sha256:9b62bc115d32ff25a7a84319e2a6f5c1ef7e28754dc6f40232e7a0d41d5063f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.20` - linux; amd64

```console
$ docker pull elasticsearch@sha256:a38105db6638bee65ae1c65d071a4f3eab14707de736f2ec8aff233f3656684d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.1 MB (365063366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0ba3f43d516cac954d089f141612701c7766ad5af29f137b9f6d7d9b6e6f1`
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
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
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
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d63249cdf19e35871818bee0514a986d1c2ece19a6535bce1e603d100ddd2a`  
		Last Modified: Tue, 16 Apr 2024 04:25:51 GMT  
		Size: 8.4 MB (8386490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d148d277e5143b750d66ea62637da2b3a06b6d94caae1ffe86df1646f3fe20`  
		Last Modified: Tue, 16 Apr 2024 04:25:50 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363be05f550bb1d1033d98d376662f768f10f043849729643b1a611ac98139a8`  
		Last Modified: Tue, 16 Apr 2024 04:25:56 GMT  
		Size: 328.8 MB (328847369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c993213d3e1cca8f044649b4698eddddbc567062c6adcca58f595bbce060583`  
		Last Modified: Tue, 16 Apr 2024 04:25:51 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76a57ed7a450d0fab0d5bac7f1e2cb002ef766e1f7617aee428a1ed9020ae9c`  
		Last Modified: Tue, 16 Apr 2024 04:25:52 GMT  
		Size: 2.0 KB (1976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e69c14073c44a6fb9f607c1eabe1be820b3ada03ba2c72101ce44fdd0bfa356`  
		Last Modified: Tue, 16 Apr 2024 04:25:52 GMT  
		Size: 192.2 KB (192165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303765b7b00dd87c3e67317660ca7892bb2c81a9e50a17e4b65598fdd40cd041`  
		Last Modified: Tue, 16 Apr 2024 04:25:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18f20330b5d6894757f73283a344800c498cd377280f5e71bf0e2efd2fb78b6`  
		Last Modified: Tue, 16 Apr 2024 04:25:53 GMT  
		Size: 109.2 KB (109247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.20` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:bfdb568f3edd8031446657280b32fa0f44d430eaf456c4dcf665c7327e23c295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3000a9d20407253b9fbd6e46c38d4d48e23e054cfe2ce75890255c2dee56bc5`

```dockerfile
```

-	Layers:
	-	`sha256:b1624b418177d79ac152c6fdf9fc916ce0aeacc7ac1176a996bb69ea4f3a774a`  
		Last Modified: Tue, 16 Apr 2024 04:25:51 GMT  
		Size: 2.3 MB (2311485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a71d24e482627120dd0ebee2d76de6ba2a54d9169a71ba69cc63d06f0776649`  
		Last Modified: Tue, 16 Apr 2024 04:25:50 GMT  
		Size: 37.7 KB (37742 bytes)  
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
$ docker pull elasticsearch@sha256:1886408460504dd4b2eef769024f65bb4d884946016ac329bfc4e0fcee2c67bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.13.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:296ee81366ecdcd183dbecf528935ec69f8ae32527d6991510d0428dfad7807b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616183900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcf95651ab53c0f3a822c55e081cdc7418c3704a39387918cacd8ca2130ca4e`
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
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
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
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44273b1b58bca5d26e4718ffc0e41a1ea8b06d6ac046fd13610856d6b83b85d`  
		Last Modified: Tue, 16 Apr 2024 04:26:57 GMT  
		Size: 8.4 MB (8386478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf4a1cae40bee39cfb6545e9b9157722d5b7d40358bc5d289c40c890beb3536`  
		Last Modified: Tue, 16 Apr 2024 04:26:57 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf9417084f3c2de53885211dcc8fd44ea51c8f959dc673c3207a1d53e1d0db`  
		Last Modified: Tue, 16 Apr 2024 04:27:05 GMT  
		Size: 580.0 MB (579968424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea381bc37e8045de02b73cc4170573962c373266517bf066a3f15fd0fd80e2`  
		Last Modified: Tue, 16 Apr 2024 04:26:56 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c16437eb432c109278ecff9cc52e05a150f6f0d3dded18928df3e6e11c9e0f1`  
		Last Modified: Tue, 16 Apr 2024 04:26:57 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04f366f67f5562c5f060ba6032e4551ff5664bcfb880386b3097884389a28f7`  
		Last Modified: Tue, 16 Apr 2024 04:26:57 GMT  
		Size: 191.9 KB (191910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1a75fe40bb2688d4c7fdda9d2a11eefcbce522df75a0fd70fba794dee7e42`  
		Last Modified: Tue, 16 Apr 2024 04:26:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9b0cb48f22a3dc17ee8f37596920104f982b990cc787514a0db32c3d132249`  
		Last Modified: Tue, 16 Apr 2024 04:26:58 GMT  
		Size: 109.2 KB (109249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2e7ce93ac14f6213ebe38e030fafa1f2bdb75aaf3eb731f846721eef47ed6c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c770ba1f6a24afe974cb4b51dea451c3b859925019df0e4a3da1ee973168faeb`

```dockerfile
```

-	Layers:
	-	`sha256:79327776d477a25c94d8478cae38ceb3ad8b4aee988c63dc16e4e8e5249d3d03`  
		Last Modified: Tue, 16 Apr 2024 04:26:56 GMT  
		Size: 2.6 MB (2590078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0d6e8704b5b9313e1caaa6f2b30f210d98bbd3bfeb27a59644ae26cae45241`  
		Last Modified: Tue, 16 Apr 2024 04:26:56 GMT  
		Size: 37.8 KB (37758 bytes)  
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
