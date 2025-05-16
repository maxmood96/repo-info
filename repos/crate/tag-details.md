<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.6`](#crate5106)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:88a1093592db1da1f0c6baf3b89bea88e219626b432d27038c17489243494aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:a30bc323915672e2c6b7b3f274bbbc59398f5829e1cbe73ac216131091a7375c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252565538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32f78f044dca6871b90399c09031cac316ebfbbe73a28e7afd4a5c8615fec9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Mon, 14 Apr 2025 21:04:12 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d65c0ff10b97fe30f1f4f8ad0e54434f7e55df9e4df317bc6b790b21a2f3b`  
		Last Modified: Thu, 15 May 2025 18:31:23 GMT  
		Size: 34.3 MB (34259521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e4ef1e9dc73613c2f92791a13eba484b005884f040ed6db89e249e700e06b5`  
		Last Modified: Thu, 15 May 2025 18:31:25 GMT  
		Size: 149.7 MB (149657184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3e4e463900b80d4e9702ba359b67152fad9042b06af211b40d4366bd7ed81b`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f91fc454e75587dcb9e1f2d14aab4fd731dcddabdadaf7df8ab691999b558e`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069766b6c7e74d39522f6dd13b146b2f5a37451a96ed55f8a2c7ba736daac040`  
		Last Modified: Thu, 15 May 2025 18:31:23 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e09ca30e54e16bf046b45bfaa7a7911b2d95b7cbb84a3693cfa0f3dfb5cf48`  
		Last Modified: Thu, 15 May 2025 18:31:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f3697a02557c7e5b8b2abeea30f7d2f23d60f6bba460d818d931ebd82abc30`  
		Last Modified: Thu, 15 May 2025 18:31:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:0dd5a92c1c147ea3c693bb8352694354d05f2c119edc5f1b03277a142852380a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8526bef86022646dbb9cf05ab98f6b049d43f49a1faddba598180eb0f811b`

```dockerfile
```

-	Layers:
	-	`sha256:ee0a8cc9b728d37ac4c62d9a1b3e9d29f3f3e14dc12beb92f0a6b604cfabc6b6`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 5.2 MB (5179018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046ae30306fd0cf8db566152737fac45b8bca4ee9f8925b66cb954b0a2964d3c`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:03873655b5526021fd3848ef9402c4a4caec7dfd05c5488448007528dc78eb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247726951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d1fa80727947dff722ed41a39aa3e17331c7c6194a2bc693751757a71f80dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Mon, 14 Apr 2025 21:03:41 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9379fff095e8fe20a8323fa2556b6639feedf28f54e6be52bf0e56969e38f73`  
		Last Modified: Wed, 30 Apr 2025 17:05:10 GMT  
		Size: 30.2 MB (30200753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed8c68b72b6172144e2cb155dda1334db75b620dba4b357a5cae1b263b32845`  
		Last Modified: Thu, 15 May 2025 21:19:18 GMT  
		Size: 150.3 MB (150335393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90a747eebdff614ccb9ce2077e157d3ebe4b9e57892273e4495d862c174698`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 1.9 MB (1943640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd43cc82c29488f68fdf06dc22136f291100980561e641894bbccc3bd23124ce`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671b69987061af7827e57db6ce6ed3186be85c3a7e0cbd3c8457db90a56b4981`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37b83f238a064fbc33ce6ce6084855c7031f0223a30af11340525a818ab31c9`  
		Last Modified: Thu, 15 May 2025 21:19:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349adf5a4234395719122f805f955ea49254b8fd20d5c5a9332f49802e4aa7ea`  
		Last Modified: Thu, 15 May 2025 21:19:15 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:e8045405db5f010ebad8522cd15576a72bb660930a1f3e8ad19477c8f2ff9aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a60f9a8d3e84e8c968f8dc7cb56cac9dfd6d9359ef8efea4a036fe837c487f`

```dockerfile
```

-	Layers:
	-	`sha256:3cb0434cd51b87f2b01c3bc610357d331cb8810f1e43e0465c2389a36522f80b`  
		Last Modified: Thu, 15 May 2025 21:19:15 GMT  
		Size: 5.2 MB (5179517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55bee07bda224614c38f7f84660fb7e16220af7d6f4d8ea943526820fee6112b`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.6`

```console
$ docker pull crate@sha256:88a1093592db1da1f0c6baf3b89bea88e219626b432d27038c17489243494aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.6` - linux; amd64

```console
$ docker pull crate@sha256:a30bc323915672e2c6b7b3f274bbbc59398f5829e1cbe73ac216131091a7375c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252565538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32f78f044dca6871b90399c09031cac316ebfbbe73a28e7afd4a5c8615fec9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Mon, 14 Apr 2025 21:04:12 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d65c0ff10b97fe30f1f4f8ad0e54434f7e55df9e4df317bc6b790b21a2f3b`  
		Last Modified: Thu, 15 May 2025 18:31:23 GMT  
		Size: 34.3 MB (34259521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e4ef1e9dc73613c2f92791a13eba484b005884f040ed6db89e249e700e06b5`  
		Last Modified: Thu, 15 May 2025 18:31:25 GMT  
		Size: 149.7 MB (149657184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3e4e463900b80d4e9702ba359b67152fad9042b06af211b40d4366bd7ed81b`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f91fc454e75587dcb9e1f2d14aab4fd731dcddabdadaf7df8ab691999b558e`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069766b6c7e74d39522f6dd13b146b2f5a37451a96ed55f8a2c7ba736daac040`  
		Last Modified: Thu, 15 May 2025 18:31:23 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e09ca30e54e16bf046b45bfaa7a7911b2d95b7cbb84a3693cfa0f3dfb5cf48`  
		Last Modified: Thu, 15 May 2025 18:31:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f3697a02557c7e5b8b2abeea30f7d2f23d60f6bba460d818d931ebd82abc30`  
		Last Modified: Thu, 15 May 2025 18:31:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.6` - unknown; unknown

```console
$ docker pull crate@sha256:0dd5a92c1c147ea3c693bb8352694354d05f2c119edc5f1b03277a142852380a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8526bef86022646dbb9cf05ab98f6b049d43f49a1faddba598180eb0f811b`

```dockerfile
```

-	Layers:
	-	`sha256:ee0a8cc9b728d37ac4c62d9a1b3e9d29f3f3e14dc12beb92f0a6b604cfabc6b6`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 5.2 MB (5179018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046ae30306fd0cf8db566152737fac45b8bca4ee9f8925b66cb954b0a2964d3c`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:03873655b5526021fd3848ef9402c4a4caec7dfd05c5488448007528dc78eb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247726951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d1fa80727947dff722ed41a39aa3e17331c7c6194a2bc693751757a71f80dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Mon, 14 Apr 2025 21:03:41 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9379fff095e8fe20a8323fa2556b6639feedf28f54e6be52bf0e56969e38f73`  
		Last Modified: Wed, 30 Apr 2025 17:05:10 GMT  
		Size: 30.2 MB (30200753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed8c68b72b6172144e2cb155dda1334db75b620dba4b357a5cae1b263b32845`  
		Last Modified: Thu, 15 May 2025 21:19:18 GMT  
		Size: 150.3 MB (150335393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90a747eebdff614ccb9ce2077e157d3ebe4b9e57892273e4495d862c174698`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 1.9 MB (1943640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd43cc82c29488f68fdf06dc22136f291100980561e641894bbccc3bd23124ce`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671b69987061af7827e57db6ce6ed3186be85c3a7e0cbd3c8457db90a56b4981`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37b83f238a064fbc33ce6ce6084855c7031f0223a30af11340525a818ab31c9`  
		Last Modified: Thu, 15 May 2025 21:19:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349adf5a4234395719122f805f955ea49254b8fd20d5c5a9332f49802e4aa7ea`  
		Last Modified: Thu, 15 May 2025 21:19:15 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.6` - unknown; unknown

```console
$ docker pull crate@sha256:e8045405db5f010ebad8522cd15576a72bb660930a1f3e8ad19477c8f2ff9aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a60f9a8d3e84e8c968f8dc7cb56cac9dfd6d9359ef8efea4a036fe837c487f`

```dockerfile
```

-	Layers:
	-	`sha256:3cb0434cd51b87f2b01c3bc610357d331cb8810f1e43e0465c2389a36522f80b`  
		Last Modified: Thu, 15 May 2025 21:19:15 GMT  
		Size: 5.2 MB (5179517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55bee07bda224614c38f7f84660fb7e16220af7d6f4d8ea943526820fee6112b`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:ffedbc7974cda08786c0c947ea192abe597a1ba15538d9bb4edbbf494cc847f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:f537194f75e09dbadb3f50f8cf3b34b55cf715af664a7bcf1afafc12adf36c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233063168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c2f8d2990e1a7e79992d2fadda933f90c212b968dd92cf8fa6c8a9745d03eb`
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
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Mon, 14 Apr 2025 21:04:12 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcec82adec80585ecd662ca78a0a2f00f1915f54a14c46e5fffbae3da506f64a`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 15.4 MB (15404609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3397a7a4a1589583fca2b027400b84db10a3df5d76a6761164d5fdc8915d8636`  
		Last Modified: Mon, 14 Apr 2025 21:08:14 GMT  
		Size: 149.0 MB (149009725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16ff60c8defcb75fcd4b47eda730704b25042bf0bacdd26db044716c5f44967`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e702fe00bb48c1f7ff88c7d399496d68fd6246a4b4c0630e662082520ef858d`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb77d490a22bdd1bff757b7c07083b03249581bcb3de663375ef4a1d681fcc`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3591542bf015fde66b8971c54f001a925cac5bb54356d0c6ccd3c525ac1f5796`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ba8241687644aaee953c448171863ea247ab515a040b7dd1ffbc9d18f13f49`  
		Last Modified: Mon, 14 Apr 2025 21:08:13 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:fc0119993a2e866843babd9ff37f9006ee11e5684564d4a1ba48f2c2deba6101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f9fcd3f5b0c955a620d476cac862dd9c5cd156f826e96268265d0d6c95da40`

```dockerfile
```

-	Layers:
	-	`sha256:37ac76c12023fccc6ff552b2d6b0fd0c5a8b7aad3a757b5a784f5a4bb1d89fe5`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 5.2 MB (5167203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332cc5481986c82035b0ef8fe8c21a9d63453825901ef3a7e3da29051e4480ca`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:929a78a846c2a43d7b2f11e10210e165f71521c46ad85dfd9dea7a975dc861f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232364545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d635f02244bb4a41091db9633e88c9c89553ffc1e9f0d1c40d718c31b6effa5a`
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
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Mon, 14 Apr 2025 21:03:41 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174a192bbbdb738a0ab32cb314abdd2dc66239fe7bb1be4022e0a269ef6131f2`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 15.5 MB (15465210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae080b7caf812fac4b8cf6a830e6c1b4c939f9879b6d496e0d9a78165f45be0`  
		Last Modified: Mon, 14 Apr 2025 21:08:55 GMT  
		Size: 149.7 MB (149708529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3779bc1d20dede154153f3cf11400f897cbc19e8d7f6622f42097f8cb98fe512`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8250ea430f0db690142025bae4c5dd61e8a3658989ae0eb05ae1ee80ab39439`  
		Last Modified: Mon, 14 Apr 2025 21:08:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098c385c76e26e9dbd06bd1f4ce38329edcb5cd18faa6f7b47db4b4ae6ebe1a0`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d28a23eb4d9b10fa7853258821d225981be6d2b2e20af490ed810560fe5ac1`  
		Last Modified: Mon, 14 Apr 2025 21:08:53 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5d4d122eca3f0aed1105a90b6224bfb70eea0dae82188c88df6a6339cbd54`  
		Last Modified: Mon, 14 Apr 2025 21:08:53 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:07b89b44a31707eaca712262b2c15cf0a8382dfcd3b4ff74fb96df1d1caa5142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5187527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d22bc368c009dad32270ad43fca210c463741de4ad59c05767fde888bddd240`

```dockerfile
```

-	Layers:
	-	`sha256:5a271bf75c301f8293930fe7bc18dbe4c73ce087714d1ce864a16963a3d8f89f`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 5.2 MB (5164499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b73b00e3c1dafdaf2e2dc0ce1df8b8ea7e116b330a2259e638a398c8b3e45c3c`  
		Last Modified: Mon, 14 Apr 2025 21:08:51 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:ffedbc7974cda08786c0c947ea192abe597a1ba15538d9bb4edbbf494cc847f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:f537194f75e09dbadb3f50f8cf3b34b55cf715af664a7bcf1afafc12adf36c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233063168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c2f8d2990e1a7e79992d2fadda933f90c212b968dd92cf8fa6c8a9745d03eb`
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
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Mon, 14 Apr 2025 21:04:12 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcec82adec80585ecd662ca78a0a2f00f1915f54a14c46e5fffbae3da506f64a`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 15.4 MB (15404609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3397a7a4a1589583fca2b027400b84db10a3df5d76a6761164d5fdc8915d8636`  
		Last Modified: Mon, 14 Apr 2025 21:08:14 GMT  
		Size: 149.0 MB (149009725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16ff60c8defcb75fcd4b47eda730704b25042bf0bacdd26db044716c5f44967`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e702fe00bb48c1f7ff88c7d399496d68fd6246a4b4c0630e662082520ef858d`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb77d490a22bdd1bff757b7c07083b03249581bcb3de663375ef4a1d681fcc`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3591542bf015fde66b8971c54f001a925cac5bb54356d0c6ccd3c525ac1f5796`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ba8241687644aaee953c448171863ea247ab515a040b7dd1ffbc9d18f13f49`  
		Last Modified: Mon, 14 Apr 2025 21:08:13 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:fc0119993a2e866843babd9ff37f9006ee11e5684564d4a1ba48f2c2deba6101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f9fcd3f5b0c955a620d476cac862dd9c5cd156f826e96268265d0d6c95da40`

```dockerfile
```

-	Layers:
	-	`sha256:37ac76c12023fccc6ff552b2d6b0fd0c5a8b7aad3a757b5a784f5a4bb1d89fe5`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 5.2 MB (5167203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332cc5481986c82035b0ef8fe8c21a9d63453825901ef3a7e3da29051e4480ca`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:929a78a846c2a43d7b2f11e10210e165f71521c46ad85dfd9dea7a975dc861f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232364545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d635f02244bb4a41091db9633e88c9c89553ffc1e9f0d1c40d718c31b6effa5a`
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
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Mon, 14 Apr 2025 21:03:41 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174a192bbbdb738a0ab32cb314abdd2dc66239fe7bb1be4022e0a269ef6131f2`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 15.5 MB (15465210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae080b7caf812fac4b8cf6a830e6c1b4c939f9879b6d496e0d9a78165f45be0`  
		Last Modified: Mon, 14 Apr 2025 21:08:55 GMT  
		Size: 149.7 MB (149708529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3779bc1d20dede154153f3cf11400f897cbc19e8d7f6622f42097f8cb98fe512`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8250ea430f0db690142025bae4c5dd61e8a3658989ae0eb05ae1ee80ab39439`  
		Last Modified: Mon, 14 Apr 2025 21:08:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098c385c76e26e9dbd06bd1f4ce38329edcb5cd18faa6f7b47db4b4ae6ebe1a0`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d28a23eb4d9b10fa7853258821d225981be6d2b2e20af490ed810560fe5ac1`  
		Last Modified: Mon, 14 Apr 2025 21:08:53 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5d4d122eca3f0aed1105a90b6224bfb70eea0dae82188c88df6a6339cbd54`  
		Last Modified: Mon, 14 Apr 2025 21:08:53 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:07b89b44a31707eaca712262b2c15cf0a8382dfcd3b4ff74fb96df1d1caa5142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5187527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d22bc368c009dad32270ad43fca210c463741de4ad59c05767fde888bddd240`

```dockerfile
```

-	Layers:
	-	`sha256:5a271bf75c301f8293930fe7bc18dbe4c73ce087714d1ce864a16963a3d8f89f`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 5.2 MB (5164499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b73b00e3c1dafdaf2e2dc0ce1df8b8ea7e116b330a2259e638a398c8b3e45c3c`  
		Last Modified: Mon, 14 Apr 2025 21:08:51 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:88a1093592db1da1f0c6baf3b89bea88e219626b432d27038c17489243494aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:a30bc323915672e2c6b7b3f274bbbc59398f5829e1cbe73ac216131091a7375c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252565538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32f78f044dca6871b90399c09031cac316ebfbbe73a28e7afd4a5c8615fec9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Mon, 14 Apr 2025 21:04:12 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d65c0ff10b97fe30f1f4f8ad0e54434f7e55df9e4df317bc6b790b21a2f3b`  
		Last Modified: Thu, 15 May 2025 18:31:23 GMT  
		Size: 34.3 MB (34259521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e4ef1e9dc73613c2f92791a13eba484b005884f040ed6db89e249e700e06b5`  
		Last Modified: Thu, 15 May 2025 18:31:25 GMT  
		Size: 149.7 MB (149657184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3e4e463900b80d4e9702ba359b67152fad9042b06af211b40d4366bd7ed81b`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f91fc454e75587dcb9e1f2d14aab4fd731dcddabdadaf7df8ab691999b558e`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069766b6c7e74d39522f6dd13b146b2f5a37451a96ed55f8a2c7ba736daac040`  
		Last Modified: Thu, 15 May 2025 18:31:23 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e09ca30e54e16bf046b45bfaa7a7911b2d95b7cbb84a3693cfa0f3dfb5cf48`  
		Last Modified: Thu, 15 May 2025 18:31:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f3697a02557c7e5b8b2abeea30f7d2f23d60f6bba460d818d931ebd82abc30`  
		Last Modified: Thu, 15 May 2025 18:31:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:0dd5a92c1c147ea3c693bb8352694354d05f2c119edc5f1b03277a142852380a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c8526bef86022646dbb9cf05ab98f6b049d43f49a1faddba598180eb0f811b`

```dockerfile
```

-	Layers:
	-	`sha256:ee0a8cc9b728d37ac4c62d9a1b3e9d29f3f3e14dc12beb92f0a6b604cfabc6b6`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 5.2 MB (5179018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046ae30306fd0cf8db566152737fac45b8bca4ee9f8925b66cb954b0a2964d3c`  
		Last Modified: Thu, 15 May 2025 18:31:22 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:03873655b5526021fd3848ef9402c4a4caec7dfd05c5488448007528dc78eb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247726951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d1fa80727947dff722ed41a39aa3e17331c7c6194a2bc693751757a71f80dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 12 May 2025 12:44:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.6.tar.gz.asc crate-5.10.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.6.tar.gz.asc     && tar -xf crate-5.10.6.tar.gz -C /crate --strip-components=1     && rm crate-5.10.6.tar.gz # buildkit
# Mon, 12 May 2025 12:44:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 12:44:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 12 May 2025 12:44:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 12 May 2025 12:44:57 GMT
VOLUME [/data]
# Mon, 12 May 2025 12:44:57 GMT
WORKDIR /data
# Mon, 12 May 2025 12:44:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 12 May 2025 12:44:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 12 May 2025 12:44:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-12T12:44:57.641286 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.6
# Mon, 12 May 2025 12:44:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 12 May 2025 12:44:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 12:44:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Mon, 14 Apr 2025 21:03:41 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9379fff095e8fe20a8323fa2556b6639feedf28f54e6be52bf0e56969e38f73`  
		Last Modified: Wed, 30 Apr 2025 17:05:10 GMT  
		Size: 30.2 MB (30200753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed8c68b72b6172144e2cb155dda1334db75b620dba4b357a5cae1b263b32845`  
		Last Modified: Thu, 15 May 2025 21:19:18 GMT  
		Size: 150.3 MB (150335393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90a747eebdff614ccb9ce2077e157d3ebe4b9e57892273e4495d862c174698`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 1.9 MB (1943640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd43cc82c29488f68fdf06dc22136f291100980561e641894bbccc3bd23124ce`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671b69987061af7827e57db6ce6ed3186be85c3a7e0cbd3c8457db90a56b4981`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37b83f238a064fbc33ce6ce6084855c7031f0223a30af11340525a818ab31c9`  
		Last Modified: Thu, 15 May 2025 21:19:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349adf5a4234395719122f805f955ea49254b8fd20d5c5a9332f49802e4aa7ea`  
		Last Modified: Thu, 15 May 2025 21:19:15 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:e8045405db5f010ebad8522cd15576a72bb660930a1f3e8ad19477c8f2ff9aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a60f9a8d3e84e8c968f8dc7cb56cac9dfd6d9359ef8efea4a036fe837c487f`

```dockerfile
```

-	Layers:
	-	`sha256:3cb0434cd51b87f2b01c3bc610357d331cb8810f1e43e0465c2389a36522f80b`  
		Last Modified: Thu, 15 May 2025 21:19:15 GMT  
		Size: 5.2 MB (5179517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55bee07bda224614c38f7f84660fb7e16220af7d6f4d8ea943526820fee6112b`  
		Last Modified: Thu, 15 May 2025 21:19:14 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json
