<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.13`](#crate51013)
-	[`crate:6.0`](#crate60)
-	[`crate:6.0.3`](#crate603)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:cfce7e180eafa1eb57ebda20a7b3678d65fbac2bbd08ba7e5a7b0dbf553d7696
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:4b516b37460f0a2bacf03586b7067d2bd892be50a9b9eb82ef9cdfe8472da51a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda42af558eee9b33a0ef939a1bd3dd0b8e95d96536d7053dab40c1d293d66bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 11:11:11 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.12.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.12.tar.gz.asc crate-5.10.12.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.12.tar.gz.asc     && tar -xf crate-5.10.12.tar.gz -C /crate --strip-components=1     && rm crate-5.10.12.tar.gz # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Sep 2025 11:11:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 23 Sep 2025 11:11:11 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
VOLUME [/data]
# Tue, 23 Sep 2025 11:11:11 GMT
WORKDIR /data
# Tue, 23 Sep 2025 11:11:11 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 23 Sep 2025 11:11:11 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-09-23T11:11:11.026928 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.12
# Tue, 23 Sep 2025 11:11:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 11:11:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd45a9bbd324d3ec8cf611471fe9203d1fc92e7a5cb0596b21fc6ef21f372c`  
		Last Modified: Fri, 26 Sep 2025 16:50:03 GMT  
		Size: 14.5 MB (14534270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbbdfd034e4076e85edb81fc8739efee091a4679cf36827b6be3faa9b025433`  
		Last Modified: Fri, 26 Sep 2025 16:56:50 GMT  
		Size: 149.7 MB (149701723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eda2422595506c72c37dab60fa107d3923fd9c2828c28c327366be58499b55`  
		Last Modified: Fri, 26 Sep 2025 16:50:01 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdfc5e3b9f2744ab9e863146e280e8bcf0fb5436ab062ddaeb041bbb790feab`  
		Last Modified: Fri, 26 Sep 2025 16:50:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bb92727650877aac6ffe551be683b458cff9faa14341132b73e735e4ae30b1`  
		Last Modified: Fri, 26 Sep 2025 16:50:01 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c24f0f41eefe38b2d899499e1345ed130bb11e0e6c564799628049eb28fe54`  
		Last Modified: Fri, 26 Sep 2025 16:50:01 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079de746a0a732b05806a834901d257ea6fadeedaeee8be0aeb06446cd340d13`  
		Last Modified: Fri, 26 Sep 2025 16:50:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:cefae9dc00274c1e240cd9712367abdfe30c6dcc44b975818bf650331c844af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e6152604ae20c0205ac2ea6e976ddf3a0f5a3cec2ab35d6d49f6b2c6be84d6`

```dockerfile
```

-	Layers:
	-	`sha256:06276497cfcb5edd8b7046682614a5309c53f7f1f00ca9815c8e82452283faa9`  
		Last Modified: Fri, 26 Sep 2025 17:38:26 GMT  
		Size: 5.2 MB (5188425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5502301e9236648610871132b6cfd81680abb7a1c57d738ae8926d64ec7f8192`  
		Last Modified: Fri, 26 Sep 2025 17:38:27 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a73bf02628a2aca666b1a8e106d73477af69b42576d33e0ce3697528a380b948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232429033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f47b9288e7125e557f24694c7b3c7c4942911fe4afd0e0c126f800d80c1cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 11:11:11 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.12.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.12.tar.gz.asc crate-5.10.12.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.12.tar.gz.asc     && tar -xf crate-5.10.12.tar.gz -C /crate --strip-components=1     && rm crate-5.10.12.tar.gz # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Sep 2025 11:11:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 23 Sep 2025 11:11:11 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
VOLUME [/data]
# Tue, 23 Sep 2025 11:11:11 GMT
WORKDIR /data
# Tue, 23 Sep 2025 11:11:11 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 23 Sep 2025 11:11:11 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-09-23T11:11:11.026928 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.12
# Tue, 23 Sep 2025 11:11:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 11:11:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 11:11:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be74d987c0956eb04dee0a3ee54d8be97e13470f5deebf55b412bc88ded6dbf`  
		Last Modified: Fri, 26 Sep 2025 16:56:28 GMT  
		Size: 14.6 MB (14585461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177bb34287b65672c4efeda49a21d425127347511b33c0c5fa97557c1b164522`  
		Last Modified: Fri, 26 Sep 2025 16:56:43 GMT  
		Size: 150.4 MB (150380059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377ef750fe2ac31a0ea589da0eabbab50900fa1729ae6e6bc72250cb1248e4ad`  
		Last Modified: Fri, 26 Sep 2025 16:56:27 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12eec45abeaefe4aff669a6c1a1f3b7406a86152e8c9d7f4fb70ff891a97782d`  
		Last Modified: Fri, 26 Sep 2025 16:56:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfa62b7418a30d3d164bd7f36392ed385babe4dd17b6100c0d9ffa46a98d806`  
		Last Modified: Fri, 26 Sep 2025 16:56:28 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3925eced3213e966391e627bc264e202c71940263f699b9d07745e36d0e3777`  
		Last Modified: Fri, 26 Sep 2025 16:56:28 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615c5bb2a3a9b3bb8763a5fa27c0ee831d03742bb8ace7f407002b5f121f8218`  
		Last Modified: Fri, 26 Sep 2025 16:56:26 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:ef9f9968cc71bca1fab290ca778cfabdef620bde728050bc5c318da1bfbc4aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240f2808f474ec80a87d154c09b775d38eb3496644059e165d3380c9fd23477d`

```dockerfile
```

-	Layers:
	-	`sha256:571bb0cf15c06df5f066216d51b102727c7cf60238cee70962e8e40b12b712d6`  
		Last Modified: Fri, 26 Sep 2025 17:38:32 GMT  
		Size: 5.2 MB (5185733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f7c1d2447fdef02a46ed00f02a93c716725daaa16f440162af9f118182ccc7`  
		Last Modified: Fri, 26 Sep 2025 17:38:33 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.13`

**does not exist** (yet?)

## `crate:6.0`

```console
$ docker pull crate@sha256:40a21da22a3e8e9fc1b94fe99f748fd5c4d56bb47314d1ff0377863857853294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:c4b28997e05792969ff60da2f3f0bb9ba08affee12e97ce92f37fc7c975d55f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232532764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f8ba5cdd4a48274f96c904452e16afeceae5123547393abe9b549364943282`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 10:56:18 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.2.tar.gz.asc crate-6.0.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.2.tar.gz.asc     && tar -xf crate-6.0.2.tar.gz -C /crate --strip-components=1     && rm crate-6.0.2.tar.gz # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 10:56:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 24 Sep 2025 10:56:18 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
VOLUME [/data]
# Wed, 24 Sep 2025 10:56:18 GMT
WORKDIR /data
# Wed, 24 Sep 2025 10:56:18 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 24 Sep 2025 10:56:18 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-09-24T10:56:18.920121 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.2
# Wed, 24 Sep 2025 10:56:18 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:56:18 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b7bb613a9da8b3b7ba3f96955aefac5f2770fa2911e95537bd89839c9e8752`  
		Last Modified: Mon, 29 Sep 2025 17:41:14 GMT  
		Size: 14.5 MB (14534475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a64eaaab2fcb00da0542899a32188f3d9d9bec83d4b505b24aff039a5819a3`  
		Last Modified: Mon, 29 Sep 2025 20:39:21 GMT  
		Size: 149.0 MB (149023730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5758847a400e037beb7f825fa5c450ebac7902fd329dc018ac18155dd65403d`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ede8f6eb8e27840852ea10ab10ada37cc2f0064604d98438a97ba8e23d2cb89`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558f96047b5a4ead90c5ea3f94c3d328084ea90057ff4aac20e6232bcc1b19a1`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03b3bbae92ce36eaf4c7e8926a939278a835e4622e5b4bda631f45c3c6a3020`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9667d72456f79b70e65f77fb5ddd4efca8b7c5ec7652eb64583dadabcf9c128`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:1727e28c728f7f77bac28a93a2b06b8940b7f549c92bf6cda337793182c7ba18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9de12acbdd586bf935463037c0039b2e7a2e4c08bf93ceaf15ac80956cae01`

```dockerfile
```

-	Layers:
	-	`sha256:fbaae4a5a3b46d4157e7e670fecca7186312bafaaa94a4400a2c2dfcf4352c5a`  
		Last Modified: Mon, 29 Sep 2025 20:38:22 GMT  
		Size: 5.2 MB (5191563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2eed0f24cc5c78814ff8b767ab3b4d402559e9d1c203447ab05a3e9cf65c4b`  
		Last Modified: Mon, 29 Sep 2025 20:38:23 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5cf4f15108e51f4f8ca409956b639b469b5ae18af2533bb9fc2dbb2d101ec26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231760786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669fd8c106c442c13da998455803d8b14dbe8437c353421ff5ca94e566d25ecd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 10:56:18 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.2.tar.gz.asc crate-6.0.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.2.tar.gz.asc     && tar -xf crate-6.0.2.tar.gz -C /crate --strip-components=1     && rm crate-6.0.2.tar.gz # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 10:56:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 24 Sep 2025 10:56:18 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
VOLUME [/data]
# Wed, 24 Sep 2025 10:56:18 GMT
WORKDIR /data
# Wed, 24 Sep 2025 10:56:18 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 24 Sep 2025 10:56:18 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-09-24T10:56:18.920121 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.2
# Wed, 24 Sep 2025 10:56:18 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:56:18 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c450c72ed5a6b4a0ddb679ef873a96251a9fd5f81957b7c38fe27bfb2cf9a0fc`  
		Last Modified: Mon, 29 Sep 2025 17:42:15 GMT  
		Size: 14.6 MB (14585565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377acd978ee0ae51e845839c3b7b9bc14f92836e75e7c7f224252fb9c9899bb`  
		Last Modified: Mon, 29 Sep 2025 21:05:55 GMT  
		Size: 149.7 MB (149711700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6e7ecc3cd5a02578c9dffcc41ae6466bffc695644612c9da5a7a4ee1e8f284`  
		Last Modified: Mon, 29 Sep 2025 17:42:13 GMT  
		Size: 1.9 MB (1943639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7408a0ab0bf2c9005cc7f595084b3d53b23870ad45fb3d4a4ae207937bb41459`  
		Last Modified: Mon, 29 Sep 2025 17:42:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0be392029e486f982d41e22e02c16d0598281bc74c1eefeebd15dae82f2ff4`  
		Last Modified: Mon, 29 Sep 2025 17:42:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25a04e7e3c12b5a592065df106a500db98a40e485abf6833f46611ad37b2d93`  
		Last Modified: Mon, 29 Sep 2025 17:42:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b803b890ab757df2a916a728268db7173ad3ed10a9022d894ac5a54050de10a8`  
		Last Modified: Mon, 29 Sep 2025 17:42:15 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:3b458badeffc4fb02e6886502c1f8389864d6b90558b8b7c0dc6f035b0e39510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b2eabde8cd2ecd4103b6d9d8049ffb7473ea1baeca464e0c5653f53fdc2a1a`

```dockerfile
```

-	Layers:
	-	`sha256:98beaff8e3d343d14fde339e6d7a5a029b6403b1d8f4d9bcc63691df48d5ee4e`  
		Last Modified: Mon, 29 Sep 2025 20:38:28 GMT  
		Size: 5.2 MB (5189482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdad26b12ba8bb5d1a2efdfedd1dfc8ff73ced3eee0a4aadbceddb49232465e8`  
		Last Modified: Mon, 29 Sep 2025 20:38:30 GMT  
		Size: 23.3 KB (23318 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.3`

**does not exist** (yet?)

## `crate:latest`

```console
$ docker pull crate@sha256:40a21da22a3e8e9fc1b94fe99f748fd5c4d56bb47314d1ff0377863857853294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:c4b28997e05792969ff60da2f3f0bb9ba08affee12e97ce92f37fc7c975d55f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232532764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f8ba5cdd4a48274f96c904452e16afeceae5123547393abe9b549364943282`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 10:56:18 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.2.tar.gz.asc crate-6.0.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.2.tar.gz.asc     && tar -xf crate-6.0.2.tar.gz -C /crate --strip-components=1     && rm crate-6.0.2.tar.gz # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 10:56:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 24 Sep 2025 10:56:18 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
VOLUME [/data]
# Wed, 24 Sep 2025 10:56:18 GMT
WORKDIR /data
# Wed, 24 Sep 2025 10:56:18 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 24 Sep 2025 10:56:18 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-09-24T10:56:18.920121 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.2
# Wed, 24 Sep 2025 10:56:18 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:56:18 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b7bb613a9da8b3b7ba3f96955aefac5f2770fa2911e95537bd89839c9e8752`  
		Last Modified: Mon, 29 Sep 2025 17:41:14 GMT  
		Size: 14.5 MB (14534475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a64eaaab2fcb00da0542899a32188f3d9d9bec83d4b505b24aff039a5819a3`  
		Last Modified: Mon, 29 Sep 2025 20:39:21 GMT  
		Size: 149.0 MB (149023730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5758847a400e037beb7f825fa5c450ebac7902fd329dc018ac18155dd65403d`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 1.9 MB (1943627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ede8f6eb8e27840852ea10ab10ada37cc2f0064604d98438a97ba8e23d2cb89`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558f96047b5a4ead90c5ea3f94c3d328084ea90057ff4aac20e6232bcc1b19a1`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03b3bbae92ce36eaf4c7e8926a939278a835e4622e5b4bda631f45c3c6a3020`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9667d72456f79b70e65f77fb5ddd4efca8b7c5ec7652eb64583dadabcf9c128`  
		Last Modified: Mon, 29 Sep 2025 17:41:13 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:1727e28c728f7f77bac28a93a2b06b8940b7f549c92bf6cda337793182c7ba18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9de12acbdd586bf935463037c0039b2e7a2e4c08bf93ceaf15ac80956cae01`

```dockerfile
```

-	Layers:
	-	`sha256:fbaae4a5a3b46d4157e7e670fecca7186312bafaaa94a4400a2c2dfcf4352c5a`  
		Last Modified: Mon, 29 Sep 2025 20:38:22 GMT  
		Size: 5.2 MB (5191563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2eed0f24cc5c78814ff8b767ab3b4d402559e9d1c203447ab05a3e9cf65c4b`  
		Last Modified: Mon, 29 Sep 2025 20:38:23 GMT  
		Size: 23.2 KB (23183 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5cf4f15108e51f4f8ca409956b639b469b5ae18af2533bb9fc2dbb2d101ec26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231760786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669fd8c106c442c13da998455803d8b14dbe8437c353421ff5ca94e566d25ecd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 09 Sep 2025 10:40:59 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 09 Sep 2025 10:40:59 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 10:56:18 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.2.tar.gz.asc crate-6.0.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.2.tar.gz.asc     && tar -xf crate-6.0.2.tar.gz -C /crate --strip-components=1     && rm crate-6.0.2.tar.gz # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 10:56:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 24 Sep 2025 10:56:18 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
VOLUME [/data]
# Wed, 24 Sep 2025 10:56:18 GMT
WORKDIR /data
# Wed, 24 Sep 2025 10:56:18 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Wed, 24 Sep 2025 10:56:18 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-09-24T10:56:18.920121 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.2
# Wed, 24 Sep 2025 10:56:18 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:56:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:56:18 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c450c72ed5a6b4a0ddb679ef873a96251a9fd5f81957b7c38fe27bfb2cf9a0fc`  
		Last Modified: Mon, 29 Sep 2025 17:42:15 GMT  
		Size: 14.6 MB (14585565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377acd978ee0ae51e845839c3b7b9bc14f92836e75e7c7f224252fb9c9899bb`  
		Last Modified: Mon, 29 Sep 2025 21:05:55 GMT  
		Size: 149.7 MB (149711700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6e7ecc3cd5a02578c9dffcc41ae6466bffc695644612c9da5a7a4ee1e8f284`  
		Last Modified: Mon, 29 Sep 2025 17:42:13 GMT  
		Size: 1.9 MB (1943639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7408a0ab0bf2c9005cc7f595084b3d53b23870ad45fb3d4a4ae207937bb41459`  
		Last Modified: Mon, 29 Sep 2025 17:42:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0be392029e486f982d41e22e02c16d0598281bc74c1eefeebd15dae82f2ff4`  
		Last Modified: Mon, 29 Sep 2025 17:42:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25a04e7e3c12b5a592065df106a500db98a40e485abf6833f46611ad37b2d93`  
		Last Modified: Mon, 29 Sep 2025 17:42:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b803b890ab757df2a916a728268db7173ad3ed10a9022d894ac5a54050de10a8`  
		Last Modified: Mon, 29 Sep 2025 17:42:15 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:3b458badeffc4fb02e6886502c1f8389864d6b90558b8b7c0dc6f035b0e39510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b2eabde8cd2ecd4103b6d9d8049ffb7473ea1baeca464e0c5653f53fdc2a1a`

```dockerfile
```

-	Layers:
	-	`sha256:98beaff8e3d343d14fde339e6d7a5a029b6403b1d8f4d9bcc63691df48d5ee4e`  
		Last Modified: Mon, 29 Sep 2025 20:38:28 GMT  
		Size: 5.2 MB (5189482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdad26b12ba8bb5d1a2efdfedd1dfc8ff73ced3eee0a4aadbceddb49232465e8`  
		Last Modified: Mon, 29 Sep 2025 20:38:30 GMT  
		Size: 23.3 KB (23318 bytes)  
		MIME: application/vnd.in-toto+json
