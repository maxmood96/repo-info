<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.17.10`](#logstash81710)
-	[`logstash:8.18.7`](#logstash8187)
-	[`logstash:8.19.4`](#logstash8194)
-	[`logstash:9.0.7`](#logstash907)
-	[`logstash:9.1.4`](#logstash914)

## `logstash:8.17.10`

```console
$ docker pull logstash@sha256:96ea673c2a1397074be4358f674f24b056c27404f472cc50191c129ff8df5ab3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.10` - linux; amd64

```console
$ docker pull logstash@sha256:c655500599f1b85c93257f143831936e370b7d629a03dc4c3706fb12d2e0aaba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.1 MB (527086232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e78ae51101e3c0f50c280ed72c34e12aa0927c5a994b9028ca1f54cb6a984d4`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9a4103026a87162feba73efe02d3fde2d74a02ed3c31f1a219b26cbeb7491d`  
		Last Modified: Thu, 02 Oct 2025 05:11:01 GMT  
		Size: 50.5 MB (50510956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308040c8fee0b3da7106642809f5a3972a3945e9fecc86d234863a831d2a9dad`  
		Last Modified: Thu, 02 Oct 2025 05:10:58 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94349e7c977b7abfd9db1448242b903c1266364848d85cbd773e78a5e65a6231`  
		Last Modified: Thu, 02 Oct 2025 06:54:54 GMT  
		Size: 440.7 MB (440696063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46ed7f5c64bb6c5e98fffdfc5d834ed4940f196034e9b6352a27403c586d0ee`  
		Last Modified: Thu, 02 Oct 2025 05:10:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718aedc7e6683f887f00ee6355fbaf08b2d093ecf61a11b4d339264d18b31e92`  
		Last Modified: Thu, 02 Oct 2025 05:10:58 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d639097ca9856aad1dbc0bf2d2f3c4e4ca51b1f16c896e02c150d63f77b33d4a`  
		Last Modified: Thu, 02 Oct 2025 05:10:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620af6e42ff59fe0502c20e18bcb7c877ef17f363a9c4432fb5b5c198f5834c1`  
		Last Modified: Thu, 02 Oct 2025 05:10:57 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973efed5515b5d41a45d15958777c51a66da5236b7be864394e56760635b77b6`  
		Last Modified: Thu, 02 Oct 2025 05:10:59 GMT  
		Size: 4.1 MB (4056206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848b64ddc8c7f126217d2da76cec1c68343a96bd27602ad36c1f5c191f783740`  
		Last Modified: Thu, 02 Oct 2025 05:10:57 GMT  
		Size: 2.1 MB (2094098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1339d2875da554c60fb81e86388f5c8f1f6003100fbb3d5d629a00d1029a75`  
		Last Modified: Thu, 02 Oct 2025 05:10:58 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:c3c2a84717e094a867629ebd0deb6ac62b33229bb6db63ad0929e6d7b771008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befca129625f2984e93f3d0d9378488df597af679064dee334fea1c9d90f8900`

```dockerfile
```

-	Layers:
	-	`sha256:3bb31ee6cb06cfb2355c1493809945b333602d95307cb7b4bd784207c7ff6f05`  
		Last Modified: Thu, 02 Oct 2025 06:53:19 GMT  
		Size: 3.7 MB (3657090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca7da4798c73113720f62f9434b2de27c43c6ae31d1a7bde81c25d94ee5f4d3`  
		Last Modified: Thu, 02 Oct 2025 06:53:20 GMT  
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
$ docker pull logstash@sha256:c7d90a77fddebe890f974718f678f3147176dd62d7cf5999d9d450de66e13243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.7` - linux; amd64

```console
$ docker pull logstash@sha256:85c086917d417e3153106fb91fe194e7fde45719da807b0a41d86800b6cddff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 MB (527301862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03a61bc9739d8f5a80809769f4e60573ccf81e63921396473cf8f88852f31a3`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360741364e3fa76b2926e18efe6b3b99edcee04f94bed81b900d51941af60eaf`  
		Last Modified: Thu, 02 Oct 2025 05:11:10 GMT  
		Size: 50.5 MB (50510911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5815b28e1fb665d4dc80bc3b784afe50c7ead734078cbf090a07fda0a4d2c445`  
		Last Modified: Thu, 02 Oct 2025 05:11:06 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe16120a383e86345be64df2c21eca881f728f39ea9150bd02a5940032bfe84`  
		Last Modified: Thu, 02 Oct 2025 06:23:03 GMT  
		Size: 441.0 MB (440979846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8d94e728776735570271acbaa71645ad2684a5a735fe772157b7e088d79af9`  
		Last Modified: Thu, 02 Oct 2025 05:11:06 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cc018187215231d8daff13b2ae6a205f29a6010076535007ff205b85954f68`  
		Last Modified: Thu, 02 Oct 2025 05:11:06 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5d0343642e7d2aba87b3c5acc00d6219e0da1f93135c0ee2c020037f08005d`  
		Last Modified: Thu, 02 Oct 2025 05:11:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2f50cb4d900d6df114634209aef8d986afac4b4dd3cd57330673589ca81804`  
		Last Modified: Thu, 02 Oct 2025 05:11:06 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68b45e7f4da964a77ff2fa0b831a005cc806b6b2948bfb4362224b07fc5653`  
		Last Modified: Thu, 02 Oct 2025 05:11:06 GMT  
		Size: 4.0 MB (4004182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0152f9738e77616628827d7d8f28d6979e1d9804d13cd999e15a7534c398ddaf`  
		Last Modified: Thu, 02 Oct 2025 05:11:06 GMT  
		Size: 2.1 MB (2078015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af58fe38f626aec73fc76f2c65f5ecc09ee359c6cd6139da2e6d2e32f65574`  
		Last Modified: Thu, 02 Oct 2025 05:11:07 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.7` - unknown; unknown

```console
$ docker pull logstash@sha256:73232e819d8b323057c7cafa2fd06438802824efa6be0d1cc3b04723573a5175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa671b60d826025f62524209b9cf9782024da0662fad01e8737537da28d296e0`

```dockerfile
```

-	Layers:
	-	`sha256:0644b056769fda5a1b136ab03ae84e8b05b00c8158017be7c26d1c4ba0282fec`  
		Last Modified: Thu, 02 Oct 2025 06:53:23 GMT  
		Size: 3.7 MB (3657649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b94cee935fb8f1a3f8f55a5305afbe6645d93f7aa1222f480a2418b855bd42b`  
		Last Modified: Thu, 02 Oct 2025 06:53:24 GMT  
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
$ docker pull logstash@sha256:29acf4b85e7f395dd76947458144beab2d10ddd97d57d17a9b55293394d8af20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.4` - linux; amd64

```console
$ docker pull logstash@sha256:652e7208cae3becb90e1518aea3149ccd7d125c94a67237ec3871e522246254e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.7 MB (527686392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff96c9ecb35871434f79de96003408b410a51ab3716c582696740cf3b64f1fd3`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9075365916f73088357bba31268a20ffa51487b49a57d738083c6fc7167a50e1`  
		Last Modified: Thu, 02 Oct 2025 05:11:28 GMT  
		Size: 50.5 MB (50511012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c7769a440fc7fa8c314299abdfae563d7bf9928be8cbeab9e03da3b2798d59`  
		Last Modified: Thu, 02 Oct 2025 05:11:25 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612bcb1bcd9628d2463ccfe149d789adfdcc585adff8e0f898c911b7b0fdd9e7`  
		Last Modified: Thu, 02 Oct 2025 08:07:20 GMT  
		Size: 441.4 MB (441364270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b5fcc0f89f7df990a92d78e3eb57531153260d6b252dc0d4f90127a9d8eea0`  
		Last Modified: Thu, 02 Oct 2025 05:11:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ff2f29dcdc1e33e51e4bef61600c30374c1a8ae8de21c095441f1ae4b13125`  
		Last Modified: Thu, 02 Oct 2025 05:11:25 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8360d23cd9f67274dff3fcfa22d386463e6783b0c73b64a7e23d53402a6180`  
		Last Modified: Thu, 02 Oct 2025 05:11:25 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc020af91e7141d47fb22dfb85827ac3d5f8ee3fd7239fbc26fdc952b737c94`  
		Last Modified: Thu, 02 Oct 2025 05:11:25 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc95f522d8a61dcead2206a77617350e3cf4ff3bdd4f44f6ac4e2b890d0e67`  
		Last Modified: Thu, 02 Oct 2025 05:11:26 GMT  
		Size: 4.0 MB (4004175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8a7ce3da528956f836a33099a18c4bba11ec3542958b894a7dd2c68b592d40`  
		Last Modified: Thu, 02 Oct 2025 05:11:25 GMT  
		Size: 2.1 MB (2078015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e74a6da5c4ea790413ab44744489a8784e7d06c2f14d02bf9b0663514b1bfb2`  
		Last Modified: Thu, 02 Oct 2025 05:11:26 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.4` - unknown; unknown

```console
$ docker pull logstash@sha256:f32280c86390806f3bff056bf015bd9c633ae9280fee83709613bc4d25266193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aacdb963d65a898e0e9b74faa2a8be010f97537bb10ea0cbc0fd024b15324b`

```dockerfile
```

-	Layers:
	-	`sha256:44d181420a2c767ae8e27c9416c4d811a40f5a406651ac6e7f102905f5b5c195`  
		Last Modified: Thu, 02 Oct 2025 06:53:33 GMT  
		Size: 3.7 MB (3653205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c01bac032a493ab2dd0f1e354b737d138d7b8ffc7df3bc5b691e200283e769a`  
		Last Modified: Thu, 02 Oct 2025 06:53:34 GMT  
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
