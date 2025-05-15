<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.6`](#crate5106)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:bc2486b823012bede7dd5097b5afb4265e6b6687a3fc4d6538f4ce204ae718a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:5286afc9099a9fa37bcc595375e8b395218ac91d559bff285b84c06a56431806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248582059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efa124dc6e7080398bc418a56b1b4a892ffe508b0bd6b4520cc740d0d50d1d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 09:26:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.5.tar.gz.asc crate-5.10.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.5.tar.gz.asc     && tar -xf crate-5.10.5.tar.gz -C /crate --strip-components=1     && rm crate-5.10.5.tar.gz # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 09:26:14 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Apr 2025 09:26:14 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
VOLUME [/data]
# Mon, 28 Apr 2025 09:26:14 GMT
WORKDIR /data
# Mon, 28 Apr 2025 09:26:14 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Apr 2025 09:26:14 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-28T09:26:14.692678 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.5
# Mon, 28 Apr 2025 09:26:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Apr 2025 09:26:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Thu, 08 May 2025 17:54:23 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2531d80023de6817002c2a3797be9bc48a67052f951793183e0748b6dad9979a`  
		Last Modified: Thu, 08 May 2025 17:54:17 GMT  
		Size: 30.3 MB (30273031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97fdfbd43951eb6e2ce7514a24181fd5ad9e71d1053e5b8d2a1ff523e4637e2`  
		Last Modified: Thu, 08 May 2025 17:54:28 GMT  
		Size: 149.7 MB (149660191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a591955bcb67fe15285d9acf42e43343b7e3758bacb9a16ba2fd9e32e3460d`  
		Last Modified: Thu, 08 May 2025 17:54:18 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f5f781cedbfa0ff86dfa6fcc23b625c98e63dedf4bfd64490dc8bdb6ae64f5`  
		Last Modified: Thu, 08 May 2025 17:54:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee31c65daed54d5c494c81daaed068db1bbf0201872a0a643b1a302ba2c543`  
		Last Modified: Thu, 08 May 2025 17:54:19 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4ba9f909d4852eecb274c820704fa92a51700ecca0c2648b2ca11cee6b5a0b`  
		Last Modified: Thu, 08 May 2025 17:54:19 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502b808bd9ea498aa61b84740328b20a3e3b3f0a358aafbdbe7ac0ec02baa36f`  
		Last Modified: Thu, 08 May 2025 17:54:20 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:91a728d97ababe6b2a60bcd212b025bd251783a88bad67134eb4506993b20476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f88fc937d91633bdc8d73f1fecaa80dfadfadc4fccba9d3c0b530e14444bf01`

```dockerfile
```

-	Layers:
	-	`sha256:f51bfe5d45f3ed0240eef44efb8d8d52f62cabfec77e748f992a7d1712fc2876`  
		Last Modified: Wed, 30 Apr 2025 17:01:59 GMT  
		Size: 5.2 MB (5169383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cddc87a4515e3a7ada3bf43b831c3d51aa42308857ae78c7edaf17b01eaa0d78`  
		Last Modified: Wed, 30 Apr 2025 17:01:58 GMT  
		Size: 23.2 KB (23200 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3bd56dc2da3c4c2bb41ba5cb1a62c5aecc7c2184acde53e230996faa6de31f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247728752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bda23076a294a68b36c2aba34f105a4d31e1756b5a93dd84ef4e8435794ce00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 09:26:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.5.tar.gz.asc crate-5.10.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.5.tar.gz.asc     && tar -xf crate-5.10.5.tar.gz -C /crate --strip-components=1     && rm crate-5.10.5.tar.gz # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 09:26:14 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Apr 2025 09:26:14 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
VOLUME [/data]
# Mon, 28 Apr 2025 09:26:14 GMT
WORKDIR /data
# Mon, 28 Apr 2025 09:26:14 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Apr 2025 09:26:14 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-28T09:26:14.692678 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.5
# Mon, 28 Apr 2025 09:26:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Apr 2025 09:26:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Thu, 08 May 2025 18:32:32 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9379fff095e8fe20a8323fa2556b6639feedf28f54e6be52bf0e56969e38f73`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 30.2 MB (30200753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b8a277ffd5ff23a1ecafe738e7734168280b78c7725c4df5837bc913fea7df`  
		Last Modified: Fri, 09 May 2025 16:04:43 GMT  
		Size: 150.3 MB (150337193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cde2427af5eabd2a52fbcc43ee0be7daf3e6f6bc874623cbb8c35fea77ca1f7`  
		Last Modified: Fri, 09 May 2025 16:02:40 GMT  
		Size: 1.9 MB (1943640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5062da19457d2b883573ba218232a1f97f6d7318c2b5fa6841c3493178b057`  
		Last Modified: Fri, 09 May 2025 16:02:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8fef20f563ad4d561167a82628b3ec1eaf7ffa04fc8f3efc6caabc5f4f286`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ba9e5c50e1fa090415ff9766e6df54863fa64541525f10875eb88f40834ac`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626c91d1033af3ad5fae5e63fe8c9e8403c27557c40ccb3fcece4ab1ecfdb9c2`  
		Last Modified: Fri, 09 May 2025 16:04:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:642301bf5c40179e36f06908124a4633e5cc72fd304ed767029f2e6a399b4c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f434f4273f801d29848a0bbf504be6b9bcb8e410223cca9692545ca0529e41f4`

```dockerfile
```

-	Layers:
	-	`sha256:33ffecd0be028f2ff8ec63a420edac9927cbf614b4ea216b424432d87b647352`  
		Last Modified: Wed, 30 Apr 2025 17:05:06 GMT  
		Size: 5.2 MB (5166691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb1bc32937011b4a8ca77800787879b9761e3d8f992b5712adf4e68c4a2a924`  
		Last Modified: Wed, 30 Apr 2025 17:05:05 GMT  
		Size: 23.3 KB (23337 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.6`

**does not exist** (yet?)

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
		Last Modified: Thu, 08 May 2025 17:54:23 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcec82adec80585ecd662ca78a0a2f00f1915f54a14c46e5fffbae3da506f64a`  
		Last Modified: Fri, 09 May 2025 07:06:46 GMT  
		Size: 15.4 MB (15404609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3397a7a4a1589583fca2b027400b84db10a3df5d76a6761164d5fdc8915d8636`  
		Last Modified: Fri, 09 May 2025 07:06:55 GMT  
		Size: 149.0 MB (149009725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16ff60c8defcb75fcd4b47eda730704b25042bf0bacdd26db044716c5f44967`  
		Last Modified: Fri, 09 May 2025 07:06:47 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e702fe00bb48c1f7ff88c7d399496d68fd6246a4b4c0630e662082520ef858d`  
		Last Modified: Fri, 09 May 2025 01:12:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb77d490a22bdd1bff757b7c07083b03249581bcb3de663375ef4a1d681fcc`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3591542bf015fde66b8971c54f001a925cac5bb54356d0c6ccd3c525ac1f5796`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ba8241687644aaee953c448171863ea247ab515a040b7dd1ffbc9d18f13f49`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
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
		Last Modified: Thu, 08 May 2025 18:32:32 GMT  
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
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098c385c76e26e9dbd06bd1f4ce38329edcb5cd18faa6f7b47db4b4ae6ebe1a0`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d28a23eb4d9b10fa7853258821d225981be6d2b2e20af490ed810560fe5ac1`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5d4d122eca3f0aed1105a90b6224bfb70eea0dae82188c88df6a6339cbd54`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
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
		Last Modified: Thu, 08 May 2025 17:54:23 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcec82adec80585ecd662ca78a0a2f00f1915f54a14c46e5fffbae3da506f64a`  
		Last Modified: Fri, 09 May 2025 07:06:46 GMT  
		Size: 15.4 MB (15404609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3397a7a4a1589583fca2b027400b84db10a3df5d76a6761164d5fdc8915d8636`  
		Last Modified: Fri, 09 May 2025 07:06:55 GMT  
		Size: 149.0 MB (149009725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16ff60c8defcb75fcd4b47eda730704b25042bf0bacdd26db044716c5f44967`  
		Last Modified: Fri, 09 May 2025 07:06:47 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e702fe00bb48c1f7ff88c7d399496d68fd6246a4b4c0630e662082520ef858d`  
		Last Modified: Fri, 09 May 2025 01:12:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb77d490a22bdd1bff757b7c07083b03249581bcb3de663375ef4a1d681fcc`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3591542bf015fde66b8971c54f001a925cac5bb54356d0c6ccd3c525ac1f5796`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ba8241687644aaee953c448171863ea247ab515a040b7dd1ffbc9d18f13f49`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
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
		Last Modified: Thu, 08 May 2025 18:32:32 GMT  
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
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098c385c76e26e9dbd06bd1f4ce38329edcb5cd18faa6f7b47db4b4ae6ebe1a0`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d28a23eb4d9b10fa7853258821d225981be6d2b2e20af490ed810560fe5ac1`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5d4d122eca3f0aed1105a90b6224bfb70eea0dae82188c88df6a6339cbd54`  
		Last Modified: Fri, 09 May 2025 01:12:20 GMT  
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
$ docker pull crate@sha256:bc2486b823012bede7dd5097b5afb4265e6b6687a3fc4d6538f4ce204ae718a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:5286afc9099a9fa37bcc595375e8b395218ac91d559bff285b84c06a56431806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248582059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efa124dc6e7080398bc418a56b1b4a892ffe508b0bd6b4520cc740d0d50d1d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 09:26:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.5.tar.gz.asc crate-5.10.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.5.tar.gz.asc     && tar -xf crate-5.10.5.tar.gz -C /crate --strip-components=1     && rm crate-5.10.5.tar.gz # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 09:26:14 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Apr 2025 09:26:14 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
VOLUME [/data]
# Mon, 28 Apr 2025 09:26:14 GMT
WORKDIR /data
# Mon, 28 Apr 2025 09:26:14 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Apr 2025 09:26:14 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-28T09:26:14.692678 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.5
# Mon, 28 Apr 2025 09:26:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Apr 2025 09:26:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Thu, 08 May 2025 17:54:23 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2531d80023de6817002c2a3797be9bc48a67052f951793183e0748b6dad9979a`  
		Last Modified: Thu, 08 May 2025 17:54:17 GMT  
		Size: 30.3 MB (30273031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97fdfbd43951eb6e2ce7514a24181fd5ad9e71d1053e5b8d2a1ff523e4637e2`  
		Last Modified: Thu, 08 May 2025 17:54:28 GMT  
		Size: 149.7 MB (149660191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a591955bcb67fe15285d9acf42e43343b7e3758bacb9a16ba2fd9e32e3460d`  
		Last Modified: Thu, 08 May 2025 17:54:18 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f5f781cedbfa0ff86dfa6fcc23b625c98e63dedf4bfd64490dc8bdb6ae64f5`  
		Last Modified: Thu, 08 May 2025 17:54:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee31c65daed54d5c494c81daaed068db1bbf0201872a0a643b1a302ba2c543`  
		Last Modified: Thu, 08 May 2025 17:54:19 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4ba9f909d4852eecb274c820704fa92a51700ecca0c2648b2ca11cee6b5a0b`  
		Last Modified: Thu, 08 May 2025 17:54:19 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502b808bd9ea498aa61b84740328b20a3e3b3f0a358aafbdbe7ac0ec02baa36f`  
		Last Modified: Thu, 08 May 2025 17:54:20 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:91a728d97ababe6b2a60bcd212b025bd251783a88bad67134eb4506993b20476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f88fc937d91633bdc8d73f1fecaa80dfadfadc4fccba9d3c0b530e14444bf01`

```dockerfile
```

-	Layers:
	-	`sha256:f51bfe5d45f3ed0240eef44efb8d8d52f62cabfec77e748f992a7d1712fc2876`  
		Last Modified: Wed, 30 Apr 2025 17:01:59 GMT  
		Size: 5.2 MB (5169383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cddc87a4515e3a7ada3bf43b831c3d51aa42308857ae78c7edaf17b01eaa0d78`  
		Last Modified: Wed, 30 Apr 2025 17:01:58 GMT  
		Size: 23.2 KB (23200 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3bd56dc2da3c4c2bb41ba5cb1a62c5aecc7c2184acde53e230996faa6de31f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247728752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bda23076a294a68b36c2aba34f105a4d31e1756b5a93dd84ef4e8435794ce00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 11 Apr 2025 11:30:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 11 Apr 2025 11:30:57 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 09:26:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.5.tar.gz.asc crate-5.10.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.5.tar.gz.asc     && tar -xf crate-5.10.5.tar.gz -C /crate --strip-components=1     && rm crate-5.10.5.tar.gz # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 09:26:14 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 28 Apr 2025 09:26:14 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
VOLUME [/data]
# Mon, 28 Apr 2025 09:26:14 GMT
WORKDIR /data
# Mon, 28 Apr 2025 09:26:14 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 28 Apr 2025 09:26:14 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-28T09:26:14.692678 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.5
# Mon, 28 Apr 2025 09:26:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 09:26:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Apr 2025 09:26:14 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Thu, 08 May 2025 18:32:32 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9379fff095e8fe20a8323fa2556b6639feedf28f54e6be52bf0e56969e38f73`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 30.2 MB (30200753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b8a277ffd5ff23a1ecafe738e7734168280b78c7725c4df5837bc913fea7df`  
		Last Modified: Fri, 09 May 2025 16:04:43 GMT  
		Size: 150.3 MB (150337193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cde2427af5eabd2a52fbcc43ee0be7daf3e6f6bc874623cbb8c35fea77ca1f7`  
		Last Modified: Fri, 09 May 2025 16:02:40 GMT  
		Size: 1.9 MB (1943640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5062da19457d2b883573ba218232a1f97f6d7318c2b5fa6841c3493178b057`  
		Last Modified: Fri, 09 May 2025 16:02:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8fef20f563ad4d561167a82628b3ec1eaf7ffa04fc8f3efc6caabc5f4f286`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ba9e5c50e1fa090415ff9766e6df54863fa64541525f10875eb88f40834ac`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626c91d1033af3ad5fae5e63fe8c9e8403c27557c40ccb3fcece4ab1ecfdb9c2`  
		Last Modified: Fri, 09 May 2025 16:04:35 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:642301bf5c40179e36f06908124a4633e5cc72fd304ed767029f2e6a399b4c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f434f4273f801d29848a0bbf504be6b9bcb8e410223cca9692545ca0529e41f4`

```dockerfile
```

-	Layers:
	-	`sha256:33ffecd0be028f2ff8ec63a420edac9927cbf614b4ea216b424432d87b647352`  
		Last Modified: Wed, 30 Apr 2025 17:05:06 GMT  
		Size: 5.2 MB (5166691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb1bc32937011b4a8ca77800787879b9761e3d8f992b5712adf4e68c4a2a924`  
		Last Modified: Wed, 30 Apr 2025 17:05:05 GMT  
		Size: 23.3 KB (23337 bytes)  
		MIME: application/vnd.in-toto+json
