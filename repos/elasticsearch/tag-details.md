<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.17`](#elasticsearch81917)
-	[`elasticsearch:9.3.6`](#elasticsearch936)
-	[`elasticsearch:9.4.2`](#elasticsearch942)

## `elasticsearch:8.19.17`

```console
$ docker pull elasticsearch@sha256:f8645eadfbf4f96e31043ed1e64e5f48ff826d0943660d48a4decd1428d9de96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.17` - linux; amd64

```console
$ docker pull elasticsearch@sha256:c111174e5cc1cac153a73bafe3c19c653b59748476af080ad64f6fcca29506e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.4 MB (724442342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ad4ea07e6bae91c37b2a95098f5456aae3c1785d5bff77b2b9b3152f60792b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 18:47:46 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 23 Jun 2026 18:47:46 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 23 Jun 2026 18:47:46 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:47:46 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 23 Jun 2026 18:48:50 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 23 Jun 2026 18:48:50 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 23 Jun 2026 18:48:50 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:48:50 GMT
ENV SHELL=/bin/bash
# Tue, 23 Jun 2026 18:48:50 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 23 Jun 2026 18:48:51 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 23 Jun 2026 18:48:51 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 23 Jun 2026 18:48:51 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 23 Jun 2026 18:48:51 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 23 Jun 2026 18:48:51 GMT
LABEL org.label-schema.build-date=2026-06-18T11:09:30.586586749Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=402bbb9d596fffa14980c1dd23afca6c7c765908 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.17 org.opencontainers.image.created=2026-06-18T11:09:30.586586749Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=402bbb9d596fffa14980c1dd23afca6c7c765908 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.17
# Tue, 23 Jun 2026 18:48:51 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 18:48:51 GMT
CMD ["eswrapper"]
# Tue, 23 Jun 2026 18:48:51 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d956965431a2405266cd19fbd13b994081409b49a29d9d2ec814cee2f9b39`  
		Last Modified: Tue, 23 Jun 2026 18:49:44 GMT  
		Size: 9.2 MB (9211286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffa3a2812fa0bca36b45b5c4a4f457a160c64a1cc16e861d5d585d1c6df0f27`  
		Last Modified: Tue, 23 Jun 2026 18:49:44 GMT  
		Size: 3.5 KB (3534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d2ad34bcd2f5267e69c5e9516369801d3f630683bf7f2167d48c26c56e0bbc`  
		Last Modified: Tue, 23 Jun 2026 18:50:04 GMT  
		Size: 685.2 MB (685221730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d32b29108766cfc81d0a47e0dfa0cd6b8f850dc4dcaf95d212f6a105f663eb0`  
		Last Modified: Tue, 23 Jun 2026 18:49:44 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058626ada7a2229f1f1913dbddb5a0bbd58a8fdb784fceae57ed214927855335`  
		Last Modified: Tue, 23 Jun 2026 18:49:45 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2867b45766aa16fc88e5a2f931d4f82393718c08f7891a0908ac1de333853caf`  
		Last Modified: Tue, 23 Jun 2026 18:49:45 GMT  
		Size: 164.2 KB (164191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6305aeebe0f010583ab9920dddfde7ecd65859669f4a83dc6c6f22e1497ef24a`  
		Last Modified: Tue, 23 Jun 2026 18:49:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e000e9b3661a3fe228160a47378ad6034eb0f3e75b66a786346bffc592bef39f`  
		Last Modified: Tue, 23 Jun 2026 18:49:47 GMT  
		Size: 97.1 KB (97102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.17` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2692fc8e89c07b9d3c843a71061b9defbf82971506d63d4d22d8541f79d3eeda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3228438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb96eec4f65c4b289680d057bed6df8a14fe41691300da010a690da30d44390`

```dockerfile
```

-	Layers:
	-	`sha256:8d7c22f779cbbad679a04ee51eff9abd552b45fed2a3221288443c98eb7b8f2f`  
		Last Modified: Tue, 23 Jun 2026 18:49:44 GMT  
		Size: 3.2 MB (3191624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d618b5d79528f82c8d4d400f622f732d4c041e4f4f533203c7cfd0fc35250d`  
		Last Modified: Tue, 23 Jun 2026 18:49:44 GMT  
		Size: 36.8 KB (36814 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.17` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:a83a78b1fa3104b51d63c91d55de907834e5f9b9b66050cce53df983926e71b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572081379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b455c1cee0bd4085a42b69abd33bf24ba357a9ad4f0a6e15d5ff4290389d61a`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 18:48:18 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 23 Jun 2026 18:48:18 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 23 Jun 2026 18:48:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:48:18 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 23 Jun 2026 18:49:01 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 23 Jun 2026 18:49:01 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 23 Jun 2026 18:49:01 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:49:01 GMT
ENV SHELL=/bin/bash
# Tue, 23 Jun 2026 18:49:01 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 23 Jun 2026 18:49:01 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 23 Jun 2026 18:49:01 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 23 Jun 2026 18:49:01 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 23 Jun 2026 18:49:01 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 23 Jun 2026 18:49:01 GMT
LABEL org.label-schema.build-date=2026-06-18T11:09:30.586586749Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=402bbb9d596fffa14980c1dd23afca6c7c765908 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.17 org.opencontainers.image.created=2026-06-18T11:09:30.586586749Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=402bbb9d596fffa14980c1dd23afca6c7c765908 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.17
# Tue, 23 Jun 2026 18:49:01 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 18:49:01 GMT
CMD ["eswrapper"]
# Tue, 23 Jun 2026 18:49:01 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0cafc562d636cd8a0def246a0ee2523ea58801ce03feca04b6b62d12413ef7`  
		Last Modified: Tue, 23 Jun 2026 18:49:41 GMT  
		Size: 8.9 MB (8903107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe37a5223fc75e76f25d9363f8e72d8474a7697b7c28f78cfc7e66891c1f7731`  
		Last Modified: Tue, 23 Jun 2026 18:49:40 GMT  
		Size: 3.5 KB (3531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d46ac912a2d83b26e1f99c2847bae7f2ed4adeac51e38e43e77caaf1b7020ba`  
		Last Modified: Tue, 23 Jun 2026 18:49:58 GMT  
		Size: 534.0 MB (534029265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0fc7e61bc0554555dce3e0309f7d017eb327ec93cbcc6ff0a27fccee199d54`  
		Last Modified: Tue, 23 Jun 2026 18:49:40 GMT  
		Size: 9.1 KB (9107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9af45b6869f821a9bcc821882bd1f738585b6186fbe790547c7d1535639b7c`  
		Last Modified: Tue, 23 Jun 2026 18:49:41 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd6bf32973d8cef80e54293f677d47bd3dbbb8dd0171f793b7f9f796a23bb82`  
		Last Modified: Tue, 23 Jun 2026 18:49:42 GMT  
		Size: 160.7 KB (160703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d27661a09a1d3d791bd9121dc8ea5a695cb92518a08df0602fc0df46e8ce7ec`  
		Last Modified: Tue, 23 Jun 2026 18:49:42 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0525dc7295dc5372f919dc78aea9a34c9625ab6a356641bc9ac661c1c08620`  
		Last Modified: Tue, 23 Jun 2026 18:49:43 GMT  
		Size: 97.1 KB (97102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.17` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8a7e17c69534288e6851cd123838ba818c683701468784e1a0fa0c662ab3e021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3229055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210735cba290a088a1ee9a93dee73cdc76e673ebe8e1df245ba752baadfd63e`

```dockerfile
```

-	Layers:
	-	`sha256:be42d3512927cfefa30441a634255ad8510eba6b3165d77cf80da9aed013985d`  
		Last Modified: Tue, 23 Jun 2026 18:49:41 GMT  
		Size: 3.2 MB (3192037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac9fbc43f920b75d35906bd6f22487ce622cad286f8929ece4da6903e68e8968`  
		Last Modified: Tue, 23 Jun 2026 18:49:40 GMT  
		Size: 37.0 KB (37018 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.6`

```console
$ docker pull elasticsearch@sha256:50ae7ab374ec86a5c3bdb89761777d7d12ee1a16cd5455d284f03e96effeaea3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:5870b494648f1e6e74d2e81d155c4c5195580597776b9657b91af4ef4c17439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.8 MB (721815640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc3b810bcd31a5e7bbfac3aea1dacff51d0120368d5c9ff082a5b4174bbe860`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Tue, 23 Jun 2026 18:48:28 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 23 Jun 2026 18:48:28 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 23 Jun 2026 18:49:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:49:14 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 23 Jun 2026 18:49:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 23 Jun 2026 18:49:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 23 Jun 2026 18:49:24 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 23 Jun 2026 18:49:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:49:24 GMT
ENV SHELL=/bin/bash
# Tue, 23 Jun 2026 18:49:24 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 23 Jun 2026 18:49:24 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 23 Jun 2026 18:49:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 23 Jun 2026 18:49:24 GMT
LABEL org.label-schema.build-date=2026-06-18T10:10:50.114739011Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:10:50.114739011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Tue, 23 Jun 2026 18:49:24 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 23 Jun 2026 18:49:24 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 23 Jun 2026 18:49:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 18:49:24 GMT
CMD ["eswrapper"]
# Tue, 23 Jun 2026 18:49:24 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbb8f4d40604f9b135e733a098f0efe0ddf3e443d8d156e29904369644720bf`  
		Last Modified: Tue, 23 Jun 2026 18:50:18 GMT  
		Size: 4.1 MB (4115395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beddf989bccd823ee99a7221c9c3ef2ecd9d84825675eb3e51a9d984622d24b3`  
		Last Modified: Tue, 23 Jun 2026 18:50:17 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde2a2e7fc62f6886cdbed44e01f323b9c6e7f9f84c266b86f98593c77fd3a99`  
		Last Modified: Tue, 23 Jun 2026 18:50:17 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32970a7adbb67cf8a490552f2b4e02fc4f8bb45c1b71acb8134a521c509c7c0`  
		Last Modified: Tue, 23 Jun 2026 18:50:33 GMT  
		Size: 676.9 MB (676930083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e36ad761a4dff8fdde6b9a5ad936ccee233272dc07bac820d74d5e0ef88165`  
		Last Modified: Tue, 23 Jun 2026 18:50:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b479afacf67efc8d18d71bf535b84789dd971bdd4e910ba2fa9523312496db0`  
		Last Modified: Tue, 23 Jun 2026 18:50:19 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96263072bc02359d4529b615c8ec2569f4dcd36f1eada2ed6aa96bbe444feaf0`  
		Last Modified: Tue, 23 Jun 2026 18:50:19 GMT  
		Size: 75.2 KB (75190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac85c2885495ee604db4fe0e0696aad94dc88c5032406f711e85f6cecf908f`  
		Last Modified: Tue, 23 Jun 2026 18:50:20 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:bed5d4988d414700a784b0a3b6c995e46a7c7b4e93dcfbb79237fc1bcfe7258d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9b7e79b7a3e8026cc284ba6820cd7b543b57a889c673fb274af9f787c947b7`

```dockerfile
```

-	Layers:
	-	`sha256:b654ecbd2f104c5bc556595eff3304249754ee49501b5597959907e371d43167`  
		Last Modified: Tue, 23 Jun 2026 18:50:17 GMT  
		Size: 2.1 MB (2089403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a655e247656837dc1b9c4bb2cfb3fab5f69c4b6a6790b886b5a13646d506d8c`  
		Last Modified: Tue, 23 Jun 2026 18:50:17 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:0b7fad9f948a0c4c22e281ddaadd479841f58ad5f0270366c1f4fd0115f27bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565855124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efc00ec4277c791ba2c6fa7d6b0e943f071b260de9358936416854fa53b74eb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:12:59 GMT
ENV container oci
# Tue, 23 Jun 2026 05:12:59 GMT
COPY dir:923fd04a317c8ab7292cc4c6490977e5f3d0a2e1ff9dc5a4ce7f5c95aef17062 in /      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:36Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:36Z" "architecture"="aarch64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:36Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:03 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:04 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 24 Jun 2026 23:04:37 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:04:37 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 24 Jun 2026 23:04:37 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 24 Jun 2026 23:04:44 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 24 Jun 2026 23:04:44 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 24 Jun 2026 23:04:44 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:04:44 GMT
ENV SHELL=/bin/bash
# Wed, 24 Jun 2026 23:04:44 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:04:44 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 24 Jun 2026 23:04:44 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 24 Jun 2026 23:04:44 GMT
LABEL org.label-schema.build-date=2026-06-18T10:10:50.114739011Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:10:50.114739011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Wed, 24 Jun 2026 23:04:44 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 24 Jun 2026 23:04:44 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 24 Jun 2026 23:04:44 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:04:44 GMT
CMD ["eswrapper"]
# Wed, 24 Jun 2026 23:04:44 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e886a58df3b8e28880911d2df47b19f07ea4be6a7f8bf083ec0dc452f63f85e2`  
		Last Modified: Wed, 24 Jun 2026 23:05:23 GMT  
		Size: 4.1 MB (4117163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3aaf084b49c4e12cb89a19178d83eea6b44116cc37d4f3f704b94df874abde`  
		Last Modified: Wed, 24 Jun 2026 23:05:22 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da0e84d7f2d6ddd3b4f31addf7012608a02af00576b2584c373b01bcae74d35`  
		Last Modified: Wed, 24 Jun 2026 23:05:22 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281a5f5922aa484df81bf55be73c4fa33f6a74119a8f8ec7ce34add5d6a1acbd`  
		Last Modified: Wed, 24 Jun 2026 23:05:33 GMT  
		Size: 522.8 MB (522843678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2eafdf6176786fbc13efea890e68e780d3a120f66f4e4bb4be1346919a1d2d`  
		Last Modified: Wed, 24 Jun 2026 23:05:24 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce5d26994ac9fc3e6e1f464f2029b7f8ff9e2ff12c9c3af79b8b1bd8d89fdeb`  
		Last Modified: Wed, 24 Jun 2026 23:05:24 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffaacd2c9accf1b4280b68259b36368239494a8433a514f2c745a90b87fe78e`  
		Last Modified: Wed, 24 Jun 2026 23:05:24 GMT  
		Size: 74.1 KB (74111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b0a59e10496ffd0edd8073fc05e09136a0c7562adf68fb34160121f3dede2d`  
		Last Modified: Wed, 24 Jun 2026 23:05:25 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:41c7282690d3724d7cba30aecb07bf66d3d1014720bb977c3e5851a97d0b6969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba499c7c4abd81253a8ce98f515951680a37c42f214a980cb412079b01065e3f`

```dockerfile
```

-	Layers:
	-	`sha256:5e9c8e4aff5b790e3d46153549f88fbf52a67e2a91a9124e07255efa00f80d19`  
		Last Modified: Wed, 24 Jun 2026 23:05:23 GMT  
		Size: 2.1 MB (2089977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b341f60ef02369cd1caf7b3fbd22c285aaf4bca90f33de181a3dc7037958fbf`  
		Last Modified: Wed, 24 Jun 2026 23:05:23 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.2`

```console
$ docker pull elasticsearch@sha256:715c5d552328d83dcee6082bd5125327332a649f8e0aedb5fe0553d7be75bf21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6d35c4030bcbfb93e50bd792f0e47d8364d3acb877d841f97195e4a110cf841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 MB (865103528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591cd0e2ee8ca7a65e8a5fbcc495dea72ee69ed3ad4dd9405cfac7cac6d8c7c7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:14:56 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 15 Jun 2026 23:16:20 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:16:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:16:20 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 15 Jun 2026 23:16:31 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 15 Jun 2026 23:16:31 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 15 Jun 2026 23:16:31 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:16:31 GMT
ENV SHELL=/bin/bash
# Mon, 15 Jun 2026 23:16:31 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:16:32 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 15 Jun 2026 23:16:32 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 15 Jun 2026 23:16:32 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Mon, 15 Jun 2026 23:16:32 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 15 Jun 2026 23:16:32 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:16:32 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:16:32 GMT
CMD ["eswrapper"]
# Mon, 15 Jun 2026 23:16:32 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cee6e5935d0f06fb2a2455cd614e34acc4b7160a12e3a58b808b268e2565d6`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 4.1 MB (4115496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbba1dbf950863e7d0a0eb29de32ea73396cce3ade6226e1cbaf636968690de`  
		Last Modified: Mon, 15 Jun 2026 23:16:23 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd7042f59b372fb4abc5d83db83bfa8af7770b21f2129f00bc09c35e188adb3`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0010da65571dbff9324067c7a1b52f2fe917942a69f772b8834ba3ed8c6834ed`  
		Last Modified: Mon, 15 Jun 2026 23:17:42 GMT  
		Size: 820.2 MB (820217877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e999231bb3ed2836a60a193d1aaa6d778394327b3787ed69739baeb513630e`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a60cf00dcb96ab3080d7257aa943a7dc7fd051c32c85087ae87a1a80f904c0a`  
		Last Modified: Mon, 15 Jun 2026 23:17:28 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4b69228720cd51da5f35484dbc36a70f12b4fdbc7294a24a5581bb807e4a2`  
		Last Modified: Mon, 15 Jun 2026 23:17:29 GMT  
		Size: 75.2 KB (75186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f039a9722a5dc5dc7d14eac04c8ef64e99ccda5639818fd31bd7731302f1be`  
		Last Modified: Mon, 15 Jun 2026 23:17:29 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3b872df0dd4450dadc8c7adb15ba02633489797efc87bf2dbed6adbc21fef085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbf79d8c0d425c13f74e0a0540b05d461de1d46e909fc7bf19d6d191a50e3a4`

```dockerfile
```

-	Layers:
	-	`sha256:aea72a5ec5e6c14e8e3bfa5a31ec4f5bd3dd7f925f964da4df2fe80726369ce0`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 2.4 MB (2391025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38de8bba6bb5a882aad927cd2e8e399526946fda882d8c3fa89fb30025ce5298`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 33.8 KB (33775 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:1c6d34f48b8da99c13ab7211fa050274ee0f4bbbec72e88cc87ba14a05a0086e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709780121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916060414839765b3c5334fc653ac7c46418e086cca1c4a193579d3ece6feb42`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:14:22 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:22 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 15 Jun 2026 23:15:33 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:15:33 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:15:33 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 15 Jun 2026 23:15:40 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 15 Jun 2026 23:15:40 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 15 Jun 2026 23:15:40 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:15:40 GMT
ENV SHELL=/bin/bash
# Mon, 15 Jun 2026 23:15:40 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:15:41 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 15 Jun 2026 23:15:41 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 15 Jun 2026 23:15:41 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Mon, 15 Jun 2026 23:15:41 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 15 Jun 2026 23:15:41 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:15:41 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:15:41 GMT
CMD ["eswrapper"]
# Mon, 15 Jun 2026 23:15:41 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cec1af2b18d221ffb16e0c6e868eb74dc2837b1ce5c301a634033ec179137`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 4.1 MB (4120762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b8276c57878e1868c3d80c94f03815f0e4d2e41c23c1316cde25a2f912b63`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5a991ca15efcc9f28e063a853a65f5a651eb3cf8c27d02b709873e1643a6a6`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87da9774d1d8d47717cf41d310f8d01606951b8f9d334033cb24b96b189e427`  
		Last Modified: Mon, 15 Jun 2026 23:16:42 GMT  
		Size: 666.7 MB (666697876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236e72258713ca2820a7fb631b0e062b52f745734faee20bcbbb8835cc3244b`  
		Last Modified: Mon, 15 Jun 2026 23:16:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f392cbca88ae4b3400b69e45137975e11de8d0191dccbdb6ceaa01337573c2aa`  
		Last Modified: Mon, 15 Jun 2026 23:16:28 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987ee265a78474021b0dc187aae5303f67f7285eb736badb60224ff17813b93`  
		Last Modified: Mon, 15 Jun 2026 23:16:29 GMT  
		Size: 74.1 KB (74109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2de42610097dca4fad2d7a0cd14cdc6f7be2ce5ba5a8c02f3ef23e99cdc948c`  
		Last Modified: Mon, 15 Jun 2026 23:16:30 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e2d9015034855aa00f21ce0cd03a53c71df1732d7185035a459a6570e6ae7222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba7561a47a030f51e709220a5b91b8d1b066f3f5eed916a600f444c2f26898b`

```dockerfile
```

-	Layers:
	-	`sha256:47b63c368795dc5ca2dc6e743c4e66dc364a9211e8c83134d84661a3f801777c`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 2.4 MB (2391587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae39a38e853d468054224d8f8bc96f65be769bcc2e0fea326218ea9a509d6dcf`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 34.0 KB (33958 bytes)  
		MIME: application/vnd.in-toto+json
