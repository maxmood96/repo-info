<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.20`](#elasticsearch71720)
-	[`elasticsearch:8.13.0`](#elasticsearch8130)

## `elasticsearch:7.17.20`

```console
$ docker pull elasticsearch@sha256:89c5c3adc9cd2a3cbfeb9a6eb9b399f16a54e1ad1423cd94856419e80ac95eaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.20` - linux; amd64

```console
$ docker pull elasticsearch@sha256:8b5b835384eacd28c1295d1c927da97f0f793f77b37faf32876c9a152452dcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364189748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88e1314b43b9da390770d88a728d356dea85fee2d48a6b79d854967b3f39d70`
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
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
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
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d4b0a1128f5b62bb3f4ffc785d576355538a8a6808cb6774266467970cae5d`  
		Last Modified: Thu, 02 May 2024 00:52:44 GMT  
		Size: 7.5 MB (7513063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cab1abf274fc286e25d2d12d06d62b2f4abe069e226704bc50259c13874968`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091252f7c9c3edf61d02ac132d43f0b74eff493e7a3ff4bb8719e97b738f5bd4`  
		Last Modified: Thu, 02 May 2024 00:52:48 GMT  
		Size: 328.8 MB (328847363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba22547cb7b528402b5684e33c1fc3694d69dffa7aa73cc5059659a98e3047af`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb5ac7a61d14740820c72145900e8acd0bdfa323f102441dbfadd4fee35454e`  
		Last Modified: Thu, 02 May 2024 00:52:44 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ac87136b0fb96486ffeac4bad1a4ddee5938ac5b40dcaeaff707909e8ea3fc`  
		Last Modified: Thu, 02 May 2024 00:52:44 GMT  
		Size: 192.2 KB (192167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03977b84fc22802f7f48e1ce151e864726dff94a2b6138c88c43c6e8ad4edcef`  
		Last Modified: Thu, 02 May 2024 00:52:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9719a7448f42b344e3e61d027060cc60a7272c4b7c037b964dfda7c64c86e7`  
		Last Modified: Thu, 02 May 2024 00:52:45 GMT  
		Size: 109.2 KB (109248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.20` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0c98fad4591d1871187ae007a064ffb329084513a67410d8b429e20a145d197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2350268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1644287c5ed8312e9ecedf26eb006dc8a8ba3b9444c314eafa57ef45ddbbe7`

```dockerfile
```

-	Layers:
	-	`sha256:8a942b644bba299cab3408d135acf025c653cb48a67f7efadb65c960595c6089`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 2.3 MB (2312522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e7195111c11958ecfde1d33b470dfd37cf77a7f41bf5b74b9c3b3a5fe1eea8`  
		Last Modified: Thu, 02 May 2024 00:52:43 GMT  
		Size: 37.7 KB (37746 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.20` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e3235c4f8b6bd4767cc5278559cd5fdecba85663db820f73597649b42c3be35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.9 MB (365890969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72fecdae27d95bfa35c53865d13b3197d7727198f17764298e4f49a0f894857`
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
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
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
	-	`sha256:935803725f5775642918295f3557fecf93003fde6403df6fcbb2379ce4795a1d`  
		Last Modified: Wed, 17 Apr 2024 18:54:25 GMT  
		Size: 26.0 MB (25976141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac237515240bdbb6ae1b0e507196e1d79fa1699f735eac5cef73567d070a25c`  
		Last Modified: Fri, 26 Apr 2024 07:46:54 GMT  
		Size: 12.9 MB (12850968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1511e67052bbb9a07ba2e2c3850c94bb9441e4c9bc5583d8df08fab94e74b6b`  
		Last Modified: Fri, 26 Apr 2024 07:46:53 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd18e81f23045fb20835f199507322dc3949783960d3c26a2ff44ba8a217578d`  
		Last Modified: Fri, 26 Apr 2024 07:47:00 GMT  
		Size: 326.8 MB (326752587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43591ed4cf3a6788d38c3c9b3654393e3f7b10530c6dbb8a95e09cea95b67419`  
		Last Modified: Fri, 26 Apr 2024 07:46:54 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b487440cab572ef3d20bd31f0fc953b436cf0d0a9a7513e38059d5c776eb0`  
		Last Modified: Fri, 26 Apr 2024 07:46:54 GMT  
		Size: 2.0 KB (1980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d0657ec7d5d1efd2d9f16e158673a5d68cd2b48b98435861a4e9e0db7316ec`  
		Last Modified: Fri, 26 Apr 2024 07:46:55 GMT  
		Size: 186.2 KB (186184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5fa854ab3ba01324d8e7d6316558a6f79c5b3035c40a7df20d8219e3ef5802`  
		Last Modified: Fri, 26 Apr 2024 07:46:55 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293d310f153070a4241eef5488c2cd7773d12848787622876431e1b471a70b4f`  
		Last Modified: Fri, 26 Apr 2024 07:46:55 GMT  
		Size: 109.3 KB (109254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.20` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:46b2a1a9d0d54fadfe33ec40c962b7e1e4eee4b5c918c0b06bee93e47df92cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2350497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c08cafaa15b43866407e281c9a90423e139bca38ffcd28b117ed52ce1695d6a`

```dockerfile
```

-	Layers:
	-	`sha256:3d374c1e258d465bac8f2d51777e3413afdac2f7d07c843f25706c30a8799c17`  
		Last Modified: Fri, 26 Apr 2024 07:46:53 GMT  
		Size: 2.3 MB (2312739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b473d14702050db092e953b940b693f897c41dd3ed518bba2cb1558e8e1644e`  
		Last Modified: Fri, 26 Apr 2024 07:46:53 GMT  
		Size: 37.8 KB (37758 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.13.0`

```console
$ docker pull elasticsearch@sha256:8d20c772e0a76bad9c7450092eab1550aa7b463b57df78988e96a973a33efff2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.13.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:873922989c6d2b276b93d6945796d87f1779a746aac0d8b7f186987e9d909fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615310065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebd258614f1a949059c1ef479d55fff22fe33389d8603d42015a9195ae2fa17`
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
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
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
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2ea7991ac665ee0176f1767a0cb6321d77991b875c43789d414d779fffadb6`  
		Last Modified: Thu, 02 May 2024 00:53:29 GMT  
		Size: 7.5 MB (7513091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d59af47707f0744635284568e60401f4d034614391cc6ea3f5b4a2b2702e87`  
		Last Modified: Thu, 02 May 2024 00:53:29 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f7c08d05fb64450017768a5d90aede83a59daedb0c76ca98f0726b2740aeda`  
		Last Modified: Thu, 02 May 2024 00:53:37 GMT  
		Size: 580.0 MB (579968162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ec7e3a371d809880bdd063b9d3810103f7f379487f4fb426532401544c13d4`  
		Last Modified: Thu, 02 May 2024 00:53:29 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863016d5e58d01da6746f66919f587684a5b6edf1003efac9f695e2dfa287460`  
		Last Modified: Thu, 02 May 2024 00:53:30 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6460b9bccd157aa152242c0e1eb056660ded4af874866180ea121ebc9cbee77b`  
		Last Modified: Thu, 02 May 2024 00:53:30 GMT  
		Size: 191.9 KB (191906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c63d583e86b5114cb38b65cc03578d62007449a101d81c540b1fe86a114fe30`  
		Last Modified: Thu, 02 May 2024 00:53:30 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e6e2a58f42cd798e6556b5aefc59942b4ed01de06534b7a392ff4c4c24bf4d`  
		Last Modified: Thu, 02 May 2024 00:53:30 GMT  
		Size: 109.3 KB (109253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:105f2a041c8ffff86a6c835edfc17b6b06f84bd8d9d089225e62605cc121e21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e0ebace38b4f779a3ea9a571de55167068d7599bc8f0c640b44c407782d35f`

```dockerfile
```

-	Layers:
	-	`sha256:114e74b1e7247f23f6e0fca4a290c78b23c9a8f4c95c79c6e0e0fe35f4c3adc4`  
		Last Modified: Thu, 02 May 2024 00:53:29 GMT  
		Size: 2.6 MB (2590145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e42475393571e7b0ae65f138bbf21bf2acace3f2d390424597c4b87ff74e3a`  
		Last Modified: Thu, 02 May 2024 00:53:29 GMT  
		Size: 37.8 KB (37762 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.13.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:dfc690d2788dfe07982c43631016271de8a00b0b6b0b278f2dcf18839ba068f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464941116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f86f2f717e44587d464cc0ede3ea37964d6b7e0ff67d19b1c7f29e7b0762f6`
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
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
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
	-	`sha256:935803725f5775642918295f3557fecf93003fde6403df6fcbb2379ce4795a1d`  
		Last Modified: Wed, 17 Apr 2024 18:54:25 GMT  
		Size: 26.0 MB (25976141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c68a907a0e04b8f16a7edc4bafd5e52d081bcd29854b7a5ce8440d4b86825b`  
		Last Modified: Fri, 26 Apr 2024 07:45:32 GMT  
		Size: 12.9 MB (12850935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415d6a34a254f788e74dc659d2d0d4d5cadab24c7a668a83d13b3c62e3722293`  
		Last Modified: Fri, 26 Apr 2024 07:45:31 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e1ac3e986ec4b76992d9cb4b388dd7753e0e10020669e5715171b9c25b6b8`  
		Last Modified: Fri, 26 Apr 2024 07:45:43 GMT  
		Size: 425.8 MB (425803294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9b5f70d7a8b8f695a7fd2c91e786d341cbc83b04a553cd8668a92a7ca06dac`  
		Last Modified: Fri, 26 Apr 2024 07:45:33 GMT  
		Size: 9.1 KB (9092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6580ae537e6fb2cdc79af7043a20eb52313f4455eba9f1be8a3fd823826f1073`  
		Last Modified: Fri, 26 Apr 2024 07:45:33 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c950a093b2ec3458f4e3e70c7509f392694201a490db09f4229e6d5c5aaff`  
		Last Modified: Fri, 26 Apr 2024 07:45:34 GMT  
		Size: 185.9 KB (185920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4ec05c7050e74a782e9bee0fe8dc06ec684e40c7706e3735ca9d6bfdfcf381`  
		Last Modified: Fri, 26 Apr 2024 07:45:34 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b0a097840c8c6564e46d9693565aa57cae41252c546cf8eb895244acfecd66`  
		Last Modified: Fri, 26 Apr 2024 07:45:35 GMT  
		Size: 109.3 KB (109253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:fc598f022f9bc69995086f523378c6145d29cfbadd113f6ed8998cf6bd576cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c70bd7ce84ad1597d2e60087bdf497939342d8b8305e75e9ec9dd8aa8df514e`

```dockerfile
```

-	Layers:
	-	`sha256:1a7a30cc65c3c284d76a6da9d4ddd647b6e7c748d47550fc542efb7644ad3b40`  
		Last Modified: Fri, 26 Apr 2024 07:45:32 GMT  
		Size: 2.6 MB (2590362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898a0889f07ad68c05d9284495d276e1cac1c49650a56458b7d13d84eac7ce99`  
		Last Modified: Fri, 26 Apr 2024 07:45:32 GMT  
		Size: 37.8 KB (37775 bytes)  
		MIME: application/vnd.in-toto+json
