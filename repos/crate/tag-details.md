<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.12`](#crate51012)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

## `crate:5.10.12`

```console
$ docker pull crate@sha256:cfce7e180eafa1eb57ebda20a7b3678d65fbac2bbd08ba7e5a7b0dbf553d7696
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.12` - linux; amd64

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `crate:5.10.12` - unknown; unknown

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

### `crate:5.10.12` - linux; arm64 variant v8

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `crate:5.10.12` - unknown; unknown

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

## `crate:5.9`

```console
$ docker pull crate@sha256:f76e157c87e2faf64c2a2aec835d99f498d19d913e9db89973c04940366263da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:20b4b8e0a312da518bb4a848b30bec4b613149c9131076250d61979994fafbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232518442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db8072eca1255bfa491975f8538e58317b63f9efb648755ad61592a161cff8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6034873a173ecc5b803c7e0bcd3aa2929069b487d0d35a1cecc313fb9ecf07d9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 14.5 MB (14534314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2881fbab7c44f8bd8730bc7a5258bf9bd5392df9a38a344bae0d12b59baba184`  
		Last Modified: Tue, 09 Sep 2025 21:10:18 GMT  
		Size: 149.0 MB (149009568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9995a0bdb2820e6c7631c1eb37bb323f8ea39ab8d7801fff92baca64817c5`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0116236db205c62b93b40d5bdc738761656cd981a911e10a6a1cf015cef0300`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ed4583831751086a65d172aec1d9d20e6aab77cf5920bcfc9a5a5b225b3e88`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d234b7aaa1e65f7c10bb072135e88363be03349c42aeb4ca6ead2ae362fa47`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30a8925465300e4bf20123c80723d7ff3e408f6d78b5c3c9a40d66f7c2bd601`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:f6cade60f0be48c0d9246d7414b3ea20e6844ebc370b6b8ce4112694f497aae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd8bae646d5875e727812f2aeb460b0a66055da91d96b9dd47ee08bff8311a`

```dockerfile
```

-	Layers:
	-	`sha256:a5bd7bbd74b593174bd051244a00519a345bdce9153dbf39632e493c7560da50`  
		Last Modified: Tue, 09 Sep 2025 23:38:34 GMT  
		Size: 5.2 MB (5186490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5bd97fa1ee90113bd942f0273ef5bd2044e61af676ffb2c4b2feb908e79c69`  
		Last Modified: Tue, 09 Sep 2025 23:38:35 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1f3d3eb3131c72f61dc106f72f445b1dbd1ae0d9b436fa65a869ea5cb36b471f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231757583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7929c4381435ac835f9a713cfa4204d0066560b5c09e2d4493b79f35da60f0d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a621df3cef737ec5f897bb4ce7f93176dfc2ed3d192143daa0b25f665d59875`  
		Last Modified: Tue, 09 Sep 2025 21:12:17 GMT  
		Size: 14.6 MB (14585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab91292c150cdb2300f1abcfb0881099b851c47e02021cdae60fc675eb754c7b`  
		Last Modified: Tue, 09 Sep 2025 21:12:26 GMT  
		Size: 149.7 MB (149708537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f47ce5519f7375e4c9c252ea859d1cad0f67a0848bd209cf5fe85422c6a908`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd3bcfe0b0f8320b4bb03aea983cd7b354ef366827eb2afc361501eaf0a50da`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fac8ce0957b7933cd4595886d0a44bbe476ad84e4e5e15a7a4e51f9af7f15f`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b066bdefd095d937f5226d4f023debb4f343d471754f30d890c825209a329`  
		Last Modified: Tue, 09 Sep 2025 21:12:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f5d6781ea7fc53d798962aa744939bc04cc7c3079126db853bd9261724e427`  
		Last Modified: Tue, 09 Sep 2025 21:12:11 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:9114b67622502217f2e0d846dc1b0d43b37b954054652d4ee27857d684218b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b51803f41e6cd2c493426a57c77b7971417769ce3c1aea71b1eeadf96d39b3`

```dockerfile
```

-	Layers:
	-	`sha256:0700bff935177de8e6dc1ac74d186792235f7661d62d2b12603cf8badb68e679`  
		Last Modified: Tue, 09 Sep 2025 23:38:40 GMT  
		Size: 5.2 MB (5183786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359270dd6674a0395407ee457ecc0335582c0fa1d22f0e1a288b56241fc516fe`  
		Last Modified: Tue, 09 Sep 2025 23:38:41 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:f76e157c87e2faf64c2a2aec835d99f498d19d913e9db89973c04940366263da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:20b4b8e0a312da518bb4a848b30bec4b613149c9131076250d61979994fafbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232518442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db8072eca1255bfa491975f8538e58317b63f9efb648755ad61592a161cff8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6034873a173ecc5b803c7e0bcd3aa2929069b487d0d35a1cecc313fb9ecf07d9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 14.5 MB (14534314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2881fbab7c44f8bd8730bc7a5258bf9bd5392df9a38a344bae0d12b59baba184`  
		Last Modified: Tue, 09 Sep 2025 21:10:18 GMT  
		Size: 149.0 MB (149009568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9995a0bdb2820e6c7631c1eb37bb323f8ea39ab8d7801fff92baca64817c5`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0116236db205c62b93b40d5bdc738761656cd981a911e10a6a1cf015cef0300`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ed4583831751086a65d172aec1d9d20e6aab77cf5920bcfc9a5a5b225b3e88`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d234b7aaa1e65f7c10bb072135e88363be03349c42aeb4ca6ead2ae362fa47`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30a8925465300e4bf20123c80723d7ff3e408f6d78b5c3c9a40d66f7c2bd601`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:f6cade60f0be48c0d9246d7414b3ea20e6844ebc370b6b8ce4112694f497aae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd8bae646d5875e727812f2aeb460b0a66055da91d96b9dd47ee08bff8311a`

```dockerfile
```

-	Layers:
	-	`sha256:a5bd7bbd74b593174bd051244a00519a345bdce9153dbf39632e493c7560da50`  
		Last Modified: Tue, 09 Sep 2025 23:38:34 GMT  
		Size: 5.2 MB (5186490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5bd97fa1ee90113bd942f0273ef5bd2044e61af676ffb2c4b2feb908e79c69`  
		Last Modified: Tue, 09 Sep 2025 23:38:35 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1f3d3eb3131c72f61dc106f72f445b1dbd1ae0d9b436fa65a869ea5cb36b471f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231757583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7929c4381435ac835f9a713cfa4204d0066560b5c09e2d4493b79f35da60f0d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a621df3cef737ec5f897bb4ce7f93176dfc2ed3d192143daa0b25f665d59875`  
		Last Modified: Tue, 09 Sep 2025 21:12:17 GMT  
		Size: 14.6 MB (14585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab91292c150cdb2300f1abcfb0881099b851c47e02021cdae60fc675eb754c7b`  
		Last Modified: Tue, 09 Sep 2025 21:12:26 GMT  
		Size: 149.7 MB (149708537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f47ce5519f7375e4c9c252ea859d1cad0f67a0848bd209cf5fe85422c6a908`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd3bcfe0b0f8320b4bb03aea983cd7b354ef366827eb2afc361501eaf0a50da`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fac8ce0957b7933cd4595886d0a44bbe476ad84e4e5e15a7a4e51f9af7f15f`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b066bdefd095d937f5226d4f023debb4f343d471754f30d890c825209a329`  
		Last Modified: Tue, 09 Sep 2025 21:12:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f5d6781ea7fc53d798962aa744939bc04cc7c3079126db853bd9261724e427`  
		Last Modified: Tue, 09 Sep 2025 21:12:11 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:9114b67622502217f2e0d846dc1b0d43b37b954054652d4ee27857d684218b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b51803f41e6cd2c493426a57c77b7971417769ce3c1aea71b1eeadf96d39b3`

```dockerfile
```

-	Layers:
	-	`sha256:0700bff935177de8e6dc1ac74d186792235f7661d62d2b12603cf8badb68e679`  
		Last Modified: Tue, 09 Sep 2025 23:38:40 GMT  
		Size: 5.2 MB (5183786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359270dd6674a0395407ee457ecc0335582c0fa1d22f0e1a288b56241fc516fe`  
		Last Modified: Tue, 09 Sep 2025 23:38:41 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:cfce7e180eafa1eb57ebda20a7b3678d65fbac2bbd08ba7e5a7b0dbf553d7696
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `crate:latest` - unknown; unknown

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

### `crate:latest` - linux; arm64 variant v8

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `crate:latest` - unknown; unknown

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
