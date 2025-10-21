<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.17.10`](#logstash81710)
-	[`logstash:8.18.8`](#logstash8188)
-	[`logstash:8.19.5`](#logstash8195)
-	[`logstash:9.0.8`](#logstash908)
-	[`logstash:9.1.5`](#logstash915)

## `logstash:8.17.10`

```console
$ docker pull logstash@sha256:12f5777d928853b20d7dbf3afb490cf09fb807a7777017ed986ac5924fbeab6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.10` - linux; amd64

```console
$ docker pull logstash@sha256:10d297e083c7803b7fb87142916db34aeee73241e0b395e45629ec60800148cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.5 MB (525497533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307dd76ce6892956956a4a83deb2847ec42fdc0ac6c5400defd7f5a28142b4b6`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5558cf4c9185e80b2273524c4e4d3fb9cee6b4e6562f86cc1d976e3e7992316`  
		Last Modified: Thu, 09 Oct 2025 21:20:11 GMT  
		Size: 48.9 MB (48922263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581e50e61380a1d59565aaf90a0137abb4b31beda40b26ffb53580c4663c5442`  
		Last Modified: Thu, 09 Oct 2025 21:20:08 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6d9fd0dd258f34969b654f3c4275bb5fee5813e9fe3b57bbabaebfa846a6fc`  
		Last Modified: Fri, 10 Oct 2025 01:35:42 GMT  
		Size: 440.7 MB (440695933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c04e5cda56caaf573317453033914a873ecb1127e3046f71531f902b18fd8e1`  
		Last Modified: Thu, 09 Oct 2025 21:20:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d914efde7df7929e5abdfc2e71c7a58e2e63856fb396e31968036fa3b2ac366`  
		Last Modified: Thu, 09 Oct 2025 21:20:07 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65191aacc40c2e4a07b9bf960de733f859e5816f56d13e59797bcdc8aa8ca606`  
		Last Modified: Thu, 09 Oct 2025 21:20:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c364e6250f9c7973556d435a588c8e8a6ca336f7bc1be520980131d1e459ae74`  
		Last Modified: Thu, 09 Oct 2025 21:20:08 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c49fdf3126961b09e19ea7c9192057ebbd5acd5c4dc157e6804748ac16df71`  
		Last Modified: Thu, 09 Oct 2025 21:20:09 GMT  
		Size: 4.1 MB (4056206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1174ae1da57e0d3327ad447d9a1a0b15cf4a614fee592e98303d90e24c7d2258`  
		Last Modified: Thu, 09 Oct 2025 21:20:08 GMT  
		Size: 2.1 MB (2094094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f80d33247fe9c7d26bb469545e85138cec3ea2088e9f2cf6e51c207968ddb1`  
		Last Modified: Thu, 09 Oct 2025 21:20:08 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:cada07fa75d6d80f921d7ceb4982037c6e5d8588b7461c67078fb3c861455be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af404ca9ca277aad50b9ea3b32fbe0ec32b1267ab7f0a28821a0728fedc56fd7`

```dockerfile
```

-	Layers:
	-	`sha256:5376872a120509a32966bee34adc5c863e6164303de7db39f87ca2af5c14b2f7`  
		Last Modified: Fri, 10 Oct 2025 00:53:25 GMT  
		Size: 3.7 MB (3657090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f636312170a91bd9fe6f221557a74dc765b7f61c88c597d572ca21d75a2fa0`  
		Last Modified: Fri, 10 Oct 2025 00:53:26 GMT  
		Size: 34.7 KB (34663 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:2221a3589fd301776ca69d846399dd746f8dd41d10d73479383bfe8867c659c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.5 MB (524521450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c8e9fc34280e20413d98b785988e5271fabce77af558e7d8839133fdefb93e`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a374cf85bb728d14fe93d492198427de29ac07813af7aa3071d9d61f6787e1d2`  
		Last Modified: Thu, 09 Oct 2025 21:24:04 GMT  
		Size: 50.7 MB (50654361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1166b1b80c9266dedb1a98daa4b2049d87740005eb68091c13cad42a2e1d90ba`  
		Last Modified: Thu, 09 Oct 2025 21:24:00 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ebf11602c2c0d6f9ef324ba03337f0596b76510a499e1252b48c38caf7067`  
		Last Modified: Thu, 09 Oct 2025 22:21:57 GMT  
		Size: 439.0 MB (438981655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dfaf916264fe36fb0e6d0f80e44eeaef9879ef3d6d932d3d2be494bbea3e88`  
		Last Modified: Thu, 09 Oct 2025 21:23:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c1eddfdcbf63c18a979cc9c6aa54213fa441737f1f8d998f55892b2193a587`  
		Last Modified: Thu, 09 Oct 2025 21:24:00 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64f053ba906b895e657891e08255f024f0cf321661d17a3bbe3d3a3a60ba1c8`  
		Last Modified: Thu, 09 Oct 2025 21:24:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383a953a15d775c78584d35cfe9d4289154e6eed052d39f1cc70387352ad3d25`  
		Last Modified: Thu, 09 Oct 2025 21:24:00 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c761b1375b8deacc4c2daf39567f17566c35905afe37bca13843f44a2afcd0`  
		Last Modified: Thu, 09 Oct 2025 21:24:00 GMT  
		Size: 4.1 MB (4056203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3ef0c983ac9e0dee053c586876c70871856b764bdb542e3de1dbf5bab1f784`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 2.0 MB (1961625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0adba66544fd0d8dd1d36f4b22c5590cf668ad089935b27eb36f866f782c456`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.10` - unknown; unknown

```console
$ docker pull logstash@sha256:8943f80166080569020c507c7094aa057ab90e6304c8b89204919946f7d0a35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34936b5899c9f00bc0f7983e1536d9cf671ac7d55a25c97bfd501ae7e45233b0`

```dockerfile
```

-	Layers:
	-	`sha256:615b41223be12ace34d72cfa9bc06ca262fc47548e6a4bf8067f80c3d68def6b`  
		Last Modified: Fri, 10 Oct 2025 00:53:30 GMT  
		Size: 3.7 MB (3657515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3547dd933dc47bf66866083b238cb5e63654cb43da5dfb084a2950f33f6d8c`  
		Last Modified: Fri, 10 Oct 2025 00:53:32 GMT  
		Size: 34.8 KB (34807 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.18.8`

```console
$ docker pull logstash@sha256:8c006abe9b1f9926222c07939abfbefc662ab65883a701a005fa6460d622f518
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.8` - linux; amd64

```console
$ docker pull logstash@sha256:377ad55bb0da79203fbea548719adc2c6d742198f72497574dc01e06227fee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525714530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5310b6b4be40ed72194f4fee098b39b8ca2e5a6e251df1a0840a344b65ff7354`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 06 Oct 2025 13:08:19 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b4b7d12085fad81ad7ec3163a7f3cc70a710841621da192e7697622e982f20`  
		Last Modified: Thu, 09 Oct 2025 21:20:06 GMT  
		Size: 48.9 MB (48922387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2801e6c15ff330e70b9332ab88f6639c91b1f3f0eae7d774db8526f6cbdc57`  
		Last Modified: Thu, 09 Oct 2025 21:20:00 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eba5ed7d944a1d29952ccfb3db307a04dbe527c911a0069691750bc5378d9f9`  
		Last Modified: Fri, 10 Oct 2025 01:34:38 GMT  
		Size: 441.0 MB (440980907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccae48fa8c35954d5933778e67a9082bbd63bc132b9b4374af7c1dd83453292a`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9340b991c583eee28ac3879ca3a55d7b265f81a2d422cfca371d0c4ba8b111`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f59104d8d1a6bf1554e5b7ceeb60f805fd0a2e1659bbd39d31cc70ea55046`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcea15f1ee09cf40b3da8cdda73c50ef50ca8cdaceba61b617f50aefaa8aa21`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53273aeb4bda01e98919eafef40fc74066aca799903202fc52667944989302cc`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 4.0 MB (4004183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7a8b0478e4a9ad3b607352cbde90f0dceb22b6ebc5f1257d64e99f02fa714`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 2.1 MB (2078019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60ff261aecaf304811f084aa2a492c33f6b25c45976cc547c4038f2ee2407c8`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:9f01ed0470443a0ec61e774d8bf316f80226724eb5a5e891cfdecfa816420f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148f4554e42b2812e060d34ce6c1ddac579773711bb79afe57c09c6001d172b6`

```dockerfile
```

-	Layers:
	-	`sha256:0980399329770b29b190e202748ee01270e1b804252036a729a74f02229bf16b`  
		Last Modified: Fri, 10 Oct 2025 00:53:35 GMT  
		Size: 3.7 MB (3657663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b5ea34633a16735d6cc449ed464af2cb65d494547aa648d87feeb90ef2f83b`  
		Last Modified: Fri, 10 Oct 2025 00:53:36 GMT  
		Size: 34.7 KB (34652 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:d8126443d2fe9e8ef2a9dee7e7df25eeb721af2b36042877103410fc01fded1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.7 MB (524700374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4b09f60acb633b24f28272df1f67d82e349cf75b1fc594ebf6e3adc955c7f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 06 Oct 2025 13:08:19 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63573c99495ce0d7e4663866b70688062419d2c6fab14fc48ee89d545d9e4fd`  
		Last Modified: Thu, 09 Oct 2025 21:22:08 GMT  
		Size: 50.7 MB (50654390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16040666ad5849dfac44240f0b9638ed221add0c480c1266be6793f01e14b7fb`  
		Last Modified: Thu, 09 Oct 2025 21:22:03 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de3f9d837667a5455efacb31c2f5634003662a7d2f84d9a81064331fa8d60a1`  
		Last Modified: Fri, 10 Oct 2025 01:34:48 GMT  
		Size: 439.2 MB (439248611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fe1f3fde0a2edceaa89fe2dfd6d28f1fb00ca1e732d34a62005008bc88a735`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb87b742c5b03aa23edbe6e2c3cc2575ae3fc29126340a98b6cf8705be3b94`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860e50aeb11965eeee28d3ca308606108364c779a810047fdefbbebb8bf155af`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001e27e71c69416570e63c689913439b42ff5eda7eb344d8eba8d65980150f20`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66151e42d94dbf9b0e521d122eecc712cf59d6a59c4ceee8ce998c2e17bb4123`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 4.0 MB (4004183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639900a06964fadf7c7124ecbdbd057d5da77f7e3f8a1874cbfbbecace1c39c`  
		Last Modified: Thu, 09 Oct 2025 21:22:02 GMT  
		Size: 1.9 MB (1925572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5204c3975e93e59a2c18c1131dbd313c2d7d01cb8e996200453ce5f83585ec0`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:4b4a6c8d728e02817972442e7fbca761ca3f8343336bc511513166d46512398d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d499c7043e4183b4e4751ca3d009bc8c81c9eaa7a3ca2a78eb55bba399e206`

```dockerfile
```

-	Layers:
	-	`sha256:e73f29e0d0122230125d66c8977c3dc9091f4c3ccd9b41ab865d5cacfdad59a0`  
		Last Modified: Fri, 10 Oct 2025 00:53:41 GMT  
		Size: 3.7 MB (3658088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84da2a7c3d55eb7a5470d8325d5e68d517d3755a71f99f1aacdf4199f2057e76`  
		Last Modified: Fri, 10 Oct 2025 00:53:42 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.5`

```console
$ docker pull logstash@sha256:8c166beb62cb6fce51cb5fcc861e6adf6525f1b00d57abc2c2771a184d007927
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.5` - linux; amd64

```console
$ docker pull logstash@sha256:a2becb5b5bcaf2ff8f8069f3d6844e4bd454add5f3b59e07985643e30ad6e351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.1 MB (526097790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6196d4198bbd42f5316fd60f44e6747c172d30beac2e37d7ea6638136e2639`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 06 Oct 2025 13:08:09 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.5 org.opencontainers.image.version=8.19.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T20:53:24+00:00 org.opencontainers.image.created=2025-09-30T20:53:24+00:00
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd57e981ef0ff263f80d2f38a94e6e36ce57178e4520dac91a272cb82f9409fb`  
		Last Modified: Thu, 09 Oct 2025 21:20:40 GMT  
		Size: 48.9 MB (48922180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daa452c22e82d4e4be81682445e3ba869adc4c458431673c705b309c5bb2277`  
		Last Modified: Thu, 09 Oct 2025 21:20:33 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71eadb20d9f3432323a1cab284caffa2a15eed907dbcab4c01323b6b6b38ddef`  
		Last Modified: Thu, 09 Oct 2025 22:21:50 GMT  
		Size: 441.4 MB (441364367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579135a01d64cfa2b1f0cf1710aeaea950c47aafa2e93d6fe1339892565ac4f2`  
		Last Modified: Thu, 09 Oct 2025 21:20:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4ea0806a7e1a9576044c86c345d6e572cc09e754e88cbc3bb793075d7c3561`  
		Last Modified: Thu, 09 Oct 2025 21:20:33 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d984af0b7346fc50e12c08d931c52994d4ea34fae2af7fc690b094b5c6c853a2`  
		Last Modified: Thu, 09 Oct 2025 21:20:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd252c6742f87184699c89ec3297ae186bfe93a8f24e0f7212bb32a0db586a5`  
		Last Modified: Thu, 09 Oct 2025 21:20:33 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1016968294e54bbbc461604464f9b8fd3c63d92ec7632f61c30db0097aa80b1`  
		Last Modified: Thu, 09 Oct 2025 21:20:34 GMT  
		Size: 4.0 MB (4004197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0685c4910ea5e5f49f63e4370b7b6ce7f67d06239a59076e3d25f4c0d0af8b73`  
		Last Modified: Thu, 09 Oct 2025 21:20:33 GMT  
		Size: 2.1 MB (2078017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b127874f016805d0d333075d295d0815bcc0b4d5a08fb1ec4975a6e01405cb`  
		Last Modified: Thu, 09 Oct 2025 21:20:33 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.5` - unknown; unknown

```console
$ docker pull logstash@sha256:87f802b471940f6ea9b9d353e954b2dd2ea916b9570d8443730267a7614a0453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbca59bc162c656240198324d88e5c7b3d86ddae5d77edfc1f6f15cb09df59d`

```dockerfile
```

-	Layers:
	-	`sha256:1889a6ced4a32d0f2327a1dd03c5cb77d6cc9a97ed494016c8363af08bcea4fa`  
		Last Modified: Fri, 10 Oct 2025 00:53:44 GMT  
		Size: 3.7 MB (3653219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1784c7fc86a13bd8a286894c190ac7b9e7031334a5b17e4744f94efead2022d9`  
		Last Modified: Fri, 10 Oct 2025 00:53:45 GMT  
		Size: 34.7 KB (34655 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:03689c8aa78f2133ad99e3dc055b08d7bacd15cb21dad02ab453df13d438ebc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.1 MB (525080789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4744d65ca6cfe63c7790578349fde754b7a6031cef1a96ca37e0abffff67cea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 06 Oct 2025 13:08:09 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.5 org.opencontainers.image.version=8.19.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T20:53:24+00:00 org.opencontainers.image.created=2025-09-30T20:53:24+00:00
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92642c1dcfa2a8cea579ea5bd54509a2a0bc5bfc5c2247b46a48f05bdca23fc4`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 50.7 MB (50654437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5b5fdc2091d6bd23264b7bd2ae5d423d5bf04d4a141f643bbac15af76a2788`  
		Last Modified: Thu, 09 Oct 2025 21:22:02 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05f054f3b7e5b9486206bc96836c329101b7c3cb1930505d12a2b279f41f709`  
		Last Modified: Fri, 10 Oct 2025 01:35:28 GMT  
		Size: 439.6 MB (439628990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e865b047b4eac9e54fb2e1529c3bd30268d9ce481b36141ef819a6144be8a55`  
		Last Modified: Thu, 09 Oct 2025 21:22:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec65d18ca0c455c124287598c8a743f6703319d6d6f884d9d62cdc950d080fd`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae6875cf929aac102c33169a036decd656b7dc65c87619301d2f792c2c08561`  
		Last Modified: Thu, 09 Oct 2025 21:22:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e44ce01e6599b6aff6665445441461e2c7b2b99bab58a8f278d785f107fe87b`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461fbbd13435d18066b27d54cfc12a63127c82c333d8dbd3bdef19ff10210872`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 4.0 MB (4004183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3a67245a0f87e7447ee3eac60f844071a37b3c760ed648e14ebe25c58b881b`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 1.9 MB (1925569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5204c3975e93e59a2c18c1131dbd313c2d7d01cb8e996200453ce5f83585ec0`  
		Last Modified: Thu, 09 Oct 2025 21:22:01 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.5` - unknown; unknown

```console
$ docker pull logstash@sha256:4d7a04ce5bc2947cd50ac1c6ff48926d3786712a7dfdc68694088356d5e1c10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e04be8f31ea3a1bbdaa4630275d11679e13a824f8da0fbdaa4c4f43413b604`

```dockerfile
```

-	Layers:
	-	`sha256:125aa3c60784bd458b3f2c061597b577957eb3e67932f41a11e15c1f5aff3500`  
		Last Modified: Fri, 10 Oct 2025 00:53:50 GMT  
		Size: 3.7 MB (3653644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a84fb3d0d6e244ed600000276844afbbdccf92be49511b9243d223f5e6453c`  
		Last Modified: Fri, 10 Oct 2025 00:53:52 GMT  
		Size: 34.8 KB (34799 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.0.8`

```console
$ docker pull logstash@sha256:11bf4ad146a50f57a35e881ca0e6bec9f98211cef76edf24a66086f552091b54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.0.8` - linux; amd64

```console
$ docker pull logstash@sha256:f64dc59e27890c2e149620e44dcc965282692aa18a6fedfa7f555e16759dc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.0 MB (484972700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d26b9ecb8fbc447007fa7772292a21f93821f35123c2109ceafd7ad2a7692e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:09:04 GMT
ENV container oci
# Mon, 06 Oct 2025 11:09:04 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-09-30T18:53:08+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-09-30T18:53:08+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586876347c1d4d154c89e942e806d42ad1e418468357f5c1e63e685765d20003`  
		Last Modified: Tue, 21 Oct 2025 11:20:15 GMT  
		Size: 5.0 MB (5017068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed25e6047918287ca7a6582fb33f44eee8131bddfc3a9f981aeb685206d1ce3`  
		Last Modified: Tue, 21 Oct 2025 11:20:01 GMT  
		Size: 438.2 MB (438220353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9c3d6b236be526ddfc5c0d0985b3110081c34d0d9cb6d7ec4860625ee975e3`  
		Last Modified: Tue, 21 Oct 2025 11:20:15 GMT  
		Size: 2.1 MB (2078855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb70d12d92c1329df1668b9c9e0ab1101c0dbb0c62d71ab9b625413054c42f8e`  
		Last Modified: Tue, 21 Oct 2025 11:20:15 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28715155d731bc4ee50cb1ec2384256f0c5509a4d5de1415c8acf9b3e872d47e`  
		Last Modified: Tue, 21 Oct 2025 11:20:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14626dbbd0752cae09761a34c950f3f618741a0f1a1c5fe595fc55fa1c3720d`  
		Last Modified: Tue, 21 Oct 2025 11:20:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951e3a0d31987335b1daaab9d368c00685261e395b1bbef4c351a9d5cf2acda4`  
		Last Modified: Tue, 21 Oct 2025 11:20:15 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.8` - unknown; unknown

```console
$ docker pull logstash@sha256:0b8d328eb8abcb8c91916c7765b774a6093262c22eb9074b8db7f9ab19cb798e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981a55315b6528aad6698a8766083b122f802dcd898b8f42e3f49a01805f8c0d`

```dockerfile
```

-	Layers:
	-	`sha256:c5b2904bc6bb9eb55d6571a6809d255567d05b87dd22327078757f9a9bee7706`  
		Last Modified: Tue, 21 Oct 2025 12:53:20 GMT  
		Size: 2.1 MB (2142432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb3f00479e48dbd7b9f6fdf2122f77e719718dd157aa9af49dbc176d3ebd41b`  
		Last Modified: Tue, 21 Oct 2025 12:53:21 GMT  
		Size: 29.6 KB (29597 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.0.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:5f1dc7b2e3492df0da2f90356797b5cf5037051014f72647cb2d82675f632f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.3 MB (481331544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed81e047ec7f91a87da7ab973b5596226030ec37217a4e4236437e3ba2de9384`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:09:04 GMT
ENV container oci
# Mon, 06 Oct 2025 11:09:04 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.0.8-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.0.8 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-09-30T18:53:08+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-09-30T18:53:08+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d621cbd388bb359b48e466d77291b2601eb3994c7268618dcc033804ad97e0ea`  
		Last Modified: Tue, 21 Oct 2025 04:21:45 GMT  
		Size: 5.0 MB (5022813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f5fa206171dc2bf9cd3f0ca8a2b0df6f303704ec98f04fdced0e85f8ee8d56`  
		Last Modified: Tue, 21 Oct 2025 04:21:40 GMT  
		Size: 436.5 MB (436482655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29f13442bca65b673cdb4f4aee5831cb97b53a2a73a51d580c6b65174336498`  
		Last Modified: Tue, 21 Oct 2025 04:21:44 GMT  
		Size: 1.9 MB (1926887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5899f898ea0268228809472c4b0acf879b214eb6d2f980a378e18e0dc2de9059`  
		Last Modified: Tue, 21 Oct 2025 04:21:44 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1ca72f9c5d2e86509c605bf6772e58bdd2e14423c0e6ca96c9ce12b2be997`  
		Last Modified: Tue, 21 Oct 2025 04:21:44 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b623c2e3cb737ecb4cf54f6eac9339583febbd521e62b74eca0669c7bca06f9`  
		Last Modified: Tue, 21 Oct 2025 04:21:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f33f2a34d5414fb301da8c058c2945ce50166c8bda2b7c126d74994f40392b`  
		Last Modified: Tue, 21 Oct 2025 04:21:44 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.0.8` - unknown; unknown

```console
$ docker pull logstash@sha256:bc7efcd266f51b5e876c9de5bc3f1f885238b1be28d5861c81942129f2c9b6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a09b3c16b88bcea2fdd81d2ed97db69c2d493e29289dff2991ed6f3a280052c`

```dockerfile
```

-	Layers:
	-	`sha256:29b6e907940d7bcbea54dbbd7de40f47f7032573d5b0218255d471ac15031007`  
		Last Modified: Tue, 21 Oct 2025 09:53:22 GMT  
		Size: 2.1 MB (2143004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b59fdbe94bfc728cfdd0f1a1970a8594cd497058eba753a920d961e263193e`  
		Last Modified: Tue, 21 Oct 2025 09:53:22 GMT  
		Size: 29.7 KB (29714 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.5`

```console
$ docker pull logstash@sha256:9765ebfe6898ca2e7f6cdb65685a16f8a83cec8eb47bdaea14aee7b51da8b9eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.5` - linux; amd64

```console
$ docker pull logstash@sha256:8243d115f85b6310b6ac2ecf1b41f1a6f80852312667104bfc09ad749d6c3b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (477036983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f342426897b7bac0a97f6ce2cf4f77c1e859026a4a54dda564b7c7fbfe996b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:10:10 GMT
ENV container oci
# Mon, 06 Oct 2025 11:10:10 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-09-30T18:55:09+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-09-30T18:55:09+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0ecb3c9505977a7eb756770950212718573cd75c99feb62a27ed19f3f7fcd0`  
		Last Modified: Tue, 21 Oct 2025 11:21:15 GMT  
		Size: 5.0 MB (5017319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae52b716c685bcf288339b4fd877b74f80585a779076ac66bebcd85df57be5b0`  
		Last Modified: Tue, 21 Oct 2025 12:57:00 GMT  
		Size: 430.3 MB (430284382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52cba0e0f4ccc21a7c7c1d54ded46f090d6a0a4a3b0e5604f4646f0db88ad5d`  
		Last Modified: Tue, 21 Oct 2025 11:21:14 GMT  
		Size: 2.1 MB (2078855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2e39c44bd07cab13202fe7b0fd56e4a042c7e51779f412fbd286c8f44fbe72`  
		Last Modified: Tue, 21 Oct 2025 11:21:14 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c895b341d5f70792931f95b3f7a51589b3ca74191257a65c00f7a3e612e59a`  
		Last Modified: Tue, 21 Oct 2025 11:21:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617efe899ac8bb88c3979c24b127691e9edea09682e082c88c71d18ffcf61d39`  
		Last Modified: Tue, 21 Oct 2025 11:21:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ee2b8a07d0a66bf578f9921357f765d5ca95707905d73d886c5db74e3be52d`  
		Last Modified: Tue, 21 Oct 2025 11:21:14 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.5` - unknown; unknown

```console
$ docker pull logstash@sha256:d85896103ab7b9fe4eea9c4ae6564ad0332d0c20f3708c31e9c646b3f5ef0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff45ff33282cf1a25db547e4572c4173324c7adedce4d245d20353b0954f8ee7`

```dockerfile
```

-	Layers:
	-	`sha256:48060aaf932bf0fe66ce28f4a1555e87cf21befd78251bda878de0653392159e`  
		Last Modified: Tue, 21 Oct 2025 12:53:26 GMT  
		Size: 2.1 MB (2075955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae09f67bb3ec139d758482bcff27a4020cc3ff37f652fee310ada1fcdf63914`  
		Last Modified: Tue, 21 Oct 2025 12:53:27 GMT  
		Size: 29.6 KB (29597 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:bcb9de6a6e7c02698fc99517b692ebef4bfcd588e053cd8a305609a4ab055ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.4 MB (473415068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5805e09e884a40e8fb4b4820922a7d2372754cc46130a36bc1a6066c700ffe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:10:10 GMT
ENV container oci
# Mon, 06 Oct 2025 11:10:10 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/logstash
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-09-30T18:55:09+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-09-30T18:55:09+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2590392e31fa605e93e7d14f3078d3ef6043cd324510bb234b552b28eae8500e`  
		Last Modified: Tue, 21 Oct 2025 04:22:15 GMT  
		Size: 5.0 MB (5022775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7372e2e1e87e90a6ff39c9258b81173021cc19b3c468f2a08bf697ed1c4d68eb`  
		Last Modified: Tue, 21 Oct 2025 13:39:14 GMT  
		Size: 428.6 MB (428566240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5990bcf40991b783c7ca844c10c691915fb49cada798ecfb20883ba3f0fc28`  
		Last Modified: Tue, 21 Oct 2025 04:22:15 GMT  
		Size: 1.9 MB (1926878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af5f479ba9308dd85cffb19532966512c595662aa5a8803d5943dd9c939b1e3`  
		Last Modified: Tue, 21 Oct 2025 04:22:15 GMT  
		Size: 1.6 KB (1572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cf276442dcb1bc6cdfdc53c7f00ebfbbf7b03d081104243b189885bee1152b`  
		Last Modified: Tue, 21 Oct 2025 04:22:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6824fc95e8596d4a056736289fb7ef0af74e7c9afb3d6ed1f0ee551fdc53b7cd`  
		Last Modified: Tue, 21 Oct 2025 04:22:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d7401046621f3590eeed70934fbf4dfb82243a6b1215a32ed42afb5e4666e9`  
		Last Modified: Tue, 21 Oct 2025 04:22:15 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.5` - unknown; unknown

```console
$ docker pull logstash@sha256:6231ad976318791cb156c86e9da8e39a0b552de5de8bf7eed039163784fbd2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2106241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9c7c7fb5c90666652492d95f9d809ae39375dd77dd218827653503d07459e7`

```dockerfile
```

-	Layers:
	-	`sha256:fa1b529b779236d2a761e27e4b1c72744c91b3271aa5eac70cf8afc1c09b4f9d`  
		Last Modified: Tue, 21 Oct 2025 09:53:29 GMT  
		Size: 2.1 MB (2076527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab28aac897a3eade469dddc03847ac8db1a1f6e1b111ee773858826ed74aaa1`  
		Last Modified: Tue, 21 Oct 2025 09:53:30 GMT  
		Size: 29.7 KB (29714 bytes)  
		MIME: application/vnd.in-toto+json
