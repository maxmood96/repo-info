<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.4`](#crate54)
-	[`crate:5.4.8`](#crate548)
-	[`crate:5.5`](#crate55)
-	[`crate:5.5.4`](#crate554)
-	[`crate:5.5.5`](#crate555)
-	[`crate:5.6`](#crate56)
-	[`crate:5.6.5`](#crate565)
-	[`crate:5.7`](#crate57)
-	[`crate:5.7.1`](#crate571)
-	[`crate:latest`](#cratelatest)

## `crate:5.4`

```console
$ docker pull crate@sha256:f3efccd94c50535bcae1f1b6fa2dede2fd506ed1fe954707b79a124fe8fc40af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4` - linux; amd64

```console
$ docker pull crate@sha256:bbefdf4ba06c24030bf051534475e1dfecbc7f489930a10ff26289a27c5f58e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300446036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0072fef66c22b253821d79867e1398eb16383c574f944d96677be8539d11ede7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Mon, 06 May 2024 18:39:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:43 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:43 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:43 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:43 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:43 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:43 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 06 May 2024 18:39:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d26ddb93039dcc46edf76bce535731e479f81e3a6c127590d47ede874ffaa`  
		Last Modified: Mon, 06 May 2024 18:41:20 GMT  
		Size: 229.6 MB (229566553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994d76ddcb7e66f097f41facfc438a1c1c1a734f664b80191aa34960f22748bc`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e413eb84a0a784d0984bdb9d65e49a77961028e8d1b1c4cbff3246c772d56762`  
		Last Modified: Mon, 06 May 2024 18:41:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6094c69e5e56b3ea58dc87a35c23cbf1bd2c5d34668c217801d902c2de26cd`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f337136039046a41bbfe342aa28e2e43b24451992b18c3e1b32bd4539df39100`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431eba8c4925bc231f3439488a4c242d876061688f2ae91ed1a66224482bfaa5`  
		Last Modified: Mon, 06 May 2024 18:41:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:87aa016580b7400b3b7eceecdb334c47ac0ace7924ec04a9ee01b5825bd9153c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297747974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d088ff841e3c98d3e147519250b4b0148c967d3567873201bfa37b0872288a1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:38:29 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Mon, 06 May 2024 19:38:33 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:38:33 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:38:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:38:33 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:38:33 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:38:33 GMT
WORKDIR /data
# Mon, 06 May 2024 19:38:33 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:38:34 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:38:34 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:38:34 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 06 May 2024 19:38:34 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:38:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:38:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2123bb96b630a9a57bdba20a03ae73029f2110dbd2ee55545be35b2989e4ce`  
		Last Modified: Mon, 06 May 2024 19:40:04 GMT  
		Size: 227.9 MB (227888432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb66280bdd7a117397c61519f29812deb826fef9fc125a5ead6ff1d77b13214`  
		Last Modified: Mon, 06 May 2024 19:39:50 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c54edabd8ed2108ac498c016520cbbc722ab3d86f6e61b31aef341d0df268a`  
		Last Modified: Mon, 06 May 2024 19:39:49 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fba01ae76af58abe1146a25e157a892741359bc34c49b0ba9d3a753cff69e1`  
		Last Modified: Mon, 06 May 2024 19:39:49 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6eaa9f6e8df29248c4dc25f46228839b962617b1dc1f8633d3145895e856917`  
		Last Modified: Mon, 06 May 2024 19:39:49 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2a221865cdd33960efe3d455905f44e86ffe7e70d6c0107def1aeabf081292`  
		Last Modified: Mon, 06 May 2024 19:39:49 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.4.8`

```console
$ docker pull crate@sha256:f3efccd94c50535bcae1f1b6fa2dede2fd506ed1fe954707b79a124fe8fc40af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.4.8` - linux; amd64

```console
$ docker pull crate@sha256:bbefdf4ba06c24030bf051534475e1dfecbc7f489930a10ff26289a27c5f58e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300446036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0072fef66c22b253821d79867e1398eb16383c574f944d96677be8539d11ede7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Mon, 06 May 2024 18:39:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:43 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:43 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:43 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:43 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:43 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:43 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:43 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 06 May 2024 18:39:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d26ddb93039dcc46edf76bce535731e479f81e3a6c127590d47ede874ffaa`  
		Last Modified: Mon, 06 May 2024 18:41:20 GMT  
		Size: 229.6 MB (229566553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994d76ddcb7e66f097f41facfc438a1c1c1a734f664b80191aa34960f22748bc`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e413eb84a0a784d0984bdb9d65e49a77961028e8d1b1c4cbff3246c772d56762`  
		Last Modified: Mon, 06 May 2024 18:41:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6094c69e5e56b3ea58dc87a35c23cbf1bd2c5d34668c217801d902c2de26cd`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f337136039046a41bbfe342aa28e2e43b24451992b18c3e1b32bd4539df39100`  
		Last Modified: Mon, 06 May 2024 18:41:02 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431eba8c4925bc231f3439488a4c242d876061688f2ae91ed1a66224482bfaa5`  
		Last Modified: Mon, 06 May 2024 18:41:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:87aa016580b7400b3b7eceecdb334c47ac0ace7924ec04a9ee01b5825bd9153c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297747974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d088ff841e3c98d3e147519250b4b0148c967d3567873201bfa37b0872288a1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:38:29 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.4.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.4.8.tar.gz.asc crate-5.4.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.4.8.tar.gz.asc     && tar -xf crate-5.4.8.tar.gz -C /crate --strip-components=1     && rm crate-5.4.8.tar.gz
# Mon, 06 May 2024 19:38:33 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:38:33 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:38:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:38:33 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:38:33 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:38:33 GMT
WORKDIR /data
# Mon, 06 May 2024 19:38:33 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:38:34 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:38:34 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:38:34 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T17:48:09.610747 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.4.8
# Mon, 06 May 2024 19:38:34 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:38:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:38:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2123bb96b630a9a57bdba20a03ae73029f2110dbd2ee55545be35b2989e4ce`  
		Last Modified: Mon, 06 May 2024 19:40:04 GMT  
		Size: 227.9 MB (227888432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb66280bdd7a117397c61519f29812deb826fef9fc125a5ead6ff1d77b13214`  
		Last Modified: Mon, 06 May 2024 19:39:50 GMT  
		Size: 1.9 MB (1939615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c54edabd8ed2108ac498c016520cbbc722ab3d86f6e61b31aef341d0df268a`  
		Last Modified: Mon, 06 May 2024 19:39:49 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fba01ae76af58abe1146a25e157a892741359bc34c49b0ba9d3a753cff69e1`  
		Last Modified: Mon, 06 May 2024 19:39:49 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6eaa9f6e8df29248c4dc25f46228839b962617b1dc1f8633d3145895e856917`  
		Last Modified: Mon, 06 May 2024 19:39:49 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2a221865cdd33960efe3d455905f44e86ffe7e70d6c0107def1aeabf081292`  
		Last Modified: Mon, 06 May 2024 19:39:49 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5`

```console
$ docker pull crate@sha256:7ac18801c020a900bf44947743b162a12313f80f88e5b5c237bcad3d5ba1f64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5` - linux; amd64

```console
$ docker pull crate@sha256:305ec522724f7af81e4cd99b722b6284b06776f1138af329bda461887c645950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187646985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5efe806570f6f11d08bc570dd7884fb07e9ce6147e42f38a7597b95db94c06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Mon, 06 May 2024 18:39:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:12 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:12 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:12 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:12 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 06 May 2024 18:39:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73053b50b5538127a1fb710a9e78631642f0fe57a18ae8fd15890c60887bf93`  
		Last Modified: Mon, 06 May 2024 18:40:51 GMT  
		Size: 116.8 MB (116767506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f053b3851702dbe8baadd6844ebdc74a8da69580c9a131e96ee9d65aedb7e4`  
		Last Modified: Mon, 06 May 2024 18:40:41 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b381b7a88b1b25b5ce0916fabdda806ec4c790412a9c9e4c0832a5da945766`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10cf788d1775ced89ff0cfe39deb33528ca4455fd23d03462a35987953beec4`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5bd70fcffa5421f6ebd6841da1069bb87c93419c1f9a2bc65f42a6ec8f4a0`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495144bfa6a9e08de71ebbf9f50c236c00e006291f737e7d8f4336377b667614`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:74067f5d036eb9a5d4242935e2269d58392d85b54fc2506ad32e701cb9893c13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186161676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93645ede94061caf4c193ac50b8a3159f243ac6e7687425dd3b5f8f5bcea4774`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:38:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Mon, 06 May 2024 19:38:03 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:38:03 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:38:03 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:38:03 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:38:03 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:38:04 GMT
WORKDIR /data
# Mon, 06 May 2024 19:38:04 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:38:04 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:38:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:38:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 06 May 2024 19:38:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:38:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:38:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431ea826ae9b2280cdc077b33d8c3a8d544ccdbbb3948dd60139e5d90ffd63f7`  
		Last Modified: Mon, 06 May 2024 19:39:39 GMT  
		Size: 116.3 MB (116302127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff36c54cdaec21e9a2fb9b7e341c50be3cf9cba9cef0c21da6db8cdd369b5f0`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 1.9 MB (1939618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95442fe2471a62ec95d8d947790046243846d41922850d089c9a44e1cfac1bf4`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1d92f66871300d2bc6d251f671cc38294b2fd538541278a30ec9f5eb4479aa`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b882dece39aa34193caa99d4bf32d5ae120120635ab12277f66f37f498bdbdb`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b211a628f97ba6702280c4da1e908a4bfb5ab48e4d55f4f9559f50f45209ab9a`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.4`

```console
$ docker pull crate@sha256:7ac18801c020a900bf44947743b162a12313f80f88e5b5c237bcad3d5ba1f64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.4` - linux; amd64

```console
$ docker pull crate@sha256:305ec522724f7af81e4cd99b722b6284b06776f1138af329bda461887c645950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187646985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5efe806570f6f11d08bc570dd7884fb07e9ce6147e42f38a7597b95db94c06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Mon, 06 May 2024 18:39:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:12 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:12 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:12 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:12 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 06 May 2024 18:39:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73053b50b5538127a1fb710a9e78631642f0fe57a18ae8fd15890c60887bf93`  
		Last Modified: Mon, 06 May 2024 18:40:51 GMT  
		Size: 116.8 MB (116767506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f053b3851702dbe8baadd6844ebdc74a8da69580c9a131e96ee9d65aedb7e4`  
		Last Modified: Mon, 06 May 2024 18:40:41 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b381b7a88b1b25b5ce0916fabdda806ec4c790412a9c9e4c0832a5da945766`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10cf788d1775ced89ff0cfe39deb33528ca4455fd23d03462a35987953beec4`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5bd70fcffa5421f6ebd6841da1069bb87c93419c1f9a2bc65f42a6ec8f4a0`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495144bfa6a9e08de71ebbf9f50c236c00e006291f737e7d8f4336377b667614`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:74067f5d036eb9a5d4242935e2269d58392d85b54fc2506ad32e701cb9893c13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186161676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93645ede94061caf4c193ac50b8a3159f243ac6e7687425dd3b5f8f5bcea4774`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:38:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Mon, 06 May 2024 19:38:03 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:38:03 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:38:03 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:38:03 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:38:03 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:38:04 GMT
WORKDIR /data
# Mon, 06 May 2024 19:38:04 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:38:04 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:38:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:38:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 06 May 2024 19:38:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:38:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:38:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431ea826ae9b2280cdc077b33d8c3a8d544ccdbbb3948dd60139e5d90ffd63f7`  
		Last Modified: Mon, 06 May 2024 19:39:39 GMT  
		Size: 116.3 MB (116302127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff36c54cdaec21e9a2fb9b7e341c50be3cf9cba9cef0c21da6db8cdd369b5f0`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 1.9 MB (1939618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95442fe2471a62ec95d8d947790046243846d41922850d089c9a44e1cfac1bf4`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1d92f66871300d2bc6d251f671cc38294b2fd538541278a30ec9f5eb4479aa`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b882dece39aa34193caa99d4bf32d5ae120120635ab12277f66f37f498bdbdb`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b211a628f97ba6702280c4da1e908a4bfb5ab48e4d55f4f9559f50f45209ab9a`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.5.5`

```console
$ docker pull crate@sha256:7ac18801c020a900bf44947743b162a12313f80f88e5b5c237bcad3d5ba1f64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.5.5` - linux; amd64

```console
$ docker pull crate@sha256:305ec522724f7af81e4cd99b722b6284b06776f1138af329bda461887c645950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187646985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5efe806570f6f11d08bc570dd7884fb07e9ce6147e42f38a7597b95db94c06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:39:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Mon, 06 May 2024 18:39:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:39:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:39:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:39:12 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:39:12 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:39:12 GMT
WORKDIR /data
# Mon, 06 May 2024 18:39:12 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:39:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:39:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 06 May 2024 18:39:12 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:39:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:39:12 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73053b50b5538127a1fb710a9e78631642f0fe57a18ae8fd15890c60887bf93`  
		Last Modified: Mon, 06 May 2024 18:40:51 GMT  
		Size: 116.8 MB (116767506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f053b3851702dbe8baadd6844ebdc74a8da69580c9a131e96ee9d65aedb7e4`  
		Last Modified: Mon, 06 May 2024 18:40:41 GMT  
		Size: 1.9 MB (1939614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b381b7a88b1b25b5ce0916fabdda806ec4c790412a9c9e4c0832a5da945766`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10cf788d1775ced89ff0cfe39deb33528ca4455fd23d03462a35987953beec4`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5bd70fcffa5421f6ebd6841da1069bb87c93419c1f9a2bc65f42a6ec8f4a0`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495144bfa6a9e08de71ebbf9f50c236c00e006291f737e7d8f4336377b667614`  
		Last Modified: Mon, 06 May 2024 18:40:40 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.5.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:74067f5d036eb9a5d4242935e2269d58392d85b54fc2506ad32e701cb9893c13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186161676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93645ede94061caf4c193ac50b8a3159f243ac6e7687425dd3b5f8f5bcea4774`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:38:00 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.5.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.5.4.tar.gz.asc crate-5.5.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.5.4.tar.gz.asc     && tar -xf crate-5.5.4.tar.gz -C /crate --strip-components=1     && rm crate-5.5.4.tar.gz
# Mon, 06 May 2024 19:38:03 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.30.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.30.2.asc crash_standalone_0.30.2     && rm -rf "$GNUPGHOME" crash_standalone_0.30.2.asc     && mv crash_standalone_0.30.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:38:03 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:38:03 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:38:03 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:38:03 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:38:04 GMT
WORKDIR /data
# Mon, 06 May 2024 19:38:04 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:38:04 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:38:04 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:38:04 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-01-29T18:39:32.739827 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.5.4
# Mon, 06 May 2024 19:38:04 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:38:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:38:04 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431ea826ae9b2280cdc077b33d8c3a8d544ccdbbb3948dd60139e5d90ffd63f7`  
		Last Modified: Mon, 06 May 2024 19:39:39 GMT  
		Size: 116.3 MB (116302127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff36c54cdaec21e9a2fb9b7e341c50be3cf9cba9cef0c21da6db8cdd369b5f0`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 1.9 MB (1939618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95442fe2471a62ec95d8d947790046243846d41922850d089c9a44e1cfac1bf4`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1d92f66871300d2bc6d251f671cc38294b2fd538541278a30ec9f5eb4479aa`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b882dece39aa34193caa99d4bf32d5ae120120635ab12277f66f37f498bdbdb`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b211a628f97ba6702280c4da1e908a4bfb5ab48e4d55f4f9559f50f45209ab9a`  
		Last Modified: Mon, 06 May 2024 19:39:30 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6`

```console
$ docker pull crate@sha256:9b94dc561bb2f3adfe1a4e254e959ad46f36af230a9b66d671e38b29bbbc6d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.6` - linux; amd64

```console
$ docker pull crate@sha256:3f84b5d0d960756eb662a2b96030bb168d1b24f1ecd99dc94ec44469b318dcae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188797435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555285bc5a8c9bb5ad1a81315430bddf1f14ffd4c023c29532890aeb949c6b89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Mon, 06 May 2024 18:38:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:49 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:49 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:49 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:49 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Mon, 06 May 2024 18:38:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:49 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7929982749cf81ce40be549b5d6960bc59a4013ba224a4f611c48f2ad01f673`  
		Last Modified: Mon, 06 May 2024 18:40:31 GMT  
		Size: 117.9 MB (117916907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f891f5354b59ee2d35bb762fcc6ea2f1a6e40841b13c3a804f243d718b380e10`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 1.9 MB (1940663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c80fb2eb604a92656588693e6d63358f8811319ba52ad9b8a85be702114e73b`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a05359db030c1e7f0afcfaa2a9b31f5fa205ce1289f8b1c1c4a79556b660b4`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a37d04b4905fcf45b457566bbfff92b8cfd4d319d960e5b42c4c710b204e0e`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314a0cbaa07e760507b8b29bce57e036d67bcc0b253227712bd6c54846630e02`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:226cfdd95eb18ac6f4c83f69ab2c2d72be0aafa0aa1a66fe1540512782d79278
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187287687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8b8e82eb1bb180a78f709495198e9b038f3b0464240dd1c33c9779ee67dffb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:37:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Mon, 06 May 2024 19:37:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:37:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:37:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:37:43 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:37:43 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:37:43 GMT
WORKDIR /data
# Mon, 06 May 2024 19:37:44 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:37:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:37:44 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:37:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Mon, 06 May 2024 19:37:44 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:37:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:37:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf18ab6a191be5c98ebb709769c076ae01daadac6c80da99ad559ec8bb83c2d`  
		Last Modified: Mon, 06 May 2024 19:39:20 GMT  
		Size: 117.4 MB (117427095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe7bdae5ab2201b2ab22673c49d262d9b46e874950ab7d236e1fbd528b3ec1`  
		Last Modified: Mon, 06 May 2024 19:39:12 GMT  
		Size: 1.9 MB (1940663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856bffaaba64cafb4de1faee735344d80f2bc5f8c99b4cc44c2b3c5305d442e7`  
		Last Modified: Mon, 06 May 2024 19:39:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe725e3f2e74872e6d64bc3fca0c030c41216348a06dbd800024ecc1811afa8`  
		Last Modified: Mon, 06 May 2024 19:39:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d317414c4888ee3a7170b3c17d7b9863b589345da0a6a946b0f978d4eddbb0`  
		Last Modified: Mon, 06 May 2024 19:39:12 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c0e8c91962e44d07163268914ab0a50be393c3175540123da055d2842cc3d`  
		Last Modified: Mon, 06 May 2024 19:39:12 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.6.5`

```console
$ docker pull crate@sha256:9b94dc561bb2f3adfe1a4e254e959ad46f36af230a9b66d671e38b29bbbc6d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.6.5` - linux; amd64

```console
$ docker pull crate@sha256:3f84b5d0d960756eb662a2b96030bb168d1b24f1ecd99dc94ec44469b318dcae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188797435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555285bc5a8c9bb5ad1a81315430bddf1f14ffd4c023c29532890aeb949c6b89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Mon, 06 May 2024 18:38:48 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:48 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:48 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:49 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:49 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:49 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:49 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:49 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Mon, 06 May 2024 18:38:49 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:49 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7929982749cf81ce40be549b5d6960bc59a4013ba224a4f611c48f2ad01f673`  
		Last Modified: Mon, 06 May 2024 18:40:31 GMT  
		Size: 117.9 MB (117916907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f891f5354b59ee2d35bb762fcc6ea2f1a6e40841b13c3a804f243d718b380e10`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 1.9 MB (1940663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c80fb2eb604a92656588693e6d63358f8811319ba52ad9b8a85be702114e73b`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a05359db030c1e7f0afcfaa2a9b31f5fa205ce1289f8b1c1c4a79556b660b4`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a37d04b4905fcf45b457566bbfff92b8cfd4d319d960e5b42c4c710b204e0e`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314a0cbaa07e760507b8b29bce57e036d67bcc0b253227712bd6c54846630e02`  
		Last Modified: Mon, 06 May 2024 18:40:20 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.6.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:226cfdd95eb18ac6f4c83f69ab2c2d72be0aafa0aa1a66fe1540512782d79278
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187287687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8b8e82eb1bb180a78f709495198e9b038f3b0464240dd1c33c9779ee67dffb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:37:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.6.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.6.5.tar.gz.asc crate-5.6.5.tar.gz     && rm -rf "$GNUPGHOME" crate-5.6.5.tar.gz.asc     && tar -xf crate-5.6.5.tar.gz -C /crate --strip-components=1     && rm crate-5.6.5.tar.gz
# Mon, 06 May 2024 19:37:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:37:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:37:43 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:37:43 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:37:43 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:37:43 GMT
WORKDIR /data
# Mon, 06 May 2024 19:37:44 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:37:44 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:37:44 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:37:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T12:27:16.639553 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.6.5
# Mon, 06 May 2024 19:37:44 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:37:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:37:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf18ab6a191be5c98ebb709769c076ae01daadac6c80da99ad559ec8bb83c2d`  
		Last Modified: Mon, 06 May 2024 19:39:20 GMT  
		Size: 117.4 MB (117427095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe7bdae5ab2201b2ab22673c49d262d9b46e874950ab7d236e1fbd528b3ec1`  
		Last Modified: Mon, 06 May 2024 19:39:12 GMT  
		Size: 1.9 MB (1940663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856bffaaba64cafb4de1faee735344d80f2bc5f8c99b4cc44c2b3c5305d442e7`  
		Last Modified: Mon, 06 May 2024 19:39:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe725e3f2e74872e6d64bc3fca0c030c41216348a06dbd800024ecc1811afa8`  
		Last Modified: Mon, 06 May 2024 19:39:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d317414c4888ee3a7170b3c17d7b9863b589345da0a6a946b0f978d4eddbb0`  
		Last Modified: Mon, 06 May 2024 19:39:12 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c0e8c91962e44d07163268914ab0a50be393c3175540123da055d2842cc3d`  
		Last Modified: Mon, 06 May 2024 19:39:12 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.7`

```console
$ docker pull crate@sha256:ccec98f986b895f89b35282788b306e7173afd9d2735a29e5c7758f84bdf0a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.7` - linux; amd64

```console
$ docker pull crate@sha256:83dabc7441469caa6e83e1e5adaaabcab318fe82b02fea35e51309625083322d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198519256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e49c7bf1e21326a81f80fa8dc016eead9e979283dd38c42372b93fe02cbac2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Mon, 06 May 2024 18:38:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:28 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:28 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:28 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:28 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Mon, 06 May 2024 18:38:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ae4cd6585a7aeda6c78af5557384cc50cbd38dafd6236cda0a387eb35834d1`  
		Last Modified: Mon, 06 May 2024 18:40:08 GMT  
		Size: 127.6 MB (127638739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9295bffe45ae4b6892cabe53c93d9a4e6b66b73c34f91d92965b221ae70a85`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 1.9 MB (1940650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7d7557f0a90aaa0dcc2782e00e595f6c4373b8d782ec7c0aac38807ea09ba9`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df2c86dc8d5e047beb57343f7d55644eb508b0fcf4529401290cf33de118ebb`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12e7999be1830b41c3e148bd482b4a6971593c4bf112cc01c04d925d4241a31`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf611f39d53636e1d5fcdb95568047d8624d684617f74c5a3eb5ab8b8d5fe43`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:86511cdb45290035f218f0768a898f912ccfc2d9f3d963e5ae66e93dae713b70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197010741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50c842526bda418de7dfe5d804507e2c63a313aa046f49a8532def7dc80ad20`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:37:17 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Mon, 06 May 2024 19:37:20 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:37:20 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:37:20 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:37:20 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:37:20 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:37:20 GMT
WORKDIR /data
# Mon, 06 May 2024 19:37:21 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:37:21 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:37:21 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:37:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Mon, 06 May 2024 19:37:21 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:37:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:37:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a560cd96675d92a9a0ec274d587fc8c58bbb54d140cea9986a3cfc550f27222`  
		Last Modified: Mon, 06 May 2024 19:39:00 GMT  
		Size: 127.2 MB (127150142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4cdd9b3c858c268d4bce9a3a22d2b8e04107d506bda08a64787f090fd9ed0a`  
		Last Modified: Mon, 06 May 2024 19:38:51 GMT  
		Size: 1.9 MB (1940669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0373138e0c0eaed3556365ee536b6f4a3071da6cac6627ab2350c3ffea4e4a56`  
		Last Modified: Mon, 06 May 2024 19:38:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac1307eb5e26dd62537a53fd3ed59e0394651ea196de30001040e2e7c3f6f2`  
		Last Modified: Mon, 06 May 2024 19:38:50 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3745be2006df3d6da5b7eb78f6b8a1295e6a493720b8fca57608ce64a14d51`  
		Last Modified: Mon, 06 May 2024 19:38:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076274663acb56a83e1b01a0daa0d5f92a9965f43998ce720227b7cd035fff3`  
		Last Modified: Mon, 06 May 2024 19:38:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:5.7.1`

```console
$ docker pull crate@sha256:ccec98f986b895f89b35282788b306e7173afd9d2735a29e5c7758f84bdf0a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:5.7.1` - linux; amd64

```console
$ docker pull crate@sha256:83dabc7441469caa6e83e1e5adaaabcab318fe82b02fea35e51309625083322d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198519256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e49c7bf1e21326a81f80fa8dc016eead9e979283dd38c42372b93fe02cbac2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Mon, 06 May 2024 18:38:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:28 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:28 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:28 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:28 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Mon, 06 May 2024 18:38:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ae4cd6585a7aeda6c78af5557384cc50cbd38dafd6236cda0a387eb35834d1`  
		Last Modified: Mon, 06 May 2024 18:40:08 GMT  
		Size: 127.6 MB (127638739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9295bffe45ae4b6892cabe53c93d9a4e6b66b73c34f91d92965b221ae70a85`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 1.9 MB (1940650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7d7557f0a90aaa0dcc2782e00e595f6c4373b8d782ec7c0aac38807ea09ba9`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df2c86dc8d5e047beb57343f7d55644eb508b0fcf4529401290cf33de118ebb`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12e7999be1830b41c3e148bd482b4a6971593c4bf112cc01c04d925d4241a31`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf611f39d53636e1d5fcdb95568047d8624d684617f74c5a3eb5ab8b8d5fe43`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:5.7.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:86511cdb45290035f218f0768a898f912ccfc2d9f3d963e5ae66e93dae713b70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197010741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50c842526bda418de7dfe5d804507e2c63a313aa046f49a8532def7dc80ad20`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:37:17 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Mon, 06 May 2024 19:37:20 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:37:20 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:37:20 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:37:20 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:37:20 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:37:20 GMT
WORKDIR /data
# Mon, 06 May 2024 19:37:21 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:37:21 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:37:21 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:37:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Mon, 06 May 2024 19:37:21 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:37:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:37:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a560cd96675d92a9a0ec274d587fc8c58bbb54d140cea9986a3cfc550f27222`  
		Last Modified: Mon, 06 May 2024 19:39:00 GMT  
		Size: 127.2 MB (127150142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4cdd9b3c858c268d4bce9a3a22d2b8e04107d506bda08a64787f090fd9ed0a`  
		Last Modified: Mon, 06 May 2024 19:38:51 GMT  
		Size: 1.9 MB (1940669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0373138e0c0eaed3556365ee536b6f4a3071da6cac6627ab2350c3ffea4e4a56`  
		Last Modified: Mon, 06 May 2024 19:38:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac1307eb5e26dd62537a53fd3ed59e0394651ea196de30001040e2e7c3f6f2`  
		Last Modified: Mon, 06 May 2024 19:38:50 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3745be2006df3d6da5b7eb78f6b8a1295e6a493720b8fca57608ce64a14d51`  
		Last Modified: Mon, 06 May 2024 19:38:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076274663acb56a83e1b01a0daa0d5f92a9965f43998ce720227b7cd035fff3`  
		Last Modified: Mon, 06 May 2024 19:38:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:ccec98f986b895f89b35282788b306e7173afd9d2735a29e5c7758f84bdf0a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:83dabc7441469caa6e83e1e5adaaabcab318fe82b02fea35e51309625083322d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198519256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e49c7bf1e21326a81f80fa8dc016eead9e979283dd38c42372b93fe02cbac2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 18:31:36 GMT
ADD file:e119ad589cbd3be448b04084dc7b08a12d0a6480ffb4619e3f9addc4a4f50f86 in / 
# Mon, 06 May 2024 18:31:37 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 18:38:08 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 18:38:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Mon, 06 May 2024 18:38:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 18:38:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 18:38:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 18:38:28 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 18:38:28 GMT
VOLUME [/data]
# Mon, 06 May 2024 18:38:28 GMT
WORKDIR /data
# Mon, 06 May 2024 18:38:28 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 18:38:28 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 18:38:28 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Mon, 06 May 2024 18:38:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 18:38:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 18:38:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d51c66a149e0bef79c9acebe5744642d5b7172e151aea0ec2c4b88dca951026`  
		Last Modified: Mon, 06 May 2024 18:32:15 GMT  
		Size: 68.5 MB (68513435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75623fe094128bfed6120fd7043b4f978b93626acc5ad798f8257698d59c9bee`  
		Last Modified: Mon, 06 May 2024 18:39:59 GMT  
		Size: 424.6 KB (424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ae4cd6585a7aeda6c78af5557384cc50cbd38dafd6236cda0a387eb35834d1`  
		Last Modified: Mon, 06 May 2024 18:40:08 GMT  
		Size: 127.6 MB (127638739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9295bffe45ae4b6892cabe53c93d9a4e6b66b73c34f91d92965b221ae70a85`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 1.9 MB (1940650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7d7557f0a90aaa0dcc2782e00e595f6c4373b8d782ec7c0aac38807ea09ba9`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df2c86dc8d5e047beb57343f7d55644eb508b0fcf4529401290cf33de118ebb`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12e7999be1830b41c3e148bd482b4a6971593c4bf112cc01c04d925d4241a31`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf611f39d53636e1d5fcdb95568047d8624d684617f74c5a3eb5ab8b8d5fe43`  
		Last Modified: Mon, 06 May 2024 18:39:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:86511cdb45290035f218f0768a898f912ccfc2d9f3d963e5ae66e93dae713b70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197010741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50c842526bda418de7dfe5d804507e2c63a313aa046f49a8532def7dc80ad20`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 06 May 2024 19:33:17 GMT
ADD file:c55a37ed4bc43b7f7709186b2ec7f5ea9deab1dcc9a4902a7049e02a82f2fa80 in / 
# Mon, 06 May 2024 19:33:18 GMT
CMD ["/bin/bash"]
# Mon, 06 May 2024 19:37:03 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Mon, 06 May 2024 19:37:17 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Mon, 06 May 2024 19:37:20 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 06 May 2024 19:37:20 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 May 2024 19:37:20 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 06 May 2024 19:37:20 GMT
RUN mkdir -p /data/data /data/log
# Mon, 06 May 2024 19:37:20 GMT
VOLUME [/data]
# Mon, 06 May 2024 19:37:20 GMT
WORKDIR /data
# Mon, 06 May 2024 19:37:21 GMT
EXPOSE 4200 4300 5432
# Mon, 06 May 2024 19:37:21 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 06 May 2024 19:37:21 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 06 May 2024 19:37:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Mon, 06 May 2024 19:37:21 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 06 May 2024 19:37:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 06 May 2024 19:37:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c20235c2702d0b80c079f4d2433eac066301affa902fb7f4a788bbb3cb24a314`  
		Last Modified: Mon, 06 May 2024 19:33:47 GMT  
		Size: 67.5 MB (67495409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b34ee62035157bffabfa5c7d8040c49a7c5e9c50076e6ec0c7b771c8c0651`  
		Last Modified: Mon, 06 May 2024 19:38:52 GMT  
		Size: 422.6 KB (422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a560cd96675d92a9a0ec274d587fc8c58bbb54d140cea9986a3cfc550f27222`  
		Last Modified: Mon, 06 May 2024 19:39:00 GMT  
		Size: 127.2 MB (127150142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4cdd9b3c858c268d4bce9a3a22d2b8e04107d506bda08a64787f090fd9ed0a`  
		Last Modified: Mon, 06 May 2024 19:38:51 GMT  
		Size: 1.9 MB (1940669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0373138e0c0eaed3556365ee536b6f4a3071da6cac6627ab2350c3ffea4e4a56`  
		Last Modified: Mon, 06 May 2024 19:38:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac1307eb5e26dd62537a53fd3ed59e0394651ea196de30001040e2e7c3f6f2`  
		Last Modified: Mon, 06 May 2024 19:38:50 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3745be2006df3d6da5b7eb78f6b8a1295e6a493720b8fca57608ce64a14d51`  
		Last Modified: Mon, 06 May 2024 19:38:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076274663acb56a83e1b01a0daa0d5f92a9965f43998ce720227b7cd035fff3`  
		Last Modified: Mon, 06 May 2024 19:38:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
