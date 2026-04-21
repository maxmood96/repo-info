<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.0`](#crate60)
-	[`crate:6.0.6`](#crate606)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.4`](#crate614)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.6`](#crate626)
-	[`crate:latest`](#cratelatest)

## `crate:6.0`

```console
$ docker pull crate@sha256:353395cab60341f04e4eb2f753a1f99d1b66835171b4ce3d741907000d14e6ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:cb32a2f91a4fe4d366218ec4e97a7b818fb4ddddc6d9b157da4e99f5acdd950c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256341331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf97f820d5d4decb94ed6fb98a34b298239f4e53a734c4af29aac2c6c15695b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:54 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:54 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:47:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:48:05 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:48:08 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:48:08 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:48:08 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:48:08 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:48:08 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 20 Apr 2026 22:48:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:48:08 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:230b501b1ea563652641fd033d7557bf9c28dc3a7371806629ab897ea7e8553a`  
		Last Modified: Tue, 07 Apr 2026 19:24:11 GMT  
		Size: 68.6 MB (68554137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86ab15903fcd2941d74f99b5546bfc9e4c419c2d69d7a1b2cdefa8109a16f6`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 31.1 MB (31065719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1fc860e50fc9a3223ee47c8d61897827dbb3ef412f7d4d1b7f8eb040eaf7fe`  
		Last Modified: Mon, 20 Apr 2026 22:48:30 GMT  
		Size: 149.0 MB (149020502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d2fdaa6905d170d0576c88dd5e65e015f297fec9bee412dfd07b140e65fd27`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 7.7 MB (7699098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc75c430c8428a879127040e003864987a78415f2bf4e8cdba3c5747609f6065`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab0b63f62c157412a18bdf375d16e1d51382846a1debd8484d6c4a0df238542`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331d31802e75ffb7a235f5690f05268819827851e9eb3372127fa0bcc44d6355`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e94d51125151b8a18d3688ca12269d5d20bb34de5818df9377e3e12d23a1`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:0a03f979cbe4252c81bfc6915735af459e9abb88dfa4d81b3cf58cf73a8cea2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54b80ca11a6a4459e08eec2144b369ee6abb071e923cbb4c4dfa1c7fc0edd15`

```dockerfile
```

-	Layers:
	-	`sha256:c910dad0b5765a53686fd35cd717d8623201724c3215fec36b84fd3eca1ef294`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 6.7 MB (6652271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c04a80e66a094dc903718942fa7c8735decfb04f76e96c02711230452c3338`  
		Last Modified: Mon, 20 Apr 2026 22:48:25 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e0687ba898c18034d33b524a7d9b459f709a3aa16b16c3a6a9d6b90104d9eda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255531549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5cf825bfef950a88f50448f40d14eed2ac05c8b23d55d1bc23cc0b99832ab0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:28 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:46:55 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:47:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:47:57 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:47:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:47:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:47:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:47:57 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:47:58 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:47:58 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:47:58 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:47:58 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:47:58 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 20 Apr 2026 22:47:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:47:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:47:58 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2aeff6e98eb0765b09a6a3ef9c4f5198dc05af5a7781716828d1545ebbdbbead`  
		Last Modified: Tue, 07 Apr 2026 19:23:45 GMT  
		Size: 67.1 MB (67143933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9cda2f80a46c1b7871ea2d8420c1a1123884fb50c111e2dbdb8f43791a976e`  
		Last Modified: Mon, 20 Apr 2026 22:47:32 GMT  
		Size: 31.0 MB (30976011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb6bb5bbfbf43c030be968d21ec322dd0397bc97a53e978566be4796831a18b`  
		Last Modified: Mon, 20 Apr 2026 22:48:20 GMT  
		Size: 149.7 MB (149712852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893bc019b96509e90221b5fe239a19b8b654b409401f11be3c68ac4cd1e354ea`  
		Last Modified: Mon, 20 Apr 2026 22:48:17 GMT  
		Size: 7.7 MB (7696874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dda71800437332e5b33adf57565ec95cbccc0b6e231dc842a5a3b3411aece66`  
		Last Modified: Mon, 20 Apr 2026 22:48:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755de7fadcf56d7db2e4466cda6e08802bb6ee43f764bf5570943e57f7525245`  
		Last Modified: Mon, 20 Apr 2026 22:48:16 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19661d0b515edd4104e84f0181bfc33426ac0e5a7849eb77998109eaa3e56c`  
		Last Modified: Mon, 20 Apr 2026 22:48:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b4d368f40b4394d484109a8cf58e8dc14dc129243e208eb0438c8a07fb62a`  
		Last Modified: Mon, 20 Apr 2026 22:48:17 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:7614dc6f554edb0cbc75d697307cffc006a5060ce4a6e543b442307d5ed41dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac5bec2b9da38bf0efe45221969b3534f8ee1d439c8ac41602b15b163bc70f8`

```dockerfile
```

-	Layers:
	-	`sha256:21b9c8f929932d54386c139317d8c792f90abdb6cbd6ec7a454e3bef3b104140`  
		Last Modified: Mon, 20 Apr 2026 22:48:16 GMT  
		Size: 6.7 MB (6650183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c195b1fde4e9e6a7e212cd72718ce1309d54010d2b12df2db1eb6640057937`  
		Last Modified: Mon, 20 Apr 2026 22:48:16 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.6`

```console
$ docker pull crate@sha256:353395cab60341f04e4eb2f753a1f99d1b66835171b4ce3d741907000d14e6ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.6` - linux; amd64

```console
$ docker pull crate@sha256:cb32a2f91a4fe4d366218ec4e97a7b818fb4ddddc6d9b157da4e99f5acdd950c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256341331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf97f820d5d4decb94ed6fb98a34b298239f4e53a734c4af29aac2c6c15695b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:54 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:54 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:47:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:48:05 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:48:08 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:48:08 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:48:08 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:48:08 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:48:08 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 20 Apr 2026 22:48:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:48:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:48:08 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:230b501b1ea563652641fd033d7557bf9c28dc3a7371806629ab897ea7e8553a`  
		Last Modified: Tue, 07 Apr 2026 19:24:11 GMT  
		Size: 68.6 MB (68554137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86ab15903fcd2941d74f99b5546bfc9e4c419c2d69d7a1b2cdefa8109a16f6`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 31.1 MB (31065719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1fc860e50fc9a3223ee47c8d61897827dbb3ef412f7d4d1b7f8eb040eaf7fe`  
		Last Modified: Mon, 20 Apr 2026 22:48:30 GMT  
		Size: 149.0 MB (149020502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d2fdaa6905d170d0576c88dd5e65e015f297fec9bee412dfd07b140e65fd27`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 7.7 MB (7699098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc75c430c8428a879127040e003864987a78415f2bf4e8cdba3c5747609f6065`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab0b63f62c157412a18bdf375d16e1d51382846a1debd8484d6c4a0df238542`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331d31802e75ffb7a235f5690f05268819827851e9eb3372127fa0bcc44d6355`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e94d51125151b8a18d3688ca12269d5d20bb34de5818df9377e3e12d23a1`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:0a03f979cbe4252c81bfc6915735af459e9abb88dfa4d81b3cf58cf73a8cea2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54b80ca11a6a4459e08eec2144b369ee6abb071e923cbb4c4dfa1c7fc0edd15`

```dockerfile
```

-	Layers:
	-	`sha256:c910dad0b5765a53686fd35cd717d8623201724c3215fec36b84fd3eca1ef294`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 6.7 MB (6652271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c04a80e66a094dc903718942fa7c8735decfb04f76e96c02711230452c3338`  
		Last Modified: Mon, 20 Apr 2026 22:48:25 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e0687ba898c18034d33b524a7d9b459f709a3aa16b16c3a6a9d6b90104d9eda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255531549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5cf825bfef950a88f50448f40d14eed2ac05c8b23d55d1bc23cc0b99832ab0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:28 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:46:55 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:47:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:47:57 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:47:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:47:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:47:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:47:57 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:47:58 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:47:58 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:47:58 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:47:58 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:47:58 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 20 Apr 2026 22:47:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:47:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:47:58 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2aeff6e98eb0765b09a6a3ef9c4f5198dc05af5a7781716828d1545ebbdbbead`  
		Last Modified: Tue, 07 Apr 2026 19:23:45 GMT  
		Size: 67.1 MB (67143933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9cda2f80a46c1b7871ea2d8420c1a1123884fb50c111e2dbdb8f43791a976e`  
		Last Modified: Mon, 20 Apr 2026 22:47:32 GMT  
		Size: 31.0 MB (30976011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb6bb5bbfbf43c030be968d21ec322dd0397bc97a53e978566be4796831a18b`  
		Last Modified: Mon, 20 Apr 2026 22:48:20 GMT  
		Size: 149.7 MB (149712852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893bc019b96509e90221b5fe239a19b8b654b409401f11be3c68ac4cd1e354ea`  
		Last Modified: Mon, 20 Apr 2026 22:48:17 GMT  
		Size: 7.7 MB (7696874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dda71800437332e5b33adf57565ec95cbccc0b6e231dc842a5a3b3411aece66`  
		Last Modified: Mon, 20 Apr 2026 22:48:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755de7fadcf56d7db2e4466cda6e08802bb6ee43f764bf5570943e57f7525245`  
		Last Modified: Mon, 20 Apr 2026 22:48:16 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19661d0b515edd4104e84f0181bfc33426ac0e5a7849eb77998109eaa3e56c`  
		Last Modified: Mon, 20 Apr 2026 22:48:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b4d368f40b4394d484109a8cf58e8dc14dc129243e208eb0438c8a07fb62a`  
		Last Modified: Mon, 20 Apr 2026 22:48:17 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:7614dc6f554edb0cbc75d697307cffc006a5060ce4a6e543b442307d5ed41dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac5bec2b9da38bf0efe45221969b3534f8ee1d439c8ac41602b15b163bc70f8`

```dockerfile
```

-	Layers:
	-	`sha256:21b9c8f929932d54386c139317d8c792f90abdb6cbd6ec7a454e3bef3b104140`  
		Last Modified: Mon, 20 Apr 2026 22:48:16 GMT  
		Size: 6.7 MB (6650183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c195b1fde4e9e6a7e212cd72718ce1309d54010d2b12df2db1eb6640057937`  
		Last Modified: Mon, 20 Apr 2026 22:48:16 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:e2cad33f0a8b8cafa919a38656f6c71c360daff6045762cf15bc46e35eb1336d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:5c0bbe40a3f57acc38bf70e2fd7b4712390155a59e3f6f49d1dd3d1572746797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256469058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7610b3a1999bf9b9ea90840b9402fbfc769770e61800546773ea3f09467fd4c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:54 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:54 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:48:13 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:48:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:48:30 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:48:30 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:48:30 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:48:30 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:48:30 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 20 Apr 2026 22:48:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:48:30 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:230b501b1ea563652641fd033d7557bf9c28dc3a7371806629ab897ea7e8553a`  
		Last Modified: Tue, 07 Apr 2026 19:24:11 GMT  
		Size: 68.6 MB (68554137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdeb7d313f069c278ed099603525e47e42741dd9c1627235d7e943b6b5f2a5c`  
		Last Modified: Mon, 20 Apr 2026 22:48:50 GMT  
		Size: 31.1 MB (31065791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7f92d3541f5bd6262daf9b06244398c4da8cfcf62a2a30713e24d3a725881`  
		Last Modified: Mon, 20 Apr 2026 22:48:52 GMT  
		Size: 149.1 MB (149148259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8406c7a64cd02bb19dfdcc9fddd01d25a27301bf714a55b4dfcd4d63daef981e`  
		Last Modified: Mon, 20 Apr 2026 22:48:49 GMT  
		Size: 7.7 MB (7698992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de8f952374ce924b542b0a49aff29be086dcad5002922c3f1200e6bc06c6754`  
		Last Modified: Mon, 20 Apr 2026 22:48:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db14288c98774282469bff79ced513819ec63d27c5305b2bf3b1b43f2a39e74d`  
		Last Modified: Mon, 20 Apr 2026 22:48:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c9df7ad53a5460829f2562cdf8ca620c17347dd667c38d8283f9ef5b96707e`  
		Last Modified: Mon, 20 Apr 2026 22:48:51 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e94d51125151b8a18d3688ca12269d5d20bb34de5818df9377e3e12d23a1`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:ab50ba2c4cd3bc1064b827bb4f2fdebd642f32455c0423ad4e2fc8c33a87137e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594a23a1d4e9d9715da20a6b662751959c6ab765747f3aa8a9b792e8c68def4a`

```dockerfile
```

-	Layers:
	-	`sha256:869014221da566d1572d8c5e0336192d4a050892ed54c16c2b8283f31b51a275`  
		Last Modified: Mon, 20 Apr 2026 22:48:49 GMT  
		Size: 6.7 MB (6651055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b10a11d3bbd500769ee8da59d3554c70e90e1930617bd900fb6ce4bf558426b`  
		Last Modified: Mon, 20 Apr 2026 22:48:49 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:b2db43465fc15d6c9b01fc53abb375a6d7de3d1bad6f0e66bb49e11372675392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255657295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b49aef3e072a23ec5138e6ddb728bc34c8a08c398cc061d2c4be02272bdc411`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:28 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:47:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:48:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:48:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:48:07 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:48:07 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:48:07 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:48:07 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 20 Apr 2026 22:48:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:48:07 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2aeff6e98eb0765b09a6a3ef9c4f5198dc05af5a7781716828d1545ebbdbbead`  
		Last Modified: Tue, 07 Apr 2026 19:23:45 GMT  
		Size: 67.1 MB (67143933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8dad1e3e2e2cc4309a5792cd82f7a6d40d862b0e1c327252e32bb0d4b9cc20`  
		Last Modified: Mon, 20 Apr 2026 22:48:29 GMT  
		Size: 31.0 MB (30975958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e020f3f86f5f5fda9de4220f5d2f74ca3c7dc4cc98fbafd7f235f8f77bea0f45`  
		Last Modified: Mon, 20 Apr 2026 22:48:30 GMT  
		Size: 149.8 MB (149838567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eff69c417decbbd2b05a79a1419201ee28c891f0072f2cd59b0d176fea4772b`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 7.7 MB (7696959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c83c84cb0319b5c28d6bf9957c919cec178471ef810c729b5b421c93c9a9e7a`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8aabc5327d966d1090ad84d0bb0f42e2c5232635a18927c7bd649e32493c2f`  
		Last Modified: Mon, 20 Apr 2026 22:48:28 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddde847b0f6643dcb5c7925c218646476ed35d507f670d56469c5a09b115ccc`  
		Last Modified: Mon, 20 Apr 2026 22:48:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f90ff5a9f99fd9ae66b7cd376f6740b8066ae499d79785951a836c08e60d89`  
		Last Modified: Mon, 20 Apr 2026 22:48:29 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:b7b3da5ebead18d80773d477141b7270cf1c82e80f9809c97d191065e4c23893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc91b35a863f39eaa4d1afa1f68c2ca81ecd5943ad8931a403d1a6740dd55ff`

```dockerfile
```

-	Layers:
	-	`sha256:f827353b31decaf08e9f9b0078ae5d30e13db6a05cf30a6ad36f105e64410aa2`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 6.6 MB (6648967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9e07557bd8af6153a5b7f2240d6a211a267692f08f431a804c851cad45fd35`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.4`

```console
$ docker pull crate@sha256:e2cad33f0a8b8cafa919a38656f6c71c360daff6045762cf15bc46e35eb1336d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.4` - linux; amd64

```console
$ docker pull crate@sha256:5c0bbe40a3f57acc38bf70e2fd7b4712390155a59e3f6f49d1dd3d1572746797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256469058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7610b3a1999bf9b9ea90840b9402fbfc769770e61800546773ea3f09467fd4c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:54 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:54 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:48:13 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:48:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:48:30 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:48:30 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:48:30 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:48:30 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:48:30 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 20 Apr 2026 22:48:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:48:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:48:30 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:230b501b1ea563652641fd033d7557bf9c28dc3a7371806629ab897ea7e8553a`  
		Last Modified: Tue, 07 Apr 2026 19:24:11 GMT  
		Size: 68.6 MB (68554137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdeb7d313f069c278ed099603525e47e42741dd9c1627235d7e943b6b5f2a5c`  
		Last Modified: Mon, 20 Apr 2026 22:48:50 GMT  
		Size: 31.1 MB (31065791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7f92d3541f5bd6262daf9b06244398c4da8cfcf62a2a30713e24d3a725881`  
		Last Modified: Mon, 20 Apr 2026 22:48:52 GMT  
		Size: 149.1 MB (149148259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8406c7a64cd02bb19dfdcc9fddd01d25a27301bf714a55b4dfcd4d63daef981e`  
		Last Modified: Mon, 20 Apr 2026 22:48:49 GMT  
		Size: 7.7 MB (7698992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de8f952374ce924b542b0a49aff29be086dcad5002922c3f1200e6bc06c6754`  
		Last Modified: Mon, 20 Apr 2026 22:48:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db14288c98774282469bff79ced513819ec63d27c5305b2bf3b1b43f2a39e74d`  
		Last Modified: Mon, 20 Apr 2026 22:48:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c9df7ad53a5460829f2562cdf8ca620c17347dd667c38d8283f9ef5b96707e`  
		Last Modified: Mon, 20 Apr 2026 22:48:51 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e94d51125151b8a18d3688ca12269d5d20bb34de5818df9377e3e12d23a1`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:ab50ba2c4cd3bc1064b827bb4f2fdebd642f32455c0423ad4e2fc8c33a87137e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594a23a1d4e9d9715da20a6b662751959c6ab765747f3aa8a9b792e8c68def4a`

```dockerfile
```

-	Layers:
	-	`sha256:869014221da566d1572d8c5e0336192d4a050892ed54c16c2b8283f31b51a275`  
		Last Modified: Mon, 20 Apr 2026 22:48:49 GMT  
		Size: 6.7 MB (6651055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b10a11d3bbd500769ee8da59d3554c70e90e1930617bd900fb6ce4bf558426b`  
		Last Modified: Mon, 20 Apr 2026 22:48:49 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:b2db43465fc15d6c9b01fc53abb375a6d7de3d1bad6f0e66bb49e11372675392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255657295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b49aef3e072a23ec5138e6ddb728bc34c8a08c398cc061d2c4be02272bdc411`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:28 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:47:51 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:48:04 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:48:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:48:07 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:48:07 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:48:07 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:48:07 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 20 Apr 2026 22:48:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:48:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:48:07 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2aeff6e98eb0765b09a6a3ef9c4f5198dc05af5a7781716828d1545ebbdbbead`  
		Last Modified: Tue, 07 Apr 2026 19:23:45 GMT  
		Size: 67.1 MB (67143933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8dad1e3e2e2cc4309a5792cd82f7a6d40d862b0e1c327252e32bb0d4b9cc20`  
		Last Modified: Mon, 20 Apr 2026 22:48:29 GMT  
		Size: 31.0 MB (30975958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e020f3f86f5f5fda9de4220f5d2f74ca3c7dc4cc98fbafd7f235f8f77bea0f45`  
		Last Modified: Mon, 20 Apr 2026 22:48:30 GMT  
		Size: 149.8 MB (149838567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eff69c417decbbd2b05a79a1419201ee28c891f0072f2cd59b0d176fea4772b`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 7.7 MB (7696959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c83c84cb0319b5c28d6bf9957c919cec178471ef810c729b5b421c93c9a9e7a`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8aabc5327d966d1090ad84d0bb0f42e2c5232635a18927c7bd649e32493c2f`  
		Last Modified: Mon, 20 Apr 2026 22:48:28 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddde847b0f6643dcb5c7925c218646476ed35d507f670d56469c5a09b115ccc`  
		Last Modified: Mon, 20 Apr 2026 22:48:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f90ff5a9f99fd9ae66b7cd376f6740b8066ae499d79785951a836c08e60d89`  
		Last Modified: Mon, 20 Apr 2026 22:48:29 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:b7b3da5ebead18d80773d477141b7270cf1c82e80f9809c97d191065e4c23893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc91b35a863f39eaa4d1afa1f68c2ca81ecd5943ad8931a403d1a6740dd55ff`

```dockerfile
```

-	Layers:
	-	`sha256:f827353b31decaf08e9f9b0078ae5d30e13db6a05cf30a6ad36f105e64410aa2`  
		Last Modified: Mon, 20 Apr 2026 22:48:27 GMT  
		Size: 6.6 MB (6648967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9e07557bd8af6153a5b7f2240d6a211a267692f08f431a804c851cad45fd35`  
		Last Modified: Mon, 20 Apr 2026 22:48:26 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2`

```console
$ docker pull crate@sha256:fc2bde5db52d3f3cee07395bf21a574261ad449b751999ba9f7c7853c5225034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:aa0621cb2cc9c0378775f6133c3442832f2593ff3ed304ab4613f4a7fcd54893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258638411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c90633329ff1cdb191b7f04fd436f38962d21b2f3e69ed26176727a386dbbe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:54 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:54 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:47:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:47:20 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.6.tar.gz.asc crate-6.2.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.6.tar.gz.asc     && tar -xf crate-6.2.6.tar.gz -C /crate --strip-components=1     && rm crate-6.2.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:47:23 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:47:23 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:47:23 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:47:23 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:47:23 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T10:35:44.058297+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.6
# Mon, 20 Apr 2026 22:47:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:47:23 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:230b501b1ea563652641fd033d7557bf9c28dc3a7371806629ab897ea7e8553a`  
		Last Modified: Tue, 07 Apr 2026 19:24:11 GMT  
		Size: 68.6 MB (68554137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86ab15903fcd2941d74f99b5546bfc9e4c419c2d69d7a1b2cdefa8109a16f6`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 31.1 MB (31065719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d6174e6b061f3fb359493038f43a259f0100ce881ac09aa67830d4f2f5a22e`  
		Last Modified: Mon, 20 Apr 2026 22:47:46 GMT  
		Size: 151.3 MB (151317876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8f9660d93d572a4baabfb9c32f0195bccdcde573a300c68416fcb4cee79993`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 7.7 MB (7698801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a44b581ef8331a9a0b26b88051ba499eb7d4ea45a1f89810be5156913b94eb`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b5c9413e8772ce5ca9e360920713e892bfdb087ca93cb9b608847abe72ba44`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a3cbd57ef41ba3e9ddf56f9f9f9706face12a7deba26a19abb2a85b39503f3`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8487dea58a82d5e57250f0c6214437e1da207b6814a500e0b4e3f6463f3a99`  
		Last Modified: Mon, 20 Apr 2026 22:47:44 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:f262c1b9223680dfdfa26ea4808ca620f053cf607c7a612ed03316b192926914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db51589d35b8cf56591395964050dfa0c035891438f6be9a2525bc82e0e700e`

```dockerfile
```

-	Layers:
	-	`sha256:38cf1608fd21a5c28e026435b8cb32ef456cad272fdce939410232d5c154fe9f`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 6.7 MB (6656879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02470e291fc5d1ef8fa41c84ff48725feda3fe85d7abb3f729b740bfa41e2828`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:07885f627f854d680de7bd0ba7003d4fa7ac708fe3bad5a1dd74a3ba2895233c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255100395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f96179e6528ce3a0e7e07d1b7dca77538f016b2a5fbd51e888c051644fc60e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:28 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:46:55 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:47:08 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.6.tar.gz.asc crate-6.2.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.6.tar.gz.asc     && tar -xf crate-6.2.6.tar.gz -C /crate --strip-components=1     && rm crate-6.2.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:47:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:47:11 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:47:11 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:47:11 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:47:11 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T10:35:44.058297+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.6
# Mon, 20 Apr 2026 22:47:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:47:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2aeff6e98eb0765b09a6a3ef9c4f5198dc05af5a7781716828d1545ebbdbbead`  
		Last Modified: Tue, 07 Apr 2026 19:23:45 GMT  
		Size: 67.1 MB (67143933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9cda2f80a46c1b7871ea2d8420c1a1123884fb50c111e2dbdb8f43791a976e`  
		Last Modified: Mon, 20 Apr 2026 22:47:32 GMT  
		Size: 31.0 MB (30976011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c4e9baa5577dac38243e286b4cccfc295fae02981734dff887da7fa190e8ce`  
		Last Modified: Mon, 20 Apr 2026 22:47:35 GMT  
		Size: 149.3 MB (149281726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f35cbb7be4c4aae26f0b8d2c48fd088dbdc54d425c6aeebc85b69538cd88dd`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 7.7 MB (7696851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c97385f16e7278c6ccdf5829e2bfb0b417923b4afbc1f4412e45d513b0cd41`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1cbac6db2e248d460c3c4fecd901d1911a502542e9347b654ecc4c61851d98`  
		Last Modified: Mon, 20 Apr 2026 22:47:32 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7aeb2770643899b3156175361dc5e61d25a758f0b61c4b2faa36c8a21b5fa23`  
		Last Modified: Mon, 20 Apr 2026 22:47:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b6d6289907d5ee3e6c627575b8f3b08aece266dd5bd672a206eec503e1f9e1`  
		Last Modified: Mon, 20 Apr 2026 22:47:33 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:3d4979bea09d9b8fb97c83ecfdd88bb3c1800aa2a7ab11ca5b184143bd547f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813f459f9f8caf9b0a588422ee4eceea1c9a621d5d71a84ca9366a31789428d8`

```dockerfile
```

-	Layers:
	-	`sha256:d19d00d2ada62e687ab2b62ea3cef693f36f85596b8bc10695f2fc72c29076e0`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 6.7 MB (6654803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98625ebc69e2cee02f051290477170e2e3e2edbcaaee371aea4dd374d8727e88`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.6`

```console
$ docker pull crate@sha256:fc2bde5db52d3f3cee07395bf21a574261ad449b751999ba9f7c7853c5225034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.6` - linux; amd64

```console
$ docker pull crate@sha256:aa0621cb2cc9c0378775f6133c3442832f2593ff3ed304ab4613f4a7fcd54893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258638411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c90633329ff1cdb191b7f04fd436f38962d21b2f3e69ed26176727a386dbbe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:54 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:54 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:47:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:47:20 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.6.tar.gz.asc crate-6.2.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.6.tar.gz.asc     && tar -xf crate-6.2.6.tar.gz -C /crate --strip-components=1     && rm crate-6.2.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:47:23 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:47:23 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:47:23 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:47:23 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:47:23 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T10:35:44.058297+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.6
# Mon, 20 Apr 2026 22:47:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:47:23 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:230b501b1ea563652641fd033d7557bf9c28dc3a7371806629ab897ea7e8553a`  
		Last Modified: Tue, 07 Apr 2026 19:24:11 GMT  
		Size: 68.6 MB (68554137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86ab15903fcd2941d74f99b5546bfc9e4c419c2d69d7a1b2cdefa8109a16f6`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 31.1 MB (31065719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d6174e6b061f3fb359493038f43a259f0100ce881ac09aa67830d4f2f5a22e`  
		Last Modified: Mon, 20 Apr 2026 22:47:46 GMT  
		Size: 151.3 MB (151317876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8f9660d93d572a4baabfb9c32f0195bccdcde573a300c68416fcb4cee79993`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 7.7 MB (7698801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a44b581ef8331a9a0b26b88051ba499eb7d4ea45a1f89810be5156913b94eb`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b5c9413e8772ce5ca9e360920713e892bfdb087ca93cb9b608847abe72ba44`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a3cbd57ef41ba3e9ddf56f9f9f9706face12a7deba26a19abb2a85b39503f3`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8487dea58a82d5e57250f0c6214437e1da207b6814a500e0b4e3f6463f3a99`  
		Last Modified: Mon, 20 Apr 2026 22:47:44 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.6` - unknown; unknown

```console
$ docker pull crate@sha256:f262c1b9223680dfdfa26ea4808ca620f053cf607c7a612ed03316b192926914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db51589d35b8cf56591395964050dfa0c035891438f6be9a2525bc82e0e700e`

```dockerfile
```

-	Layers:
	-	`sha256:38cf1608fd21a5c28e026435b8cb32ef456cad272fdce939410232d5c154fe9f`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 6.7 MB (6656879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02470e291fc5d1ef8fa41c84ff48725feda3fe85d7abb3f729b740bfa41e2828`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:07885f627f854d680de7bd0ba7003d4fa7ac708fe3bad5a1dd74a3ba2895233c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255100395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f96179e6528ce3a0e7e07d1b7dca77538f016b2a5fbd51e888c051644fc60e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:28 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:46:55 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:47:08 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.6.tar.gz.asc crate-6.2.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.6.tar.gz.asc     && tar -xf crate-6.2.6.tar.gz -C /crate --strip-components=1     && rm crate-6.2.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:47:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:47:11 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:47:11 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:47:11 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:47:11 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T10:35:44.058297+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.6
# Mon, 20 Apr 2026 22:47:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:47:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2aeff6e98eb0765b09a6a3ef9c4f5198dc05af5a7781716828d1545ebbdbbead`  
		Last Modified: Tue, 07 Apr 2026 19:23:45 GMT  
		Size: 67.1 MB (67143933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9cda2f80a46c1b7871ea2d8420c1a1123884fb50c111e2dbdb8f43791a976e`  
		Last Modified: Mon, 20 Apr 2026 22:47:32 GMT  
		Size: 31.0 MB (30976011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c4e9baa5577dac38243e286b4cccfc295fae02981734dff887da7fa190e8ce`  
		Last Modified: Mon, 20 Apr 2026 22:47:35 GMT  
		Size: 149.3 MB (149281726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f35cbb7be4c4aae26f0b8d2c48fd088dbdc54d425c6aeebc85b69538cd88dd`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 7.7 MB (7696851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c97385f16e7278c6ccdf5829e2bfb0b417923b4afbc1f4412e45d513b0cd41`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1cbac6db2e248d460c3c4fecd901d1911a502542e9347b654ecc4c61851d98`  
		Last Modified: Mon, 20 Apr 2026 22:47:32 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7aeb2770643899b3156175361dc5e61d25a758f0b61c4b2faa36c8a21b5fa23`  
		Last Modified: Mon, 20 Apr 2026 22:47:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b6d6289907d5ee3e6c627575b8f3b08aece266dd5bd672a206eec503e1f9e1`  
		Last Modified: Mon, 20 Apr 2026 22:47:33 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.6` - unknown; unknown

```console
$ docker pull crate@sha256:3d4979bea09d9b8fb97c83ecfdd88bb3c1800aa2a7ab11ca5b184143bd547f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813f459f9f8caf9b0a588422ee4eceea1c9a621d5d71a84ca9366a31789428d8`

```dockerfile
```

-	Layers:
	-	`sha256:d19d00d2ada62e687ab2b62ea3cef693f36f85596b8bc10695f2fc72c29076e0`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 6.7 MB (6654803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98625ebc69e2cee02f051290477170e2e3e2edbcaaee371aea4dd374d8727e88`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:fc2bde5db52d3f3cee07395bf21a574261ad449b751999ba9f7c7853c5225034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:aa0621cb2cc9c0378775f6133c3442832f2593ff3ed304ab4613f4a7fcd54893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258638411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c90633329ff1cdb191b7f04fd436f38962d21b2f3e69ed26176727a386dbbe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:54 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:54 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:47:06 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:47:20 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.6.tar.gz.asc crate-6.2.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.6.tar.gz.asc     && tar -xf crate-6.2.6.tar.gz -C /crate --strip-components=1     && rm crate-6.2.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:47:23 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:47:23 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:47:23 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:47:23 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:47:23 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T10:35:44.058297+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.6
# Mon, 20 Apr 2026 22:47:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:47:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:47:23 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:230b501b1ea563652641fd033d7557bf9c28dc3a7371806629ab897ea7e8553a`  
		Last Modified: Tue, 07 Apr 2026 19:24:11 GMT  
		Size: 68.6 MB (68554137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86ab15903fcd2941d74f99b5546bfc9e4c419c2d69d7a1b2cdefa8109a16f6`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 31.1 MB (31065719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d6174e6b061f3fb359493038f43a259f0100ce881ac09aa67830d4f2f5a22e`  
		Last Modified: Mon, 20 Apr 2026 22:47:46 GMT  
		Size: 151.3 MB (151317876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8f9660d93d572a4baabfb9c32f0195bccdcde573a300c68416fcb4cee79993`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 7.7 MB (7698801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a44b581ef8331a9a0b26b88051ba499eb7d4ea45a1f89810be5156913b94eb`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b5c9413e8772ce5ca9e360920713e892bfdb087ca93cb9b608847abe72ba44`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a3cbd57ef41ba3e9ddf56f9f9f9706face12a7deba26a19abb2a85b39503f3`  
		Last Modified: Mon, 20 Apr 2026 22:47:43 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8487dea58a82d5e57250f0c6214437e1da207b6814a500e0b4e3f6463f3a99`  
		Last Modified: Mon, 20 Apr 2026 22:47:44 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:f262c1b9223680dfdfa26ea4808ca620f053cf607c7a612ed03316b192926914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db51589d35b8cf56591395964050dfa0c035891438f6be9a2525bc82e0e700e`

```dockerfile
```

-	Layers:
	-	`sha256:38cf1608fd21a5c28e026435b8cb32ef456cad272fdce939410232d5c154fe9f`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 6.7 MB (6656879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02470e291fc5d1ef8fa41c84ff48725feda3fe85d7abb3f729b740bfa41e2828`  
		Last Modified: Mon, 20 Apr 2026 22:47:42 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:07885f627f854d680de7bd0ba7003d4fa7ac708fe3bad5a1dd74a3ba2895233c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255100395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f96179e6528ce3a0e7e07d1b7dca77538f016b2a5fbd51e888c051644fc60e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 07 Apr 2026 19:23:28 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 07 Apr 2026 19:23:28 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 22:46:55 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 20 Apr 2026 22:47:08 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.6.tar.gz.asc crate-6.2.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.6.tar.gz.asc     && tar -xf crate-6.2.6.tar.gz -C /crate --strip-components=1     && rm crate-6.2.6.tar.gz # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 22:47:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 20 Apr 2026 22:47:11 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
VOLUME [/data]
# Mon, 20 Apr 2026 22:47:11 GMT
WORKDIR /data
# Mon, 20 Apr 2026 22:47:11 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 20 Apr 2026 22:47:11 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T10:35:44.058297+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.6
# Mon, 20 Apr 2026 22:47:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 20 Apr 2026 22:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 22:47:11 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2aeff6e98eb0765b09a6a3ef9c4f5198dc05af5a7781716828d1545ebbdbbead`  
		Last Modified: Tue, 07 Apr 2026 19:23:45 GMT  
		Size: 67.1 MB (67143933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9cda2f80a46c1b7871ea2d8420c1a1123884fb50c111e2dbdb8f43791a976e`  
		Last Modified: Mon, 20 Apr 2026 22:47:32 GMT  
		Size: 31.0 MB (30976011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c4e9baa5577dac38243e286b4cccfc295fae02981734dff887da7fa190e8ce`  
		Last Modified: Mon, 20 Apr 2026 22:47:35 GMT  
		Size: 149.3 MB (149281726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f35cbb7be4c4aae26f0b8d2c48fd088dbdc54d425c6aeebc85b69538cd88dd`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 7.7 MB (7696851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c97385f16e7278c6ccdf5829e2bfb0b417923b4afbc1f4412e45d513b0cd41`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1cbac6db2e248d460c3c4fecd901d1911a502542e9347b654ecc4c61851d98`  
		Last Modified: Mon, 20 Apr 2026 22:47:32 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7aeb2770643899b3156175361dc5e61d25a758f0b61c4b2faa36c8a21b5fa23`  
		Last Modified: Mon, 20 Apr 2026 22:47:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b6d6289907d5ee3e6c627575b8f3b08aece266dd5bd672a206eec503e1f9e1`  
		Last Modified: Mon, 20 Apr 2026 22:47:33 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:3d4979bea09d9b8fb97c83ecfdd88bb3c1800aa2a7ab11ca5b184143bd547f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813f459f9f8caf9b0a588422ee4eceea1c9a621d5d71a84ca9366a31789428d8`

```dockerfile
```

-	Layers:
	-	`sha256:d19d00d2ada62e687ab2b62ea3cef693f36f85596b8bc10695f2fc72c29076e0`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 6.7 MB (6654803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98625ebc69e2cee02f051290477170e2e3e2edbcaaee371aea4dd374d8727e88`  
		Last Modified: Mon, 20 Apr 2026 22:47:31 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
