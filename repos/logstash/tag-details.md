<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.17.10`](#logstash81710)
-	[`logstash:8.18.7`](#logstash8187)
-	[`logstash:8.19.4`](#logstash8194)
-	[`logstash:9.0.7`](#logstash907)
-	[`logstash:9.1.4`](#logstash914)

## `logstash:8.17.10`

```console
$ docker pull logstash@sha256:3dba599dd38fb4f93da88695a0c511efd3d84eb413d5262f26575b899fe07788
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.10` - linux; amd64

```console
$ docker pull logstash@sha256:905a165f6c87ba168364f6aafbdafce3b510c4487539786a08a772b0f7b00257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.0 MB (523979498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925a9d44457f4d8788f77592a32c132e6c506792eac38affea6aa45e4dd3d35e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 08:18:47 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.10 org.opencontainers.image.version=8.17.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-06T09:36:38+00:00 org.opencontainers.image.created=2025-08-06T09:36:38+00:00
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579bcce4de643d530f781684978c4a68dac722b6a60828d036a4b9ce477857b8`  
		Last Modified: Mon, 15 Sep 2025 22:21:01 GMT  
		Size: 47.4 MB (47403277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba2c0a6caed177e2ec76fd814200dcecbc8a32574d1dbd848b5fd30d1c4f598`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8fd3abb625fa37009f7009ee6da7d321ec1c66368c4d16e205796f5f0ceaff`  
		Last Modified: Tue, 16 Sep 2025 02:29:27 GMT  
		Size: 440.7 MB (440696591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f415177e3d6977934337520b5f80338e5dc33fb448e32effba80538b714072`  
		Last Modified: Mon, 15 Sep 2025 22:20:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed5d7e5e76f837474ac746c18cb575c620394f7bac30f385e5ff5b6d41642d5`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ad7b31d7c9d3ee063a98308a85ca92747f513417d7fdf50894e19c105bc6e9`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cfcdc4c411a57cfb109aa039a7b22d2ae15c40aacffcfe6e6707c0000b9a8d`  
		Last Modified: Mon, 15 Sep 2025 22:20:56 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62d905567d916c8d1476c32c55261a638e8ed9e7f1e2fb36be8fae4865f4be7`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 4.1 MB (4056197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2860d77b3e4d5cf0142f2a6c713fb19bc5055d1e7943cf99b7c8cb14744ec086`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 2.1 MB (2094090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a25506f627bfd5936cc6e97e041245addf0ffaf72f8732170b173340f0f147`  
		Last Modified: Mon, 15 Sep 2025 22:20:57 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:41afefff9e23d763515f0f530e56492bf39f9999dd86ef565e591b9493f5defb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0412088455f3be53298b01ad6c8ebc91ac946f3044babd3b6efa754c0af81a42`

```dockerfile
```

-	Layers:
	-	`sha256:e67b9a77cf2b48528219c055e8e0b9e02690d06bbc819c41c46102f9e7acd88d`  
		Last Modified: Tue, 16 Sep 2025 00:53:22 GMT  
		Size: 3.7 MB (3657090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0524551cff5670fa7b45aa6b49bc94f32787f863e6314a2315fe5709f2751e50`  
		Last Modified: Tue, 16 Sep 2025 00:53:23 GMT  
		Size: 34.7 KB (34664 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:b717cf03cd9e7a24a25eaf174513ab06e9c301b25fe1b7422946cb037696b253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.8 MB (525841974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a109254473cc2a6b904ea9eaf268251b963e04f6498a9e45c55dc9cf132e925d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 08:18:47 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.10 org.opencontainers.image.version=8.17.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-08-06T09:36:38+00:00 org.opencontainers.image.created=2025-08-06T09:36:38+00:00
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519035ddd769536885fc1ae1b424af65c0dce05a437022e1cbb7f98c63b5c940`  
		Last Modified: Thu, 02 Oct 2025 01:26:36 GMT  
		Size: 52.0 MB (51975191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bba4d21da2c02031b0ff2e0de0d0d74c26ffaf92d6ac8c9c242a86c288bd2b`  
		Last Modified: Thu, 02 Oct 2025 01:26:21 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0256e894f923671fb7b28dc6fa4f22d6df262fd36b9c5c75a346159529b288c`  
		Last Modified: Thu, 02 Oct 2025 02:34:00 GMT  
		Size: 439.0 MB (438981495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2255b24182ddd929fcfea37d340175da55d2ed9f475c84142adfb49b53fdea13`  
		Last Modified: Thu, 02 Oct 2025 01:26:21 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3825e56196f0e9ea41907391761012d10e926184eee68691be221e52cae90abd`  
		Last Modified: Thu, 02 Oct 2025 01:26:21 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b15c34e599a476f2326315c81db466c2b1bff3645c65784d30209a89ea6ea4`  
		Last Modified: Thu, 02 Oct 2025 01:26:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b9d817db30a822086e0731fd4eaf3ebe41622e19b0311d978a25908cfc2b05`  
		Last Modified: Thu, 02 Oct 2025 01:26:21 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb31eb5b0efe4e7d0ca7e11d5cf588cd8e0bbd8b936f14519071aa59b0a0416`  
		Last Modified: Thu, 02 Oct 2025 01:26:22 GMT  
		Size: 4.1 MB (4056204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab5c59b42421776ad7ecd9de1f39647c22d9e4e5027a1cc2cb210f15553045`  
		Last Modified: Thu, 02 Oct 2025 01:26:21 GMT  
		Size: 2.0 MB (1961620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc4fa5f684d986124b11aa69a40fded97472867820b27fbe13dd08591ef4877`  
		Last Modified: Thu, 02 Oct 2025 01:26:20 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:d23fd79d08cc46e782c3b3cd44b8f04d08d39f63cf7978ac926516a92a852100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9251def4c13d9f048e97512aaa996d7afeeb9df48ca05f601654a14cc30e739`

```dockerfile
```

-	Layers:
	-	`sha256:1d0dadf2aa83c38e4981f80a5cfc06a5926deeed86e4b0c7fa8dd49532ea1022`  
		Last Modified: Thu, 02 Oct 2025 03:53:21 GMT  
		Size: 3.7 MB (3657515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da87df6e3df437a92d64f773128347901f90ab5cd6690917627b50a59576f44c`  
		Last Modified: Thu, 02 Oct 2025 03:53:22 GMT  
		Size: 34.8 KB (34807 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.18.7`

```console
$ docker pull logstash@sha256:ee67d6b9592157f96f490604b7d0d3e6953718e157bfae4b20bf5cdc91668519
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.7` - linux; amd64

```console
$ docker pull logstash@sha256:3dd480d92d8d45684bc18ab2f7925632b5b8da48fae230512ac8f77a4f47b200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524202572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d93301a9b1dfae633ad2e33a43872a8831b1568f991da67765ce1dde77608b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/logstash
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 16 Sep 2025 08:32:12 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.7 org.opencontainers.image.version=8.18.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-09T20:32:30+00:00 org.opencontainers.image.created=2025-09-09T20:32:30+00:00
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683daac8f55b8c39c6efac24271b3d9ad3e26f8572a533493441d51add3235e2`  
		Last Modified: Tue, 16 Sep 2025 18:02:43 GMT  
		Size: 47.4 MB (47410876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fa495453266cc5b135f688e8ce62639de93fccf6cc30e37903223a0a56a4a9`  
		Last Modified: Tue, 16 Sep 2025 18:02:35 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34b613f9b0ab7e553db9cdcf85fc1f22d3f2c0dd0dd50c3e4b02b13d7d660fc`  
		Last Modified: Tue, 16 Sep 2025 18:09:30 GMT  
		Size: 441.0 MB (440980153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e1f8411d0ac0e85b91edf10067200cc018f6579858009bdc1609dd7e1bc3f1`  
		Last Modified: Tue, 16 Sep 2025 18:02:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ebe138b4dac794e0d310062f9ce26338f42b0d7023320c313324921c4f6cf`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0df81189cd3cdf52297fdf08962ddba3300ef56a41d288362e143299388685`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7ca17a9f239146a1c1bb3ba02a7c9601bbd027f8b2a6a91fc08873437f942d`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a954c93c3b8dd327d2832bc9bb1a15e4f52bc0a81ee9f50cf2dde9ea9d5cc54c`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 4.0 MB (4004187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba3adbf5489c03b1bcacafc6d94205b6da7c5130c61fb23f427871699ec1e02`  
		Last Modified: Tue, 16 Sep 2025 18:02:37 GMT  
		Size: 2.1 MB (2078012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae963b11313e5f5f67219f6b57e5f45efe8aeb303e774e48483bdcb5b13f66`  
		Last Modified: Tue, 16 Sep 2025 18:02:36 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.7` - unknown; unknown

```console
$ docker pull logstash@sha256:f0d6adf780755aee565bf4d23d776d05755df3f377372904e1e096e08f4393f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0a46c6f2076521677680f87a169de4f3715c8445c985cdd579b6053aded75c`

```dockerfile
```

-	Layers:
	-	`sha256:5f95b14583b757118dede6b9768b899994f19d51b1f12ce11876a56522863420`  
		Last Modified: Tue, 16 Sep 2025 18:53:24 GMT  
		Size: 3.7 MB (3657649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c255529988e4546a307a3989ef079a4aafad76ee2f380916498d0b1753c44e`  
		Last Modified: Tue, 16 Sep 2025 18:53:25 GMT  
		Size: 34.7 KB (34652 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:8abe100f5ccd46f753c393c83896f39b55a91c83f0f876c7c37570e77d75012f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.0 MB (526020775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ed5777e00da0551744fac02c7b06a20a61d45272871b0a744b7c46f23acab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
ARG RELEASE
# Tue, 16 Sep 2025 08:32:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Sep 2025 08:32:12 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/logstash
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 16 Sep 2025 08:32:12 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.7 org.opencontainers.image.version=8.18.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-09T20:32:30+00:00 org.opencontainers.image.created=2025-09-09T20:32:30+00:00
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0327d7ad42ae52fde5e9c3fe862c700688c13478a72fd139517a394e8f5232`  
		Last Modified: Thu, 02 Oct 2025 01:26:23 GMT  
		Size: 52.0 MB (51975218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35bcc0e12fa975eb8fdc3ce494985926c79e7626c0679394c854b73dad0c155`  
		Last Modified: Thu, 02 Oct 2025 01:26:20 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c293bc73170323ae5fe01bb58f0a715933db0e5536e0979f6b0e66940ea4d6`  
		Last Modified: Thu, 02 Oct 2025 03:53:42 GMT  
		Size: 439.2 MB (439248336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3e321717e6030bc8115cbd555ac495c5b4e8d879c47fe7dbb7bad9d099bd8c`  
		Last Modified: Thu, 02 Oct 2025 01:26:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2430ec443a1248f0d09a487e0c2eb66e58021f141a805645d13906f94aff791f`  
		Last Modified: Thu, 02 Oct 2025 01:26:21 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a368ac7ea88d57d5615398c0cbee389cb97d5ab7481cba26246dd72bcfeaec45`  
		Last Modified: Thu, 02 Oct 2025 01:26:21 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e157461006233643c4d58eb0eeaa2c3c2e95e6d33f07dbf644d023267f8a5ae4`  
		Last Modified: Thu, 02 Oct 2025 01:26:20 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2429caaad8c55bc60cc77cfd207c289c9437e92d9bb9e35fb3fdd410feca62`  
		Last Modified: Thu, 02 Oct 2025 01:26:22 GMT  
		Size: 4.0 MB (4004188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3139e042c75772a82ca0bf159c3630762f01f9590170342a7677d2a61de0e08b`  
		Last Modified: Thu, 02 Oct 2025 01:26:32 GMT  
		Size: 1.9 MB (1925564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f32fdbc1ebec063a9b7ad78a004f65e439db205e36337522c5b7af072741c2`  
		Last Modified: Thu, 02 Oct 2025 01:26:21 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.7` - unknown; unknown

```console
$ docker pull logstash@sha256:01b0b1a65ced450be3c412a1d6eb276c5287844d0e5ed8b21deeda2d11c23aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb609cbbfb6bb523c5f357a1384fd4747be011b8f8f86897471a67f313cb254c`

```dockerfile
```

-	Layers:
	-	`sha256:cb00c0c0910e77671dba1247abf2cc40b1519701d9f07870652f1d31d4e59c0b`  
		Last Modified: Thu, 02 Oct 2025 03:53:27 GMT  
		Size: 3.7 MB (3658074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73082d87d970aac30f4d0e037250233626254bb2276384384f6562f8b31d343`  
		Last Modified: Thu, 02 Oct 2025 03:53:28 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.4`

```console
$ docker pull logstash@sha256:628017446dc749eac27dfaedc16fc14f514a52a791a377e589805bf07954c149
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.4` - linux; amd64

```console
$ docker pull logstash@sha256:758e9cb5457bc8a2d4a130112a4dda506192215f9c053042bf3224f500d8eaf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.3 MB (525261419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e8db18f84d40ba3df3318dcd6c46ebb4ae1981f38c6baafa4e652e0d1e11c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 18 Sep 2025 08:07:26 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.4 org.opencontainers.image.version=8.19.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-09T20:37:29+00:00 org.opencontainers.image.created=2025-09-09T20:37:29+00:00
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e8a09bcc55010a9f249521ddcaf490a2453ff601376b25589371e31078960f`  
		Last Modified: Thu, 18 Sep 2025 18:52:15 GMT  
		Size: 48.1 MB (48085685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83746b49af5bd8320110899d6c30b3884e966f6b9b40f68e97be0dd9d5470c4e`  
		Last Modified: Thu, 18 Sep 2025 18:52:09 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdd74ad860bd1f50c637bafcedb6f1f666cba9a2e8f939d61cc6ea02dce2e50`  
		Last Modified: Thu, 18 Sep 2025 21:54:08 GMT  
		Size: 441.4 MB (441364191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042fbd91a6301af2f4dfafc42533ae12f2589085e0fb4405552916835df38cde`  
		Last Modified: Thu, 18 Sep 2025 18:52:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2030f244d06962c6b1f3c9f724c6706fab10a0a552f91bb737d97252086c530`  
		Last Modified: Thu, 18 Sep 2025 18:52:09 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6570b0fc397b45fef4aac6f5fb34dd44559557e2bf8c249d5dcfdac43f2404b6`  
		Last Modified: Thu, 18 Sep 2025 18:52:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf86639004c7d50ce0a3e345b68464006c55a27aa1b62dabbf497f411fdbe61`  
		Last Modified: Thu, 18 Sep 2025 18:52:10 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd1f2ff29ca527a5bacab5041651be6c11c511c1be843308145eda4f013b07d`  
		Last Modified: Thu, 18 Sep 2025 18:52:11 GMT  
		Size: 4.0 MB (4004190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d1c7bcd066daac2e15caf683f410828fa405d4484deafe90184096ed793fb5`  
		Last Modified: Thu, 18 Sep 2025 18:52:10 GMT  
		Size: 2.1 MB (2078011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59130aaaf38d62800b4cbd923c6215523be6fd8885b28209075e23fd28de9d8b`  
		Last Modified: Thu, 18 Sep 2025 18:52:10 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.4` - unknown; unknown

```console
$ docker pull logstash@sha256:e1416e01637752f109ef469d2268af85895a0f92a9a1118352259977247f4753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb06035c0f5a68d767aab371fb964b6cdb87de2b5408ea9fd03ac66a1fec726`

```dockerfile
```

-	Layers:
	-	`sha256:e53af1484e7ae8f52bdbacec4eba1e9e952f0a2fc842768653e858711d5bf259`  
		Last Modified: Thu, 18 Sep 2025 21:53:18 GMT  
		Size: 3.7 MB (3653205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f300551e9002dbd7937d90a6465dbea9d4a69434113e32eecbbb2f311c7fe7b9`  
		Last Modified: Thu, 18 Sep 2025 21:53:19 GMT  
		Size: 34.7 KB (34656 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:11d6252b8e0a3733ad069921c2d2fb4ee4fe585170f4938acf662cb7c84e1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.4 MB (526400121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cdc7ae89f116d08450b4006b482ad2a370d35802dc3abf998bb83afd5db2b2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 18 Sep 2025 08:07:26 GMT
ARG RELEASE
# Thu, 18 Sep 2025 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Sep 2025 08:07:26 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 18 Sep 2025 08:07:26 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.4 org.opencontainers.image.version=8.19.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-09T20:37:29+00:00 org.opencontainers.image.created=2025-09-09T20:37:29+00:00
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf35a9cfb74267dc0fd77025d8d4a577383b773562c0b02e1f77a65db34cbb3`  
		Last Modified: Thu, 02 Oct 2025 04:16:15 GMT  
		Size: 52.0 MB (51975338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b45b18fe817bb1fdcf2aea64f74e6af8a18bc89873edbce75243b46498c08e0`  
		Last Modified: Thu, 02 Oct 2025 02:16:17 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4beb866dc1246b1ec7d480fe6e2e94ac6e4d8e51326b68246dd216ea245d4`  
		Last Modified: Thu, 02 Oct 2025 04:01:55 GMT  
		Size: 439.6 MB (439627565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd34a43e7d872000acb5d0b933f065d84d0d13b36131fae310df8df517b2f1b`  
		Last Modified: Thu, 02 Oct 2025 02:16:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bac12fe8c6881a650d461cad305a8b85c4d818f24ac979e9a3e246afd9cb21f`  
		Last Modified: Thu, 02 Oct 2025 02:16:15 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defc5fd815793ddab9a9bc37f5c25b5dcc87bc41889c620299ec0534cc228c8b`  
		Last Modified: Thu, 02 Oct 2025 02:16:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56da5e2ae6ea158b1d5693e19a5fcdf06e1bf3041baa643adf331f30aafabc9f`  
		Last Modified: Thu, 02 Oct 2025 02:16:15 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6bfe78eed52a7225d9f827f98e860b7de0590aa1ebd2bd1041bfcb3d47ac06`  
		Last Modified: Thu, 02 Oct 2025 02:16:16 GMT  
		Size: 4.0 MB (4004184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a25687ca900ed05d54e295b856756f17dcba4452766db7e332cb68c1f98fe7`  
		Last Modified: Thu, 02 Oct 2025 02:16:16 GMT  
		Size: 1.9 MB (1925565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a2013c1a05c70bc7b6c59928fb106f0f612132e01c919557b997e19ac05c40`  
		Last Modified: Thu, 02 Oct 2025 02:16:15 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.4` - unknown; unknown

```console
$ docker pull logstash@sha256:0060383c60bde383067c0c378a5bc13cf0cf36d31719ff643dcd87b0ac67fa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803321766289689b2a9de3ec18c1cd9b20ec169871d5fad65a6c61027d0425c9`

```dockerfile
```

-	Layers:
	-	`sha256:adf2c2e7a394e06d77e0b2928a87330a3a7a764c569cb06ae3c781d601ae6222`  
		Last Modified: Thu, 02 Oct 2025 03:53:33 GMT  
		Size: 3.7 MB (3653630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3776de0f510386604dd4b9fbcdb2384353308f67fec38a16e3c3db4eeefa72b4`  
		Last Modified: Thu, 02 Oct 2025 03:53:34 GMT  
		Size: 34.8 KB (34799 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.7`

```console
$ docker pull logstash@sha256:c77cf530b292c770c16b04841275dfa6ea76570d926c4109628ddff5f3abeba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.7` - linux; amd64

```console
$ docker pull logstash@sha256:494151fb3ea43b0a2d51e2815d3fff0409fc0d615d1068504e4dd37ff84de556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.0 MB (484966529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f52326d762ff945fb06ffbecde6386ad79aa9ceea5228ee0a909cf4b3fdc6d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/logstash
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-09T20:25:10+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-09T20:25:10+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e9424f752957cfe9c7841c2d792d51725b8d70c82572840dbdcf2cd2b5d472`  
		Last Modified: Tue, 30 Sep 2025 09:59:11 GMT  
		Size: 5.0 MB (5017244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa36917dc5a02617d364932ee73e542048817db28ff95a76bda57ad436a93f84`  
		Last Modified: Wed, 01 Oct 2025 13:45:25 GMT  
		Size: 438.2 MB (438219944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d372afdcd96813bcef1175b1048de0a2cab0b28bec8d88c8d7417a3f3db041b3`  
		Last Modified: Tue, 30 Sep 2025 09:59:11 GMT  
		Size: 2.1 MB (2078188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b60eb5bc9decc92e020bd382a5504fbd77c1f3d3af830e9054b70c58ebc90f`  
		Last Modified: Tue, 30 Sep 2025 09:59:10 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a27627fac9ecd294abe031aeed2ccc24c6a304baee99711127a71861b64a4`  
		Last Modified: Tue, 30 Sep 2025 09:59:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220c9f0b8a4fffeb41b0ebf8b1ad4ec328bd90323a5d84cb6aa4b3a67ad5f26`  
		Last Modified: Tue, 30 Sep 2025 09:59:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4151ecc2f10fd40152bdbf3cbe8d5793955297db6dc79150579ff32139c32b`  
		Last Modified: Tue, 30 Sep 2025 09:59:06 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.7` - unknown; unknown

```console
$ docker pull logstash@sha256:2a574a9dc63c837ef4d730e2aaee08a58171185506a040f3b679664fdd4d1b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a81025fc2b733bdf3104fe6c79908ae6ffe5347e1b068f584322ff972bd637`

```dockerfile
```

-	Layers:
	-	`sha256:12c262e528fe02b997b080bba4dddae89198080c0b70877af3c90fcdfd1cd6a7`  
		Last Modified: Wed, 01 Oct 2025 16:39:59 GMT  
		Size: 2.1 MB (2142418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838b80b5d7930a93798f60f3eb1925b79661dc8378558e30ca8a775473b0b08f`  
		Last Modified: Wed, 01 Oct 2025 16:39:57 GMT  
		Size: 29.5 KB (29535 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:320c5ac336acb3857b53ba0477a0ff3595410e1bc58bb4b7d60eb45ed1c52346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.3 MB (481335330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db4edad41628b3f4d94afde4789332db84313b3e945078bf8789595071b7bba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/logstash
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-09T20:25:10+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-09T20:25:10+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb40e285537da1f9c1c4abe864c5134527a4a5a9ed773fbaf662c1d74f95294`  
		Last Modified: Tue, 30 Sep 2025 03:21:16 GMT  
		Size: 5.0 MB (5022835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b939fe29be0059d26b18ea89702f8ce9e9222081642b7dd85e9adc906d646`  
		Last Modified: Wed, 01 Oct 2025 16:40:29 GMT  
		Size: 436.5 MB (436483024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0d4661ea9488547f709c6b8746bfa199d71e9a1fcb73ded6979bc3ba86b662`  
		Last Modified: Tue, 30 Sep 2025 03:21:16 GMT  
		Size: 1.9 MB (1926414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05284d4b1ab30260453de1ad56e775c0f5c53cb96b22eb2fd2cfb3e3859233db`  
		Last Modified: Tue, 30 Sep 2025 03:21:16 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc083e58d37b050afac74113e873e4ff9c185dded7460259facced7d14eea4e`  
		Last Modified: Tue, 30 Sep 2025 03:21:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92e38a3b2e6db20dc0514137f8d45621135c2e384126f912895ad67e0afd7aa`  
		Last Modified: Tue, 30 Sep 2025 03:21:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6049ac6df8bf49383b0fb9f820e4c5271c70cd5d3edaf68348f351d39401f7`  
		Last Modified: Tue, 30 Sep 2025 03:21:17 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.7` - unknown; unknown

```console
$ docker pull logstash@sha256:0912e6afcd7ab83cd05f5ae92e63e68433929204b1691525fd28dfcc177bcc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b836f7f85dfba1f7ede4626626dcef0ddcb6849d08f17fdf1bc2ff26e5991f`

```dockerfile
```

-	Layers:
	-	`sha256:40d76bd249206071cd0ac8c55a405c1d5a382c630c9991ad5e6a900522ed9868`  
		Last Modified: Wed, 01 Oct 2025 12:53:21 GMT  
		Size: 2.1 MB (2142990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d04e48040a9487c94fcd7884141c174b0e1b9521e66078003e8c35893f277b3a`  
		Last Modified: Wed, 01 Oct 2025 12:53:22 GMT  
		Size: 29.7 KB (29654 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.4`

```console
$ docker pull logstash@sha256:bdbb79fc2879158908e8867fd57642e4e537e8b956b7db7df5b609ebdc427ea1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.4` - linux; amd64

```console
$ docker pull logstash@sha256:e6b7eac2efe9fecae61f6eb730af57ba1ad0a95bed120ecbb909ecc372ace8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477029582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b02d4c94ad290b4cec78d5e38fe927a6cf702219b24a46173ac59689a3f993f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-09T20:25:53+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-09T20:25:53+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07ee381bc2f473dc2f985ecb1b38c4e28cda88177c5fadeba528443319d9b5b`  
		Last Modified: Tue, 30 Sep 2025 09:59:07 GMT  
		Size: 5.0 MB (5017240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5a62aa480a591aef3271defc217b4a10805875952d29481e26161cd6575dc0`  
		Last Modified: Wed, 01 Oct 2025 15:53:43 GMT  
		Size: 430.3 MB (430282999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96902051eab4e86d4164911806b8eb0bb427b45037ce5fd13dd405472c50268a`  
		Last Modified: Tue, 30 Sep 2025 09:59:06 GMT  
		Size: 2.1 MB (2078187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add3743a1cc5447d90cabe43729a44ce19a7df0e087df546b94f40f9428104c0`  
		Last Modified: Tue, 30 Sep 2025 09:59:05 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9984809312247256a09c91cc4da6c980cfcca10170d12fe0960ba30501c55c67`  
		Last Modified: Tue, 30 Sep 2025 09:59:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bac3f5fb872d72b1fc3c874abe25117f19b21d1063f30bbda526a5a1e4f4dd`  
		Last Modified: Tue, 30 Sep 2025 09:59:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb3ecca337148db4e63d648ba494a19fd9433e3d4381d95fd30f99c33c41bf`  
		Last Modified: Tue, 30 Sep 2025 09:59:05 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.4` - unknown; unknown

```console
$ docker pull logstash@sha256:77c80618245a05cead9bfbdec8479641f733ea4fe19daa0a104919c5d4fef00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d634e0c2fa88addc6de4e439975e0993b2fc0afa0a6332373e3eae71c41c6d`

```dockerfile
```

-	Layers:
	-	`sha256:406c1fa46ac75da57346dc7fcb99c0d985fb429f933faa14daba927a164b5257`  
		Last Modified: Wed, 01 Oct 2025 15:53:24 GMT  
		Size: 2.1 MB (2075941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd8ec0e3b118dc40411ed343133ddedd539408ffc5dc18ca748cd88970f6a3b`  
		Last Modified: Wed, 01 Oct 2025 15:53:24 GMT  
		Size: 29.5 KB (29537 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f6547629b791032bb9bb065027eea1ac4c8d931d6a515e512dc4973c738f183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.4 MB (473419281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b037364ff7d676bac741163317fd9e5e4b552be75da719698e87eb6ba492637`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-09T20:25:53+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-09T20:25:53+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58052bed18f60691b17dbd6e3079a0f04284f50ffe3b8ec5c55d1fd55642223`  
		Last Modified: Tue, 30 Sep 2025 03:21:24 GMT  
		Size: 5.0 MB (5022849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501077b5fdec09aa9f246575bde5b8ead7c88761fe285b22335fa957ae3060b9`  
		Last Modified: Wed, 01 Oct 2025 11:05:38 GMT  
		Size: 428.6 MB (428566961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0303f67507b6958c60319533c278b1435f23b37761165df1db94c649024acf`  
		Last Modified: Tue, 30 Sep 2025 03:21:24 GMT  
		Size: 1.9 MB (1926413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9272ce8dc814582afdcbd8ac99101dc4e91722bee67677e32791047819402b77`  
		Last Modified: Tue, 30 Sep 2025 03:21:24 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f134b58c56661864b04971781ab590ba3a993de51ca387e67afa42e15907a83`  
		Last Modified: Tue, 30 Sep 2025 03:21:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4096b17db6e9fd72232d0d1434f58ed3fb41b2be9703577e18a0141def27bd76`  
		Last Modified: Tue, 30 Sep 2025 03:21:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2a1d6aad483e8e80f91b0aa9c6308a9ce21002d1bb07b331ad968f32109a18`  
		Last Modified: Tue, 30 Sep 2025 03:21:24 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.4` - unknown; unknown

```console
$ docker pull logstash@sha256:bb6b3c9443e8b6ed01efe2746b42b60844a6a4661f5c75dce241d4cdf70b793b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2106167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec531b541ebb2cf8aa7b33b9d01952150ef0d25d3128d9479d1e5650de87750`

```dockerfile
```

-	Layers:
	-	`sha256:fd6436cc7321c1466f75084744bc2a2e5c4c34280497b32c119e6d37179912d7`  
		Last Modified: Wed, 01 Oct 2025 12:53:27 GMT  
		Size: 2.1 MB (2076513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f3e74460cecd6f8efadc3c592b97fac2ce6556af97d24370e7ebe5107acd9d`  
		Last Modified: Wed, 01 Oct 2025 12:53:28 GMT  
		Size: 29.7 KB (29654 bytes)  
		MIME: application/vnd.in-toto+json
