## `crate:latest`

```console
$ docker pull crate@sha256:1cae9c8cfe814bee7867cb643619f3e50a0349687a44aa9e4f3d3f58b03a2aed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:fd76d1b9f6a59fef3579849dcf70896b9cacffe4056f23c508a4af41d850ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233089624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01549dc152fc90ce2d01053f4f78f294e915562e5286006c28aeb9146b5bbc1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:20:33 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:20:33 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:11:03 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:11:04 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:11:04 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:11:04 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:11:04 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:11:04 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 05 Jan 2026 19:11:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:11:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:11:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:27b4a02f35e059b231a8869fb4ef82ee3ef52c7c0e3dbef81464d6b3b26922be`  
		Last Modified: Mon, 05 Jan 2026 18:21:18 GMT  
		Size: 67.5 MB (67510075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deb99bbe4a25c1266e7d6135b74aa048062ad833a5da7c4a3c1c0709761a647`  
		Last Modified: Mon, 05 Jan 2026 19:11:44 GMT  
		Size: 14.5 MB (14500482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f3eb4f912636d874a99e50ca38b6138a1046a2845df02f42ba4788e6415820`  
		Last Modified: Mon, 05 Jan 2026 19:11:56 GMT  
		Size: 149.1 MB (149133558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33126ec70617c2e99a89ab94195ba8e70459d09a3dc20f03300770642bb5dbc3`  
		Last Modified: Mon, 05 Jan 2026 19:11:22 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5587d8039e028413927960e0af3ad8eea851b7e6707aebf5e8a78eac3d868`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499414e23067d6c17cc7429e7992bc2a846203ce8eef5126556618b7c584733`  
		Last Modified: Mon, 05 Jan 2026 19:11:23 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aa3768dc6a70044c58e97e4734af0b94c2b392c939b06a0213c54d35830018`  
		Last Modified: Mon, 05 Jan 2026 19:11:42 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c72c75614345c96f74616aab3677a5588f4afbbcc4e1501f6778bcd10b0d458`  
		Last Modified: Mon, 05 Jan 2026 19:11:24 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:c60023a6b2bc8cf1613c25aa37a539981c2f18036a46edc182e28691e2f61d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00916d57213e9c242ca3931911e35cad649f74e1b171df2f62a5647d0e7aa253`

```dockerfile
```

-	Layers:
	-	`sha256:01294e1f930349abb8b726ff630f768ad6578e2f3cb0214c23069ee1b6f246b0`  
		Last Modified: Mon, 05 Jan 2026 21:38:47 GMT  
		Size: 5.2 MB (5191066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb8c597756ff70313672c657eb61bbff6632864b3d9416d59f88d6083792720`  
		Last Modified: Mon, 05 Jan 2026 21:39:06 GMT  
		Size: 23.1 KB (23140 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6f0588dd705130e20776deb2ea508469841e8d6df273c3ec9c795a79bdf83ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232299708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57bd7fcb863de98748fcfb05f98e9bf7e5156eff79f17202a3a6cc2112d8fd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 05 Jan 2026 18:21:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 05 Jan 2026 18:21:22 GMT
CMD ["/bin/bash"]
# Mon, 05 Jan 2026 19:10:37 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 05 Jan 2026 19:10:51 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 19:10:54 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 05 Jan 2026 19:10:54 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
VOLUME [/data]
# Mon, 05 Jan 2026 19:10:54 GMT
WORKDIR /data
# Mon, 05 Jan 2026 19:10:54 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 05 Jan 2026 19:10:54 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Mon, 05 Jan 2026 19:10:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 05 Jan 2026 19:10:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Jan 2026 19:10:54 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:011bf9e5e83deb6ccf3c1372474219dc8eea84d48f05953f5cfc754726740b85`  
		Last Modified: Mon, 05 Jan 2026 18:21:39 GMT  
		Size: 66.0 MB (65975452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e186f7c9f7875ae691d770756e07fe683f116fa83ac5675d95ecd2f5438b0`  
		Last Modified: Mon, 05 Jan 2026 19:11:13 GMT  
		Size: 14.6 MB (14556792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60c36734288713909bd1d362d192cdd2d9e035d0f1a328f1defd96f22fd0397`  
		Last Modified: Mon, 05 Jan 2026 19:11:56 GMT  
		Size: 149.8 MB (149821958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995b61c8be80805bcd77a5783eb3c40f15fd1a6a2eec77539b46f86622c0af9b`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22400d915397da65fea77ef50d015c6688d4187c74dc972d918e00cb87b8ac94`  
		Last Modified: Mon, 05 Jan 2026 19:11:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7929a8cb6b03858daed57ba39f3ecd54441ce49cbcd7de07869f493db5b42ba`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b3f6f90a2a7ad07dc212640ea3241bccc789273ae92bc38e7c298b7009cd57`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a03a7b43c271c70f02ec765acc240757df3f9fd90691ccad53fd2f0f0a3c2c`  
		Last Modified: Mon, 05 Jan 2026 19:11:32 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:20454104972590ecee7bfadc2e0a9c23a73bd45625e7942854a30bd94a80e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83e7da3c7e3d2c6a0feba043903912e9082dbb80860a46cc01d638bd6e54496`

```dockerfile
```

-	Layers:
	-	`sha256:24ed7c16ea6bb876f70125e1e0f702e220361e1fed5ffff77fcf79abbaa04cd5`  
		Last Modified: Mon, 05 Jan 2026 21:39:12 GMT  
		Size: 5.2 MB (5188985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:127491178df144883dfa88b10e4117be855880c9abbb59f622ef9eda55f6639e`  
		Last Modified: Mon, 05 Jan 2026 21:39:13 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
