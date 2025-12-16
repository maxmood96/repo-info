<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.18.8`](#logstash8188)
-	[`logstash:8.19.8`](#logstash8198)
-	[`logstash:9.1.8`](#logstash918)
-	[`logstash:9.2.2`](#logstash922)

## `logstash:8.18.8`

```console
$ docker pull logstash@sha256:f2608dcb12d14d3aa4a3aad470bbcac1f5cc391baa64a0c560f41a70c7e514b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.8` - linux; amd64

```console
$ docker pull logstash@sha256:0c561a809266e5787e59e27cf7c10ad53a51d695aa01464b3fe1fe3447f28303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.8 MB (525824723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2d032d949a350fca05beb8a66e8387d7e95d55153b47169c374c5c5c97d650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Thu, 13 Nov 2025 23:28:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:56 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:37 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:37 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:37 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:37 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:38 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:38 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Thu, 13 Nov 2025 23:29:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd79b80ccaa55c41f750c02665aedad9405ced41da54b49d0be9208fd2d5d6`  
		Last Modified: Thu, 13 Nov 2025 23:30:45 GMT  
		Size: 49.0 MB (49030452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429834f6c7f98c2abc9f1c4742c85442daf5653762f7a26de93eb462bac346df`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1e8a17be130a7f1d7217bdb655fd8126de4f651453d3d6e89436d6d1d342b0`  
		Last Modified: Fri, 14 Nov 2025 02:26:54 GMT  
		Size: 441.0 MB (440981473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d1fa58ef233269bc32839e4f818d021168cb0c6e80e0200148f4c3cff15b0f`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30fbcc4fda19e49a762266e0e6faded74b019c5aabdb92f222341949c77a44c`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20a0b4ac67d42cb574f5eb946d234c5257b40c6b153f029dc385f75f6a8ce2a`  
		Last Modified: Thu, 13 Nov 2025 23:30:37 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c249e208f213784ac2ece9cea2b943c597c3cf702e90c5f37cb445217ed81`  
		Last Modified: Thu, 13 Nov 2025 23:30:37 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb233dac8d41e821577474435b7f1a1769b4bee17a2e45734d903c3eb6bcf0c`  
		Last Modified: Thu, 13 Nov 2025 23:30:41 GMT  
		Size: 4.0 MB (4004180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a382d3f5355e9be2f82d6625b36b3a8e72685cfcf41b1b116ca460e6b39b4efe`  
		Last Modified: Thu, 13 Nov 2025 23:30:37 GMT  
		Size: 2.1 MB (2078022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664a3632afa8063325511c3e4f4995f36e06390039e1a84893ebdd91e574e018`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:2b0556efd6d5028087e0dcb7eaf140ae64c164864695dd5a4180bb4eb6872d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ace81df77812ed20bb2a9d7277e0e88c0e1c9da9ee07e7bf541d544ece1077f`

```dockerfile
```

-	Layers:
	-	`sha256:e9a099deaf531ca02082a6f0b37812c340b9e4419acc44f046dcd834a9c26c2c`  
		Last Modified: Fri, 14 Nov 2025 01:53:26 GMT  
		Size: 3.7 MB (3657663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d73e810d46eba1a1728c1b8064af55f67a3a2dc44d3da8cf9c8664068be48f`  
		Last Modified: Fri, 14 Nov 2025 01:53:26 GMT  
		Size: 34.6 KB (34608 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:eda3d8c0f02db1a48df7826ed5a096b0c5331594e5a6f67397e8c5a9614cc57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.0 MB (524967182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b14e7870f762fbe697e10861bb87bb433bb4d7176d2ea76762c64a6d2ad8fc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Thu, 13 Nov 2025 23:28:31 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:14 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:14 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Thu, 13 Nov 2025 23:29:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e2941a2ca4b19bbd5b2b6121b4d7ea76e18d66621a65bc2b69892a6695274a`  
		Last Modified: Thu, 13 Nov 2025 23:30:10 GMT  
		Size: 50.9 MB (50920587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92811a7a0282e3c3ac478c27030a0833d205ecfa3722d637ff310259ff4c61cd`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46880e8efe89d131f1fcef7fbbc1bac25b066a52c522510ea5a4d54905c43408`  
		Last Modified: Fri, 14 Nov 2025 02:27:30 GMT  
		Size: 439.2 MB (439248985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e816dbf151b745cf877898cf1f38eb5d1e9fdba9cb829677c7db3f51e2356a`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd8b3a2856c46ef6c5fc08409f79704e1e152daf357e774a4112e9a0e6e3310`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38a53e225d75eff12773ef054757fc3c918925e9c6a254255a6abae89b9454d`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0611631f79d04d18e50936612a7f2ed8941206427eb741095e883b9554d5abd9`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1c7deb1dda72ff0ea0be3b4ec4a75470d63cdc3b774dbbed0ce150ef7c8aa6`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 4.0 MB (4004181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769e7b7e10a84cb8c18514c4fb229e6085c41326be9344426201b72d03d95cb`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.9 MB (1925573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7261f1bc119d985222300eb703ac17b3f85ef3be1d2b7c59548d52b1931610`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:282ec9c8c443d33ce1d7b8ae801910caf07e84f50e12b7640d560cce877f10f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc02dbb43679cc9148cb7874de46881ffa09231366dd245364e0924316feaec`

```dockerfile
```

-	Layers:
	-	`sha256:eb2724933da0910479dfd0de4d69f32aaede2048f786924e0754d75f1a82048a`  
		Last Modified: Fri, 14 Nov 2025 01:53:31 GMT  
		Size: 3.7 MB (3658088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff2be8520e57438521bdce72e162db54d896d0333fd5b8b4a3e65312794eb7f`  
		Last Modified: Fri, 14 Nov 2025 01:53:32 GMT  
		Size: 34.8 KB (34752 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.8`

```console
$ docker pull logstash@sha256:97e6e30db9a6fb65c80209eb68d1061b181843493d94ba2182cf165abc8fa144
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.8` - linux; amd64

```console
$ docker pull logstash@sha256:becf6ffcd89d11456d21d5e17aaf0488c7c48c220f0969c4b0c410e4119a1fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526514136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3044a5876030745933f5c19dc351925ae325db656907d5db68607fd741063763`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Tue, 02 Dec 2025 18:19:01 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 02 Dec 2025 18:19:01 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 02 Dec 2025 18:19:23 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Dec 2025 18:19:23 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Dec 2025 18:19:23 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 18:19:23 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:19:23 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 02 Dec 2025 18:19:23 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 02 Dec 2025 18:19:24 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 02 Dec 2025 18:19:24 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 02 Dec 2025 18:19:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 18:19:24 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 02 Dec 2025 18:19:24 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 02 Dec 2025 18:19:24 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 18:19:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 02 Dec 2025 18:19:24 GMT
USER 1000
# Tue, 02 Dec 2025 18:19:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Dec 2025 18:19:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.8 org.opencontainers.image.version=8.19.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-11-25T19:46:58+00:00 org.opencontainers.image.created=2025-11-25T19:46:58+00:00
# Tue, 02 Dec 2025 18:19:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcff2319986ac972a60ad3f23916dbdd53bdda0a260b9d64f163abc3fbf4ad19`  
		Last Modified: Tue, 02 Dec 2025 18:20:22 GMT  
		Size: 49.3 MB (49298232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a08ab36e794dd2c65d67e96212ae66d8866586abf75c6eb6a6a20770ffff4d`  
		Last Modified: Tue, 02 Dec 2025 18:20:16 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c74ed6bed7b8adf3502d6f2a4cbdc35582c45a9b4c65980f461e7f38b590d4`  
		Last Modified: Tue, 02 Dec 2025 18:22:37 GMT  
		Size: 441.4 MB (441401245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac087d4eea783185a413b3b29c84b7f308ccdbfdd6ace26537117b65b63e79b`  
		Last Modified: Tue, 02 Dec 2025 18:20:16 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4352238f613b90f01790a722989621c9547c42a5536ae95557ef30239de9f`  
		Last Modified: Tue, 02 Dec 2025 18:20:16 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b5f6fb22717311d04a107c0132a800ef7ea906b97a5e8aa43c7217c1a55568`  
		Last Modified: Tue, 02 Dec 2025 18:20:16 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b991a6df071a3c0fb87dc07b83bc4244cd5a0d809c1af4267e6e9eb9ee5a8717`  
		Last Modified: Tue, 02 Dec 2025 18:20:16 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62de6b26d9539910d01ca420163ade79cbaf6467657c7af04d1c07c45cc9a57d`  
		Last Modified: Tue, 02 Dec 2025 18:20:16 GMT  
		Size: 4.0 MB (4005443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76e6cff87043e31435ce6d19d66d6519b4c03d3cc0f074a7bfa71cf30d63999`  
		Last Modified: Tue, 02 Dec 2025 18:20:17 GMT  
		Size: 2.1 MB (2078628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e33469e2bd262aa5971e4f1463d77cb878bd23ad4dad4c395fa9bdcd60f9ca6`  
		Last Modified: Tue, 02 Dec 2025 18:20:16 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.8` - unknown; unknown

```console
$ docker pull logstash@sha256:b833e31d02d5519260c0511e1efdfce1687c162df17fef01a9f49fbc784a3d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbd28284c692610fe55ef6c76b3e56dd736b0182e8829dada75eeca7b94914f`

```dockerfile
```

-	Layers:
	-	`sha256:2677e9438dd9a97edca214e1f7e798fc5e06d6f1e1df71392c319844bbd49635`  
		Last Modified: Tue, 02 Dec 2025 19:53:22 GMT  
		Size: 3.7 MB (3653224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2833fced09814b5ab8cf5d745eadb2270956d13e9f99491b991045a0b487a765`  
		Last Modified: Tue, 02 Dec 2025 19:53:26 GMT  
		Size: 34.6 KB (34613 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:3165395cc88c930a44d10ca48e57201bd78efb0247cb2a15ee81cd81c2bdddf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.8 MB (525835229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f574d535960118dabc1bcf683e122a443630884f96ab72ce60376611e074f14`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Tue, 02 Dec 2025 18:19:53 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 02 Dec 2025 18:19:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 02 Dec 2025 18:20:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Dec 2025 18:20:14 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Dec 2025 18:20:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 18:20:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:20:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 02 Dec 2025 18:20:15 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 02 Dec 2025 18:20:15 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 02 Dec 2025 18:20:15 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 02 Dec 2025 18:20:15 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 18:20:15 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 02 Dec 2025 18:20:15 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 02 Dec 2025 18:20:15 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 18:20:15 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 02 Dec 2025 18:20:15 GMT
USER 1000
# Tue, 02 Dec 2025 18:20:15 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Dec 2025 18:20:15 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.8 org.opencontainers.image.version=8.19.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-11-25T19:46:58+00:00 org.opencontainers.image.created=2025-11-25T19:46:58+00:00
# Tue, 02 Dec 2025 18:20:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584f1ed2bdaec4367d78d17f65457fcb89781437955bb7805daf0696771b98df`  
		Last Modified: Tue, 02 Dec 2025 18:21:25 GMT  
		Size: 51.3 MB (51343626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5ca49bfce62bd95707b66a5a4648340c9b6ff1720ebb6dfa3cd0a31b4cfcfa`  
		Last Modified: Tue, 02 Dec 2025 18:21:15 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2bd8a5f8c02eca4c02c9537551c634d9fd94a8b821e8e21bff2c86b1dfb4cb`  
		Last Modified: Tue, 02 Dec 2025 21:57:48 GMT  
		Size: 439.7 MB (439691810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b103141fd7d02bae3792bfdccf929f40bf8dbb04faa0f862fb924967a09a017`  
		Last Modified: Tue, 02 Dec 2025 18:21:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4557200dc51519fc44d07e8852fe7d8222add26a3111cfc781fa429da8fff3`  
		Last Modified: Tue, 02 Dec 2025 18:21:15 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec89a70dc61e136b69d4c0094cf6dcaa60a8b9b43e01b75ae174d24777d9ae97`  
		Last Modified: Tue, 02 Dec 2025 18:21:15 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c2dde747ad6e6bfc39342924df96a6d35477743a64fa9f42e5d8166f8508f`  
		Last Modified: Tue, 02 Dec 2025 18:21:16 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf56552476b485f52384e025d0887ccaf4f3fdf35ca95cf0a4c20fa4081397b`  
		Last Modified: Tue, 02 Dec 2025 18:21:16 GMT  
		Size: 4.0 MB (4005435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11622fb208e6380d525c3fd563725b6bd1ba5554088da1eeed2bd0db72f48ce6`  
		Last Modified: Tue, 02 Dec 2025 18:21:16 GMT  
		Size: 1.9 MB (1926497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f328cc1a45f0cab2ef3ec79a66782271161a886308e4d9134c55faab0a04120`  
		Last Modified: Tue, 02 Dec 2025 18:21:16 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.8` - unknown; unknown

```console
$ docker pull logstash@sha256:3e85f646dc4b48762b35210855955db3c8da5755863c1c5b97fc3e951a7920d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e8c69206b1ed3ae29f44a2abff1b1df0363bbe7f1b0d798cf6536d382be1bb`

```dockerfile
```

-	Layers:
	-	`sha256:aaf7e5509b614ce87c6e0085b37ee9f86dd297223ff57a76d3e5bac61018f343`  
		Last Modified: Tue, 02 Dec 2025 19:53:31 GMT  
		Size: 3.7 MB (3653649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b6ce2a088301d5e84708f9a9af2a4c43bdbd03a30592fdaf5cbb26b4203492`  
		Last Modified: Tue, 02 Dec 2025 19:53:32 GMT  
		Size: 34.8 KB (34756 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.8`

```console
$ docker pull logstash@sha256:82372275ff845b17714fcf390b6588786e0356474a4f2d0b76e294adf501e0b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.8` - linux; amd64

```console
$ docker pull logstash@sha256:527b42003805007484c82e227d49ad818957636c79ad9600ee06273b4997dabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.6 MB (477615917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debdf57d476a5e038255e315a01fe6dd300c87563f09c6f1dd5daf6fb8328388`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Tue, 09 Dec 2025 01:27:55 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Dec 2025 01:27:55 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:27:55 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Dec 2025 01:27:55 GMT
WORKDIR /usr/share
# Tue, 09 Dec 2025 01:28:03 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 09 Dec 2025 01:28:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Dec 2025 01:28:51 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 09 Dec 2025 01:28:51 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 09 Dec 2025 01:28:52 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 09 Dec 2025 01:28:52 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 09 Dec 2025 01:28:52 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:28:52 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Dec 2025 01:28:52 GMT
USER 1000
# Tue, 09 Dec 2025 01:28:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Dec 2025 01:28:52 GMT
LABEL org.label-schema.build-date=2025-11-25T19:41:48+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.8 org.opencontainers.image.created=2025-11-25T19:41:48+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 09 Dec 2025 01:28:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027ffd0478e85b0d6637f5566dcd7bbec02cf673f108dcc05bf2338863cf46b7`  
		Last Modified: Tue, 09 Dec 2025 01:29:42 GMT  
		Size: 5.2 MB (5153909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff2419917384d4046f526cb92552597d5d7317044cfc2fcedad3597b7e7c6ba`  
		Last Modified: Tue, 09 Dec 2025 01:29:52 GMT  
		Size: 430.3 MB (430339500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864b40ad88d67586cda90fc6c08cacf4ffe9b91e1c9cbe31c5fb739d8103bab`  
		Last Modified: Tue, 09 Dec 2025 01:29:42 GMT  
		Size: 2.1 MB (2078844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ede7c05bc0ccdcc93f029915fd04331390b5ddf5741bc9c563f28df02d0ac1`  
		Last Modified: Tue, 09 Dec 2025 01:29:41 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c9a4da92377efebb450f54c4caa9f9cba754608ae3bb87cc85855449e18053`  
		Last Modified: Tue, 09 Dec 2025 01:29:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0936afda2d47599b165b93499207c466ff1212bfac2749d67f22e930e1fa873c`  
		Last Modified: Tue, 09 Dec 2025 01:29:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc00536a85239e836a11064293d1c6aff82e454a5a8f71a7a0dd15cb2aede34a`  
		Last Modified: Tue, 09 Dec 2025 01:29:41 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.8` - unknown; unknown

```console
$ docker pull logstash@sha256:e058123c342970ed107d881a32a8126c5bfc684828fedc38a1620de54e802ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163c880b7445c350314349a9ade2b510c862088faba3a1a74f135572662f337d`

```dockerfile
```

-	Layers:
	-	`sha256:eead1b8eb320200f4762d1c798b8af410c4c5f4de1c2372a6fe4dfb6ea265b45`  
		Last Modified: Tue, 09 Dec 2025 04:53:29 GMT  
		Size: 2.1 MB (2090561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588558b656097cf5b5a7c45de433aad53f7a2f54b497371092bc55095c98f6b1`  
		Last Modified: Tue, 09 Dec 2025 04:53:30 GMT  
		Size: 29.6 KB (29554 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:5a42681c45e231e6b34bddd281dd7e3ea03ebfb332bedd52609daeb400b11615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.9 MB (473920453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b933197165bc672b6f03d026505cf3d04bcab8addc9438514100bbd697403c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Tue, 09 Dec 2025 02:17:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Dec 2025 02:17:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:17:57 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Dec 2025 02:17:57 GMT
WORKDIR /usr/share
# Tue, 09 Dec 2025 02:18:05 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 09 Dec 2025 02:18:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Dec 2025 02:18:58 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 09 Dec 2025 02:18:58 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 09 Dec 2025 02:18:58 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 09 Dec 2025 02:18:58 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 09 Dec 2025 02:18:58 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:18:58 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Dec 2025 02:18:58 GMT
USER 1000
# Tue, 09 Dec 2025 02:18:58 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Dec 2025 02:18:58 GMT
LABEL org.label-schema.build-date=2025-11-25T19:41:48+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.8 org.opencontainers.image.created=2025-11-25T19:41:48+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 09 Dec 2025 02:18:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187b1540e06d4aee6e751d4cc0c7a0108bbee187095119e0dfdf7821c346b00`  
		Last Modified: Tue, 09 Dec 2025 02:19:50 GMT  
		Size: 5.2 MB (5153628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29010967f42008bd26973841110f319ecbc10185b473366eb37232968540dbd8`  
		Last Modified: Tue, 09 Dec 2025 02:21:23 GMT  
		Size: 428.6 MB (428614246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126cf3f2cad9e50431fd84e5e8b268a2d39edb49971ab04842e525cddf1ba84`  
		Last Modified: Tue, 09 Dec 2025 02:19:50 GMT  
		Size: 1.9 MB (1926850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2af92de8aad79a891d9239319a6be196ca7595cb0ca64bc9cc2b6bd3cdaace6`  
		Last Modified: Tue, 09 Dec 2025 02:19:50 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e76c48932b13d965cd2f7334f3ac5d59aee7dafe6966fc8336d2c5f28dc30c`  
		Last Modified: Tue, 09 Dec 2025 02:19:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e4596d32cfaffe8f5cb2e89fc199e17a83531911fc0b65d60c71d16085714`  
		Last Modified: Tue, 09 Dec 2025 02:19:50 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3790f6ae5d416df5b4f777f83b76972fd92e28669cb396c2e98a7a2a9d9a9d`  
		Last Modified: Tue, 09 Dec 2025 02:19:50 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.8` - unknown; unknown

```console
$ docker pull logstash@sha256:46e4f94c0bfa3f9791a8293cab317d6bb963e71376c40b8e1174728208c57e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1688f621a28a728a546d4eccd2724036a486bcd537d9c7a444385cc5af3d47d5`

```dockerfile
```

-	Layers:
	-	`sha256:bb480a0210ceabbad5e4c98894fceeebe6649923a5ccffa4f302f04a244ce854`  
		Last Modified: Tue, 09 Dec 2025 04:53:33 GMT  
		Size: 2.1 MB (2091131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f423912c9a9ea05c76dcddf01401915de9505e68c8b93516a53a36a8130b7907`  
		Last Modified: Tue, 09 Dec 2025 04:53:34 GMT  
		Size: 29.7 KB (29671 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.2`

```console
$ docker pull logstash@sha256:6bba2d363f46569b6e21c57c490dc93d2f526d9972293dab1e89d8ab913063ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.2` - linux; amd64

```console
$ docker pull logstash@sha256:7440d0614267a42f7037930ab927b85dc9e35144fae531f016c3c7898473a8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487925255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e921df81928f207eb321e3670f8c2becd7805ab6e342a3e35ce84890132fc0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Tue, 09 Dec 2025 01:27:55 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Dec 2025 01:27:55 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:27:55 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Dec 2025 01:27:55 GMT
WORKDIR /usr/share
# Tue, 09 Dec 2025 01:28:03 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 09 Dec 2025 01:30:38 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Dec 2025 01:30:38 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 09 Dec 2025 01:30:38 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 09 Dec 2025 01:30:38 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 09 Dec 2025 01:30:38 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 09 Dec 2025 01:30:38 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:30:38 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Dec 2025 01:30:38 GMT
USER 1000
# Tue, 09 Dec 2025 01:30:38 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Dec 2025 01:30:38 GMT
LABEL org.label-schema.build-date=2025-11-25T19:42:51+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.2 org.opencontainers.image.created=2025-11-25T19:42:51+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 09 Dec 2025 01:30:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027ffd0478e85b0d6637f5566dcd7bbec02cf673f108dcc05bf2338863cf46b7`  
		Last Modified: Tue, 09 Dec 2025 01:29:42 GMT  
		Size: 5.2 MB (5153909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3893ff17811d15fd485f957838cb8ab20f7db73c2d630f3839e12a6332080bb6`  
		Last Modified: Tue, 09 Dec 2025 01:32:32 GMT  
		Size: 440.6 MB (440648847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0553c6a24d82e90ca3c3b81e6b2521a7f1ce3ab569ddb408363da4a3679edea4`  
		Last Modified: Tue, 09 Dec 2025 01:31:28 GMT  
		Size: 2.1 MB (2078836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c670f179733d27edc422dd3ddae477deef93ad5eda33ffb10d635efccd4d1c3a`  
		Last Modified: Tue, 09 Dec 2025 01:31:27 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb51b82465436d18e71895a4eca55f46d7415cafad4fa5f91b58fb852be3de47`  
		Last Modified: Tue, 09 Dec 2025 01:31:27 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5da194ef8cbd236672fb8b4e8bbacebea732113e2f717d4cbd9568ff272fac`  
		Last Modified: Tue, 09 Dec 2025 01:31:27 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5230a3e99272981493c645324d21319f71558d05e7398f4172fefd688853bc`  
		Last Modified: Tue, 09 Dec 2025 01:31:27 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.2` - unknown; unknown

```console
$ docker pull logstash@sha256:6ac5357bef5f8912a63f6a31c8bf794ad04289fc19611dc1b3b7e8842faa348b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150d6b07a06b535ec864cc063b12ca8739cca0c77e5e72cc3f5a240a88e57635`

```dockerfile
```

-	Layers:
	-	`sha256:4724088f06e0773d235fe6bcb5cd164469bfb74da6097ebd779a49c74ccf52cb`  
		Last Modified: Tue, 09 Dec 2025 04:53:38 GMT  
		Size: 2.1 MB (2100381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9db1f7fe0853c571afe32d526d7b75c48d174ec85eea75725927732201dc61`  
		Last Modified: Tue, 09 Dec 2025 04:53:39 GMT  
		Size: 29.6 KB (29602 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:6767e4e82c8b01c2ff63bb07e65beb34cb1731403f471abb3df5b4dcc22314cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.2 MB (484223468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d06efc3ca516beae66029a9a2e05924da3e8002559edd6eaef498210d2b768`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Tue, 09 Dec 2025 02:18:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Dec 2025 02:18:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:18:48 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 09 Dec 2025 02:18:48 GMT
WORKDIR /usr/share
# Tue, 09 Dec 2025 02:18:55 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 09 Dec 2025 02:19:46 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Dec 2025 02:19:46 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 09 Dec 2025 02:19:46 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 09 Dec 2025 02:19:46 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 09 Dec 2025 02:19:46 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 09 Dec 2025 02:19:46 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:19:46 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Dec 2025 02:19:46 GMT
USER 1000
# Tue, 09 Dec 2025 02:19:46 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Dec 2025 02:19:46 GMT
LABEL org.label-schema.build-date=2025-11-25T19:42:51+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.2 org.opencontainers.image.created=2025-11-25T19:42:51+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 09 Dec 2025 02:19:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d038c8ab14401db1f160ef04265b33b9b5bad5d0d890ba47c745a41fae8df4`  
		Last Modified: Tue, 09 Dec 2025 02:20:41 GMT  
		Size: 5.2 MB (5153583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3823306f8e4dbcba6b1ecfe947480478016872220f8f3740112ebb74c6e2f81`  
		Last Modified: Tue, 09 Dec 2025 02:20:58 GMT  
		Size: 438.9 MB (438917313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d10ea37bff68864434c233b6ded40b79a1f312b562825929c1c0555c027e343`  
		Last Modified: Tue, 09 Dec 2025 02:20:40 GMT  
		Size: 1.9 MB (1926844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc84078c33ec53978864cd0eb0aa3b8e553aaaa6f654707b5c491f03c4bae9`  
		Last Modified: Tue, 09 Dec 2025 02:20:41 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd9a23ade26dd0769298b6fcc7c16411002adcef25d2f255317ac6f62964a26`  
		Last Modified: Tue, 09 Dec 2025 02:20:40 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5153040ecdebea80d9a9f4a0d9e54d3fa5dcad19e91e842602f2c3b4c9476a46`  
		Last Modified: Tue, 09 Dec 2025 02:20:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8ef9e404ddbad8ce8d16e18d1a7525ee42a36328d4f84f1996954c153d3b5f`  
		Last Modified: Tue, 09 Dec 2025 02:20:40 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.2` - unknown; unknown

```console
$ docker pull logstash@sha256:d2ebf32b215e13c32ee27fe504388ebd570ef3090593f8b2449044e17378036c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95f04afa3001173d5a1d282dcdbbf79ff42e17617d8538670557427a7f082bb`

```dockerfile
```

-	Layers:
	-	`sha256:3d01250a91651100bcff212118bf83a8089b84b56081a2339d4de51ba17dc9b3`  
		Last Modified: Tue, 09 Dec 2025 04:53:42 GMT  
		Size: 2.1 MB (2100951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a7f80c4667a24e451cf529c34d46d61188dbd642fe86e91117c6a1943d58dab`  
		Last Modified: Tue, 09 Dec 2025 04:53:43 GMT  
		Size: 29.7 KB (29719 bytes)  
		MIME: application/vnd.in-toto+json
