<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.20`](#logstash71720)
-	[`logstash:8.13.0`](#logstash8130)

## `logstash:7.17.20`

```console
$ docker pull logstash@sha256:6b56354b81d355c361a574dbcbb1a5e05a89350a241ecf728732c077b03eff74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.20` - linux; amd64

```console
$ docker pull logstash@sha256:03d5bdfe6b9b9a8ae8829f03aea24b6cd043d1c0303ce3d434cb2517099a1007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.6 MB (444616527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8638023377bd4f75267014acaa3b07987088e3addbc12ca5eab804e0caa6551`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.20-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.20 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 09 Apr 2024 08:24:48 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
USER 1000
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.20 org.opencontainers.image.version=7.17.20 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-26T08:47:56+00:00 org.opencontainers.image.created=2024-03-26T08:47:56+00:00
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846a58f3f0d75f76b009624ac6cc39a486f16838ec5a7651f890db6b4369fbda`  
		Last Modified: Thu, 02 May 2024 00:53:21 GMT  
		Size: 47.9 MB (47864891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08706a1845f4144317f59d4611a31ef2872374bb8ae18e4d90004263aa1f6bd6`  
		Last Modified: Thu, 02 May 2024 00:53:19 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b566f273c1fe84988b9ea010a5a72e45c864833caf4b2e0cf8d299cb9d546570`  
		Last Modified: Thu, 02 May 2024 00:53:29 GMT  
		Size: 367.3 MB (367332399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f39abeda81b666f6901a9ccb15a0929c5d67b1bd9f9c4dcf9b39d3d17568d52`  
		Last Modified: Thu, 02 May 2024 00:53:19 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f47c5a8f7bc6a29581c2443ce3db453bcc03aeb100f20e3ed81764b30ddc2c`  
		Last Modified: Thu, 02 May 2024 00:53:20 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d5c39c0e90ab71b42c35f5390d226f3cfe5e04a122a20097a5af50b02a3f26`  
		Last Modified: Thu, 02 May 2024 00:53:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dac3d392a2cd609ab360fd47060bc31f78decc60af7a82b24630976c0bbc7b`  
		Last Modified: Thu, 02 May 2024 00:53:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7cf5b318e65dfbaf9d878bf5b082f3ff8bb2985c054b1fec5fb9325a813ad8`  
		Last Modified: Thu, 02 May 2024 00:53:21 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a72488077c0a1f942e1ce8799d68a33332a9075d9f9ca75112b9d5cf5cb3556`  
		Last Modified: Thu, 02 May 2024 00:53:22 GMT  
		Size: 1.9 MB (1902986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7066dd97404c96efe2f76edd1d295f022836d825e8bf6fd1fee1a59d39e07e86`  
		Last Modified: Thu, 02 May 2024 00:53:22 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.20` - unknown; unknown

```console
$ docker pull logstash@sha256:f3dbda401ca19b5d52699d69ca1d734902cc1af2d3daff12da6022f05fffda1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e728d65678d672c153ed97c3a0a32e2afaa543aa222530b97dafeaca13eb5735`

```dockerfile
```

-	Layers:
	-	`sha256:b3bb1aae35b46ddde2c2eb547db4ff874cdbca4ac3777d21be4c049473f12b89`  
		Last Modified: Thu, 02 May 2024 00:53:19 GMT  
		Size: 3.0 MB (2978474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27913e6936009dc3192c954b6e4f216c66e23563a2039f29c31f46cc88805fdf`  
		Last Modified: Thu, 02 May 2024 00:53:18 GMT  
		Size: 32.2 KB (32173 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.20` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:195faa23814306358615437754803967531ae65e897e00346980f95b23261de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434847842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce89e4a6c177dfa1dde12fd18af07bd0b26b792f76f3f895feba5b4f956490b0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.20-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.20 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 09 Apr 2024 08:24:48 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
USER 1000
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.20 org.opencontainers.image.version=7.17.20 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-26T08:47:56+00:00 org.opencontainers.image.created=2024-03-26T08:47:56+00:00
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:935803725f5775642918295f3557fecf93003fde6403df6fcbb2379ce4795a1d`  
		Last Modified: Wed, 17 Apr 2024 18:54:25 GMT  
		Size: 26.0 MB (25976141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ecde1e241c08684748c64821a9f8e9c01ff041fa5bc49591bb8d71d1040306`  
		Last Modified: Fri, 26 Apr 2024 08:00:36 GMT  
		Size: 42.9 MB (42916843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0490b5abbb57452d98af0c894756e29f045b6cd89bf8c8e291aae56acee5ceb`  
		Last Modified: Fri, 26 Apr 2024 08:00:35 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d08a2dd05895f61c5b12e8619436604075c556bc92f09b0a47e8f4a58cf816`  
		Last Modified: Fri, 26 Apr 2024 08:00:43 GMT  
		Size: 364.0 MB (364047268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934dc90e93a78f928001fe73663d67c47d6fb2481f23d751cc6eb270bc03b5ad`  
		Last Modified: Fri, 26 Apr 2024 08:00:35 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2804b71af89545044fd1bb47ead5319853c0accd2293dfde90b37893db953b`  
		Last Modified: Fri, 26 Apr 2024 08:00:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c21b1c04b2b2dfceb9f05fe300a06af2b00827db356a86a77a1bf829d43c110`  
		Last Modified: Fri, 26 Apr 2024 08:00:36 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b3b052be11e1a642526ebfc2ba04cd68e5a12764e87e2b4cccfdb20c1c172`  
		Last Modified: Fri, 26 Apr 2024 08:00:37 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c4813d2247edb8a2a0d583f2b24c3fd78506a8b6c010ecfc3375049c63427e`  
		Last Modified: Fri, 26 Apr 2024 08:00:37 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbcf50ff02199cbc9edd936bd45a15b64750694eb316ec6d4257e6a94ec6a07`  
		Last Modified: Fri, 26 Apr 2024 08:00:38 GMT  
		Size: 1.9 MB (1902992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c950a54aa7a903db24da39e7c98c42249bc9f026eba760162dc3318525271dbb`  
		Last Modified: Fri, 26 Apr 2024 08:00:38 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.20` - unknown; unknown

```console
$ docker pull logstash@sha256:57fe349853b90938ed6a2dd926c49e17db01f0306a02f6f0325afb5a2e8b71a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146c70fc661622bf7a06e6056ff6bd08823f83e6e9389b53d00440074f9a19af`

```dockerfile
```

-	Layers:
	-	`sha256:9e2a4959c97ee12c1730dcd375ed594c988bc8b4abc7eeb9a659b73f66b5288c`  
		Last Modified: Fri, 26 Apr 2024 08:00:35 GMT  
		Size: 3.0 MB (2978694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19087fe1f5078954bc635607f00da456b3bfb5df4a6dad74c045894e1b8a6e4b`  
		Last Modified: Fri, 26 Apr 2024 08:00:35 GMT  
		Size: 32.0 KB (32015 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.13.0`

```console
$ docker pull logstash@sha256:a637727d69cd8c2a4d6ff26c9f1cc8783766598f36c36488badc9001dce367e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.13.0` - linux; amd64

```console
$ docker pull logstash@sha256:92afe4aebeb722296a28479a1533abb7a291b5ee294c59b7faa691b072710779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.8 MB (490825311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be364664b3e88cbc48275f3e01122250326c3a8282bd45cb2cd5efcceb41e87b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' && apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all && apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.13.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 13:49:26 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.0 org.opencontainers.image.version=8.13.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-21T09:15:34+00:00 org.opencontainers.image.created=2024-03-21T09:15:34+00:00
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4c16a72c442cd1448f63004326bdd5bd7d0391bdc53faf1e24a0913cf60d87`  
		Last Modified: Thu, 02 May 2024 00:52:59 GMT  
		Size: 47.9 MB (47864645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da78bc1c409bac6df9fa17f8d877d2cd4df068c096863137a1f2b4dc3fdc12a7`  
		Last Modified: Thu, 02 May 2024 00:52:58 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee0544d560fc33251fea2696e4a22cc2d9fd91630d0961541b1764eb1d4ccfd`  
		Last Modified: Thu, 02 May 2024 00:53:04 GMT  
		Size: 413.5 MB (413538459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00b5a276229f4f6880fd5ba4ad5d0cdce1a5e0b7793e20079d89b245e81b180`  
		Last Modified: Thu, 02 May 2024 00:52:58 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4c49fbaf06099617ae0f56d51206dbea4f18bfe4149f760229e4a7086f1e40`  
		Last Modified: Thu, 02 May 2024 00:52:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4b2fe60c879f0a138358872a61cb52fd4c1272b2b274fe6c5f7b2e5171badd`  
		Last Modified: Thu, 02 May 2024 00:52:59 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54cbf40c9b33af212c6629ce4d1add13525db7d1adec0bbed8f2fb3081f7b73`  
		Last Modified: Thu, 02 May 2024 00:53:00 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3c53bbdd54dae62a4d9c4464fbd2b8ca4a96e86001c9f54d0579c154f2faa3`  
		Last Modified: Thu, 02 May 2024 00:52:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fbc9259ccf1cf069f3f48f6655b404604220a990a6e0b6281dec31ee215e45`  
		Last Modified: Thu, 02 May 2024 00:53:00 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ae181287fff671ae54fb9644d4ab9d8f053dcd5dde47f590e88e832ff5dd94`  
		Last Modified: Thu, 02 May 2024 00:53:00 GMT  
		Size: 1.9 MB (1903442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761d7f2e5e733faaaadab570d62797117cd08a85145995e9ab80916523640aa6`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.0` - unknown; unknown

```console
$ docker pull logstash@sha256:8a171d46d20f8b203ddbee1e19149b18e0c28a913241d4617760bd984c251991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3213565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22f3438f60cafa09e2c78e39f0e8d104eb52fbc631581c1a324546b183929fd`

```dockerfile
```

-	Layers:
	-	`sha256:413c4a931e55dfeefa2872cf09e9b8f6594af99fc45ffa86cdb8be2f8021f71e`  
		Last Modified: Thu, 02 May 2024 00:52:58 GMT  
		Size: 3.2 MB (3178871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e48f9cecd894441d441cca96a5bd6bd38aeb66d55d998e7864eb81230eee2cd5`  
		Last Modified: Thu, 02 May 2024 00:52:58 GMT  
		Size: 34.7 KB (34694 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.13.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:b56446a58d8dcaf1d4be3f3c35444add2a0625bd439ee9840a93ec64825e411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.6 MB (477625464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd659dfd321d22c916b2501ae9cf2c7ee157073b26d452d3d6969cfe0524c81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' && apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all && apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.13.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 13:49:26 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.0 org.opencontainers.image.version=8.13.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-21T09:15:34+00:00 org.opencontainers.image.created=2024-03-21T09:15:34+00:00
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b148d046c7b9f612d3dc9a31efd661236dc9542c63cd57d8301063d58d9b9f4d`  
		Last Modified: Thu, 02 May 2024 11:41:06 GMT  
		Size: 37.4 MB (37393329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a35ca5b552a3c7d60ff82e8d60879775d4af189842dec320a045191495d8068`  
		Last Modified: Thu, 02 May 2024 11:41:05 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a416522947b70a43f51d4488272d5bed6e23c032d1ad64a7a4a588ee96e3d291`  
		Last Modified: Thu, 02 May 2024 11:41:13 GMT  
		Size: 412.3 MB (412346073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d073ebf720a6c8dbb1070ce22ed9851c1c4ebb77c8aeead59609e14b90f6b5c`  
		Last Modified: Thu, 02 May 2024 11:41:05 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629b93081be2c2a2b05a0b9f881196c8e6c547b6832c920283792695c886997f`  
		Last Modified: Thu, 02 May 2024 11:41:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48c75ad08e8d2ca0b7ffdc669eebc783268c87622f9ed8ef2a494c935ce36cb`  
		Last Modified: Thu, 02 May 2024 11:41:06 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a5f5712c09ecb3544f90664b777f5513fedeb1c80cbb8038f6acdbb313bf15`  
		Last Modified: Thu, 02 May 2024 11:41:07 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b490f0e6b75391d3e4252daa6a620eede2aadbe0e2dc49a0533a8358309ca0`  
		Last Modified: Thu, 02 May 2024 11:41:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4331c3c1e5ebf5894abd3b50839c0a21688e7c3d9985b55b677839413eddf568`  
		Last Modified: Thu, 02 May 2024 11:41:08 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730597144a478b9c0202f3d9a1b8941b60fa0b384a228ef0b2c9a0d6181f0c65`  
		Last Modified: Thu, 02 May 2024 11:41:09 GMT  
		Size: 1.9 MB (1903445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af48dca893c03e251014ed41b5772d151c8e9f7858ffba23498c0a91244e966`  
		Last Modified: Thu, 02 May 2024 11:41:09 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.0` - unknown; unknown

```console
$ docker pull logstash@sha256:749d5dda7b334fa38c01df30a863aa95a646c6f51cfc1600f08cc3a4f1dd3eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3213628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2c6946c61752de1344a29a870cd4090cad3c95d41d90381044f482dc1cde65`

```dockerfile
```

-	Layers:
	-	`sha256:2445357ea3b4fe1d7203cf96d52fff7f78863cc0602c618bce72c6b9ffa54d61`  
		Last Modified: Thu, 02 May 2024 11:41:05 GMT  
		Size: 3.2 MB (3179091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72c706fd4d7517e9b34ee95e29f1495b7f0ff15e61b1897e9652a2ff59c1e4c4`  
		Last Modified: Thu, 02 May 2024 11:41:05 GMT  
		Size: 34.5 KB (34537 bytes)  
		MIME: application/vnd.in-toto+json
