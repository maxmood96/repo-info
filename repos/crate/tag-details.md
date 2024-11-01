<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.8`](#crate58)
-	[`crate:5.8.5`](#crate585)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.2`](#crate592)
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
$ docker pull crate@sha256:873233efad8e7ff377b76245d7cfea8e24ad69163dc45fbbd6236093cfa9c419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:3a17bca88347d4c236eb1b6236c2ecfe6c200298a8ee208145e39b937c0251a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b161ddbf1b03a9975d85fc24a4e5f497a34670f8eee96de2b92b55473e58648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 14:17:31 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.2.tar.gz.asc crate-5.9.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.2.tar.gz.asc     && tar -xf crate-5.9.2.tar.gz -C /crate --strip-components=1     && rm crate-5.9.2.tar.gz # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Oct 2024 14:17:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 29 Oct 2024 14:17:31 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
VOLUME [/data]
# Tue, 29 Oct 2024 14:17:31 GMT
WORKDIR /data
# Tue, 29 Oct 2024 14:17:31 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-29T14:17:31.301155 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.2
# Tue, 29 Oct 2024 14:17:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Oct 2024 14:17:31 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e909ff336b3a8b3f79491d0059d6eb8e9c867221cc1d02001486a1d90dc803be`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 69.2 MB (69206030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75c6678d20518489ed7c9e26ea158f6fc99390d9a070e63bd294372720191a8`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 11.1 MB (11073760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871bd4b0c46b8c464951dbe1e77374de7e9fc21b38b1202c16b6022e59d57331`  
		Last Modified: Thu, 31 Oct 2024 21:59:31 GMT  
		Size: 147.2 MB (147193078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c260f82be535eab7329b244dff4c6dd629fe0c5890f113dd92111b54f8d427f`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1357cc0d3480a87f241a8179e6382d534419814b33c7d99766e8beaed1845ca1`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebd530480a4fc9104c3b300a0801ba712d10e6d5aa8be4626649847e4c8dbfd`  
		Last Modified: Thu, 31 Oct 2024 21:59:30 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07141e7efba6c965743bf6d3a8e7e517f167c704689ccaa4e7663ac4d053ab3c`  
		Last Modified: Thu, 31 Oct 2024 21:59:30 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29aa774588588e8c7b63747ae9fb391c71e428ff815938b741c73c4c5ccd43f5`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:827b815876bb85270f911f3d97e415ccc025e5f2b6ac1940111b0f7fac59d644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877f1e6fb0b6107f920387823f4b5592ef8c1c7ac7dec1c37a76d05dc96db463`

```dockerfile
```

-	Layers:
	-	`sha256:b993186cd1260b537e6e30536e2e256ffe882852e55c5201837874d3836fecf8`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 5.2 MB (5222394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd823197d4122d20c2baf556f2f3ec79261bab05a436fc982f7e0a04461f5bff`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 23.1 KB (23121 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c0a6149400096563612e91b2cd0e7cd64d5cf7f72f6b5eb0d403fbee86640515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229534998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1918a54e53d6c96187ef39dec1b92ce3c5be50a5468bd50c5c2102d041a329`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 14:17:31 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.2.tar.gz.asc crate-5.9.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.2.tar.gz.asc     && tar -xf crate-5.9.2.tar.gz -C /crate --strip-components=1     && rm crate-5.9.2.tar.gz # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Oct 2024 14:17:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 29 Oct 2024 14:17:31 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
VOLUME [/data]
# Tue, 29 Oct 2024 14:17:31 GMT
WORKDIR /data
# Tue, 29 Oct 2024 14:17:31 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-29T14:17:31.301155 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.2
# Tue, 29 Oct 2024 14:17:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Oct 2024 14:17:31 GMT
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
	-	`sha256:e44d54b7288042b9359cfb2c70b08338ce73ed92d616accb7f3a76a432424d1a`  
		Last Modified: Thu, 31 Oct 2024 21:59:39 GMT  
		Size: 148.4 MB (148358731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff14396b6fd74f51a2189283d42cb3c1f10dae0b37e008592eae79fff26d7f96`  
		Last Modified: Thu, 31 Oct 2024 21:59:35 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ec23ad67f03eed012c70e45bdebc40e2b94527037d903c20f9d515c5c418b4`  
		Last Modified: Thu, 31 Oct 2024 21:59:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83db5f369c1abc3434da22221077e0d0791a777068538394ddc0b1918a874e99`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640af021fc832e1e06db309b07c5172833d227b816913b044970b483a10a4caf`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c542a5f3b3823f491ee850be41fcdb94c8c98183ee1769103eb00847286f3734`  
		Last Modified: Thu, 31 Oct 2024 21:59:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:d358ab2a2ac226484fcd37b4ecbae3c61b7c71a82542f893f11f2bbdf9af00c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a587d02eea6f717b6640e5db3e8c45c041f8b4c46d1c8a8e8d5d704a3915ad`

```dockerfile
```

-	Layers:
	-	`sha256:9436f112fdae95af520070746da6808ba8e95e856636070402d69637dd7561e2`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 5.2 MB (5219098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec04fbf88b7254e59d4c13bb0d97797b92a6f2234770a14e641ce84b536e76f2`  
		Last Modified: Thu, 31 Oct 2024 21:59:35 GMT  
		Size: 23.3 KB (23257 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.2`

```console
$ docker pull crate@sha256:873233efad8e7ff377b76245d7cfea8e24ad69163dc45fbbd6236093cfa9c419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.2` - linux; amd64

```console
$ docker pull crate@sha256:3a17bca88347d4c236eb1b6236c2ecfe6c200298a8ee208145e39b937c0251a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b161ddbf1b03a9975d85fc24a4e5f497a34670f8eee96de2b92b55473e58648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 14:17:31 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.2.tar.gz.asc crate-5.9.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.2.tar.gz.asc     && tar -xf crate-5.9.2.tar.gz -C /crate --strip-components=1     && rm crate-5.9.2.tar.gz # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Oct 2024 14:17:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 29 Oct 2024 14:17:31 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
VOLUME [/data]
# Tue, 29 Oct 2024 14:17:31 GMT
WORKDIR /data
# Tue, 29 Oct 2024 14:17:31 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-29T14:17:31.301155 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.2
# Tue, 29 Oct 2024 14:17:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Oct 2024 14:17:31 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e909ff336b3a8b3f79491d0059d6eb8e9c867221cc1d02001486a1d90dc803be`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 69.2 MB (69206030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75c6678d20518489ed7c9e26ea158f6fc99390d9a070e63bd294372720191a8`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 11.1 MB (11073760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871bd4b0c46b8c464951dbe1e77374de7e9fc21b38b1202c16b6022e59d57331`  
		Last Modified: Thu, 31 Oct 2024 21:59:31 GMT  
		Size: 147.2 MB (147193078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c260f82be535eab7329b244dff4c6dd629fe0c5890f113dd92111b54f8d427f`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1357cc0d3480a87f241a8179e6382d534419814b33c7d99766e8beaed1845ca1`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebd530480a4fc9104c3b300a0801ba712d10e6d5aa8be4626649847e4c8dbfd`  
		Last Modified: Thu, 31 Oct 2024 21:59:30 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07141e7efba6c965743bf6d3a8e7e517f167c704689ccaa4e7663ac4d053ab3c`  
		Last Modified: Thu, 31 Oct 2024 21:59:30 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29aa774588588e8c7b63747ae9fb391c71e428ff815938b741c73c4c5ccd43f5`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.2` - unknown; unknown

```console
$ docker pull crate@sha256:827b815876bb85270f911f3d97e415ccc025e5f2b6ac1940111b0f7fac59d644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877f1e6fb0b6107f920387823f4b5592ef8c1c7ac7dec1c37a76d05dc96db463`

```dockerfile
```

-	Layers:
	-	`sha256:b993186cd1260b537e6e30536e2e256ffe882852e55c5201837874d3836fecf8`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 5.2 MB (5222394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd823197d4122d20c2baf556f2f3ec79261bab05a436fc982f7e0a04461f5bff`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 23.1 KB (23121 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c0a6149400096563612e91b2cd0e7cd64d5cf7f72f6b5eb0d403fbee86640515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229534998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1918a54e53d6c96187ef39dec1b92ce3c5be50a5468bd50c5c2102d041a329`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 14:17:31 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.2.tar.gz.asc crate-5.9.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.2.tar.gz.asc     && tar -xf crate-5.9.2.tar.gz -C /crate --strip-components=1     && rm crate-5.9.2.tar.gz # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Oct 2024 14:17:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 29 Oct 2024 14:17:31 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
VOLUME [/data]
# Tue, 29 Oct 2024 14:17:31 GMT
WORKDIR /data
# Tue, 29 Oct 2024 14:17:31 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-29T14:17:31.301155 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.2
# Tue, 29 Oct 2024 14:17:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Oct 2024 14:17:31 GMT
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
	-	`sha256:e44d54b7288042b9359cfb2c70b08338ce73ed92d616accb7f3a76a432424d1a`  
		Last Modified: Thu, 31 Oct 2024 21:59:39 GMT  
		Size: 148.4 MB (148358731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff14396b6fd74f51a2189283d42cb3c1f10dae0b37e008592eae79fff26d7f96`  
		Last Modified: Thu, 31 Oct 2024 21:59:35 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ec23ad67f03eed012c70e45bdebc40e2b94527037d903c20f9d515c5c418b4`  
		Last Modified: Thu, 31 Oct 2024 21:59:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83db5f369c1abc3434da22221077e0d0791a777068538394ddc0b1918a874e99`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640af021fc832e1e06db309b07c5172833d227b816913b044970b483a10a4caf`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c542a5f3b3823f491ee850be41fcdb94c8c98183ee1769103eb00847286f3734`  
		Last Modified: Thu, 31 Oct 2024 21:59:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.2` - unknown; unknown

```console
$ docker pull crate@sha256:d358ab2a2ac226484fcd37b4ecbae3c61b7c71a82542f893f11f2bbdf9af00c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a587d02eea6f717b6640e5db3e8c45c041f8b4c46d1c8a8e8d5d704a3915ad`

```dockerfile
```

-	Layers:
	-	`sha256:9436f112fdae95af520070746da6808ba8e95e856636070402d69637dd7561e2`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 5.2 MB (5219098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec04fbf88b7254e59d4c13bb0d97797b92a6f2234770a14e641ce84b536e76f2`  
		Last Modified: Thu, 31 Oct 2024 21:59:35 GMT  
		Size: 23.3 KB (23257 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:873233efad8e7ff377b76245d7cfea8e24ad69163dc45fbbd6236093cfa9c419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:3a17bca88347d4c236eb1b6236c2ecfe6c200298a8ee208145e39b937c0251a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b161ddbf1b03a9975d85fc24a4e5f497a34670f8eee96de2b92b55473e58648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 14:17:31 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.2.tar.gz.asc crate-5.9.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.2.tar.gz.asc     && tar -xf crate-5.9.2.tar.gz -C /crate --strip-components=1     && rm crate-5.9.2.tar.gz # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Oct 2024 14:17:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 29 Oct 2024 14:17:31 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
VOLUME [/data]
# Tue, 29 Oct 2024 14:17:31 GMT
WORKDIR /data
# Tue, 29 Oct 2024 14:17:31 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-29T14:17:31.301155 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.2
# Tue, 29 Oct 2024 14:17:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Oct 2024 14:17:31 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e909ff336b3a8b3f79491d0059d6eb8e9c867221cc1d02001486a1d90dc803be`  
		Last Modified: Tue, 24 Sep 2024 01:00:51 GMT  
		Size: 69.2 MB (69206030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75c6678d20518489ed7c9e26ea158f6fc99390d9a070e63bd294372720191a8`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 11.1 MB (11073760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871bd4b0c46b8c464951dbe1e77374de7e9fc21b38b1202c16b6022e59d57331`  
		Last Modified: Thu, 31 Oct 2024 21:59:31 GMT  
		Size: 147.2 MB (147193078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c260f82be535eab7329b244dff4c6dd629fe0c5890f113dd92111b54f8d427f`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1357cc0d3480a87f241a8179e6382d534419814b33c7d99766e8beaed1845ca1`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebd530480a4fc9104c3b300a0801ba712d10e6d5aa8be4626649847e4c8dbfd`  
		Last Modified: Thu, 31 Oct 2024 21:59:30 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07141e7efba6c965743bf6d3a8e7e517f167c704689ccaa4e7663ac4d053ab3c`  
		Last Modified: Thu, 31 Oct 2024 21:59:30 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29aa774588588e8c7b63747ae9fb391c71e428ff815938b741c73c4c5ccd43f5`  
		Last Modified: Thu, 31 Oct 2024 21:59:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:827b815876bb85270f911f3d97e415ccc025e5f2b6ac1940111b0f7fac59d644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877f1e6fb0b6107f920387823f4b5592ef8c1c7ac7dec1c37a76d05dc96db463`

```dockerfile
```

-	Layers:
	-	`sha256:b993186cd1260b537e6e30536e2e256ffe882852e55c5201837874d3836fecf8`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 5.2 MB (5222394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd823197d4122d20c2baf556f2f3ec79261bab05a436fc982f7e0a04461f5bff`  
		Last Modified: Thu, 31 Oct 2024 21:59:29 GMT  
		Size: 23.1 KB (23121 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c0a6149400096563612e91b2cd0e7cd64d5cf7f72f6b5eb0d403fbee86640515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229534998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1918a54e53d6c96187ef39dec1b92ce3c5be50a5468bd50c5c2102d041a329`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 23 Sep 2024 15:17:35 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 23 Sep 2024 15:17:35 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 14:17:31 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.2.tar.gz.asc crate-5.9.2.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.2.tar.gz.asc     && tar -xf crate-5.9.2.tar.gz -C /crate --strip-components=1     && rm crate-5.9.2.tar.gz # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Oct 2024 14:17:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 29 Oct 2024 14:17:31 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
VOLUME [/data]
# Tue, 29 Oct 2024 14:17:31 GMT
WORKDIR /data
# Tue, 29 Oct 2024 14:17:31 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-10-29T14:17:31.301155 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.2
# Tue, 29 Oct 2024 14:17:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 14:17:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Oct 2024 14:17:31 GMT
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
	-	`sha256:e44d54b7288042b9359cfb2c70b08338ce73ed92d616accb7f3a76a432424d1a`  
		Last Modified: Thu, 31 Oct 2024 21:59:39 GMT  
		Size: 148.4 MB (148358731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff14396b6fd74f51a2189283d42cb3c1f10dae0b37e008592eae79fff26d7f96`  
		Last Modified: Thu, 31 Oct 2024 21:59:35 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ec23ad67f03eed012c70e45bdebc40e2b94527037d903c20f9d515c5c418b4`  
		Last Modified: Thu, 31 Oct 2024 21:59:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83db5f369c1abc3434da22221077e0d0791a777068538394ddc0b1918a874e99`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640af021fc832e1e06db309b07c5172833d227b816913b044970b483a10a4caf`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c542a5f3b3823f491ee850be41fcdb94c8c98183ee1769103eb00847286f3734`  
		Last Modified: Thu, 31 Oct 2024 21:59:37 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:d358ab2a2ac226484fcd37b4ecbae3c61b7c71a82542f893f11f2bbdf9af00c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a587d02eea6f717b6640e5db3e8c45c041f8b4c46d1c8a8e8d5d704a3915ad`

```dockerfile
```

-	Layers:
	-	`sha256:9436f112fdae95af520070746da6808ba8e95e856636070402d69637dd7561e2`  
		Last Modified: Thu, 31 Oct 2024 21:59:36 GMT  
		Size: 5.2 MB (5219098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec04fbf88b7254e59d4c13bb0d97797b92a6f2234770a14e641ce84b536e76f2`  
		Last Modified: Thu, 31 Oct 2024 21:59:35 GMT  
		Size: 23.3 KB (23257 bytes)  
		MIME: application/vnd.in-toto+json
