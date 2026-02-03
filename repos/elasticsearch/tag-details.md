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
$ docker pull elasticsearch@sha256:c1fd1b6a09000283ecdf036113c77bcff64c40c34772d23d04a0a125527ce5ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:5a603b560c539b8930a78cb1a93446ec005661dc3ee881e17cd65c73f9a9118c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.6 MB (730643051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4623e8207579cba6d8b40ec93d03c5220e0b12f0e40400f6f5b8d27398206d39`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Mon, 26 Jan 2026 22:05:29 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:05:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 26 Jan 2026 22:06:54 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:06:54 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:06:54 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 26 Jan 2026 22:07:04 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:04 GMT
ENV SHELL=/bin/bash
# Mon, 26 Jan 2026 22:07:04 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 26 Jan 2026 22:07:04 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Mon, 26 Jan 2026 22:07:04 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 26 Jan 2026 22:07:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:07:04 GMT
CMD ["eswrapper"]
# Mon, 26 Jan 2026 22:07:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21efb3ee2d6e5b6a6f847b91b53d0720e20ec04a32edf5e3f2afe6cd6c3962f2`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 4.3 MB (4286292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309687df99ca8a16d2eb6713e5e524d6be56a817e9d4e62a0eb6e198fbcf8d5`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 1.5 KB (1533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc8395d188d85a869d09c3b38732e3076ea72628ab627aabdecfcffd8c7cf2b`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9abaed0152751cd0fd394a766ea16c2acbd495dbc670724183763fb1b4b989`  
		Last Modified: Mon, 26 Jan 2026 22:08:09 GMT  
		Size: 686.3 MB (686261779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dbbf014bebb14d21319b980356fecd96c1557d8d9a5b9dcea79e8db5c3b735`  
		Last Modified: Mon, 26 Jan 2026 22:07:58 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0558f50c4fd45cd06bbb4836375a832f317ef0bcfa9d721a1b1a7982c3d54dfd`  
		Last Modified: Mon, 26 Jan 2026 22:07:58 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b487f353f99170ce8e2d0d23edefb6990361f1e5c2530ab982f45e1b8709cd`  
		Last Modified: Mon, 26 Jan 2026 22:07:58 GMT  
		Size: 75.2 KB (75180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e76aa407a5de5aacad7cdf902d36e4a42e83af6679fd7631c6aedf87e12190`  
		Last Modified: Mon, 26 Jan 2026 22:07:59 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6515cd966003bbf78302450b2ec1b2c35e832e076cee1ccf6f6a3e23ad6d591c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75343c5d77ab3a87b7e58a1e74213f163a6ca7bf88bdf1d4c6d3154af142f180`

```dockerfile
```

-	Layers:
	-	`sha256:f628c1425b8d92cad255acfe9ce6a184ccf0eefd0b562ee3a55bb6766ca07ae4`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 2.1 MB (2085728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42da45dd5023e71fb7f29ff10b1569acf74da7669c826a7d01700c7cf4cd9f93`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 33.9 KB (33867 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:362331d217721a8301fe41239a3ed2349ca90eaad69879a52fa63d7f69edd442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574629943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e543e94a502d9faffd908acd4fa4f1afb206f35e06cec0ce3ec41059e027185d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Mon, 26 Jan 2026 22:05:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:05:27 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 26 Jan 2026 22:06:22 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:06:22 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:06:22 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 26 Jan 2026 22:06:28 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 26 Jan 2026 22:06:28 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 26 Jan 2026 22:06:28 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:06:28 GMT
ENV SHELL=/bin/bash
# Mon, 26 Jan 2026 22:06:28 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:06:28 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 26 Jan 2026 22:06:28 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 26 Jan 2026 22:06:28 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Mon, 26 Jan 2026 22:06:28 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 26 Jan 2026 22:06:29 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:06:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:06:29 GMT
CMD ["eswrapper"]
# Mon, 26 Jan 2026 22:06:29 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fede9481ad2d2a5daa610d3a860308b3b04fd5caf79669738d934facb1e1ea80`  
		Last Modified: Mon, 26 Jan 2026 22:07:07 GMT  
		Size: 4.3 MB (4297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9ff6a49150a7a19feb4325a929fbc437bcc07f08104303a65dda49145ed59b`  
		Last Modified: Mon, 26 Jan 2026 22:07:07 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc57f21a3870c175c73e605cab60c338a56b7bbe63d7f0d4cca6816e8909cce`  
		Last Modified: Mon, 26 Jan 2026 22:07:07 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463893edc47350d18a0d6ae2732d0625a2e63cbe39282440ac1740e21f2ac9e`  
		Last Modified: Mon, 26 Jan 2026 22:07:17 GMT  
		Size: 532.0 MB (532020336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d4643b1cd331424d5a050620eb07118fd4b22931af8dab28de9f7c6b9e9f49`  
		Last Modified: Mon, 26 Jan 2026 22:07:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d812254818aa2f494ce706b8d618298f3f674335b5213866463cb5d2b65e582f`  
		Last Modified: Mon, 26 Jan 2026 22:07:08 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a284f6ab5c54d7cd3035bc42a0d0757ddc751bfe2e57fac6d1db3816504f391a`  
		Last Modified: Mon, 26 Jan 2026 22:07:08 GMT  
		Size: 74.1 KB (74105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c1527291a7227ad3c0e38fd380c47f57394d970d7598e7b9f50a84efec6dcc`  
		Last Modified: Mon, 26 Jan 2026 22:07:09 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:091165220e12fa6c314f59dd306c7be4bda6bc3826c0dfe349a9bc8f1f45ca2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d706a097e4c547633df13622e6fe20a111f0a71d8d0651420a50d2288a690a45`

```dockerfile
```

-	Layers:
	-	`sha256:a0643e052a5145169bb6078d245514febd8593d0eba5dbb4b7f3749306a1e68a`  
		Last Modified: Mon, 26 Jan 2026 22:07:07 GMT  
		Size: 2.1 MB (2086290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6601eb7421be145a20cb4b4fa58cab6e154884483f4a5f70188b8c22b0125785`  
		Last Modified: Mon, 26 Jan 2026 22:07:06 GMT  
		Size: 34.0 KB (34049 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.5`

```console
$ docker pull elasticsearch@sha256:d4d0b293668c88f100eba98f1e86bbc6fe3faed55c2828f674dea1cbcbab07e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f0f892f7777bd23b5c14aa72564e03df5e927e60bd370a715f367e165dd9af4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.2 MB (738195855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f106704de6c62f2e30cf1a06558016b93a9c03c6c20e7e8c3f40cd12c3aa96d9`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Tue, 03 Feb 2026 18:57:46 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 03 Feb 2026 18:57:47 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 03 Feb 2026 18:59:03 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 18:59:03 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 18:59:03 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 03 Feb 2026 18:59:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:59:13 GMT
ENV SHELL=/bin/bash
# Tue, 03 Feb 2026 18:59:13 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 03 Feb 2026 18:59:13 GMT
LABEL org.label-schema.build-date=2026-01-28T22:05:53.857690766Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T22:05:53.857690766Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Tue, 03 Feb 2026 18:59:13 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 03 Feb 2026 18:59:13 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 18:59:13 GMT
CMD ["eswrapper"]
# Tue, 03 Feb 2026 18:59:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8169483b3206ada475abb7c51757bee55eb64cfd1efc08f82cb24339425a20dd`  
		Last Modified: Tue, 03 Feb 2026 19:00:09 GMT  
		Size: 4.3 MB (4286267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a11cf00da740a0022c56061d03378b035f467bcce1125a2557fd1c3f570a37`  
		Last Modified: Tue, 03 Feb 2026 19:00:09 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b03d01c7b1ff6f365f058df1ea461ce27aee13a36fb034cdaa2563a91c49e1`  
		Last Modified: Tue, 03 Feb 2026 19:00:09 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bba2bfb3ef5f7a291587a07ad479c5a82c099aaa1d6b1e7af908348f22432fe`  
		Last Modified: Tue, 03 Feb 2026 19:00:26 GMT  
		Size: 693.8 MB (693814616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17ddb719b83b332007dd17a3840919e48bcc756e983fa1ee741e608ff90c8c6`  
		Last Modified: Tue, 03 Feb 2026 19:00:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e88fa7a019e23c9c91061b72dfda5869f265a9b0b5ac8e544d0483ef9cdee7d`  
		Last Modified: Tue, 03 Feb 2026 19:00:11 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9781dda4437fdc5e344267c805a60bea1b11234d7fee5b8919a29ee33ee0f205`  
		Last Modified: Tue, 03 Feb 2026 19:00:11 GMT  
		Size: 75.2 KB (75178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00daed21886a1e1ee099ca25893a7be91e865b94e1df7db61df740eb78d67273`  
		Last Modified: Tue, 03 Feb 2026 19:00:13 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a196f033e80550676a3321a8c8da1de97d8642eef1208c8d20196c8dffe3c243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020e4222f58a0efdfe92d673addd2e5c570d99d3481fabc80a3e0512f2cb9018`

```dockerfile
```

-	Layers:
	-	`sha256:e779193bd2b91299cae64cd4c4a903174aefc26d133f6290c9d9cfb621edbf58`  
		Last Modified: Tue, 03 Feb 2026 19:00:09 GMT  
		Size: 2.1 MB (2098087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09cd4cd4e09515d09e91730f26fa55fccdfd180e40025fc9e768f635d31615f`  
		Last Modified: Tue, 03 Feb 2026 19:00:10 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:4cc1c28a02f7ca325225759f4379c9b800e12c0e969b09619992cf4923b860ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.2 MB (582213997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38dafc80e6cde3ed44eec9d26f48053d47e929a24118dc783535e5c6e0ea30f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Tue, 03 Feb 2026 18:56:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 03 Feb 2026 18:56:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 03 Feb 2026 18:56:46 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 18:56:46 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 18:56:46 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 03 Feb 2026 18:56:52 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 03 Feb 2026 18:56:52 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 03 Feb 2026 18:56:52 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:56:52 GMT
ENV SHELL=/bin/bash
# Tue, 03 Feb 2026 18:56:52 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Feb 2026 18:56:53 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 03 Feb 2026 18:56:53 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 03 Feb 2026 18:56:53 GMT
LABEL org.label-schema.build-date=2026-01-28T22:05:53.857690766Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T22:05:53.857690766Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Tue, 03 Feb 2026 18:56:53 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 03 Feb 2026 18:56:53 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 03 Feb 2026 18:56:53 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 18:56:53 GMT
CMD ["eswrapper"]
# Tue, 03 Feb 2026 18:56:53 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9f04b3d5a77d94a61014844382160cb828bd21832d318f9c2ad7ec5c8f90b5`  
		Last Modified: Tue, 03 Feb 2026 18:57:31 GMT  
		Size: 4.3 MB (4297540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46991455029432b560728d7021100d6732b85b561b7a917d50c07dbfdc42803b`  
		Last Modified: Tue, 03 Feb 2026 18:57:31 GMT  
		Size: 1.5 KB (1537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a098630d0c0ed9032187e792857fe4f3529328c6bdbfe1c6e9165734c9405736`  
		Last Modified: Tue, 03 Feb 2026 18:57:31 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55d137cb2b02c224c82ecb725fbe37df1355c98da7a4c367c60fa778111b358`  
		Last Modified: Tue, 03 Feb 2026 18:57:41 GMT  
		Size: 539.6 MB (539604365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585595d2787cefc02c42a50bf788318211dd778c17d59f7fdd6ee5177dd7c322`  
		Last Modified: Tue, 03 Feb 2026 18:57:32 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7658a8d238b54a9959b8bce711e419e32c9aafb62721804a7c65f80ad313ec06`  
		Last Modified: Tue, 03 Feb 2026 18:57:32 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eef00b58b0511fb58f4a6b9b20e2d1aa9ac1a17d6439e34dfb3c77bc5af01c`  
		Last Modified: Tue, 03 Feb 2026 18:57:33 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8514fbc791f1cc0f582f936448c453f44718ebf2456cc61d3ba03e7a7e77aed2`  
		Last Modified: Tue, 03 Feb 2026 18:57:33 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:20ded05e4f5bae644b8520059a93334c95ee5f8cb69a95a83d569c74cb0cc3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0e96d577f0dcf590a11783d8bcc320bc3c0cdb7cf868f805b8f7d06dfce917`

```dockerfile
```

-	Layers:
	-	`sha256:dca536870c194049d986cec07aefe309be5be683f6b49b16e10bf2c3436d04cc`  
		Last Modified: Tue, 03 Feb 2026 18:57:31 GMT  
		Size: 2.1 MB (2098649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfccacfbd6f7c42b83dc9e60f9dbb24bb80f8f39a929803d3170c60e6879c5ef`  
		Last Modified: Tue, 03 Feb 2026 18:57:31 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.0`

```console
$ docker pull elasticsearch@sha256:76045cd5895cb8b4655048c018eb23af6c4d1f2642659a4c3ee18b3bf984e07a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:a9a14dbb037de5c582ceed9e4140d3c6767e23e5d2070a3cd7275e3d6183740c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.3 MB (716336982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5227f0b78211af74a60161ed39a2a9552aa68007c9d76a1fe7e06ba17987785`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Tue, 03 Feb 2026 18:57:49 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 03 Feb 2026 18:57:49 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 03 Feb 2026 18:59:03 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 18:59:03 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 18:59:03 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 03 Feb 2026 18:59:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:59:13 GMT
ENV SHELL=/bin/bash
# Tue, 03 Feb 2026 18:59:13 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 03 Feb 2026 18:59:13 GMT
LABEL org.label-schema.build-date=2026-01-29T10:05:46.708397977Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=17b451d8979a29e31935fe1eb901310350b30e62 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T10:05:46.708397977Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=17b451d8979a29e31935fe1eb901310350b30e62 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Tue, 03 Feb 2026 18:59:13 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 03 Feb 2026 18:59:13 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 03 Feb 2026 18:59:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 18:59:13 GMT
CMD ["eswrapper"]
# Tue, 03 Feb 2026 18:59:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1c3fe0f6cf81d884423853d26865a3e2bad992a7034fa03530b07f65ceca08`  
		Last Modified: Tue, 03 Feb 2026 19:00:08 GMT  
		Size: 4.3 MB (4286308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb79cdb219b6083b34bcde48636e88e017dd63f498fd2e5a56995f010c680082`  
		Last Modified: Tue, 03 Feb 2026 19:00:11 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d2fb7ffa1ff78878329ea76bc34be5b539cfe5a877c2a787b868f55db5b88e`  
		Last Modified: Tue, 03 Feb 2026 19:00:09 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190539ae40593ef4b801ced8264513336488f302ec55c36e3268388188c1e1bb`  
		Last Modified: Tue, 03 Feb 2026 19:00:22 GMT  
		Size: 672.0 MB (671955702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6778bd9e9db0eb2baca1b29b8b72e46580a2bebaf0d4011505509785434abe`  
		Last Modified: Tue, 03 Feb 2026 19:00:11 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54affbe3a54afcdf970b258821f3a750dce1f834bf398cf464f4104149f9d6`  
		Last Modified: Tue, 03 Feb 2026 19:00:12 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1613888dc0c48d413e6b98e0f3433f7e6381144ab7034123042b59d1ac48aed2`  
		Last Modified: Tue, 03 Feb 2026 19:00:13 GMT  
		Size: 75.2 KB (75177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00daed21886a1e1ee099ca25893a7be91e865b94e1df7db61df740eb78d67273`  
		Last Modified: Tue, 03 Feb 2026 19:00:13 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e55bb667d649ffb0ad8912e620f687c7cf366c17379d4aaaf66bf22fd713b280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f860a252231afc087c32154192e2dc693fb7053bfffc00311367fd5a82661ce5`

```dockerfile
```

-	Layers:
	-	`sha256:9b41489cdc5177af68ba5b3594db6a1e61ceb42142dcb5a6590d8b042e35cacc`  
		Last Modified: Tue, 03 Feb 2026 19:00:08 GMT  
		Size: 2.1 MB (2089727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d7c27be4058e1419ad303ccaac65c66639b9ea1c11b5b6272388f0acd66cc0`  
		Last Modified: Tue, 03 Feb 2026 19:00:08 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:4d042f3319093a39546de8ce83efd9583fbd1913ba4e6a0f39afa51cf8991d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.4 MB (560352595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80495630608cae3a72ab1f9b894b9aabfce9b36db741ff4b1880a9c8ae33d3ab`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Tue, 03 Feb 2026 18:56:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 03 Feb 2026 18:56:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 03 Feb 2026 18:56:46 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 18:56:46 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 18:56:46 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 03 Feb 2026 18:58:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 03 Feb 2026 18:58:26 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 03 Feb 2026 18:58:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 18:58:26 GMT
ENV SHELL=/bin/bash
# Tue, 03 Feb 2026 18:58:26 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Feb 2026 18:58:26 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 03 Feb 2026 18:58:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 03 Feb 2026 18:58:26 GMT
LABEL org.label-schema.build-date=2026-01-29T10:05:46.708397977Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=17b451d8979a29e31935fe1eb901310350b30e62 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T10:05:46.708397977Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=17b451d8979a29e31935fe1eb901310350b30e62 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Tue, 03 Feb 2026 18:58:26 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 03 Feb 2026 18:58:27 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 03 Feb 2026 18:58:27 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 18:58:27 GMT
CMD ["eswrapper"]
# Tue, 03 Feb 2026 18:58:27 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9f04b3d5a77d94a61014844382160cb828bd21832d318f9c2ad7ec5c8f90b5`  
		Last Modified: Tue, 03 Feb 2026 18:57:31 GMT  
		Size: 4.3 MB (4297540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46991455029432b560728d7021100d6732b85b561b7a917d50c07dbfdc42803b`  
		Last Modified: Tue, 03 Feb 2026 18:57:31 GMT  
		Size: 1.5 KB (1537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a098630d0c0ed9032187e792857fe4f3529328c6bdbfe1c6e9165734c9405736`  
		Last Modified: Tue, 03 Feb 2026 18:57:31 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b3c6ec2c2398748b189bcb16686f70466edcf2a943c9b68424eba78e6e845e`  
		Last Modified: Tue, 03 Feb 2026 18:59:22 GMT  
		Size: 517.7 MB (517742964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d71fdd5f126f009e27c64f1297a939e6719ca871c2c3b309e31a03f3c7018`  
		Last Modified: Tue, 03 Feb 2026 18:59:04 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9c20001c597e28d45d7fdf4c15d9153396d0f015f16002462766d81e409d59`  
		Last Modified: Tue, 03 Feb 2026 18:59:05 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be3f33c46b2764e690cbfb035ecfb6fe9e5710284764baf7a345cc42bf4afde`  
		Last Modified: Tue, 03 Feb 2026 18:59:05 GMT  
		Size: 74.1 KB (74111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fc0e244e26e7cd89ffc71944ae9e2f7c2a3e660d7c739a737e742fd343e831`  
		Last Modified: Tue, 03 Feb 2026 18:59:06 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f8276f7c741228b81c9a0386d206712e0c30456f8dff72be29634fed7d2c14af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1ee68d7dab5847d6f036d7bda57d472776dc015a531a0b852f18b3c9df44dd`

```dockerfile
```

-	Layers:
	-	`sha256:93dcfa5998a51f376c65d9eccf6bbc5359104aee3054f4db232e3023014a4ecb`  
		Last Modified: Tue, 03 Feb 2026 18:59:05 GMT  
		Size: 2.1 MB (2090289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:753ce788c26ac2ea3c5693d2cbc670c4f6ba1e4bf91e7ad94cee76ee02c64c66`  
		Last Modified: Tue, 03 Feb 2026 18:59:05 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
