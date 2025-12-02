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
$ docker pull elasticsearch@sha256:bfad0c616167e79203b5ecd75918293b46beb4ae39f4cb20f7ff9f7f3c27ac02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:c22450f4084bf3d6e524ec2fe865f65463c8d1936854473d48f0511bca2066f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.4 MB (727394151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf85cfadee94973f7cae96ec5761c41da26d0451dc5c4d52bc6daea418a8ee3`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 00:41:22 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:41:22 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Dec 2025 00:42:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 00:42:39 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 00:42:39 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Dec 2025 00:42:49 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:42:49 GMT
ENV SHELL=/bin/bash
# Tue, 02 Dec 2025 00:42:49 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Dec 2025 00:42:49 GMT
LABEL org.label-schema.build-date=2025-11-07T10:07:43.588125290Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=49e091e266fdfecd2b3a96f9d390719838fb742d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-07T10:07:43.588125290Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=49e091e266fdfecd2b3a96f9d390719838fb742d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Tue, 02 Dec 2025 00:42:49 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Dec 2025 00:42:49 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:42:49 GMT
CMD ["eswrapper"]
# Tue, 02 Dec 2025 00:42:49 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c968390321444119f7cd1f5d207544afe3e3888502f6409eaca38d5023c9f7e`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 4.3 MB (4286404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cdf7081dcc19960dcfc3c92eeedeabb6ee414c2f3b61503b1bb7e77a3b7abb`  
		Last Modified: Tue, 02 Dec 2025 00:44:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303ccde3f8dd3cf6ccd08004e03810da11916f7f51fe05ce670b45161700a8ac`  
		Last Modified: Tue, 02 Dec 2025 00:44:03 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12503a48bb3ed707ecbceb76075ed83922de7c90ccff66a58b79162a3a58301`  
		Last Modified: Tue, 02 Dec 2025 01:49:22 GMT  
		Size: 683.0 MB (682977709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c194126afd032866f35a858d05aac0c18fe4c6d612e30c04108a236d3509fa`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062731c8f934def5dc79b17f8b5280cd70335cd48711c64da6297b616ec4abda`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dfbf1f3a7e112755bf2ea0129549307167969193348575d2f2db145555046e`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0088b3e0aefb3e32eb52185b91dc7170929be89d3d96d3522377547ccd9094a7`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8381ac206dfb84068a5e08f94806347721dbc92137c94951eac30698a976d7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46067503d03f590013ca7b67d7be3fa2d648a16ab83c8fc65f1edd45f999a990`

```dockerfile
```

-	Layers:
	-	`sha256:f5cd619d7a991edb2819f501fc864b67379e04a02afd71f69ae88a5491ff5a22`  
		Last Modified: Tue, 02 Dec 2025 01:25:35 GMT  
		Size: 2.1 MB (2091577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d6f54c5e1ea8a30e213c7bef0eeed8462a24feca9036b9567490db6bce3729`  
		Last Modified: Tue, 02 Dec 2025 01:25:36 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e92d48659226516220ffc4ee67c04c89bd7822043378df8ba9a1999b39f3fa5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565655384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900b4cc684a380adb4672826305e8ebc3e19da8ad078b21d7dae47e56c869768`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 00:47:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:47:21 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Dec 2025 00:48:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 00:48:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 00:48:18 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Dec 2025 00:48:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Dec 2025 00:48:24 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Dec 2025 00:48:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:48:24 GMT
ENV SHELL=/bin/bash
# Tue, 02 Dec 2025 00:48:24 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:48:25 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Dec 2025 00:48:25 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Dec 2025 00:48:25 GMT
LABEL org.label-schema.build-date=2025-11-07T10:07:43.588125290Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=49e091e266fdfecd2b3a96f9d390719838fb742d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-07T10:07:43.588125290Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=49e091e266fdfecd2b3a96f9d390719838fb742d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Tue, 02 Dec 2025 00:48:25 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Dec 2025 00:48:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Dec 2025 00:48:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:48:25 GMT
CMD ["eswrapper"]
# Tue, 02 Dec 2025 00:48:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141d7cbcad79acee03d95d076560d9fc0cba1f6ce8c3344813b883715dd24722`  
		Last Modified: Tue, 02 Dec 2025 00:49:25 GMT  
		Size: 4.3 MB (4298512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55ee7f0075faec2cbaa383b0eefc22b6c30b81b84945f5fa2bcb2c0d5d81fee`  
		Last Modified: Tue, 02 Dec 2025 00:49:23 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088a64d4710deb9b313f68fe88fb0d7a90f4268a3f82491aa813519a05c3fcf7`  
		Last Modified: Tue, 02 Dec 2025 00:49:22 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f2e3a92e3aa483571a6ac7c79ba2406583a675934a3030dcd2f95809f65990`  
		Last Modified: Tue, 02 Dec 2025 02:24:03 GMT  
		Size: 523.0 MB (523046712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd3b33da1bb0cd7674d18ef0ad7b25559a4bca4dcbbd58983a1aaca312ccee3`  
		Last Modified: Tue, 02 Dec 2025 00:49:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9a0a9df324fdd8e5ce38835aeb2c1598e2ab2e3a16446dce3bca9483ebe989`  
		Last Modified: Tue, 02 Dec 2025 00:49:23 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf81ddebca25dea3d7a7ffa7008142b64895cfc942196e021389f1fd8bb5e121`  
		Last Modified: Tue, 02 Dec 2025 00:49:22 GMT  
		Size: 74.1 KB (74111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178e5e888e6e35dd55abc9f19361431e929f9a646d198ced9bbe9666a12a685d`  
		Last Modified: Tue, 02 Dec 2025 00:49:22 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:78e2dc6a3c0d8b0cf60e7b74c70d4daf6b875d83dd472f27a1e3fa0c5e93e2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2126177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cac519ac551e924f9bf99b2bbd4a217bb674734e5d2b2494b1d619519558f44`

```dockerfile
```

-	Layers:
	-	`sha256:6b10c967d65f7b04f5f05832e1c2e33a2e3f0e725e41ac2b0e05957a0a1e490d`  
		Last Modified: Tue, 02 Dec 2025 01:25:40 GMT  
		Size: 2.1 MB (2092139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ad967150fcf9b6c5ac307795a5c8dc4138030d2cedff6cba141ee2378d78d4`  
		Last Modified: Tue, 02 Dec 2025 01:25:41 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.1`

```console
$ docker pull elasticsearch@sha256:5d176d5b6e55249f71ce037e53c83b29afcd26237eadf0c97bd6f6168812d4b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:3440a83803f62f0a4337c14bc8f8a5a907cfd230d84b59b5e7669d0c47137083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.2 MB (737160493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4eb8ee9229b9a5243ef7aff7f073dca01080e9b88d170f49c7792ff7e9648d2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 00:41:23 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:41:24 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Dec 2025 00:42:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 00:42:39 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 00:42:39 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Dec 2025 00:42:48 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:42:49 GMT
ENV SHELL=/bin/bash
# Tue, 02 Dec 2025 00:42:49 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Dec 2025 00:42:49 GMT
LABEL org.label-schema.build-date=2025-11-06T22:07:39.673130621Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T22:07:39.673130621Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Tue, 02 Dec 2025 00:42:49 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Dec 2025 00:42:49 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Dec 2025 00:42:49 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:42:49 GMT
CMD ["eswrapper"]
# Tue, 02 Dec 2025 00:42:49 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf6b260fc03e425905b93696155ecb6b71c0c8081a61893929f54968b511c6f`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 4.3 MB (4286352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f0312cfc7b1185fbd37fd5665315058de9abb9ecd96d8ac7bbce2e403f520`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 1.5 KB (1538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376823dbdc4563b9b755de86cb185efe517d8935d717d03727654bdd1096214d`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0a5d6ee4910ad48ee3d0709c1f72109b382a7004366471b972408b0dfec6e1`  
		Last Modified: Tue, 02 Dec 2025 01:27:09 GMT  
		Size: 692.7 MB (692744098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c1001e4b1ff61fa4bd5338cd86154aecea21394d85f2912118c9d9c8c2f4fd`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f044454f54c1854da8064cdb1f235e014b76469b4a99eec427cf34e4dc6d1a86`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054d373583d95d73de86753c46a45e53ec408a9078265dbfabe3a100c4e55ada`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 75.2 KB (75179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0088b3e0aefb3e32eb52185b91dc7170929be89d3d96d3522377547ccd9094a7`  
		Last Modified: Tue, 02 Dec 2025 00:44:04 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d179b175f6dc6da53d56340146b5acadffb0e566dfa5edf9423025cd4694c6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5021a5a080ed98b24a77427e2544758956aeaa51d06152ccfc71813d0d7e2450`

```dockerfile
```

-	Layers:
	-	`sha256:724d9cec7dd3311b9ddfa79664aeae202e203df2bee32aa2ac20c32edaa2547d`  
		Last Modified: Tue, 02 Dec 2025 01:25:47 GMT  
		Size: 2.1 MB (2097824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d842ca14c8752d833c9bd456f1338f823ecabe766f5d8c4b33bbd408af85166b`  
		Last Modified: Tue, 02 Dec 2025 01:25:48 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:20652eae817a7aa1c223d6f4bdc0addbb72786b2ff819f4923c1c74f99f2198f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.1 MB (581145906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd56dd36c088a1a2e45b0709db5ade5eac6b75441d1751fe8576c9fbf9cd44d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 00:47:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:47:22 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Dec 2025 00:48:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 00:48:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 00:48:18 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Dec 2025 00:48:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Dec 2025 00:48:24 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Dec 2025 00:48:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:48:24 GMT
ENV SHELL=/bin/bash
# Tue, 02 Dec 2025 00:48:24 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:48:24 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Dec 2025 00:48:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Dec 2025 00:48:24 GMT
LABEL org.label-schema.build-date=2025-11-06T22:07:39.673130621Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T22:07:39.673130621Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Tue, 02 Dec 2025 00:48:24 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Dec 2025 00:48:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Dec 2025 00:48:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:48:25 GMT
CMD ["eswrapper"]
# Tue, 02 Dec 2025 00:48:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ae7b0e77242ded15df89d4c7d2397808e3c94a4c59286946b40d1c1fdc153a`  
		Last Modified: Tue, 02 Dec 2025 00:49:21 GMT  
		Size: 4.3 MB (4298549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378ce96317ad510d6df2de0ec49e02db2fc2017d285b06e4440e1c3b5e507619`  
		Last Modified: Tue, 02 Dec 2025 00:49:21 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088a64d4710deb9b313f68fe88fb0d7a90f4268a3f82491aa813519a05c3fcf7`  
		Last Modified: Tue, 02 Dec 2025 00:49:22 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43c825f0d6a84a4771a065cf1d41fe34c380718b4fc8e5b10263310d2ecdaf9`  
		Last Modified: Tue, 02 Dec 2025 02:27:34 GMT  
		Size: 538.5 MB (538537202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe8973e51091bb7cb35a737377c3897d4117a3d2d5bcbd1c61382b59182471c`  
		Last Modified: Tue, 02 Dec 2025 00:49:21 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb384d06ce2e8d11a54ab7b9730d385f4dff2f106e4f6e886f7e02af2432fb16`  
		Last Modified: Tue, 02 Dec 2025 00:49:22 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a573df687e00fc29d6bc1d8119b2dd50066a7cf6929ecdc726c71af02157db`  
		Last Modified: Tue, 02 Dec 2025 00:49:22 GMT  
		Size: 74.1 KB (74109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178e5e888e6e35dd55abc9f19361431e929f9a646d198ced9bbe9666a12a685d`  
		Last Modified: Tue, 02 Dec 2025 00:49:22 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:378d255eaeb213d892fc4327afb5c75c27e1d8e719fc23417850d62d89d1676a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d75bb75604fc28fb1c607246b11e9076894bc226de2f22ca1b532b84874b08`

```dockerfile
```

-	Layers:
	-	`sha256:fde031493e4be3ed811ff4000ed0c47b74ef37ebdb2da7a0e22e8f07fac75322`  
		Last Modified: Tue, 02 Dec 2025 01:25:52 GMT  
		Size: 2.1 MB (2098386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab420c44ff7bd500463d520ac76c6d5a17d67f203ebe0f03d29140c3c4da09ce`  
		Last Modified: Tue, 02 Dec 2025 01:25:53 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
