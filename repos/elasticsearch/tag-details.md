<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.11`](#elasticsearch81911)
-	[`elasticsearch:9.2.5`](#elasticsearch925)
-	[`elasticsearch:9.3.0`](#elasticsearch930)

## `elasticsearch:8.19.11`

```console
$ docker pull elasticsearch@sha256:4866a92df947106b74e44d08b55ce4e99aeae8e074ecdc6dab67d2131773dccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.11` - linux; amd64

```console
$ docker pull elasticsearch@sha256:ddef154765efe95d5f94e26f460ce604e20668cf67b1822943a156c1edf1455e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.5 MB (716541323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048ca9c8593ded8c015fd9ab6cb132523cebca0369e4ec6fddd330c9de6edfae`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:34 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 17 Feb 2026 20:20:34 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 17 Feb 2026 20:20:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Feb 2026 20:20:34 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 17 Feb 2026 20:22:03 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 17 Feb 2026 20:22:03 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Feb 2026 20:22:03 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:22:03 GMT
ENV SHELL=/bin/bash
# Tue, 17 Feb 2026 20:22:03 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:22:04 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 17 Feb 2026 20:22:04 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Feb 2026 20:22:04 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Feb 2026 20:22:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 17 Feb 2026 20:22:04 GMT
LABEL org.label-schema.build-date=2026-01-28T22:06:09.337243873Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c5253e1bcb0268a5dafed9dee18e16fd3144d7d6 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.11 org.opencontainers.image.created=2026-01-28T22:06:09.337243873Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c5253e1bcb0268a5dafed9dee18e16fd3144d7d6 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.11
# Tue, 17 Feb 2026 20:22:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:22:04 GMT
CMD ["eswrapper"]
# Tue, 17 Feb 2026 20:22:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684406ba667aed3a96bf2f2df9f706794e0541b1ff35c4ca07e166418ba83a35`  
		Last Modified: Tue, 17 Feb 2026 20:22:54 GMT  
		Size: 6.6 MB (6615836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057a4adac372c0826d5014f9b0ef5f46792e8538d63ef0ae3e178f3e11d495bc`  
		Last Modified: Tue, 17 Feb 2026 20:22:53 GMT  
		Size: 3.5 KB (3530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92e05011abb4aa65e2ac5d5b5cdb22b3cd20daacc8427878bfe41aaa605bcab`  
		Last Modified: Tue, 17 Feb 2026 20:23:07 GMT  
		Size: 679.9 MB (679903196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cae876ae148fbd60d00a8d6e3cd7e502370882e278f616b5a74d4199b32757`  
		Last Modified: Tue, 17 Feb 2026 20:22:53 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f60481087d6cc8ce06e91b72b083afbcd3027f6b9b4025d9f4a26118fce72e3`  
		Last Modified: Tue, 17 Feb 2026 20:22:55 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69fc464ae2e622a669be357c9886c97e99eea9cc8c0de3c2ef7b6769ea036c1`  
		Last Modified: Tue, 17 Feb 2026 20:22:54 GMT  
		Size: 163.9 KB (163936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171e34dbe7cff1d33bc957788c68dfda09c9dd09d09f2fb3b32d478a2dd72b76`  
		Last Modified: Tue, 17 Feb 2026 20:22:55 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a18f06c14adb61caf0f479f38a26314f5a128f3a4c91731ed48ce9bc2f087a1`  
		Last Modified: Tue, 17 Feb 2026 20:22:56 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.11` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d01a2f7380fc6a83c7cc4157230e02713d00e41957348b74d5e68a08c1034e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3a2b6329c43e053f3fe1d6a96a731f2dba512db642d0c8acb78835e604302a`

```dockerfile
```

-	Layers:
	-	`sha256:ea2ca0ddcc3e331ca411869ce26aaf96bda0910416ec532d03ccf4b0931642f8`  
		Last Modified: Tue, 17 Feb 2026 20:22:54 GMT  
		Size: 3.2 MB (3208982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5436e351d0d67ee89014947a9058363be27ccce3b427d3d6b7e72ecb0c74e9`  
		Last Modified: Tue, 17 Feb 2026 20:22:53 GMT  
		Size: 36.8 KB (36847 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.11` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:0621096ee58556ac5f46bef1a3c14d82f8743d78e61d53ab721672ee7df23596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564247223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf103577e3c978033702f5aaf819527cb29e98259b2f138bd37a2f48b33582a6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:04 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 17 Feb 2026 20:20:04 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 17 Feb 2026 20:20:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Feb 2026 20:20:04 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 17 Feb 2026 20:21:11 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 17 Feb 2026 20:21:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Feb 2026 20:21:11 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:21:11 GMT
ENV SHELL=/bin/bash
# Tue, 17 Feb 2026 20:21:11 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:21:11 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 17 Feb 2026 20:21:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Feb 2026 20:21:12 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Feb 2026 20:21:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 17 Feb 2026 20:21:12 GMT
LABEL org.label-schema.build-date=2026-01-28T22:06:09.337243873Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c5253e1bcb0268a5dafed9dee18e16fd3144d7d6 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.11 org.opencontainers.image.created=2026-01-28T22:06:09.337243873Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c5253e1bcb0268a5dafed9dee18e16fd3144d7d6 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.11
# Tue, 17 Feb 2026 20:21:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:21:12 GMT
CMD ["eswrapper"]
# Tue, 17 Feb 2026 20:21:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d79b605ee275697c192c5e541dbcf964e311641394895d6a8ff3876e5f2b43`  
		Last Modified: Tue, 17 Feb 2026 20:21:51 GMT  
		Size: 6.5 MB (6515380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a9532c1e285f5442f59eeeefbe0252d4f07d48036703e87675ae310db6572f`  
		Last Modified: Tue, 17 Feb 2026 20:21:50 GMT  
		Size: 3.5 KB (3529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e208100d59f32e235d46a569946eeb4b98b957914111009872974e30552d49f`  
		Last Modified: Tue, 17 Feb 2026 20:22:00 GMT  
		Size: 528.6 MB (528576040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8351fd5a645546078623e953411b17d2a40caef89919708ee3edb58a06566a`  
		Last Modified: Tue, 17 Feb 2026 20:21:50 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4120227e4781e9dc18ebc1068bb55541ee17aa1b27b77ede9b89d90c50e23e`  
		Last Modified: Tue, 17 Feb 2026 20:21:52 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858ac217c8ab5c1c9a37fa5c0b1deca31d8825806e05853dd335cbaa4fc522ea`  
		Last Modified: Tue, 17 Feb 2026 20:21:52 GMT  
		Size: 160.4 KB (160364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c4ba1de6e41345a23e1f07950670d52241a0ce688c85882a256781522cf9e`  
		Last Modified: Tue, 17 Feb 2026 20:21:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1e44a8904bbae4a608aa492b24646339c97a23c85d46ca7f6361ea45fe534d`  
		Last Modified: Tue, 17 Feb 2026 20:21:53 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.11` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a3cb8da1ffa0c6833a347628da874752d47473d7f901fe591ce188d6be403b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae12b36db3f5a162fee526df59c2af381617631805f43b9a40b15bd5d3cd4cd`

```dockerfile
```

-	Layers:
	-	`sha256:e9317417bef8f9eb111ca589fbb23578424f069633de624f153f24a3735663cd`  
		Last Modified: Tue, 17 Feb 2026 20:21:51 GMT  
		Size: 3.2 MB (3209395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922112193ea2cf47e9e1751b6c2a8243b7dfba3fa772c7c7e721a5b30cca62e7`  
		Last Modified: Tue, 17 Feb 2026 20:21:50 GMT  
		Size: 37.0 KB (37050 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.5`

```console
$ docker pull elasticsearch@sha256:c2a1f3ac15e5d21fe05e34321c46b6d1520609918ae0e1a375667a7be3b7b98d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:88279399b3fb37c1a97f760d79c27a0773d683d6d95d62ddf19a01e038ed4956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.2 MB (738220850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7247b4f2f2da5945794f5ea711f9f3186724153b0c4fa64fb4fb899f9663b67f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Wed, 18 Feb 2026 19:20:19 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:20:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 18 Feb 2026 19:21:35 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:21:35 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 18 Feb 2026 19:21:35 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 18 Feb 2026 19:21:44 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 18 Feb 2026 19:21:45 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 18 Feb 2026 19:21:45 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:21:45 GMT
ENV SHELL=/bin/bash
# Wed, 18 Feb 2026 19:21:45 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:21:45 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 18 Feb 2026 19:21:45 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 18 Feb 2026 19:21:45 GMT
LABEL org.label-schema.build-date=2026-01-28T22:05:53.857690766Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T22:05:53.857690766Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Wed, 18 Feb 2026 19:21:45 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 18 Feb 2026 19:21:45 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 18 Feb 2026 19:21:45 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 18 Feb 2026 19:21:45 GMT
CMD ["eswrapper"]
# Wed, 18 Feb 2026 19:21:45 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f7d9d00b53b16011a2d144379280cd76d4320b81ae8749c0f2ac9e445a6998`  
		Last Modified: Wed, 18 Feb 2026 19:22:38 GMT  
		Size: 4.3 MB (4282770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c8e0e64a5f38f8c7c677348289f4691140dd14aa7d44d846d40daf74563337`  
		Last Modified: Wed, 18 Feb 2026 19:22:37 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d9ae9a1d40aab30e1f0282718507b647ddcb2cb86632a6adb9286a0275fd12`  
		Last Modified: Wed, 18 Feb 2026 19:22:37 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcde56fecdd755a4b4783475171688c8e18fd3c8873fa269306a440a9f861592`  
		Last Modified: Wed, 18 Feb 2026 19:22:54 GMT  
		Size: 693.8 MB (693814527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4524ceb3b6ab972080ff7812649a21c16925e0f54085e9e287f83094858ccf50`  
		Last Modified: Wed, 18 Feb 2026 19:22:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4adf192f25261a3469c16aaa8a3743b2148ca70540d938508814b642fed749a`  
		Last Modified: Wed, 18 Feb 2026 19:22:39 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce31c5be2c463ce139c3d0a4449b9ef2f2dd60f1bdb1103ed7502d256049c3d`  
		Last Modified: Wed, 18 Feb 2026 19:22:39 GMT  
		Size: 75.2 KB (75181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8878538a2d1ee3daffbcfe128fec5aec9b4f181465e25ba19336d938029c971b`  
		Last Modified: Wed, 18 Feb 2026 19:22:40 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:97289e1cb84f3a3aa3b54793650e9f5a4ed8514dea77d43748325c22b0496901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f081b39249b4ba2eb2cd9cc166a53aefa4e88c3fb29729666ec7077a369ba3`

```dockerfile
```

-	Layers:
	-	`sha256:de585ba494e4263a6830eabfabd90a7c59ff449eeeecfec3fbb6e94a1141b18e`  
		Last Modified: Wed, 18 Feb 2026 19:22:37 GMT  
		Size: 2.1 MB (2098141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87de6ee581512471238589c6f27384138623d5a409a0426150c159b5ca6142b7`  
		Last Modified: Wed, 18 Feb 2026 19:22:37 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:bf8490fad08755178b9e9da036333c860558d6e36706f8c5bed3fcb2063671b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.2 MB (582184924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d573a1b358311da05840fa06e3bb8e8127646e46a7da8f86083719efcbff5b6e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Wed, 18 Feb 2026 19:19:00 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:19:00 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 18 Feb 2026 19:20:04 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:20:04 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 18 Feb 2026 19:20:04 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 18 Feb 2026 19:20:10 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 18 Feb 2026 19:20:10 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 18 Feb 2026 19:20:10 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:20:10 GMT
ENV SHELL=/bin/bash
# Wed, 18 Feb 2026 19:20:10 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:20:10 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 18 Feb 2026 19:20:10 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 18 Feb 2026 19:20:10 GMT
LABEL org.label-schema.build-date=2026-01-28T22:05:53.857690766Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T22:05:53.857690766Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c26a2652b4f4e323c18bdb4f56f0038c8aece886 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Wed, 18 Feb 2026 19:20:10 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 18 Feb 2026 19:20:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 18 Feb 2026 19:20:10 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 18 Feb 2026 19:20:10 GMT
CMD ["eswrapper"]
# Wed, 18 Feb 2026 19:20:10 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff67675d405d7dcd8bcc5fe29f366109b4c77211f3c607202e85e69678117e1`  
		Last Modified: Wed, 18 Feb 2026 19:20:50 GMT  
		Size: 4.3 MB (4289671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98801047e2706ee41ea66ac28426559046b021ce8c67060bd2f46a459ed0cb9`  
		Last Modified: Wed, 18 Feb 2026 19:20:50 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f18b7293759c4b551f10dfd255298ccc2d034fbbc18a2d0ab29cc6015fa5bc`  
		Last Modified: Wed, 18 Feb 2026 19:20:50 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cda423f1cff16e653071e559bb0dfed33dbc1629885f4bd9b15a0aa1f61bd6`  
		Last Modified: Wed, 18 Feb 2026 19:21:00 GMT  
		Size: 539.6 MB (539604273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de46d4631d808035fedd296a5154bc5441be8e185aa92b0456810544f9dc928c`  
		Last Modified: Wed, 18 Feb 2026 19:20:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a379f8fec2332f1508500aacee21da14581573b36316d8cbee11be01d68da1`  
		Last Modified: Wed, 18 Feb 2026 19:20:51 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5c16c7b196fce1a3b867362c901d4a154895275eab50a91cf949e5937f0845`  
		Last Modified: Wed, 18 Feb 2026 19:20:52 GMT  
		Size: 74.1 KB (74107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fa5cb11debba314631f3c057d363b2df1d1ef64e7d0d4bd39c3eeac8f7477a`  
		Last Modified: Wed, 18 Feb 2026 19:20:52 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d62f95a75b081a48f17035d075f0e09d5d3bb876a7ed4f78839dd99e70176801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd880732aa5754e288be3838bada7f155f1c91b006df592ee58140ace5e7156d`

```dockerfile
```

-	Layers:
	-	`sha256:c549501a4139cb86a37e2f317f60855b62f93815a419d40d6534128c1f2371ec`  
		Last Modified: Wed, 18 Feb 2026 19:20:50 GMT  
		Size: 2.1 MB (2098703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371847611bc5a185f9b4fcfda017e994652735b760d18dd292155a2aaf431808`  
		Last Modified: Wed, 18 Feb 2026 19:20:50 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.0`

```console
$ docker pull elasticsearch@sha256:d6dbcf006047aafb87719e6e0b673c2067a760c902bd207059e84b27b22e2bb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f9d3f7a2093d16c8e1feac228396b9f1693e58104d064f69d050e4aaa3143703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.4 MB (716362075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd311980f77ad2e7fd7b6382b918107aa2fe191a29d351b344e7d00b1b4dbb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Wed, 18 Feb 2026 19:20:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:20:21 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 18 Feb 2026 19:21:30 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:21:30 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 18 Feb 2026 19:21:30 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 18 Feb 2026 19:21:40 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 18 Feb 2026 19:21:40 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 18 Feb 2026 19:21:40 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:21:40 GMT
ENV SHELL=/bin/bash
# Wed, 18 Feb 2026 19:21:40 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:21:40 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 18 Feb 2026 19:21:40 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 18 Feb 2026 19:21:40 GMT
LABEL org.label-schema.build-date=2026-01-29T10:05:46.708397977Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=17b451d8979a29e31935fe1eb901310350b30e62 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T10:05:46.708397977Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=17b451d8979a29e31935fe1eb901310350b30e62 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Wed, 18 Feb 2026 19:21:40 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 18 Feb 2026 19:21:40 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 18 Feb 2026 19:21:40 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 18 Feb 2026 19:21:40 GMT
CMD ["eswrapper"]
# Wed, 18 Feb 2026 19:21:40 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41de172b747d8d649cabc8b8aa735c6072c0dfa083eaa156346f1205076ef69f`  
		Last Modified: Wed, 18 Feb 2026 19:22:32 GMT  
		Size: 4.3 MB (4282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9613329a10c0ef41e09a6f8604cc68383ccdf1299587cfece3d196b57ee071ed`  
		Last Modified: Wed, 18 Feb 2026 19:22:32 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4e679501ef4739e758ef6ee0f22eccc49169448b05896e6fb2a9809baa7b9e`  
		Last Modified: Wed, 18 Feb 2026 19:22:32 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf1d3cc0251a939db7aa5c633a7390eeb0f0d929e58433bda0cf349e953cf60`  
		Last Modified: Wed, 18 Feb 2026 19:22:45 GMT  
		Size: 672.0 MB (671955737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a83b76b2c03a1a97b06c820f82a82819df9089d7dca0aea5591e73bff965f6`  
		Last Modified: Wed, 18 Feb 2026 19:22:33 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ac809395ee0cddfef0648d246ff885744e9e432478294ca97edb55a6677638`  
		Last Modified: Wed, 18 Feb 2026 19:22:33 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d093fbb20007297dc0126360fa79c0b7d801cf0ee1fc46f80cefa0c4b55b5b`  
		Last Modified: Wed, 18 Feb 2026 19:22:34 GMT  
		Size: 75.2 KB (75185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab374fb50d8681f6256bc9c89be6fe103852060b91fcb5e84b3030e692f2457`  
		Last Modified: Wed, 18 Feb 2026 19:22:35 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1ad856dd8d777a52fe8ca0032c2fbf199f68ec0b4e53f5f59c3497a07482411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00ca96c951113340935a19fee7771d8d260eaee21d453b66802a61296eadc12`

```dockerfile
```

-	Layers:
	-	`sha256:8a82eda92459682f5182cec78621a227578e34f26aeba9ed7a48a4907e19d40c`  
		Last Modified: Wed, 18 Feb 2026 19:22:32 GMT  
		Size: 2.1 MB (2089781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c434e01e525012a3d4981de20b4562b8ea57bb6cddc91177b85d8d4558adccdd`  
		Last Modified: Wed, 18 Feb 2026 19:22:32 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b0392265ac5d00d89d08cc7e8e37f83d850460e5469992216fcfd8e862ae5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.3 MB (560323907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6265b22b7fe86ef2aae2020795fc965e0aa08db783a9f2c63a05497e1ade8f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Wed, 18 Feb 2026 19:19:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:19:15 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 18 Feb 2026 19:20:11 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:20:11 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 18 Feb 2026 19:20:11 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 18 Feb 2026 19:20:17 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 18 Feb 2026 19:20:17 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 18 Feb 2026 19:20:17 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:20:17 GMT
ENV SHELL=/bin/bash
# Wed, 18 Feb 2026 19:20:17 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:20:17 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 18 Feb 2026 19:20:17 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 18 Feb 2026 19:20:17 GMT
LABEL org.label-schema.build-date=2026-01-29T10:05:46.708397977Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=17b451d8979a29e31935fe1eb901310350b30e62 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T10:05:46.708397977Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=17b451d8979a29e31935fe1eb901310350b30e62 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Wed, 18 Feb 2026 19:20:17 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 18 Feb 2026 19:20:17 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 18 Feb 2026 19:20:17 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 18 Feb 2026 19:20:17 GMT
CMD ["eswrapper"]
# Wed, 18 Feb 2026 19:20:17 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add48db702b69c8580fadfdf282fa232b519aa73078160219d78ab24388596ae`  
		Last Modified: Wed, 18 Feb 2026 19:20:56 GMT  
		Size: 4.3 MB (4289733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eba0a3f5a557ced6447d1f800d0f88b78bef92bdf7a416b7f2654781136ccb7`  
		Last Modified: Wed, 18 Feb 2026 19:20:56 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0402a4273575dca262d84dfc0f7fcc3cdcf2ee2949ae9e1d61c476667631e553`  
		Last Modified: Wed, 18 Feb 2026 19:20:56 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b2a2e52d9c0467a2fa359887299a62cdd981bb71f891fb53d3fda7f42fb685`  
		Last Modified: Wed, 18 Feb 2026 19:21:09 GMT  
		Size: 517.7 MB (517743191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f17ef3761228b0e6e2ee17a9d56b653d67909dbf2f8afe3f517ef5bf2806f5a`  
		Last Modified: Wed, 18 Feb 2026 19:20:57 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea041c761c72ca42b75ba294e39904d347a4d265060ff91eab37d624d5183f45`  
		Last Modified: Wed, 18 Feb 2026 19:20:57 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6455d8f23192f8db4f71e85bce11e82656097866b5f92a43142efa05b4af37`  
		Last Modified: Wed, 18 Feb 2026 19:20:57 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350fea922b727af116a80833bd10f329052e0483ee42b993cd5493a187a7fd9d`  
		Last Modified: Wed, 18 Feb 2026 19:20:58 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b4bf73579f93a2c6638df6eb7c1f116e2f5d1d912f04d0d49e5c5aaf215d1d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c6a6e0cd39ae20cc0016dadd04235a22ae23c80319e37053425586a00d737a`

```dockerfile
```

-	Layers:
	-	`sha256:f23695ca1311e16fd0da14ab5c039bacf67d03a5b55126414b4e9185185ac59e`  
		Last Modified: Wed, 18 Feb 2026 19:20:56 GMT  
		Size: 2.1 MB (2090343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5667b2cdfff395b935db770864253c67fd84ee935127cb35cf2d261177ae3fa2`  
		Last Modified: Wed, 18 Feb 2026 19:20:56 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
