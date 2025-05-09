<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.28`](#logstash71728)
-	[`logstash:8.17.6`](#logstash8176)
-	[`logstash:8.18.1`](#logstash8181)
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
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0a9a0e49135760c6a5a55434b15ef272724426e7de6411c257d97c07fcca25`  
		Last Modified: Wed, 09 Apr 2025 01:19:59 GMT  
		Size: 51.8 MB (51841555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c5b47f107cb437e2f453681cdeca9d03ecc8d375fd74e43d80a2237ae016a1`  
		Last Modified: Wed, 09 Apr 2025 01:19:57 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8a7f4d067a7abcb2c49699d87582c262281c77c63e818e6b7d59df9cc04837`  
		Last Modified: Wed, 09 Apr 2025 01:20:07 GMT  
		Size: 376.0 MB (375953820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee541d0097e99be72865fbccd04549f39c9cb518f245fe6d781febadbdc4da`  
		Last Modified: Wed, 09 Apr 2025 01:19:57 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e536a7c74e6de920dd9b20e9e7db18d9b00e58d1fe32492e22cd1653b518c2`  
		Last Modified: Wed, 09 Apr 2025 01:19:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6519c9c72daf7bf8c99a9ddce0319e78a0329578d14e0057a1973f60958997`  
		Last Modified: Wed, 09 Apr 2025 01:19:59 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f6811998c4c02a3234880408af19ac1cbf568c353e5b3d9c9075be45157964`  
		Last Modified: Wed, 09 Apr 2025 01:19:59 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d36d0f262466d0248eabd85512cae7e928f427baf771105234fb7fe314026`  
		Last Modified: Wed, 09 Apr 2025 01:20:00 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af7627aa24218b689af904fe683c729682abf5773144e11b986d432a201cf54`  
		Last Modified: Wed, 09 Apr 2025 01:20:01 GMT  
		Size: 2.1 MB (2094543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b5bcc60c98b2a2be4f6d6338fd08f33a6a1ca50eaf6ca47e294be513a244b5`  
		Last Modified: Wed, 09 Apr 2025 01:20:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Wed, 09 Apr 2025 01:19:58 GMT  
		Size: 3.3 MB (3338992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e48fd86aca853c5dd96ae3beb0a3ff6063a7129647ec8d31fd3ae6808e91fc`  
		Last Modified: Wed, 09 Apr 2025 01:19:57 GMT  
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
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0939b7441eaba115b97c3db22600a75f8a6b389cd1e4fd73f8bc862248af1807`  
		Last Modified: Wed, 09 Apr 2025 08:26:26 GMT  
		Size: 39.0 MB (39010198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d596e9398c708ab58590ffdc6322e2aff73fcb4a9fb693efc6be081a048efd1`  
		Last Modified: Wed, 09 Apr 2025 08:26:25 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d88adde7b488546cae09abfe3a08fee78e0893e310cf8dd27467a82b741140d`  
		Last Modified: Wed, 09 Apr 2025 08:26:35 GMT  
		Size: 372.7 MB (372748625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5365133754261c5f87817063987eb918df86c3699d09ad200a0793747759f00`  
		Last Modified: Wed, 09 Apr 2025 08:26:25 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909bb53a563e678c1a801b62d307dae1dc0173738c2fe4414ef2fea1fa53e25f`  
		Last Modified: Wed, 09 Apr 2025 08:26:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b08c2d477f11420408969f1b97a6d8ac214cef78063686b28b6a109a0b79a`  
		Last Modified: Wed, 09 Apr 2025 08:26:26 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0c0b535add31d7def3ab14bc0b2d07468a62e3b52b0bfbb8316f5f5f7cbeaa`  
		Last Modified: Wed, 09 Apr 2025 08:26:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dbec348d3d7a0a3d8110e46340315b3916fa6da0e675ffaf17adcb6e9f8bc6`  
		Last Modified: Wed, 09 Apr 2025 08:26:27 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd9c1eb0c5a30657cc2e0218881cc32e3749f5f8b198afcce6c389f7e62eb17`  
		Last Modified: Wed, 09 Apr 2025 08:26:28 GMT  
		Size: 2.1 MB (2094544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6750cfeb851dc339e2df67372c88e0733072cab3df91a1b7f77083b7d49b2bb5`  
		Last Modified: Wed, 09 Apr 2025 08:26:28 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Wed, 09 Apr 2025 08:26:26 GMT  
		Size: 3.3 MB (3339228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77dcb4c11329f0b60d058bea97ede94e6062e9a4e15813a67d79aabbd5fd3b21`  
		Last Modified: Wed, 09 Apr 2025 08:26:25 GMT  
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
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197edc6bd3269011b533cbb7e8b3639c64725dd1f2ed5f3848c64681ec85675`  
		Last Modified: Fri, 09 May 2025 19:02:08 GMT  
		Size: 52.4 MB (52382230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57744598d88c8308ed6f2232d34a60c26f5cd3a823b4bf1efd36a0f26b0ebe3d`  
		Last Modified: Fri, 09 May 2025 19:02:07 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4931bfdcbcf711f42edb943ac87b6d8d71934ddb693ff0baad3315dde065fb`  
		Last Modified: Fri, 09 May 2025 19:02:16 GMT  
		Size: 438.8 MB (438815223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9fe70b51275531f8bc5f9a283be24ad76ba33ba2328727e14e1faa266a6a33`  
		Last Modified: Fri, 09 May 2025 19:02:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903735ecb6e30a318046fe5702a51045bc861b1acb2762c0bf79a43ade8f5e0`  
		Last Modified: Fri, 09 May 2025 19:02:08 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322b56efd943035bbbca06fd39512f1381b7ff7b2ea3776799e514669963ae6`  
		Last Modified: Fri, 09 May 2025 19:02:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f115783a195dcdd598214fc98b3b4fc10ee765d238dd1c1d05ba4795d21fe43`  
		Last Modified: Fri, 09 May 2025 19:02:09 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a909bc506cb68cb0b16cbc500c014f8fc4b43cf1e7f5e3764b1e55d1aa60215`  
		Last Modified: Fri, 09 May 2025 19:02:09 GMT  
		Size: 4.1 MB (4054809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0002094c59b881d05c49afff486ee4cc0842710b828ff5db705bccb8ed593daf`  
		Last Modified: Fri, 09 May 2025 19:02:09 GMT  
		Size: 2.1 MB (2093835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7e90aeb95044c7a697ad900eb9d9cdd562073851fe3c1a46c2fdfed87ae7f5`  
		Last Modified: Fri, 09 May 2025 19:02:10 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Fri, 09 May 2025 19:02:07 GMT  
		Size: 3.5 MB (3512306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:785590c45c0c784b5bef23e7194f9e21c139065e61f99a4596ae3dcc65e03dc2`  
		Last Modified: Fri, 09 May 2025 19:02:07 GMT  
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
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d67c1bd3c9da18476c361a404d289c14a3b659b3c9838eeb5fb76622ca373c0`  
		Last Modified: Fri, 09 May 2025 20:41:15 GMT  
		Size: 39.2 MB (39161298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadbe60a13b17a898594fb205d68343531555f48df7c2212f4ad5839fe3fa0fe`  
		Last Modified: Fri, 09 May 2025 20:41:14 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dca1e3bd6ad14a562fa2d1dd9a6066890780a5f1dfbd740d1f4c1c2accbc3a1`  
		Last Modified: Fri, 09 May 2025 20:41:23 GMT  
		Size: 437.1 MB (437100383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565da4f09eb262a7e9ca0d54a7ed648299b45ce8e4d16efb63faef836ff83d6`  
		Last Modified: Fri, 09 May 2025 20:41:14 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3498a07a7d8380a4b6872023d11762b63d02a1a59c4f806424f8a4842d4cab8e`  
		Last Modified: Fri, 09 May 2025 20:41:15 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c12209273b3011f85ea2e5f3dc17b7e2d3283b5b2204fcb09205615c795e6d`  
		Last Modified: Fri, 09 May 2025 20:41:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b645e99c4f66d782c419b59f507576deb9947c4ddde5e690d1709add872805`  
		Last Modified: Fri, 09 May 2025 20:41:16 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7ffba4e26570d8e7096752e917e130dc6c9ad745ca7585988a993ada6ff9d0`  
		Last Modified: Fri, 09 May 2025 20:41:16 GMT  
		Size: 4.1 MB (4054808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e81f7bd61af1261e69b9411c4f662a67100d0ff81e7805c28bc5411d3634cf3`  
		Last Modified: Fri, 09 May 2025 20:41:17 GMT  
		Size: 2.0 MB (1960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf97055b212574556533682cde6b49535d3fd0df750cf96486d3c6d5df9000ce`  
		Last Modified: Fri, 09 May 2025 20:41:17 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Fri, 09 May 2025 20:41:14 GMT  
		Size: 3.5 MB (3511918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781fd046b71bbfccb1f6674d89cd234bb4015bf3bdbeb5c70b9107b9d6caa627`  
		Last Modified: Fri, 09 May 2025 20:41:14 GMT  
		Size: 34.7 KB (34736 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.18.1`

```console
$ docker pull logstash@sha256:14001930ab723f9451fe3d286325d233dd4e12093bbcc66a5d928e14f7d9907c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.1` - linux; amd64

```console
$ docker pull logstash@sha256:9322b38f17ed5b3010da32e3b62a5d7bd9723d660e8b9680593c98c2fbabc4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.9 MB (524900277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b62172e94fcba5c5c6f20ed869bed06b748e58cfb06587e453c37a75c31b4f7`
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
# Tue, 06 May 2025 09:07:22 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 06 May 2025 09:07:22 GMT
WORKDIR /usr/share/logstash
# Tue, 06 May 2025 09:07:22 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 09:07:22 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 09:07:22 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 06 May 2025 09:07:22 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 06 May 2025 09:07:22 GMT
USER 1000
# Tue, 06 May 2025 09:07:22 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 06 May 2025 09:07:22 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.1 org.opencontainers.image.version=8.18.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-04-29T15:58:41+00:00 org.opencontainers.image.created=2025-04-29T15:58:41+00:00
# Tue, 06 May 2025 09:07:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268f1602eebdf71583dd7b9c0fbed2f51ee4c9c423e733d98f8f619bc9a3d31d`  
		Last Modified: Fri, 09 May 2025 19:01:46 GMT  
		Size: 52.4 MB (52382220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b348fca76a503225574ee4359a8664f2d4849d9542c85253d09cd2b876099e61`  
		Last Modified: Fri, 09 May 2025 19:01:45 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a427a3fe2804f9f501d7cbea5db71b140f229bbcb74139f420c46fc76a0e29`  
		Last Modified: Fri, 09 May 2025 19:01:53 GMT  
		Size: 438.9 MB (438852548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03756776bbaaab525af974fcf9e96983220e34ec4e88628a0bf7ae1c0034afb6`  
		Last Modified: Fri, 09 May 2025 19:01:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc8d16af1e0cca4b31d6ecfaa2a7f8c3d166eded28e2f87c57c897d28807223`  
		Last Modified: Fri, 09 May 2025 19:01:46 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a586bd4ddfdc1fc03d16efce3e2d0a855c9575cf035284c3571a180e7e73a9`  
		Last Modified: Fri, 09 May 2025 19:01:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd62b493bba0d157764165b2222222c43196181452330b55e698f20ba537abdd`  
		Last Modified: Fri, 09 May 2025 19:01:47 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c45fb955b3f15cf0a570bc38289968293fc64036bada92d105a87347170715`  
		Last Modified: Fri, 09 May 2025 19:01:47 GMT  
		Size: 4.1 MB (4054802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf880e9409270fe5099053f891ebc8de33fda6a28ca65e49990b803c3e2e068`  
		Last Modified: Fri, 09 May 2025 19:01:48 GMT  
		Size: 2.1 MB (2093834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1e094e4ae3b5cd6b2bbf1fca306298a8129f70db265eba498788689afbb3d1`  
		Last Modified: Fri, 09 May 2025 19:01:48 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.1` - unknown; unknown

```console
$ docker pull logstash@sha256:2a3c17f6f75f14586f6e913e49c4f928dca44d327360122164b5e683567a6479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c425ab5a2a77021b15d7e5a83bda51ff4509ce0759b8e039c1136da5fee878`

```dockerfile
```

-	Layers:
	-	`sha256:9b8c13c92bb8b5a4394a8d9a5b379d8f32f19b9ee5113f7933c75693f7cd826b`  
		Last Modified: Fri, 09 May 2025 19:01:45 GMT  
		Size: 3.5 MB (3512867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f908ce42481a74989b0eeb60048ca72a7fbc43570b540b6541a657e431ca52`  
		Last Modified: Fri, 09 May 2025 19:01:45 GMT  
		Size: 34.6 KB (34593 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:0720b51d6781226d0bd7cfebef438a6d14b5b7f122ce8599b4a2eda636bd99dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.3 MB (508296821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b25160d1258da4821b6cc04220e0248d0d7afc772cd6f3cb3272190386e0050`
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
# Tue, 06 May 2025 09:07:22 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 06 May 2025 09:07:22 GMT
WORKDIR /usr/share/logstash
# Tue, 06 May 2025 09:07:22 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 09:07:22 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 09:07:22 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 06 May 2025 09:07:22 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 06 May 2025 09:07:22 GMT
USER 1000
# Tue, 06 May 2025 09:07:22 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 06 May 2025 09:07:22 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.1 org.opencontainers.image.version=8.18.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-04-29T15:58:41+00:00 org.opencontainers.image.created=2025-04-29T15:58:41+00:00
# Tue, 06 May 2025 09:07:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d67c1bd3c9da18476c361a404d289c14a3b659b3c9838eeb5fb76622ca373c0`  
		Last Modified: Fri, 09 May 2025 20:41:15 GMT  
		Size: 39.2 MB (39161298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadbe60a13b17a898594fb205d68343531555f48df7c2212f4ad5839fe3fa0fe`  
		Last Modified: Fri, 09 May 2025 20:41:14 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc0fd237f4965ccced130683490d0282313ec5ecdf4b467ad241e0d429536ba`  
		Last Modified: Fri, 09 May 2025 20:42:58 GMT  
		Size: 437.1 MB (437135614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9df98e1d06ee4ccbf454a18ca0a7e34c4103af7801e81058aaec4da79d010b`  
		Last Modified: Fri, 09 May 2025 20:42:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d9ccb9eb84cf7efa486f51d3c94a3a569f069042773ac0d343696c851c829a`  
		Last Modified: Fri, 09 May 2025 20:42:47 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721a755204ba729be392d9c8432ea9f0e73da3cc441017598a12b4c977019f83`  
		Last Modified: Fri, 09 May 2025 20:42:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141cd838d4dd8d6d3baa36cf2357dab3122f23ec961e25f3db21309b2fcf7769`  
		Last Modified: Fri, 09 May 2025 20:42:48 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f110a51e4dcdf871ff7728aaead84cab7e992ab207dcf928db64dd3699aa248`  
		Last Modified: Fri, 09 May 2025 20:42:49 GMT  
		Size: 4.1 MB (4054802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4147bb07fbe08d9ef3d0ecc7b6d4a00ce0150315d2daf2e6539a094c717d93`  
		Last Modified: Fri, 09 May 2025 20:42:49 GMT  
		Size: 2.0 MB (1960970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f621ac7ed6b090c0e61c5d75e8bb642f55dbc4ffe4fc6be912c4f7a3e8d4b88`  
		Last Modified: Fri, 09 May 2025 20:42:49 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.1` - unknown; unknown

```console
$ docker pull logstash@sha256:8ca7853afa74cc67685ba2944ac51bc8c1facce3b5348a76c58bf44c2696fa93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241edc5d7f67a8a944b30d033270249059e2f62161d627b94dfa9804f5805206`

```dockerfile
```

-	Layers:
	-	`sha256:d81d69a563b6c2ff3055c06866299722ffd3304672e6b28ec8648d94387195aa`  
		Last Modified: Fri, 09 May 2025 20:42:48 GMT  
		Size: 3.5 MB (3512479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9953585e6c0d0fea69b854d4562b541cb17c1cd5b72f38db0af85d7d42f8a5f6`  
		Last Modified: Fri, 09 May 2025 20:42:47 GMT  
		Size: 34.7 KB (34736 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.1`

```console
$ docker pull logstash@sha256:41fa5940adc61a384119248bfb5c205c593d7e88527b45a38e9c5a3ed372e0fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.1` - linux; amd64

```console
$ docker pull logstash@sha256:50838649f6d9dabaf177004408ad299e94acfa2347aa0e117f64a94f0bdb8cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483447001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351d0980e90d37d8a5ae776c7596f8cf779dde31080079c07fafd4bba25235d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL url="https://www.redhat.com"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Apr 2025 15:46:09 GMT
ENV container oci
# Mon, 28 Apr 2025 15:46:09 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Mon, 28 Apr 2025 15:46:09 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 28 Apr 2025 15:46:09 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 15:46:10 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 28 Apr 2025 15:46:10 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Mon, 28 Apr 2025 15:46:10 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
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
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Mon, 28 Apr 2025 16:55:19 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b941810ae245ec8384bebcba894f4295d8c538516b663d00d9e0aa3b5fae1dc`  
		Last Modified: Fri, 09 May 2025 19:01:52 GMT  
		Size: 5.0 MB (5013399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab7f0bab9e0ff6fb473932bf9ab24d7185a80a33f0dee25c927daf17b6d7a9e`  
		Last Modified: Fri, 09 May 2025 19:02:02 GMT  
		Size: 436.7 MB (436650338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab873e1da3ccaaaa0db781fb47b12ba1de1d12ce516769ab4d46c93775b852d`  
		Last Modified: Fri, 09 May 2025 19:01:52 GMT  
		Size: 2.1 MB (2065801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c69526233f588661410bac7c295a64360bf201488524175387abacd45af3`  
		Last Modified: Fri, 09 May 2025 19:01:52 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd245714571a9b6d48dea962fa2787b9e39f17341aba2b371076214da1a821`  
		Last Modified: Fri, 09 May 2025 19:01:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d0a8a02d32e6b3d9b5ee1b632a78cc203fa045d936515ced305bcb12f113be`  
		Last Modified: Fri, 09 May 2025 19:01:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a0eae2dc5040ab57d53036ea9c6de4047d62668df1dddf1606920234ccb97`  
		Last Modified: Fri, 09 May 2025 19:01:53 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.1` - unknown; unknown

```console
$ docker pull logstash@sha256:13164aeda07ce90de62191d7d3b8e996a69f7ef964178b69d99d3ddec778f1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b08b38974492d50bb5a7fd33ecaf1d9c31fe55525e6a8483bc0f0a027995c43`

```dockerfile
```

-	Layers:
	-	`sha256:18197e5854d5e88aff4d21a57342a3e7fe7a677a261f4f67159e9a64619eafc4`  
		Last Modified: Fri, 09 May 2025 19:01:52 GMT  
		Size: 2.1 MB (2111736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b99d5d5f7416e88e199702543d293fb74cc24c5f8d330064bce25967168e7a`  
		Last Modified: Fri, 09 May 2025 19:01:51 GMT  
		Size: 29.5 KB (29540 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:d82ed451ab5a386ac7262a7e59f90ca2ed4fdcd5bbb124d1e97ffd024f43d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.8 MB (479783135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2402dbe20523f99cb47e8cf2964e8fe3250d9c9582ed97e3d41dc0ecc9aece7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL url="https://www.redhat.com"
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Apr 2025 15:48:53 GMT
ENV container oci
# Mon, 28 Apr 2025 15:48:53 GMT
COPY dir:37e2781211ed66b85e838f75f63c4036aeedc358075b7ac677bbe4ad43998692 in / 
# Mon, 28 Apr 2025 15:48:54 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 28 Apr 2025 15:48:54 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 15:48:54 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 28 Apr 2025 15:48:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Mon, 28 Apr 2025 15:48:54 GMT
LABEL "build-date"="2025-04-28T15:48:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
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
	-	`sha256:2aa6bd15812764b98217de512ddcd6b7fc8cb96437e1fa30d7963118dce559ff`  
		Last Modified: Mon, 28 Apr 2025 16:55:35 GMT  
		Size: 37.9 MB (37887470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50247513b05ecc658fb095a955e2e7086d1c19387a0fa2565657e4645247930`  
		Last Modified: Fri, 09 May 2025 20:44:23 GMT  
		Size: 5.0 MB (5018571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1115678972952fdf75407544511b3d17e466f1f8d8dbd1e614f46626cb2a662c`  
		Last Modified: Fri, 09 May 2025 20:44:32 GMT  
		Size: 434.9 MB (434936057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7883c94e885cf3630fa495c669f69d188b5ff09a01c9ce9478c6eae16805815`  
		Last Modified: Fri, 09 May 2025 20:44:24 GMT  
		Size: 1.9 MB (1938130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2691d8f6d1519d3eac4fea6929909ccf6722065b92d178ededac82d31ecfa9a`  
		Last Modified: Fri, 09 May 2025 20:44:23 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14959bd57c8fe955515d7048b873492f83ea943f0ccf740ddc73356faf1f65fe`  
		Last Modified: Fri, 09 May 2025 20:44:24 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a51c8641b497072f5d384a741de80bf5f54eeac399ec7050bbd1cdab46e8ce`  
		Last Modified: Fri, 09 May 2025 20:44:25 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752437b31ac7adad20ad1054e9187aac815dc6a27f02b3c72b0d639be0f2c147`  
		Last Modified: Fri, 09 May 2025 20:44:25 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.1` - unknown; unknown

```console
$ docker pull logstash@sha256:b0a2bcc15b1c1ed8429d6718573538d1db449d68d7c75b6856fc49cdae215623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0276eec99357aaf5be09c20c10c688368c9965d4ae0823ba41e0031bdb09742`

```dockerfile
```

-	Layers:
	-	`sha256:25bfe36a8c3bb217d9bb51525d5a26c605d783179c8312e053e2a62b5b756d98`  
		Last Modified: Fri, 09 May 2025 20:44:23 GMT  
		Size: 2.1 MB (2112131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f03a10c59fad5f677e98e7dde8e3c396f1f0a75305889fefd6700e88b5c0c5a`  
		Last Modified: Fri, 09 May 2025 20:44:23 GMT  
		Size: 29.7 KB (29657 bytes)  
		MIME: application/vnd.in-toto+json
