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
		Last Modified: Mon, 17 Feb 2025 19:09:11 GMT  
		Size: 23.3 KB (23285 bytes)  
		MIME: application/vnd.in-toto+json
