<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.18.8`](#elasticsearch8188)
-	[`elasticsearch:8.19.7`](#elasticsearch8197)
-	[`elasticsearch:9.1.7`](#elasticsearch917)
-	[`elasticsearch:9.2.1`](#elasticsearch921)

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
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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

## `elasticsearch:8.19.7`

```console
$ docker pull elasticsearch@sha256:ff698b2f7dd37c8b7517a73194559d604e6568b3882af05d8190a2d5244c1988
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:32a9715a88879b61b93da5f057a1b6d097dbdacf1232ec0cf84358e3616dbedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.8 MB (706830529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cd795a3b5d5dea733f4239c0338f16d6182c7fd4c31d4cd73af5eb24e354ec`
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
# Thu, 13 Nov 2025 23:22:31 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Nov 2025 23:22:31 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:22:31 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:22:31 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Nov 2025 23:24:03 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:24:03 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:24:03 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:24:03 GMT
ENV SHELL=/bin/bash
# Thu, 13 Nov 2025 23:24:03 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:24:04 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Nov 2025 23:24:04 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:24:04 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:24:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Nov 2025 23:24:04 GMT
LABEL org.label-schema.build-date=2025-11-07T13:35:54.762042224Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=198d86868932741b4e0d184425510217febc27d1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:35:54.762042224Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=198d86868932741b4e0d184425510217febc27d1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Thu, 13 Nov 2025 23:24:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:24:04 GMT
CMD ["eswrapper"]
# Thu, 13 Nov 2025 23:24:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eedf2cb97239fee53fa50bcc02e66327659cb1e53544a9294513f1ed881ec6e`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 4.5 MB (4493928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7510353cd2679ad87546d0043d91cab8a626eeb49ef21c6b8087d4e34e542e`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b579f6be3438fae726b022e5cdc4345daf7925027e9476d295117f7b853f0201`  
		Last Modified: Fri, 14 Nov 2025 01:30:03 GMT  
		Size: 672.3 MB (672317228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed55c1ff45199138809922057270d3b955e8235b81ffdaa11d8e3898a03e857c`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ec5d0f363c674cd5224287f26102f06e681532e4cde073e8ab837b64cca6c3`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e41eb3f0160f8d319d6bb033453df01b901fa678a2512735b5e4078c16c99f`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 163.9 KB (163936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93004e76c5cc12a458e548c1dabbaf000e8546096f876ed2657525cacf32eb9c`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4b73630156627ea04b267c9f185cf70d5f4feb7f30bde2b765988cbae974e`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:510811dd5bbab1a99a4641d620afaa57dc2c10b1663e387236c07310370be3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d20df509ae3e7e3cc970113ae1808075d7872e0568c89e62011404c894f7a1`

```dockerfile
```

-	Layers:
	-	`sha256:4dbe87d60eadcd0ac2e6fa4554cf784c73c9b8fdadea03efd1fe1cca3791cf09`  
		Last Modified: Fri, 14 Nov 2025 01:25:40 GMT  
		Size: 3.2 MB (3215994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209650b0846ff2dcf6605a414d4391dcd69497bcf300a37c9a8115a450a08a95`  
		Last Modified: Fri, 14 Nov 2025 01:25:41 GMT  
		Size: 36.8 KB (36840 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e9849d694a27ed0427df5a2b83621057f8129d974f93b4b05b6c9578491c3f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.0 MB (549047435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2226b55500b37fcfe688d6cfeb27c4a57240108c74b983319ecb1581d4477aa`
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
# Thu, 13 Nov 2025 23:22:15 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Nov 2025 23:22:15 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:22:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:22:15 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Nov 2025 23:23:20 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:23:20 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:23:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:23:20 GMT
ENV SHELL=/bin/bash
# Thu, 13 Nov 2025 23:23:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:21 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Nov 2025 23:23:21 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:21 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:21 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Nov 2025 23:23:21 GMT
LABEL org.label-schema.build-date=2025-11-07T13:35:54.762042224Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=198d86868932741b4e0d184425510217febc27d1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:35:54.762042224Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=198d86868932741b4e0d184425510217febc27d1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Thu, 13 Nov 2025 23:23:21 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:23:21 GMT
CMD ["eswrapper"]
# Thu, 13 Nov 2025 23:23:21 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5dc2b0d5e559cfcb00c026e4821bafbf21b712d0bf5b2dae416e038be43066`  
		Last Modified: Thu, 13 Nov 2025 23:24:17 GMT  
		Size: 4.5 MB (4498781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a529ad298c4b710fb7ec862b44a7a661935eb5a73655ffce521073802ed3ba`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 3.5 KB (3529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6c03c065daeb81cc8b7c15141229a93cd14aa49c7b091fbc57c6458c45dd6`  
		Last Modified: Fri, 14 Nov 2025 02:16:08 GMT  
		Size: 515.4 MB (515396014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369fca0716a1d41a91e8317b6816825ad75030e323ac3470d0244d34cc95c998`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3b7cf8e0dd9b3b69416d9dd1dd2551bd0299f61a769ba6849354d09b8e9a9c`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8955afe7bb1d0b05dcd79e2f203d8136c27c2863c8a4cce7fcd5a9051d4a4f74`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 160.4 KB (160365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1117e6b09102410992e67ecf06fc0104bdc33d3e7787278a1c0124271dc28`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049b864e3d605dd66c0a078becc7cda1505f4eda3c71e22c6cf5af999a9cf9b0`  
		Last Modified: Thu, 13 Nov 2025 23:24:14 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:23d662ec26f67ac7c4912df55daf57bdd9aaf306b82c105e914a6f36c9265140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ce87df191f61141850731d8170a4c14ed1daa7f9992dd6be2d1341b53a0567`

```dockerfile
```

-	Layers:
	-	`sha256:9cc1ff05f03678690f4144529afd86bc02cb841ca1eb370163ddadebe57b5c39`  
		Last Modified: Fri, 14 Nov 2025 01:25:46 GMT  
		Size: 3.2 MB (3216407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5059f722d6b952bb3a2b01fefb3882703fb3b7930bc9715928e946483618b9f3`  
		Last Modified: Fri, 14 Nov 2025 01:25:46 GMT  
		Size: 37.0 KB (37043 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.7`

```console
$ docker pull elasticsearch@sha256:85fe870be3fef8feae5d503049a16b2374c41c1f94300b1e6f7bfde0bfd2f69a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:c003f5ba7d801ca52be7d67e6da3130bc94b3319756b80fd2e5e3a4bec37ba9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.3 MB (727346944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e008b448d88892906d06638ebebd1ee21459d2642047cda9f38e2e28f449de7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:25:53 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:25:53 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 12 Nov 2025 00:26:35 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:26:35 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 12 Nov 2025 00:26:35 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 12 Nov 2025 00:26:45 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 12 Nov 2025 00:26:45 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 12 Nov 2025 00:26:45 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:26:45 GMT
ENV SHELL=/bin/bash
# Wed, 12 Nov 2025 00:26:45 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:26:45 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 12 Nov 2025 00:26:45 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 12 Nov 2025 00:26:45 GMT
LABEL org.label-schema.build-date=2025-11-07T10:07:43.588125290Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=49e091e266fdfecd2b3a96f9d390719838fb742d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-07T10:07:43.588125290Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=49e091e266fdfecd2b3a96f9d390719838fb742d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Wed, 12 Nov 2025 00:26:45 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 12 Nov 2025 00:26:45 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 12 Nov 2025 00:26:45 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:26:45 GMT
CMD ["eswrapper"]
# Wed, 12 Nov 2025 00:26:45 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1008c9c06e5777b45b9b239b7aaeca626eb83d38a1efb1a89ce3ad8bb204b4`  
		Last Modified: Wed, 12 Nov 2025 00:27:59 GMT  
		Size: 4.3 MB (4278540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492d835f5502c4e4cb907a0226cca5e9c09e2c2c00aecf45b658c807f31a59a4`  
		Last Modified: Wed, 12 Nov 2025 00:27:59 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a454a7bc521294c6ebc0f80c980c7e35e14c7133dc802655c7326491c066c`  
		Last Modified: Wed, 12 Nov 2025 00:27:59 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec065018e4b4e32aa9ffa839515d59ba5846858cedf4c39a1b1aaa44790d1f5`  
		Last Modified: Wed, 12 Nov 2025 01:40:53 GMT  
		Size: 683.0 MB (682977709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2758f7ed6b39cabd6f00ad34f61a244fe7873050532622e6aa2b98c3d2dfe4`  
		Last Modified: Wed, 12 Nov 2025 00:27:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0769f3656eb08f206cdbce9d5f63da4fd7d5da382a8395cd603f98432456782b`  
		Last Modified: Wed, 12 Nov 2025 00:27:59 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea73bcc06f7f650c60ff0c27076d2fcc355750304508b1960dcaa168b56700e`  
		Last Modified: Wed, 12 Nov 2025 00:27:59 GMT  
		Size: 75.2 KB (75181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa7937defb14bbe5e922773be79f99214ffcf0ae5925600adeee47eaf311003`  
		Last Modified: Wed, 12 Nov 2025 00:27:58 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a7049d6f517e8ca5ce26f87ae47501d87dc7693923cd33728d0590dfdc080607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7315309919a6501dd0b35fa8d14e3516a1c2e6017767d64e9eef9dc4daa89b`

```dockerfile
```

-	Layers:
	-	`sha256:e61c0502677d3a73d77a7243e0f08ef4b6fe5408fb5bede50e13bc0fe09b4b15`  
		Last Modified: Wed, 12 Nov 2025 01:25:24 GMT  
		Size: 2.1 MB (2091561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6383eb1ee1676c10e973fb59c1de9f618dac6bc1b02490afb36a385c0b0799`  
		Last Modified: Wed, 12 Nov 2025 01:25:25 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c37925af583fa5ed1cb29f35fabaa4f074b1c49cef5b01cdfe50e7acc3b001e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.6 MB (565637171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c304adb52f7325eeeb78ef90c4a8d5d42ef25b8b22694805b2e78b8e83cdea36`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:39:20 GMT
ENV container oci
# Mon, 03 Nov 2025 14:39:21 GMT
COPY dir:e6638cbef7baa2be94a007ecfd2531710d358328001d7cc1a125e3837ced3f20 in /      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:39:21 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:39:04Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:49 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:50 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 12 Nov 2025 00:28:45 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:28:45 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 12 Nov 2025 00:28:45 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 12 Nov 2025 00:28:51 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 12 Nov 2025 00:28:51 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 12 Nov 2025 00:28:51 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:28:51 GMT
ENV SHELL=/bin/bash
# Wed, 12 Nov 2025 00:28:51 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:28:52 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 12 Nov 2025 00:28:52 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 12 Nov 2025 00:28:52 GMT
LABEL org.label-schema.build-date=2025-11-07T10:07:43.588125290Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=49e091e266fdfecd2b3a96f9d390719838fb742d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-07T10:07:43.588125290Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=49e091e266fdfecd2b3a96f9d390719838fb742d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Wed, 12 Nov 2025 00:28:52 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 12 Nov 2025 00:28:52 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 12 Nov 2025 00:28:52 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:28:52 GMT
CMD ["eswrapper"]
# Wed, 12 Nov 2025 00:28:52 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:fccdcd3fc47f898d65f9d4531d01539ce33a7ec8038500d557bfe58eb4b6ae87`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.2 MB (38211473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e42faad1da175fec4759783362bf16c78cd6b0c08823076558c88e3aee2a52`  
		Last Modified: Wed, 12 Nov 2025 00:29:50 GMT  
		Size: 4.3 MB (4290484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f3615146061a70f0d6d69478d09c79eb7619f38695b120211da6be89ca308b`  
		Last Modified: Wed, 12 Nov 2025 00:29:50 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991eb645e65c713592fdba98b58f86492898a57a65d883f940c7f1fd734f5f31`  
		Last Modified: Wed, 12 Nov 2025 00:29:50 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c452eec3495f454dfbdcf4e4916af41b01cc3886d1513e2aa323663f684afdaa`  
		Last Modified: Wed, 12 Nov 2025 05:47:55 GMT  
		Size: 523.0 MB (523046757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d63aea09dc3e1c9f87638953a61c2932489d91f2def0fa8fb2d5d70f889ad`  
		Last Modified: Wed, 12 Nov 2025 00:29:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70444632359bcf8621f3e92fced7e436e7861f1848dca13f5d45fcfd3f5db7`  
		Last Modified: Wed, 12 Nov 2025 00:29:50 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ada2f476e30ca2aa25afaeb99cfdfe056c4e0d3afc4f86f3c9894a3f6bb300`  
		Last Modified: Wed, 12 Nov 2025 00:29:50 GMT  
		Size: 74.1 KB (74106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c390c8d53140c08c7f8e253d217915f596239d5f19e32bbfadee594a496a1b`  
		Last Modified: Wed, 12 Nov 2025 00:29:50 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:31a9e2d1556b283b3a77542d6c84ac184f6bf61f390fc2b5ad223241f55759d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2126160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18c6ec4a849680979acad07301efd8cf14a9cf3fc7afbd34efa6669dc70ac21`

```dockerfile
```

-	Layers:
	-	`sha256:aff01ff774ba8b62c1b21ea12a0c72d0163cd2bc7382d47073a066ddd12c0444`  
		Last Modified: Wed, 12 Nov 2025 01:25:29 GMT  
		Size: 2.1 MB (2092123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9f671ec6a0fee11fc49ea5a17ce3125bd53cd20756333f1d06ea8c957ba2e95`  
		Last Modified: Wed, 12 Nov 2025 01:25:30 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.1`

```console
$ docker pull elasticsearch@sha256:b22783af4415a45b64dc8448883686325fe922f3e1bd8b9ed7ea1fe05067c1af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9f79096a8e7320b7c9a664e4a5f12e20034e9022c3d83de1fec8e58cbbbc67c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.1 MB (737113350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de20fa8c2755ff2dfc57a9d946e950f047e49088daec3270861c54e92794a828`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:04 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 12 Nov 2025 00:28:18 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:28:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 12 Nov 2025 00:28:18 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 12 Nov 2025 00:28:28 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 12 Nov 2025 00:28:28 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 12 Nov 2025 00:28:28 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:28:28 GMT
ENV SHELL=/bin/bash
# Wed, 12 Nov 2025 00:28:28 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:28:28 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 12 Nov 2025 00:28:28 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 12 Nov 2025 00:28:28 GMT
LABEL org.label-schema.build-date=2025-11-06T22:07:39.673130621Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T22:07:39.673130621Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Wed, 12 Nov 2025 00:28:28 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 12 Nov 2025 00:28:28 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 12 Nov 2025 00:28:28 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:28:28 GMT
CMD ["eswrapper"]
# Wed, 12 Nov 2025 00:28:28 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d901735e0f6d126faa2cb382a8ed191f0b810a14d45001cbea1ad24017c977`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 4.3 MB (4278575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188eba4bb7cc0b82ce255a340d83ff28c9609d985bd94b82b8ec38b685b52036`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c748381424bf6dce56fc282297231b0d6c0f8f5e0dd6b50eecb87a7f88f9c625`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bf8cb5fecd30610048048c3d952965c3e92b5d039e7d4b4cfe8ab56a8d72d2`  
		Last Modified: Wed, 12 Nov 2025 01:27:38 GMT  
		Size: 692.7 MB (692744079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8227b32df95ba0f73daf732b182aebe0843ea9cdcdf7351b7c7f40c3de7a314`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf14cc8a68d8c75cb579664d1ba9083848c0c745cb2c1fed38036e2eac34aaa`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad830220ba8537b8358a83f0c1ea49f37e57d4f2c12c979b8f6bf7bb21d51173`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc2cddb8cf87b00978ba0e55d215ae9481b6f765dded0269bacc766f824792`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:aae8f22484e60d85098481c5b008afea9246e2894646dfcbb8936ea523e890a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e65132f10ea3f9cdce02938100bc26aa6b82e602450d4174b07d3f585d9fee`

```dockerfile
```

-	Layers:
	-	`sha256:613e1ab1f1a0056569ec46de3f50972934de624999dffe7612667ca9b8bf99b8`  
		Last Modified: Wed, 12 Nov 2025 01:25:36 GMT  
		Size: 2.1 MB (2097808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2100a502cf015cebc96119446d726ebda07a8d8e97ebdb19cf8bd2d6ce651f7`  
		Last Modified: Wed, 12 Nov 2025 01:25:37 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:076f3e9e4e6fe5c2f99792fd567225721fbec626528fdd1adf7b16e5c2570da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.1 MB (581127614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ff09035145bf303e4ea2e9ba22eb5002378418a769cdf5329139a5112c9fce`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:39:20 GMT
ENV container oci
# Mon, 03 Nov 2025 14:39:21 GMT
COPY dir:e6638cbef7baa2be94a007ecfd2531710d358328001d7cc1a125e3837ced3f20 in /      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:39:21 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:39:04Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:45 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:45 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 12 Nov 2025 00:28:41 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:28:41 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 12 Nov 2025 00:28:41 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 12 Nov 2025 00:28:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:28:47 GMT
ENV SHELL=/bin/bash
# Wed, 12 Nov 2025 00:28:47 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 12 Nov 2025 00:28:47 GMT
LABEL org.label-schema.build-date=2025-11-06T22:07:39.673130621Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T22:07:39.673130621Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Wed, 12 Nov 2025 00:28:47 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 12 Nov 2025 00:28:47 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 12 Nov 2025 00:28:47 GMT
CMD ["eswrapper"]
# Wed, 12 Nov 2025 00:28:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:fccdcd3fc47f898d65f9d4531d01539ce33a7ec8038500d557bfe58eb4b6ae87`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.2 MB (38211473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19bcb95679c0e867cac6e9f103c60cf1fa5e1b23040c8f3fdfbb67d1c1c4e53`  
		Last Modified: Wed, 12 Nov 2025 00:29:45 GMT  
		Size: 4.3 MB (4290482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3418a30254895acf6444bd744000cd9d4f2d41a8a1fdb795937c2b366e8e86c`  
		Last Modified: Wed, 12 Nov 2025 00:29:45 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ab044951070c9a5410a65a2c440baa96c34d214de12da889537f763b2d4d1`  
		Last Modified: Wed, 12 Nov 2025 00:29:45 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1733b8916f05ef381d02290422e2f7bd3b16b716ccfcadfbccfe40d1d4355db`  
		Last Modified: Wed, 12 Nov 2025 01:38:40 GMT  
		Size: 538.5 MB (538537211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00c794a1ad43cb01ff1ccd94d53521af97261997e4779e8c6dc97512093c98e`  
		Last Modified: Wed, 12 Nov 2025 00:29:45 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9f19af993a002dc04075863aa9f15f73bb3dae84a064ca3f873e25785206c2`  
		Last Modified: Wed, 12 Nov 2025 00:29:45 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8345e99d214714fa3c91558c7638abce95cf7f22e7dc892a85b155a22eed755f`  
		Last Modified: Wed, 12 Nov 2025 00:29:45 GMT  
		Size: 74.1 KB (74105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec6c28abfc7071fc73315160446fdb387e9909e43b67e8bae282cac1c158e81`  
		Last Modified: Wed, 12 Nov 2025 00:29:45 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d88278acc5ee660450141bb6984ba1e8c482243cc6db67a2b70bf38940fe0e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f14bb258cba99ffd3b51a8f8766bbcaedca6596cabcc89c3ded78112c5c67a0`

```dockerfile
```

-	Layers:
	-	`sha256:b0fd1c5503c52ecf930024643a340e74e6cbef03094bd9aee2d15c94ababb430`  
		Last Modified: Wed, 12 Nov 2025 01:25:41 GMT  
		Size: 2.1 MB (2098370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13f231069df16e525fb041e0342e097caa9e98e9f639496f50fe8ab8e806ec1`  
		Last Modified: Wed, 12 Nov 2025 01:25:42 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
