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
$ docker pull logstash@sha256:ed1c3fa1bfd6097f0fee231d781d3aaa5d8e60fbdd7b62694fd4c6f8cce80b19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.2` - linux; amd64

```console
$ docker pull logstash@sha256:748fa2b87a8f1c98af0a28718d07a55e0ca741da7e10020f3f72be7c39307363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.2 MB (482233932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604cb90943f81eb29d9b893a827508078fc54d6578dc508a94e560de64d85c61`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL url="https://www.redhat.com"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Jun 2025 06:03:26 GMT
ENV container oci
# Thu, 05 Jun 2025 06:03:26 GMT
COPY dir:bac616b15ea24c824075e7e76d7146b6c91b244abd89c8cc5c4ec0f5677c20ac in / 
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL "build-date"="2025-06-09T17:19:15" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e18551b8a7ac3e7aa6347d84b9f0b5c8cc8fe52" "release"="1749489516"
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
	-	`sha256:cd6ccba083d707ef742eaac8378ef1580e2dfd96b8e9198ff1681af8b60dcdf5`  
		Last Modified: Mon, 09 Jun 2025 18:09:32 GMT  
		Size: 39.6 MB (39630845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2617e9f9b84b4daf3131b31b478151bded287b496efd0452511ff3cc0823afd3`  
		Last Modified: Wed, 11 Jun 2025 04:11:49 GMT  
		Size: 5.0 MB (5024866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaa15a3cc8feee670a4bc2a173b8f5e518c698525ec85192ff751a7ead1a533`  
		Last Modified: Wed, 11 Jun 2025 04:12:26 GMT  
		Size: 435.5 MB (435509502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dde9bf64eb5844708a16336efac5d5538e6d73999e76c281d4f26fb6acaef7`  
		Last Modified: Wed, 11 Jun 2025 02:27:28 GMT  
		Size: 2.1 MB (2065817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b2fc3ee87b180242bfe15a39e0e118a70168e316a0b2fb69c476f083d464f`  
		Last Modified: Wed, 11 Jun 2025 02:27:38 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6a1f4ab4e459b3cf28bf953a204cdc776cf0b2ba22c7aa34f789605a099ab6`  
		Last Modified: Wed, 11 Jun 2025 02:27:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850990f7396487dc16bae80bafe5e8239f0b4b8c081de8dc9197c5500697b8c3`  
		Last Modified: Wed, 11 Jun 2025 02:27:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a021dd132c83f218077e172c76e7f70de96266d42b27509916c9d9c7b0004725`  
		Last Modified: Wed, 11 Jun 2025 02:27:47 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.2` - unknown; unknown

```console
$ docker pull logstash@sha256:c80c58222fe48fb64252d6cdf213ba34aee82478e1780e1fc0c17f35c7a2b34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0909709a18b803e835f6a299c968b7ee3b0e46b2af206d0c2d9933a3ba4322b7`

```dockerfile
```

-	Layers:
	-	`sha256:09d9ba2102ffb6a9225b24940dc2bdd68daf0aac8f121a875ad8f26aee4ca0fa`  
		Last Modified: Wed, 11 Jun 2025 03:53:20 GMT  
		Size: 2.1 MB (2134174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3215370f47268eabb65c065e19980b5af194193d53d2d22d956bb9092878a6`  
		Last Modified: Wed, 11 Jun 2025 03:53:20 GMT  
		Size: 29.5 KB (29540 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:25617b975af0c28b75dbdb0aaab7af83ed956128fe2349e1f4bc85ef05e77acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.7 MB (478682414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeef6dcc485a38d7129200216b657c2cff3a640ff12d47664012d014bfdde05`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL url="https://www.redhat.com"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Jun 2025 06:03:26 GMT
ENV container oci
# Thu, 05 Jun 2025 06:03:26 GMT
COPY dir:dd3dc18ab466569b07043336c84190595a673cf78699fcf70dbf83deddf44d87 in / 
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL "build-date"="2025-06-09T17:24:02" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e18551b8a7ac3e7aa6347d84b9f0b5c8cc8fe52" "release"="1749489516"
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
	-	`sha256:f258ee7f14ce0e3998c50b14ce17a0c0115edefcb69d96c3ef016548422246c8`  
		Last Modified: Mon, 09 Jun 2025 18:09:34 GMT  
		Size: 37.9 MB (37922296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fcf0ad241392ebec42d2be6e272a59362236753957f89e948515f40b696be4`  
		Last Modified: Tue, 10 Jun 2025 17:49:36 GMT  
		Size: 5.0 MB (5025459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d5c21b0e3860a92366981412ed373cbbc1fec7ad6dda6b6f953dc693ead9ca`  
		Last Modified: Thu, 12 Jun 2025 04:54:37 GMT  
		Size: 433.8 MB (433793596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5546ddb997cb66604877877f44ef8e566509b3e8f62390afeda7136e018ab8ba`  
		Last Modified: Wed, 11 Jun 2025 23:12:27 GMT  
		Size: 1.9 MB (1938159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5124711d3dda2d26ccac96edfa1043328cc9294578a62ad522e881c43320201`  
		Last Modified: Wed, 11 Jun 2025 23:12:27 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4e1361bfb93c922a29dd140d3c5bb79598b08698eb7658e43241540f85d357`  
		Last Modified: Wed, 11 Jun 2025 23:12:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0051c16577f824f071d369d4127f88cad96205f1026bada66fd831aacd3e5009`  
		Last Modified: Wed, 11 Jun 2025 23:12:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5be0e2436eb76a0a7c1c7c5d22d72b4a3dfa5decf90cf644e79d457ec65dce5`  
		Last Modified: Wed, 11 Jun 2025 23:12:29 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.2` - unknown; unknown

```console
$ docker pull logstash@sha256:55674423224ce2d7f5d4f7dfd65aacf4aa19fd8cf53bce1529799ddf4bb8bcb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178669181074613cb164eb81718b506dea426d6f63d280d57c26788ee13d6b65`

```dockerfile
```

-	Layers:
	-	`sha256:514e53075854885f067f91a529c1c2484ccc1d75f6b2ea5bca897b7522cc8f68`  
		Last Modified: Thu, 12 Jun 2025 00:53:22 GMT  
		Size: 2.1 MB (2134746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20470341d3e63178d5cc1195e92a850458490104cdda614595d441804aa5c8b6`  
		Last Modified: Thu, 12 Jun 2025 00:53:23 GMT  
		Size: 29.7 KB (29659 bytes)  
		MIME: application/vnd.in-toto+json
