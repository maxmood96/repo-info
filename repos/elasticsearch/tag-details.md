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
$ docker pull elasticsearch@sha256:1746375d49b80c75dd789022136dde1faf1283f3075725a05ac4afb839b5d8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:3b164b8848cd702672fb224d6584b44beaea2bc76e1a06498d0aa150234a5a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.8 MB (721804994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b659bdb20105c468bbcd0d99201f50a8c0b7b4fd2241176f68201945ab2a27dc`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:51 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:51 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 24 Jun 2026 23:06:38 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:06:38 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 24 Jun 2026 23:06:38 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 24 Jun 2026 23:06:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 24 Jun 2026 23:06:47 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 24 Jun 2026 23:06:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:06:47 GMT
ENV SHELL=/bin/bash
# Wed, 24 Jun 2026 23:06:47 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:06:47 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 24 Jun 2026 23:06:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 24 Jun 2026 23:06:47 GMT
LABEL org.label-schema.build-date=2026-06-18T10:10:50.114739011Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:10:50.114739011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Wed, 24 Jun 2026 23:06:47 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 24 Jun 2026 23:06:47 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 24 Jun 2026 23:06:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:06:47 GMT
CMD ["eswrapper"]
# Wed, 24 Jun 2026 23:06:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d7d73b5be9b2df07eed5962d9389d4aa59abe48d2acf4b4cff122d6498f554`  
		Last Modified: Wed, 24 Jun 2026 23:07:40 GMT  
		Size: 4.1 MB (4113808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450a7feda641adb102bafc808f55c2c7299a13f5d7d82060c6ae6f5b411a72e9`  
		Last Modified: Wed, 24 Jun 2026 23:07:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a3b039bad79d05b2fd0bc379e192be371cf644e60465d3d26fdfd2368ff1f`  
		Last Modified: Wed, 24 Jun 2026 23:07:40 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9f30321766749fac59d04a6f3f1097561906ad32b1f90c1559500cd9e868f9`  
		Last Modified: Wed, 24 Jun 2026 23:07:53 GMT  
		Size: 676.9 MB (676930084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa63e1eba7f17b52dce65853ab932254e02bb0c80a63847746e7465c1048ff21`  
		Last Modified: Wed, 24 Jun 2026 23:07:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc423e2935b43c480481e26a21e2cc9de0214388315d0f9bb71b445698f1742`  
		Last Modified: Wed, 24 Jun 2026 23:07:42 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ede7c6398d0573e9370591cdcc97f8cca76961c65a8d3681d45e129cc0b6404`  
		Last Modified: Wed, 24 Jun 2026 23:07:42 GMT  
		Size: 75.2 KB (75188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21008c62d31db02a5b3f362a740f680051bc2c65f84f6a746b0c567ca5aebfd0`  
		Last Modified: Wed, 24 Jun 2026 23:07:42 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8ab611c7774aebfaf35e21fbc88062dbceebf5383753b7c73149e9e495531e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921850967ace9163d3e15c268d0ddf09978a67ab1bf48f437709c57fb594f7ba`

```dockerfile
```

-	Layers:
	-	`sha256:011332a3df721e161d616e757bb15941fa2b735b29df25af39db08bd086e4d52`  
		Last Modified: Wed, 24 Jun 2026 23:07:40 GMT  
		Size: 2.1 MB (2089415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d05c775bfa86c2d87cd7d5b052732aa7647279081a789ed0972e1248da509c`  
		Last Modified: Wed, 24 Jun 2026 23:07:40 GMT  
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
$ docker pull elasticsearch@sha256:bf238b346eb3b5e561762e742de248df7cc330a678bb01c9957df3b790965e8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:88f19414dc95f19793778b921f91a7b5802eb1d62954d346a9070aba22cb0c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 MB (865092861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed30196a929098579308f70922034eb545c28abcb645f84af43521e5bf419c0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:52 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:52 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 24 Jun 2026 23:06:16 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:06:16 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 24 Jun 2026 23:06:16 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 24 Jun 2026 23:06:27 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 24 Jun 2026 23:06:27 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 24 Jun 2026 23:06:27 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:06:27 GMT
ENV SHELL=/bin/bash
# Wed, 24 Jun 2026 23:06:27 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:06:27 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 24 Jun 2026 23:06:27 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 24 Jun 2026 23:06:27 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Wed, 24 Jun 2026 23:06:27 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 24 Jun 2026 23:06:27 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 24 Jun 2026 23:06:27 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:06:27 GMT
CMD ["eswrapper"]
# Wed, 24 Jun 2026 23:06:27 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a89e60295ea4fba5265600753ffa5d9f23b46759dda725c70f3b7942e1fc34`  
		Last Modified: Wed, 24 Jun 2026 23:07:24 GMT  
		Size: 4.1 MB (4113674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b69f19d1ea78fc319f22223248de860e9a3db1c65ddd3d72dd587d8dde892e6`  
		Last Modified: Wed, 24 Jun 2026 23:07:24 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803306eac4553acb8c696d004c7b5b2bbfa95ff7064846fd6de002ea6ff9f129`  
		Last Modified: Wed, 24 Jun 2026 23:07:24 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5970818186afe545eb926401aa88022b96728b755cc5d561987b0716185851d2`  
		Last Modified: Wed, 24 Jun 2026 23:07:42 GMT  
		Size: 820.2 MB (820218098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976525127bea92631767b36a2d6dcd7259418766efe432cf99cf54fa39bc5794`  
		Last Modified: Wed, 24 Jun 2026 23:07:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482176bb31a22a3aac45edbb2f7f7543cc1ce217a0e612239df3d944b48004bc`  
		Last Modified: Wed, 24 Jun 2026 23:07:26 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fb49cc1a8af7d729c336d6380b9d158198b9b341eaad66077b8026f6e43d8f`  
		Last Modified: Wed, 24 Jun 2026 23:07:26 GMT  
		Size: 75.2 KB (75184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e111b6d0adb04ae114ad0557394a867da712f023fbfdf654f52572366804ac27`  
		Last Modified: Wed, 24 Jun 2026 23:07:27 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:16978d55bfd343ff4a17871e2f7194b71498724cbe82c55be9a7cf34fe1e85c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1448722bdc7c6032d00fb6ec5644ca2b594e0dd550cc7d7d91c7157070bfec0c`

```dockerfile
```

-	Layers:
	-	`sha256:3e15f9a0bb8c45e70ce3c5ce0fdb67c5f79fe871ead3e80108b9a69ac43793a2`  
		Last Modified: Wed, 24 Jun 2026 23:07:24 GMT  
		Size: 2.4 MB (2391037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ffaa6de101ec4ff658c265289ad363dd388732d6ba7e1605120c979e9567216`  
		Last Modified: Wed, 24 Jun 2026 23:07:24 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:25c70468471a75a044b1cf8e6bc569710d9b6d8d2728ae206adea87491b9f473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.7 MB (709709508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4e2f3709fa1253724f03d5c7f6ceb4f595cac22668ca2dace704df9233234d`
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
# Wed, 24 Jun 2026 23:04:06 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:06 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 24 Jun 2026 23:06:59 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:06:59 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 24 Jun 2026 23:06:59 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 24 Jun 2026 23:07:07 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 24 Jun 2026 23:07:07 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 24 Jun 2026 23:07:07 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:07:07 GMT
ENV SHELL=/bin/bash
# Wed, 24 Jun 2026 23:07:07 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:07:07 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 24 Jun 2026 23:07:07 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 24 Jun 2026 23:07:07 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Wed, 24 Jun 2026 23:07:07 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 24 Jun 2026 23:07:07 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 24 Jun 2026 23:07:07 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 23:07:07 GMT
CMD ["eswrapper"]
# Wed, 24 Jun 2026 23:07:07 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa5fac13f719da8bfc0b663d7e11ba21273fbe2ed71792908d573edeaa764b`  
		Last Modified: Wed, 24 Jun 2026 23:07:53 GMT  
		Size: 4.1 MB (4117199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a38b2fca235bdec5824e129f1c62a8bfec5c803abe0f2b5f67f8ef6aff5446`  
		Last Modified: Wed, 24 Jun 2026 23:07:52 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad64cf327ebcffcfe4b0fb5bd7d1cd59c5b6ad77354caafa8f8baaf14c89715b`  
		Last Modified: Wed, 24 Jun 2026 23:07:52 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce7eb1f33d574d23d736f413843a1afc060192e38bd739ac414e76e1ca5f05`  
		Last Modified: Wed, 24 Jun 2026 23:08:06 GMT  
		Size: 666.7 MB (666698029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8306c1df88c5e7a13d4ec8d146e0f598ad875e629bffceefa1623e0716ee4e`  
		Last Modified: Wed, 24 Jun 2026 23:07:54 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5e090e7f6fb9600378fbc79cb185d3ba0c04b609362a354ba78dfd45476ed1`  
		Last Modified: Wed, 24 Jun 2026 23:07:54 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bd7800edb1ff84b9ccb462109eafd7ef79a04b51af2dca0007a29e36fc06c5`  
		Last Modified: Wed, 24 Jun 2026 23:07:55 GMT  
		Size: 74.1 KB (74107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e498898c587c27c9ba2304d2a9ce1321918aef590eeddcf92350e0fd1dd4718b`  
		Last Modified: Wed, 24 Jun 2026 23:07:55 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1290e6bb7ebac8484b695f832afd59d18ff9099d134ada88e158590c5131ae09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08db891893a38f5e42da7ff63b03e3d5fc246f324eb96cd443cee4938066372f`

```dockerfile
```

-	Layers:
	-	`sha256:d5b5c3b68c8da1b6d984408a56e0f3df8cf07d090178731120d5868fea7352e8`  
		Last Modified: Wed, 24 Jun 2026 23:07:53 GMT  
		Size: 2.4 MB (2391599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b026278484e4284972d81d9344787d304ea33a377a063976959795e76634946`  
		Last Modified: Wed, 24 Jun 2026 23:07:52 GMT  
		Size: 34.0 KB (33957 bytes)  
		MIME: application/vnd.in-toto+json
