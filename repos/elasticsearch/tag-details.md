<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.11`](#elasticsearch81911)
-	[`elasticsearch:9.1.10`](#elasticsearch9110)
-	[`elasticsearch:9.2.5`](#elasticsearch925)
-	[`elasticsearch:9.3.0`](#elasticsearch930)

## `elasticsearch:8.19.11`

```console
$ docker pull elasticsearch@sha256:752a824ff8f8ab6aa5111c597185967e24d61c7bd9252a110073be389015f479
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.11` - linux; amd64

```console
$ docker pull elasticsearch@sha256:67febb0bbcfbd2ad588a07800918d6caa0a7793cabe2b69762e0242c716d4915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.9 MB (722921259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0529ef7114d93ab05401c0bcceb6ad723c7fc2989571edbc707b72989b8f89`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Tue, 03 Feb 2026 18:57:21 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 03 Feb 2026 18:57:21 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 03 Feb 2026 18:57:21 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 18:57:21 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 03 Feb 2026 18:58:20 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 03 Feb 2026 18:58:20 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 18:58:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:58:20 GMT
ENV SHELL=/bin/bash
# Tue, 03 Feb 2026 18:58:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Feb 2026 18:58:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 03 Feb 2026 18:58:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 03 Feb 2026 18:58:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 03 Feb 2026 18:58:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 03 Feb 2026 18:58:20 GMT
LABEL org.label-schema.build-date=2026-01-28T22:06:09.337243873Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c5253e1bcb0268a5dafed9dee18e16fd3144d7d6 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.11 org.opencontainers.image.created=2026-01-28T22:06:09.337243873Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c5253e1bcb0268a5dafed9dee18e16fd3144d7d6 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.11
# Tue, 03 Feb 2026 18:58:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 18:58:20 GMT
CMD ["eswrapper"]
# Tue, 03 Feb 2026 18:58:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd230edf7729651b76b0e6d790047950fae154c36f8116d61dfd44211536a5a9`  
		Last Modified: Tue, 03 Feb 2026 18:59:10 GMT  
		Size: 13.0 MB (12997278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fdc0a8a3a5f2bfd11d08f64732d24e54b88cc4eebba8191db2c683d6b0c47c`  
		Last Modified: Tue, 03 Feb 2026 18:59:09 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a0f50e23ca082142b4caa601f339c5cbceb765f8d690cf44d07080678c163`  
		Last Modified: Tue, 03 Feb 2026 18:59:22 GMT  
		Size: 679.9 MB (679903290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec74c16b695c49fa5021be493bf0589588c598d6df8e2f64540bbf264166d363`  
		Last Modified: Tue, 03 Feb 2026 18:59:09 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92851e16c85b4fbc66501ddbf5ed2ace377017bdae0a9eedb87c1032672f3c3e`  
		Last Modified: Tue, 03 Feb 2026 18:59:11 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d875054debb3b00bfbede822155e39477650d9f4ae9e82a6b2718748862bc4`  
		Last Modified: Tue, 03 Feb 2026 18:59:11 GMT  
		Size: 163.9 KB (163938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05b6d59a83e6014b4a0aaa7e7fa29e73af49fed445d4b59f089ca428825bee0`  
		Last Modified: Tue, 03 Feb 2026 18:59:11 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a26c5c85d5b573c8604fcc4d2a9269325cc44acc80e0fcfb5a97b960f9d706`  
		Last Modified: Tue, 03 Feb 2026 18:59:12 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.11` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f7539c29b1d518df79ec531136d4f6892cf04a326f9ac2f0a8cbd7af8c198a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d05d33fee1c0e12d3f350120aa79842a4c6158dbad56f508e5c442da84e1413`

```dockerfile
```

-	Layers:
	-	`sha256:6c231ba8d7281286905ca5b5402e3a6743c1d80630341ff186295aa0cec53abf`  
		Last Modified: Tue, 03 Feb 2026 18:59:10 GMT  
		Size: 3.2 MB (3208966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5488395401510d669119157afe9956d2eea173493af00c14b7d3bb0245bd1712`  
		Last Modified: Tue, 03 Feb 2026 18:59:09 GMT  
		Size: 36.9 KB (36856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.11` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:dd49b5a732b92017a74230e61fdc5ca1816972f4549634895cfd705b69dfcd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570307462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21432819e10331531223f176015e8e1282f2b4da78cf87d88f0c839913d4817`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Tue, 03 Feb 2026 18:56:17 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 03 Feb 2026 18:56:17 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 03 Feb 2026 18:56:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 18:56:17 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 03 Feb 2026 18:57:01 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 03 Feb 2026 18:57:01 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 18:57:01 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:57:01 GMT
ENV SHELL=/bin/bash
# Tue, 03 Feb 2026 18:57:01 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Feb 2026 18:57:01 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 03 Feb 2026 18:57:01 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 03 Feb 2026 18:57:02 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 03 Feb 2026 18:57:02 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 03 Feb 2026 18:57:02 GMT
LABEL org.label-schema.build-date=2026-01-28T22:06:09.337243873Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c5253e1bcb0268a5dafed9dee18e16fd3144d7d6 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.11 org.opencontainers.image.created=2026-01-28T22:06:09.337243873Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c5253e1bcb0268a5dafed9dee18e16fd3144d7d6 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.11
# Tue, 03 Feb 2026 18:57:02 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 18:57:02 GMT
CMD ["eswrapper"]
# Tue, 03 Feb 2026 18:57:02 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5698ab10442e11f47845120f2c982834054cd170b5c4ff4d8b659193abebef85`  
		Last Modified: Tue, 03 Feb 2026 18:57:42 GMT  
		Size: 12.6 MB (12576947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c7fef2a6adc19818cddd6edc491b818558a2c36a634a998c8de06c3241050d`  
		Last Modified: Tue, 03 Feb 2026 18:57:41 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a143f069a71ed57531ba073db9a8a631dff3f021d27a597f3540f147e31e7ed`  
		Last Modified: Tue, 03 Feb 2026 18:57:52 GMT  
		Size: 528.6 MB (528576014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c924a86eccb7fd9e163b145129d902cad39835423eb43c7b449d330b57569f7e`  
		Last Modified: Tue, 03 Feb 2026 18:57:41 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a1c20d731d2086d5dac8376338709916a2ab73f2d105501475d58bfa7ff45f`  
		Last Modified: Tue, 03 Feb 2026 18:57:42 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b234684ac7d4c25febc60c7c12cbb7626591dba364f8b42eb5bafd90cd80051f`  
		Last Modified: Tue, 03 Feb 2026 18:57:42 GMT  
		Size: 160.4 KB (160361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965faaddc2dcbdbd94cbfa56bf077f4ca5210b999aa9e3cb44c6cfb2859e8099`  
		Last Modified: Tue, 03 Feb 2026 18:57:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcb54944e350c17a657d1198491b171c3ff1750f5660e78db688e52ea2e8bcc`  
		Last Modified: Tue, 03 Feb 2026 18:57:43 GMT  
		Size: 115.5 KB (115528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.11` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:80fa03e0681e0b13f6da8578204fbca87fb5855c7b386eec311f07bfaf427377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3814546f24217179da7b281bebbfd2cb88adb0841a8b66363cd501a6e87f42fd`

```dockerfile
```

-	Layers:
	-	`sha256:6806f9b765d481d199e574004e2cfb1092af7439273909b6c919a35cfe9d0088`  
		Last Modified: Tue, 03 Feb 2026 18:57:41 GMT  
		Size: 3.2 MB (3209379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7951c913e176774dc0f7585f547f5a72db2f7d051c9c4bc0228dddac7afb0fd`  
		Last Modified: Tue, 03 Feb 2026 18:57:41 GMT  
		Size: 37.1 KB (37059 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.10`

```console
$ docker pull elasticsearch@sha256:b36bb7288ac1f94a3f983b16fbc99e52b3170b37a4f52cb4c1bb87746cab29b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:ad75d6f8d098cfa93ab92976cc0837a60423d85c9006ff86096e3ea0e8fb6da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.6 MB (730648222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8986c40ee9d8471f5ea8aa0102089b9769bbaf67b95c68bbf82aecd68aaf19b6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:08:48 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:48 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 00:10:05 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:10:05 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:10:05 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 00:10:15 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 00:10:15 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 00:10:15 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:10:15 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 00:10:15 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:10:15 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 00:10:15 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 00:10:15 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Thu, 05 Feb 2026 00:10:15 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 00:10:15 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:10:15 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:10:15 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 00:10:15 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23034f21d08b650152940b6b72ddb10358f54c1f42f7623c919575aecf5b987`  
		Last Modified: Thu, 05 Feb 2026 00:11:06 GMT  
		Size: 4.3 MB (4287385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6992355c642e3731991af76b629124dd8b409d23ab6a1bde18b589867cbf56`  
		Last Modified: Thu, 05 Feb 2026 00:11:06 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5680343e35e980caca353ea41efbdcdd9924c14370e0c67093e0c04abccaa17e`  
		Last Modified: Thu, 05 Feb 2026 00:11:07 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d58875d89da1cf556fc599e023c296c626ac9d901384f88f742e72345cf6348`  
		Last Modified: Thu, 05 Feb 2026 00:11:20 GMT  
		Size: 686.3 MB (686261826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2de11c1f985bd755beeca66663a079224fc1ea092cf8451300830087c426d`  
		Last Modified: Thu, 05 Feb 2026 00:11:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7f242c0eda17443910c523cbb2151389631a8652a4898069f52cb24b87b15`  
		Last Modified: Thu, 05 Feb 2026 00:11:08 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87847955eff599282c2da408ae72fe24c8dde1949c7ac733be58ae83e9c040ec`  
		Last Modified: Thu, 05 Feb 2026 00:11:08 GMT  
		Size: 75.2 KB (75181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0d129fa0e6168eccda5867f4ddc58c1c8cd88fd0838ecac6015ad7943fcb76`  
		Last Modified: Thu, 05 Feb 2026 00:11:09 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f5910785a9fb60eb0f322bb4bed0bf2e7f347460b88a63820ac5f4e4add26e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143178e0f04650017cbf2deaa229953fe6e086f8617c8cabe6c29e84414a49fa`

```dockerfile
```

-	Layers:
	-	`sha256:492f6eb13cffd24f7784690dc131bf62660afc38d79099e21120341f082f4d02`  
		Last Modified: Thu, 05 Feb 2026 00:11:07 GMT  
		Size: 2.1 MB (2085752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98e3aa6ff161ed20beafe22c70ef864de222bffbbcd35ac89f1e5df5834fbfb`  
		Last Modified: Thu, 05 Feb 2026 00:11:06 GMT  
		Size: 33.9 KB (33867 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:063523b2fda465e062b797d24bf66abc05f655a8b97df5238b8f447ba00cbae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574602465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a19fb371517e2ca2354f2d5ed1c88d2e9bbf3138a51bb8a62661118b3effab`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:08:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:11 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 00:09:09 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:09:09 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:09:09 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 00:09:16 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 00:09:16 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 00:09:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:09:16 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 00:09:16 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:09:16 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 00:09:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 00:09:16 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Thu, 05 Feb 2026 00:09:16 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 00:09:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:09:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:09:16 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 00:09:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1089b965fdbaed0bb8eeefebd4251d508351efb26157e7a58a793e72547604a`  
		Last Modified: Thu, 05 Feb 2026 00:09:56 GMT  
		Size: 4.3 MB (4297940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa1dd9606edceb2d22e5bdd24d4fc88b0f4d0380b28c0919b28a9b60679ba32`  
		Last Modified: Thu, 05 Feb 2026 00:09:55 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b9e4aa81e08aa74930aed05e2ac15c62a99bab8bc70d464e1f3e26b6cb4da8`  
		Last Modified: Thu, 05 Feb 2026 00:09:55 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9250ddbbec510dd40b1266439651f1c57c01e661fd9518f4dbfd83a5afe566`  
		Last Modified: Thu, 05 Feb 2026 00:10:06 GMT  
		Size: 532.0 MB (532020350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20fb2a695af8663adeef9c763c85c28097a962e0659e280a66183a970fb1b1b`  
		Last Modified: Thu, 05 Feb 2026 00:09:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0d112c511415069a2cc363cec9439375fd39a0bb0c1ad3446b95c30d6983f4`  
		Last Modified: Thu, 05 Feb 2026 00:09:57 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24877fff7219736c77ae2bf387407b1b17cce8085034fb22441b433d64b6ac80`  
		Last Modified: Thu, 05 Feb 2026 00:09:57 GMT  
		Size: 74.1 KB (74106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c514906971995eca87b866d163fa9472607c564e32bd129196bafd0f0a95f`  
		Last Modified: Thu, 05 Feb 2026 00:09:58 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1003a80585c8979a89f8a7f2558730c7bc0551bfd9a57cd4a41c05ee563ba2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd133e9ab566acbd1aeb167f625f611f959b48a3feababfc0c9681552a3ba03`

```dockerfile
```

-	Layers:
	-	`sha256:dd2a02183bfd915f3916eb19ed922e431f13799ceb8db62eb9a5a5d0de9596fe`  
		Last Modified: Thu, 05 Feb 2026 00:09:55 GMT  
		Size: 2.1 MB (2086314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef9b9fcafd0bf57bacbce88eda236ab5a8a1d192763b401d0b86159816b5edd`  
		Last Modified: Thu, 05 Feb 2026 00:09:55 GMT  
		Size: 34.0 KB (34049 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.5`

```console
$ docker pull elasticsearch@sha256:af9c1b6004f5de8dc8733337201eb5b65a2a1fb778a66447ed214a1ff3edbf15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:79ef05ed2373da1b6fee102bd84715699a44ed5058a676d1f6a776f678899e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.2 MB (738201297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a85190da1349312851c20f09d7537ffde47bd0c5315af44ed545dde4cdfb65`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:08:46 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:46 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 00:10:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:10:01 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:10:01 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 00:10:11 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 00:10:11 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 00:10:11 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:10:11 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 00:10:11 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:10:11 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 00:10:11 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 00:10:11 GMT
LABEL org.label-schema.build-date=2026-01-28T22:05:53.857690766Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T22:05:53.857690766Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Thu, 05 Feb 2026 00:10:11 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 00:10:11 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:10:11 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:10:11 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 00:10:11 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31913d7e11f8b8d26984c878283ddb1e44f3114f7894e85c7b3ba167e8c9387`  
		Last Modified: Thu, 05 Feb 2026 00:11:04 GMT  
		Size: 4.3 MB (4287402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111d91b775a0e7862b31aece6af8efcd2239ab117956fe484d0124de881b3d81`  
		Last Modified: Thu, 05 Feb 2026 00:11:03 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5f4f9069d3c5b2bbd001ef8a38f27e0559f2d3a5f08e16d2e8fd0665987f2`  
		Last Modified: Thu, 05 Feb 2026 00:11:04 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19c1b224b7f54e8926c52697c1b00e55877041e245dee215012a79844b38bb3`  
		Last Modified: Thu, 05 Feb 2026 00:11:17 GMT  
		Size: 693.8 MB (693814875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc1f3037427b71e65d999e1f8491d21b19f031a6b607aa4d70ed025a2a6a49`  
		Last Modified: Thu, 05 Feb 2026 00:11:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3700e2b1781877cb8ea497468efb3d86d8ea4ac04df44b1e5f317cc86e799d37`  
		Last Modified: Thu, 05 Feb 2026 00:11:05 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae6b42a4d0caede0c3e373a17ac05a21a73ae582b7a44bdff692c6bb4e2374f`  
		Last Modified: Thu, 05 Feb 2026 00:11:06 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4d6c44be7ef60663930edd4689ab8df8b069eb0568a756a5ff8a079d72e6a`  
		Last Modified: Thu, 05 Feb 2026 00:11:06 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a9a6d9b91d0e56193fe6c3fb651c303fac0cf55117a6b018d6b9d3007e580328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a07bd451363e149adbd075113ce2803ee4d5e06c13d6a7275875f17513a5fe`

```dockerfile
```

-	Layers:
	-	`sha256:2aa587dfb1dfa667f7fbd98233f1a2d6f0fea45e649da3112d21c07a8c3af732`  
		Last Modified: Thu, 05 Feb 2026 00:11:04 GMT  
		Size: 2.1 MB (2098111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc914b8502ea72380e600eefddc3effbd6d3fbfa5ca332bdd4a27899e90b0ced`  
		Last Modified: Thu, 05 Feb 2026 00:11:04 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b973adeb181f591f37b4a3fb753cebd11f269e03f534303b98c07011fcde87cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.2 MB (582186329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57cb4687a5545d5de0735523889bd53ffb9d0f46cbb23335ef8e2d73a4978cc1`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:08:19 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:19 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 00:09:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:09:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:09:18 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 00:09:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 00:09:24 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 00:09:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:09:24 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 00:09:24 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:09:24 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 00:09:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 00:09:24 GMT
LABEL org.label-schema.build-date=2026-01-28T22:05:53.857690766Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T22:05:53.857690766Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Thu, 05 Feb 2026 00:09:24 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 00:09:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:09:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:09:25 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 00:09:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5effc05b2de7594a63db9bc3e884526822a4b04dc982654913cbe87a62cc8`  
		Last Modified: Thu, 05 Feb 2026 00:10:04 GMT  
		Size: 4.3 MB (4297883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaffe28daff28cf36463b5fc5003bc2467b478e9d6d0f0f1b2ad32af2a6fd1c6`  
		Last Modified: Thu, 05 Feb 2026 00:10:04 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0726f9f484afefb057fbefbee19663f8523433c8193f4b97f29842e116ba4514`  
		Last Modified: Thu, 05 Feb 2026 00:10:04 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ee0be29f081c8cd3265207be69b650e4439e34b3443a5e4fc06658d7916c65`  
		Last Modified: Thu, 05 Feb 2026 00:10:14 GMT  
		Size: 539.6 MB (539604279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e249775589c02f60a5f783192db4f4bbfe8fb301e1a1aa0b5d618d5c691c1a`  
		Last Modified: Thu, 05 Feb 2026 00:10:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5210412a1c2ffcbbd4d7e4a981cfe7cdb015b0c05f686f3a7755a7b52589cf1f`  
		Last Modified: Thu, 05 Feb 2026 00:10:05 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d852e0e95a5c01521e302e15116ec97b256748ab6396aeaa57248c04a1bc04`  
		Last Modified: Thu, 05 Feb 2026 00:10:05 GMT  
		Size: 74.1 KB (74107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56463b473129b7ea0f8650d4b4d68517e9d5ef215f0607b9fcb35b7107cbb699`  
		Last Modified: Thu, 05 Feb 2026 00:10:06 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4e14dd52335a16eef2db1842d97aee3b70129005318b25d3b776881405a5e2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4038a9de4f5be3c73876737008fb9cd792622dca011528fb0d9ef220b9d90a16`

```dockerfile
```

-	Layers:
	-	`sha256:c1176fc25de95af3d143525f72efa9ee379c0db89b49701dfc5c3c39f9a1dc1f`  
		Last Modified: Thu, 05 Feb 2026 00:10:04 GMT  
		Size: 2.1 MB (2098673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbeb5937016eff6aa8453141d95fa08eb8c3fd64f122ef09a443e38d7d0ab9c`  
		Last Modified: Thu, 05 Feb 2026 00:10:04 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.0`

```console
$ docker pull elasticsearch@sha256:3a41ebcbbc50f201bf9d49beaa7c4d02e833bae9c014a669c6fe3b3579103d94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:7d3751ebc4d889f20435c6fb4fab22f16755bfe07f77ec2c406fbfc2d594bb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.3 MB (716342148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386c0322cf8b53c020dd810a28f3386ee521049f7f2d31dc23395a026f394879`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:08:53 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:53 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 00:10:06 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:10:06 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:10:06 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 00:10:15 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 00:10:15 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 00:10:15 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:10:15 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 00:10:16 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:10:16 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 00:10:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 00:10:16 GMT
LABEL org.label-schema.build-date=2026-01-29T10:05:46.708397977Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=17b451d8979a29e31935fe1eb901310350b30e62 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T10:05:46.708397977Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=17b451d8979a29e31935fe1eb901310350b30e62 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Thu, 05 Feb 2026 00:10:16 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 00:10:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:10:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:10:16 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 00:10:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173275bba411d62dbbb15a9ea5e660a2062d842fc7f4ae3a9ce170cdbcff1f62`  
		Last Modified: Thu, 05 Feb 2026 00:11:09 GMT  
		Size: 4.3 MB (4287402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8992b94accf07b2beae26cd57f708f95c5bced1aef7bc53789b0490c23f0e7d8`  
		Last Modified: Thu, 05 Feb 2026 00:11:09 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ccaf3aab751d6ba8d423f199834a6fc66f63c0d5cd4484f7ea95d504090ce`  
		Last Modified: Thu, 05 Feb 2026 00:11:08 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892921087a0293b2c8a2895c88e8fa645b98f91c82b838bd6fe8da74b8bd6dfa`  
		Last Modified: Thu, 05 Feb 2026 00:11:20 GMT  
		Size: 672.0 MB (671955731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a7e7458778aa946edc201a126219e7a7e3f043327b002952f3949d7277085d`  
		Last Modified: Thu, 05 Feb 2026 00:11:10 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f26259d8c8d548a931f20a2c1c53efecc465d0eac38df9a67132333e3530c31`  
		Last Modified: Thu, 05 Feb 2026 00:11:10 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661b5871664d52c7cb0790288cd513fa4f711130d8f60d98814e60627417693d`  
		Last Modified: Thu, 05 Feb 2026 00:11:10 GMT  
		Size: 75.2 KB (75180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86414f2e035b569d6e479b27b6a2a028fa914de2a850b5e653220c7e0f632d4`  
		Last Modified: Thu, 05 Feb 2026 00:11:11 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0d1ec84803660c06b2221db882a718494f15eab2bb4ea3cb29a0c03efe782bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726094c67a642d8249cf964ec51d5c9d6271519d4a942ade0f5a389d56bf7d62`

```dockerfile
```

-	Layers:
	-	`sha256:62abd9f62e8489f182af7389a1e63c7209d543b17eb01de5b3932e47ade44b39`  
		Last Modified: Thu, 05 Feb 2026 00:11:09 GMT  
		Size: 2.1 MB (2089751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4e3b0d96b202dd59e25063dcff1026c3d507be325775b4142d69787767e28d`  
		Last Modified: Thu, 05 Feb 2026 00:11:08 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:9b522dda6c97b839451fd0696ab9b0b9588e19d854461bed95e39fe8231fc94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.3 MB (560325278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63627259329c5d9b9c8fb7e13ffd0ed20cf5ba0279f77a978385eb1d3d5463ad`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:08:24 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:24 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 00:09:17 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:09:17 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:09:17 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 00:09:23 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 00:09:24 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 00:09:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:09:24 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 00:09:24 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:09:24 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 00:09:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 00:09:24 GMT
LABEL org.label-schema.build-date=2026-01-29T10:05:46.708397977Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=17b451d8979a29e31935fe1eb901310350b30e62 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T10:05:46.708397977Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=17b451d8979a29e31935fe1eb901310350b30e62 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Thu, 05 Feb 2026 00:09:24 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 00:09:24 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:09:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:09:24 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 00:09:24 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44285d1421b78b2251c91716f16f0043a3d3250a378807e444a0eb0587f25e3c`  
		Last Modified: Thu, 05 Feb 2026 00:10:03 GMT  
		Size: 4.3 MB (4297896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7b61a773a7eba009f075bd48dab19c2bcd381f9d1e377ed70ab6d5d43d9421`  
		Last Modified: Thu, 05 Feb 2026 00:10:02 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead057b4f8ae48b1774d8c9395aeb295ab40a35baaf955bc8fa989fdf5d2b43d`  
		Last Modified: Thu, 05 Feb 2026 00:10:02 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac119e855522e0dfe2f02d9a5b55212f71e987f51811e53fb30883f93be829ce`  
		Last Modified: Thu, 05 Feb 2026 00:10:13 GMT  
		Size: 517.7 MB (517743211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459665073cf5662cd514d37c92bd49e62d8a89994613677659e002abc8d2b9ff`  
		Last Modified: Thu, 05 Feb 2026 00:10:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2713b1c738fcf642f063daf49bf959f72177056dc1b996c6ed0324afd0dfc160`  
		Last Modified: Thu, 05 Feb 2026 00:10:04 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b9959809752790a86a5db8dc6ca98f8780a2942e8384d803c09447a900993a`  
		Last Modified: Thu, 05 Feb 2026 00:10:04 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f611827138eea9a3cf56b346b307dce9a6bafc7c10e0ba23bc9fabf33f9423a8`  
		Last Modified: Thu, 05 Feb 2026 00:10:05 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:fb2bc18ef7e2f0048a34d37f30544c109a745f84b2433c66407d44d03da87605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f958e85cd4645a1bfb78c6c281520aa6c8595be7816611335b5beb26328aa52`

```dockerfile
```

-	Layers:
	-	`sha256:967f0ebf3838250ef35f304565d36c87c9d124236731aa37e112d53b196a8a06`  
		Last Modified: Thu, 05 Feb 2026 00:10:03 GMT  
		Size: 2.1 MB (2090313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd96e150aa259efc6a904d6ffff20fba143e3281a8a7976a9715f4566b1492e`  
		Last Modified: Thu, 05 Feb 2026 00:10:02 GMT  
		Size: 34.0 KB (34036 bytes)  
		MIME: application/vnd.in-toto+json
