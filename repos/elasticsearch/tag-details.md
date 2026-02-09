<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.11`](#elasticsearch81911)
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

## `elasticsearch:9.2.5`

```console
$ docker pull elasticsearch@sha256:6bdc289517e3a7cdaa5fbc8ebed8b21918d00e1be889035ab938d655e8a1ab28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:68f548696bdb454737994c05fccc1f16b9e35983cb5a829438a24e45aa8af0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.2 MB (738242198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a05198b73a559a63ef9e0e4329ab058f7d1843a05cb32587460d72564b4a81`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:49:59 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:50:00 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 19:50:42 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:50:42 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:50:42 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 19:50:52 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 19:50:52 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 19:50:52 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:52 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 19:50:52 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 19:50:52 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 19:50:52 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 19:50:52 GMT
LABEL org.label-schema.build-date=2026-01-28T22:05:53.857690766Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T22:05:53.857690766Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Thu, 05 Feb 2026 19:50:52 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 19:50:53 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:50:53 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 19:50:53 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 19:50:53 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e3fd0605721cc834c25c400199639eefdef007e757342b78f492c3e6b2f967`  
		Last Modified: Thu, 05 Feb 2026 19:51:44 GMT  
		Size: 4.3 MB (4281758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fa403e13183f1da5c201274bebf69f24736b37f04fdb6816cf301605ad466c`  
		Last Modified: Thu, 05 Feb 2026 19:51:43 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a42fafc332a3ecb431f54953aae3080fdc8fceef8adf706fc82db50e72a785a`  
		Last Modified: Thu, 05 Feb 2026 19:51:43 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f25888798e07740335d8d1743de62e29959a0491de374e3d3a74c2a426715e0`  
		Last Modified: Thu, 05 Feb 2026 19:52:00 GMT  
		Size: 693.8 MB (693814600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cab4355c2b20a5ca97d5ed9ee5f3301842d113cf38ee5ead789b0bbfc70abd`  
		Last Modified: Thu, 05 Feb 2026 19:51:44 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e669d97eb39575dd6823314de7e328a8d4fa5eb8e67a6fc5f1179023ed28be2`  
		Last Modified: Thu, 05 Feb 2026 19:51:45 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9107bb0d72940472be850ec0edc111134024281b98076ab38cfabeb977f2cb19`  
		Last Modified: Thu, 05 Feb 2026 19:51:45 GMT  
		Size: 75.2 KB (75179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4a7dee25afc6c81fb121eaeaf15df958f08b875f2a6be3d7ccff3c1970ada9`  
		Last Modified: Thu, 05 Feb 2026 19:51:46 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f2c8c7467b452a7ba73d01628554cbb03999c50d0e2e94d92129272769b89575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af525f4ce19474305ea2553bdb416bef7ad876f35c549d3378235cfa2be788`

```dockerfile
```

-	Layers:
	-	`sha256:4cd21ba2058c3c381bf2b25cfaa0c512de42bc2883f4eb6f808d7aaa36088fcd`  
		Last Modified: Thu, 05 Feb 2026 19:51:44 GMT  
		Size: 2.1 MB (2098131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c78aa9901e058ac5896138eb2c17d8388123c0349f70b33e253784e46ed375d`  
		Last Modified: Thu, 05 Feb 2026 19:51:43 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:1c83d2ab53c3fef545fcc7aac4f35d99b37e529c19c62d0d12c13925d7c99995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.2 MB (582199977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf866db2c4f447e51830e759887164354a7bfe1ac408b4efcfdad408ef404d8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:49:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:49:12 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 19:49:59 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:49:59 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:49:59 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 19:50:05 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 19:50:06 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 19:50:06 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:50:06 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 19:50:06 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 19:50:06 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 19:50:06 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 19:50:06 GMT
LABEL org.label-schema.build-date=2026-01-28T22:05:53.857690766Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T22:05:53.857690766Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Thu, 05 Feb 2026 19:50:06 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 19:50:06 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:50:06 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 19:50:06 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 19:50:06 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43faee406c85096aa4a31d013226ecf86afb48437f059460f3a0ae2c453ded3a`  
		Last Modified: Thu, 05 Feb 2026 19:50:45 GMT  
		Size: 4.3 MB (4291354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f6e875b92a2ee6d3517530cd4de1f159eae49dbb624681bfea9b2a9363f558`  
		Last Modified: Thu, 05 Feb 2026 19:50:45 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0c198af70534e2cf1c83f3304d9e1a6f7fae3da4c5913b5713000f6af588a6`  
		Last Modified: Thu, 05 Feb 2026 19:50:45 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e958262320b6a5a335a0e631f6683b64da0f73fdf933292099f8efd75749e`  
		Last Modified: Thu, 05 Feb 2026 19:50:56 GMT  
		Size: 539.6 MB (539604365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64b5992657206aee0450227d701c27de9820d5db55ed1989c880bd602046ffc`  
		Last Modified: Thu, 05 Feb 2026 19:50:46 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c366e0909416accdf2316a19efcc7aff1582453b44b371f193ba490e3abf85cc`  
		Last Modified: Thu, 05 Feb 2026 19:50:47 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807c40db7813e0880c352f3cb3224cfe1637fd370ab4984fd76e6e10b583553b`  
		Last Modified: Thu, 05 Feb 2026 19:50:47 GMT  
		Size: 74.1 KB (74104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2872c288764087575f1f2632279eb9ac85a4d1fef64e1b222b8d43dad7e52a`  
		Last Modified: Thu, 05 Feb 2026 19:50:48 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e5bb4a542aa2dd7312cd6d40850e655829fdcc0b858a0b2d0c5ce6cb3d0a9d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e01cd87d1d1c5f39e325667f147bd761aa91ab33b1c37b3876ed6a4bca89c2`

```dockerfile
```

-	Layers:
	-	`sha256:b7d6fe2e53e861165ab7d2fdfdd893c23f8b1114d19aaf857396580c4a5aa472`  
		Last Modified: Thu, 05 Feb 2026 19:50:45 GMT  
		Size: 2.1 MB (2098693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcf8de2f95218d8a52346d835b1e9133f626dd518753a9279655e10b69773ea`  
		Last Modified: Thu, 05 Feb 2026 19:50:45 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.0`

```console
$ docker pull elasticsearch@sha256:89738cb1d6042ac20eddc3768eb3bb7e92bdf816a83a261b3bf11fb3544ae751
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:68dd1986d87f5007f4e11028dee69e3d7cff63022d1e9b1b26c55caf4bce39c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.4 MB (716383320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089e6c84f357d9921b0879a96bf130474e960704caaa1f9f895fef1033ef50ff`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:50:06 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:50:06 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 19:51:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:51:15 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:51:15 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 19:51:25 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 19:51:25 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 19:51:25 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:51:25 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 19:51:25 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 19:51:25 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 19:51:25 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 19:51:25 GMT
LABEL org.label-schema.build-date=2026-01-29T10:05:46.708397977Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=17b451d8979a29e31935fe1eb901310350b30e62 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T10:05:46.708397977Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=17b451d8979a29e31935fe1eb901310350b30e62 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Thu, 05 Feb 2026 19:51:25 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 19:51:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:51:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 19:51:25 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 19:51:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d450354643b16fb8a514786b728681b81afb4395b143ebd474a89f4f1a9e441b`  
		Last Modified: Thu, 05 Feb 2026 19:52:17 GMT  
		Size: 4.3 MB (4281746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35dbec60257ac1abe229444dabd5f3a67a4c4335b3b93ac1e3ff1ba5999f764`  
		Last Modified: Thu, 05 Feb 2026 19:52:17 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc706e4512c02c8528a136699f845d381817a0b73f6c36fac36fa921cf75b927`  
		Last Modified: Thu, 05 Feb 2026 19:52:17 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdd5303de1d653477e053c140682af9a858b52b7e55e0ebe747c2706c396aa2`  
		Last Modified: Thu, 05 Feb 2026 19:52:32 GMT  
		Size: 672.0 MB (671955733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bccbaf44e286bd1717d16530e90bfd65399d050fbb3ddf86998e89d431b9a3`  
		Last Modified: Thu, 05 Feb 2026 19:52:18 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c40e321eb3aa27af16339b19ca1d04526a8e7cba0923016e0431c7bd64395a0`  
		Last Modified: Thu, 05 Feb 2026 19:52:18 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d864befd18684bd0a4ee2506667f645b728735ad15ecfda51257bfa75bc433`  
		Last Modified: Thu, 05 Feb 2026 19:52:19 GMT  
		Size: 75.2 KB (75180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8186102c1a5b38b7638ca71a5088f01000274ec5fab748d3025555cf73aefe86`  
		Last Modified: Thu, 05 Feb 2026 19:52:19 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ce6ecbdccdeb1d49df82ee33aae6083c525d4d996cdd1cc47886abcee4fd2fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf930e0e2abfdc93c0a5ea783eed45829b45be0288cf6758f00dd03075f6ede`

```dockerfile
```

-	Layers:
	-	`sha256:bb279f4e9dae2c4af62d1ec2c3eae21b23361826eeb02ca3f8199ef7cc6af331`  
		Last Modified: Thu, 05 Feb 2026 19:52:17 GMT  
		Size: 2.1 MB (2089771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3adf039b43a0b3ed72be65d752c8c3259c9839b486472db967f6692c190a092b`  
		Last Modified: Thu, 05 Feb 2026 19:52:17 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:0cd4c26c0185b4dcfb21fdf96e9d723c37a5d2711304bf66c8085eb7a6542047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.3 MB (560338539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c012c0f274f6178675b399a1e7537d49e3a1df418f589c4939ea3d742355a4`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:48:45 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:48:46 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Feb 2026 19:49:37 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:49:37 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:49:37 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Feb 2026 19:49:43 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 05 Feb 2026 19:49:43 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 05 Feb 2026 19:49:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:49:43 GMT
ENV SHELL=/bin/bash
# Thu, 05 Feb 2026 19:49:43 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 19:49:43 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Feb 2026 19:49:43 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Feb 2026 19:49:43 GMT
LABEL org.label-schema.build-date=2026-01-29T10:05:46.708397977Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=17b451d8979a29e31935fe1eb901310350b30e62 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T10:05:46.708397977Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=17b451d8979a29e31935fe1eb901310350b30e62 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Thu, 05 Feb 2026 19:49:43 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 05 Feb 2026 19:49:43 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:49:43 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 19:49:43 GMT
CMD ["eswrapper"]
# Thu, 05 Feb 2026 19:49:43 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6feaafb3e33a33db11ffd97a8f9e4bb816d9498abdcafa7f58a6e3ddcdd28`  
		Last Modified: Thu, 05 Feb 2026 19:50:21 GMT  
		Size: 4.3 MB (4291268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474439cec5c1d4829f5b7195e40fde2d7b9ef54ba00db6e7ecf9d9d4248149a1`  
		Last Modified: Thu, 05 Feb 2026 19:50:21 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67cca018b4987eaeafca08a974540afff5143adeb16730f00b99147e449accc`  
		Last Modified: Thu, 05 Feb 2026 19:50:21 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4375c74cf962405e9f90003885e51b4275541fd4806564ee45de0313a92e7286`  
		Last Modified: Thu, 05 Feb 2026 19:50:31 GMT  
		Size: 517.7 MB (517743009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a080cbe7d9f4e89867a80e585803e98d403be524ee05ce64f79f22c911f62272`  
		Last Modified: Thu, 05 Feb 2026 19:50:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d1d6f6b9380806bec8ca2f0854236993332bd76ca7b8c329c8cfc400420870`  
		Last Modified: Thu, 05 Feb 2026 19:50:23 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0331c5d382064ae92e45a8717307221a99cbd9f40f007da5b6a43b24e834a055`  
		Last Modified: Thu, 05 Feb 2026 19:50:23 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87edb849579b713e9c6cc81a8124796e460e1cbc6b1d8351a09f1d2cd84ad20e`  
		Last Modified: Thu, 05 Feb 2026 19:50:24 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1826f29223c9ae56b04162e54ab32f5c3577b66800147f2a03416b510f528a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3374975579d82d07561a6d7ee3c14754a9943ad88bbc27885f5c72d8dc6e6ed1`

```dockerfile
```

-	Layers:
	-	`sha256:a39d83068eabc9bf1435400c1f23a12725f5843ad697939121b690c81636a24f`  
		Last Modified: Thu, 05 Feb 2026 19:50:22 GMT  
		Size: 2.1 MB (2090333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d0e141a62549493d52ea48464821e5869be2f18b76a42d301ac585d0384db9`  
		Last Modified: Thu, 05 Feb 2026 19:50:21 GMT  
		Size: 34.0 KB (34036 bytes)  
		MIME: application/vnd.in-toto+json
