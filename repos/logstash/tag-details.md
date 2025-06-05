<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.28`](#logstash71728)
-	[`logstash:8.17.6`](#logstash8176)
-	[`logstash:8.18.2`](#logstash8182)
-	[`logstash:9.0.1`](#logstash901)

## `logstash:7.17.28`

```console
$ docker pull logstash@sha256:a33651ffe9c9710445c539952a20675ba094e175e77ef711727e572d0720d3d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.28` - linux; amd64

```console
$ docker pull logstash@sha256:71f6b05ec719aef84c8e50bc38d987a61170270254edaa470db65e8e5f59a4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.4 MB (457404901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f962566cb0c11034228112abe7e82f1f006f9de494b85a8e55b9a811803d866`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 25 Feb 2025 11:58:14 GMT
ARG RELEASE
# Tue, 25 Feb 2025 11:58:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Feb 2025 11:58:14 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Feb 2025 11:58:14 GMT
CMD ["/bin/bash"]
# Tue, 25 Feb 2025 11:58:14 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.28-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.28 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Feb 2025 11:58:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Feb 2025 11:58:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 11:58:14 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Feb 2025 11:58:14 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
USER 1000
# Tue, 25 Feb 2025 11:58:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.28 org.opencontainers.image.version=7.17.28 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-18T11:10:52+00:00 org.opencontainers.image.created=2025-02-18T11:10:52+00:00
# Tue, 25 Feb 2025 11:58:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0a9a0e49135760c6a5a55434b15ef272724426e7de6411c257d97c07fcca25`  
		Last Modified: Thu, 08 May 2025 17:24:34 GMT  
		Size: 51.8 MB (51841555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c5b47f107cb437e2f453681cdeca9d03ecc8d375fd74e43d80a2237ae016a1`  
		Last Modified: Thu, 08 May 2025 17:24:29 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8a7f4d067a7abcb2c49699d87582c262281c77c63e818e6b7d59df9cc04837`  
		Last Modified: Thu, 08 May 2025 17:44:34 GMT  
		Size: 376.0 MB (375953820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee541d0097e99be72865fbccd04549f39c9cb518f245fe6d781febadbdc4da`  
		Last Modified: Thu, 08 May 2025 17:24:29 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e536a7c74e6de920dd9b20e9e7db18d9b00e58d1fe32492e22cd1653b518c2`  
		Last Modified: Thu, 08 May 2025 17:24:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6519c9c72daf7bf8c99a9ddce0319e78a0329578d14e0057a1973f60958997`  
		Last Modified: Thu, 08 May 2025 17:24:30 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f6811998c4c02a3234880408af19ac1cbf568c353e5b3d9c9075be45157964`  
		Last Modified: Thu, 08 May 2025 17:24:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d36d0f262466d0248eabd85512cae7e928f427baf771105234fb7fe314026`  
		Last Modified: Thu, 08 May 2025 17:24:30 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af7627aa24218b689af904fe683c729682abf5773144e11b986d432a201cf54`  
		Last Modified: Thu, 08 May 2025 17:24:31 GMT  
		Size: 2.1 MB (2094543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b5bcc60c98b2a2be4f6d6338fd08f33a6a1ca50eaf6ca47e294be513a244b5`  
		Last Modified: Thu, 08 May 2025 17:24:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.28` - unknown; unknown

```console
$ docker pull logstash@sha256:12e48fcfcd189c8021a71012904b991d24076aa9e22b382a9367599ec1bb1a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3371178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3870cb4ff8535c5ca564503724a701ccdd3772fe831a1608577b110580ef52`

```dockerfile
```

-	Layers:
	-	`sha256:c8745bcc9b9f68c4241c9c31fead2c8d75c7880d98cf68892ee17a404ebe82df`  
		Last Modified: Fri, 09 May 2025 10:16:51 GMT  
		Size: 3.3 MB (3338992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e48fd86aca853c5dd96ae3beb0a3ff6063a7129647ec8d31fd3ae6808e91fc`  
		Last Modified: Fri, 09 May 2025 10:16:51 GMT  
		Size: 32.2 KB (32186 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.28` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:93d0e6a929c88a8b59cbb9610c990b44abdf9a0d7349f38700ca60ee6f1a7333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.8 MB (439835627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e49d81da248a4a2d8047a415a131f0f57938befa77cf2e83236f2bc73b8d47e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 25 Feb 2025 11:58:14 GMT
ARG RELEASE
# Tue, 25 Feb 2025 11:58:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Feb 2025 11:58:14 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 Feb 2025 11:58:14 GMT
CMD ["/bin/bash"]
# Tue, 25 Feb 2025 11:58:14 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.28-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.28 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Feb 2025 11:58:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Feb 2025 11:58:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 11:58:14 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Feb 2025 11:58:14 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
USER 1000
# Tue, 25 Feb 2025 11:58:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.28 org.opencontainers.image.version=7.17.28 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-18T11:10:52+00:00 org.opencontainers.image.created=2025-02-18T11:10:52+00:00
# Tue, 25 Feb 2025 11:58:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0939b7441eaba115b97c3db22600a75f8a6b389cd1e4fd73f8bc862248af1807`  
		Last Modified: Fri, 09 May 2025 06:14:43 GMT  
		Size: 39.0 MB (39010198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d596e9398c708ab58590ffdc6322e2aff73fcb4a9fb693efc6be081a048efd1`  
		Last Modified: Fri, 09 May 2025 06:14:32 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d88adde7b488546cae09abfe3a08fee78e0893e310cf8dd27467a82b741140d`  
		Last Modified: Fri, 09 May 2025 06:15:14 GMT  
		Size: 372.7 MB (372748625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5365133754261c5f87817063987eb918df86c3699d09ad200a0793747759f00`  
		Last Modified: Fri, 09 May 2025 06:14:41 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909bb53a563e678c1a801b62d307dae1dc0173738c2fe4414ef2fea1fa53e25f`  
		Last Modified: Fri, 09 May 2025 06:14:44 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b08c2d477f11420408969f1b97a6d8ac214cef78063686b28b6a109a0b79a`  
		Last Modified: Fri, 09 May 2025 06:14:46 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0c0b535add31d7def3ab14bc0b2d07468a62e3b52b0bfbb8316f5f5f7cbeaa`  
		Last Modified: Fri, 09 May 2025 06:14:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dbec348d3d7a0a3d8110e46340315b3916fa6da0e675ffaf17adcb6e9f8bc6`  
		Last Modified: Fri, 09 May 2025 06:14:50 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd9c1eb0c5a30657cc2e0218881cc32e3749f5f8b198afcce6c389f7e62eb17`  
		Last Modified: Fri, 09 May 2025 06:14:52 GMT  
		Size: 2.1 MB (2094544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6750cfeb851dc339e2df67372c88e0733072cab3df91a1b7f77083b7d49b2bb5`  
		Last Modified: Fri, 09 May 2025 06:14:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.28` - unknown; unknown

```console
$ docker pull logstash@sha256:f979dbb108331734dfd706a1f4d10c3b9b412cc35112288ea8049d91fa4d3419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3371542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e07fce5f1e143927440c90b00efd632e7e8cfae0061ad7b4d8e2476562aba6`

```dockerfile
```

-	Layers:
	-	`sha256:acd4b032d59c7dc8ac2def0b0f6aa6b1dca8fa12bbd809bf43a7605f7b96adb0`  
		Last Modified: Fri, 09 May 2025 10:16:53 GMT  
		Size: 3.3 MB (3339228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77dcb4c11329f0b60d058bea97ede94e6062e9a4e15813a67d79aabbd5fd3b21`  
		Last Modified: Fri, 09 May 2025 10:16:55 GMT  
		Size: 32.3 KB (32314 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.17.6`

```console
$ docker pull logstash@sha256:04ee87a5dc23b4e9118e9726540ea7602bd13bd3c98623ad17a417e165f6a3e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.6` - linux; amd64

```console
$ docker pull logstash@sha256:b07cd69929bab450b555e65e8a72ce0d52596c04ff77b7dde98b97a40f175e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.9 MB (524862975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438e439223fda5d016b1554d7e6430a770e51b67485a07d7c125ae5745be579a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Tue, 06 May 2025 08:53:36 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 06 May 2025 08:53:36 GMT
WORKDIR /usr/share/logstash
# Tue, 06 May 2025 08:53:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 08:53:36 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 08:53:36 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 06 May 2025 08:53:36 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 06 May 2025 08:53:36 GMT
USER 1000
# Tue, 06 May 2025 08:53:36 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 06 May 2025 08:53:36 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.6 org.opencontainers.image.version=8.17.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-04-29T15:54:52+00:00 org.opencontainers.image.created=2025-04-29T15:54:52+00:00
# Tue, 06 May 2025 08:53:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197edc6bd3269011b533cbb7e8b3639c64725dd1f2ed5f3848c64681ec85675`  
		Last Modified: Fri, 09 May 2025 19:03:33 GMT  
		Size: 52.4 MB (52382230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57744598d88c8308ed6f2232d34a60c26f5cd3a823b4bf1efd36a0f26b0ebe3d`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4931bfdcbcf711f42edb943ac87b6d8d71934ddb693ff0baad3315dde065fb`  
		Last Modified: Sat, 17 May 2025 06:04:03 GMT  
		Size: 438.8 MB (438815223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9fe70b51275531f8bc5f9a283be24ad76ba33ba2328727e14e1faa266a6a33`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903735ecb6e30a318046fe5702a51045bc861b1acb2762c0bf79a43ade8f5e0`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322b56efd943035bbbca06fd39512f1381b7ff7b2ea3776799e514669963ae6`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f115783a195dcdd598214fc98b3b4fc10ee765d238dd1c1d05ba4795d21fe43`  
		Last Modified: Fri, 09 May 2025 19:03:15 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a909bc506cb68cb0b16cbc500c014f8fc4b43cf1e7f5e3764b1e55d1aa60215`  
		Last Modified: Fri, 09 May 2025 19:03:15 GMT  
		Size: 4.1 MB (4054809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0002094c59b881d05c49afff486ee4cc0842710b828ff5db705bccb8ed593daf`  
		Last Modified: Fri, 09 May 2025 19:03:15 GMT  
		Size: 2.1 MB (2093835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7e90aeb95044c7a697ad900eb9d9cdd562073851fe3c1a46c2fdfed87ae7f5`  
		Last Modified: Fri, 09 May 2025 19:03:14 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.6` - unknown; unknown

```console
$ docker pull logstash@sha256:5d35b2f1b51a5cef286a35a4f9d36711be90d3aa43aa00faaad854d7db5c32ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a641f7fdee494b7e8e9efd6cf13945aa9caa43ed184bc02b1effcaee7620db`

```dockerfile
```

-	Layers:
	-	`sha256:fedbb153abee72146ba7f3db819ca2181dcaef042b98135758aee0ee3233d3bd`  
		Last Modified: Sun, 18 May 2025 02:26:14 GMT  
		Size: 3.5 MB (3512306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:785590c45c0c784b5bef23e7194f9e21c139065e61f99a4596ae3dcc65e03dc2`  
		Last Modified: Sun, 18 May 2025 02:26:15 GMT  
		Size: 34.6 KB (34592 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:83015e24ef62d6683e1eac0e05c3ff36840427d0ff4afc5b7df8e04c2a5b2e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.3 MB (508261599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173ef3e812c6538185c5a89ee34c23a0f682bdb9818bc27fbb8bcee71211550d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Tue, 06 May 2025 08:53:36 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 06 May 2025 08:53:36 GMT
WORKDIR /usr/share/logstash
# Tue, 06 May 2025 08:53:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 08:53:36 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 08:53:36 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 06 May 2025 08:53:36 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 06 May 2025 08:53:36 GMT
USER 1000
# Tue, 06 May 2025 08:53:36 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 06 May 2025 08:53:36 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.6 org.opencontainers.image.version=8.17.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-04-29T15:54:52+00:00 org.opencontainers.image.created=2025-04-29T15:54:52+00:00
# Tue, 06 May 2025 08:53:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d67c1bd3c9da18476c361a404d289c14a3b659b3c9838eeb5fb76622ca373c0`  
		Last Modified: Sun, 18 May 2025 02:25:35 GMT  
		Size: 39.2 MB (39161298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadbe60a13b17a898594fb205d68343531555f48df7c2212f4ad5839fe3fa0fe`  
		Last Modified: Fri, 16 May 2025 17:35:49 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dca1e3bd6ad14a562fa2d1dd9a6066890780a5f1dfbd740d1f4c1c2accbc3a1`  
		Last Modified: Fri, 16 May 2025 19:24:22 GMT  
		Size: 437.1 MB (437100383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565da4f09eb262a7e9ca0d54a7ed648299b45ce8e4d16efb63faef836ff83d6`  
		Last Modified: Fri, 16 May 2025 19:24:00 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3498a07a7d8380a4b6872023d11762b63d02a1a59c4f806424f8a4842d4cab8e`  
		Last Modified: Fri, 16 May 2025 19:23:48 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c12209273b3011f85ea2e5f3dc17b7e2d3283b5b2204fcb09205615c795e6d`  
		Last Modified: Fri, 16 May 2025 19:23:51 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b645e99c4f66d782c419b59f507576deb9947c4ddde5e690d1709add872805`  
		Last Modified: Fri, 16 May 2025 19:23:58 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7ffba4e26570d8e7096752e917e130dc6c9ad745ca7585988a993ada6ff9d0`  
		Last Modified: Fri, 16 May 2025 19:23:56 GMT  
		Size: 4.1 MB (4054808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e81f7bd61af1261e69b9411c4f662a67100d0ff81e7805c28bc5411d3634cf3`  
		Last Modified: Fri, 16 May 2025 19:23:59 GMT  
		Size: 2.0 MB (1960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf97055b212574556533682cde6b49535d3fd0df750cf96486d3c6d5df9000ce`  
		Last Modified: Fri, 16 May 2025 19:24:05 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.6` - unknown; unknown

```console
$ docker pull logstash@sha256:770d27e079560919d5ba17a41c8152caef1d8b91a2bd6d4789e058f50d8554de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96b5bf026d9f464e9f95691c56c1adfc3f2f449563d5afd48f9e18d06bff4b1`

```dockerfile
```

-	Layers:
	-	`sha256:fe9d18ac130697f87bc64216abf811e4cc259d6501cedfc9725749e45b617d87`  
		Last Modified: Sun, 18 May 2025 02:26:32 GMT  
		Size: 3.5 MB (3511918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781fd046b71bbfccb1f6674d89cd234bb4015bf3bdbeb5c70b9107b9d6caa627`  
		Last Modified: Sun, 18 May 2025 02:26:32 GMT  
		Size: 34.7 KB (34736 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.18.2`

```console
$ docker pull logstash@sha256:f9cd539d6907afa8871c8d69620c45434252f930a5e21e60be2475b3b06be06a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.2` - linux; amd64

```console
$ docker pull logstash@sha256:f59718164eafd252a33c50651d80af448088bf6c70aa50146ffc106ba02eff94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.1 MB (532112194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456393a56716cd40c94f3dcb87ced0c4fd93ff0baf5ed787bf02c1c8f6e6ee30`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Thu, 29 May 2025 09:13:46 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 29 May 2025 09:13:46 GMT
WORKDIR /usr/share/logstash
# Thu, 29 May 2025 09:13:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 29 May 2025 09:13:46 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 May 2025 09:13:46 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 29 May 2025 09:13:46 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 29 May 2025 09:13:46 GMT
USER 1000
# Thu, 29 May 2025 09:13:46 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 29 May 2025 09:13:46 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.2 org.opencontainers.image.version=8.18.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-05-21T16:41:43+00:00 org.opencontainers.image.created=2025-05-21T16:41:43+00:00
# Thu, 29 May 2025 09:13:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99054fed409847690b86b0dcac84715ed5b006a18a3bb8e533d4113c06f833c`  
		Last Modified: Tue, 03 Jun 2025 13:45:29 GMT  
		Size: 60.7 MB (60732571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ab2f5b3c128abd3ddac568b42aa6decb9e623ec4a1e4028fb8a885f335d5f7`  
		Last Modified: Tue, 03 Jun 2025 13:45:09 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d36efa56af13c873870a4736c952893026db879c330676ff7af529b358b61a`  
		Last Modified: Tue, 03 Jun 2025 13:45:25 GMT  
		Size: 437.7 MB (437714109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5843152c678d513172cdad5456085bee588f269760c9e25f3ab82fc90f896837`  
		Last Modified: Tue, 03 Jun 2025 13:45:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c23c31274a9422be3494e6d98b4296c1249b62d2ad9c0896a3c715cd10acc9b`  
		Last Modified: Tue, 03 Jun 2025 13:45:19 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99474d5bc5894fb0f67f82615e2bebc8cffd5053584c30df01cad2c3f0a9af0b`  
		Last Modified: Tue, 03 Jun 2025 13:45:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2259c44d16e864f0504117dd3d9ebf04b9f45e06b3a891751572d522edd2913a`  
		Last Modified: Tue, 03 Jun 2025 13:45:23 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b0c6f08e7d7a50628fc5348983f363e589c3eb8253d473277d897c705bfa96`  
		Last Modified: Tue, 03 Jun 2025 13:45:27 GMT  
		Size: 4.1 MB (4054801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91e2184e69dde9f7cd4d89e78d50326aea1bb2b3d83de1e4d7b1b9fd6dc01de`  
		Last Modified: Tue, 03 Jun 2025 13:45:30 GMT  
		Size: 2.1 MB (2093836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b70fdfec21a0f3893cb12b6a7530245d608ecb2bf302a6e31f6b135098330e`  
		Last Modified: Tue, 03 Jun 2025 13:45:31 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.2` - unknown; unknown

```console
$ docker pull logstash@sha256:2b2eb6c81694b4676bb78dda118f41b2ec24f8a1c7dc07a028bd906f262d4342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3584734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b49b02ed0a0ce8406509039e9a1c68439c73f9dc2574798e16605cc9021ce6`

```dockerfile
```

-	Layers:
	-	`sha256:db58f9f55f37b07d2a9014291ea263c2ed83f313ceea0e5c6cc94cac5b433b65`  
		Last Modified: Thu, 05 Jun 2025 08:00:19 GMT  
		Size: 3.6 MB (3550141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6643356c7b4fd3137b495f359e82b33f3f838d6eedcbaa024fa026135a66f2`  
		Last Modified: Thu, 05 Jun 2025 08:00:16 GMT  
		Size: 34.6 KB (34593 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:62eb19cbc77e2038e1428c56b1a3918dcf65bfc8de46cc3362c8f7ccf14c5044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.2 MB (514209952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b101d65f05f4f8cc0c1322a856c7f77981934795009fd1264e23d87822d144b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Thu, 29 May 2025 09:13:46 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 29 May 2025 09:13:46 GMT
WORKDIR /usr/share/logstash
# Thu, 29 May 2025 09:13:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 29 May 2025 09:13:46 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 May 2025 09:13:46 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 29 May 2025 09:13:46 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 29 May 2025 09:13:46 GMT
USER 1000
# Thu, 29 May 2025 09:13:46 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 29 May 2025 09:13:46 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.2 org.opencontainers.image.version=8.18.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-05-21T16:41:43+00:00 org.opencontainers.image.created=2025-05-21T16:41:43+00:00
# Thu, 29 May 2025 09:13:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9697b390ebee11ef54c775af14d5505fe35e70fcbbe45c69a364d9184e261155`  
		Last Modified: Tue, 03 Jun 2025 14:05:47 GMT  
		Size: 46.2 MB (46214150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ed1102dc0c2330db0223cfc76d34ff60de565ec5522731d27383b34f3ededc`  
		Last Modified: Tue, 03 Jun 2025 14:05:32 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a5719a29cd6912adcdabfa8f537b43dda92efed2da3c7197c7dcfbad28fec3`  
		Last Modified: Tue, 03 Jun 2025 14:06:00 GMT  
		Size: 436.0 MB (435995877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b4bfc20e43d1e195055df78dff6089ef100248d1309d634911dafd7a6d6bf7`  
		Last Modified: Tue, 03 Jun 2025 14:05:49 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d6a43dceab7731e0e0245262852f89c42ec64c9df00222556022dfea2d0d5b`  
		Last Modified: Tue, 03 Jun 2025 14:05:55 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d73045b141429fb3b4195178adc866b55b042270520db4af87cc744209cb1`  
		Last Modified: Tue, 03 Jun 2025 14:05:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72515c404b358eecf21f684debbc943a2b567259e0ad2eb64f7af3e0f8932eee`  
		Last Modified: Tue, 03 Jun 2025 14:06:05 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea31142a21d0afe0d31fe4a63301f112d5c81a7c7306355bfca7cf2f9eb3bc3`  
		Last Modified: Tue, 03 Jun 2025 14:06:08 GMT  
		Size: 4.1 MB (4054801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b626513f77758e2bd3f263f5be60922a003929d617c06e191c90c765787825e`  
		Last Modified: Tue, 03 Jun 2025 14:06:21 GMT  
		Size: 2.0 MB (1960973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54a0bc8531e10a90e5c21d2c3256d261fb0624097907f8bd1219b24eebba257`  
		Last Modified: Tue, 03 Jun 2025 14:06:15 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.2` - unknown; unknown

```console
$ docker pull logstash@sha256:b0591d80d4e8101b850e568714286933fd74cd6d42d352ad09ad79b35ca90777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3584489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec3858909bc3621ae79bf8645482d779e576997395bc5bf90a6c9f41ccdd3aa`

```dockerfile
```

-	Layers:
	-	`sha256:0238e2f0fa92fa580ca57a4b4142dd4bef953515196a7695334bf109c811856f`  
		Last Modified: Thu, 05 Jun 2025 08:00:49 GMT  
		Size: 3.5 MB (3549753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:064356accd60688e8b34cbbf2b5a52af70337cb23015a19e5c1ed19b18b4be54`  
		Last Modified: Thu, 05 Jun 2025 08:00:48 GMT  
		Size: 34.7 KB (34736 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.1`

```console
$ docker pull logstash@sha256:1063f42def9f3b92627c4823620540b55a63d2a22aa51f752f80997977131904
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.1` - linux; amd64

```console
$ docker pull logstash@sha256:3a833ba4ba369da409a5ce7086265489240a1748ff17a3ebf1e4acb9b248dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483389038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560dbf784072c8ae0050bdbaaf4519eb804e67d6b3e49db5e67e0086c7c9fe62`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 09 May 2025 04:49:38 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 09 May 2025 04:49:38 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 09 May 2025 04:49:38 GMT
LABEL url="https://www.redhat.com"
# Fri, 09 May 2025 04:49:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 09 May 2025 04:49:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 09 May 2025 04:49:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 09 May 2025 04:49:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.openshift.expose-services=""
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 09 May 2025 04:49:38 GMT
ENV container oci
# Fri, 09 May 2025 04:49:38 GMT
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Fri, 09 May 2025 04:49:38 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 09 May 2025 04:49:38 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 04:49:38 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Fri, 09 May 2025 04:49:38 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Fri, 09 May 2025 04:49:38 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 09 May 2025 04:49:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 04:49:38 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 09 May 2025 04:49:38 GMT
WORKDIR /usr/share
# Fri, 09 May 2025 04:49:38 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz "https://artifacts.elastic.co/downloads/logstash/logstash-9.0.1-linux-${arch}.tar.gz" &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 May 2025 04:49:38 GMT
WORKDIR /usr/share/logstash
# Fri, 09 May 2025 04:49:38 GMT
USER 1000
# Fri, 09 May 2025 04:49:38 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 09 May 2025 04:49:38 GMT
LABEL org.label-schema.build-date=2025-04-29T15:45:11+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.1 org.opencontainers.image.created=2025-04-29T15:45:11+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 09 May 2025 04:49:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Thu, 15 May 2025 19:24:28 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab07cd1e9f08e3bf815c9738d59d15451b4e64e9436ffef52f5da14bac29fa`  
		Last Modified: Tue, 03 Jun 2025 13:34:34 GMT  
		Size: 5.0 MB (5024894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dc5fabe7b5ee266cd7eb0aaaa0cdf94133b383a1aff0b1419f1cb32cb126c9`  
		Last Modified: Tue, 03 Jun 2025 13:34:42 GMT  
		Size: 436.7 MB (436650340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82ac529e232268a1088200220cae1bdce2b47221d7ee6546866139878363892`  
		Last Modified: Tue, 03 Jun 2025 13:34:34 GMT  
		Size: 2.1 MB (2065798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474f4e0225aa0aa0aac5468a37fc48ba0320be5e82f869afb0a930922ad32808`  
		Last Modified: Tue, 03 Jun 2025 13:34:35 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d0b493dd70aef91973f0e1a3d9ca4c0084fcc0302595cac3e3fa69910c413f`  
		Last Modified: Tue, 03 Jun 2025 13:35:25 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b72815fed3706845fa9145e34e8e891cf3195a13b35b0e88013ff06211a5c0`  
		Last Modified: Tue, 03 Jun 2025 13:34:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a92f55c18c65610061979b2d84a4b417482315d9e6d821792af180ab1a12740`  
		Last Modified: Tue, 03 Jun 2025 13:34:36 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.1` - unknown; unknown

```console
$ docker pull logstash@sha256:06167300950928e38848243166f114a72e342e8e6ae3c39a06cb7922e98842d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83214818eaedf78d5fce1d4ddcf0d07e0a6a4f34f4db38731b0aaa09586cfb55`

```dockerfile
```

-	Layers:
	-	`sha256:18e4582a37146d983a47bde46ad8a7a7d12b1693e8c59ba9783c05706761da49`  
		Last Modified: Thu, 05 Jun 2025 12:12:40 GMT  
		Size: 2.1 MB (2144198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6b915fe8abdcb8c0868153ce6dc8d8a40f523b59a0719976ef4daf627781ea`  
		Last Modified: Thu, 05 Jun 2025 12:12:41 GMT  
		Size: 29.5 KB (29540 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e753ed8eb4e1a98992af349fbf6ac2c38954cb57b45d5ebe945ef304382dfbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.8 MB (479778962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844c7963bc91573861764acb862c9d9275d88680e894f31a1a1956dab6592a90`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 09 May 2025 04:49:38 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 09 May 2025 04:49:38 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 09 May 2025 04:49:38 GMT
LABEL url="https://www.redhat.com"
# Fri, 09 May 2025 04:49:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 09 May 2025 04:49:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 09 May 2025 04:49:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 09 May 2025 04:49:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.openshift.expose-services=""
# Fri, 09 May 2025 04:49:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 09 May 2025 04:49:38 GMT
ENV container oci
# Fri, 09 May 2025 04:49:38 GMT
COPY dir:3fa6b42aa9cb1575a22397e201df9f16228db85fb99450db2e9f8bef40a52c0f in / 
# Fri, 09 May 2025 04:49:38 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 09 May 2025 04:49:38 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 04:49:38 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Fri, 09 May 2025 04:49:38 GMT
LABEL "build-date"="2025-05-14T10:40:32" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Fri, 09 May 2025 04:49:38 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 09 May 2025 04:49:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 04:49:38 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 09 May 2025 04:49:38 GMT
WORKDIR /usr/share
# Fri, 09 May 2025 04:49:38 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz "https://artifacts.elastic.co/downloads/logstash/logstash-9.0.1-linux-${arch}.tar.gz" &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 May 2025 04:49:38 GMT
WORKDIR /usr/share/logstash
# Fri, 09 May 2025 04:49:38 GMT
USER 1000
# Fri, 09 May 2025 04:49:38 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 09 May 2025 04:49:38 GMT
LABEL org.label-schema.build-date=2025-04-29T15:45:11+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.1 org.opencontainers.image.created=2025-04-29T15:45:11+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 09 May 2025 04:49:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9cf99093c2fb01ee3da769d664a9212c42b7d50516f9e77975132a6540ccdf3b`  
		Last Modified: Thu, 15 May 2025 19:25:04 GMT  
		Size: 37.9 MB (37876105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec65e79d68463ea4232f49a6848acfdcc4fe6f349538fd98bb1c810141c8621e`  
		Last Modified: Thu, 15 May 2025 19:38:08 GMT  
		Size: 5.0 MB (5025840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5d198fe1aab5013d1f21610b9f2ccb5329ab79fb4f48ae97b95d3262cd4bbd`  
		Last Modified: Thu, 15 May 2025 19:38:19 GMT  
		Size: 434.9 MB (434935984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69de77aaa68fb90d20854ec8b20c177c3bc5c76be30e445325b99cc8bc7ad6`  
		Last Modified: Thu, 15 May 2025 19:38:08 GMT  
		Size: 1.9 MB (1938131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a39c6dd2b795d5db2c8b86a34668e81ef7601533f1bcfe6eff5f6af7a422913`  
		Last Modified: Thu, 15 May 2025 19:38:08 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db5eddf9b8749b00159567554796217e76ef5657b4b0839d81fba3913576d62`  
		Last Modified: Thu, 15 May 2025 19:38:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7830bddc983ffb9320e893ef12aaa42baa582a218aa642158b64748d95346e38`  
		Last Modified: Thu, 15 May 2025 19:38:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10ef19163cb12d45830257215047c94f74817793839d98b9a82ddfd74ae50ac`  
		Last Modified: Thu, 15 May 2025 19:38:08 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.1` - unknown; unknown

```console
$ docker pull logstash@sha256:252204589c7e276504f517a37d6eaead24b7f68e97413fef09eaa98ea5a87cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2174428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35fcce3f8e6ba21006bf6be864e14744f1577582efb288b5c10c1ac882dfe55`

```dockerfile
```

-	Layers:
	-	`sha256:6c0ed920a4d9fa5a22477efe69dbabd0239dcd965631bed67fa534550fbbe694`  
		Last Modified: Thu, 05 Jun 2025 12:13:24 GMT  
		Size: 2.1 MB (2144770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea0b3307579f7d919ec1434266b5a5c4356737069dde6e34c4c2d5f0ea0f498`  
		Last Modified: Thu, 05 Jun 2025 12:13:25 GMT  
		Size: 29.7 KB (29658 bytes)  
		MIME: application/vnd.in-toto+json
