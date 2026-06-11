<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.0`](#crate60)
-	[`crate:6.0.7`](#crate607)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.4`](#crate614)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.9`](#crate629)
-	[`crate:6.3`](#crate63)
-	[`crate:6.3.3`](#crate633)
-	[`crate:latest`](#cratelatest)

## `crate:6.0`

```console
$ docker pull crate@sha256:cc3fe799ebd2f29e215d6de6f93f54177bcc9417b95c1f1eefcbbff8668663c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:a321d5b46c2634a265e4888aa64cb080ef745397183398ae160d4e2a69351f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244569300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cc9b32757dd31ee2f721d730d60df4cd72c4c257fc514b114482dede7dab66`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:07:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.7.tar.gz.asc crate-6.0.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.7.tar.gz.asc     && tar -xf crate-6.0.7.tar.gz -C /crate --strip-components=1     && rm crate-6.0.7.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:10 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:10 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:10 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:10 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-09T10:39:03.498747+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.7
# Thu, 11 Jun 2026 19:07:10 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c711948fb4110e45f618b3b3a533059eff1bf9295c1cc41e547c33af5be66`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 18.2 MB (18206135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac24950efde76115158a007e2775634c7f0f0debbb8e4c6eba6678d0c74804c`  
		Last Modified: Thu, 11 Jun 2026 19:07:33 GMT  
		Size: 149.0 MB (149020351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a9588e94031567b495842c2839cd3a65b68698025c6ace7b25ada0fa4c325b`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 8.8 MB (8787933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471dd6e55bd4d530e23c8704b398fc26c54fe1422fea135ada359ef4db30d256`  
		Last Modified: Thu, 11 Jun 2026 19:07:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ccf4607b9623c0156a86969c11c9375fcb9ea9d7172c8c6970143c4fb157ec`  
		Last Modified: Thu, 11 Jun 2026 19:07:30 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c57467152718a0f4662579702cee3b4dbb2f7c215361d25651b5bb31f5435cb`  
		Last Modified: Thu, 11 Jun 2026 19:07:30 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a28c4b907e2d082b39effceb4e972f7ea04361c8fa43021a8bb07ea8a540ce`  
		Last Modified: Thu, 11 Jun 2026 19:07:31 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:5983b938d541eed4d6ab55a77e28a1491820a6014d14e19b4e1b493b4f173f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e57729f05b0fe465094cfd9813904b4e3915916e72493930ba82d76e587862`

```dockerfile
```

-	Layers:
	-	`sha256:767174739348b643012a1149d3b7f526ca871f5ee3b2112c492825c6aa5e5232`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 6.7 MB (6652307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a52cc69986ee679da1de97563f5a451c6e0ac774b9a0b3e307d736bd8e1d997`  
		Last Modified: Thu, 11 Jun 2026 19:07:28 GMT  
		Size: 21.3 KB (21343 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6cf3ee37cb7a6fd75ec02bf2c9006497cd5f86fd95194ee71f5d35a3b65d0e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243888573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fcaff9a0df848e0fb7cd0541f557d1dada2e15edf963c9ebb61d538f23ab8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:45 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:06:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.7.tar.gz.asc crate-6.0.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.7.tar.gz.asc     && tar -xf crate-6.0.7.tar.gz -C /crate --strip-components=1     && rm crate-6.0.7.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:01 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-09T10:39:03.498747+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.7
# Thu, 11 Jun 2026 19:07:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3057bba23eb1d45d847a5bbc9d2b0534c22818ed9210c7f426266ba09506d9a8`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 18.3 MB (18255591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b9b27e145fc10e6de8685f6420a6fbc9f3e808108562ad6264e092676a11b`  
		Last Modified: Thu, 11 Jun 2026 19:07:24 GMT  
		Size: 149.7 MB (149712738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f0e3c37556b8e94a9117e4719d7d7d28be0dc467f64ba2c90c1d2547819fe7`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 8.8 MB (8785181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263248e7b99493ac7cb28c1729684fb8610fb006f07a6158fc3ae17212e6dfdb`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f55a660fd9b9d004b7293a0adad781ace9edc661cd3bf7943f7e96d75ac4919`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292eeaf85963ddafe1c41665b83f541c2f7a1bb6c7a6d3d2e6e9570793434b9d`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4788a1f3966001274574e071036a9a4a5d0a24b53b78552e27500b7a6911d9`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:adf7ccef70f686331fedb8ec41606ce96aa93ec5dae9f6be66410570bb39a235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3db803e70e054b44e4e85ab0c6baeef99eb117c035ccfbc69a7509d6f8fd2b4`

```dockerfile
```

-	Layers:
	-	`sha256:bc1c5b361587e94b786b11e6ba2ec388299c4f79798e03cc5a64a4ff552f6e65`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 6.7 MB (6650219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb32ef54e456749c047be65ae8249d99d88f1bef8c18e5fb702042107a29943`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.7`

```console
$ docker pull crate@sha256:cc3fe799ebd2f29e215d6de6f93f54177bcc9417b95c1f1eefcbbff8668663c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.7` - linux; amd64

```console
$ docker pull crate@sha256:a321d5b46c2634a265e4888aa64cb080ef745397183398ae160d4e2a69351f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244569300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cc9b32757dd31ee2f721d730d60df4cd72c4c257fc514b114482dede7dab66`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:07:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.7.tar.gz.asc crate-6.0.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.7.tar.gz.asc     && tar -xf crate-6.0.7.tar.gz -C /crate --strip-components=1     && rm crate-6.0.7.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:10 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:10 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:10 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:10 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:10 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-09T10:39:03.498747+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.7
# Thu, 11 Jun 2026 19:07:10 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c711948fb4110e45f618b3b3a533059eff1bf9295c1cc41e547c33af5be66`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 18.2 MB (18206135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac24950efde76115158a007e2775634c7f0f0debbb8e4c6eba6678d0c74804c`  
		Last Modified: Thu, 11 Jun 2026 19:07:33 GMT  
		Size: 149.0 MB (149020351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a9588e94031567b495842c2839cd3a65b68698025c6ace7b25ada0fa4c325b`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 8.8 MB (8787933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471dd6e55bd4d530e23c8704b398fc26c54fe1422fea135ada359ef4db30d256`  
		Last Modified: Thu, 11 Jun 2026 19:07:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ccf4607b9623c0156a86969c11c9375fcb9ea9d7172c8c6970143c4fb157ec`  
		Last Modified: Thu, 11 Jun 2026 19:07:30 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c57467152718a0f4662579702cee3b4dbb2f7c215361d25651b5bb31f5435cb`  
		Last Modified: Thu, 11 Jun 2026 19:07:30 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a28c4b907e2d082b39effceb4e972f7ea04361c8fa43021a8bb07ea8a540ce`  
		Last Modified: Thu, 11 Jun 2026 19:07:31 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.7` - unknown; unknown

```console
$ docker pull crate@sha256:5983b938d541eed4d6ab55a77e28a1491820a6014d14e19b4e1b493b4f173f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e57729f05b0fe465094cfd9813904b4e3915916e72493930ba82d76e587862`

```dockerfile
```

-	Layers:
	-	`sha256:767174739348b643012a1149d3b7f526ca871f5ee3b2112c492825c6aa5e5232`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 6.7 MB (6652307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a52cc69986ee679da1de97563f5a451c6e0ac774b9a0b3e307d736bd8e1d997`  
		Last Modified: Thu, 11 Jun 2026 19:07:28 GMT  
		Size: 21.3 KB (21343 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6cf3ee37cb7a6fd75ec02bf2c9006497cd5f86fd95194ee71f5d35a3b65d0e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243888573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fcaff9a0df848e0fb7cd0541f557d1dada2e15edf963c9ebb61d538f23ab8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:45 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:06:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.7.tar.gz.asc crate-6.0.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.7.tar.gz.asc     && tar -xf crate-6.0.7.tar.gz -C /crate --strip-components=1     && rm crate-6.0.7.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:01 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-09T10:39:03.498747+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.7
# Thu, 11 Jun 2026 19:07:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3057bba23eb1d45d847a5bbc9d2b0534c22818ed9210c7f426266ba09506d9a8`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 18.3 MB (18255591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b9b27e145fc10e6de8685f6420a6fbc9f3e808108562ad6264e092676a11b`  
		Last Modified: Thu, 11 Jun 2026 19:07:24 GMT  
		Size: 149.7 MB (149712738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f0e3c37556b8e94a9117e4719d7d7d28be0dc467f64ba2c90c1d2547819fe7`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 8.8 MB (8785181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263248e7b99493ac7cb28c1729684fb8610fb006f07a6158fc3ae17212e6dfdb`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f55a660fd9b9d004b7293a0adad781ace9edc661cd3bf7943f7e96d75ac4919`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292eeaf85963ddafe1c41665b83f541c2f7a1bb6c7a6d3d2e6e9570793434b9d`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4788a1f3966001274574e071036a9a4a5d0a24b53b78552e27500b7a6911d9`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.7` - unknown; unknown

```console
$ docker pull crate@sha256:adf7ccef70f686331fedb8ec41606ce96aa93ec5dae9f6be66410570bb39a235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3db803e70e054b44e4e85ab0c6baeef99eb117c035ccfbc69a7509d6f8fd2b4`

```dockerfile
```

-	Layers:
	-	`sha256:bc1c5b361587e94b786b11e6ba2ec388299c4f79798e03cc5a64a4ff552f6e65`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 6.7 MB (6650219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb32ef54e456749c047be65ae8249d99d88f1bef8c18e5fb702042107a29943`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:753365db9731e36a877cfe96ea6fbb0d3ee1b40313d8da3535c221a79f139e82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:2e3b4a7a39737a7cc2f921b44395a658323cbc70a54693108341e7dde443d6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243678500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666dafbab0339a15e8ef0d0c31f52f0eaf487114093d542020b6da8918ac97d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:19 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:19 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:19 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:19 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 02 Jun 2026 19:07:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e052d92adf7148aa9b835ffddf93fd54630929c5fefd071bad70925a3547f50`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 18.2 MB (18205737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f83a0481b4e877a894f65fc03ad961007450d38e01235244e33426bc4cc48a`  
		Last Modified: Tue, 02 Jun 2026 19:07:39 GMT  
		Size: 149.1 MB (149148315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1132439d4a63d1deb1b2a925b2500914d1e8d5727d35c71e033838b724279831`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 7.8 MB (7769569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d717ddb753565ae6d8b2918b13ac52f0d3903351c218e46bb0446828ddef01`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2afb107c94b753ea1c981b2a7cbaf9310a489f1ddcf71d46e2febf804ae9a`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a753e2c8492466ff3aa70d0b771c786a8d730afa752dbfb7917f7b64a58fc5`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6147fb3832c464a244e72eb85da6e203a94e91b2726459b815c7dc046fcee364`  
		Last Modified: Tue, 02 Jun 2026 19:07:38 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:c336c6de0c164564a37a441b2031b02330af91669a966c2e33708820506f5c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6574bc5a7a5acfe60c8ed9a4cf97f72574400c0fe825bc669958ab8f05529fc8`

```dockerfile
```

-	Layers:
	-	`sha256:d304293455deedbad9d30318e5cdf785eaa0d2ae9385cf969a1f8294c44bb63d`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 6.7 MB (6651083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9dcd647a21a4ab9197c17637c6b1cb3fad73fff3a4eb13b82b09385a1618424`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:eef0870a7d8fa8aaf2bf2c62c1671848f0117740852678ead325e0d9582c0948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242995244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e538fc1619dd443946fc09df4612b3a6a30f34aa0b22a0060995cbfd8c7aca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:39 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:39 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:39 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:39 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:39 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 02 Jun 2026 19:07:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88506b1de13c16a213e6a3b4f0711aa96d74476f569e561548a2f9989d4ea48b`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 18.3 MB (18256355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4c930f405362f947670cdf0f3bafda81e3fe3d3d89b375150cece8aa54a55b`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 149.8 MB (149838687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23ac36343d380d856b7e9a0930da0b1c6cec4dd888c9fae02e1d1a21ea13d15`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 7.8 MB (7765143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5219489f75d85cfc703ef97fe3d55281174720c7f6999ca5231c4226704f0f`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2676ec0bb7378a497c644e2191271e47101600767d83327d3edb559c6a9cc7`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5dec100a8744c89c3d7864a55c571c949dfbd1094ba32fd6e3d6e07867ac54`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66510f3c681343e67232ceb7f1213b24c9e4c486dd798ef6c2fa046ad28658c1`  
		Last Modified: Tue, 02 Jun 2026 19:08:00 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:13b95e1897aed537996abca63c4f5e326f89616ea4fdaef06ae3586dbc3c6233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf792062332f44bb4c8d5fd4378ecc8a3f424c653314ba217d9a8a5691b6236`

```dockerfile
```

-	Layers:
	-	`sha256:cec2eaf56c130c25a32d8d95aa74a4039c8e97503b04a5e6182db6b390179440`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 6.6 MB (6648995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c24d9590dee1bacb7cd5f5c9a99dc979d002b0f6a60efb8aa3c8f8958d4bd3`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.4`

```console
$ docker pull crate@sha256:753365db9731e36a877cfe96ea6fbb0d3ee1b40313d8da3535c221a79f139e82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.4` - linux; amd64

```console
$ docker pull crate@sha256:2e3b4a7a39737a7cc2f921b44395a658323cbc70a54693108341e7dde443d6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243678500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666dafbab0339a15e8ef0d0c31f52f0eaf487114093d542020b6da8918ac97d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:04 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:16 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:19 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:19 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:19 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:19 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:19 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 02 Jun 2026 19:07:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:19 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e052d92adf7148aa9b835ffddf93fd54630929c5fefd071bad70925a3547f50`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 18.2 MB (18205737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f83a0481b4e877a894f65fc03ad961007450d38e01235244e33426bc4cc48a`  
		Last Modified: Tue, 02 Jun 2026 19:07:39 GMT  
		Size: 149.1 MB (149148315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1132439d4a63d1deb1b2a925b2500914d1e8d5727d35c71e033838b724279831`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 7.8 MB (7769569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d717ddb753565ae6d8b2918b13ac52f0d3903351c218e46bb0446828ddef01`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2afb107c94b753ea1c981b2a7cbaf9310a489f1ddcf71d46e2febf804ae9a`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a753e2c8492466ff3aa70d0b771c786a8d730afa752dbfb7917f7b64a58fc5`  
		Last Modified: Tue, 02 Jun 2026 19:07:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6147fb3832c464a244e72eb85da6e203a94e91b2726459b815c7dc046fcee364`  
		Last Modified: Tue, 02 Jun 2026 19:07:38 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:c336c6de0c164564a37a441b2031b02330af91669a966c2e33708820506f5c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6574bc5a7a5acfe60c8ed9a4cf97f72574400c0fe825bc669958ab8f05529fc8`

```dockerfile
```

-	Layers:
	-	`sha256:d304293455deedbad9d30318e5cdf785eaa0d2ae9385cf969a1f8294c44bb63d`  
		Last Modified: Tue, 02 Jun 2026 19:07:36 GMT  
		Size: 6.7 MB (6651083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9dcd647a21a4ab9197c17637c6b1cb3fad73fff3a4eb13b82b09385a1618424`  
		Last Modified: Tue, 02 Jun 2026 19:07:35 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:eef0870a7d8fa8aaf2bf2c62c1671848f0117740852678ead325e0d9582c0948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242995244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e538fc1619dd443946fc09df4612b3a6a30f34aa0b22a0060995cbfd8c7aca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:39 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 02 Jun 2026 19:07:39 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
VOLUME [/data]
# Tue, 02 Jun 2026 19:07:39 GMT
WORKDIR /data
# Tue, 02 Jun 2026 19:07:39 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 02 Jun 2026 19:07:39 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Tue, 02 Jun 2026 19:07:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88506b1de13c16a213e6a3b4f0711aa96d74476f569e561548a2f9989d4ea48b`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 18.3 MB (18256355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4c930f405362f947670cdf0f3bafda81e3fe3d3d89b375150cece8aa54a55b`  
		Last Modified: Tue, 02 Jun 2026 19:08:01 GMT  
		Size: 149.8 MB (149838687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23ac36343d380d856b7e9a0930da0b1c6cec4dd888c9fae02e1d1a21ea13d15`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 7.8 MB (7765143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5219489f75d85cfc703ef97fe3d55281174720c7f6999ca5231c4226704f0f`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2676ec0bb7378a497c644e2191271e47101600767d83327d3edb559c6a9cc7`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5dec100a8744c89c3d7864a55c571c949dfbd1094ba32fd6e3d6e07867ac54`  
		Last Modified: Tue, 02 Jun 2026 19:07:59 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66510f3c681343e67232ceb7f1213b24c9e4c486dd798ef6c2fa046ad28658c1`  
		Last Modified: Tue, 02 Jun 2026 19:08:00 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:13b95e1897aed537996abca63c4f5e326f89616ea4fdaef06ae3586dbc3c6233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf792062332f44bb4c8d5fd4378ecc8a3f424c653314ba217d9a8a5691b6236`

```dockerfile
```

-	Layers:
	-	`sha256:cec2eaf56c130c25a32d8d95aa74a4039c8e97503b04a5e6182db6b390179440`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 6.6 MB (6648995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c24d9590dee1bacb7cd5f5c9a99dc979d002b0f6a60efb8aa3c8f8958d4bd3`  
		Last Modified: Tue, 02 Jun 2026 19:07:57 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2`

```console
$ docker pull crate@sha256:ba6cd569612ea8e4b6d22aa08c8a5138b28f3107c3b02fae5daeba7dd489f006
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:6132362595dfbe7206fb4d978906b2695dc494e385715a58be28f33cce909e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246881939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6590fd2b69293954dee94f5e77ff0f6898d67461c03477ccc72c35e95c89fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:07:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.9.tar.gz.asc crate-6.2.9.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.9.tar.gz.asc     && tar -xf crate-6.2.9.tar.gz -C /crate --strip-components=1     && rm crate-6.2.9.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:09 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T09:59:55.856088+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.9
# Thu, 11 Jun 2026 19:07:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c975638391721f537bd1eeb4096d07eda00984eb1ee492d3bba41e55bf0aa`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 18.2 MB (18206147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3d8ecc2ecf03e550368751a7b877c5cbeae58f54a2f7bbe1fd1d88ec1d2a0b`  
		Last Modified: Thu, 11 Jun 2026 19:07:32 GMT  
		Size: 151.3 MB (151333038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabc3731c6525b60646930070e270626863fd0a80cfc839b8699a8b64df7babc`  
		Last Modified: Thu, 11 Jun 2026 19:07:28 GMT  
		Size: 8.8 MB (8787872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471dd6e55bd4d530e23c8704b398fc26c54fe1422fea135ada359ef4db30d256`  
		Last Modified: Thu, 11 Jun 2026 19:07:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2bb743a78032fc6953c3551dabfa2ef733fb9cbe8bcbe39b21b240715788d0`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90d79a6c79e114e5b8620fc0af2e7b0f13e44e6629fb05b24fd2c34b15944aa`  
		Last Modified: Thu, 11 Jun 2026 19:07:30 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3584ae0643d237a89a70a09851dc284160e337a0e4848856846efbe9274bcc`  
		Last Modified: Thu, 11 Jun 2026 19:07:30 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:17277f0ad8294049405c2bfc1e644eb5b9a94c538d3a19fa4e6e76920ad94917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6677963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d7f6737b647bab0f4028325197c346f4aa5020a577650bdc8d36d8748fbe88`

```dockerfile
```

-	Layers:
	-	`sha256:6f7347b4baee4f047b1a75fe6515f1960d00c2f446b2654b6a257d9edc51b623`  
		Last Modified: Thu, 11 Jun 2026 19:07:28 GMT  
		Size: 6.7 MB (6656619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c909c55ab88f2eb1f817d1e5d3ea9113d5f865a27ed624db642f1e79b02a36b0`  
		Last Modified: Thu, 11 Jun 2026 19:07:27 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:33f7292c948b8232b7513320e6ed1d842325ceb8c96d063b30ea9b491e6b42e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243477005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f8abd9eb965e5117e977269a8444f9393fb597f5a9fd3c1201e3df2f019ee3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:07:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:07:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.9.tar.gz.asc crate-6.2.9.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.9.tar.gz.asc     && tar -xf crate-6.2.9.tar.gz -C /crate --strip-components=1     && rm crate-6.2.9.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:30 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:30 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:30 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:30 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:30 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T09:59:55.856088+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.9
# Thu, 11 Jun 2026 19:07:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:30 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9176b7524c8754da59e56678b69e66c7c0a11b168714495464e09095f90b946`  
		Last Modified: Thu, 11 Jun 2026 19:07:51 GMT  
		Size: 18.3 MB (18255587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bc3a53dd1760f4bb8043bf3e0ff14c7a310364e0d360864b5ca8e97c467703`  
		Last Modified: Thu, 11 Jun 2026 19:07:54 GMT  
		Size: 149.3 MB (149301293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4991ae33234d0cf41c1aa3ef4c6ac265d2570e6589c63ab4b3b5001157dfad08`  
		Last Modified: Thu, 11 Jun 2026 19:07:50 GMT  
		Size: 8.8 MB (8785066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980dd6e48760356dbc7a08cb2449f2a10156c3d88ee5735440b03c5b0d33f6a`  
		Last Modified: Thu, 11 Jun 2026 19:07:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ef5f127a4f74c27912c48a28ce6e727471bf85d9c02b1423c5bce35a79e2f2`  
		Last Modified: Thu, 11 Jun 2026 19:07:51 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd5f635f45d27c91f1b582fefac5c5eae8f1a94b9f10260a4cfbd4851296a0f`  
		Last Modified: Thu, 11 Jun 2026 19:07:52 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120e3e8ed6eb7f3b6d86e6281fdcd61e9bc59bb050a51b47de759ca8a5509b5e`  
		Last Modified: Thu, 11 Jun 2026 19:07:52 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:78fcb489bf1e2ddfc265247af18bf256bf6dd4d270ebca04aca7091f8bc88a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f204dca07d8d471402d250cbf0999b74227f522f02623e942a65a914dbec18`

```dockerfile
```

-	Layers:
	-	`sha256:f0c7e631bfa79a4c5ce0f6bbd00fc1369f2cf0a5c55ee742153cb1ebe527aa3c`  
		Last Modified: Thu, 11 Jun 2026 19:07:50 GMT  
		Size: 6.7 MB (6654531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b132232f1b6daa527c9b8be24196b9d50c7907c0a53fedc59242299fc196e298`  
		Last Modified: Thu, 11 Jun 2026 19:07:50 GMT  
		Size: 21.5 KB (21468 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.9`

```console
$ docker pull crate@sha256:ba6cd569612ea8e4b6d22aa08c8a5138b28f3107c3b02fae5daeba7dd489f006
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.9` - linux; amd64

```console
$ docker pull crate@sha256:6132362595dfbe7206fb4d978906b2695dc494e385715a58be28f33cce909e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246881939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6590fd2b69293954dee94f5e77ff0f6898d67461c03477ccc72c35e95c89fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:07:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.9.tar.gz.asc crate-6.2.9.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.9.tar.gz.asc     && tar -xf crate-6.2.9.tar.gz -C /crate --strip-components=1     && rm crate-6.2.9.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:09 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:09 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:09 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:09 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:09 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T09:59:55.856088+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.9
# Thu, 11 Jun 2026 19:07:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:09 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c975638391721f537bd1eeb4096d07eda00984eb1ee492d3bba41e55bf0aa`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 18.2 MB (18206147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3d8ecc2ecf03e550368751a7b877c5cbeae58f54a2f7bbe1fd1d88ec1d2a0b`  
		Last Modified: Thu, 11 Jun 2026 19:07:32 GMT  
		Size: 151.3 MB (151333038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabc3731c6525b60646930070e270626863fd0a80cfc839b8699a8b64df7babc`  
		Last Modified: Thu, 11 Jun 2026 19:07:28 GMT  
		Size: 8.8 MB (8787872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471dd6e55bd4d530e23c8704b398fc26c54fe1422fea135ada359ef4db30d256`  
		Last Modified: Thu, 11 Jun 2026 19:07:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2bb743a78032fc6953c3551dabfa2ef733fb9cbe8bcbe39b21b240715788d0`  
		Last Modified: Thu, 11 Jun 2026 19:07:29 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90d79a6c79e114e5b8620fc0af2e7b0f13e44e6629fb05b24fd2c34b15944aa`  
		Last Modified: Thu, 11 Jun 2026 19:07:30 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3584ae0643d237a89a70a09851dc284160e337a0e4848856846efbe9274bcc`  
		Last Modified: Thu, 11 Jun 2026 19:07:30 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.9` - unknown; unknown

```console
$ docker pull crate@sha256:17277f0ad8294049405c2bfc1e644eb5b9a94c538d3a19fa4e6e76920ad94917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6677963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d7f6737b647bab0f4028325197c346f4aa5020a577650bdc8d36d8748fbe88`

```dockerfile
```

-	Layers:
	-	`sha256:6f7347b4baee4f047b1a75fe6515f1960d00c2f446b2654b6a257d9edc51b623`  
		Last Modified: Thu, 11 Jun 2026 19:07:28 GMT  
		Size: 6.7 MB (6656619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c909c55ab88f2eb1f817d1e5d3ea9113d5f865a27ed624db642f1e79b02a36b0`  
		Last Modified: Thu, 11 Jun 2026 19:07:27 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:33f7292c948b8232b7513320e6ed1d842325ceb8c96d063b30ea9b491e6b42e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243477005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f8abd9eb965e5117e977269a8444f9393fb597f5a9fd3c1201e3df2f019ee3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:07:14 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:07:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.9.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.9.tar.gz.asc crate-6.2.9.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.9.tar.gz.asc     && tar -xf crate-6.2.9.tar.gz -C /crate --strip-components=1     && rm crate-6.2.9.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:30 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:30 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:30 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:30 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:30 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T09:59:55.856088+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.9
# Thu, 11 Jun 2026 19:07:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:30 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9176b7524c8754da59e56678b69e66c7c0a11b168714495464e09095f90b946`  
		Last Modified: Thu, 11 Jun 2026 19:07:51 GMT  
		Size: 18.3 MB (18255587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bc3a53dd1760f4bb8043bf3e0ff14c7a310364e0d360864b5ca8e97c467703`  
		Last Modified: Thu, 11 Jun 2026 19:07:54 GMT  
		Size: 149.3 MB (149301293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4991ae33234d0cf41c1aa3ef4c6ac265d2570e6589c63ab4b3b5001157dfad08`  
		Last Modified: Thu, 11 Jun 2026 19:07:50 GMT  
		Size: 8.8 MB (8785066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980dd6e48760356dbc7a08cb2449f2a10156c3d88ee5735440b03c5b0d33f6a`  
		Last Modified: Thu, 11 Jun 2026 19:07:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ef5f127a4f74c27912c48a28ce6e727471bf85d9c02b1423c5bce35a79e2f2`  
		Last Modified: Thu, 11 Jun 2026 19:07:51 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd5f635f45d27c91f1b582fefac5c5eae8f1a94b9f10260a4cfbd4851296a0f`  
		Last Modified: Thu, 11 Jun 2026 19:07:52 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120e3e8ed6eb7f3b6d86e6281fdcd61e9bc59bb050a51b47de759ca8a5509b5e`  
		Last Modified: Thu, 11 Jun 2026 19:07:52 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.9` - unknown; unknown

```console
$ docker pull crate@sha256:78fcb489bf1e2ddfc265247af18bf256bf6dd4d270ebca04aca7091f8bc88a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6675999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f204dca07d8d471402d250cbf0999b74227f522f02623e942a65a914dbec18`

```dockerfile
```

-	Layers:
	-	`sha256:f0c7e631bfa79a4c5ce0f6bbd00fc1369f2cf0a5c55ee742153cb1ebe527aa3c`  
		Last Modified: Thu, 11 Jun 2026 19:07:50 GMT  
		Size: 6.7 MB (6654531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b132232f1b6daa527c9b8be24196b9d50c7907c0a53fedc59242299fc196e298`  
		Last Modified: Thu, 11 Jun 2026 19:07:50 GMT  
		Size: 21.5 KB (21468 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.3`

```console
$ docker pull crate@sha256:973c785501138da251815cf1dc19c395e80a94147ae7f8f785b8d7c1b8887920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.3` - linux; amd64

```console
$ docker pull crate@sha256:3978cfe1ac22f85f5781b9b72822cb083054a28aa8bf14b6f47ac978c8d661eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234624633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c811879bd013171143a4940b419f94411c5d5858d8ef01b748fa2c1988f7dacc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:06:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.3.tar.gz.asc crate-6.3.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.3.tar.gz.asc     && tar -xf crate-6.3.3.tar.gz -C /crate --strip-components=1     && rm crate-6.3.3.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:01 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T12:47:05.822670+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.3
# Thu, 11 Jun 2026 19:07:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa1806ec35a0d6398f5520aa37c1e8ea7891159ac2c221a9b7ad5f8d47728c0`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 18.2 MB (18206147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851e40ab878f9cc512f2b2132b1885bb32ea1d1b353acdcc3e11f9bf467704df`  
		Last Modified: Thu, 11 Jun 2026 19:07:23 GMT  
		Size: 139.1 MB (139075596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dfbe46a7c99c0edac86c6dadb94fa9c06a5d96f8be1f6e6e440bf6c3559a8f`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 8.8 MB (8788008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263248e7b99493ac7cb28c1729684fb8610fb006f07a6158fc3ae17212e6dfdb`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3490a183b1713390764d3d1667fbb4d4ee2b9b5df9368dd233986098e1cc382`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f63587515104608560b8d6a25920296cb80cc6f4a4805fd5948339baae90d05`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdb0a6d8cfbfa77257ee74a733773af044a6368e56813db44cec70641840cf`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3` - unknown; unknown

```console
$ docker pull crate@sha256:18bd83633c7ce2f6f22dbc64519bc4e3b672c71bcff94225d104d8d87ddd6e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bed11bef970c0d84f91cc1facf69dcdffaa5787f28484acd779d27b235caf9`

```dockerfile
```

-	Layers:
	-	`sha256:8b39162693384e9dc07661afd83ee58d8f5c7b7dc653e4f03ae830f41ef54880`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 6.6 MB (6606400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8234e28fd36ed98dd2e2a90225a25556cc3c56d8c37fbae840505e4988fb57`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8132a1b7faf18255e999fe86bd77273abf202405aa079ede0e58838ba2e9a674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231217597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd6bac745727eb6ab04d094a81d30408163969d563f4dc5e8b013c477da0898`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:06:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.3.tar.gz.asc crate-6.3.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.3.tar.gz.asc     && tar -xf crate-6.3.3.tar.gz -C /crate --strip-components=1     && rm crate-6.3.3.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:00 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:00 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:00 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:00 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T12:47:05.822670+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.3
# Thu, 11 Jun 2026 19:07:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:00 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0debbb59f1128849d84080aa7112fbed559626e82546f504b92ac2fefbfc97e1`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 18.3 MB (18255509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552683e066453c555f839dd355e9a34e69d541984e85a77f85e7180ccbaa3fa`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 137.0 MB (137042093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596b75ba99cecb206fb4f7f0b6641928bbd4da28353cdbb299eb39550b92630`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 8.8 MB (8784931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3b121cdb9821a0c73d0a301d4aebce299ee5f92313f082dbd6b97dbc5badc4`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc3d1b2ce3ef77b77a14e27d3dc2bf72136c176de35783754d3e6fc4f3e53e`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7e9628b7510cff9b6fdd3931b0014a05612ed8b134016f43650217f07a231d`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bab713511f560bf7b1c1015d63b783154a56374f4266ebfe3c08125abce7a1`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3` - unknown; unknown

```console
$ docker pull crate@sha256:c83146f72ad9092e314c19f6874eb1d1751a6ea49bafcc98053366c56a862aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b52acd8e07b865401aedb2e388ae3259aec67b7468f1f988d98640714dc04`

```dockerfile
```

-	Layers:
	-	`sha256:65f964dcbddc11660e484ae4bccd0a53f1295637099e1506a56e8db7e0780f4b`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 6.6 MB (6604324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20569144d3f7fbf9e9130a9d6e70dbad7956f8d444d33a52add843439ee616f`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.3.3`

```console
$ docker pull crate@sha256:973c785501138da251815cf1dc19c395e80a94147ae7f8f785b8d7c1b8887920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.3.3` - linux; amd64

```console
$ docker pull crate@sha256:3978cfe1ac22f85f5781b9b72822cb083054a28aa8bf14b6f47ac978c8d661eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234624633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c811879bd013171143a4940b419f94411c5d5858d8ef01b748fa2c1988f7dacc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:06:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.3.tar.gz.asc crate-6.3.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.3.tar.gz.asc     && tar -xf crate-6.3.3.tar.gz -C /crate --strip-components=1     && rm crate-6.3.3.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:01 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T12:47:05.822670+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.3
# Thu, 11 Jun 2026 19:07:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa1806ec35a0d6398f5520aa37c1e8ea7891159ac2c221a9b7ad5f8d47728c0`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 18.2 MB (18206147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851e40ab878f9cc512f2b2132b1885bb32ea1d1b353acdcc3e11f9bf467704df`  
		Last Modified: Thu, 11 Jun 2026 19:07:23 GMT  
		Size: 139.1 MB (139075596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dfbe46a7c99c0edac86c6dadb94fa9c06a5d96f8be1f6e6e440bf6c3559a8f`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 8.8 MB (8788008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263248e7b99493ac7cb28c1729684fb8610fb006f07a6158fc3ae17212e6dfdb`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3490a183b1713390764d3d1667fbb4d4ee2b9b5df9368dd233986098e1cc382`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f63587515104608560b8d6a25920296cb80cc6f4a4805fd5948339baae90d05`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdb0a6d8cfbfa77257ee74a733773af044a6368e56813db44cec70641840cf`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3.3` - unknown; unknown

```console
$ docker pull crate@sha256:18bd83633c7ce2f6f22dbc64519bc4e3b672c71bcff94225d104d8d87ddd6e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bed11bef970c0d84f91cc1facf69dcdffaa5787f28484acd779d27b235caf9`

```dockerfile
```

-	Layers:
	-	`sha256:8b39162693384e9dc07661afd83ee58d8f5c7b7dc653e4f03ae830f41ef54880`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 6.6 MB (6606400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8234e28fd36ed98dd2e2a90225a25556cc3c56d8c37fbae840505e4988fb57`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.3.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8132a1b7faf18255e999fe86bd77273abf202405aa079ede0e58838ba2e9a674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231217597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd6bac745727eb6ab04d094a81d30408163969d563f4dc5e8b013c477da0898`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:06:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.3.tar.gz.asc crate-6.3.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.3.tar.gz.asc     && tar -xf crate-6.3.3.tar.gz -C /crate --strip-components=1     && rm crate-6.3.3.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:00 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:00 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:00 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:00 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T12:47:05.822670+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.3
# Thu, 11 Jun 2026 19:07:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:00 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0debbb59f1128849d84080aa7112fbed559626e82546f504b92ac2fefbfc97e1`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 18.3 MB (18255509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552683e066453c555f839dd355e9a34e69d541984e85a77f85e7180ccbaa3fa`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 137.0 MB (137042093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596b75ba99cecb206fb4f7f0b6641928bbd4da28353cdbb299eb39550b92630`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 8.8 MB (8784931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3b121cdb9821a0c73d0a301d4aebce299ee5f92313f082dbd6b97dbc5badc4`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc3d1b2ce3ef77b77a14e27d3dc2bf72136c176de35783754d3e6fc4f3e53e`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7e9628b7510cff9b6fdd3931b0014a05612ed8b134016f43650217f07a231d`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bab713511f560bf7b1c1015d63b783154a56374f4266ebfe3c08125abce7a1`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.3.3` - unknown; unknown

```console
$ docker pull crate@sha256:c83146f72ad9092e314c19f6874eb1d1751a6ea49bafcc98053366c56a862aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b52acd8e07b865401aedb2e388ae3259aec67b7468f1f988d98640714dc04`

```dockerfile
```

-	Layers:
	-	`sha256:65f964dcbddc11660e484ae4bccd0a53f1295637099e1506a56e8db7e0780f4b`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 6.6 MB (6604324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20569144d3f7fbf9e9130a9d6e70dbad7956f8d444d33a52add843439ee616f`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:973c785501138da251815cf1dc19c395e80a94147ae7f8f785b8d7c1b8887920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:3978cfe1ac22f85f5781b9b72822cb083054a28aa8bf14b6f47ac978c8d661eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234624633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c811879bd013171143a4940b419f94411c5d5858d8ef01b748fa2c1988f7dacc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:12 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:53 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:06:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.3.tar.gz.asc crate-6.3.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.3.tar.gz.asc     && tar -xf crate-6.3.3.tar.gz -C /crate --strip-components=1     && rm crate-6.3.3.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:01 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T12:47:05.822670+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.3
# Thu, 11 Jun 2026 19:07:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e787432b3044759d693031c5b5b1f432cb4b7cc6c8f9d21577a5906dd5e538c5`  
		Last Modified: Tue, 02 Jun 2026 19:04:29 GMT  
		Size: 68.6 MB (68553003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa1806ec35a0d6398f5520aa37c1e8ea7891159ac2c221a9b7ad5f8d47728c0`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 18.2 MB (18206147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851e40ab878f9cc512f2b2132b1885bb32ea1d1b353acdcc3e11f9bf467704df`  
		Last Modified: Thu, 11 Jun 2026 19:07:23 GMT  
		Size: 139.1 MB (139075596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dfbe46a7c99c0edac86c6dadb94fa9c06a5d96f8be1f6e6e440bf6c3559a8f`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 8.8 MB (8788008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263248e7b99493ac7cb28c1729684fb8610fb006f07a6158fc3ae17212e6dfdb`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3490a183b1713390764d3d1667fbb4d4ee2b9b5df9368dd233986098e1cc382`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f63587515104608560b8d6a25920296cb80cc6f4a4805fd5948339baae90d05`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdb0a6d8cfbfa77257ee74a733773af044a6368e56813db44cec70641840cf`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:18bd83633c7ce2f6f22dbc64519bc4e3b672c71bcff94225d104d8d87ddd6e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bed11bef970c0d84f91cc1facf69dcdffaa5787f28484acd779d27b235caf9`

```dockerfile
```

-	Layers:
	-	`sha256:8b39162693384e9dc07661afd83ee58d8f5c7b7dc653e4f03ae830f41ef54880`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 6.6 MB (6606400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8234e28fd36ed98dd2e2a90225a25556cc3c56d8c37fbae840505e4988fb57`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:8132a1b7faf18255e999fe86bd77273abf202405aa079ede0e58838ba2e9a674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231217597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd6bac745727eb6ab04d094a81d30408163969d563f4dc5e8b013c477da0898`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:17 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:17 GMT
CMD ["/bin/bash"]
# Thu, 11 Jun 2026 19:06:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 11 Jun 2026 19:06:56 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.3.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.3.3.tar.gz.asc crate-6.3.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.3.3.tar.gz.asc     && tar -xf crate-6.3.3.tar.gz -C /crate --strip-components=1     && rm crate-6.3.3.tar.gz # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 19:07:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 11 Jun 2026 19:07:00 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
VOLUME [/data]
# Thu, 11 Jun 2026 19:07:00 GMT
WORKDIR /data
# Thu, 11 Jun 2026 19:07:00 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 11 Jun 2026 19:07:00 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-06-08T12:47:05.822670+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.3.3
# Thu, 11 Jun 2026 19:07:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 19:07:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 19:07:00 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:f4e642e2dc39d48325d258aab2be76368a8810b551698a78f8de70b4d572f710`  
		Last Modified: Tue, 02 Jun 2026 19:04:33 GMT  
		Size: 67.1 MB (67133180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0debbb59f1128849d84080aa7112fbed559626e82546f504b92ac2fefbfc97e1`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 18.3 MB (18255509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552683e066453c555f839dd355e9a34e69d541984e85a77f85e7180ccbaa3fa`  
		Last Modified: Thu, 11 Jun 2026 19:07:22 GMT  
		Size: 137.0 MB (137042093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596b75ba99cecb206fb4f7f0b6641928bbd4da28353cdbb299eb39550b92630`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 8.8 MB (8784931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3b121cdb9821a0c73d0a301d4aebce299ee5f92313f082dbd6b97dbc5badc4`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc3d1b2ce3ef77b77a14e27d3dc2bf72136c176de35783754d3e6fc4f3e53e`  
		Last Modified: Thu, 11 Jun 2026 19:07:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7e9628b7510cff9b6fdd3931b0014a05612ed8b134016f43650217f07a231d`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bab713511f560bf7b1c1015d63b783154a56374f4266ebfe3c08125abce7a1`  
		Last Modified: Thu, 11 Jun 2026 19:07:21 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:c83146f72ad9092e314c19f6874eb1d1751a6ea49bafcc98053366c56a862aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6626101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b52acd8e07b865401aedb2e388ae3259aec67b7468f1f988d98640714dc04`

```dockerfile
```

-	Layers:
	-	`sha256:65f964dcbddc11660e484ae4bccd0a53f1295637099e1506a56e8db7e0780f4b`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 6.6 MB (6604324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20569144d3f7fbf9e9130a9d6e70dbad7956f8d444d33a52add843439ee616f`  
		Last Modified: Thu, 11 Jun 2026 19:07:19 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
