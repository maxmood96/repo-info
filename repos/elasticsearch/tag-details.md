<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.18.8`](#elasticsearch8188)
-	[`elasticsearch:8.19.10`](#elasticsearch81910)
-	[`elasticsearch:9.1.10`](#elasticsearch9110)
-	[`elasticsearch:9.2.4`](#elasticsearch924)

## `elasticsearch:8.18.8`

```console
$ docker pull elasticsearch@sha256:e5b3511e96ee1c58e9027d9d06185be4e627074717b40f6145e860b39c851d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:35ecc9ceafc87e7e60973f820793db03c21af60410daea2b4b8b6f192e06a5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.4 MB (699422102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc452320d24ce506503a786fbb099915ccfda188e38dc39ee9a02e904db4356`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:24 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Nov 2025 23:22:25 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:22:25 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:22:25 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Nov 2025 23:23:55 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:23:55 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:23:55 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:23:55 GMT
ENV SHELL=/bin/bash
# Thu, 13 Nov 2025 23:23:55 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Nov 2025 23:23:56 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:56 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Nov 2025 23:23:56 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Thu, 13 Nov 2025 23:23:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:23:56 GMT
CMD ["eswrapper"]
# Thu, 13 Nov 2025 23:23:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c43ef599f7a98ef31360bd3771828770c70193f3b08e03430ff63352d1879c8`  
		Last Modified: Tue, 13 Jan 2026 01:54:46 GMT  
		Size: 4.5 MB (4493909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f7b345db94a1a2c86c7e241bac630afd7c708a4540a5db8ca5523ac1da61e`  
		Last Modified: Tue, 13 Jan 2026 01:54:39 GMT  
		Size: 3.5 KB (3534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d27b11736af81fe4f0c3b5bee6534722ce2b0f084588d47dad6966c0aa4a6a1`  
		Last Modified: Tue, 13 Jan 2026 03:05:46 GMT  
		Size: 664.9 MB (664908814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b46a367471c93768bfac25f1547059ab2f1bd1d200cd2dd370fa11b9b2cc37`  
		Last Modified: Tue, 13 Jan 2026 01:54:50 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c0aa5ff83b648b37592a0d6e8d0e888650d97e71e606cd607eb29692d0518`  
		Last Modified: Tue, 13 Jan 2026 01:54:54 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41db951a09358077109950cd0cfb24fbec2a7dc5690e9175a388b6d00fcd5089`  
		Last Modified: Tue, 13 Jan 2026 01:54:56 GMT  
		Size: 163.9 KB (163935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff2aa099f19d62676a29e3ec7f8b2874349672def2cf3b834fffea50c6e4ae`  
		Last Modified: Tue, 13 Jan 2026 01:55:04 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b1972ad4e20e050b4102887185fea470d4215100c4aba3d82cb6fb1e637812`  
		Last Modified: Tue, 13 Jan 2026 01:55:05 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d0daf70580c4cba91cdd0ed4c6cd71677db0c923a8027ba4b75aada7a6a2f4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae5830d902bc2d758204867320ea83541a43eb19bb1fa7696bccf0881186a96`

```dockerfile
```

-	Layers:
	-	`sha256:9995af78231b89816a76739c50ba1f806a2cc015d6ae90cf0842586906d04931`  
		Last Modified: Wed, 14 Jan 2026 08:05:52 GMT  
		Size: 3.2 MB (3192944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436e294639573790ef3eb79fa2513fd3c74f12f8bc626acfdb13396b89cfdca8`  
		Last Modified: Wed, 14 Jan 2026 08:05:31 GMT  
		Size: 38.3 KB (38346 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:488365ccd5c96cc323443fb11f05caa6f38a92478f0ed0d20720e8ceef06b533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.7 MB (541654815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e5c1d0847c150e67ed3e57c8b83555a6f7f8a8cc7c205333eefa45f3a239f3`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:07 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Nov 2025 23:22:07 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:22:07 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:22:07 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Nov 2025 23:23:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:23:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:23:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:23:12 GMT
ENV SHELL=/bin/bash
# Thu, 13 Nov 2025 23:23:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:12 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Nov 2025 23:23:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Nov 2025 23:23:13 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Thu, 13 Nov 2025 23:23:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:23:13 GMT
CMD ["eswrapper"]
# Thu, 13 Nov 2025 23:23:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc64f53563943fb470824b87140561802dd52d43f4628eb68bb7fa8f57a0b5db`  
		Last Modified: Tue, 13 Jan 2026 09:06:12 GMT  
		Size: 4.5 MB (4498895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f44bc7b0af09b3a694a152f1433649cc2cbeb6f770e442b41bec589997f56`  
		Last Modified: Tue, 13 Jan 2026 09:06:11 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9728459a5a3f4abb547584c07ae44961768661babd029b4713cb12ae80e9924`  
		Last Modified: Tue, 13 Jan 2026 09:06:39 GMT  
		Size: 508.0 MB (508003274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d526010e9271cf1fa50c3ce58b45edc2baeb72f63c9103694e37f4077e63a15`  
		Last Modified: Tue, 13 Jan 2026 09:06:11 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f26d3872bef9a883c14b822ea082a9dbe814100cdcb33e6651be5133102f3a6`  
		Last Modified: Tue, 13 Jan 2026 09:06:11 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e542b2865e2c21d02b52969930d99a03a04fe759cdd4f2d2ce726640d3d37bdb`  
		Last Modified: Tue, 13 Jan 2026 09:06:11 GMT  
		Size: 160.4 KB (160368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c191344f90bbd2a51a6f8d0bab30596843eca8331bfbc68310678792d9bba0b9`  
		Last Modified: Tue, 13 Jan 2026 09:06:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057047f0e243f23a7af94bfd9a04e48c031c234ab097c42fb5345c01e0f4f118`  
		Last Modified: Tue, 13 Jan 2026 09:06:11 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2c61bcff8d19e16d5e371f6d67e44c05122a20062a9bc9497c13d439273794c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c2c1559c8e3e5b599c799acab4da7a6849233e298853011329c3bf143ef2d8`

```dockerfile
```

-	Layers:
	-	`sha256:7be2357a91cb793fac5a7b45556077661c810924e084b5530d9a0af487cc5806`  
		Last Modified: Tue, 13 Jan 2026 12:15:11 GMT  
		Size: 3.2 MB (3193357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b82cbadcba6dca71ecc5d86882b31ebb377b61b1f4ba16d2605bc675a987df`  
		Last Modified: Tue, 13 Jan 2026 12:15:10 GMT  
		Size: 38.5 KB (38548 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.10`

```console
$ docker pull elasticsearch@sha256:47a4f9ebbfec455950cfebf54694e2352bcd73d3c147b0f8731d4e1530a632bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2703b052b6490b37e29330fd3cdaf502de5c8dafb03249eeaa93a28d5c70d772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.4 MB (712350854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2738464e6e1d67de4e35ef5d02f240ce24b46c1e170419fa10c6e0ce40f6de20`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Jan 2026 19:04:27 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 13 Jan 2026 19:04:28 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:04:28 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:04:28 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:11 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:11 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:05:11 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:05:11 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:05:11 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:05:11 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 13 Jan 2026 19:05:11 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 13 Jan 2026 19:05:11 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:05:11 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:49.939644068Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=493241b351be6d9f40d52a1406c91a23b4148821 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T22:07:49.939644068Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=493241b351be6d9f40d52a1406c91a23b4148821 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Tue, 13 Jan 2026 19:05:11 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:05:11 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:05:11 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e5c72c4246f421c91991379f585b3ad2c8b8fff2b333ef0f75d666f3d99b61`  
		Last Modified: Tue, 13 Jan 2026 19:06:39 GMT  
		Size: 6.8 MB (6845540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c482c1352ee5615b2ed44c6a5fa261f04aa6d69adb11e7607049fae12cdb0024`  
		Last Modified: Tue, 13 Jan 2026 19:06:39 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc6b8fadd2bbcd9dce0539be05bb07fc6dac7740512215b2052f6fc394f1d45`  
		Last Modified: Tue, 13 Jan 2026 19:09:38 GMT  
		Size: 675.5 MB (675485941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd315a1d920d08535756d56a5b07a44360c63a6a0440d402b144ff422b06de7d`  
		Last Modified: Tue, 13 Jan 2026 19:06:40 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efedb449a7ef5108e9401e58d06205e7d7a9269d54b1c3433086f162f81e3e9`  
		Last Modified: Tue, 13 Jan 2026 19:06:39 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299d938e0413ffb3b41cc824b890a0ca527e80bdb00650b772430f3fd1f5da58`  
		Last Modified: Tue, 13 Jan 2026 19:06:39 GMT  
		Size: 163.9 KB (163936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e13484e83c1909905078b38924c09f730c798ee6f6e83fafdd3af3e3fda9d50`  
		Last Modified: Tue, 13 Jan 2026 19:06:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71542cd587bb7e013a3e85c8425a4de9e2bbbc165a0a6b9c8fb75d3bdf88a47`  
		Last Modified: Tue, 13 Jan 2026 19:06:45 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:7716380285f870700ba5a5b8f830cb74f2bfbf4789d34217e50bd968a8ba95b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7da90b825ba66b836f985165c5ed227a4622744e462082d244ee566166927b`

```dockerfile
```

-	Layers:
	-	`sha256:d633849c408cad91849d64545c7740d80cf827553326e51d8df96db560e938ff`  
		Last Modified: Tue, 13 Jan 2026 21:00:48 GMT  
		Size: 3.2 MB (3210136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02429fdb58bc904d985401fc030c2facbc6c98377c0404bb08362bf61ca7b5ec`  
		Last Modified: Tue, 13 Jan 2026 21:00:50 GMT  
		Size: 36.8 KB (36847 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:225c142ff0d2592143cc0dd8b79e2fe3d6aa582009051565a65db50f331f033c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.2 MB (560219900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1aab5d3305a86aedf4c155b01fcb8ac93120de1e103c0e414182e4effbb170f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Tue, 13 Jan 2026 19:04:15 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 13 Jan 2026 19:04:15 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:04:15 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:04:15 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:00 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:00 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:00 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:05:00 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:05:00 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:05:00 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:05:00 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 13 Jan 2026 19:05:00 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 13 Jan 2026 19:05:00 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:05:00 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:49.939644068Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=493241b351be6d9f40d52a1406c91a23b4148821 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T22:07:49.939644068Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=493241b351be6d9f40d52a1406c91a23b4148821 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Tue, 13 Jan 2026 19:05:00 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:05:00 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:05:00 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18223c03726e25778a9cb18858a70943036e6f80ab03e2d93b0f5643bba6bde0`  
		Last Modified: Tue, 13 Jan 2026 19:06:12 GMT  
		Size: 6.9 MB (6914986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496ccd796ed15f66046991ae2c66b246382e9b1f1b68e3cb137523d4bbaa8c6`  
		Last Modified: Tue, 13 Jan 2026 19:06:11 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21430913bf6a0975553f5ebf3d79a7d5ab3c8c9d8701b4481f4e0e0db39338bc`  
		Last Modified: Tue, 13 Jan 2026 19:08:18 GMT  
		Size: 524.2 MB (524152283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8702781ab191dacd5504208f5a6a44e200c1b3155219a8a29942a032bd3070`  
		Last Modified: Tue, 13 Jan 2026 19:06:10 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2267f389292c43c3faacfcd6ddc06c130d8d96b34c0280218d810a8226f1dcb6`  
		Last Modified: Tue, 13 Jan 2026 19:06:11 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4c7acb886ed4da528f5ec5f5eed4b18b4efae4afdae67073f221409f4cd7b6`  
		Last Modified: Tue, 13 Jan 2026 19:06:11 GMT  
		Size: 160.4 KB (160360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8b828da5d52b711c42992611b4cd0b9b543d43deea333e3d95c91189580b31`  
		Last Modified: Tue, 13 Jan 2026 19:06:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d648cb43691b8db77704963e60821e81990155e6ed3d45d55ff8b139011d64`  
		Last Modified: Tue, 13 Jan 2026 19:06:11 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:edc457c8ea8f14a364461d5f7f89cd316ad55054515583e4591aa9963e91fea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3247598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52fd4d051e7ca78618d0cf7fbc40caf48f1fba1cbd263a208f9b5661682947c`

```dockerfile
```

-	Layers:
	-	`sha256:a2156e867c03d916e2d3d86d57c47126e7c9afc22843f4ce3856a3df9ca50a29`  
		Last Modified: Tue, 13 Jan 2026 22:25:23 GMT  
		Size: 3.2 MB (3210549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b7abc0ae6b1c330cb8186ab9abc0d149a44b1c6db5abed5097095254f1238f`  
		Last Modified: Tue, 13 Jan 2026 22:25:23 GMT  
		Size: 37.0 KB (37049 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.10`

```console
$ docker pull elasticsearch@sha256:d3eee558a27908ecbab13abe2c7a2da3916d82dd72059bcd4fa30db047f9def3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:074cf8dbaf38c21d1c091ed9cd74e1e05e055b6ef5da03df238504f5061a45d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.7 MB (730679535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8c2e353225161ffd82f10fda527bb68b96d5e837557ee5952a95b98419f089`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Tue, 13 Jan 2026 19:04:49 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:04:49 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:05:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:39 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 13 Jan 2026 19:05:39 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 13 Jan 2026 19:05:39 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:05:39 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:05:39 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:05:39 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:05:39 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:05:39 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 13 Jan 2026 19:05:39 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 13 Jan 2026 19:05:40 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:05:40 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:05:40 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:05:40 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e23f2204869bf926ac63b7d410dad1857f33da172f2d98b2a0b7e94f868fd1`  
		Last Modified: Tue, 13 Jan 2026 19:07:03 GMT  
		Size: 4.3 MB (4286930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d8823ef737cc217b99af433fdbb9eef9c194d322de487ce0340bc0b70cb6d7`  
		Last Modified: Tue, 13 Jan 2026 19:07:03 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75ec7e84981720a5c06beea4be6d44c1d3597bbdc477fca5d82196def0bd877`  
		Last Modified: Tue, 13 Jan 2026 19:07:03 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d168b0c63937f5028b69536c9dbe05759a406bcb1abc0e011456df0983419e6`  
		Last Modified: Tue, 13 Jan 2026 19:06:45 GMT  
		Size: 686.3 MB (686261903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746896185b691a6f8363079f29e59e070d5e040f6012d2951e82c4f5754f853`  
		Last Modified: Tue, 13 Jan 2026 19:07:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae8f92750e63523f31551a2cbf8e9e89b5d0a27bd0c12a58e1bb2f9b56d4b9`  
		Last Modified: Tue, 13 Jan 2026 19:07:03 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720a7bf8671812088c8bb58cb7042c43c318fefee2b67cc357250bee552bc595`  
		Last Modified: Tue, 13 Jan 2026 19:07:06 GMT  
		Size: 75.2 KB (75174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847482ebfea8d6fd8dc6b69b0af54a29a0e51e7693612cdbb1d0d1e7fa0c1649`  
		Last Modified: Tue, 13 Jan 2026 19:07:04 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:de81f30410fe8e436f7ab9608c29acc2020ea5cb8c709dd732f35dbfd26bc6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2cf6f5f01e394064c2985f6277f4846e1452b50eb204369e900dd9d478fc28`

```dockerfile
```

-	Layers:
	-	`sha256:d6f23ae1086f0f56481ac7b89aa7b3f1b3f8997322f168621c803bec5186be7a`  
		Last Modified: Tue, 13 Jan 2026 22:25:28 GMT  
		Size: 2.1 MB (2085720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88dbbf076513e616497b9c8eee42b5fec44f7d082952dc4a9f501da89b71ac78`  
		Last Modified: Tue, 13 Jan 2026 22:25:29 GMT  
		Size: 33.9 KB (33867 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:82a9f9951003b0ca40133589139d48622c74e6770112353eb6cb14f64ae0fa14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574629696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89daa3df089b833e2d13533923cfa69661b6205f90300f8e5dd6e72a071708b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Tue, 13 Jan 2026 19:04:56 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:04:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:31 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:05:31 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:31 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:37 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:05:37 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:05:37 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:05:37 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 13 Jan 2026 19:05:37 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 13 Jan 2026 19:05:37 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:05:37 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:05:37 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6eef4c50ba658394d871753e7b16d95d7f180af70fccbe59fa16350651bcc`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 4.3 MB (4298172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4feb70d22c28cfc93d2a7df5ca12d959674d39b229819900252d87fdb1ad0440`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4aae3348ff67dcfc867e74ba7d93521cf602cc522d0c2875042b12c9abb756`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68acb52bef2ef59ccb0ac066ffd86c1cffd791d6070b775b4cad2bf0812fbac2`  
		Last Modified: Tue, 13 Jan 2026 19:09:13 GMT  
		Size: 532.0 MB (532020251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95f0ffa6327b4db525da6f9ce76baff708ded8fbf0a177b858e544a470ff009`  
		Last Modified: Tue, 13 Jan 2026 19:06:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdce219363a9ec7b79cb90fb71fbe48bfedd3a356eff83ad75c95396b9988ec7`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb0c47193e805c92ab1b4d1243c0212768703043c1972cc20a8fb7cffe19c2`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 74.1 KB (74106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2be888867fe7da31fcb8dde53d5a2e2068ef34d393b53da119cc63580ed4b86`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4d6447aa360331dfe80a8ac179608602e418af946d13b976f66b6f5e1c727ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa578bca94c87534691bcf84136de56f6acdd34289f971b0b0be7c03baddb1f`

```dockerfile
```

-	Layers:
	-	`sha256:73b67e6d459854eab823ce4a6def697f894a8529570195b7df38317bc63a49eb`  
		Last Modified: Tue, 13 Jan 2026 22:25:33 GMT  
		Size: 2.1 MB (2086282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fb87ab692b4926a4c9557dfd4794ce94f62843951d84be3d67fb67acd3b77a`  
		Last Modified: Tue, 13 Jan 2026 22:25:34 GMT  
		Size: 34.0 KB (34049 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.4`

```console
$ docker pull elasticsearch@sha256:0266542f69c89f877dda8d1c8eaa235a084c4bee66d8ae5e2e5b86c78e0217bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b0ff3e5e81f31d0ea45d7c02f4002f19e02bcf6fc18a97645db0c6186bb468f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.2 MB (738215790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae97915efe574b9ab24db5cdce51385478620ae42a5de980b44922f43c75049`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Tue, 13 Jan 2026 19:05:06 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:05:06 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:50 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:05:50 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:50 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:59 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:06:00 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:06:00 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:06:00 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:25.170027027Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dfc5c38614c29a598e132c035b66160d3d350894 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T22:07:25.170027027Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dfc5c38614c29a598e132c035b66160d3d350894 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 13 Jan 2026 19:06:00 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 13 Jan 2026 19:06:00 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:06:00 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:06:00 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a877ebc65964478715852678c19a87adf2ab3a229532447230dbd0f0f5f609ac`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 4.3 MB (4286917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d947b5843b56e1069a042d0f4426a1a1a5fd4f030fc4a25336d4ea6576074290`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60461ed3c7672bb78ac1791b2f7345c220f7a2e1b19e8ab5dc905ffb19e5b3cc`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375691d4f0e7a9e37f85dc57f9b782d46bbf12923c2cf2738bc0151d40a18ec8`  
		Last Modified: Tue, 13 Jan 2026 19:11:18 GMT  
		Size: 693.8 MB (693798165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65259db570a20d0ebb6f10a1b8d98ed8c12cce2bbab01ee8be3c702e981c215`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff621a01d060747a9f4f930bb9988ccb23aab774158fdeef0f955250955e4b5f`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47daa5a9ab20e056fbf6ef84aa9d237f9223d0660fd3197b4821d4ca700830fe`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 75.2 KB (75176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f457b6a3af683cddc209588fc640c8bebbf8df156bdf7fdaa3e4d8f474ba015`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0fafd42043b2e56aa2f99b6a1f6be13e83d608f06b4d62d99036ecca190ef480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a78366f7f46241a909568f5764b41d83c9db9460c0d013424d027c3588e3dbf`

```dockerfile
```

-	Layers:
	-	`sha256:7b0b6ab2fffb9a4759bc08ca5d7d7984ee74be35ee8cee577a8b18e57b6d0590`  
		Last Modified: Tue, 13 Jan 2026 22:25:38 GMT  
		Size: 2.1 MB (2098079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0cb1f137ee81e81f96eeb4c570c8790867ec39dd88930b0f5485a0e286ad20`  
		Last Modified: Tue, 13 Jan 2026 22:25:39 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:a3ea466801f0a1b488862a5ff7f2fc57618b110c81e9f3394b0dce53d24aca3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.2 MB (582193062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c9efd012faea1fdb6d2f3ea00158aac0b5ff8459270734fa4215db2e8b9df6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Tue, 13 Jan 2026 19:05:02 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:05:02 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:05:35 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:35 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:42 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:05:42 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:05:42 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:05:42 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:25.170027027Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dfc5c38614c29a598e132c035b66160d3d350894 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T22:07:25.170027027Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dfc5c38614c29a598e132c035b66160d3d350894 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 13 Jan 2026 19:05:42 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 13 Jan 2026 19:05:42 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:05:42 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:05:42 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e62a8581c382d8da952c01546837d1fe0f5c11d5f5f6ef729eb63188fb7837`  
		Last Modified: Tue, 13 Jan 2026 19:06:38 GMT  
		Size: 4.3 MB (4298096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018848372f79ca08b0d1aba230bd8f3454483c4b2327a7c2b2fb91d2d82aea7f`  
		Last Modified: Tue, 13 Jan 2026 19:06:38 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dec0cfbb4bd918688e8dc322c026d75462b49ca7969fc8825aaf87583baa4c`  
		Last Modified: Tue, 13 Jan 2026 19:06:38 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc7abb11045518494838a2041f3c44ef5d8f27247b888f54fe76b6bd750cc4`  
		Last Modified: Tue, 13 Jan 2026 19:09:21 GMT  
		Size: 539.6 MB (539583697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963ad772b8813588b7843e9f65eea33c02aba4f4f6a1841f85b6065ed134aa05`  
		Last Modified: Tue, 13 Jan 2026 19:06:38 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4656c38f6aee475dde7362b44f7dcc8c8fe5e043cab002fb333067a69c81bfec`  
		Last Modified: Tue, 13 Jan 2026 19:06:38 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238e9d27770b758c838e17a3240638a99e68743110bbac384f8d22399e30ab55`  
		Last Modified: Tue, 13 Jan 2026 19:06:39 GMT  
		Size: 74.1 KB (74104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c8d90ed27fef28cf3d1193c7ead1b4a5c08122ddcd03f12ecad40fc4b8bfc`  
		Last Modified: Tue, 13 Jan 2026 19:06:38 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:71598f08ef45f33ee8bfd84931a2cd741dcebbec81225fea1fbfb7ff43ec193a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e5501790c44a3ff757065de73ee9aaebdcd449299c2594bb8d096e2dab4d7c`

```dockerfile
```

-	Layers:
	-	`sha256:b751cb3303bcd07a4220c4a74c284b7f4703e7477c4878a4fdb7a765f4da5f60`  
		Last Modified: Tue, 13 Jan 2026 22:25:48 GMT  
		Size: 2.1 MB (2098641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcc8a775d50a2ffebe49f6603f38c1793debe5bf7a353f32c7e82863d54ac872`  
		Last Modified: Tue, 13 Jan 2026 22:25:48 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
