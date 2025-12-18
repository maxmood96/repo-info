<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.18.8`](#elasticsearch8188)
-	[`elasticsearch:8.19.9`](#elasticsearch8199)
-	[`elasticsearch:9.1.9`](#elasticsearch919)
-	[`elasticsearch:9.2.3`](#elasticsearch923)

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
		Last Modified: Thu, 13 Nov 2025 23:25:05 GMT  
		Size: 4.5 MB (4493909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f7b345db94a1a2c86c7e241bac630afd7c708a4540a5db8ca5523ac1da61e`  
		Last Modified: Thu, 13 Nov 2025 23:25:05 GMT  
		Size: 3.5 KB (3534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d27b11736af81fe4f0c3b5bee6534722ce2b0f084588d47dad6966c0aa4a6a1`  
		Last Modified: Fri, 14 Nov 2025 01:40:46 GMT  
		Size: 664.9 MB (664908814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b46a367471c93768bfac25f1547059ab2f1bd1d200cd2dd370fa11b9b2cc37`  
		Last Modified: Thu, 13 Nov 2025 23:25:04 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c0aa5ff83b648b37592a0d6e8d0e888650d97e71e606cd607eb29692d0518`  
		Last Modified: Thu, 13 Nov 2025 23:25:04 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41db951a09358077109950cd0cfb24fbec2a7dc5690e9175a388b6d00fcd5089`  
		Last Modified: Thu, 13 Nov 2025 23:25:05 GMT  
		Size: 163.9 KB (163935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff2aa099f19d62676a29e3ec7f8b2874349672def2cf3b834fffea50c6e4ae`  
		Last Modified: Thu, 13 Nov 2025 23:25:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b1972ad4e20e050b4102887185fea470d4215100c4aba3d82cb6fb1e637812`  
		Last Modified: Thu, 13 Nov 2025 23:25:04 GMT  
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
		Last Modified: Fri, 14 Nov 2025 01:25:30 GMT  
		Size: 3.2 MB (3192944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436e294639573790ef3eb79fa2513fd3c74f12f8bc626acfdb13396b89cfdca8`  
		Last Modified: Fri, 14 Nov 2025 01:25:31 GMT  
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
		Last Modified: Thu, 13 Nov 2025 23:24:07 GMT  
		Size: 4.5 MB (4498895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f44bc7b0af09b3a694a152f1433649cc2cbeb6f770e442b41bec589997f56`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9728459a5a3f4abb547584c07ae44961768661babd029b4713cb12ae80e9924`  
		Last Modified: Fri, 14 Nov 2025 02:55:02 GMT  
		Size: 508.0 MB (508003274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d526010e9271cf1fa50c3ce58b45edc2baeb72f63c9103694e37f4077e63a15`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f26d3872bef9a883c14b822ea082a9dbe814100cdcb33e6651be5133102f3a6`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e542b2865e2c21d02b52969930d99a03a04fe759cdd4f2d2ce726640d3d37bdb`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 160.4 KB (160368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c191344f90bbd2a51a6f8d0bab30596843eca8331bfbc68310678792d9bba0b9`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057047f0e243f23a7af94bfd9a04e48c031c234ab097c42fb5345c01e0f4f118`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
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
		Last Modified: Fri, 14 Nov 2025 01:25:36 GMT  
		Size: 3.2 MB (3193357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b82cbadcba6dca71ecc5d86882b31ebb377b61b1f4ba16d2605bc675a987df`  
		Last Modified: Fri, 14 Nov 2025 01:25:36 GMT  
		Size: 38.5 KB (38548 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.9`

```console
$ docker pull elasticsearch@sha256:dee84085936b5b5fc3a6d322ff7545c939f99269b2d94bf19ea4af968893bbc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.9` - linux; amd64

```console
$ docker pull elasticsearch@sha256:1070ddcda41b99d3a1c1c0d8ac14291370fe3c66b8c9f51f5bf4312d2dd76140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.1 MB (712108027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4428f6bdc4f57b428aa60a61acdc081fd1f9860902fb409b2f871c33bbf7b23a`
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
# Thu, 18 Dec 2025 19:09:55 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 18 Dec 2025 19:09:55 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Dec 2025 19:09:55 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:09:55 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Dec 2025 19:10:54 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 18 Dec 2025 19:10:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:10:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:10:54 GMT
ENV SHELL=/bin/bash
# Thu, 18 Dec 2025 19:10:54 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:10:55 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Dec 2025 19:10:55 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Dec 2025 19:10:55 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Dec 2025 19:10:55 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Dec 2025 19:10:55 GMT
LABEL org.label-schema.build-date=2025-12-16T22:07:42.115850075Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f60dd5fdef48c4b6cf97721154cd49b3b4794fb0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.9 org.opencontainers.image.created=2025-12-16T22:07:42.115850075Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f60dd5fdef48c4b6cf97721154cd49b3b4794fb0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.9
# Thu, 18 Dec 2025 19:10:55 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 19:10:55 GMT
CMD ["eswrapper"]
# Thu, 18 Dec 2025 19:10:55 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c7f575ecc192fd3441508f70480acecb20688c40e0e157c20c53e36a78ff09`  
		Last Modified: Thu, 18 Dec 2025 19:12:16 GMT  
		Size: 6.6 MB (6632781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82430d77f7ac199337b9f3f204dedac79d4a3cb8acf4a987513e21d013d644b6`  
		Last Modified: Thu, 18 Dec 2025 19:12:15 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2640ecea212cdc9a0be0daecacda6ba0eb03acd0ded80a228b68e24850d80cc7`  
		Last Modified: Thu, 18 Dec 2025 19:14:31 GMT  
		Size: 675.5 MB (675455889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330eb0229fee5b2c2957e7c76d6301788b12cef5450770f4e549da996c4badc0`  
		Last Modified: Thu, 18 Dec 2025 19:12:15 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b820d49c74e25f932318a5dbf7c408eb72aeff1266d1c77eb09266177602c97`  
		Last Modified: Thu, 18 Dec 2025 19:12:15 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd16f1d91bd69568766f19006fb3b4e07264b10a203d3117c6812f05eec30970`  
		Last Modified: Thu, 18 Dec 2025 19:12:15 GMT  
		Size: 163.9 KB (163929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa01ce0eb2ced897462e525ea52f90ccf977f045664f18ad14c72d59977e762f`  
		Last Modified: Thu, 18 Dec 2025 19:12:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5845070cdd5993a0ad3597949264e2f5f172840a6eb2beae9fd07e4c9a586573`  
		Last Modified: Thu, 18 Dec 2025 19:12:15 GMT  
		Size: 115.5 KB (115529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.9` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ffe01cb686641220f42e62f10fe704bfe3e375288a8a903d0acbba15f87abaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451f95a0c6795a59109330e429670a595caa62521aa77d4fe6b0ff0bc8e48a08`

```dockerfile
```

-	Layers:
	-	`sha256:048483e414cfe0af899f59aa130c7eefa8de174282a3b8e6dd62f5d5fe95f09a`  
		Last Modified: Thu, 18 Dec 2025 19:25:22 GMT  
		Size: 3.2 MB (3214864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c7e840228700f7dca1d45d0dccebfca1edf76102362df97c80ef6e115269dd`  
		Last Modified: Thu, 18 Dec 2025 19:25:23 GMT  
		Size: 36.8 KB (36840 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.9` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:4899865e22df659d1400d4d00dd6b4294609bb7e32091f304f596a87ece8e77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (559994153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81e9f2d5a38359d1ad1758d37781a01ae9583cf5f25849bf4174d02f4ecda0c`
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
# Thu, 18 Dec 2025 19:09:44 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 18 Dec 2025 19:09:44 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Dec 2025 19:09:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:09:44 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Dec 2025 19:10:21 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 18 Dec 2025 19:10:21 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:10:21 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:10:21 GMT
ENV SHELL=/bin/bash
# Thu, 18 Dec 2025 19:10:22 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:10:22 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Dec 2025 19:10:22 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Dec 2025 19:10:22 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Dec 2025 19:10:22 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Dec 2025 19:10:22 GMT
LABEL org.label-schema.build-date=2025-12-16T22:07:42.115850075Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f60dd5fdef48c4b6cf97721154cd49b3b4794fb0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.9 org.opencontainers.image.created=2025-12-16T22:07:42.115850075Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f60dd5fdef48c4b6cf97721154cd49b3b4794fb0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.9
# Thu, 18 Dec 2025 19:10:22 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 19:10:22 GMT
CMD ["eswrapper"]
# Thu, 18 Dec 2025 19:10:22 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2140e0f9d50b88dc2385cf7cae3f7b54794d2804e634db765fe635b534336bdc`  
		Last Modified: Thu, 18 Dec 2025 19:11:30 GMT  
		Size: 6.7 MB (6712132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53f229da06801a257881d22effce492b447d1ca7a33bf0c111601ad064c739e`  
		Last Modified: Thu, 18 Dec 2025 19:11:28 GMT  
		Size: 3.5 KB (3529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1821aed77f88ff62351a435111528462268b6a61af0a955121e178ac28a1942a`  
		Last Modified: Thu, 18 Dec 2025 19:11:42 GMT  
		Size: 524.1 MB (524129367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf818df3cf4e80a8a9d4cdd8732f98101d58aac35d1590d5f853d379a529aea`  
		Last Modified: Thu, 18 Dec 2025 19:11:28 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6a40720b3b0cba3650d618e5a1d9157d676f9daf782563e15594ab6802e8f0`  
		Last Modified: Thu, 18 Dec 2025 19:11:28 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc95b33fdeadc9d94b893f49c5f9311a1d332f0efe8c528e2b954eee6646ea5`  
		Last Modified: Thu, 18 Dec 2025 19:11:28 GMT  
		Size: 160.4 KB (160376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0d7af1f0241e39dbe8faa9f8e688c8366fbdaafe065a236cafb6d72f816d8b`  
		Last Modified: Thu, 18 Dec 2025 19:11:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e778ce96325b5914a45208351fdb5ca2ab1de2b788ebd5fb07099d8ecf47164`  
		Last Modified: Thu, 18 Dec 2025 19:11:28 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.9` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:78f85a9877d1d4505b719d8aab6c0960f732d2eb678f0abdedd75e33a9127855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0e96dda5d2fb6597c8ef22bb03d0d766bc208b553ab8bedf1b17f8e77bc453`

```dockerfile
```

-	Layers:
	-	`sha256:4fd2f5e8db12670f700ba7d3531eae476adaf11ae832917a8f41146e6a2c2dec`  
		Last Modified: Thu, 18 Dec 2025 19:25:31 GMT  
		Size: 3.2 MB (3215277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e757ee33aae5131439a9f8a50713d10ac03fe60743577012c5d521a9e3bd3b5`  
		Last Modified: Thu, 18 Dec 2025 19:25:32 GMT  
		Size: 37.0 KB (37042 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.9`

```console
$ docker pull elasticsearch@sha256:0db71cf020b29a880ccd53d8ead2ae094f7121e8f9f7a9a840fc0720482b315c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.9` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e67591d8e9360cf80688c8a5b0b9bb8dd0ef773ce0e8fc6caae887eebb35f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.7 MB (730660661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced1015992b85a8bc1e02853b17a7fba63ae6e8e98f78b421343a571848ef266`
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
# Thu, 18 Dec 2025 19:12:05 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:12:05 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Dec 2025 19:12:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:12:51 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:12:51 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Dec 2025 19:13:01 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Dec 2025 19:13:01 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Dec 2025 19:13:01 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:13:01 GMT
ENV SHELL=/bin/bash
# Thu, 18 Dec 2025 19:13:01 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:13:01 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Dec 2025 19:13:01 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Dec 2025 19:13:01 GMT
LABEL org.label-schema.build-date=2025-12-16T22:07:32.093242252Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=5cf7cb8c6f69b8c284f3ea738db6932703574d3d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.9 org.opencontainers.image.created=2025-12-16T22:07:32.093242252Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=5cf7cb8c6f69b8c284f3ea738db6932703574d3d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.9
# Thu, 18 Dec 2025 19:13:01 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.9 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Dec 2025 19:13:01 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Dec 2025 19:13:01 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 19:13:01 GMT
CMD ["eswrapper"]
# Thu, 18 Dec 2025 19:13:01 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767bba3543c3ccab5106d8d5b28f7e3f7641e3afe91a2aff4083a025c20b76c`  
		Last Modified: Thu, 18 Dec 2025 19:14:13 GMT  
		Size: 4.3 MB (4286944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac19569d94f483381cd49c76e3d2e92588d905f1da278512fca8b9a1955acd0`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09163d3fa69e255a029137389b8db29a6e948fec4d39b35a3b1c0862724a65b7`  
		Last Modified: Thu, 18 Dec 2025 19:14:14 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c841d0485338390a1fa7f76753ef5984ace63c93145f2e97401b595c44b972`  
		Last Modified: Thu, 18 Dec 2025 19:14:26 GMT  
		Size: 686.2 MB (686243003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d4ea8da01d560cc09dd318e8251a22ef618316c61c81134339ce126197d918`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674fec8f88305cc9e15a3cb8b481a56e52cd7b80dc429e66fa24a7e413b734e9`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c3b94f1d911bc9eb7d5038ff0a1ca4589ae1b3f9d1c26133b5baac931fe905`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 75.2 KB (75179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bebb58b47846caa40d00615b6f84dfc64c3b0a9e71929496c84959e11dd89fa`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.9` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5a504e1500d0c720c2b15207d809a016e4ffd9727b9d3b07256375aba813545b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd081f5dc681a425b85f7764f6f7644f64e6788c0b836057d5276baefb40e515`

```dockerfile
```

-	Layers:
	-	`sha256:a18b0464e14e072990d6583f26e8d274203aeb07b504bb645c9d7322cea832b6`  
		Last Modified: Thu, 18 Dec 2025 19:25:32 GMT  
		Size: 2.1 MB (2090447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f3365d81911328d46d7fc8c8665452b1e3d461205d4780ecd692acb8fb7ba0d`  
		Last Modified: Thu, 18 Dec 2025 19:25:33 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.9` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:1972c9256d3b25d74fde77db077102f0daf10f248d929a2a07edb954885f4792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574609546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfed8c79d1375f2221809fde9067f599a9f1b2fa334ddddc05a30773d5d8d3a3`
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
# Thu, 18 Dec 2025 19:11:30 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:11:30 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Dec 2025 19:12:03 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:12:03 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:12:03 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Dec 2025 19:12:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Dec 2025 19:12:10 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Dec 2025 19:12:10 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:12:10 GMT
ENV SHELL=/bin/bash
# Thu, 18 Dec 2025 19:12:10 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:12:10 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Dec 2025 19:12:10 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Dec 2025 19:12:10 GMT
LABEL org.label-schema.build-date=2025-12-16T22:07:32.093242252Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=5cf7cb8c6f69b8c284f3ea738db6932703574d3d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.9 org.opencontainers.image.created=2025-12-16T22:07:32.093242252Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=5cf7cb8c6f69b8c284f3ea738db6932703574d3d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.9
# Thu, 18 Dec 2025 19:12:10 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.9 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Dec 2025 19:12:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Dec 2025 19:12:10 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 19:12:10 GMT
CMD ["eswrapper"]
# Thu, 18 Dec 2025 19:12:10 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7de056334880bd11cbb2cad5d50cf70cda70a6d5697dd2947efbddf10fcd2c6`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 4.3 MB (4298155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062bae6421f5fc84a109526a5e9fa86ed82e54a4d0068bc20debe0c0e4fb4a73`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9737a921e83c23c37470ea0a44613dd386be6b2a35ccb28c6d1d8e16955a3d34`  
		Last Modified: Thu, 18 Dec 2025 19:13:05 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08580c7a5ea2333846a2343e99e9d550ad66365614fcecbd3d54a4d210812b8`  
		Last Modified: Thu, 18 Dec 2025 19:14:14 GMT  
		Size: 532.0 MB (532000104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab699f7a7f31e7f3401e322b186f6b19b67950e79f83757f555e7ca88bff5459`  
		Last Modified: Thu, 18 Dec 2025 19:13:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9137791832946fbfa455ea3ee1cbedb09eac3302ad0e67606d42dd28cb874a39`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4ff745d236b1f38ae9657bc92fbed05e8c114f83b79448693693b5b53a1d91`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 74.1 KB (74113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3402b38e19954cdfdf3d9877cfb901e220111b8a6405503c02c1661d36b38bb4`  
		Last Modified: Thu, 18 Dec 2025 19:13:05 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.9` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d6b06dfae346afee5883ba244c85ad5e99963850da66d9d9c47184c9307e8e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe16ed37e011359fbf8c344da4f9c778fcb7a842cd1040de854c56309477a78`

```dockerfile
```

-	Layers:
	-	`sha256:a9854b91f8748ad1cf178c2f04c34d498502daea9b1733e69105fa0c46bf0ce3`  
		Last Modified: Thu, 18 Dec 2025 19:25:37 GMT  
		Size: 2.1 MB (2091009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00277f7653c1621a63d19f6b7939daf3ff3e3db083b3d70521c6db67c60503ad`  
		Last Modified: Thu, 18 Dec 2025 19:25:38 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.3`

```console
$ docker pull elasticsearch@sha256:f1eee5cad02476a967aa040406c38e6e176b9eea4e0b99e997dcf8079e8ca0c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:493721ee30e0641d160ea1fa9eb841f068f006dff17ea81e1a076b06adc37065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.9 MB (737916768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6728c69f7fc0f76b000fd7f5202a7c904e583562cde81eaf2f91ee8fb58fc72`
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
# Thu, 18 Dec 2025 19:12:03 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:12:03 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Dec 2025 19:12:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:12:47 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:12:47 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Dec 2025 19:12:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Dec 2025 19:12:57 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Dec 2025 19:12:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:12:57 GMT
ENV SHELL=/bin/bash
# Thu, 18 Dec 2025 19:12:57 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:12:57 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Dec 2025 19:12:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Dec 2025 19:12:57 GMT
LABEL org.label-schema.build-date=2025-12-16T10:09:08.849001802Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d8972a71dbbd64ff17f2f4dba9ca2c3fe09fb100 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.3 org.opencontainers.image.created=2025-12-16T10:09:08.849001802Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d8972a71dbbd64ff17f2f4dba9ca2c3fe09fb100 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.3
# Thu, 18 Dec 2025 19:12:57 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.3 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Dec 2025 19:12:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Dec 2025 19:12:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 19:12:57 GMT
CMD ["eswrapper"]
# Thu, 18 Dec 2025 19:12:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d44f2c3976ded9b16199de07d25edd6ccbd0e2a0a4eb93f1712fbdc985db9a`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 4.3 MB (4286934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb758f8ef5db3fff65560a5517284e8296d24e3b97c1903001d71251d6e971de`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6ebe239ffaaecf73417636caafd32ddbf16ee8ab6f5766cd74e8932ef6995d`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7af9e56da63c39d6a9cff19ebd87130bc3723c0672f8a423c2c67a7513829c`  
		Last Modified: Thu, 18 Dec 2025 19:14:47 GMT  
		Size: 693.5 MB (693499125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23391cb3312c1b53161e949de530cb3c8f9f3f8aa79927806278b0ea3de165af`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39f68f235aa92eb83537050c2eafd6b0d08ea61d77d32f3fde9362288ba7e0`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f38bde45467f12ea5efa808106142a2ca87fe70974a2c20e8fb2ae06c933c5`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 75.2 KB (75179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a881477255899bcf54d41fc0d554a11317d9ca8d0210ff3c8eb802af378b973`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a7e7c129c94fea21f5d235de146eb86d2ab0c994689e77271cbdab00da910200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5f4a63bc31b2bf39ea763222db358a80854ef94258a0311ee6b39a28adb0a6`

```dockerfile
```

-	Layers:
	-	`sha256:ae392ba112c5c587dcebedb4b52a2a3781fbcdec059a50f7ae6d9011132977f2`  
		Last Modified: Thu, 18 Dec 2025 19:25:42 GMT  
		Size: 2.1 MB (2098055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:282dcda56cb7ea877449cb10546876e72ff7d551009b49cc8ee6b0317e189acc`  
		Last Modified: Thu, 18 Dec 2025 19:25:52 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d22ef495da4ad769dd0d6ca3aca36779302cf9f7d45a4294385812143112838f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.9 MB (581892637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d4e98b36e9c1e11de2d664495c10cbc5245639e996b2811ccddb83eae36c6d`
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
# Thu, 18 Dec 2025 19:11:31 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:11:31 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Dec 2025 19:12:05 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:12:05 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:12:05 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Dec 2025 19:12:11 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Dec 2025 19:12:11 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Dec 2025 19:12:11 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:12:11 GMT
ENV SHELL=/bin/bash
# Thu, 18 Dec 2025 19:12:11 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:12:11 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Dec 2025 19:12:11 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Dec 2025 19:12:11 GMT
LABEL org.label-schema.build-date=2025-12-16T10:09:08.849001802Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d8972a71dbbd64ff17f2f4dba9ca2c3fe09fb100 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.3 org.opencontainers.image.created=2025-12-16T10:09:08.849001802Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d8972a71dbbd64ff17f2f4dba9ca2c3fe09fb100 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.3
# Thu, 18 Dec 2025 19:12:11 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.3 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Dec 2025 19:12:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Dec 2025 19:12:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 19:12:12 GMT
CMD ["eswrapper"]
# Thu, 18 Dec 2025 19:12:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44e7a3ffa23f8f10e35bb5bb2ddb011fc38b581eff292ee40da348889a4e44`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 4.3 MB (4298149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad97cdb415aeeda46b7981c8b8ae3a000e091d894ccb6cb653ab9c8d364b158c`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713ba77e7b27644440c49dc0b6c98d4640b14678cd8e491ba35c040f2b4187ce`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2da39e61d1aa909b97c7b5a37d40a632f5b1ba91ec0084a9d128de8f33fc22`  
		Last Modified: Thu, 18 Dec 2025 19:14:40 GMT  
		Size: 539.3 MB (539283201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d63acfc3ed97a9fc03e8b98128bef0cb599e34ab141ad7d4eae7e878813e48e`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb25d35cf3bc11fff2b803b14b4f273c3c80bd047ffe64af1184705b53e60dc5`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a006b672f42324c9685a4dcd445cc341df864aff178634ad4ba33524ac5774`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 74.1 KB (74114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a06d30b48abbc470f60c1fdb6bced33808f1865e77867bbb734c929259b84`  
		Last Modified: Thu, 18 Dec 2025 19:13:06 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:eb2ab90a95fcfd70bba5c99922b5da1d1a578ed6d589311e354632a7d2a999e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0f559761455a796f96d5263e3c4231a137be959d9c089b754686cfa31ba472`

```dockerfile
```

-	Layers:
	-	`sha256:04e9aaca97bbce555de8dddb0bd9a56ee8b0795dd59200e50208ec416b7d28c4`  
		Last Modified: Thu, 18 Dec 2025 19:25:58 GMT  
		Size: 2.1 MB (2098617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2defe8e880bed35c6d2b47cae83b313175369be0f7bd555faa098a9ed3e2c2f6`  
		Last Modified: Thu, 18 Dec 2025 19:25:59 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json
