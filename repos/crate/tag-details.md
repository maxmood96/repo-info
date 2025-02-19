<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.1`](#crate5101)
-	[`crate:5.7`](#crate57)
-	[`crate:5.7.6`](#crate576)
-	[`crate:5.8`](#crate58)
-	[`crate:5.8.6`](#crate586)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.10`](#crate5910)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:58eb8c71600008609bca10e9c7e1a3784d505d9f04991fa331423807c91d12bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:666bb236ef15bc4c081fb0d6420b0df94074bac139bd58b6624d77aae2c1ea55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aba0995eb00b98f9b0ffefc9d2ad7a2849aa1ffc3b091d68bd737520f2814d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 11:37:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.1.tar.gz.asc crate-5.10.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.1.tar.gz.asc     && tar -xf crate-5.10.1.tar.gz -C /crate --strip-components=1     && rm crate-5.10.1.tar.gz # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 11:37:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 11:37:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 11:37:21 GMT
WORKDIR /data
# Thu, 13 Feb 2025 11:37:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T11:37:21.577398 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.1
# Thu, 13 Feb 2025 11:37:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 11:37:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Wed, 05 Feb 2025 05:27:15 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e08da2fbb8511dde834ed4e9a1aceb1ff391def8f04a3f2066dced44ba18bc6`  
		Last Modified: Tue, 18 Feb 2025 21:29:40 GMT  
		Size: 15.4 MB (15360839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7a32e8ee0628c751dae3e049df63437944254b491f7ed187909bfea65914b8`  
		Last Modified: Wed, 19 Feb 2025 00:38:55 GMT  
		Size: 149.7 MB (149653771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cca6596b145b8e103ac3bc556c1b267b0dffc61e9400f7ea396730a7accf10e`  
		Last Modified: Tue, 18 Feb 2025 21:29:39 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0e1e357b5b9915c81d64de46ad296e5bac5d341fb14413f2f71ca0e34cf0dd`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197b5ca764ff548fa55d6b275d5de6da88c29077660995af974871b1860707f`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7ba24f601573bce233292a6d0890ee10011ebbc412ca53ad4529778942494`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7156998a59bacc352db9450332e37ced91d37d5a818d4264c05ab22fb652a4be`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:bdf022e20bb34837bec75993654d840c4c72afc95c3b7600686b76874a575945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2340878f15cbc13a3d8c8494a7002f30d81d459a11c7b1554de23854c628d2`

```dockerfile
```

-	Layers:
	-	`sha256:e562fd8c51030a6728344bff6c7c82c0a53271cfe98276502fc0ef91a411adf2`  
		Last Modified: Wed, 19 Feb 2025 00:38:32 GMT  
		Size: 5.2 MB (5155069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725a014961de078af9a35614cfb486e17488ae54f01708de09b6b807ff3a7239`  
		Last Modified: Wed, 19 Feb 2025 00:38:33 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:057210175979c2c3e1923a4946e68e2aaa05258fe95f401471d3ac69a03b5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232343259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cf2307d56235cc186d15d56a3386b42043766582dc76001bf0ab9f5a9232b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 11:37:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.1.tar.gz.asc crate-5.10.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.1.tar.gz.asc     && tar -xf crate-5.10.1.tar.gz -C /crate --strip-components=1     && rm crate-5.10.1.tar.gz # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 11:37:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 11:37:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 11:37:21 GMT
WORKDIR /data
# Thu, 13 Feb 2025 11:37:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T11:37:21.577398 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.1
# Thu, 13 Feb 2025 11:37:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 11:37:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 08:45:30 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b02f2e8a13da0eae97095160d13c034035c694f70538f09411a09ba10308a`  
		Last Modified: Tue, 18 Feb 2025 21:30:00 GMT  
		Size: 15.4 MB (15421456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3069e8e758098e1903794ec516aa5b4c444b1a5b755d43340372d56e9b80109f`  
		Last Modified: Wed, 19 Feb 2025 02:53:51 GMT  
		Size: 150.3 MB (150333456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7534623abb40b966db4acd7a2e20a9cbb47c8775dc18286b26de01cca3490`  
		Last Modified: Tue, 18 Feb 2025 21:29:55 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b71f8980ca69b56f2de0a7d7b0fba11300f0f9b57160065e701269709e1382`  
		Last Modified: Tue, 18 Feb 2025 21:29:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108c22a110542fb61fd00a843073b9e449a6c7dd77a32d17989e98e0a01d2ff4`  
		Last Modified: Tue, 18 Feb 2025 21:29:48 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ca601928ed7ec5f3dcb60e7f7105b09b762b1adee6c0feab468e40ab06487`  
		Last Modified: Tue, 18 Feb 2025 21:29:48 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168c3513c13ca5e035cff09d1f976fb9a4d00e62f894ed7c5f1854396b338a29`  
		Last Modified: Tue, 18 Feb 2025 21:29:48 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:2dfa98c6486ef7c77674ff767b410a55e17feb66716f8e57fda8e9b0c20ecd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef027cdd0752da3744ea160ca2e1395a8530cd903175c59bff27a8c68e34c85`

```dockerfile
```

-	Layers:
	-	`sha256:ef8d446aa50b963074c82c9c2b7188a0dd89bd831400ede6ccfed25c03eb548a`  
		Last Modified: Wed, 19 Feb 2025 00:38:35 GMT  
		Size: 5.2 MB (5152377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5070853231affa7e164b1061d71c6d895c7a512628e8eb78e63b162e2c7cb06f`  
		Last Modified: Wed, 19 Feb 2025 00:38:35 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.1`

```console
$ docker pull crate@sha256:58eb8c71600008609bca10e9c7e1a3784d505d9f04991fa331423807c91d12bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.1` - linux; amd64

```console
$ docker pull crate@sha256:666bb236ef15bc4c081fb0d6420b0df94074bac139bd58b6624d77aae2c1ea55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aba0995eb00b98f9b0ffefc9d2ad7a2849aa1ffc3b091d68bd737520f2814d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 11:37:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.1.tar.gz.asc crate-5.10.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.1.tar.gz.asc     && tar -xf crate-5.10.1.tar.gz -C /crate --strip-components=1     && rm crate-5.10.1.tar.gz # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 11:37:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 11:37:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 11:37:21 GMT
WORKDIR /data
# Thu, 13 Feb 2025 11:37:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T11:37:21.577398 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.1
# Thu, 13 Feb 2025 11:37:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 11:37:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Wed, 05 Feb 2025 05:27:15 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e08da2fbb8511dde834ed4e9a1aceb1ff391def8f04a3f2066dced44ba18bc6`  
		Last Modified: Tue, 18 Feb 2025 21:29:40 GMT  
		Size: 15.4 MB (15360839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7a32e8ee0628c751dae3e049df63437944254b491f7ed187909bfea65914b8`  
		Last Modified: Wed, 19 Feb 2025 00:38:55 GMT  
		Size: 149.7 MB (149653771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cca6596b145b8e103ac3bc556c1b267b0dffc61e9400f7ea396730a7accf10e`  
		Last Modified: Tue, 18 Feb 2025 21:29:39 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0e1e357b5b9915c81d64de46ad296e5bac5d341fb14413f2f71ca0e34cf0dd`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197b5ca764ff548fa55d6b275d5de6da88c29077660995af974871b1860707f`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7ba24f601573bce233292a6d0890ee10011ebbc412ca53ad4529778942494`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7156998a59bacc352db9450332e37ced91d37d5a818d4264c05ab22fb652a4be`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.1` - unknown; unknown

```console
$ docker pull crate@sha256:bdf022e20bb34837bec75993654d840c4c72afc95c3b7600686b76874a575945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2340878f15cbc13a3d8c8494a7002f30d81d459a11c7b1554de23854c628d2`

```dockerfile
```

-	Layers:
	-	`sha256:e562fd8c51030a6728344bff6c7c82c0a53271cfe98276502fc0ef91a411adf2`  
		Last Modified: Wed, 19 Feb 2025 00:38:32 GMT  
		Size: 5.2 MB (5155069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725a014961de078af9a35614cfb486e17488ae54f01708de09b6b807ff3a7239`  
		Last Modified: Wed, 19 Feb 2025 00:38:33 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:057210175979c2c3e1923a4946e68e2aaa05258fe95f401471d3ac69a03b5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232343259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cf2307d56235cc186d15d56a3386b42043766582dc76001bf0ab9f5a9232b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 11:37:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.1.tar.gz.asc crate-5.10.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.1.tar.gz.asc     && tar -xf crate-5.10.1.tar.gz -C /crate --strip-components=1     && rm crate-5.10.1.tar.gz # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 11:37:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 11:37:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 11:37:21 GMT
WORKDIR /data
# Thu, 13 Feb 2025 11:37:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T11:37:21.577398 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.1
# Thu, 13 Feb 2025 11:37:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 11:37:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 08:45:30 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b02f2e8a13da0eae97095160d13c034035c694f70538f09411a09ba10308a`  
		Last Modified: Tue, 18 Feb 2025 21:30:00 GMT  
		Size: 15.4 MB (15421456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3069e8e758098e1903794ec516aa5b4c444b1a5b755d43340372d56e9b80109f`  
		Last Modified: Wed, 19 Feb 2025 02:53:51 GMT  
		Size: 150.3 MB (150333456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7534623abb40b966db4acd7a2e20a9cbb47c8775dc18286b26de01cca3490`  
		Last Modified: Tue, 18 Feb 2025 21:29:55 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b71f8980ca69b56f2de0a7d7b0fba11300f0f9b57160065e701269709e1382`  
		Last Modified: Tue, 18 Feb 2025 21:29:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108c22a110542fb61fd00a843073b9e449a6c7dd77a32d17989e98e0a01d2ff4`  
		Last Modified: Tue, 18 Feb 2025 21:29:48 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ca601928ed7ec5f3dcb60e7f7105b09b762b1adee6c0feab468e40ab06487`  
		Last Modified: Tue, 18 Feb 2025 21:29:48 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168c3513c13ca5e035cff09d1f976fb9a4d00e62f894ed7c5f1854396b338a29`  
		Last Modified: Tue, 18 Feb 2025 21:29:48 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.1` - unknown; unknown

```console
$ docker pull crate@sha256:2dfa98c6486ef7c77674ff767b410a55e17feb66716f8e57fda8e9b0c20ecd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef027cdd0752da3744ea160ca2e1395a8530cd903175c59bff27a8c68e34c85`

```dockerfile
```

-	Layers:
	-	`sha256:ef8d446aa50b963074c82c9c2b7188a0dd89bd831400ede6ccfed25c03eb548a`  
		Last Modified: Wed, 19 Feb 2025 00:38:35 GMT  
		Size: 5.2 MB (5152377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5070853231affa7e164b1061d71c6d895c7a512628e8eb78e63b162e2c7cb06f`  
		Last Modified: Wed, 19 Feb 2025 00:38:35 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7`

```console
$ docker pull crate@sha256:43616811da15804be5a5134a4a67b235f2661aca4da18d74b367db74e815cf02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:18ed0795fd515536aedc431a2e4fd595e2e8903fdced32995be7c8179564ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 MB (222473692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3380feb3474142b276669d506057975611857f6603cec8f9f112dfd5d876c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 15:36:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.6.tar.gz.asc crate-5.7.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.6.tar.gz.asc     && tar -xf crate-5.7.6.tar.gz -C /crate --strip-components=1     && rm crate-5.7.6.tar.gz # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 15:36:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 15:36:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 15:36:24 GMT
WORKDIR /data
# Thu, 30 Jan 2025 15:36:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T15:36:24.232944 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.6
# Thu, 30 Jan 2025 15:36:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 15:36:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Fri, 13 Dec 2024 15:55:44 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254467af6af8d54539de364df9914c81db0a46c2098bc5db770cefa342042c82`  
		Last Modified: Tue, 04 Feb 2025 20:24:33 GMT  
		Size: 14.1 MB (14148802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec741d4522fe5273ce35453c5fc8c676906dbb3204c97f4b127dee2dbb8fe912`  
		Last Modified: Thu, 06 Feb 2025 05:45:31 GMT  
		Size: 127.3 MB (127300400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e6024f4229768049397eeaf4c4a330900415b5b2b69ec7017c98d007813582`  
		Last Modified: Thu, 06 Feb 2025 05:45:26 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b41076b4a31aeb711bf08ad6dfed385041e4d1d536e4b7159b26ca64787741`  
		Last Modified: Thu, 06 Feb 2025 05:45:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd0c0376a2c568adb60c69c40f36eee4b01d34d554de3463fe6517f0fe2267`  
		Last Modified: Tue, 04 Feb 2025 20:24:39 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e46437bde054233098392d9cc0a0f5c2fb62ba462f57ed67117fee0f14a6a56`  
		Last Modified: Thu, 06 Feb 2025 05:45:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c3357cb43370f7a2c4ed8039390cb22268c72b5a7f7dc2b029adbe14a63479`  
		Last Modified: Thu, 06 Feb 2025 05:45:29 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:4f1aee1457eef2e84cf605d2d7bbb7a62f69df337350b2df6fa9ad3a6502b739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7e1b8ab92e2d8a0e804f48728361cba944de2688406eb24436658f19a3a9eb`

```dockerfile
```

-	Layers:
	-	`sha256:79ad35a1f957ff0cdb355dac65c0999a2269d4bf812595fd54583913d8c082dc`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 6.3 MB (6307614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63707574a469fb5256260de2b08956303124c0611a371df45ff210c37227bcfd`  
		Last Modified: Mon, 03 Feb 2025 22:27:52 GMT  
		Size: 22.8 KB (22826 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:56df24803f48b69ef67afe35a3e93d8d2041a328b9b2bb1dcdd24aa015726d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220990509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ae41fa9c6d6c159723a120b03cfd2d47ea4d5589ea4e5d79b726e90a7d6704`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 15:36:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.6.tar.gz.asc crate-5.7.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.6.tar.gz.asc     && tar -xf crate-5.7.6.tar.gz -C /crate --strip-components=1     && rm crate-5.7.6.tar.gz # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 15:36:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 15:36:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 15:36:24 GMT
WORKDIR /data
# Thu, 30 Jan 2025 15:36:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T15:36:24.232944 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.6
# Thu, 30 Jan 2025 15:36:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 15:36:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Fri, 13 Dec 2024 16:05:36 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Tue, 04 Feb 2025 20:23:47 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a694484b4f2b3cc627b9a4633882816f10897352a8cf82a335c5f7bc1daa1`  
		Last Modified: Tue, 04 Feb 2025 20:25:22 GMT  
		Size: 126.9 MB (126862648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c1120ca3977821758c69f8b6b8b977bde97b00c8913de6189dcab3ad3e6d95`  
		Last Modified: Thu, 13 Feb 2025 10:20:05 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522051da5393eb1667d5e5c8942b273ea9500a2c6f39ba2f6a09855bb8e8768e`  
		Last Modified: Thu, 13 Feb 2025 10:20:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793fd747b95fce4bc57e63c7697e08194f17e0deb3cc48fb00012854049f2a7`  
		Last Modified: Tue, 04 Feb 2025 20:25:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9c7b8b1a09e8fa4f0e8e349e3aa8455b092e7767e2ced9b5d4a8adeb994e8`  
		Last Modified: Thu, 13 Feb 2025 10:20:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612f1530af53fd7cb71104d96227621a0bdd8ab331c380554144c1b5227708c`  
		Last Modified: Thu, 13 Feb 2025 10:20:08 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7` - unknown; unknown

```console
$ docker pull crate@sha256:8546dae2b9393070cf5de782664e55fc4d8d5043d82ae5f373f2dbff969423bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6328485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88a57d6771cd6148eca809c037130a0eee707592f2ba9d6cc2248fb9e56c32f`

```dockerfile
```

-	Layers:
	-	`sha256:65a92c74cb9153eecbe3aee799b45ec390bb40474b07477f19e87749b15460dc`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 6.3 MB (6305534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5fbee603b6fc8414e65a4bada522e097094dab0f15da087b2465240aa196110`  
		Last Modified: Mon, 03 Feb 2025 22:29:11 GMT  
		Size: 23.0 KB (22951 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.7.6`

```console
$ docker pull crate@sha256:43616811da15804be5a5134a4a67b235f2661aca4da18d74b367db74e815cf02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.7.6` - linux; amd64

```console
$ docker pull crate@sha256:18ed0795fd515536aedc431a2e4fd595e2e8903fdced32995be7c8179564ca84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 MB (222473692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3380feb3474142b276669d506057975611857f6603cec8f9f112dfd5d876c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 15:36:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.6.tar.gz.asc crate-5.7.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.6.tar.gz.asc     && tar -xf crate-5.7.6.tar.gz -C /crate --strip-components=1     && rm crate-5.7.6.tar.gz # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 15:36:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 15:36:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 15:36:24 GMT
WORKDIR /data
# Thu, 30 Jan 2025 15:36:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T15:36:24.232944 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.6
# Thu, 30 Jan 2025 15:36:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 15:36:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Fri, 13 Dec 2024 15:55:44 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254467af6af8d54539de364df9914c81db0a46c2098bc5db770cefa342042c82`  
		Last Modified: Tue, 04 Feb 2025 20:24:33 GMT  
		Size: 14.1 MB (14148802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec741d4522fe5273ce35453c5fc8c676906dbb3204c97f4b127dee2dbb8fe912`  
		Last Modified: Thu, 06 Feb 2025 05:45:31 GMT  
		Size: 127.3 MB (127300400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e6024f4229768049397eeaf4c4a330900415b5b2b69ec7017c98d007813582`  
		Last Modified: Thu, 06 Feb 2025 05:45:26 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b41076b4a31aeb711bf08ad6dfed385041e4d1d536e4b7159b26ca64787741`  
		Last Modified: Thu, 06 Feb 2025 05:45:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd0c0376a2c568adb60c69c40f36eee4b01d34d554de3463fe6517f0fe2267`  
		Last Modified: Tue, 04 Feb 2025 20:24:39 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e46437bde054233098392d9cc0a0f5c2fb62ba462f57ed67117fee0f14a6a56`  
		Last Modified: Thu, 06 Feb 2025 05:45:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c3357cb43370f7a2c4ed8039390cb22268c72b5a7f7dc2b029adbe14a63479`  
		Last Modified: Thu, 06 Feb 2025 05:45:29 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.6` - unknown; unknown

```console
$ docker pull crate@sha256:4f1aee1457eef2e84cf605d2d7bbb7a62f69df337350b2df6fa9ad3a6502b739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7e1b8ab92e2d8a0e804f48728361cba944de2688406eb24436658f19a3a9eb`

```dockerfile
```

-	Layers:
	-	`sha256:79ad35a1f957ff0cdb355dac65c0999a2269d4bf812595fd54583913d8c082dc`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 6.3 MB (6307614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63707574a469fb5256260de2b08956303124c0611a371df45ff210c37227bcfd`  
		Last Modified: Mon, 03 Feb 2025 22:27:52 GMT  
		Size: 22.8 KB (22826 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.7.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:56df24803f48b69ef67afe35a3e93d8d2041a328b9b2bb1dcdd24aa015726d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220990509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ae41fa9c6d6c159723a120b03cfd2d47ea4d5589ea4e5d79b726e90a7d6704`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 15:36:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.6.tar.gz.asc crate-5.7.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.6.tar.gz.asc     && tar -xf crate-5.7.6.tar.gz -C /crate --strip-components=1     && rm crate-5.7.6.tar.gz # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 15:36:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 15:36:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 15:36:24 GMT
WORKDIR /data
# Thu, 30 Jan 2025 15:36:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T15:36:24.232944 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.6
# Thu, 30 Jan 2025 15:36:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 15:36:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 15:36:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Fri, 13 Dec 2024 16:05:36 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Tue, 04 Feb 2025 20:23:47 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a694484b4f2b3cc627b9a4633882816f10897352a8cf82a335c5f7bc1daa1`  
		Last Modified: Tue, 04 Feb 2025 20:25:22 GMT  
		Size: 126.9 MB (126862648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c1120ca3977821758c69f8b6b8b977bde97b00c8913de6189dcab3ad3e6d95`  
		Last Modified: Thu, 13 Feb 2025 10:20:05 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522051da5393eb1667d5e5c8942b273ea9500a2c6f39ba2f6a09855bb8e8768e`  
		Last Modified: Thu, 13 Feb 2025 10:20:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793fd747b95fce4bc57e63c7697e08194f17e0deb3cc48fb00012854049f2a7`  
		Last Modified: Tue, 04 Feb 2025 20:25:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9c7b8b1a09e8fa4f0e8e349e3aa8455b092e7767e2ced9b5d4a8adeb994e8`  
		Last Modified: Thu, 13 Feb 2025 10:20:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612f1530af53fd7cb71104d96227621a0bdd8ab331c380554144c1b5227708c`  
		Last Modified: Thu, 13 Feb 2025 10:20:08 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.7.6` - unknown; unknown

```console
$ docker pull crate@sha256:8546dae2b9393070cf5de782664e55fc4d8d5043d82ae5f373f2dbff969423bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6328485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88a57d6771cd6148eca809c037130a0eee707592f2ba9d6cc2248fb9e56c32f`

```dockerfile
```

-	Layers:
	-	`sha256:65a92c74cb9153eecbe3aee799b45ec390bb40474b07477f19e87749b15460dc`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 6.3 MB (6305534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5fbee603b6fc8414e65a4bada522e097094dab0f15da087b2465240aa196110`  
		Last Modified: Mon, 03 Feb 2025 22:29:11 GMT  
		Size: 23.0 KB (22951 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.8`

```console
$ docker pull crate@sha256:8eaaa7b8c69bf129c7bfcb7a1cd75a5d041c0fb87d486962b17c4d9e84e219bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.8` - linux; amd64

```console
$ docker pull crate@sha256:b22680dd8c850160a3ca3c64222c58668f131334c3b97ede9f92cb0d53d839c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225138679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3e44a76dd0d896a6245eef05117086c7184760610677bda3c6d26a52362b87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 16:42:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.6.tar.gz.asc crate-5.8.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.6.tar.gz.asc     && tar -xf crate-5.8.6.tar.gz -C /crate --strip-components=1     && rm crate-5.8.6.tar.gz # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 16:42:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 16:42:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 16:42:57 GMT
WORKDIR /data
# Thu, 30 Jan 2025 16:42:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T16:42:57.310116 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.6
# Thu, 30 Jan 2025 16:42:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 16:42:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Fri, 13 Dec 2024 15:55:44 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf9946c1bea126dd289995cb9fe4ee972e362c34682631c30c2c21bd2e6ecc`  
		Last Modified: Tue, 04 Feb 2025 20:23:04 GMT  
		Size: 14.1 MB (14148854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac03f18a4b6f7343ab9933dfa5bc4b782cf73b2875a1abfe5cbf4766256e625`  
		Last Modified: Thu, 06 Feb 2025 05:40:55 GMT  
		Size: 130.0 MB (129965335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985fe587a198cb5e064002316fb9cd22c6b30ab1ac82a4075edf8d479f2f7cc`  
		Last Modified: Tue, 04 Feb 2025 11:58:42 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2928f35de96488de94410e8fddd3e70f485f29c816a279087908b554e8cc706d`  
		Last Modified: Wed, 05 Feb 2025 17:15:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa264a761fd1fed3689fa5ab9867f3702f4061afd2b7e0d854e800da33c7f1c`  
		Last Modified: Tue, 04 Feb 2025 20:23:11 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae068b8169ea2d576728ae29925f19164bd80dbd5f6a09a4191e018a0e64db`  
		Last Modified: Thu, 06 Feb 2025 05:40:50 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b284bef0d222ffade4d31491dac20a13ce7059bd59244b308f5417b2eb3a4d`  
		Last Modified: Wed, 05 Feb 2025 15:46:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:c54f3d4f8111056f39ce5aae78081790b4b257a25b15297c003b0c4cbb2926dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6323304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23372c9f21ebb3a5ee0a537c164f4b4f853f2a5d747f0cb7489afbd85bebca8`

```dockerfile
```

-	Layers:
	-	`sha256:e84e45619740f426db47f582c6a4fa72cf45c20cc49de86fcbe6641e9c5e1a01`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 6.3 MB (6300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24148919db358c8cecee9dc07d387bba928ecabe02467579be5b6e41dab24038`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 22.8 KB (22826 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bfdc8a8faf6e4ecbd04f4f395f208a7e430b454b06df52eb67e60f8801440861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223540739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5added6112601e5abfb14d1b73567dec272004ee864ffeca4dd9f7572fad518f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 16:42:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.6.tar.gz.asc crate-5.8.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.6.tar.gz.asc     && tar -xf crate-5.8.6.tar.gz -C /crate --strip-components=1     && rm crate-5.8.6.tar.gz # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 16:42:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 16:42:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 16:42:57 GMT
WORKDIR /data
# Thu, 30 Jan 2025 16:42:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T16:42:57.310116 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.6
# Thu, 30 Jan 2025 16:42:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 16:42:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Fri, 13 Dec 2024 16:05:36 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Tue, 04 Feb 2025 20:23:47 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925575c4ad696b0392b1e5623678226cf327e83ef5dd77249f56efb83e08db7f`  
		Last Modified: Thu, 13 Feb 2025 10:19:49 GMT  
		Size: 129.4 MB (129412881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f56b72c56eaef6be6c960e2edbdd52131ca0d785fe2814fd0cc98c348a0842`  
		Last Modified: Sun, 09 Feb 2025 00:48:25 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17da6553dd1a472e3daefd9753b66f5290c055c25008fa3b9d21847fdebeb16`  
		Last Modified: Tue, 04 Feb 2025 20:23:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768bb6ba7c924dd6d4374c154c75f42b420500db97f26e46ad78a44d93dacac6`  
		Last Modified: Thu, 13 Feb 2025 10:19:42 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3da709d79ed5b345bf3ae95fab349ffc4f3ee6f5a0af717d96c5e95b6e3cf81`  
		Last Modified: Sun, 09 Feb 2025 00:48:29 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e86115430a3330e27af6bbd3793fa03f403720f84d0ec347f31d85d18709094`  
		Last Modified: Sun, 09 Feb 2025 00:48:31 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:39334effa5723f5c5be9daefd89e6285099626ac85b61aefb52c7bf510bf3486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6320733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a988c18880d0246452e33bbb744595b2e8362d60f9739529c93965bb47805563`

```dockerfile
```

-	Layers:
	-	`sha256:f6e9fb7c38563db8dc6d44f6c25d5135bd18ac7eab9a4383b1ca816179a845d7`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 6.3 MB (6297784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c18b938e7f03ecd9760265c48521b957dc7cad62f0dc5761077a4337ece73322`  
		Last Modified: Mon, 03 Feb 2025 22:28:19 GMT  
		Size: 22.9 KB (22949 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.8.6`

```console
$ docker pull crate@sha256:8eaaa7b8c69bf129c7bfcb7a1cd75a5d041c0fb87d486962b17c4d9e84e219bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.8.6` - linux; amd64

```console
$ docker pull crate@sha256:b22680dd8c850160a3ca3c64222c58668f131334c3b97ede9f92cb0d53d839c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225138679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3e44a76dd0d896a6245eef05117086c7184760610677bda3c6d26a52362b87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 16:42:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.6.tar.gz.asc crate-5.8.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.6.tar.gz.asc     && tar -xf crate-5.8.6.tar.gz -C /crate --strip-components=1     && rm crate-5.8.6.tar.gz # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 16:42:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 16:42:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 16:42:57 GMT
WORKDIR /data
# Thu, 30 Jan 2025 16:42:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T16:42:57.310116 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.6
# Thu, 30 Jan 2025 16:42:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 16:42:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Fri, 13 Dec 2024 15:55:44 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf9946c1bea126dd289995cb9fe4ee972e362c34682631c30c2c21bd2e6ecc`  
		Last Modified: Tue, 04 Feb 2025 20:23:04 GMT  
		Size: 14.1 MB (14148854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac03f18a4b6f7343ab9933dfa5bc4b782cf73b2875a1abfe5cbf4766256e625`  
		Last Modified: Thu, 06 Feb 2025 05:40:55 GMT  
		Size: 130.0 MB (129965335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985fe587a198cb5e064002316fb9cd22c6b30ab1ac82a4075edf8d479f2f7cc`  
		Last Modified: Tue, 04 Feb 2025 11:58:42 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2928f35de96488de94410e8fddd3e70f485f29c816a279087908b554e8cc706d`  
		Last Modified: Wed, 05 Feb 2025 17:15:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa264a761fd1fed3689fa5ab9867f3702f4061afd2b7e0d854e800da33c7f1c`  
		Last Modified: Tue, 04 Feb 2025 20:23:11 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae068b8169ea2d576728ae29925f19164bd80dbd5f6a09a4191e018a0e64db`  
		Last Modified: Thu, 06 Feb 2025 05:40:50 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b284bef0d222ffade4d31491dac20a13ce7059bd59244b308f5417b2eb3a4d`  
		Last Modified: Wed, 05 Feb 2025 15:46:19 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8.6` - unknown; unknown

```console
$ docker pull crate@sha256:c54f3d4f8111056f39ce5aae78081790b4b257a25b15297c003b0c4cbb2926dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6323304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23372c9f21ebb3a5ee0a537c164f4b4f853f2a5d747f0cb7489afbd85bebca8`

```dockerfile
```

-	Layers:
	-	`sha256:e84e45619740f426db47f582c6a4fa72cf45c20cc49de86fcbe6641e9c5e1a01`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 6.3 MB (6300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24148919db358c8cecee9dc07d387bba928ecabe02467579be5b6e41dab24038`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 22.8 KB (22826 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.8.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bfdc8a8faf6e4ecbd04f4f395f208a7e430b454b06df52eb67e60f8801440861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223540739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5added6112601e5abfb14d1b73567dec272004ee864ffeca4dd9f7572fad518f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 16:42:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.6.tar.gz.asc crate-5.8.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.6.tar.gz.asc     && tar -xf crate-5.8.6.tar.gz -C /crate --strip-components=1     && rm crate-5.8.6.tar.gz # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 16:42:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 16:42:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 16:42:57 GMT
WORKDIR /data
# Thu, 30 Jan 2025 16:42:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T16:42:57.310116 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.6
# Thu, 30 Jan 2025 16:42:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 16:42:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 16:42:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Fri, 13 Dec 2024 16:05:36 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Tue, 04 Feb 2025 20:23:47 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925575c4ad696b0392b1e5623678226cf327e83ef5dd77249f56efb83e08db7f`  
		Last Modified: Thu, 13 Feb 2025 10:19:49 GMT  
		Size: 129.4 MB (129412881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f56b72c56eaef6be6c960e2edbdd52131ca0d785fe2814fd0cc98c348a0842`  
		Last Modified: Sun, 09 Feb 2025 00:48:25 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17da6553dd1a472e3daefd9753b66f5290c055c25008fa3b9d21847fdebeb16`  
		Last Modified: Tue, 04 Feb 2025 20:23:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768bb6ba7c924dd6d4374c154c75f42b420500db97f26e46ad78a44d93dacac6`  
		Last Modified: Thu, 13 Feb 2025 10:19:42 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3da709d79ed5b345bf3ae95fab349ffc4f3ee6f5a0af717d96c5e95b6e3cf81`  
		Last Modified: Sun, 09 Feb 2025 00:48:29 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e86115430a3330e27af6bbd3793fa03f403720f84d0ec347f31d85d18709094`  
		Last Modified: Sun, 09 Feb 2025 00:48:31 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8.6` - unknown; unknown

```console
$ docker pull crate@sha256:39334effa5723f5c5be9daefd89e6285099626ac85b61aefb52c7bf510bf3486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6320733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a988c18880d0246452e33bbb744595b2e8362d60f9739529c93965bb47805563`

```dockerfile
```

-	Layers:
	-	`sha256:f6e9fb7c38563db8dc6d44f6c25d5135bd18ac7eab9a4383b1ca816179a845d7`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 6.3 MB (6297784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c18b938e7f03ecd9760265c48521b957dc7cad62f0dc5761077a4337ece73322`  
		Last Modified: Mon, 03 Feb 2025 22:28:19 GMT  
		Size: 22.9 KB (22949 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:8ee4e7c5828423e26b82930db9dbe2b6a643cf6c239f02b9fc01cf8acc900f4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:cdecdfe5f7bb16386c56f98ed83f6c71cc7267b607b6120550f0103df8173b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232318640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c62763f9cdd816d464bc4215cc3c8835f1485840838261ced993d0183d65ed2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 08:21:45 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.10.tar.gz.asc crate-5.9.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.10.tar.gz.asc     && tar -xf crate-5.9.10.tar.gz -C /crate --strip-components=1     && rm crate-5.9.10.tar.gz # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 08:21:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 08:21:45 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 08:21:45 GMT
WORKDIR /data
# Thu, 13 Feb 2025 08:21:45 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 08:21:45 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T08:21:45.977195 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.10
# Thu, 13 Feb 2025 08:21:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 08:21:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Wed, 05 Feb 2025 05:27:15 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776886394fa1b302292fb905ba724b5eafa0cd5983cd1bdbc417eebf6718c04`  
		Last Modified: Tue, 18 Feb 2025 21:29:53 GMT  
		Size: 15.4 MB (15360678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8cebb67ecf3b065c6e93ef7ba489c6e948071a61d9b1fe48b879b1573d78e5`  
		Last Modified: Wed, 19 Feb 2025 02:38:22 GMT  
		Size: 149.0 MB (149007926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaa24793d7dfbf434dada4b931f23e251fba3c2c1f94635bc4a98f23eda3b49`  
		Last Modified: Tue, 18 Feb 2025 21:29:42 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5395069e3dbfa2a3e3eb9625e317bddc0d4323135f2270aabc1823c68ffe8a45`  
		Last Modified: Tue, 18 Feb 2025 21:29:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d602d36b1c09b55da1e5723970b0424fcf9bfd03dd8c4acca344bd997cf9085b`  
		Last Modified: Tue, 18 Feb 2025 21:29:41 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936591c428056162330ff4ee79c5fd55dc7d10e11ab637768a45407595e5bf4e`  
		Last Modified: Tue, 18 Feb 2025 21:29:41 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e1a13418f92827985f23a3489209d41bb94d966f85a366b08d45bf3035ba1d`  
		Last Modified: Tue, 18 Feb 2025 21:29:41 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:df41fff59e5de1a8c6b61d160b673226771726b2d50d18ba6270de8cc1689e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61d6758c4c2751528cb308d7cd30c156d881b4e9165286dfc7a17f5965337ed`

```dockerfile
```

-	Layers:
	-	`sha256:8305df36285f3be658af3c58ee5e6121a695c5ff472198faefdf6e11e9e4ae05`  
		Last Modified: Wed, 19 Feb 2025 00:38:43 GMT  
		Size: 5.2 MB (5152897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7726e7fb8ef7752765e2902adecdfa9e173d73f2bc48717203195e7ed14892e0`  
		Last Modified: Wed, 19 Feb 2025 00:38:43 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a8f102a27df7796aaee35a1506e0146a3d3ff3f620eb069f2ba89da7c71e702f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231716465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7839ba17bd0b13251a7c80a0cecc55278b22ed3b00a954f701286fe5261cd077`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 08:21:45 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.10.tar.gz.asc crate-5.9.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.10.tar.gz.asc     && tar -xf crate-5.9.10.tar.gz -C /crate --strip-components=1     && rm crate-5.9.10.tar.gz # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 08:21:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 08:21:45 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 08:21:45 GMT
WORKDIR /data
# Thu, 13 Feb 2025 08:21:45 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 08:21:45 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T08:21:45.977195 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.10
# Thu, 13 Feb 2025 08:21:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 08:21:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 08:45:30 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b02f2e8a13da0eae97095160d13c034035c694f70538f09411a09ba10308a`  
		Last Modified: Tue, 18 Feb 2025 21:30:00 GMT  
		Size: 15.4 MB (15421456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd035166f890172321b5e3e3095cc2969c3fd2ba2c0dfcdf1d83df0d255d8969`  
		Last Modified: Wed, 19 Feb 2025 17:56:58 GMT  
		Size: 149.7 MB (149706667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a306bc1ce8b99face284d3d84985fe152b79bf3eb93b57836cb5a81f103fc9ce`  
		Last Modified: Tue, 18 Feb 2025 21:30:30 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a2869ca0e96c57cec0bb57f85bfc4636e977113b379110af9e3c44fde96e3d`  
		Last Modified: Tue, 18 Feb 2025 21:30:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69941a2aa75f90b23dff6ec29b17ca8f99b8e1201476ad60630925d453dbe6d`  
		Last Modified: Tue, 18 Feb 2025 21:30:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f7485bbd675d7db773dd7a5e45f64200c89a6b13988781b68a18bda995c219`  
		Last Modified: Tue, 18 Feb 2025 21:30:23 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c194fc30dcdc9c164b9e3666a101a62d3a60e92a55e0b000b8704ba8d90a79a1`  
		Last Modified: Tue, 18 Feb 2025 21:30:23 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:eef1927cb6471fa6dda4e4acd6a376090ae8adbf09f85198ec9701bc50a297a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24450c55e648f0f1a727123eb3d568389bc76ab26bdbd51cf7e0cac7b08ec222`

```dockerfile
```

-	Layers:
	-	`sha256:adf727fc7dfcc7ee60b5d7dfb6ea4c67aa20381d3cdf2e24b835be4faf28186e`  
		Last Modified: Wed, 19 Feb 2025 00:38:46 GMT  
		Size: 5.2 MB (5150193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530e8697cf706f58b9a5908fd3dd266065e3ca706586d4ee9c923bff8365f44d`  
		Last Modified: Wed, 19 Feb 2025 00:38:46 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.10`

```console
$ docker pull crate@sha256:8ee4e7c5828423e26b82930db9dbe2b6a643cf6c239f02b9fc01cf8acc900f4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.10` - linux; amd64

```console
$ docker pull crate@sha256:cdecdfe5f7bb16386c56f98ed83f6c71cc7267b607b6120550f0103df8173b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232318640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c62763f9cdd816d464bc4215cc3c8835f1485840838261ced993d0183d65ed2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 08:21:45 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.10.tar.gz.asc crate-5.9.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.10.tar.gz.asc     && tar -xf crate-5.9.10.tar.gz -C /crate --strip-components=1     && rm crate-5.9.10.tar.gz # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 08:21:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 08:21:45 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 08:21:45 GMT
WORKDIR /data
# Thu, 13 Feb 2025 08:21:45 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 08:21:45 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T08:21:45.977195 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.10
# Thu, 13 Feb 2025 08:21:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 08:21:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Wed, 05 Feb 2025 05:27:15 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776886394fa1b302292fb905ba724b5eafa0cd5983cd1bdbc417eebf6718c04`  
		Last Modified: Tue, 18 Feb 2025 21:29:53 GMT  
		Size: 15.4 MB (15360678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8cebb67ecf3b065c6e93ef7ba489c6e948071a61d9b1fe48b879b1573d78e5`  
		Last Modified: Wed, 19 Feb 2025 02:38:22 GMT  
		Size: 149.0 MB (149007926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaa24793d7dfbf434dada4b931f23e251fba3c2c1f94635bc4a98f23eda3b49`  
		Last Modified: Tue, 18 Feb 2025 21:29:42 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5395069e3dbfa2a3e3eb9625e317bddc0d4323135f2270aabc1823c68ffe8a45`  
		Last Modified: Tue, 18 Feb 2025 21:29:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d602d36b1c09b55da1e5723970b0424fcf9bfd03dd8c4acca344bd997cf9085b`  
		Last Modified: Tue, 18 Feb 2025 21:29:41 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936591c428056162330ff4ee79c5fd55dc7d10e11ab637768a45407595e5bf4e`  
		Last Modified: Tue, 18 Feb 2025 21:29:41 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e1a13418f92827985f23a3489209d41bb94d966f85a366b08d45bf3035ba1d`  
		Last Modified: Tue, 18 Feb 2025 21:29:41 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.10` - unknown; unknown

```console
$ docker pull crate@sha256:df41fff59e5de1a8c6b61d160b673226771726b2d50d18ba6270de8cc1689e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61d6758c4c2751528cb308d7cd30c156d881b4e9165286dfc7a17f5965337ed`

```dockerfile
```

-	Layers:
	-	`sha256:8305df36285f3be658af3c58ee5e6121a695c5ff472198faefdf6e11e9e4ae05`  
		Last Modified: Wed, 19 Feb 2025 00:38:43 GMT  
		Size: 5.2 MB (5152897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7726e7fb8ef7752765e2902adecdfa9e173d73f2bc48717203195e7ed14892e0`  
		Last Modified: Wed, 19 Feb 2025 00:38:43 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a8f102a27df7796aaee35a1506e0146a3d3ff3f620eb069f2ba89da7c71e702f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231716465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7839ba17bd0b13251a7c80a0cecc55278b22ed3b00a954f701286fe5261cd077`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 08:21:45 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.10.tar.gz.asc crate-5.9.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.10.tar.gz.asc     && tar -xf crate-5.9.10.tar.gz -C /crate --strip-components=1     && rm crate-5.9.10.tar.gz # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 08:21:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 08:21:45 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 08:21:45 GMT
WORKDIR /data
# Thu, 13 Feb 2025 08:21:45 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 08:21:45 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T08:21:45.977195 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.10
# Thu, 13 Feb 2025 08:21:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 08:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 08:21:45 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 08:45:30 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b02f2e8a13da0eae97095160d13c034035c694f70538f09411a09ba10308a`  
		Last Modified: Tue, 18 Feb 2025 21:30:00 GMT  
		Size: 15.4 MB (15421456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd035166f890172321b5e3e3095cc2969c3fd2ba2c0dfcdf1d83df0d255d8969`  
		Last Modified: Wed, 19 Feb 2025 17:56:58 GMT  
		Size: 149.7 MB (149706667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a306bc1ce8b99face284d3d84985fe152b79bf3eb93b57836cb5a81f103fc9ce`  
		Last Modified: Tue, 18 Feb 2025 21:30:30 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a2869ca0e96c57cec0bb57f85bfc4636e977113b379110af9e3c44fde96e3d`  
		Last Modified: Tue, 18 Feb 2025 21:30:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69941a2aa75f90b23dff6ec29b17ca8f99b8e1201476ad60630925d453dbe6d`  
		Last Modified: Tue, 18 Feb 2025 21:30:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f7485bbd675d7db773dd7a5e45f64200c89a6b13988781b68a18bda995c219`  
		Last Modified: Tue, 18 Feb 2025 21:30:23 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c194fc30dcdc9c164b9e3666a101a62d3a60e92a55e0b000b8704ba8d90a79a1`  
		Last Modified: Tue, 18 Feb 2025 21:30:23 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.10` - unknown; unknown

```console
$ docker pull crate@sha256:eef1927cb6471fa6dda4e4acd6a376090ae8adbf09f85198ec9701bc50a297a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24450c55e648f0f1a727123eb3d568389bc76ab26bdbd51cf7e0cac7b08ec222`

```dockerfile
```

-	Layers:
	-	`sha256:adf727fc7dfcc7ee60b5d7dfb6ea4c67aa20381d3cdf2e24b835be4faf28186e`  
		Last Modified: Wed, 19 Feb 2025 00:38:46 GMT  
		Size: 5.2 MB (5150193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530e8697cf706f58b9a5908fd3dd266065e3ca706586d4ee9c923bff8365f44d`  
		Last Modified: Wed, 19 Feb 2025 00:38:46 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:58eb8c71600008609bca10e9c7e1a3784d505d9f04991fa331423807c91d12bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:666bb236ef15bc4c081fb0d6420b0df94074bac139bd58b6624d77aae2c1ea55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aba0995eb00b98f9b0ffefc9d2ad7a2849aa1ffc3b091d68bd737520f2814d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 11:37:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.1.tar.gz.asc crate-5.10.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.1.tar.gz.asc     && tar -xf crate-5.10.1.tar.gz -C /crate --strip-components=1     && rm crate-5.10.1.tar.gz # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 11:37:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 11:37:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 11:37:21 GMT
WORKDIR /data
# Thu, 13 Feb 2025 11:37:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T11:37:21.577398 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.1
# Thu, 13 Feb 2025 11:37:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 11:37:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Wed, 05 Feb 2025 05:27:15 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e08da2fbb8511dde834ed4e9a1aceb1ff391def8f04a3f2066dced44ba18bc6`  
		Last Modified: Tue, 18 Feb 2025 21:29:40 GMT  
		Size: 15.4 MB (15360839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7a32e8ee0628c751dae3e049df63437944254b491f7ed187909bfea65914b8`  
		Last Modified: Wed, 19 Feb 2025 00:38:55 GMT  
		Size: 149.7 MB (149653771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cca6596b145b8e103ac3bc556c1b267b0dffc61e9400f7ea396730a7accf10e`  
		Last Modified: Tue, 18 Feb 2025 21:29:39 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0e1e357b5b9915c81d64de46ad296e5bac5d341fb14413f2f71ca0e34cf0dd`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197b5ca764ff548fa55d6b275d5de6da88c29077660995af974871b1860707f`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb7ba24f601573bce233292a6d0890ee10011ebbc412ca53ad4529778942494`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7156998a59bacc352db9450332e37ced91d37d5a818d4264c05ab22fb652a4be`  
		Last Modified: Tue, 18 Feb 2025 21:29:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:bdf022e20bb34837bec75993654d840c4c72afc95c3b7600686b76874a575945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2340878f15cbc13a3d8c8494a7002f30d81d459a11c7b1554de23854c628d2`

```dockerfile
```

-	Layers:
	-	`sha256:e562fd8c51030a6728344bff6c7c82c0a53271cfe98276502fc0ef91a411adf2`  
		Last Modified: Wed, 19 Feb 2025 00:38:32 GMT  
		Size: 5.2 MB (5155069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725a014961de078af9a35614cfb486e17488ae54f01708de09b6b807ff3a7239`  
		Last Modified: Wed, 19 Feb 2025 00:38:33 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:057210175979c2c3e1923a4946e68e2aaa05258fe95f401471d3ac69a03b5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232343259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cf2307d56235cc186d15d56a3386b42043766582dc76001bf0ab9f5a9232b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 11:37:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.1.tar.gz.asc crate-5.10.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.1.tar.gz.asc     && tar -xf crate-5.10.1.tar.gz -C /crate --strip-components=1     && rm crate-5.10.1.tar.gz # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 11:37:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 13 Feb 2025 11:37:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
VOLUME [/data]
# Thu, 13 Feb 2025 11:37:21 GMT
WORKDIR /data
# Thu, 13 Feb 2025 11:37:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-02-13T11:37:21.577398 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.1
# Thu, 13 Feb 2025 11:37:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 13 Feb 2025 11:37:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Feb 2025 11:37:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 08:45:30 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b02f2e8a13da0eae97095160d13c034035c694f70538f09411a09ba10308a`  
		Last Modified: Tue, 18 Feb 2025 21:30:00 GMT  
		Size: 15.4 MB (15421456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3069e8e758098e1903794ec516aa5b4c444b1a5b755d43340372d56e9b80109f`  
		Last Modified: Wed, 19 Feb 2025 02:53:51 GMT  
		Size: 150.3 MB (150333456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7534623abb40b966db4acd7a2e20a9cbb47c8775dc18286b26de01cca3490`  
		Last Modified: Tue, 18 Feb 2025 21:29:55 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b71f8980ca69b56f2de0a7d7b0fba11300f0f9b57160065e701269709e1382`  
		Last Modified: Tue, 18 Feb 2025 21:29:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108c22a110542fb61fd00a843073b9e449a6c7dd77a32d17989e98e0a01d2ff4`  
		Last Modified: Tue, 18 Feb 2025 21:29:48 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ca601928ed7ec5f3dcb60e7f7105b09b762b1adee6c0feab468e40ab06487`  
		Last Modified: Tue, 18 Feb 2025 21:29:48 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168c3513c13ca5e035cff09d1f976fb9a4d00e62f894ed7c5f1854396b338a29`  
		Last Modified: Tue, 18 Feb 2025 21:29:48 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:2dfa98c6486ef7c77674ff767b410a55e17feb66716f8e57fda8e9b0c20ecd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef027cdd0752da3744ea160ca2e1395a8530cd903175c59bff27a8c68e34c85`

```dockerfile
```

-	Layers:
	-	`sha256:ef8d446aa50b963074c82c9c2b7188a0dd89bd831400ede6ccfed25c03eb548a`  
		Last Modified: Wed, 19 Feb 2025 00:38:35 GMT  
		Size: 5.2 MB (5152377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5070853231affa7e164b1061d71c6d895c7a512628e8eb78e63b162e2c7cb06f`  
		Last Modified: Wed, 19 Feb 2025 00:38:35 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json
