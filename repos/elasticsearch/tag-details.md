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
$ docker pull elasticsearch@sha256:da2c1769534f9b90ac5faa5584152a05d2972c5ffa9137fcff42b6b9d024ff84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:8217de4fd36a8f4e5fc7d776925501cf9fd3eb87237879365778fde67aeb8a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.8 MB (721816618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c2a5a6eede7321d3fea61a3c94a02cd5e4a9d3b05371f61c1230c5ec3df360`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:29 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:29 GMT
COPY dir:739d9f5e7f28cc70aad7ae94223fd7338511092b65f74c794a7b61ab61297289 in /      
# Mon, 29 Jun 2026 04:51:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:29 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:50:08Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:50:08Z" "architecture"="x86_64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:50:08Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:12:14 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:12:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 30 Jun 2026 00:12:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:12:57 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 00:12:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 30 Jun 2026 00:13:07 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 30 Jun 2026 00:13:07 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 30 Jun 2026 00:13:07 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:13:07 GMT
ENV SHELL=/bin/bash
# Tue, 30 Jun 2026 00:13:07 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:13:07 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 30 Jun 2026 00:13:07 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 30 Jun 2026 00:13:07 GMT
LABEL org.label-schema.build-date=2026-06-18T10:10:50.114739011Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:10:50.114739011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Tue, 30 Jun 2026 00:13:07 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 30 Jun 2026 00:13:07 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 00:13:07 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 00:13:07 GMT
CMD ["eswrapper"]
# Tue, 30 Jun 2026 00:13:07 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec749682792b418b3dc3d81ca98ddabd1ebb1043573a60a06cd67389ccaa38`  
		Last Modified: Tue, 30 Jun 2026 00:14:01 GMT  
		Size: 4.1 MB (4109715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c25803f222736acf5299fb08b551a17c6836677c0b1ee608f6282156af561e`  
		Last Modified: Tue, 30 Jun 2026 00:14:00 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabc6381d7e4ae2b5ec864f4055537723f88502a1a18e6fbbd7db6b82fad9ace`  
		Last Modified: Tue, 30 Jun 2026 00:14:00 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e852ce21476524d833c01949804846c75c627e7f55ec38127100ce564c4924a9`  
		Last Modified: Tue, 30 Jun 2026 00:14:14 GMT  
		Size: 676.9 MB (676930121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcccf37a8b268f2a022c1a8cb76c98c77a133d1548636ad4e7bb17c2945a133b`  
		Last Modified: Tue, 30 Jun 2026 00:14:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c705518226ed26ffc2e828333edd4d9d5ef1f8226e71b25ed30f742c016e457`  
		Last Modified: Tue, 30 Jun 2026 00:14:01 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7957fe4a908262cfd56d9040fe3f1aba8b0e35b4c663a95f8b2a7e72596da0c`  
		Last Modified: Tue, 30 Jun 2026 00:14:02 GMT  
		Size: 75.2 KB (75188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463e4588dafbb352c245c6901e52f88829d6555cfe09832122b684a949e517e`  
		Last Modified: Tue, 30 Jun 2026 00:14:03 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:75c6f1a694fced64d9c65f4b2b74be98e9db29c174d8e62bf0e37bbe9c98a2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1cd943f1d8220cce4800e3e8282d234e7d0f9886bf24dcb477f666b6612576`

```dockerfile
```

-	Layers:
	-	`sha256:c90e76833c530bed7ff3a2f53ffc6f4b4a78b5c4abd1535d6f66d100781ddae0`  
		Last Modified: Tue, 30 Jun 2026 00:14:00 GMT  
		Size: 2.1 MB (2089437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebed21ec2c9c6592eb289de0a5bbb712ce919b43a53dca390961bd482f32f1d7`  
		Last Modified: Tue, 30 Jun 2026 00:14:00 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:10cf69c1e35bc05fa7db59a5f9639ce025ffacd192ec068e84e441e50d03588c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565865057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d446bd55157934a274961d5d3c116151d526201e82eda090bb8b2090fb4842`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:52:40 GMT
ENV container oci
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:e6026d5a9734bc68758c885a994b1d95fd048fb5657a86e6b5e51129e847f4d9 in /      
# Mon, 29 Jun 2026 04:52:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:52:40 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /root/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:52:17Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:52:17Z" "architecture"="aarch64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:52:17Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:10:24 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:10:24 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 30 Jun 2026 00:11:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:11:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 00:11:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 30 Jun 2026 00:11:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 30 Jun 2026 00:11:26 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 30 Jun 2026 00:11:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:11:26 GMT
ENV SHELL=/bin/bash
# Tue, 30 Jun 2026 00:11:26 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:11:26 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 30 Jun 2026 00:11:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 30 Jun 2026 00:11:26 GMT
LABEL org.label-schema.build-date=2026-06-18T10:10:50.114739011Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:10:50.114739011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1f1ab65304a7633cd6511a1fa2b65c914064e724 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Tue, 30 Jun 2026 00:11:26 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 30 Jun 2026 00:11:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 00:11:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 00:11:26 GMT
CMD ["eswrapper"]
# Tue, 30 Jun 2026 00:11:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e3eac87d1d7580d5b8d38d78d1920a501fa6b200310444b0eb0a02af50fdde`  
		Last Modified: Tue, 30 Jun 2026 00:12:04 GMT  
		Size: 4.1 MB (4113490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3e2bb9add381ac74c152d87e8c81ea640ef1caeeeee53eef92e7bb1488b47d`  
		Last Modified: Tue, 30 Jun 2026 00:12:04 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269dcf18641f6b24d7ec44c26b9c47ac3ebb158cdb0b22a8e92d5c4c70917e3e`  
		Last Modified: Tue, 30 Jun 2026 00:12:04 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73912270f020a9f2c9d4753cda5cc0063a241ba97fd443868db4ee34080edf13`  
		Last Modified: Tue, 30 Jun 2026 00:12:16 GMT  
		Size: 522.8 MB (522843675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f5895701793a344e9b97fa981ccd1340ccc866ea343cec615933ae5dfa8cfe`  
		Last Modified: Tue, 30 Jun 2026 00:12:05 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9f588cebef054cfb41c2a10ce00a9acc77f5368c130740496317e89ca4b6b5`  
		Last Modified: Tue, 30 Jun 2026 00:12:05 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b7bac961f3712bcd3ccb67e80525331b21dedb246bdd9fc843e404abf1dd22`  
		Last Modified: Tue, 30 Jun 2026 00:12:06 GMT  
		Size: 74.1 KB (74105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9419f7578b3d797a019ee2f5a87be3a3f82bad366b10740204ecc527574cb0ed`  
		Last Modified: Tue, 30 Jun 2026 00:12:07 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9d61ca29ffba2404911e1cf7779b2b618d04ce4e9862e48ba5f9623a4fe7a41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e137fd5aaa08e261f11a03f0f31c76a54531959177c3536dc8ddb135f4bfca`

```dockerfile
```

-	Layers:
	-	`sha256:d4dd05028e7d070282c3529a513df098374acc6593111ff6d255560fd679189e`  
		Last Modified: Tue, 30 Jun 2026 00:12:04 GMT  
		Size: 2.1 MB (2088217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da41e1654a509855e6e075b460def298e13b1b74dd6b82ec0a59a244ed6104c5`  
		Last Modified: Tue, 30 Jun 2026 00:12:04 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.2`

```console
$ docker pull elasticsearch@sha256:63c772a9408727ffc53987304d12695c4863aa0e44a7bc2ab035037fba8195f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:da74579271b817c6b32a442ce2d7ee45aefdc15dc2e2ed5d05bf9e35f5a1a047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 MB (865104572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c270f751e11a8f21c67fad435837fd15479f4689d3503cf2b4dd9aa0e25fbbd2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:29 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:29 GMT
COPY dir:739d9f5e7f28cc70aad7ae94223fd7338511092b65f74c794a7b61ab61297289 in /      
# Mon, 29 Jun 2026 04:51:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:29 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:50:08Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:50:08Z" "architecture"="x86_64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:50:08Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:12:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:12:19 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 30 Jun 2026 00:12:52 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:12:52 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 00:12:52 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 30 Jun 2026 00:13:03 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 30 Jun 2026 00:13:03 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 30 Jun 2026 00:13:03 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:13:03 GMT
ENV SHELL=/bin/bash
# Tue, 30 Jun 2026 00:13:03 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:13:03 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 30 Jun 2026 00:13:03 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 30 Jun 2026 00:13:03 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Tue, 30 Jun 2026 00:13:03 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 30 Jun 2026 00:13:03 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 00:13:03 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 00:13:03 GMT
CMD ["eswrapper"]
# Tue, 30 Jun 2026 00:13:03 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60740e73de6d7a25e1b3b7dc70c0d01f38b34a53b807d6aefaff2d24d98f7fe`  
		Last Modified: Tue, 30 Jun 2026 00:14:01 GMT  
		Size: 4.1 MB (4109727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a8fea33d89f65f7e4e21c564efce1bbdb4ba5cdc7d0ccfd8844a32572dd330`  
		Last Modified: Tue, 30 Jun 2026 00:14:00 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a36b59205a514743cabb3a6522db255a7de831988d1d8d3c55146dd1a32fc4`  
		Last Modified: Tue, 30 Jun 2026 00:14:00 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59885f37eba7e25c7dd44fc40f013888244b5fb6d3862b2516ae09724e83f73`  
		Last Modified: Tue, 30 Jun 2026 00:14:18 GMT  
		Size: 820.2 MB (820218068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c609ae7357304b2e225e9aa825fa22e3fce65b725b3942b6212e1fe7f8aa6db`  
		Last Modified: Tue, 30 Jun 2026 00:14:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe87120808e9d4d535a76ec81e86638085c147044781c72b5a7798923c305ba`  
		Last Modified: Tue, 30 Jun 2026 00:14:02 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d32d554f29460242929cf4ff7681b4bfef62d0974d1e18244b64a1d4545d44`  
		Last Modified: Tue, 30 Jun 2026 00:14:02 GMT  
		Size: 75.2 KB (75186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712a7c9e1102f408de5e51a400749fc97a2d49d1470ad589c18577f109cb51c6`  
		Last Modified: Tue, 30 Jun 2026 00:14:03 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b26599a8e77c531ae02a7fc19c6e11b0831d323988fa60b2ef3347548e492235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3801f038dcb92f54a599f4957b7e0aa119d75533b2a4d24be9bb1ce1abf6ab`

```dockerfile
```

-	Layers:
	-	`sha256:cfcfda357a6d1f92a8e12f0c35dd45f5d21399e9291ff39bd58e0f38f078a038`  
		Last Modified: Tue, 30 Jun 2026 00:14:01 GMT  
		Size: 2.4 MB (2391059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be78721d254d7b77badd40b8696c42ba4ee76e5e465096466fb10770ebbf893`  
		Last Modified: Tue, 30 Jun 2026 00:14:00 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:0c49ff498f99b449b7b931f11c979ccfa66d4b14f8d18c8551640a1d5eeb2557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.7 MB (709719265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0d8221bb6e6cf0c4ac94d89825098265a2b63c11b5b0b026bba93ac591a453`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:52:40 GMT
ENV container oci
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:e6026d5a9734bc68758c885a994b1d95fd048fb5657a86e6b5e51129e847f4d9 in /      
# Mon, 29 Jun 2026 04:52:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:52:40 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /root/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:52:17Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:52:17Z" "architecture"="aarch64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:52:17Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:10:45 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:10:45 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 30 Jun 2026 00:11:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:11:47 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 00:11:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 30 Jun 2026 00:11:54 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 30 Jun 2026 00:11:54 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 30 Jun 2026 00:11:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:11:54 GMT
ENV SHELL=/bin/bash
# Tue, 30 Jun 2026 00:11:54 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:11:54 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 30 Jun 2026 00:11:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 30 Jun 2026 00:11:54 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Tue, 30 Jun 2026 00:11:54 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 30 Jun 2026 00:11:54 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 00:11:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 00:11:54 GMT
CMD ["eswrapper"]
# Tue, 30 Jun 2026 00:11:54 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a457d80a092773fd5393e3f2b58b0cec0fc0bc38efe2887cfac1add0497b64a`  
		Last Modified: Tue, 30 Jun 2026 00:12:39 GMT  
		Size: 4.1 MB (4113497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634a0d8eda0a977f4637f026d5b0058517b6c5bc4ecc92e2b1e5abb19928effc`  
		Last Modified: Tue, 30 Jun 2026 00:12:39 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf877a7d880808940bb095e5c29313a3702f77fa783b18cc5e8a435bc48706b`  
		Last Modified: Tue, 30 Jun 2026 00:12:39 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dba096faf6f39e721a80e47c4b76fa7b148b5b6511d63c12929aaa7c0902f9`  
		Last Modified: Tue, 30 Jun 2026 00:12:51 GMT  
		Size: 666.7 MB (666697876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cee12912f45154675650a86192c7385d0fed6aa86977551dc74bb5735bb5c1`  
		Last Modified: Tue, 30 Jun 2026 00:12:40 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcca38d77f9bd42a234884956619ccb104b5b56a12396fd176450396d935260a`  
		Last Modified: Tue, 30 Jun 2026 00:12:40 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381232fbaa3b728e0020b709348cc18e39f5b8218a88f1febde895a6c7b0fb9c`  
		Last Modified: Tue, 30 Jun 2026 00:12:41 GMT  
		Size: 74.1 KB (74102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97900965a65ee2e428fe0a22e1fac18a7d573068f6b9a223932a5dcb94a198c`  
		Last Modified: Tue, 30 Jun 2026 00:12:41 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9d45ba6c00f9a772839eaa4a3965d1de22d79aef3b6a13fe86051c4c40ded953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b731d2b3bc84d3090576cadbcbdbeebb53dc321606bf62fc335f6e3873af6981`

```dockerfile
```

-	Layers:
	-	`sha256:7528575f7b475571cfe999b5c34ae80dd1b074b631f59e7b9a31a37a35561ba6`  
		Last Modified: Tue, 30 Jun 2026 00:12:39 GMT  
		Size: 2.4 MB (2389839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a172304bb5678a6382482b698614f7fc5c3c1c8661be2085729b5dae92dd3211`  
		Last Modified: Tue, 30 Jun 2026 00:12:39 GMT  
		Size: 34.0 KB (33958 bytes)  
		MIME: application/vnd.in-toto+json
