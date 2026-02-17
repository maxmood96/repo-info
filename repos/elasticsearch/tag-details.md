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
