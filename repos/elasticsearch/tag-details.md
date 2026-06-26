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
$ docker pull elasticsearch@sha256:13f90e02a1181b850f6b940eaa1dc602470cea21f30c6918976c0e534c21f905
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:5fb4f4e1645d3406f069ca6619c31dc6185612ff31d76b2c9f547d68f6b9daf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.8 MB (721823450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5f2a9f5b1df2bca1f0ce4b006639f82546792c90b32d21eccd5fbd404a7c9e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:47:54 GMT
ENV container oci
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:a7d61486b18f71651e6d0b0c0267c96964cdf86a5c99a34dafc1bfd05eac4cc1 in /      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:47:55 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /root/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:47:36Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:47:36Z" "architecture"="x86_64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:47:36Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:27:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:27:22 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 25 Jun 2026 23:28:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:28:44 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 25 Jun 2026 23:28:44 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 25 Jun 2026 23:28:54 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 25 Jun 2026 23:28:54 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 25 Jun 2026 23:28:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:28:54 GMT
ENV SHELL=/bin/bash
# Thu, 25 Jun 2026 23:28:54 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:28:54 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 25 Jun 2026 23:28:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 25 Jun 2026 23:28:54 GMT
LABEL org.label-schema.build-date=2026-06-18T10:10:50.114739011Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:10:50.114739011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Thu, 25 Jun 2026 23:28:54 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 25 Jun 2026 23:28:54 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 25 Jun 2026 23:28:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:28:54 GMT
CMD ["eswrapper"]
# Thu, 25 Jun 2026 23:28:54 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:837b9d7bd4c8301d318ec8c5cd7e5aab81e392d60e90b733f39c67bbadc97aef`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 40.7 MB (40689274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a74b65654f4ba4ac8a14b9b8a1bd5463a6112e469d8e73f2c4d7e3a25303e6`  
		Last Modified: Thu, 25 Jun 2026 23:29:47 GMT  
		Size: 4.1 MB (4114126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ae69750a50785632cdf3b6f4800261ac817d732145d553e12dca8c41b46404`  
		Last Modified: Thu, 25 Jun 2026 23:29:47 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892d41dd03a580abecb88f1de0931f01b05a58e5e293da4358c2d2e2becca29b`  
		Last Modified: Thu, 25 Jun 2026 23:29:47 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adbb16a2fbd41d00a0cd325f3542caa1b8bd6bdaec806b47cac93381529e391`  
		Last Modified: Thu, 25 Jun 2026 23:30:02 GMT  
		Size: 676.9 MB (676930093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1756430c5a315a62cb4dd616d366b7b0ec0654d8b9866cbfc1902afc658a5d`  
		Last Modified: Thu, 25 Jun 2026 23:29:48 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02545147cff82a6590a98c35795706f2ead6646d97380e65d70b3ab5e2272a72`  
		Last Modified: Thu, 25 Jun 2026 23:29:48 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c62cebbcfa2f6dffbcd3f17f9e6b4f32109e0375cacdfbbe442878a33c7d5f`  
		Last Modified: Thu, 25 Jun 2026 23:29:49 GMT  
		Size: 75.2 KB (75185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4d772daaf80d2d4282eed7c385fab89c20cb68a3c9e86507cec1a31d5303a4`  
		Last Modified: Thu, 25 Jun 2026 23:29:49 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:dc58d257defce66fb3ee82751edf5d6e1e882dc919cd9dcad475ba3968a6a9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02462ad0b4307d3ff62c08551b3d4f257be021b9dcfff73ecf1bae8246d3ccca`

```dockerfile
```

-	Layers:
	-	`sha256:fdfedf5f1d5f23c4c67fe7cdff51019fc0786892f5b8e09aeb1c6140fb0b1c09`  
		Last Modified: Thu, 25 Jun 2026 23:29:47 GMT  
		Size: 2.1 MB (2089429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e347bcb7046faceb704872058bb49e73c0da8b8b133f7325a4e43037e8f8849a`  
		Last Modified: Thu, 25 Jun 2026 23:29:47 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:87daa0bbddf650005f4ae038a3a9ac086d8b42a4f146d545c57511351d87494d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565860373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94571f066286cf4c8e1ee4d41afd035851b6d093986c3b7565603ef2de55b808`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:52 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b536f0b76258d9997dadb73f000a4dcb4ac61a94c87f2002404cf80795af1987 in /      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:53 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:54 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:49:31Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:49:31Z" "architecture"="aarch64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:49:31Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:27 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:27 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 25 Jun 2026 23:27:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:27:27 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 25 Jun 2026 23:27:27 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 25 Jun 2026 23:27:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 25 Jun 2026 23:27:33 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 25 Jun 2026 23:27:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:27:33 GMT
ENV SHELL=/bin/bash
# Thu, 25 Jun 2026 23:27:33 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:27:34 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 25 Jun 2026 23:27:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 25 Jun 2026 23:27:34 GMT
LABEL org.label-schema.build-date=2026-06-18T10:10:50.114739011Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:10:50.114739011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Thu, 25 Jun 2026 23:27:34 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 25 Jun 2026 23:27:34 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 25 Jun 2026 23:27:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:34 GMT
CMD ["eswrapper"]
# Thu, 25 Jun 2026 23:27:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f224574d4b82cf6adf57df98fdab92768ce7f1579fbe0678919b872f4d435c0e`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 38.8 MB (38818113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf655b46e6e2ca6cab9e1c98664e1226e6d4e9de78a23171a167bd49a90d6d0f`  
		Last Modified: Thu, 25 Jun 2026 23:28:12 GMT  
		Size: 4.1 MB (4110045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c694a1bf7a6df0e7c4ea85f8f6de51b76e4ed42776b15c5b506ad93d6b14e70f`  
		Last Modified: Thu, 25 Jun 2026 23:28:12 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cef34e9b32a0125dc63540f29eb789efca1e522db533730b6c0ed0168ac812d`  
		Last Modified: Thu, 25 Jun 2026 23:28:12 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dac7720a08789166041cb20d47d36271b0645719b1e31a2b6ef301d7ea9359`  
		Last Modified: Thu, 25 Jun 2026 23:28:22 GMT  
		Size: 522.8 MB (522843765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d1da203a555e61d8a294bccb0d15bf7f5ed04f68d07ceb855f0ac1c77273e`  
		Last Modified: Thu, 25 Jun 2026 23:28:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00aa501684a6650c5ae6c896a553ff51894fd3c301d41356b0c5e9642ad97ef`  
		Last Modified: Thu, 25 Jun 2026 23:28:13 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dfabbeb60784cfbe66612651a85b91dafcaee1456e6ff6b18268f6e72b6b89`  
		Last Modified: Thu, 25 Jun 2026 23:28:14 GMT  
		Size: 74.1 KB (74104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a5a9f9ca9765bd2b05a74ecc0970c75a58a8c6d281097876c81d3bb61331d1`  
		Last Modified: Thu, 25 Jun 2026 23:28:15 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1b1cc51eabb1b25fe2c6f78a9d78e8040104a42106bc0e405fb60e9316d97706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe5dbc5489d3b4b36e16c092da592b7d21a0f2b7cbd824e09be4fe88be8dda8`

```dockerfile
```

-	Layers:
	-	`sha256:93a8ff1a7d90dbe4957827515215d6267cc5da6870f4f35f7fde7e7f343f75eb`  
		Last Modified: Thu, 25 Jun 2026 23:28:12 GMT  
		Size: 2.1 MB (2088209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b611efee48c232391179fb59df3de3bbebb2574e276c32c9e44b41e9a2539da`  
		Last Modified: Thu, 25 Jun 2026 23:28:12 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.2`

```console
$ docker pull elasticsearch@sha256:e182d810a437e30ad7d0221fc153910a06d9be5b05e57e59e7983467b89e41e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b80ebe31e5c0ceac8adc374d7df888f611789b66ab6f4f795b5c0e6a24f2eb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 MB (865111449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567a3bee336daff89a9435a047b687baac9479d1435aed487c91bdfd6a5e8a69`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:47:54 GMT
ENV container oci
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:a7d61486b18f71651e6d0b0c0267c96964cdf86a5c99a34dafc1bfd05eac4cc1 in /      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:47:55 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /root/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:47:36Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:47:36Z" "architecture"="x86_64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:47:36Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:27:22 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:27:23 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 25 Jun 2026 23:28:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:28:52 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 25 Jun 2026 23:28:52 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 25 Jun 2026 23:29:03 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 25 Jun 2026 23:29:03 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 25 Jun 2026 23:29:03 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:29:03 GMT
ENV SHELL=/bin/bash
# Thu, 25 Jun 2026 23:29:03 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:29:03 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 25 Jun 2026 23:29:03 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 25 Jun 2026 23:29:03 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Thu, 25 Jun 2026 23:29:03 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 25 Jun 2026 23:29:03 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 25 Jun 2026 23:29:03 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:29:03 GMT
CMD ["eswrapper"]
# Thu, 25 Jun 2026 23:29:03 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:837b9d7bd4c8301d318ec8c5cd7e5aab81e392d60e90b733f39c67bbadc97aef`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 40.7 MB (40689274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e39d9cbea175cb56405316dbf6ae0c91d1c285d1307fb6056584abc5fdf5f`  
		Last Modified: Thu, 25 Jun 2026 23:29:59 GMT  
		Size: 4.1 MB (4114137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b5fedbfc75c2ef05c05729eb4e7170df1c0ad7b35168808a8823cbae93e77`  
		Last Modified: Thu, 25 Jun 2026 23:29:58 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867e218737476b0f0c2a8e86744cce6670bfd9980778bec598fc4a961ec3e0d9`  
		Last Modified: Thu, 25 Jun 2026 23:29:58 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1cb771850896a5ae33e9fe032a818f240ec0365becc3574ca962918e38bee`  
		Last Modified: Thu, 25 Jun 2026 23:30:16 GMT  
		Size: 820.2 MB (820218074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062fb80e15e75af8d257e0ca1d59405852d49bc356fc043c51683af9dd02e152`  
		Last Modified: Thu, 25 Jun 2026 23:29:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed50eb89d242722a2739523775da5a6a39036644be2a9e2f20300ad390988ed`  
		Last Modified: Thu, 25 Jun 2026 23:30:00 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c3b782524716c25f90b61c295eab0ec399c418dbc9d0dba9a07bb09ce6ae6f`  
		Last Modified: Thu, 25 Jun 2026 23:30:00 GMT  
		Size: 75.2 KB (75184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f17e09faab5bed6e320a1bab40e94ae2ed5090a16aeb701c537f80a989c9e`  
		Last Modified: Thu, 25 Jun 2026 23:30:01 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:330de3b2e04972efc5905a64d6d56aff3189f0344953d05f0333696f54dd4ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d600535e6e46d8af8a086986494d4805bca27bbd132811ba0cb3822ed50f4236`

```dockerfile
```

-	Layers:
	-	`sha256:89a611a61edf03a8b805572d9aaa1f0bac9e7eb841d7c1fe1ae17a4c3befe9ce`  
		Last Modified: Thu, 25 Jun 2026 23:29:58 GMT  
		Size: 2.4 MB (2391051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8c2ee04d072bbbed2dd1bd9fcd4a0ea1cd036202070f281428638264b5a120`  
		Last Modified: Thu, 25 Jun 2026 23:29:59 GMT  
		Size: 33.8 KB (33773 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:2a51d5e464602ac97e340645ca2e972ea688723af776ac29ad48cdf11b0b9871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.7 MB (709714459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11944ec8c057c30e80cdddbf890452df469f9f1cb2787a1e269e5045f0dee88`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:52 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b536f0b76258d9997dadb73f000a4dcb4ac61a94c87f2002404cf80795af1987 in /      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:53 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:54 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:49:31Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:49:31Z" "architecture"="aarch64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:49:31Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:32 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:32 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 25 Jun 2026 23:27:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:27:47 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 25 Jun 2026 23:27:47 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 25 Jun 2026 23:27:55 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 25 Jun 2026 23:27:55 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 25 Jun 2026 23:27:55 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:27:55 GMT
ENV SHELL=/bin/bash
# Thu, 25 Jun 2026 23:27:55 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:27:55 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 25 Jun 2026 23:27:55 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 25 Jun 2026 23:27:55 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Thu, 25 Jun 2026 23:27:55 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 25 Jun 2026 23:27:56 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 25 Jun 2026 23:27:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:56 GMT
CMD ["eswrapper"]
# Thu, 25 Jun 2026 23:27:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f224574d4b82cf6adf57df98fdab92768ce7f1579fbe0678919b872f4d435c0e`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 38.8 MB (38818113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e350bc372d49717c84938414cc907e85efa30ebb7889b2fb850b4195ac9fb4`  
		Last Modified: Thu, 25 Jun 2026 23:28:42 GMT  
		Size: 4.1 MB (4110013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276e8da00eb20c75445baf33de0ca3c1e261611129613fb2dd08e6ebfb355ab5`  
		Last Modified: Thu, 25 Jun 2026 23:28:42 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe32a62f1d74a232cb1a91895c2134c2f6c4b0f02b3b90109fd0bd9cb7bc9dd`  
		Last Modified: Thu, 25 Jun 2026 23:28:42 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52f99d19969f1fca6748670f6a5bf3f3fe8cef5509c74ad27e3049c5be4af30`  
		Last Modified: Thu, 25 Jun 2026 23:28:58 GMT  
		Size: 666.7 MB (666697881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c1da03a38286fe001c31698de36c476764740a881c8b4eb81ebcd44a37b298`  
		Last Modified: Thu, 25 Jun 2026 23:28:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c7c67245a4706da4d186e8dfc1c6922b2251dc0fa504e710cf9466c994221`  
		Last Modified: Thu, 25 Jun 2026 23:28:43 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a27fe368816c32acdc3c1156835a5978d88e4ba3c4c6f92da75dd68ed31102`  
		Last Modified: Thu, 25 Jun 2026 23:28:43 GMT  
		Size: 74.1 KB (74104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d9fad58c6d41dbd04fbb8afbdfec3401321aff1684c70ef20d2be59026018d`  
		Last Modified: Thu, 25 Jun 2026 23:28:44 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4c90af4aa903cf7f50c5908ce323c3b9a168f5d043daca1d196f9169b7b6ca01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62abddf969f626cc26f55d6cc231a0760f787d87f8228c2f2c5bc373843943d`

```dockerfile
```

-	Layers:
	-	`sha256:b6c616dac98c60a133a4b713beff9d64198c80de23ec58631a0e6b7c9facc7dd`  
		Last Modified: Thu, 25 Jun 2026 23:28:42 GMT  
		Size: 2.4 MB (2389831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ddf3703892511cf607975c0ed325f2d347e1ab3ec9adcd70389d23602cdc09`  
		Last Modified: Thu, 25 Jun 2026 23:28:42 GMT  
		Size: 34.0 KB (33957 bytes)  
		MIME: application/vnd.in-toto+json
