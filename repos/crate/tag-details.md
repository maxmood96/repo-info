<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.8`](#crate58)
-	[`crate:5.8.5`](#crate585)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.3`](#crate593)
-	[`crate:latest`](#cratelatest)

## `crate:5.8`

```console
$ docker pull crate@sha256:640d5a01e58b1f8b39312a83d2871ebcaf9a031165de4d5a3bddce574f381804
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.8` - linux; amd64

```console
$ docker pull crate@sha256:8f78a3d0b4fbe12fcef1dc61dcd51c859591c291032487f01ff0d33ca55d9246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212191570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8890d0038b570b29ff7603b2554386c90a1cc8a0cce46257a644118501fe9154`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 13:54:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.5.tar.gz.asc crate-5.8.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.5.tar.gz.asc     && tar -xf crate-5.8.5.tar.gz -C /crate --strip-components=1     && rm crate-5.8.5.tar.gz # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 13:54:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Oct 2024 13:54:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
VOLUME [/data]
# Mon, 28 Oct 2024 13:54:06 GMT
WORKDIR /data
# Mon, 28 Oct 2024 13:54:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-28T13:54:06.325139 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.5
# Mon, 28 Oct 2024 13:54:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e909ff336b3a8b3f79491d0059d6eb8e9c867221cc1d02001486a1d90dc803be`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 69.2 MB (69206030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71167f1f97b422593ddca341f29e7291ae5b6a44f17ecb1dd50a99100cffcef`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 11.1 MB (11073790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8576a5d11848041ba4dff6de1d1f804fd8909668446260b536de1d7be2dc5977`  
		Last Modified: Thu, 31 Oct 2024 21:59:27 GMT  
		Size: 130.0 MB (129966243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57b6b326bb4eddf6470462938b943b8b867e4ee2dfe17fa24a88feacab6f6e`  
		Last Modified: Thu, 31 Oct 2024 21:59:25 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a91f60e87e72551b41174b6db906c186e518aca34717e21e676ab3338bb2f8f`  
		Last Modified: Thu, 31 Oct 2024 21:59:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0d8dc4394ef0ca87d7a68a200b3b694ae91bdf9d85e90723542dd45ab2ed3e`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a523e45210d032c21ab69df588eade81050327790fd38e800991ba813a21e5ca`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29aa774588588e8c7b63747ae9fb391c71e428ff815938b741c73c4c5ccd43f5`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:9fe36fb444e69c9f175bf4d925372334ebda1621fb39e2d0df393fcac98f9052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691ba7297746cc54789e84f0d384a0f083a3797679549587669cc6a3015a1fd6`

```dockerfile
```

-	Layers:
	-	`sha256:1610be6dd1597cbae53a409bbbae05ed9bb2072e8c5aa047b2c523532d49cfa4`  
		Last Modified: Thu, 31 Oct 2024 21:59:25 GMT  
		Size: 5.2 MB (5205994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44aad78d7e26b4c974e61feb03dd6ec48da4cbd6b7e5cd287651544be7fe57cc`  
		Last Modified: Thu, 31 Oct 2024 21:59:25 GMT  
		Size: 22.8 KB (22826 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7ab820a863010a3b1b485b82c3b1de5879d1cb18e6eafe67a353b014cd2aba05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210588223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1aa03fcb0b9b5585aba176698bf8d0a617c9f28639b31b7e67e37b22aab4e44`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 13:54:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.5.tar.gz.asc crate-5.8.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.5.tar.gz.asc     && tar -xf crate-5.8.5.tar.gz -C /crate --strip-components=1     && rm crate-5.8.5.tar.gz # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 13:54:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Oct 2024 13:54:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
VOLUME [/data]
# Mon, 28 Oct 2024 13:54:06 GMT
WORKDIR /data
# Mon, 28 Oct 2024 13:54:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-28T13:54:06.325139 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.5
# Mon, 28 Oct 2024 13:54:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:022ce932f83232e8eff99d0bbc45d209d6a94bc90cc2b1efcc609bdb66eb424f`  
		Last Modified: Tue, 24 Sep 2024 01:02:43 GMT  
		Size: 68.2 MB (68171751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930614a3bc6cc1bcd2866b8c0f47e3c9050b7170831bc5d28b81be6a30006395`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 11.1 MB (11059002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b3ccffc7443312d0bbf7c5d4aa199408a9ddf130e74d819f1481e4a0a3f4c`  
		Last Modified: Thu, 31 Oct 2024 22:00:53 GMT  
		Size: 129.4 MB (129411961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b05b2c7f72a06f107850399db25b6d4d5aedbdc199b02a81abf4b294bc874e`  
		Last Modified: Thu, 31 Oct 2024 22:00:49 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657a6097f8dc33cb669eb3a7b0b936807adedd70e8b470f2f94acac456e899a6`  
		Last Modified: Thu, 31 Oct 2024 22:00:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc60521b8152e45356b6ca6306f79378219fd121124de6dfee29b9243b66602`  
		Last Modified: Thu, 31 Oct 2024 22:00:49 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b9bf9b7b85584e93390f0f0975f12283233cd77f5f2fd545f9c1d9696d4cb8`  
		Last Modified: Thu, 31 Oct 2024 22:00:50 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d829be57bc713b7be525427c63eb32629724164d61564c3cd7bdd36cbbe11c`  
		Last Modified: Thu, 31 Oct 2024 22:00:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8` - unknown; unknown

```console
$ docker pull crate@sha256:617adf0c665634ce51d9d9a0e896d8c7d8ca052e2ff26d66f3a44ea2459a5ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5226247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a86c7950de2fba050d1ef71d202fc3e85235a1f78c4c14cd7ab054907cdb993`

```dockerfile
```

-	Layers:
	-	`sha256:047f121cd3acd21fdd6355b398cca35b19b627abbd4b397f019a15b5942aa9ec`  
		Last Modified: Thu, 31 Oct 2024 22:00:50 GMT  
		Size: 5.2 MB (5203296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4d06a62279e146c7c7d9d29d5e16bdf30f9c7e05265948524cb9dcd29df9b9`  
		Last Modified: Thu, 31 Oct 2024 22:00:49 GMT  
		Size: 23.0 KB (22951 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.8.5`

```console
$ docker pull crate@sha256:640d5a01e58b1f8b39312a83d2871ebcaf9a031165de4d5a3bddce574f381804
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.8.5` - linux; amd64

```console
$ docker pull crate@sha256:8f78a3d0b4fbe12fcef1dc61dcd51c859591c291032487f01ff0d33ca55d9246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212191570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8890d0038b570b29ff7603b2554386c90a1cc8a0cce46257a644118501fe9154`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 13:54:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.5.tar.gz.asc crate-5.8.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.5.tar.gz.asc     && tar -xf crate-5.8.5.tar.gz -C /crate --strip-components=1     && rm crate-5.8.5.tar.gz # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 13:54:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Oct 2024 13:54:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
VOLUME [/data]
# Mon, 28 Oct 2024 13:54:06 GMT
WORKDIR /data
# Mon, 28 Oct 2024 13:54:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-28T13:54:06.325139 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.5
# Mon, 28 Oct 2024 13:54:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e909ff336b3a8b3f79491d0059d6eb8e9c867221cc1d02001486a1d90dc803be`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 69.2 MB (69206030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71167f1f97b422593ddca341f29e7291ae5b6a44f17ecb1dd50a99100cffcef`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 11.1 MB (11073790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8576a5d11848041ba4dff6de1d1f804fd8909668446260b536de1d7be2dc5977`  
		Last Modified: Thu, 31 Oct 2024 21:59:27 GMT  
		Size: 130.0 MB (129966243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57b6b326bb4eddf6470462938b943b8b867e4ee2dfe17fa24a88feacab6f6e`  
		Last Modified: Thu, 31 Oct 2024 21:59:25 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a91f60e87e72551b41174b6db906c186e518aca34717e21e676ab3338bb2f8f`  
		Last Modified: Thu, 31 Oct 2024 21:59:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0d8dc4394ef0ca87d7a68a200b3b694ae91bdf9d85e90723542dd45ab2ed3e`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a523e45210d032c21ab69df588eade81050327790fd38e800991ba813a21e5ca`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29aa774588588e8c7b63747ae9fb391c71e428ff815938b741c73c4c5ccd43f5`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8.5` - unknown; unknown

```console
$ docker pull crate@sha256:9fe36fb444e69c9f175bf4d925372334ebda1621fb39e2d0df393fcac98f9052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691ba7297746cc54789e84f0d384a0f083a3797679549587669cc6a3015a1fd6`

```dockerfile
```

-	Layers:
	-	`sha256:1610be6dd1597cbae53a409bbbae05ed9bb2072e8c5aa047b2c523532d49cfa4`  
		Last Modified: Thu, 31 Oct 2024 21:59:25 GMT  
		Size: 5.2 MB (5205994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44aad78d7e26b4c974e61feb03dd6ec48da4cbd6b7e5cd287651544be7fe57cc`  
		Last Modified: Thu, 31 Oct 2024 21:59:25 GMT  
		Size: 22.8 KB (22826 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.8.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7ab820a863010a3b1b485b82c3b1de5879d1cb18e6eafe67a353b014cd2aba05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210588223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1aa03fcb0b9b5585aba176698bf8d0a617c9f28639b31b7e67e37b22aab4e44`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 13:54:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.8.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.8.5.tar.gz.asc crate-5.8.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.8.5.tar.gz.asc     && tar -xf crate-5.8.5.tar.gz -C /crate --strip-components=1     && rm crate-5.8.5.tar.gz # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 13:54:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Oct 2024 13:54:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
VOLUME [/data]
# Mon, 28 Oct 2024 13:54:06 GMT
WORKDIR /data
# Mon, 28 Oct 2024 13:54:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-28T13:54:06.325139 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.8.5
# Mon, 28 Oct 2024 13:54:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 13:54:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 13:54:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:022ce932f83232e8eff99d0bbc45d209d6a94bc90cc2b1efcc609bdb66eb424f`  
		Last Modified: Tue, 24 Sep 2024 01:02:43 GMT  
		Size: 68.2 MB (68171751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930614a3bc6cc1bcd2866b8c0f47e3c9050b7170831bc5d28b81be6a30006395`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 11.1 MB (11059002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b3ccffc7443312d0bbf7c5d4aa199408a9ddf130e74d819f1481e4a0a3f4c`  
		Last Modified: Thu, 31 Oct 2024 22:00:53 GMT  
		Size: 129.4 MB (129411961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b05b2c7f72a06f107850399db25b6d4d5aedbdc199b02a81abf4b294bc874e`  
		Last Modified: Thu, 31 Oct 2024 22:00:49 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657a6097f8dc33cb669eb3a7b0b936807adedd70e8b470f2f94acac456e899a6`  
		Last Modified: Thu, 31 Oct 2024 22:00:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc60521b8152e45356b6ca6306f79378219fd121124de6dfee29b9243b66602`  
		Last Modified: Thu, 31 Oct 2024 22:00:49 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b9bf9b7b85584e93390f0f0975f12283233cd77f5f2fd545f9c1d9696d4cb8`  
		Last Modified: Thu, 31 Oct 2024 22:00:50 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d829be57bc713b7be525427c63eb32629724164d61564c3cd7bdd36cbbe11c`  
		Last Modified: Thu, 31 Oct 2024 22:00:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.8.5` - unknown; unknown

```console
$ docker pull crate@sha256:617adf0c665634ce51d9d9a0e896d8c7d8ca052e2ff26d66f3a44ea2459a5ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5226247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a86c7950de2fba050d1ef71d202fc3e85235a1f78c4c14cd7ab054907cdb993`

```dockerfile
```

-	Layers:
	-	`sha256:047f121cd3acd21fdd6355b398cca35b19b627abbd4b397f019a15b5942aa9ec`  
		Last Modified: Thu, 31 Oct 2024 22:00:50 GMT  
		Size: 5.2 MB (5203296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4d06a62279e146c7c7d9d29d5e16bdf30f9c7e05265948524cb9dcd29df9b9`  
		Last Modified: Thu, 31 Oct 2024 22:00:49 GMT  
		Size: 23.0 KB (22951 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:1aaa49762826e76faf034be1c9f826beab9c5d5a51b8259a8b50bfb9553ffbce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:98834cee749fe0d4dd67238e7a8c65d28e1982cc53307dabc350fccd544d6750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232636472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ebc19b2f903d080c53f545e3d7fa39b99b753e4bf5c1ec3f62673c65df27cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 12:05:43 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.3.tar.gz.asc crate-5.9.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.3.tar.gz.asc     && tar -xf crate-5.9.3.tar.gz -C /crate --strip-components=1     && rm crate-5.9.3.tar.gz # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 12:05:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 14 Nov 2024 12:05:43 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
VOLUME [/data]
# Thu, 14 Nov 2024 12:05:43 GMT
WORKDIR /data
# Thu, 14 Nov 2024 12:05:43 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-14T12:05:43.779769 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.3
# Thu, 14 Nov 2024 12:05:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 12:05:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e909ff336b3a8b3f79491d0059d6eb8e9c867221cc1d02001486a1d90dc803be`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 69.2 MB (69206030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc2bde4c0cbc399ae603e4c19348d42f0e41b13dec5986280400625bb600e3f`  
		Last Modified: Mon, 18 Nov 2024 19:06:00 GMT  
		Size: 14.3 MB (14274815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75730ee1c5bd48eb8f55936c364e09ed4f61331942a5c50fdd70579ed05911`  
		Last Modified: Mon, 18 Nov 2024 19:06:03 GMT  
		Size: 147.2 MB (147210115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2ec39676e044911d82a6746e52084d894d1c342fa4d6f7f8c6b5699e8882dc`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6220b89af5687ccb25142714753112809e918a567ae9c4f8318875864d40a417`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c2135326a4da33cd828ceb44f126fef988898141edffae0957cae93fcfae75`  
		Last Modified: Mon, 18 Nov 2024 19:06:00 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6505d2952f2f1ceb5ef8af72a79e325db5b197aa93869267dd30310459b448fe`  
		Last Modified: Mon, 18 Nov 2024 19:06:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c574d540e848f5d5178babeea4ef473d1b760f76e7bb2698915290915226fc`  
		Last Modified: Mon, 18 Nov 2024 19:06:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:160b411486c46042ebb32e927f3b85212255753347cd2a2ccabe5d4342afcf18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d606abb101812876a23e20edcf5c0db68ac2aca093b9073ce5000b94d5862ba0`

```dockerfile
```

-	Layers:
	-	`sha256:06d2904b3ca5cdc22f43867a074f7c06b16744dccb8ae929e5925a02e4fff52c`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 5.2 MB (5222386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98714958e56dc641208dfac532f10148cc4cad7f5cc52744f665b6b0f3ef31cb`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:89e2a891861d637e671e11a671f00c878728bd1be02fb6b690142ff739f33bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232805269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e12bf03e721738f71a6d7943854925fa73fc36a65c3529e98eb7b002cd3956`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 12:05:43 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.3.tar.gz.asc crate-5.9.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.3.tar.gz.asc     && tar -xf crate-5.9.3.tar.gz -C /crate --strip-components=1     && rm crate-5.9.3.tar.gz # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 12:05:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 14 Nov 2024 12:05:43 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
VOLUME [/data]
# Thu, 14 Nov 2024 12:05:43 GMT
WORKDIR /data
# Thu, 14 Nov 2024 12:05:43 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-14T12:05:43.779769 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.3
# Thu, 14 Nov 2024 12:05:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 12:05:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:022ce932f83232e8eff99d0bbc45d209d6a94bc90cc2b1efcc609bdb66eb424f`  
		Last Modified: Tue, 24 Sep 2024 01:02:43 GMT  
		Size: 68.2 MB (68171751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1f5f91638aad0e425195c880bb4fde88b12d39a0dbaaf1c7bdaf7a5fa85323`  
		Last Modified: Mon, 18 Nov 2024 19:07:10 GMT  
		Size: 14.3 MB (14315352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefdcfeb0f94f1021437cbb347550f561452ae49fb27274962dc162cc9b24257`  
		Last Modified: Mon, 18 Nov 2024 19:07:13 GMT  
		Size: 148.4 MB (148372652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc800e256b6987dc929b6b82185dd5faf43ddb2efa73c42278a614177841d5e9`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac785e60799834f1bcea2cba5bb5715fd7d94cd6b0a92b6a51eefd6490e10f41`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebe5d275b424a427ed1c98460e3808eab7a54acce38b9594229f5fa4bfd01ab`  
		Last Modified: Mon, 18 Nov 2024 19:07:10 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7961ad197acacae96a191b22c478d5eecdaa9be47ae31fa5608abdabc3659d`  
		Last Modified: Mon, 18 Nov 2024 19:07:11 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6adbd880d1a4b33d6c77dc7d0584e3ddd122db1e583c17d5c3a199338ee750`  
		Last Modified: Mon, 18 Nov 2024 19:07:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:25a0c3107ac7c6c791d522153cb7551decf4c8f3fc309b0e465d6229c17e98a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df60f5c769fa8810944de35cfd2511b7c6818d26527658a3f78e7508fb0fcd43`

```dockerfile
```

-	Layers:
	-	`sha256:f1e700e35f3d87b074132ffaf1bc97940eecd79c2390036cdb6fb2a0e6b20d9d`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 5.2 MB (5219090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0522b8953a54333a7f225a0e5ab24f6825c295bc64230a96b35fc12aeda2b374`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 23.3 KB (23258 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.3`

```console
$ docker pull crate@sha256:1aaa49762826e76faf034be1c9f826beab9c5d5a51b8259a8b50bfb9553ffbce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.3` - linux; amd64

```console
$ docker pull crate@sha256:98834cee749fe0d4dd67238e7a8c65d28e1982cc53307dabc350fccd544d6750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232636472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ebc19b2f903d080c53f545e3d7fa39b99b753e4bf5c1ec3f62673c65df27cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 12:05:43 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.3.tar.gz.asc crate-5.9.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.3.tar.gz.asc     && tar -xf crate-5.9.3.tar.gz -C /crate --strip-components=1     && rm crate-5.9.3.tar.gz # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 12:05:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 14 Nov 2024 12:05:43 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
VOLUME [/data]
# Thu, 14 Nov 2024 12:05:43 GMT
WORKDIR /data
# Thu, 14 Nov 2024 12:05:43 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-14T12:05:43.779769 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.3
# Thu, 14 Nov 2024 12:05:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 12:05:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e909ff336b3a8b3f79491d0059d6eb8e9c867221cc1d02001486a1d90dc803be`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 69.2 MB (69206030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc2bde4c0cbc399ae603e4c19348d42f0e41b13dec5986280400625bb600e3f`  
		Last Modified: Mon, 18 Nov 2024 19:06:00 GMT  
		Size: 14.3 MB (14274815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75730ee1c5bd48eb8f55936c364e09ed4f61331942a5c50fdd70579ed05911`  
		Last Modified: Mon, 18 Nov 2024 19:06:03 GMT  
		Size: 147.2 MB (147210115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2ec39676e044911d82a6746e52084d894d1c342fa4d6f7f8c6b5699e8882dc`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6220b89af5687ccb25142714753112809e918a567ae9c4f8318875864d40a417`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c2135326a4da33cd828ceb44f126fef988898141edffae0957cae93fcfae75`  
		Last Modified: Mon, 18 Nov 2024 19:06:00 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6505d2952f2f1ceb5ef8af72a79e325db5b197aa93869267dd30310459b448fe`  
		Last Modified: Mon, 18 Nov 2024 19:06:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c574d540e848f5d5178babeea4ef473d1b760f76e7bb2698915290915226fc`  
		Last Modified: Mon, 18 Nov 2024 19:06:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.3` - unknown; unknown

```console
$ docker pull crate@sha256:160b411486c46042ebb32e927f3b85212255753347cd2a2ccabe5d4342afcf18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d606abb101812876a23e20edcf5c0db68ac2aca093b9073ce5000b94d5862ba0`

```dockerfile
```

-	Layers:
	-	`sha256:06d2904b3ca5cdc22f43867a074f7c06b16744dccb8ae929e5925a02e4fff52c`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 5.2 MB (5222386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98714958e56dc641208dfac532f10148cc4cad7f5cc52744f665b6b0f3ef31cb`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:89e2a891861d637e671e11a671f00c878728bd1be02fb6b690142ff739f33bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232805269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e12bf03e721738f71a6d7943854925fa73fc36a65c3529e98eb7b002cd3956`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 12:05:43 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.3.tar.gz.asc crate-5.9.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.3.tar.gz.asc     && tar -xf crate-5.9.3.tar.gz -C /crate --strip-components=1     && rm crate-5.9.3.tar.gz # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 12:05:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 14 Nov 2024 12:05:43 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
VOLUME [/data]
# Thu, 14 Nov 2024 12:05:43 GMT
WORKDIR /data
# Thu, 14 Nov 2024 12:05:43 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-14T12:05:43.779769 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.3
# Thu, 14 Nov 2024 12:05:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 12:05:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:022ce932f83232e8eff99d0bbc45d209d6a94bc90cc2b1efcc609bdb66eb424f`  
		Last Modified: Tue, 24 Sep 2024 01:02:43 GMT  
		Size: 68.2 MB (68171751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1f5f91638aad0e425195c880bb4fde88b12d39a0dbaaf1c7bdaf7a5fa85323`  
		Last Modified: Mon, 18 Nov 2024 19:07:10 GMT  
		Size: 14.3 MB (14315352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefdcfeb0f94f1021437cbb347550f561452ae49fb27274962dc162cc9b24257`  
		Last Modified: Mon, 18 Nov 2024 19:07:13 GMT  
		Size: 148.4 MB (148372652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc800e256b6987dc929b6b82185dd5faf43ddb2efa73c42278a614177841d5e9`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac785e60799834f1bcea2cba5bb5715fd7d94cd6b0a92b6a51eefd6490e10f41`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebe5d275b424a427ed1c98460e3808eab7a54acce38b9594229f5fa4bfd01ab`  
		Last Modified: Mon, 18 Nov 2024 19:07:10 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7961ad197acacae96a191b22c478d5eecdaa9be47ae31fa5608abdabc3659d`  
		Last Modified: Mon, 18 Nov 2024 19:07:11 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6adbd880d1a4b33d6c77dc7d0584e3ddd122db1e583c17d5c3a199338ee750`  
		Last Modified: Mon, 18 Nov 2024 19:07:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.3` - unknown; unknown

```console
$ docker pull crate@sha256:25a0c3107ac7c6c791d522153cb7551decf4c8f3fc309b0e465d6229c17e98a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df60f5c769fa8810944de35cfd2511b7c6818d26527658a3f78e7508fb0fcd43`

```dockerfile
```

-	Layers:
	-	`sha256:f1e700e35f3d87b074132ffaf1bc97940eecd79c2390036cdb6fb2a0e6b20d9d`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 5.2 MB (5219090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0522b8953a54333a7f225a0e5ab24f6825c295bc64230a96b35fc12aeda2b374`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 23.3 KB (23258 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:1aaa49762826e76faf034be1c9f826beab9c5d5a51b8259a8b50bfb9553ffbce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:98834cee749fe0d4dd67238e7a8c65d28e1982cc53307dabc350fccd544d6750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232636472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ebc19b2f903d080c53f545e3d7fa39b99b753e4bf5c1ec3f62673c65df27cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 12:05:43 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.3.tar.gz.asc crate-5.9.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.3.tar.gz.asc     && tar -xf crate-5.9.3.tar.gz -C /crate --strip-components=1     && rm crate-5.9.3.tar.gz # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 12:05:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 14 Nov 2024 12:05:43 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
VOLUME [/data]
# Thu, 14 Nov 2024 12:05:43 GMT
WORKDIR /data
# Thu, 14 Nov 2024 12:05:43 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-14T12:05:43.779769 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.3
# Thu, 14 Nov 2024 12:05:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 12:05:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e909ff336b3a8b3f79491d0059d6eb8e9c867221cc1d02001486a1d90dc803be`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 69.2 MB (69206030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc2bde4c0cbc399ae603e4c19348d42f0e41b13dec5986280400625bb600e3f`  
		Last Modified: Mon, 18 Nov 2024 19:06:00 GMT  
		Size: 14.3 MB (14274815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75730ee1c5bd48eb8f55936c364e09ed4f61331942a5c50fdd70579ed05911`  
		Last Modified: Mon, 18 Nov 2024 19:06:03 GMT  
		Size: 147.2 MB (147210115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2ec39676e044911d82a6746e52084d894d1c342fa4d6f7f8c6b5699e8882dc`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6220b89af5687ccb25142714753112809e918a567ae9c4f8318875864d40a417`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c2135326a4da33cd828ceb44f126fef988898141edffae0957cae93fcfae75`  
		Last Modified: Mon, 18 Nov 2024 19:06:00 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6505d2952f2f1ceb5ef8af72a79e325db5b197aa93869267dd30310459b448fe`  
		Last Modified: Mon, 18 Nov 2024 19:06:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c574d540e848f5d5178babeea4ef473d1b760f76e7bb2698915290915226fc`  
		Last Modified: Mon, 18 Nov 2024 19:06:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:160b411486c46042ebb32e927f3b85212255753347cd2a2ccabe5d4342afcf18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d606abb101812876a23e20edcf5c0db68ac2aca093b9073ce5000b94d5862ba0`

```dockerfile
```

-	Layers:
	-	`sha256:06d2904b3ca5cdc22f43867a074f7c06b16744dccb8ae929e5925a02e4fff52c`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 5.2 MB (5222386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98714958e56dc641208dfac532f10148cc4cad7f5cc52744f665b6b0f3ef31cb`  
		Last Modified: Mon, 18 Nov 2024 19:05:59 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:89e2a891861d637e671e11a671f00c878728bd1be02fb6b690142ff739f33bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232805269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e12bf03e721738f71a6d7943854925fa73fc36a65c3529e98eb7b002cd3956`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 12:05:43 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.3.tar.gz.asc crate-5.9.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.3.tar.gz.asc     && tar -xf crate-5.9.3.tar.gz -C /crate --strip-components=1     && rm crate-5.9.3.tar.gz # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 12:05:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 14 Nov 2024 12:05:43 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
VOLUME [/data]
# Thu, 14 Nov 2024 12:05:43 GMT
WORKDIR /data
# Thu, 14 Nov 2024 12:05:43 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-11-14T12:05:43.779769 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.3
# Thu, 14 Nov 2024 12:05:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Nov 2024 12:05:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 12:05:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:022ce932f83232e8eff99d0bbc45d209d6a94bc90cc2b1efcc609bdb66eb424f`  
		Last Modified: Tue, 24 Sep 2024 01:02:43 GMT  
		Size: 68.2 MB (68171751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1f5f91638aad0e425195c880bb4fde88b12d39a0dbaaf1c7bdaf7a5fa85323`  
		Last Modified: Mon, 18 Nov 2024 19:07:10 GMT  
		Size: 14.3 MB (14315352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefdcfeb0f94f1021437cbb347550f561452ae49fb27274962dc162cc9b24257`  
		Last Modified: Mon, 18 Nov 2024 19:07:13 GMT  
		Size: 148.4 MB (148372652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc800e256b6987dc929b6b82185dd5faf43ddb2efa73c42278a614177841d5e9`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac785e60799834f1bcea2cba5bb5715fd7d94cd6b0a92b6a51eefd6490e10f41`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebe5d275b424a427ed1c98460e3808eab7a54acce38b9594229f5fa4bfd01ab`  
		Last Modified: Mon, 18 Nov 2024 19:07:10 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7961ad197acacae96a191b22c478d5eecdaa9be47ae31fa5608abdabc3659d`  
		Last Modified: Mon, 18 Nov 2024 19:07:11 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6adbd880d1a4b33d6c77dc7d0584e3ddd122db1e583c17d5c3a199338ee750`  
		Last Modified: Mon, 18 Nov 2024 19:07:11 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:25a0c3107ac7c6c791d522153cb7551decf4c8f3fc309b0e465d6229c17e98a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df60f5c769fa8810944de35cfd2511b7c6818d26527658a3f78e7508fb0fcd43`

```dockerfile
```

-	Layers:
	-	`sha256:f1e700e35f3d87b074132ffaf1bc97940eecd79c2390036cdb6fb2a0e6b20d9d`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 5.2 MB (5219090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0522b8953a54333a7f225a0e5ab24f6825c295bc64230a96b35fc12aeda2b374`  
		Last Modified: Mon, 18 Nov 2024 19:07:09 GMT  
		Size: 23.3 KB (23258 bytes)  
		MIME: application/vnd.in-toto+json
