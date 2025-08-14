<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.5`](#elasticsearch8185)
-	[`elasticsearch:8.19.2`](#elasticsearch8192)
-	[`elasticsearch:9.0.5`](#elasticsearch905)
-	[`elasticsearch:9.1.2`](#elasticsearch912)

## `elasticsearch:8.17.10`

```console
$ docker pull elasticsearch@sha256:244d140465f44f6d3f90af3afad5b5067a66b3b70e630cdeac74dab4eac68fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:077f0433aaced608ef146548457c3f4cfa6e3318929c2b3f9be982d35fdd9dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (677035638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e0b5cfb2093e0a4765f453c08cced709baadcd53260d3fc04b70fe771e0dd7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f42a288b966d9429e23c905375420984dcba3dfe113d8daffd0ff8031bf538e`  
		Last Modified: Tue, 12 Aug 2025 18:06:38 GMT  
		Size: 4.6 MB (4570929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f54b3080c699259d019a8b90cd41f6e1370f4636352638aa4d59d29dacb2d`  
		Last Modified: Tue, 12 Aug 2025 18:05:48 GMT  
		Size: 3.5 KB (3531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11762109912b06205c739918a4eba045ad520df1a0ab7ce64789fb0c9181d581`  
		Last Modified: Tue, 12 Aug 2025 18:33:39 GMT  
		Size: 642.4 MB (642446807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf79fa945cec7a70224bbe24e8d01a838ae1eb13cb7f3a0b6bed7b70bf2f74bb`  
		Last Modified: Tue, 12 Aug 2025 18:06:34 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd98ec9c9dc3d429b5e8444569d2be9f91a564cfc68a4fe95bf7200cd6f9439d`  
		Last Modified: Tue, 12 Aug 2025 18:06:34 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead110a2b5500c73256a9a1a72747b55055e8202d21d058f47d43b2b0b4e2241`  
		Last Modified: Tue, 12 Aug 2025 18:06:34 GMT  
		Size: 163.9 KB (163933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2e2364919b3d1c5029ede16447bb564360a0967a7725ef706556faaf8525b0`  
		Last Modified: Tue, 12 Aug 2025 18:06:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c76ca41070d4de2ec402eb09bafc13cf776bf145583dfa77ba0d67969a175`  
		Last Modified: Tue, 12 Aug 2025 18:06:36 GMT  
		Size: 115.5 KB (115540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8f48ed65ef30defaa33f3e435dc1757a59adf79d9d9d61e31abde398bc8cc755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376c27730df4699cf6b4d6fcae78bc077c0ba1a9fed5b08af16001987658e29d`

```dockerfile
```

-	Layers:
	-	`sha256:7045d83b0f9ed2b8c02d6ca0e4af41715ecd370c47e5d2a730ad46332d23fd24`  
		Last Modified: Tue, 12 Aug 2025 18:25:21 GMT  
		Size: 3.2 MB (3164781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6058a3c1ae0cc4d1c4f1519d564dd0d5848fcebab9c89a3339d0057b13481277`  
		Last Modified: Tue, 12 Aug 2025 18:25:22 GMT  
		Size: 38.4 KB (38396 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:483abccfb14266c40db9f48a05c49e6b11e595b652dd7df0a08b7fae4bde4b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.2 MB (521242908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be8d46c7ab6234b5f0120a83e78ee206235512f1c753db6688f1a3ea5ae3573`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac61f541f2874aaa66d823336c3abf67a79365936686e5c309259f31f2b7df`  
		Last Modified: Tue, 12 Aug 2025 18:43:13 GMT  
		Size: 4.6 MB (4577717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48678243c7c7792d915a1b08304001956ee7087b432e5b54d00003da282c6d36`  
		Last Modified: Tue, 12 Aug 2025 18:43:11 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c858693d1dd880402c6d347692606b6b022c8f2d792e3ecdf6f61fc64c22b9af`  
		Last Modified: Tue, 12 Aug 2025 21:28:51 GMT  
		Size: 487.5 MB (487514131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4e2088a65c92821c5e5346282191c7253e479768befddc0be078ca8db37747`  
		Last Modified: Tue, 12 Aug 2025 18:43:12 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406c4d51322605452bf539415b518331ac352291b3648a8a0ed77b5aed40fe0d`  
		Last Modified: Tue, 12 Aug 2025 18:43:13 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b34edd9b304ed4062c60f7cc2a6c3f85f4e3fe4ad919ccd7bd51c50e1cafa0`  
		Last Modified: Tue, 12 Aug 2025 18:43:13 GMT  
		Size: 160.4 KB (160359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f15b357e0a688c7f90bdfb145802870dad0fcf25d6fa386c52f198fb31075d4`  
		Last Modified: Tue, 12 Aug 2025 18:43:14 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf6b150b870ef747e376c3922a1104425fb94fe891835b293abab754935134`  
		Last Modified: Tue, 12 Aug 2025 18:43:14 GMT  
		Size: 115.5 KB (115539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:080993cba0411c0093535b8a23688525a1568954b78857169394761811352310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257bfbf6d7487559cce05949e0dedc395517ec9d27b3f97ea6cbbf371f2e6ced`

```dockerfile
```

-	Layers:
	-	`sha256:92ad1caa805096bfdf8bb501cd47ad9b6a3806f477424e24578975a70e6c9d57`  
		Last Modified: Tue, 12 Aug 2025 21:25:24 GMT  
		Size: 3.2 MB (3164565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d462f1d5fbe012e7b9e71b6970fcd6de2ca0676353af162aab74ee487e10f1c1`  
		Last Modified: Tue, 12 Aug 2025 21:25:24 GMT  
		Size: 38.6 KB (38599 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.5`

```console
$ docker pull elasticsearch@sha256:4aa7d5e353af37bbb9a03530c1d47ee705b54efeff193969afa90f09113dfb5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:ab7c11c8b63649e241f3ff377d3554653aebc41c14760dc94349acdbf5b25ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.3 MB (688273808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce52e7998a5217e00ff94ef7a248e3c5d010741e674b58869cac6f7380b8375`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T22:11:13.597825044Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1fe650052fafd984ded08146c77c6b71b7da7dec org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T22:11:13.597825044Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1fe650052fafd984ded08146c77c6b71b7da7dec org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ae5faf161f9e61d8224b9a6d4092a21dc358144708d78e5f1233ada4e0f2c0`  
		Last Modified: Tue, 12 Aug 2025 18:05:49 GMT  
		Size: 4.6 MB (4571026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f54b3080c699259d019a8b90cd41f6e1370f4636352638aa4d59d29dacb2d`  
		Last Modified: Tue, 12 Aug 2025 18:05:48 GMT  
		Size: 3.5 KB (3531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0493b4de35c1a61450d4285210924a4645b65b189bce2dc06ac82b3558b8336a`  
		Last Modified: Tue, 12 Aug 2025 18:32:46 GMT  
		Size: 653.7 MB (653684867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39753f4288719bc47ad9c974d6f6e4b1f691a2c29b2f395012bc68756de3781a`  
		Last Modified: Tue, 12 Aug 2025 18:05:45 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b44308797f321d166737ec3575aa7d7293d153f85559a107cb515d83fde0cf`  
		Last Modified: Tue, 12 Aug 2025 18:05:44 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ce592a971102eab0985100438d5d61c62c9d303be141d4532a9f7502cc5fb2`  
		Last Modified: Tue, 12 Aug 2025 18:05:46 GMT  
		Size: 163.9 KB (163938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d622f46e391e3e1fe3a728b9aac0ba14da2b03ba6ed2cafbafd8ddc97c551e`  
		Last Modified: Tue, 12 Aug 2025 18:05:46 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2cb1d47f9caef16096fa9f6776501081bee5330b1bc7093c949fcd5044730d`  
		Last Modified: Tue, 12 Aug 2025 18:05:46 GMT  
		Size: 115.5 KB (115544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8d8acfe9c6ba3aa1bce59acdb59f76c7552a62bb1581f501dd628e63e46cfaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3235875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020e48be155340836dce6b9009f01af5e5c1bf2f21106cd2a72e1688eb629cab`

```dockerfile
```

-	Layers:
	-	`sha256:13ff649c0886ea40a5b369e3234590d2b38b8fa0c7232e7902c46a7453cf9bb8`  
		Last Modified: Tue, 12 Aug 2025 18:25:26 GMT  
		Size: 3.2 MB (3197486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e332fcc7f7ac1491a9736973e9e7c1c7673a605732e3d1e95040d7020156f605`  
		Last Modified: Tue, 12 Aug 2025 18:25:27 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:6526d39b4fdb9b5de1838c5550e530aa297b7d42a27f67aa40a8bee4c9d777f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.7 MB (530657122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcf8331673874b1266acb0afdc53623624ae418358a57006bca9cb917b00005`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T22:11:13.597825044Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1fe650052fafd984ded08146c77c6b71b7da7dec org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T22:11:13.597825044Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1fe650052fafd984ded08146c77c6b71b7da7dec org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac61f541f2874aaa66d823336c3abf67a79365936686e5c309259f31f2b7df`  
		Last Modified: Tue, 12 Aug 2025 18:43:13 GMT  
		Size: 4.6 MB (4577717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48678243c7c7792d915a1b08304001956ee7087b432e5b54d00003da282c6d36`  
		Last Modified: Tue, 12 Aug 2025 18:43:11 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f21244a0305ea2d9d25d121bef96c3152ee9edb68bda2caeb22e34fd713008`  
		Last Modified: Tue, 12 Aug 2025 23:00:53 GMT  
		Size: 496.9 MB (496928336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98022fe4f333003afe2dca5b6c342d7125159a26031d9c30ff23ac5ed9493d91`  
		Last Modified: Tue, 12 Aug 2025 18:44:55 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35189f5390625f20e470a72a3f861bf36465dcf7912570e511f50e719f271c`  
		Last Modified: Tue, 12 Aug 2025 18:44:54 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c90056783fccec027338dcc2ebb547f44b5393e149784a1c5ab79b114291267`  
		Last Modified: Tue, 12 Aug 2025 18:44:54 GMT  
		Size: 160.4 KB (160369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bd613aa9a679d670188c11de1449c6046696a9b26aeec18079f16f09d200a5`  
		Last Modified: Tue, 12 Aug 2025 18:44:54 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb4040c50785816ea539e366f1b9b6e52d3a0fa76bcc2e225241d6006b9350a`  
		Last Modified: Tue, 12 Aug 2025 18:44:55 GMT  
		Size: 115.5 KB (115539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:82594065ff021c49f06f44a4f5682afe25703ed14724d997adf52ed934efc0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3236491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0416d864230ac091963bef72fd70a6eac915d88a6447e04f598fa90992df00`

```dockerfile
```

-	Layers:
	-	`sha256:333d4ca990c25cd300de3b3126a8ae3ef786eb1df62b077f407298153ea05bbc`  
		Last Modified: Tue, 12 Aug 2025 21:25:29 GMT  
		Size: 3.2 MB (3197899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c82215d661e48146348de088bfc3fd7b897f0c8eb2abed2ae809a636a8d476c`  
		Last Modified: Tue, 12 Aug 2025 21:25:30 GMT  
		Size: 38.6 KB (38592 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.2`

```console
$ docker pull elasticsearch@sha256:9ff5988b2ffbf38c3759f9fa3057a1147a716df12781d78b23aa160e1ec282ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:bb2753c105f3a883e11b48e1913ce47ca3a51c72d5fcc36b5430e6c93261af30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.0 MB (695023154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213d35ed0d0e670ada05426c212f854bb7d1a445dc5ceb37b37a2869d6ed59e1`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T10:07:54.721189302Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1c00e18ef14acd650768ff01f037eaede0c1f7b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T10:07:54.721189302Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1c00e18ef14acd650768ff01f037eaede0c1f7b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc5ca9c61278488f19e219929c00984b2de94f0ca16ca073f100e4da25728d7`  
		Last Modified: Tue, 12 Aug 2025 18:09:37 GMT  
		Size: 4.6 MB (4570983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2720ae5d3b6089b73f2dcd7f7c479e9983c5c0697a690924a6e79fad2ea669`  
		Last Modified: Tue, 12 Aug 2025 18:09:37 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e44b889f19ae8fa6a69ef39d5aed38333264d5bc2970cbdf59754b6937174ff`  
		Last Modified: Tue, 12 Aug 2025 18:31:01 GMT  
		Size: 660.4 MB (660434267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22d5bb56d077d1d1f74dc96668f476dd0bcc2177caa7163961c40cd2efc7a41`  
		Last Modified: Tue, 12 Aug 2025 18:09:35 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0f8e028866fc060d1f369ddce5047b19dab454ac91dc13cfbbb9b79070dd62`  
		Last Modified: Tue, 12 Aug 2025 18:09:35 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58443565ebdb3f2f4e1d65a80f5b234c9445258a42d85f58d456054d846313b1`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 163.9 KB (163934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fe47e12374ca45664179fbbdca7ed17f67c1b1691553c4a1d06c6c8f4fa90d`  
		Last Modified: Tue, 12 Aug 2025 18:09:35 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d811e05e29c3fec68f68055ad26116aba4484c8c81c4d1a59644baf4a33bf5c`  
		Last Modified: Tue, 12 Aug 2025 18:09:35 GMT  
		Size: 115.5 KB (115538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a0b5f0194d5c702e9e5409bf8cac9309e49958aeea4c79c12e2b59c32c765c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3255285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c873c82510be9ae19075b3cda603ab30259951b9623f2ec620216d34089b1aa7`

```dockerfile
```

-	Layers:
	-	`sha256:c9510e93c19249a5dd09b2f72cdc4f25f48f7fd13b3eb47823a8af564822704c`  
		Last Modified: Tue, 12 Aug 2025 18:25:32 GMT  
		Size: 3.2 MB (3218403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61afde129fb003142fd41837ff65e0f02e34f168deeb9df33d0957c94f519ea1`  
		Last Modified: Tue, 12 Aug 2025 18:25:33 GMT  
		Size: 36.9 KB (36882 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:68615edeb02071aed32639e719a120f1155d99d1779ccd960c70e1b78d216b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.4 MB (537399072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9441abf912766b3057ccd53846486cbf315dfb4b4406d5434b6b990fe330fde`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T10:07:54.721189302Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1c00e18ef14acd650768ff01f037eaede0c1f7b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T10:07:54.721189302Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1c00e18ef14acd650768ff01f037eaede0c1f7b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32607fb7c0c83ad992f61bab4b68553112f5fa0057b86385359f340125198f`  
		Last Modified: Tue, 12 Aug 2025 18:47:38 GMT  
		Size: 4.6 MB (4577723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1ed51a00341c73bea96daf1fc3c4dbc2cca0ddb75a0a867943556bd44a3219`  
		Last Modified: Tue, 12 Aug 2025 18:47:32 GMT  
		Size: 3.5 KB (3531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641fd1ef22064ed5a6a38ed9a19e09425f1f047c6e8e60b48e7aa03bdbf958b6`  
		Last Modified: Tue, 12 Aug 2025 23:22:15 GMT  
		Size: 503.7 MB (503670294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cec4c2a302bbc222959cf25192108523bf92b5d46fe1dee9ebdc9960e06e81c`  
		Last Modified: Tue, 12 Aug 2025 18:47:33 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f347e062332d36efe395ef2c608b00f1413b97fb728d42aef0962eab4371f0ed`  
		Last Modified: Tue, 12 Aug 2025 18:47:32 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e7ea24aa7bde11123dc210f5ba823a26e8186b1ea4553cc1f2a7d0a1825043`  
		Last Modified: Tue, 12 Aug 2025 18:47:33 GMT  
		Size: 160.4 KB (160354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562705cbfe08fb7b2027bae928997ca233d210f2cf647b98f8e0e42492e5f190`  
		Last Modified: Tue, 12 Aug 2025 18:47:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bddce535b2bf15cedf194702be0109c638159a973290b6ccac58b00c1e048e`  
		Last Modified: Tue, 12 Aug 2025 18:47:33 GMT  
		Size: 115.5 KB (115538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:abd54352678c10388d9fe4904c6aab939acb9a2a012f20022b43e000e6a36ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3255902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ccef16ed2070a90287474167f369211b54a37f41a36e8e29a325a84542eb72`

```dockerfile
```

-	Layers:
	-	`sha256:0ad8707cc5b21fe8cdb37b1de6c3f671d5c1c54d0c331f851502b00440530194`  
		Last Modified: Tue, 12 Aug 2025 21:25:33 GMT  
		Size: 3.2 MB (3218816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01d63f424238234f6d5973e06b24c94657b71d0fff91737ef79e7b5078b6be43`  
		Last Modified: Tue, 12 Aug 2025 21:25:34 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.5`

```console
$ docker pull elasticsearch@sha256:87bf6b28efa7625d8a1e285696086d8d5c24143947c443e4859dfc1ad5e4e895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:4dcf0ede9f7a35463de09983f47469c5e6d8ea93dfcd43a0fd6de2c651432480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.2 MB (700247807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353a37ba012272b782f23297ee76009bb85d66d904f7bb9c0b7309102f542c2e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:38:57 GMT
ENV container oci
# Thu, 07 Aug 2025 16:38:58 GMT
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Thu, 07 Aug 2025 16:38:58 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:38:58 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:38:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:38:59 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T22:11:00.741626477Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=abacf6d19441c06668da7264241312caee03cef5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T22:11:00.741626477Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=abacf6d19441c06668da7264241312caee03cef5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a9a82d55e373efe13158797dd6f98296c5a2207df8666919409f90687af496`  
		Last Modified: Wed, 13 Aug 2025 23:16:56 GMT  
		Size: 4.3 MB (4284275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9f4b3d1afd3d0181217a84ef904397fc11c2776fcfaad83c4b6a4cbd2c27f6`  
		Last Modified: Wed, 13 Aug 2025 23:16:56 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec8180c260bea2a69dab600a4deccbf9fe218301803381f50d066e1518504fd`  
		Last Modified: Wed, 13 Aug 2025 23:16:56 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4569734777202480898fdf87a2a7b0c15213503055f5fcda28fbda33d6597ff8`  
		Last Modified: Thu, 14 Aug 2025 01:24:13 GMT  
		Size: 656.2 MB (656221697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e46d8d20778897f688ee685ee7f1c692a103a67f817518e23a6f521c613c541`  
		Last Modified: Wed, 13 Aug 2025 23:16:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f24ced92468eda33f1a28c63a4165550275818d562757b2310dfec622daec`  
		Last Modified: Wed, 13 Aug 2025 23:16:48 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800b8ffb1c43322bda946a39e01c2e695d209ede33b378785cf4289ff60fb44`  
		Last Modified: Wed, 13 Aug 2025 23:16:48 GMT  
		Size: 75.7 KB (75746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e25803f16ee77a119660805e1a0c0eed602c1e23f9041c914126ded4bb2a5d`  
		Last Modified: Wed, 13 Aug 2025 23:16:49 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c8e8104e51eeec80aa63196ae4bcd63e9537cbe8c3c2d455bb13a026eb05cd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2067638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75977d4429d3a1622231931adfb6d5687d0470fa95ed52936c9b0234cec9ffd`

```dockerfile
```

-	Layers:
	-	`sha256:19c29cad88fd78b35a6b7dda3f4edf95c3ee40cdae7bf37eb06651865189cfc8`  
		Last Modified: Thu, 14 Aug 2025 00:25:18 GMT  
		Size: 2.0 MB (2033799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d63e70f18eeba04ca0d8ed129962dcea0bb52953cd042fe135fbbaefad3b4f5`  
		Last Modified: Thu, 14 Aug 2025 00:25:19 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c99985dd0784e6ae8c3a36a40007bcfaf41218ac20171f82defc7ee597f2eff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.7 MB (538666798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb3ed02952a0dadcbde404a75813aebbc9d3d4c8d77163e748dbf72a4fe15d7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:43:47 GMT
ENV container oci
# Thu, 07 Aug 2025 16:43:48 GMT
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:43:48 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:43:49 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T22:11:00.741626477Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=abacf6d19441c06668da7264241312caee03cef5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T22:11:00.741626477Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=abacf6d19441c06668da7264241312caee03cef5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ae68ff313f78851fbf66137c0a49a327986447045fa7f2497adbc1b57f88db56`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.8 MB (37819116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75308d0ac5a425abed1f8819eb37d4ab57057319595017b63eecce3b4e16eab9`  
		Last Modified: Thu, 14 Aug 2025 09:32:04 GMT  
		Size: 4.3 MB (4292602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a31db30e452e162a036d85d481ff184571e4963d31acf433f52ef7994e94bd`  
		Last Modified: Thu, 14 Aug 2025 09:32:10 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bc1f91f1c0eb0d239f3d471e4997e1ab3bf3ee338a875cb2832dd7fb88afec`  
		Last Modified: Thu, 14 Aug 2025 09:32:14 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d25eff9b4b0a311457b0e021d4e735681ad025c7cdcb013a5eb58c19fb2ead`  
		Last Modified: Thu, 14 Aug 2025 16:53:06 GMT  
		Size: 496.5 MB (496466083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99ef1a74262d823fdc0080f010a46c6aea7d38f627f8209fb6ea2c07f31171`  
		Last Modified: Thu, 14 Aug 2025 09:32:18 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37408bd8cf57a0f41fffbf1b3eaa53ac7803d448c31a67f35c43d192041ce40`  
		Last Modified: Thu, 14 Aug 2025 09:32:21 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8b6858e60c84c181d226f8d41e6a5291469ebcdbf172662882b118e6e1de01`  
		Last Modified: Thu, 14 Aug 2025 09:32:24 GMT  
		Size: 74.6 KB (74641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bc70029f7b41f7c43de8d2bdac6d7669628883f46dcff9b1bff9d5d4c8b210`  
		Last Modified: Thu, 14 Aug 2025 09:32:28 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:82f1886b119e078192962d9b3cad19e29bf6696d504fae5bf2d64c045067c2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94f39f3a78a0220cfd7ea7eb1b104832a42b98212b671303fa77cf5c3808653`

```dockerfile
```

-	Layers:
	-	`sha256:f8ade9f26be29d68cf6e38fa1659002172ed92fcf41482c0d02d24075fd1ff09`  
		Last Modified: Thu, 14 Aug 2025 12:25:22 GMT  
		Size: 2.0 MB (2034363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2bc49a5dd507be4eec5fa9c505e02ece7897f299b1d5c19b03134bc7196cc6c`  
		Last Modified: Thu, 14 Aug 2025 12:25:23 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.2`

```console
$ docker pull elasticsearch@sha256:b1c50fb8d09ea8486c6422e3c5a0d48c97b931bf2dbc42c5321081845f1ff449
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:28cd5d8cee38b04536640b20267766e1acf9dc798d4270cdc37923e650da6177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.3 MB (715268417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cb4874c5fe692cc81275353bf95cfa4f42c0e12de139a6de73cf73514278ed`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:38:57 GMT
ENV container oci
# Thu, 07 Aug 2025 16:38:58 GMT
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Thu, 07 Aug 2025 16:38:58 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:38:58 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:38:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:38:59 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T15:04:41.449624592Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ca1a70216fbdefbef3c65b1dff04903ea5964ef5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T15:04:41.449624592Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=ca1a70216fbdefbef3c65b1dff04903ea5964ef5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e839ea5017600067984f33322c723fbb2926d3882004507f1bbf54bde509d26e`  
		Last Modified: Wed, 13 Aug 2025 23:16:27 GMT  
		Size: 4.3 MB (4284249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b264f1dd030f83cebefe2c2d44c015386cec5d3ebca456d8b05e30f83ea65b`  
		Last Modified: Wed, 13 Aug 2025 23:16:29 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f57a6b9768a9d9f33b59ee12d25e9e66ae920a01acadfd6b74f25a52ba315`  
		Last Modified: Wed, 13 Aug 2025 23:16:30 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd0d9c3f650dce723f8144caf690c5d64634d2b8d2ff5cea8af66ffc8433290`  
		Last Modified: Wed, 13 Aug 2025 23:16:42 GMT  
		Size: 671.2 MB (671242325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ef43482de7c2b8eddf13848a69831588f5c8616fe938acca6201e563adc6d`  
		Last Modified: Wed, 13 Aug 2025 23:16:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d24bec251d2a91b3f1d977e87c2e6bc8091f7ae8faacaa6fcd65606277b211`  
		Last Modified: Wed, 13 Aug 2025 23:16:31 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080987e4afe9971e4cc2added74c21b1e593ab4ac9aeff3ddd2e489fae14391b`  
		Last Modified: Wed, 13 Aug 2025 23:16:31 GMT  
		Size: 75.8 KB (75751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73b5cae8d3877b510a546bd2785482ce7a83fa0bd0214eae70722db19836424`  
		Last Modified: Wed, 13 Aug 2025 23:16:31 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a0183a53aad1bcf061099d1bffe4eba95d3158fc9f844da02ea2a19dc0df4d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd5a141a02fca4a6f73cd9b749bef0622f42eb5260d1250a63881c811d0d7bc`

```dockerfile
```

-	Layers:
	-	`sha256:eefdff54942f1fe0f81378fb9ab326ea95a28c6e397bf43156912bdbd839bff9`  
		Last Modified: Thu, 14 Aug 2025 00:25:25 GMT  
		Size: 2.1 MB (2088158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e67e509981eb73981026f93bfc940abcaafb4c7e1450b164474872f337377d4`  
		Last Modified: Thu, 14 Aug 2025 00:25:26 GMT  
		Size: 33.8 KB (33838 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c87bb3d9f66a7da42bdfba55571cc80f3a5cc908bf865f7bf89475b365ecc70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553689617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc8903e8ff5e503355d6ad230767f79beb6e5803348dac8370f501d82113897`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:43:47 GMT
ENV container oci
# Thu, 07 Aug 2025 16:43:48 GMT
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:43:48 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:43:49 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T15:04:41.449624592Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ca1a70216fbdefbef3c65b1dff04903ea5964ef5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T15:04:41.449624592Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=ca1a70216fbdefbef3c65b1dff04903ea5964ef5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ae68ff313f78851fbf66137c0a49a327986447045fa7f2497adbc1b57f88db56`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.8 MB (37819116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75308d0ac5a425abed1f8819eb37d4ab57057319595017b63eecce3b4e16eab9`  
		Last Modified: Thu, 14 Aug 2025 09:32:04 GMT  
		Size: 4.3 MB (4292602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a31db30e452e162a036d85d481ff184571e4963d31acf433f52ef7994e94bd`  
		Last Modified: Thu, 14 Aug 2025 09:32:10 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bc1f91f1c0eb0d239f3d471e4997e1ab3bf3ee338a875cb2832dd7fb88afec`  
		Last Modified: Thu, 14 Aug 2025 09:32:14 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4869bb9b167e08c65346669fb520edbcbab6cd411726218a7368e9f32257fd3`  
		Last Modified: Thu, 14 Aug 2025 10:13:15 GMT  
		Size: 511.5 MB (511488901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54526b76acad0ae919e49d329185c7aae4648c7832ab8f6b88f4b574caf9b504`  
		Last Modified: Thu, 14 Aug 2025 09:23:31 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deea1a1365f5633f157152174d6e1ea9902e7a98e38dbcfd9d5d59c49b8e2283`  
		Last Modified: Thu, 14 Aug 2025 09:23:31 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc545d601f3c957ff588d4ae10dddb3ddc90cc512e323607d78f5f90b2136419`  
		Last Modified: Thu, 14 Aug 2025 09:23:31 GMT  
		Size: 74.6 KB (74642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df57e2ccea6c05ae9a576d4bd7619c15d20f353bd7922944ff78ca3b60625bb5`  
		Last Modified: Thu, 14 Aug 2025 09:23:31 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2441565d97d721d1d309be99e6979d63d430651f61ff8e7ffb2e050fe7a2391f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca439369cf1fb08120a09a2d978bc4c1ea3e0fc1ed4fae74412003a0a514e6c`

```dockerfile
```

-	Layers:
	-	`sha256:bf4c066df5343af043d69fcf50ff74ead696d3f56709723898b55ccd6f1510c8`  
		Last Modified: Thu, 14 Aug 2025 12:25:26 GMT  
		Size: 2.1 MB (2088722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df67b779fd1a788a91c55df8b7bb05e46ee65c2b4753903baebd427b8292a8b0`  
		Last Modified: Thu, 14 Aug 2025 12:25:27 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
