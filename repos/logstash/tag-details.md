<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.28`](#logstash71728)
-	[`logstash:8.16.6`](#logstash8166)
-	[`logstash:8.17.4`](#logstash8174)

## `logstash:7.17.28`

```console
$ docker pull logstash@sha256:e1462c41e8dca2001e11805df5bf3b856007af7b88cb5436f8275213cebd2076
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
$ docker pull logstash@sha256:92c6155c544067117f34825566c8e59e3a6b4a38bfc83b35b7e20718a1804dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.0 MB (446040736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5ce884935e2ac1ca059e68efd991f100d8b93eb1b12806d2776c013b44ea6e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb01db6dc1b3740bc20e03824d4628f0f418bd66256ecc7924eeb9eb1ff10b6b`  
		Last Modified: Tue, 25 Feb 2025 23:55:19 GMT  
		Size: 45.2 MB (45219399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0424e35676f6ec7c72c69aca0aed12a5e1a492f94b9c5798eb75a60f01abc9d7`  
		Last Modified: Tue, 25 Feb 2025 23:55:17 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf6a3049a27f377393db29513cede80f9e0a5f18ae0e32eab48287fe164aaa8`  
		Last Modified: Tue, 25 Feb 2025 23:55:28 GMT  
		Size: 372.7 MB (372748393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6257b2b970efcfb5860074d122704a20930f06a4be2550a99cf3ca10fc8bc21`  
		Last Modified: Tue, 25 Feb 2025 23:55:17 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b74fb47b9434a518ad7ec6e6c3390fbe8f2676a61e86a0e50e733ba692aef2`  
		Last Modified: Tue, 25 Feb 2025 23:55:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224dc8442929514734ba84928b925193d34ba2843106c068024f04a7b08b4cea`  
		Last Modified: Tue, 25 Feb 2025 23:55:18 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82839b3fe92f6a6a117c8dfbed99c393eca46d8f926f7168ea84b20fbe6095f`  
		Last Modified: Tue, 25 Feb 2025 23:55:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0888ca5549a286ef05f9e9ef1026c8131e06754f35a9a93ebf9a3711016822`  
		Last Modified: Tue, 25 Feb 2025 23:55:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1fc2885bff8cd7de1669590c51fdc64ee2f995ce6b9ab613b96417e079df60`  
		Last Modified: Tue, 25 Feb 2025 23:55:20 GMT  
		Size: 2.1 MB (2094532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2febf965eca2cb279b669a5e13e79b685da7fc64b91506e0e1d291df508bdcbf`  
		Last Modified: Tue, 25 Feb 2025 23:55:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.28` - unknown; unknown

```console
$ docker pull logstash@sha256:0c5943d2bb0879bf1ecbe19093cfa40e7c5cfb57ba24d371197977df96be68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ca0c43ea9b7dfc1c2da377cc4e6e11256ec760c998fd3c497567c3243dbfbc`

```dockerfile
```

-	Layers:
	-	`sha256:e5c2ee4e405e3ee145956e3d96d56461147fd87d979174efc9e995d007101b38`  
		Last Modified: Tue, 25 Feb 2025 23:55:17 GMT  
		Size: 3.3 MB (3339982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a0516240d62014ae19a808626e7051f7d788842ae980f954ebf0fd09e8e831`  
		Last Modified: Tue, 25 Feb 2025 23:55:17 GMT  
		Size: 32.3 KB (32314 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.16.6`

```console
$ docker pull logstash@sha256:2d745205a85a232421284202bc559ce9ac561252f1d2ed3d6b9e53fca6340fbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.6` - linux; amd64

```console
$ docker pull logstash@sha256:c52a4b8750952242340c98ec17354474b0464ea28f5daa1b6fc8716a62f79cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.8 MB (523825779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314eb126f876ea55d48a0e8392835ed16aa9ff10035b5b3cd4cf4ddbfb22ff44`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 25 Mar 2025 08:54:09 GMT
ARG RELEASE
# Tue, 25 Mar 2025 08:54:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Mar 2025 08:54:09 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 08:54:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 08:54:09 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.6 org.opencontainers.image.version=8.16.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-03-19T17:10:56+00:00 org.opencontainers.image.created=2025-03-19T17:10:56+00:00
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a3e9b0273756f2a006bbc1bd16e60046fd0c22727c80ee9f8a420a532a341`  
		Last Modified: Wed, 09 Apr 2025 01:19:56 GMT  
		Size: 51.9 MB (51850374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f8ba0e39a008e6cd6a1ff7f37c3e647cf5a4c290ab95830451caa0a7953709`  
		Last Modified: Wed, 09 Apr 2025 01:19:55 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403183b40dbb52f307ae25bee1ff926f7739b2feb7bb6ab3a31bc6a244a37350`  
		Last Modified: Wed, 09 Apr 2025 01:20:02 GMT  
		Size: 438.3 MB (438310470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739a7c18da6211c07ae0585fa533337c474856138cdcdb4814c5225d165e39a5`  
		Last Modified: Wed, 09 Apr 2025 01:19:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193bd179822cbfccfb821ccf7605dbf979980de7ef723145d98a710b00df63f9`  
		Last Modified: Wed, 09 Apr 2025 01:19:56 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a1c1701e878d07419c67d7b0f87e867e2e59e5af3d5aabd9d8a4b473b6a1a6`  
		Last Modified: Wed, 09 Apr 2025 01:19:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfefb56a4d4f98f3ba5366cc953eb95231f126d6cdecc347d8e93ef52345ab00`  
		Last Modified: Wed, 09 Apr 2025 01:19:56 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5eb30dd278e7f6066a9e551a40995d75d1639bce252f56a9421621058a137f`  
		Last Modified: Wed, 09 Apr 2025 01:19:57 GMT  
		Size: 4.1 MB (4054502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d240d5a84cb568e6f00fd58a57da5fb99eba9ad0f7336ec588257dfa3004ae6`  
		Last Modified: Wed, 09 Apr 2025 01:19:57 GMT  
		Size: 2.1 MB (2093570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26f3d9d249c743bd437f7fe590ea5dfc663cdd31b463fb0042e3670d3c2788b`  
		Last Modified: Wed, 09 Apr 2025 01:19:57 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.6` - unknown; unknown

```console
$ docker pull logstash@sha256:9394a2104e811259c67e5ef5616eb6a39e07219536705b725ddc07fd333477db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68d4f8b600bc088a9b376b89099734c797854e2c4ed390578685751863fe17c`

```dockerfile
```

-	Layers:
	-	`sha256:378b66425fd49cfa974d36d944579426f24dc7569cbace6a8ed87aed68ab7e31`  
		Last Modified: Wed, 09 Apr 2025 01:19:55 GMT  
		Size: 3.5 MB (3519286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe503edb78fdc7f6099195110deaccdbae769a44de9b4e2d007ef7c987934baa`  
		Last Modified: Wed, 09 Apr 2025 01:19:55 GMT  
		Size: 34.6 KB (34593 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:28b9c9cb697a5721d340c64920233a8951435c95524c28227b4b1cac5061b61f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.9 MB (513916007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ebc0a6ec951a55d112e49d10f11d9f684c066d96ddb3d913b5b7dac0ccf4fa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 08:54:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 08:54:09 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.6 org.opencontainers.image.version=8.16.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-03-19T17:10:56+00:00 org.opencontainers.image.created=2025-03-19T17:10:56+00:00
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992eb71d1a3781cc39688c56ea6aee6aba021d05f3ebb3409c6befcaccca1d2`  
		Last Modified: Tue, 25 Mar 2025 19:54:04 GMT  
		Size: 45.3 MB (45326096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a087d2afbe4d0f3f89a791aeaf11cdaf6ae77949ec7fe66f01c6cafbe39da741`  
		Last Modified: Tue, 25 Mar 2025 19:54:02 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591065cbe07c9ee71e2b82cf32b81dcb7b8fca4cb2c09e170dfd149386408efc`  
		Last Modified: Tue, 25 Mar 2025 19:54:15 GMT  
		Size: 436.6 MB (436594078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971c9b3682921d9a7bcd35680994331e80901c5f0b996ddb38e83844d4618e77`  
		Last Modified: Tue, 25 Mar 2025 19:54:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a73389368d795f43904ff5ccc2d2c55717bfefe889ec1bf0bff8c42c661d9c9`  
		Last Modified: Tue, 25 Mar 2025 19:54:03 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f3c56e92f87df3d97bfc5ff6e741f2112b20065017d4caaf2b9ba9f816a619`  
		Last Modified: Tue, 25 Mar 2025 19:54:04 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd21411802df91049703d2a8ac609be2a6d8aaa3cf2193aef233ad51351796b`  
		Last Modified: Tue, 25 Mar 2025 19:54:04 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178e0c24c8dd84f4b4ccaea59d16930ef195451aa02f4b9320abaaf1840cb41c`  
		Last Modified: Tue, 25 Mar 2025 19:54:05 GMT  
		Size: 4.1 MB (4054502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02d3e33ab38d96da3c165e7ddd5024b7e51f472d1e0fecd28829b53401b2916`  
		Last Modified: Tue, 25 Mar 2025 19:54:06 GMT  
		Size: 2.0 MB (1961022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2af904b7968987eb1f370d75fbb68fc3924dab9a2450d45e3794e0bd0421ea5`  
		Last Modified: Tue, 25 Mar 2025 19:54:06 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.6` - unknown; unknown

```console
$ docker pull logstash@sha256:e6a339f91664ee76d89375118ba7ef1357ca08c4289624b05d2e33a73de02f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8ac7a278c3add75416d26757e1b125889c36059cf4a887584fa1d88c3c6c42`

```dockerfile
```

-	Layers:
	-	`sha256:5995e68816cb367228893d3279fa24caa062d96975b1ed56896231cb7475c7f0`  
		Last Modified: Tue, 25 Mar 2025 19:54:03 GMT  
		Size: 3.5 MB (3519652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b24bfa9229cadda9b1b4079f5a0c74215526614226b2996fabcd86c023dd246`  
		Last Modified: Tue, 25 Mar 2025 19:54:02 GMT  
		Size: 34.7 KB (34736 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.17.4`

```console
$ docker pull logstash@sha256:985699153c24ad2cda3cf46c528522f300c048df0dc1deb069fb8277bd51081e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.4` - linux; amd64

```console
$ docker pull logstash@sha256:e547e50d6cb000be7973e0231fbcc67cbf9ae8c0d4d10240b02d053a3e8ff699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524202850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013d0114419ebdde885295ac639ea554c6ff4b616d21500ff16fa693b73bf177`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 25 Mar 2025 09:28:57 GMT
ARG RELEASE
# Tue, 25 Mar 2025 09:28:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Mar 2025 09:28:57 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Mar 2025 09:28:57 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 09:28:57 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 09:28:57 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.4 org.opencontainers.image.version=8.17.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-03-19T17:05:46+00:00 org.opencontainers.image.created=2025-03-19T17:05:46+00:00
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958e4478a1e9ec1f46fe70dd654efb777e5dc7b3939ed336407e11d49db836e6`  
		Last Modified: Wed, 09 Apr 2025 01:20:11 GMT  
		Size: 51.9 MB (51850253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ccd2411948c6ebb996febb5a620a3ef3663c24611de6786fc882cfcd086351`  
		Last Modified: Wed, 09 Apr 2025 01:20:10 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba944652d1442f341e3ab55b17c9f21805bd9d1de3d514343b8e0cf48bdb129`  
		Last Modified: Wed, 09 Apr 2025 01:20:19 GMT  
		Size: 438.7 MB (438687672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c508b5082fa09bebdeae0bc10ec7a0e37df2722d7b9f8ac07440ec3b5c93c498`  
		Last Modified: Wed, 09 Apr 2025 01:20:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0146e846f2a8308cdf691480d27aea876f8b29593dfebe38b8d95134843b28`  
		Last Modified: Wed, 09 Apr 2025 01:20:11 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaf0a3eba924c562d21c8faee785ff87e877e4de4cb3b0222e79d28ffbd891d`  
		Last Modified: Wed, 09 Apr 2025 01:20:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39131559be1b40bd5e028a98563835312b2a67fc8e15cb22481ff7806e20ec79`  
		Last Modified: Wed, 09 Apr 2025 01:20:12 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41429a1e55f3b139c2bd2353832ab093e4f78183ab75c3d0d466fe5779a48bd6`  
		Last Modified: Wed, 09 Apr 2025 01:20:12 GMT  
		Size: 4.1 MB (4054503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cd4a99596be6147f29cf608e761f866aefb469c773cbb846c48f87ca0ee9ac`  
		Last Modified: Wed, 09 Apr 2025 01:20:13 GMT  
		Size: 2.1 MB (2093559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399fbe13ad2d723ab4d24d7f2331d421b4939eb2d5568d61372b66b3bab2a023`  
		Last Modified: Wed, 09 Apr 2025 01:20:13 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.4` - unknown; unknown

```console
$ docker pull logstash@sha256:bc8cfe0e813587ab38e280a6605f717e383ca1913936d0079919df1a2914443b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0333a6c9d8c866682fef2258ec3131fcf68205b9da73ceced115d95837206f`

```dockerfile
```

-	Layers:
	-	`sha256:8ff74c829e85a5d6c7772c7bd9d57c6a60386491c31da006bfde46b1aecd5168`  
		Last Modified: Wed, 09 Apr 2025 01:20:11 GMT  
		Size: 3.5 MB (3510229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aca4e3136d8e8d0afbfb04289bb4afc33acc7e41543284e111aca2644334161e`  
		Last Modified: Wed, 09 Apr 2025 01:20:10 GMT  
		Size: 34.6 KB (34593 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c9778e8d23d7505ea092a9759f5ec7224e3138fff28bc270f43c65187fd5f7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514301761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1d90d5292fec33398dcaed78d5be8c795f01008da0b2248da0a5dbce85a117`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 09:28:57 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 09:28:57 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.4 org.opencontainers.image.version=8.17.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-03-19T17:05:46+00:00 org.opencontainers.image.created=2025-03-19T17:05:46+00:00
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992eb71d1a3781cc39688c56ea6aee6aba021d05f3ebb3409c6befcaccca1d2`  
		Last Modified: Tue, 25 Mar 2025 19:54:04 GMT  
		Size: 45.3 MB (45326096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a087d2afbe4d0f3f89a791aeaf11cdaf6ae77949ec7fe66f01c6cafbe39da741`  
		Last Modified: Tue, 25 Mar 2025 19:54:02 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2963477387999b0a6718114d6d90c6fc7c2ece88bebc93683ef7e7da6a05328`  
		Last Modified: Tue, 25 Mar 2025 20:05:52 GMT  
		Size: 437.0 MB (436979845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4caa99343280868689f053bf38e94660333b930ef263c9e1f03cb14794d4573`  
		Last Modified: Tue, 25 Mar 2025 20:05:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7439fc7befb6e184d447e2c3431e528a1c4dc17b5e7638f270031d86ce702f33`  
		Last Modified: Tue, 25 Mar 2025 20:05:42 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa6d9c09294db6892278ed7613a698c685f3b0546bed4451a2dab39bc1fa3e3`  
		Last Modified: Tue, 25 Mar 2025 20:05:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292d22a0c516af252c68b2820c402dcf9858b08b50bb14610e84331bae15c33c`  
		Last Modified: Tue, 25 Mar 2025 20:05:43 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bb81fe4f3164444952da6b04e82cd43de9d9db463d5b0c10352c41a649ff56`  
		Last Modified: Tue, 25 Mar 2025 20:05:44 GMT  
		Size: 4.1 MB (4054500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a828670b0d5fb6c366688550025864af69f29b98e0e91c912224c406f3c99d22`  
		Last Modified: Tue, 25 Mar 2025 20:05:44 GMT  
		Size: 2.0 MB (1961020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3919be392294b3a8d2e5abbc1f23a63587e22740da81fdd181f3c16c256b07`  
		Last Modified: Tue, 25 Mar 2025 20:05:44 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.4` - unknown; unknown

```console
$ docker pull logstash@sha256:d31fb8d5c259b6b0fba04112274ea32b148799e24914d5d44e7be8459f37ef07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350c2e5ca43a36930e8d0e6ad3ab35b52471aff054e74522bac7ee2544dda215`

```dockerfile
```

-	Layers:
	-	`sha256:dfdf643d9e6e09712e0d5e756e7bd4efd2e40826ee1fa839234facb93923a345`  
		Last Modified: Tue, 25 Mar 2025 20:05:43 GMT  
		Size: 3.5 MB (3510595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090317d302296d4577b1a9464d2c12761778b763903b8f30fff09ef122762f64`  
		Last Modified: Tue, 25 Mar 2025 20:05:42 GMT  
		Size: 34.7 KB (34736 bytes)  
		MIME: application/vnd.in-toto+json
