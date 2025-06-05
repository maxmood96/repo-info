<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.28`](#logstash71728)
-	[`logstash:8.17.6`](#logstash8176)
-	[`logstash:8.18.2`](#logstash8182)
-	[`logstash:9.0.2`](#logstash902)

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

## `logstash:9.0.2`

```console
$ docker pull logstash@sha256:a4b3cdce2d08e9f53cf9ee6224481ab0f84bb8dbea254edb5aba3d0cc917fad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.2` - linux; amd64

```console
$ docker pull logstash@sha256:845b4fbe43143b4a0078b0b2cf07ab4cf3b4979b708f52e75e743dc80595e51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.2 MB (482247945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e962a9df27821ddc10967b0257d5cc8fbf25dcb32546badef1f24944564ceefa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 14 May 2025 10:36:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 14 May 2025 10:36:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 14 May 2025 10:36:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 14 May 2025 10:36:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 14 May 2025 10:36:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 14 May 2025 10:36:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 14 May 2025 10:36:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 14 May 2025 10:36:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 14 May 2025 10:36:11 GMT
ENV container oci
# Wed, 14 May 2025 10:36:11 GMT
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Wed, 14 May 2025 10:36:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 14 May 2025 10:36:11 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 10:36:11 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 14 May 2025 10:36:12 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Thu, 05 Jun 2025 06:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Jun 2025 06:03:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 06:03:26 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Jun 2025 06:03:26 GMT
WORKDIR /usr/share
# Thu, 05 Jun 2025 06:03:26 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz "https://artifacts.elastic.co/downloads/logstash/logstash-9.0.2-linux-${arch}.tar.gz" &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Jun 2025 06:03:26 GMT
USER 1000
# Thu, 05 Jun 2025 06:03:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL org.label-schema.build-date=2025-05-26T15:41:48+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.2 org.opencontainers.image.created=2025-05-26T15:41:48+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Jun 2025 06:03:26 GMT
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
	-	`sha256:8fb850d8bfdba457df243c3b831e128c735ea119b47ba0122dea5ca5a7c17e68`  
		Last Modified: Thu, 05 Jun 2025 17:28:52 GMT  
		Size: 5.0 MB (5024890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9fcecc04f73152b4f9d0728a5d034c0d0652cecab194f78c4364f3b4db2a7f`  
		Last Modified: Thu, 05 Jun 2025 19:04:29 GMT  
		Size: 435.5 MB (435509243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11ab2695c98304bb2c47bddaf53a0ff1f5454f80ed846a0908a75dec42ec31f`  
		Last Modified: Thu, 05 Jun 2025 17:28:51 GMT  
		Size: 2.1 MB (2065810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35a2be82c8e184d24b5b8c4c05060647248fce94c36a8371e465119a5982fee`  
		Last Modified: Thu, 05 Jun 2025 17:28:51 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cb70ae230dc0c9323f4b1c72312ad81be523260b1e2eb405e3deec6ec3fe73`  
		Last Modified: Thu, 05 Jun 2025 17:28:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6da653dcff5e7c8f0ea7c9efdbb500a632bf4d91916335c41f1df5739449a0`  
		Last Modified: Thu, 05 Jun 2025 17:28:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7025c6f341c2cdd74a3e077c1d4e35a52ce4e0f82e49ab12a8a022f76ddf7e4`  
		Last Modified: Thu, 05 Jun 2025 17:28:52 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.2` - unknown; unknown

```console
$ docker pull logstash@sha256:3eb90b2ceb0e8fd8a9d65e8bdf265a1e28317a007705b22c8219070ba265ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934618ea87f1edc3895f86b665898701c1dac8b105058490d73bb0635f1a3900`

```dockerfile
```

-	Layers:
	-	`sha256:837dfee128922c3abb4def72ecc492053794ead5690278e56d38bbfdb201852b`  
		Last Modified: Thu, 05 Jun 2025 18:53:29 GMT  
		Size: 2.1 MB (2137191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1f837d3725fa01096c14a939a14835d7120e158065f395ab54f287fa3354897`  
		Last Modified: Thu, 05 Jun 2025 18:53:30 GMT  
		Size: 29.5 KB (29540 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:0f5a67d3a95887b5a6d3ffe47ec25ee3315e2f6ec2609079d61fc1022c9ee023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.6 MB (478637436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff34188012a76dd36a51d735df834991582579116a7da94f96b5d199a40c393`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 14 May 2025 10:40:48 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 14 May 2025 10:40:48 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 14 May 2025 10:40:48 GMT
LABEL url="https://www.redhat.com"
# Wed, 14 May 2025 10:40:48 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 14 May 2025 10:40:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 14 May 2025 10:40:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 14 May 2025 10:40:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.openshift.expose-services=""
# Wed, 14 May 2025 10:40:48 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 14 May 2025 10:40:48 GMT
ENV container oci
# Wed, 14 May 2025 10:40:49 GMT
COPY dir:3fa6b42aa9cb1575a22397e201df9f16228db85fb99450db2e9f8bef40a52c0f in / 
# Wed, 14 May 2025 10:40:49 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 14 May 2025 10:40:49 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 10:40:50 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 14 May 2025 10:40:50 GMT
LABEL "build-date"="2025-05-14T10:40:32" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
# Thu, 05 Jun 2025 06:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Jun 2025 06:03:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 06:03:26 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Jun 2025 06:03:26 GMT
WORKDIR /usr/share
# Thu, 05 Jun 2025 06:03:26 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz "https://artifacts.elastic.co/downloads/logstash/logstash-9.0.2-linux-${arch}.tar.gz" &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
WORKDIR /usr/share/logstash
# Thu, 05 Jun 2025 06:03:26 GMT
USER 1000
# Thu, 05 Jun 2025 06:03:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL org.label-schema.build-date=2025-05-26T15:41:48+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.2 org.opencontainers.image.created=2025-05-26T15:41:48+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 05 Jun 2025 06:03:26 GMT
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
	-	`sha256:a3f3cf24b66532ae06cdec8d1de53a019f3ad8400e49827fc87c9f6647864760`  
		Last Modified: Thu, 05 Jun 2025 17:38:06 GMT  
		Size: 5.0 MB (5025817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a59bf917c3f93c54fc218c41d1c10ea3ad7faab430946858b5c030606bf3e9`  
		Last Modified: Thu, 05 Jun 2025 19:49:40 GMT  
		Size: 433.8 MB (433794473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a226cd8d14f5591cd0f30210d988dc41b6fd771604dcb225c2b53aa96e23e8`  
		Last Modified: Thu, 05 Jun 2025 17:38:13 GMT  
		Size: 1.9 MB (1938138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc1b59316c25bcdbc26e32d14f72912e932724e5f8ceeaaa49a8df4777cbb25`  
		Last Modified: Thu, 05 Jun 2025 17:38:10 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387ecae820c80a011a13e5c21115640eaf5562609c10b9312e175c2cbff5907d`  
		Last Modified: Thu, 05 Jun 2025 17:38:12 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9077694f9cd448db44206213da2f5b6bf983e1de154fe74a9ddaaab15639dda`  
		Last Modified: Thu, 05 Jun 2025 17:38:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64a23f9be105c842f99b29869a7e84c836a9c92de6d33607daac420ef6df912`  
		Last Modified: Thu, 05 Jun 2025 17:38:11 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.2` - unknown; unknown

```console
$ docker pull logstash@sha256:71f90a5a7630d06ad24e88fd3146bb9d857a59fa62eac72034bc0c8d009e1831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a2bd69b4c47eea6172990c7bbc9e194c04c9c0907031c4816618b5aa117cef`

```dockerfile
```

-	Layers:
	-	`sha256:e2bd958427d12399113fb548a4eca924ddee4460f3102fa7bc8246eb1d3c078a`  
		Last Modified: Thu, 05 Jun 2025 18:53:34 GMT  
		Size: 2.1 MB (2137763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:288fe86e16def7485444b433410657e76ed3b50d0c36cb28e66257fc435d6c06`  
		Last Modified: Thu, 05 Jun 2025 18:53:35 GMT  
		Size: 29.7 KB (29658 bytes)  
		MIME: application/vnd.in-toto+json
