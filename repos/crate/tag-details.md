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
$ docker pull crate@sha256:1f6816f5c39d3b865c7f94c671e42e30d66c8f34d51f3ba799a1bcb25a546fa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:8b7b1f58fe55555fe6c27580012e7166da949791a3b2363a7fbed32263ff5afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225587992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8987540d01d4c5fed65e7dcb5862181f2d2d164e7b2b9c0ef4a689ccd70953f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:44:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 08:44:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 10 Feb 2025 08:44:00 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
VOLUME [/data]
# Mon, 10 Feb 2025 08:44:00 GMT
WORKDIR /data
# Mon, 10 Feb 2025 08:44:00 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Mon, 10 Feb 2025 08:44:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 10 Feb 2025 08:44:00 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Wed, 05 Feb 2025 05:27:15 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea820d27945f005c9b69d8ea92c4d0f25000dbb156b37791997bdfcd1c2e758d`  
		Last Modified: Tue, 11 Feb 2025 01:30:55 GMT  
		Size: 8.6 MB (8641009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb94d7b414e90c3f3871c601e95dca0ab4c687019a8f6ed661b404160e125b89`  
		Last Modified: Tue, 11 Feb 2025 02:43:30 GMT  
		Size: 149.0 MB (148996947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ed03b326d3bc5453c227aab6e5e82ac1dbc3a2c4c5c109498962271f6b51fa`  
		Last Modified: Tue, 11 Feb 2025 02:43:26 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9c1238e4795e0d98e3cb48ab3eb88a837f55e633c3c74e22130edd53dd71b8`  
		Last Modified: Tue, 11 Feb 2025 02:43:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549898892dd789312dbb226526fbbbce45a36e56553f8e9d483e1feff3513b75`  
		Last Modified: Tue, 11 Feb 2025 00:26:49 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c0dd267949f90795ff3df18a49f652e866b76bc11bfa0fce7edb294a831200`  
		Last Modified: Tue, 11 Feb 2025 00:26:49 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2c25f69192d2ca449a82b47af0874c4c90e4ce17c43b56d29375484d180155`  
		Last Modified: Tue, 11 Feb 2025 00:26:49 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:8e83aa4774d6bf08aff9e6c226d5f1389fc81bcf6dfd5a98764021d786fe7e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4956951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9fd44027d3ed4dad675b2220c452dd494560ac5ae290e926a2ee31d2eb031c`

```dockerfile
```

-	Layers:
	-	`sha256:33ed25fd9c1ae691b5808f96552bc61a25dd333a8f773f42e367e231f6a63e9c`  
		Last Modified: Tue, 11 Feb 2025 09:01:27 GMT  
		Size: 4.9 MB (4933803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429978fb91b1e230ccce23c7093ab02a71ba2e7f4251636c1f37b970185e325d`  
		Last Modified: Tue, 11 Feb 2025 09:01:28 GMT  
		Size: 23.1 KB (23148 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7152cd082dadfe9880b30fca4977a0e8e0ee6201d3396bbb1c0dd50dea01c370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224783381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ba384a8598dfbde66199cd54768a3a74adcae5f260e746de73b6df3aba79e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:44:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 08:44:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 10 Feb 2025 08:44:00 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
VOLUME [/data]
# Mon, 10 Feb 2025 08:44:00 GMT
WORKDIR /data
# Mon, 10 Feb 2025 08:44:00 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Mon, 10 Feb 2025 08:44:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 10 Feb 2025 08:44:00 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 08:45:30 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364d81053736e60664dd73f5fa40a3119061bfd28e2a6d7746e2c2b5c402473`  
		Last Modified: Tue, 11 Feb 2025 13:59:05 GMT  
		Size: 8.5 MB (8507487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994e666de53f6a0d7b941b198543193843f071b5a81f8a25c373af4717073967`  
		Last Modified: Tue, 11 Feb 2025 13:59:12 GMT  
		Size: 149.7 MB (149687547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c55549a65b64e8806ef82c60d44ecfa53007806e1533892aa4b7a798c8d114`  
		Last Modified: Tue, 11 Feb 2025 13:59:05 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe24f776894e710210bff9cc21a6b95e0719b9c9ca7561dda8b787c539c2f92`  
		Last Modified: Tue, 11 Feb 2025 16:29:52 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff522f4f011ecb5a1cea8e09d7482e47a7371d12951640c74630357c68175e74`  
		Last Modified: Tue, 11 Feb 2025 13:59:04 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059112c53f3bfce0913ad3b97c4f5dff28032a6ded3eef0a21dfad33212c1d4a`  
		Last Modified: Tue, 11 Feb 2025 13:59:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1727e2af351e578d8be45c5baa9d9c876dd9a5af5cd65eaec813de5f43f224`  
		Last Modified: Tue, 11 Feb 2025 16:29:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:ae9423f2aa0086ac220e3ac6f6d55aa5860551fbff38de6a470ad80afabbdfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4954396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbbcaa609c19623f5a1495d54943430a79663eb69d1377c892052af02e52fed`

```dockerfile
```

-	Layers:
	-	`sha256:d63cc8a97cc469bd347755def0bd69075da044166273e146148f6538eb7f2829`  
		Last Modified: Wed, 12 Feb 2025 05:40:40 GMT  
		Size: 4.9 MB (4931111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3496621dc0af8e511b556f80cdf1273e44f61a8dbda89091c0e93dc41459470f`  
		Last Modified: Mon, 10 Feb 2025 23:27:55 GMT  
		Size: 23.3 KB (23285 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.9`

```console
$ docker pull crate@sha256:1f6816f5c39d3b865c7f94c671e42e30d66c8f34d51f3ba799a1bcb25a546fa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.9` - linux; amd64

```console
$ docker pull crate@sha256:8b7b1f58fe55555fe6c27580012e7166da949791a3b2363a7fbed32263ff5afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225587992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8987540d01d4c5fed65e7dcb5862181f2d2d164e7b2b9c0ef4a689ccd70953f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:44:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 08:44:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 10 Feb 2025 08:44:00 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
VOLUME [/data]
# Mon, 10 Feb 2025 08:44:00 GMT
WORKDIR /data
# Mon, 10 Feb 2025 08:44:00 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Mon, 10 Feb 2025 08:44:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 10 Feb 2025 08:44:00 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Wed, 05 Feb 2025 05:27:15 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea820d27945f005c9b69d8ea92c4d0f25000dbb156b37791997bdfcd1c2e758d`  
		Last Modified: Tue, 11 Feb 2025 01:30:55 GMT  
		Size: 8.6 MB (8641009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb94d7b414e90c3f3871c601e95dca0ab4c687019a8f6ed661b404160e125b89`  
		Last Modified: Tue, 11 Feb 2025 02:43:30 GMT  
		Size: 149.0 MB (148996947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ed03b326d3bc5453c227aab6e5e82ac1dbc3a2c4c5c109498962271f6b51fa`  
		Last Modified: Tue, 11 Feb 2025 02:43:26 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9c1238e4795e0d98e3cb48ab3eb88a837f55e633c3c74e22130edd53dd71b8`  
		Last Modified: Tue, 11 Feb 2025 02:43:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549898892dd789312dbb226526fbbbce45a36e56553f8e9d483e1feff3513b75`  
		Last Modified: Tue, 11 Feb 2025 00:26:49 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c0dd267949f90795ff3df18a49f652e866b76bc11bfa0fce7edb294a831200`  
		Last Modified: Tue, 11 Feb 2025 00:26:49 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2c25f69192d2ca449a82b47af0874c4c90e4ce17c43b56d29375484d180155`  
		Last Modified: Tue, 11 Feb 2025 00:26:49 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.9` - unknown; unknown

```console
$ docker pull crate@sha256:8e83aa4774d6bf08aff9e6c226d5f1389fc81bcf6dfd5a98764021d786fe7e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4956951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9fd44027d3ed4dad675b2220c452dd494560ac5ae290e926a2ee31d2eb031c`

```dockerfile
```

-	Layers:
	-	`sha256:33ed25fd9c1ae691b5808f96552bc61a25dd333a8f773f42e367e231f6a63e9c`  
		Last Modified: Tue, 11 Feb 2025 09:01:27 GMT  
		Size: 4.9 MB (4933803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429978fb91b1e230ccce23c7093ab02a71ba2e7f4251636c1f37b970185e325d`  
		Last Modified: Tue, 11 Feb 2025 09:01:28 GMT  
		Size: 23.1 KB (23148 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7152cd082dadfe9880b30fca4977a0e8e0ee6201d3396bbb1c0dd50dea01c370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224783381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ba384a8598dfbde66199cd54768a3a74adcae5f260e746de73b6df3aba79e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:44:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 08:44:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 10 Feb 2025 08:44:00 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
VOLUME [/data]
# Mon, 10 Feb 2025 08:44:00 GMT
WORKDIR /data
# Mon, 10 Feb 2025 08:44:00 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Mon, 10 Feb 2025 08:44:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 10 Feb 2025 08:44:00 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 08:45:30 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364d81053736e60664dd73f5fa40a3119061bfd28e2a6d7746e2c2b5c402473`  
		Last Modified: Tue, 11 Feb 2025 13:59:05 GMT  
		Size: 8.5 MB (8507487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994e666de53f6a0d7b941b198543193843f071b5a81f8a25c373af4717073967`  
		Last Modified: Tue, 11 Feb 2025 13:59:12 GMT  
		Size: 149.7 MB (149687547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c55549a65b64e8806ef82c60d44ecfa53007806e1533892aa4b7a798c8d114`  
		Last Modified: Tue, 11 Feb 2025 13:59:05 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe24f776894e710210bff9cc21a6b95e0719b9c9ca7561dda8b787c539c2f92`  
		Last Modified: Tue, 11 Feb 2025 16:29:52 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff522f4f011ecb5a1cea8e09d7482e47a7371d12951640c74630357c68175e74`  
		Last Modified: Tue, 11 Feb 2025 13:59:04 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059112c53f3bfce0913ad3b97c4f5dff28032a6ded3eef0a21dfad33212c1d4a`  
		Last Modified: Tue, 11 Feb 2025 13:59:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1727e2af351e578d8be45c5baa9d9c876dd9a5af5cd65eaec813de5f43f224`  
		Last Modified: Tue, 11 Feb 2025 16:29:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.9` - unknown; unknown

```console
$ docker pull crate@sha256:ae9423f2aa0086ac220e3ac6f6d55aa5860551fbff38de6a470ad80afabbdfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4954396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbbcaa609c19623f5a1495d54943430a79663eb69d1377c892052af02e52fed`

```dockerfile
```

-	Layers:
	-	`sha256:d63cc8a97cc469bd347755def0bd69075da044166273e146148f6538eb7f2829`  
		Last Modified: Wed, 12 Feb 2025 05:40:40 GMT  
		Size: 4.9 MB (4931111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3496621dc0af8e511b556f80cdf1273e44f61a8dbda89091c0e93dc41459470f`  
		Last Modified: Mon, 10 Feb 2025 23:27:55 GMT  
		Size: 23.3 KB (23285 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:1f6816f5c39d3b865c7f94c671e42e30d66c8f34d51f3ba799a1bcb25a546fa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:8b7b1f58fe55555fe6c27580012e7166da949791a3b2363a7fbed32263ff5afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225587992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8987540d01d4c5fed65e7dcb5862181f2d2d164e7b2b9c0ef4a689ccd70953f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:44:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 08:44:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 10 Feb 2025 08:44:00 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
VOLUME [/data]
# Mon, 10 Feb 2025 08:44:00 GMT
WORKDIR /data
# Mon, 10 Feb 2025 08:44:00 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Mon, 10 Feb 2025 08:44:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 10 Feb 2025 08:44:00 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Wed, 05 Feb 2025 05:27:15 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea820d27945f005c9b69d8ea92c4d0f25000dbb156b37791997bdfcd1c2e758d`  
		Last Modified: Tue, 11 Feb 2025 01:30:55 GMT  
		Size: 8.6 MB (8641009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb94d7b414e90c3f3871c601e95dca0ab4c687019a8f6ed661b404160e125b89`  
		Last Modified: Tue, 11 Feb 2025 02:43:30 GMT  
		Size: 149.0 MB (148996947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ed03b326d3bc5453c227aab6e5e82ac1dbc3a2c4c5c109498962271f6b51fa`  
		Last Modified: Tue, 11 Feb 2025 02:43:26 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9c1238e4795e0d98e3cb48ab3eb88a837f55e633c3c74e22130edd53dd71b8`  
		Last Modified: Tue, 11 Feb 2025 02:43:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549898892dd789312dbb226526fbbbce45a36e56553f8e9d483e1feff3513b75`  
		Last Modified: Tue, 11 Feb 2025 00:26:49 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c0dd267949f90795ff3df18a49f652e866b76bc11bfa0fce7edb294a831200`  
		Last Modified: Tue, 11 Feb 2025 00:26:49 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2c25f69192d2ca449a82b47af0874c4c90e4ce17c43b56d29375484d180155`  
		Last Modified: Tue, 11 Feb 2025 00:26:49 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:8e83aa4774d6bf08aff9e6c226d5f1389fc81bcf6dfd5a98764021d786fe7e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4956951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9fd44027d3ed4dad675b2220c452dd494560ac5ae290e926a2ee31d2eb031c`

```dockerfile
```

-	Layers:
	-	`sha256:33ed25fd9c1ae691b5808f96552bc61a25dd333a8f773f42e367e231f6a63e9c`  
		Last Modified: Tue, 11 Feb 2025 09:01:27 GMT  
		Size: 4.9 MB (4933803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429978fb91b1e230ccce23c7093ab02a71ba2e7f4251636c1f37b970185e325d`  
		Last Modified: Tue, 11 Feb 2025 09:01:28 GMT  
		Size: 23.1 KB (23148 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7152cd082dadfe9880b30fca4977a0e8e0ee6201d3396bbb1c0dd50dea01c370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224783381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ba384a8598dfbde66199cd54768a3a74adcae5f260e746de73b6df3aba79e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:44:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.9.tar.gz.asc crate-5.9.9.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.9.tar.gz.asc     && tar -xf crate-5.9.9.tar.gz -C /crate --strip-components=1     && rm crate-5.9.9.tar.gz # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 08:44:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 10 Feb 2025 08:44:00 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
VOLUME [/data]
# Mon, 10 Feb 2025 08:44:00 GMT
WORKDIR /data
# Mon, 10 Feb 2025 08:44:00 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-30T19:32:04.698118 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.9
# Mon, 10 Feb 2025 08:44:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:44:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 10 Feb 2025 08:44:00 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 08:45:30 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364d81053736e60664dd73f5fa40a3119061bfd28e2a6d7746e2c2b5c402473`  
		Last Modified: Tue, 11 Feb 2025 13:59:05 GMT  
		Size: 8.5 MB (8507487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994e666de53f6a0d7b941b198543193843f071b5a81f8a25c373af4717073967`  
		Last Modified: Tue, 11 Feb 2025 13:59:12 GMT  
		Size: 149.7 MB (149687547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c55549a65b64e8806ef82c60d44ecfa53007806e1533892aa4b7a798c8d114`  
		Last Modified: Tue, 11 Feb 2025 13:59:05 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe24f776894e710210bff9cc21a6b95e0719b9c9ca7561dda8b787c539c2f92`  
		Last Modified: Tue, 11 Feb 2025 16:29:52 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff522f4f011ecb5a1cea8e09d7482e47a7371d12951640c74630357c68175e74`  
		Last Modified: Tue, 11 Feb 2025 13:59:04 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059112c53f3bfce0913ad3b97c4f5dff28032a6ded3eef0a21dfad33212c1d4a`  
		Last Modified: Tue, 11 Feb 2025 13:59:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1727e2af351e578d8be45c5baa9d9c876dd9a5af5cd65eaec813de5f43f224`  
		Last Modified: Tue, 11 Feb 2025 16:29:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:ae9423f2aa0086ac220e3ac6f6d55aa5860551fbff38de6a470ad80afabbdfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4954396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbbcaa609c19623f5a1495d54943430a79663eb69d1377c892052af02e52fed`

```dockerfile
```

-	Layers:
	-	`sha256:d63cc8a97cc469bd347755def0bd69075da044166273e146148f6538eb7f2829`  
		Last Modified: Wed, 12 Feb 2025 05:40:40 GMT  
		Size: 4.9 MB (4931111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3496621dc0af8e511b556f80cdf1273e44f61a8dbda89091c0e93dc41459470f`  
		Last Modified: Mon, 10 Feb 2025 23:27:55 GMT  
		Size: 23.3 KB (23285 bytes)  
		MIME: application/vnd.in-toto+json
