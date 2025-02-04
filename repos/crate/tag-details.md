<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.7`](#crate57)
-	[`crate:5.7.6`](#crate576)
-	[`crate:5.8`](#crate58)
-	[`crate:5.8.6`](#crate586)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.9`](#crate599)
-	[`crate:latest`](#cratelatest)

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
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254467af6af8d54539de364df9914c81db0a46c2098bc5db770cefa342042c82`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 14.1 MB (14148802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec741d4522fe5273ce35453c5fc8c676906dbb3204c97f4b127dee2dbb8fe912`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 127.3 MB (127300400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e6024f4229768049397eeaf4c4a330900415b5b2b69ec7017c98d007813582`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b41076b4a31aeb711bf08ad6dfed385041e4d1d536e4b7159b26ca64787741`  
		Last Modified: Mon, 03 Feb 2025 22:27:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd0c0376a2c568adb60c69c40f36eee4b01d34d554de3463fe6517f0fe2267`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e46437bde054233098392d9cc0a0f5c2fb62ba462f57ed67117fee0f14a6a56`  
		Last Modified: Mon, 03 Feb 2025 22:27:54 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c3357cb43370f7a2c4ed8039390cb22268c72b5a7f7dc2b029adbe14a63479`  
		Last Modified: Mon, 03 Feb 2025 22:27:54 GMT  
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
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a694484b4f2b3cc627b9a4633882816f10897352a8cf82a335c5f7bc1daa1`  
		Last Modified: Mon, 03 Feb 2025 22:29:15 GMT  
		Size: 126.9 MB (126862648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c1120ca3977821758c69f8b6b8b977bde97b00c8913de6189dcab3ad3e6d95`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522051da5393eb1667d5e5c8942b273ea9500a2c6f39ba2f6a09855bb8e8768e`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793fd747b95fce4bc57e63c7697e08194f17e0deb3cc48fb00012854049f2a7`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9c7b8b1a09e8fa4f0e8e349e3aa8455b092e7767e2ced9b5d4a8adeb994e8`  
		Last Modified: Mon, 03 Feb 2025 22:29:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612f1530af53fd7cb71104d96227621a0bdd8ab331c380554144c1b5227708c`  
		Last Modified: Mon, 03 Feb 2025 22:29:13 GMT  
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
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254467af6af8d54539de364df9914c81db0a46c2098bc5db770cefa342042c82`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 14.1 MB (14148802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec741d4522fe5273ce35453c5fc8c676906dbb3204c97f4b127dee2dbb8fe912`  
		Last Modified: Mon, 03 Feb 2025 22:27:56 GMT  
		Size: 127.3 MB (127300400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e6024f4229768049397eeaf4c4a330900415b5b2b69ec7017c98d007813582`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b41076b4a31aeb711bf08ad6dfed385041e4d1d536e4b7159b26ca64787741`  
		Last Modified: Mon, 03 Feb 2025 22:27:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd0c0376a2c568adb60c69c40f36eee4b01d34d554de3463fe6517f0fe2267`  
		Last Modified: Mon, 03 Feb 2025 22:27:53 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e46437bde054233098392d9cc0a0f5c2fb62ba462f57ed67117fee0f14a6a56`  
		Last Modified: Mon, 03 Feb 2025 22:27:54 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c3357cb43370f7a2c4ed8039390cb22268c72b5a7f7dc2b029adbe14a63479`  
		Last Modified: Mon, 03 Feb 2025 22:27:54 GMT  
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
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a694484b4f2b3cc627b9a4633882816f10897352a8cf82a335c5f7bc1daa1`  
		Last Modified: Mon, 03 Feb 2025 22:29:15 GMT  
		Size: 126.9 MB (126862648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c1120ca3977821758c69f8b6b8b977bde97b00c8913de6189dcab3ad3e6d95`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522051da5393eb1667d5e5c8942b273ea9500a2c6f39ba2f6a09855bb8e8768e`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793fd747b95fce4bc57e63c7697e08194f17e0deb3cc48fb00012854049f2a7`  
		Last Modified: Mon, 03 Feb 2025 22:29:12 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9c7b8b1a09e8fa4f0e8e349e3aa8455b092e7767e2ced9b5d4a8adeb994e8`  
		Last Modified: Mon, 03 Feb 2025 22:29:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612f1530af53fd7cb71104d96227621a0bdd8ab331c380554144c1b5227708c`  
		Last Modified: Mon, 03 Feb 2025 22:29:13 GMT  
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
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf9946c1bea126dd289995cb9fe4ee972e362c34682631c30c2c21bd2e6ecc`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 14.1 MB (14148854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac03f18a4b6f7343ab9933dfa5bc4b782cf73b2875a1abfe5cbf4766256e625`  
		Last Modified: Mon, 03 Feb 2025 22:27:14 GMT  
		Size: 130.0 MB (129965335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985fe587a198cb5e064002316fb9cd22c6b30ab1ac82a4075edf8d479f2f7cc`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2928f35de96488de94410e8fddd3e70f485f29c816a279087908b554e8cc706d`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa264a761fd1fed3689fa5ab9867f3702f4061afd2b7e0d854e800da33c7f1c`  
		Last Modified: Mon, 03 Feb 2025 22:27:13 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae068b8169ea2d576728ae29925f19164bd80dbd5f6a09a4191e018a0e64db`  
		Last Modified: Mon, 03 Feb 2025 22:27:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b284bef0d222ffade4d31491dac20a13ce7059bd59244b308f5417b2eb3a4d`  
		Last Modified: Mon, 03 Feb 2025 22:27:13 GMT  
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
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925575c4ad696b0392b1e5623678226cf327e83ef5dd77249f56efb83e08db7f`  
		Last Modified: Mon, 03 Feb 2025 22:28:22 GMT  
		Size: 129.4 MB (129412881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f56b72c56eaef6be6c960e2edbdd52131ca0d785fe2814fd0cc98c348a0842`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17da6553dd1a472e3daefd9753b66f5290c055c25008fa3b9d21847fdebeb16`  
		Last Modified: Mon, 03 Feb 2025 22:28:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768bb6ba7c924dd6d4374c154c75f42b420500db97f26e46ad78a44d93dacac6`  
		Last Modified: Mon, 03 Feb 2025 22:28:19 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3da709d79ed5b345bf3ae95fab349ffc4f3ee6f5a0af717d96c5e95b6e3cf81`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e86115430a3330e27af6bbd3793fa03f403720f84d0ec347f31d85d18709094`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
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
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf9946c1bea126dd289995cb9fe4ee972e362c34682631c30c2c21bd2e6ecc`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 14.1 MB (14148854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac03f18a4b6f7343ab9933dfa5bc4b782cf73b2875a1abfe5cbf4766256e625`  
		Last Modified: Mon, 03 Feb 2025 22:27:14 GMT  
		Size: 130.0 MB (129965335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985fe587a198cb5e064002316fb9cd22c6b30ab1ac82a4075edf8d479f2f7cc`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2928f35de96488de94410e8fddd3e70f485f29c816a279087908b554e8cc706d`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa264a761fd1fed3689fa5ab9867f3702f4061afd2b7e0d854e800da33c7f1c`  
		Last Modified: Mon, 03 Feb 2025 22:27:13 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae068b8169ea2d576728ae29925f19164bd80dbd5f6a09a4191e018a0e64db`  
		Last Modified: Mon, 03 Feb 2025 22:27:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b284bef0d222ffade4d31491dac20a13ce7059bd59244b308f5417b2eb3a4d`  
		Last Modified: Mon, 03 Feb 2025 22:27:13 GMT  
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
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925575c4ad696b0392b1e5623678226cf327e83ef5dd77249f56efb83e08db7f`  
		Last Modified: Mon, 03 Feb 2025 22:28:22 GMT  
		Size: 129.4 MB (129412881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f56b72c56eaef6be6c960e2edbdd52131ca0d785fe2814fd0cc98c348a0842`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17da6553dd1a472e3daefd9753b66f5290c055c25008fa3b9d21847fdebeb16`  
		Last Modified: Mon, 03 Feb 2025 22:28:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768bb6ba7c924dd6d4374c154c75f42b420500db97f26e46ad78a44d93dacac6`  
		Last Modified: Mon, 03 Feb 2025 22:28:19 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3da709d79ed5b345bf3ae95fab349ffc4f3ee6f5a0af717d96c5e95b6e3cf81`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e86115430a3330e27af6bbd3793fa03f403720f84d0ec347f31d85d18709094`  
		Last Modified: Mon, 03 Feb 2025 22:28:20 GMT  
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
$ docker pull crate@sha256:850839faa80215a8b29a038c988dd0747e62ea7e3510df52f457e239c5ab549d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:1ba5e54937c1d1db134ecdd2655fbd56ec641667aa8acad563ff61f53980948d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244170273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b234a437c016e38e8e3a928f47c9a248775e45562914fe277e1bb21b9a10cc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 19:32:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 19:32:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 19:32:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 19:32:04 GMT
WORKDIR /data
# Thu, 30 Jan 2025 19:32:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Thu, 30 Jan 2025 19:32:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 19:32:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7060334d467a30abf76f403c26c6978e68eb1dee253afade4f8abc8f98e2078a`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 14.1 MB (14148819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ebda62cca6f0dcb947614bf67187402f80c36f04a03e72b6265c9d3e783b74`  
		Last Modified: Mon, 03 Feb 2025 22:27:13 GMT  
		Size: 149.0 MB (148996967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd47a8b1a61b4557d9a2e3f002b47a448a1557f4eea0a4c016f3e826e2f17aba`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2c3ad2ed65a24166b34852cf95401b7fb2e1983f9b8329dcaff45d73bbbae`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad29c4cd7982e452a57e6c160f9b943bdad6303b318f834f8ef82c543443fe`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e714bcfa52cdeef2bd8d00fbba66e4afb0ebbb7eb31ea6eab55e3d4173d3ff8`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a87ece2581a25ceac97e033fe9b427a1010e7b3361c3d1cdeaa91075180416`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:73841a5349bab56e524671624aa1727ba0d1a32062d16cdd1feafc4b14dbdbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5ba6f7b03195cb09f4e90990eaa3e4ae7a6b3381a223935701ed8e05f86ddf`

```dockerfile
```

-	Layers:
	-	`sha256:cf4aa7ff6d7a1a14793839d40a91544682a7002503ad0492ddce4c38772b6eee`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 6.3 MB (6316964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf4ec2c5b682b1447250b7ad74f7f75dfb27a12af1995bf1513a3ecec74530f`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:30201f153126607fb466f6062de51aa7ba01e1eac12cf238c41a196d86c2a7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243815460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1790a544fcd415f90d06371703e357a3500c9d0127cc8c00a667bcd6a3809980`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 19:32:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 19:32:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 19:32:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 19:32:04 GMT
WORKDIR /data
# Thu, 30 Jan 2025 19:32:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Thu, 30 Jan 2025 19:32:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 19:32:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bf66707dec5d2f82653b4f7ad51c4b46c113a5930d3532722479bc31847cd5`  
		Last Modified: Mon, 03 Feb 2025 22:27:29 GMT  
		Size: 149.7 MB (149687597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d0278053e13a27449c91e368e120bf6fa6842897388d1d651f4edb18f96e7b`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a653373af6a4a7ec4cea106f86c52bbbb5e6819dfd9f8265398118ae042f0f`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb68f6c4f4f387e18f87c165558344046a9e58dd877ffe74bd0fb511f139749`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105347481c8c898094aa850a0f019f6926512a61baf19d7f61b742f652a4938a`  
		Last Modified: Mon, 03 Feb 2025 22:27:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7019449f77e61bd4bbf83ce34d78312b9500e49668ea6ebe9f81e6b172ea2342`  
		Last Modified: Mon, 03 Feb 2025 22:27:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:9700867d68cbbffa10d4502142ac51ea46ae6500fa26850b6aa496642c7c2203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6336932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287070fee01c3e2b9a337b55de5cf48d3520d795768882dd1d1224fd0da7cc9f`

```dockerfile
```

-	Layers:
	-	`sha256:a2251b91a1ef059c18ec3ce320d1b27d6a011d11bf0a548ff571b5aa631e6e52`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 6.3 MB (6313673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbf6c337d142e87d995ee0e26cec41b0f40a07b05f1d07cb7d140f8a67ab53b8`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 23.3 KB (23259 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.9`

```console
$ docker pull crate@sha256:850839faa80215a8b29a038c988dd0747e62ea7e3510df52f457e239c5ab549d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.9` - linux; amd64

```console
$ docker pull crate@sha256:1ba5e54937c1d1db134ecdd2655fbd56ec641667aa8acad563ff61f53980948d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244170273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b234a437c016e38e8e3a928f47c9a248775e45562914fe277e1bb21b9a10cc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 19:32:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 19:32:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 19:32:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 19:32:04 GMT
WORKDIR /data
# Thu, 30 Jan 2025 19:32:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Thu, 30 Jan 2025 19:32:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 19:32:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7060334d467a30abf76f403c26c6978e68eb1dee253afade4f8abc8f98e2078a`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 14.1 MB (14148819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ebda62cca6f0dcb947614bf67187402f80c36f04a03e72b6265c9d3e783b74`  
		Last Modified: Mon, 03 Feb 2025 22:27:13 GMT  
		Size: 149.0 MB (148996967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd47a8b1a61b4557d9a2e3f002b47a448a1557f4eea0a4c016f3e826e2f17aba`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2c3ad2ed65a24166b34852cf95401b7fb2e1983f9b8329dcaff45d73bbbae`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad29c4cd7982e452a57e6c160f9b943bdad6303b318f834f8ef82c543443fe`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e714bcfa52cdeef2bd8d00fbba66e4afb0ebbb7eb31ea6eab55e3d4173d3ff8`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a87ece2581a25ceac97e033fe9b427a1010e7b3361c3d1cdeaa91075180416`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.9` - unknown; unknown

```console
$ docker pull crate@sha256:73841a5349bab56e524671624aa1727ba0d1a32062d16cdd1feafc4b14dbdbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5ba6f7b03195cb09f4e90990eaa3e4ae7a6b3381a223935701ed8e05f86ddf`

```dockerfile
```

-	Layers:
	-	`sha256:cf4aa7ff6d7a1a14793839d40a91544682a7002503ad0492ddce4c38772b6eee`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 6.3 MB (6316964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf4ec2c5b682b1447250b7ad74f7f75dfb27a12af1995bf1513a3ecec74530f`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:30201f153126607fb466f6062de51aa7ba01e1eac12cf238c41a196d86c2a7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243815460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1790a544fcd415f90d06371703e357a3500c9d0127cc8c00a667bcd6a3809980`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 19:32:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 19:32:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 19:32:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 19:32:04 GMT
WORKDIR /data
# Thu, 30 Jan 2025 19:32:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Thu, 30 Jan 2025 19:32:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 19:32:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bf66707dec5d2f82653b4f7ad51c4b46c113a5930d3532722479bc31847cd5`  
		Last Modified: Mon, 03 Feb 2025 22:27:29 GMT  
		Size: 149.7 MB (149687597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d0278053e13a27449c91e368e120bf6fa6842897388d1d651f4edb18f96e7b`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a653373af6a4a7ec4cea106f86c52bbbb5e6819dfd9f8265398118ae042f0f`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb68f6c4f4f387e18f87c165558344046a9e58dd877ffe74bd0fb511f139749`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105347481c8c898094aa850a0f019f6926512a61baf19d7f61b742f652a4938a`  
		Last Modified: Mon, 03 Feb 2025 22:27:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7019449f77e61bd4bbf83ce34d78312b9500e49668ea6ebe9f81e6b172ea2342`  
		Last Modified: Mon, 03 Feb 2025 22:27:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.9` - unknown; unknown

```console
$ docker pull crate@sha256:9700867d68cbbffa10d4502142ac51ea46ae6500fa26850b6aa496642c7c2203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6336932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287070fee01c3e2b9a337b55de5cf48d3520d795768882dd1d1224fd0da7cc9f`

```dockerfile
```

-	Layers:
	-	`sha256:a2251b91a1ef059c18ec3ce320d1b27d6a011d11bf0a548ff571b5aa631e6e52`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 6.3 MB (6313673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbf6c337d142e87d995ee0e26cec41b0f40a07b05f1d07cb7d140f8a67ab53b8`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 23.3 KB (23259 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:850839faa80215a8b29a038c988dd0747e62ea7e3510df52f457e239c5ab549d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:1ba5e54937c1d1db134ecdd2655fbd56ec641667aa8acad563ff61f53980948d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244170273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b234a437c016e38e8e3a928f47c9a248775e45562914fe277e1bb21b9a10cc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 19:32:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 19:32:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 19:32:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 19:32:04 GMT
WORKDIR /data
# Thu, 30 Jan 2025 19:32:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Thu, 30 Jan 2025 19:32:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 19:32:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7060334d467a30abf76f403c26c6978e68eb1dee253afade4f8abc8f98e2078a`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 14.1 MB (14148819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ebda62cca6f0dcb947614bf67187402f80c36f04a03e72b6265c9d3e783b74`  
		Last Modified: Mon, 03 Feb 2025 22:27:13 GMT  
		Size: 149.0 MB (148996967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd47a8b1a61b4557d9a2e3f002b47a448a1557f4eea0a4c016f3e826e2f17aba`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2c3ad2ed65a24166b34852cf95401b7fb2e1983f9b8329dcaff45d73bbbae`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad29c4cd7982e452a57e6c160f9b943bdad6303b318f834f8ef82c543443fe`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e714bcfa52cdeef2bd8d00fbba66e4afb0ebbb7eb31ea6eab55e3d4173d3ff8`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a87ece2581a25ceac97e033fe9b427a1010e7b3361c3d1cdeaa91075180416`  
		Last Modified: Mon, 03 Feb 2025 22:27:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:73841a5349bab56e524671624aa1727ba0d1a32062d16cdd1feafc4b14dbdbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5ba6f7b03195cb09f4e90990eaa3e4ae7a6b3381a223935701ed8e05f86ddf`

```dockerfile
```

-	Layers:
	-	`sha256:cf4aa7ff6d7a1a14793839d40a91544682a7002503ad0492ddce4c38772b6eee`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 6.3 MB (6316964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf4ec2c5b682b1447250b7ad74f7f75dfb27a12af1995bf1513a3ecec74530f`  
		Last Modified: Mon, 03 Feb 2025 22:27:11 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:30201f153126607fb466f6062de51aa7ba01e1eac12cf238c41a196d86c2a7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243815460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1790a544fcd415f90d06371703e357a3500c9d0127cc8c00a667bcd6a3809980`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 19:32:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 19:32:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 Jan 2025 19:32:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
VOLUME [/data]
# Thu, 30 Jan 2025 19:32:04 GMT
WORKDIR /data
# Thu, 30 Jan 2025 19:32:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Thu, 30 Jan 2025 19:32:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 30 Jan 2025 19:32:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Jan 2025 19:32:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5286574881d2889f37ff9fd12d49a1c878f36710954a166299b77d0a51e7b1fa`  
		Last Modified: Mon, 18 Nov 2024 21:41:04 GMT  
		Size: 78.0 MB (77988775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e54b9774d98e43ef136991e64eb6d2c2dc39dd9d1fa40c61b048c89868bce5`  
		Last Modified: Wed, 15 Jan 2025 01:26:04 GMT  
		Size: 14.2 MB (14193579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bf66707dec5d2f82653b4f7ad51c4b46c113a5930d3532722479bc31847cd5`  
		Last Modified: Mon, 03 Feb 2025 22:27:29 GMT  
		Size: 149.7 MB (149687597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d0278053e13a27449c91e368e120bf6fa6842897388d1d651f4edb18f96e7b`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a653373af6a4a7ec4cea106f86c52bbbb5e6819dfd9f8265398118ae042f0f`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb68f6c4f4f387e18f87c165558344046a9e58dd877ffe74bd0fb511f139749`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105347481c8c898094aa850a0f019f6926512a61baf19d7f61b742f652a4938a`  
		Last Modified: Mon, 03 Feb 2025 22:27:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7019449f77e61bd4bbf83ce34d78312b9500e49668ea6ebe9f81e6b172ea2342`  
		Last Modified: Mon, 03 Feb 2025 22:27:26 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:9700867d68cbbffa10d4502142ac51ea46ae6500fa26850b6aa496642c7c2203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6336932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287070fee01c3e2b9a337b55de5cf48d3520d795768882dd1d1224fd0da7cc9f`

```dockerfile
```

-	Layers:
	-	`sha256:a2251b91a1ef059c18ec3ce320d1b27d6a011d11bf0a548ff571b5aa631e6e52`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 6.3 MB (6313673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbf6c337d142e87d995ee0e26cec41b0f40a07b05f1d07cb7d140f8a67ab53b8`  
		Last Modified: Mon, 03 Feb 2025 22:27:25 GMT  
		Size: 23.3 KB (23259 bytes)  
		MIME: application/vnd.in-toto+json
