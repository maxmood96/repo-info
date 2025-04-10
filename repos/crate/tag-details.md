<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.4`](#crate5104)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:1d2f9eaea9216b7c4dc0c7649d4eef6ba63daeb3838223350cf5f26f0822bdf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:911058f315f515ad91967e28e46874dd8b66a23a1c27cd4ecaaadf2019fdfe3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249184929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368939091a292e8d53bf4c946436ffa71bfd8743797d204d552aec54c125d879`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 17:01:35 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.3.tar.gz.asc crate-5.10.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.3.tar.gz.asc     && tar -xf crate-5.10.3.tar.gz -C /crate --strip-components=1     && rm crate-5.10.3.tar.gz # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 17:01:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Mar 2025 17:01:35 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
VOLUME [/data]
# Tue, 18 Mar 2025 17:01:35 GMT
WORKDIR /data
# Tue, 18 Mar 2025 17:01:35 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 18 Mar 2025 17:01:35 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-03-18T17:01:35.515323 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.3
# Tue, 18 Mar 2025 17:01:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 17:01:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff9082e4e13cd798b73161454aa2918ef61ac8f8f0c30e821efbb658630be12`  
		Last Modified: Fri, 21 Mar 2025 16:23:05 GMT  
		Size: 31.6 MB (31578148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107b86ba42fc0fd2649982e0caf3c4bf6dc0ea9aa384a4cd789e4a82e9a49315`  
		Last Modified: Fri, 21 Mar 2025 16:23:06 GMT  
		Size: 149.7 MB (149656744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58038e37724a5fc4338968951c4fa2377144b429a1db0c21c3b6c1ed96cc449a`  
		Last Modified: Fri, 21 Mar 2025 16:23:04 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce1c7731b89fd6aa1eef70ee25a5922c8d2ce5b0b2820f8bc0fb57c8cc8622`  
		Last Modified: Fri, 21 Mar 2025 16:23:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e848812a66d3837e25bdfd9750977ff57dc0a079fc2bcaf14c86ea5f48d052`  
		Last Modified: Fri, 21 Mar 2025 16:23:05 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c23503e2c58b6119ce06768620eed4a8c99e677a391064736432f78b4695a`  
		Last Modified: Fri, 21 Mar 2025 16:23:05 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3477a786cc5440c8547874099b792e2b3b90fa0559f310a3a41c78c6b7173db`  
		Last Modified: Fri, 21 Mar 2025 16:23:05 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:44a452abbe88c5d02d656836ae571eeb3da6858700a933495b31f9c46101cc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcdf4be2ec9dbe87d5641627c5bd50c5c219e068cccbd5ddf1cfb69cc2d9610`

```dockerfile
```

-	Layers:
	-	`sha256:7d65aa01197f5d720b3bc927f513395488ee689058514456012da59c24ecaa79`  
		Last Modified: Fri, 21 Mar 2025 16:23:04 GMT  
		Size: 5.2 MB (5155083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0693a6fab70aa84d6f96ca6d3d5384ac0f635a50b863f9a1bf1b4b2d3cd569`  
		Last Modified: Fri, 21 Mar 2025 16:23:04 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:cacc4d5b669fcc07de3f59dd95e6b323942e1ed72d5052111110b1dcf3ad1fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248411312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daec1bbf51a8a7811005d2aca2c972d36b36d47a58cec42a5bc69c32e6b0c653`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 17:01:35 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.3.tar.gz.asc crate-5.10.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.3.tar.gz.asc     && tar -xf crate-5.10.3.tar.gz -C /crate --strip-components=1     && rm crate-5.10.3.tar.gz # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 17:01:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Mar 2025 17:01:35 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
VOLUME [/data]
# Tue, 18 Mar 2025 17:01:35 GMT
WORKDIR /data
# Tue, 18 Mar 2025 17:01:35 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 18 Mar 2025 17:01:35 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-03-18T17:01:35.515323 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.3
# Tue, 18 Mar 2025 17:01:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 17:01:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 00:50:10 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4903f98e06e57191357956ae574a0ed32c6d14d49b511d0784b8f4f07a4c66`  
		Last Modified: Fri, 21 Mar 2025 16:22:26 GMT  
		Size: 31.5 MB (31485516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279f21ad4ee54fef939c04d5469d1e210dea16b96c2638465a9714d3bc78d60`  
		Last Modified: Fri, 21 Mar 2025 16:22:29 GMT  
		Size: 150.3 MB (150337445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e605eb7ab3de3d6ed75daa285f2e5cbd03a7c9196966fa75d59b6c4847ea1355`  
		Last Modified: Fri, 21 Mar 2025 16:22:26 GMT  
		Size: 1.9 MB (1943635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a1c4317b74ca9ae6fcb50c471e79d7d2cda7b5712e5c38125f0b0a614f661e`  
		Last Modified: Fri, 21 Mar 2025 16:22:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d572faa925656899f3786b6aaedcc17a5761677f82fabf2573fb8874079ce8`  
		Last Modified: Fri, 21 Mar 2025 16:22:26 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fcbbd100918330ea6284c89655574f5c5f310fc5f432d47732a666d422ddcb`  
		Last Modified: Fri, 21 Mar 2025 16:22:27 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188bb3f059b8ea7cfec62ad169d26e9b95bbf8311fa61042191848b329f65dfe`  
		Last Modified: Fri, 21 Mar 2025 16:22:27 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:11601907779dec8338f13f7a26ef2c20e842769da70018f5c264310780bc52cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9cf004b304fbb7d46ae27452055636fe5c7c62dbfe692ff61892383a0052df`

```dockerfile
```

-	Layers:
	-	`sha256:93d220916fd441f64838b89a06184e7483b31bbba8351aa04f529eec8243fe31`  
		Last Modified: Fri, 21 Mar 2025 16:22:26 GMT  
		Size: 5.2 MB (5152391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2341e0eee0b9cf46bd405961c7f2cf64f17c7648853002898ce6a284c67e7902`  
		Last Modified: Fri, 21 Mar 2025 16:22:25 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.4`

**does not exist** (yet?)

## `crate:5.9`

```console
$ docker pull crate@sha256:e3dd4d50be80451eb62749af1b5fcf0e16ec47cafc8cd5b5dd2ad914d1c96e9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:5aed75680c94894504f363163271287bace465064dcfff63b727895882480825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248535439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d7139865af0912992d6f34f8594a51eb5f5fedb6326ef8ba4f5b58dcb12606`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 16:15:41 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.12.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.12.tar.gz.asc crate-5.9.12.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.12.tar.gz.asc     && tar -xf crate-5.9.12.tar.gz -C /crate --strip-components=1     && rm crate-5.9.12.tar.gz # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 16:15:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Mar 2025 16:15:41 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
VOLUME [/data]
# Tue, 18 Mar 2025 16:15:41 GMT
WORKDIR /data
# Tue, 18 Mar 2025 16:15:41 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 18 Mar 2025 16:15:41 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-03-18T16:15:41.208927 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.12
# Tue, 18 Mar 2025 16:15:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 16:15:41 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f24d76e54aff67fe63e25ec6aa2530ef5b742aa843f6ec3280e8ee806b29a2`  
		Last Modified: Fri, 21 Mar 2025 16:23:26 GMT  
		Size: 31.6 MB (31578088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee37341f4b07e36c9a2dc1a1bad1db4d35fa8e0767d3d4c8db4cf0f160ca262`  
		Last Modified: Fri, 21 Mar 2025 16:23:28 GMT  
		Size: 149.0 MB (149007311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4788c573488d15c2a2c7188fd26adaafb07f3c2aa94c09829248c77e30d4c73c`  
		Last Modified: Fri, 21 Mar 2025 16:23:25 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8e9d2f8e53636805dc2b126220ba0dbe3bd0f272bbe9689bf32c7320b8f409`  
		Last Modified: Fri, 21 Mar 2025 16:23:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c059159101c85e3778c9795de3f7ad5c8f56d232659a042f6e8ac2ef98cd72`  
		Last Modified: Fri, 21 Mar 2025 16:23:26 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25133a9a4381cc59018b8ee3b81334e2dca7e22235fb90909e5959f3aeceac4b`  
		Last Modified: Fri, 21 Mar 2025 16:23:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3fe9124f07cd146327c4762769ac4998ccc39f80e3da9339aae9180cc46cd`  
		Last Modified: Fri, 21 Mar 2025 16:23:27 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:0576525d429aa92615f1765f897d80ecf97431e8b47643e76c82a3adfb9f465e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e368bc8e8cdfde3530da8b6fc73689fe1a0d172f00a39483ff58574ac75a7a73`

```dockerfile
```

-	Layers:
	-	`sha256:cd5e0e732d67380b69bb0b993652b254e0c661cdc6deb5fba48b44079579cfd9`  
		Last Modified: Fri, 21 Mar 2025 16:23:25 GMT  
		Size: 5.2 MB (5152911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81baee3e54538b3dac8bc6efa494121cfd1923f94aa63bb37b7817fecd26a1b8`  
		Last Modified: Fri, 21 Mar 2025 16:23:25 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:43cc3a0fd5dc44f911a9cee874b916a5b613e64e702623e5c4dc06d5e7289254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247773605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0d525b06caed1ac04733652de5c8660d9319d68779780fbfc7c60ceb6b77f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 16:15:41 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.12.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.12.tar.gz.asc crate-5.9.12.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.12.tar.gz.asc     && tar -xf crate-5.9.12.tar.gz -C /crate --strip-components=1     && rm crate-5.9.12.tar.gz # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 16:15:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Mar 2025 16:15:41 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
VOLUME [/data]
# Tue, 18 Mar 2025 16:15:41 GMT
WORKDIR /data
# Tue, 18 Mar 2025 16:15:41 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 18 Mar 2025 16:15:41 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-03-18T16:15:41.208927 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.12
# Tue, 18 Mar 2025 16:15:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Mar 2025 16:15:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 16:15:41 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 00:50:10 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4903f98e06e57191357956ae574a0ed32c6d14d49b511d0784b8f4f07a4c66`  
		Last Modified: Fri, 21 Mar 2025 16:22:26 GMT  
		Size: 31.5 MB (31485516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2dd03d0fa0586d6010f4c2764b12f7da79d16d6a59c9477b0421678b797cc6`  
		Last Modified: Fri, 21 Mar 2025 16:23:20 GMT  
		Size: 149.7 MB (149699737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf76775c00b56ac03b7dfc0e1443a8fd2213767b4986a780db7914cbfc7626d`  
		Last Modified: Fri, 21 Mar 2025 16:23:16 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed3d7292335520a7c59e051c023ebc7cddb0c16a3bc6f5f40bd8c1c77c2357d`  
		Last Modified: Fri, 21 Mar 2025 16:23:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe5c53f2a15f4b989c6f42383748111156d97cb05f6bedede704729fa17a50`  
		Last Modified: Fri, 21 Mar 2025 16:23:16 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae462f59d3e62cfcad3b858961f4b03e5315404d3e5ca590b95537bf07e1ec6c`  
		Last Modified: Fri, 21 Mar 2025 16:23:17 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dd570674d6f0e732cbdea3ba1e5584282e509032298dd6a7c62a72977bfe6`  
		Last Modified: Fri, 21 Mar 2025 16:23:17 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:c51e8f1c8327e5aa8387e217114bbac3c73db67fa5f12e62ad48475779c9c3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037de0a8a005ffd4cc96be0079818f91bd284fe75223a483c23cd4a57efc92b7`

```dockerfile
```

-	Layers:
	-	`sha256:06efeaa988ab50a582e3246aa7bdce708a0ea7eeb20abaabfb2f5696b847b600`  
		Last Modified: Fri, 21 Mar 2025 16:23:17 GMT  
		Size: 5.2 MB (5150207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:debe603243e248f704c1881d555301edadbfe1b592d96524459752d92f62c3de`  
		Last Modified: Fri, 21 Mar 2025 16:23:16 GMT  
		Size: 23.0 KB (23027 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

**does not exist** (yet?)

## `crate:latest`

```console
$ docker pull crate@sha256:1d2f9eaea9216b7c4dc0c7649d4eef6ba63daeb3838223350cf5f26f0822bdf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:911058f315f515ad91967e28e46874dd8b66a23a1c27cd4ecaaadf2019fdfe3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249184929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368939091a292e8d53bf4c946436ffa71bfd8743797d204d552aec54c125d879`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 17:01:35 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.3.tar.gz.asc crate-5.10.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.3.tar.gz.asc     && tar -xf crate-5.10.3.tar.gz -C /crate --strip-components=1     && rm crate-5.10.3.tar.gz # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 17:01:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Mar 2025 17:01:35 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
VOLUME [/data]
# Tue, 18 Mar 2025 17:01:35 GMT
WORKDIR /data
# Tue, 18 Mar 2025 17:01:35 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 18 Mar 2025 17:01:35 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-03-18T17:01:35.515323 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.3
# Tue, 18 Mar 2025 17:01:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 17:01:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:01fb3dc90bfbc7a0b852bb1b0ca52339dff620622b1fb96bd564087acbcf4fb9`  
		Last Modified: Tue, 04 Feb 2025 19:32:43 GMT  
		Size: 66.0 MB (66004531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff9082e4e13cd798b73161454aa2918ef61ac8f8f0c30e821efbb658630be12`  
		Last Modified: Fri, 21 Mar 2025 16:23:05 GMT  
		Size: 31.6 MB (31578148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107b86ba42fc0fd2649982e0caf3c4bf6dc0ea9aa384a4cd789e4a82e9a49315`  
		Last Modified: Fri, 21 Mar 2025 16:23:06 GMT  
		Size: 149.7 MB (149656744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58038e37724a5fc4338968951c4fa2377144b429a1db0c21c3b6c1ed96cc449a`  
		Last Modified: Fri, 21 Mar 2025 16:23:04 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce1c7731b89fd6aa1eef70ee25a5922c8d2ce5b0b2820f8bc0fb57c8cc8622`  
		Last Modified: Fri, 21 Mar 2025 16:23:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e848812a66d3837e25bdfd9750977ff57dc0a079fc2bcaf14c86ea5f48d052`  
		Last Modified: Fri, 21 Mar 2025 16:23:05 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c23503e2c58b6119ce06768620eed4a8c99e677a391064736432f78b4695a`  
		Last Modified: Fri, 21 Mar 2025 16:23:05 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3477a786cc5440c8547874099b792e2b3b90fa0559f310a3a41c78c6b7173db`  
		Last Modified: Fri, 21 Mar 2025 16:23:05 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:44a452abbe88c5d02d656836ae571eeb3da6858700a933495b31f9c46101cc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcdf4be2ec9dbe87d5641627c5bd50c5c219e068cccbd5ddf1cfb69cc2d9610`

```dockerfile
```

-	Layers:
	-	`sha256:7d65aa01197f5d720b3bc927f513395488ee689058514456012da59c24ecaa79`  
		Last Modified: Fri, 21 Mar 2025 16:23:04 GMT  
		Size: 5.2 MB (5155083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0693a6fab70aa84d6f96ca6d3d5384ac0f635a50b863f9a1bf1b4b2d3cd569`  
		Last Modified: Fri, 21 Mar 2025 16:23:04 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:cacc4d5b669fcc07de3f59dd95e6b323942e1ed72d5052111110b1dcf3ad1fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248411312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daec1bbf51a8a7811005d2aca2c972d36b36d47a58cec42a5bc69c32e6b0c653`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 04 Feb 2025 10:07:34 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 04 Feb 2025 10:07:34 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 17:01:35 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.3.tar.gz.asc crate-5.10.3.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.3.tar.gz.asc     && tar -xf crate-5.10.3.tar.gz -C /crate --strip-components=1     && rm crate-5.10.3.tar.gz # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 17:01:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Mar 2025 17:01:35 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
VOLUME [/data]
# Tue, 18 Mar 2025 17:01:35 GMT
WORKDIR /data
# Tue, 18 Mar 2025 17:01:35 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 18 Mar 2025 17:01:35 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-03-18T17:01:35.515323 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.3
# Tue, 18 Mar 2025 17:01:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Mar 2025 17:01:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Mar 2025 17:01:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:fde35c1a76eb22cfbd6a2eae80b77b0f1faf115bf4dc80a9f47e9c063b99c818`  
		Last Modified: Wed, 05 Feb 2025 00:50:10 GMT  
		Size: 64.6 MB (64642835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4903f98e06e57191357956ae574a0ed32c6d14d49b511d0784b8f4f07a4c66`  
		Last Modified: Fri, 21 Mar 2025 16:22:26 GMT  
		Size: 31.5 MB (31485516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279f21ad4ee54fef939c04d5469d1e210dea16b96c2638465a9714d3bc78d60`  
		Last Modified: Fri, 21 Mar 2025 16:22:29 GMT  
		Size: 150.3 MB (150337445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e605eb7ab3de3d6ed75daa285f2e5cbd03a7c9196966fa75d59b6c4847ea1355`  
		Last Modified: Fri, 21 Mar 2025 16:22:26 GMT  
		Size: 1.9 MB (1943635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a1c4317b74ca9ae6fcb50c471e79d7d2cda7b5712e5c38125f0b0a614f661e`  
		Last Modified: Fri, 21 Mar 2025 16:22:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d572faa925656899f3786b6aaedcc17a5761677f82fabf2573fb8874079ce8`  
		Last Modified: Fri, 21 Mar 2025 16:22:26 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fcbbd100918330ea6284c89655574f5c5f310fc5f432d47732a666d422ddcb`  
		Last Modified: Fri, 21 Mar 2025 16:22:27 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188bb3f059b8ea7cfec62ad169d26e9b95bbf8311fa61042191848b329f65dfe`  
		Last Modified: Fri, 21 Mar 2025 16:22:27 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:11601907779dec8338f13f7a26ef2c20e842769da70018f5c264310780bc52cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9cf004b304fbb7d46ae27452055636fe5c7c62dbfe692ff61892383a0052df`

```dockerfile
```

-	Layers:
	-	`sha256:93d220916fd441f64838b89a06184e7483b31bbba8351aa04f529eec8243fe31`  
		Last Modified: Fri, 21 Mar 2025 16:22:26 GMT  
		Size: 5.2 MB (5152391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2341e0eee0b9cf46bd405961c7f2cf64f17c7648853002898ce6a284c67e7902`  
		Last Modified: Fri, 21 Mar 2025 16:22:25 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json
