<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:6.0`](#crate60)
-	[`crate:6.0.6`](#crate606)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.4`](#crate614)
-	[`crate:6.2`](#crate62)
-	[`crate:6.2.7`](#crate627)
-	[`crate:latest`](#cratelatest)

## `crate:6.0`

```console
$ docker pull crate@sha256:e53431ac81272fd94cf0c08a95373c462f5dc3d079f6c6494346dd585a368e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:ee9e676fea4b4452055643c62a9b0efadf7a2348709ce27b9b6d43c0a34089ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243713222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce29deef433ecfd886e6e0f90536add834c85e04c511a47254b609efb8267910`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:53 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:30 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 04 May 2026 20:46:47 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:46:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:46:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:46:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:46:47 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:46:47 GMT
WORKDIR /data
# Mon, 04 May 2026 20:46:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:46:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:46:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:46:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 04 May 2026 20:46:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:46:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:46:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1f3c9b769bded38c7c4e291e2a502ac107500084472a144cb5542844ac4b66a8`  
		Last Modified: Mon, 04 May 2026 20:41:10 GMT  
		Size: 68.6 MB (68568777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8840ec00c5adf1017467c8161eb17971b966cadae9b7c1fccb959686a06a4f`  
		Last Modified: Mon, 04 May 2026 20:47:07 GMT  
		Size: 18.4 MB (18371232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bfe6dc3c3e8c1bb2cfe671440068cf519ea730a294442ca0afb0b5b1c68c`  
		Last Modified: Mon, 04 May 2026 20:47:10 GMT  
		Size: 149.0 MB (149020497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcbb52bca905fe002d461a148102e53ca6e903611a5acaba93a25d7d32d06bd`  
		Last Modified: Mon, 04 May 2026 20:47:06 GMT  
		Size: 7.8 MB (7750838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36ae47efb0d53fb32f5e4c12454cc32e6e134b05c1a85bef784eb507684afea`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd80fcc3aeb915756752c65896b29b020cf41c54482ca8554a6cad4aa952a0f`  
		Last Modified: Mon, 04 May 2026 20:47:07 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0cf244745299977376fe9920f55644ecafed11ed5481c9e3add306f9097a4c`  
		Last Modified: Mon, 04 May 2026 20:47:07 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c6112cf544ac55bafe9615466f77dd593dc7079251ff7d117360dd1275fe9`  
		Last Modified: Mon, 04 May 2026 20:47:08 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:a65f4c2331cf7e010d466e9986b7ce37871caded63bbef0714db5483da6fdd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33949f59fb18f8ec3498c96162932f49b063fcdc7e0bea7e1d39b5e5d2a3227b`

```dockerfile
```

-	Layers:
	-	`sha256:06c97c271d03cf1bd63d7739f6ca75898a9ca6aae12ba44dc12ddd6176c4b85b`  
		Last Modified: Mon, 04 May 2026 20:47:06 GMT  
		Size: 6.7 MB (6652281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb061e849b0bb0850273ffb9f7fa52a6ebb283d42052a1f6c100339f73a9fa5`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:71eedfe1c27bdab829645b27be58415a6983ac32009d7289eb97745ce150baf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243044051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11954d63cca26a823283b215f052485d7aed1006e04ca1ad738fdaa05d467089`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:24 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:24 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:50 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:47:03 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 04 May 2026 20:47:06 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:47:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:47:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:47:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:47:06 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:47:06 GMT
WORKDIR /data
# Mon, 04 May 2026 20:47:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:47:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:47:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:47:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 04 May 2026 20:47:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:47:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:47:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2fb29370f1d8bb35e2d2cd7d7725eeaa5a9460517381edc86fc3a163d6ec8248`  
		Last Modified: Mon, 04 May 2026 20:40:41 GMT  
		Size: 67.2 MB (67153935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35380c232da6988620f3b068f79e8830391c6aeb8c5225d53176b965f3c1c162`  
		Last Modified: Mon, 04 May 2026 20:47:27 GMT  
		Size: 18.4 MB (18424036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf2d9c41b8e48f7bf1335f404c9e8d8e0d89e7cdf33c18ec56c0065cc04ec0`  
		Last Modified: Mon, 04 May 2026 20:47:30 GMT  
		Size: 149.7 MB (149712775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2bfd6c21ba797e6f453061bcd38436853312039da01c918cc65e22e9a4924d`  
		Last Modified: Mon, 04 May 2026 20:47:26 GMT  
		Size: 7.8 MB (7751428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705095e4d79b96ad166a8eff93aaa3cb4b3f2a0a841a0f9c53919b66ca22aa85`  
		Last Modified: Mon, 04 May 2026 20:47:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1785c85230d4cb9c6f8f0174df7ac23e713d6fae728d32aa4e64892521e767b`  
		Last Modified: Mon, 04 May 2026 20:47:27 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4419a2b75ea1a39150e82194af36592fc8900592b1c9941c3451d85f71688ed6`  
		Last Modified: Mon, 04 May 2026 20:47:27 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849ed0444999f7470cedd055552156f1031e19e4806e16dc8930cfb6905ee76d`  
		Last Modified: Mon, 04 May 2026 20:47:28 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:b9c22421308e54b3a9a7a22b1555099aed393f5fcd694c57576659a742372cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83ef49b55f52896a224445cb267318c4db9f3801357a4ed8c3c1e1ddfa8406a`

```dockerfile
```

-	Layers:
	-	`sha256:b1556acb31172873e08bfd20875b23733617356bdee26d4665e1a6ea0b07ae39`  
		Last Modified: Mon, 04 May 2026 20:47:26 GMT  
		Size: 6.7 MB (6650193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19bc82c7038c5ec02518ea14ec2a0544d11f25795d3ac5535f1f601b4734a819`  
		Last Modified: Mon, 04 May 2026 20:47:25 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.6`

```console
$ docker pull crate@sha256:e53431ac81272fd94cf0c08a95373c462f5dc3d079f6c6494346dd585a368e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.6` - linux; amd64

```console
$ docker pull crate@sha256:ee9e676fea4b4452055643c62a9b0efadf7a2348709ce27b9b6d43c0a34089ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243713222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce29deef433ecfd886e6e0f90536add834c85e04c511a47254b609efb8267910`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:53 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:30 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:44 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 04 May 2026 20:46:47 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:46:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:46:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:46:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:46:47 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:46:47 GMT
WORKDIR /data
# Mon, 04 May 2026 20:46:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:46:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:46:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:46:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 04 May 2026 20:46:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:46:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:46:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1f3c9b769bded38c7c4e291e2a502ac107500084472a144cb5542844ac4b66a8`  
		Last Modified: Mon, 04 May 2026 20:41:10 GMT  
		Size: 68.6 MB (68568777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8840ec00c5adf1017467c8161eb17971b966cadae9b7c1fccb959686a06a4f`  
		Last Modified: Mon, 04 May 2026 20:47:07 GMT  
		Size: 18.4 MB (18371232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bfe6dc3c3e8c1bb2cfe671440068cf519ea730a294442ca0afb0b5b1c68c`  
		Last Modified: Mon, 04 May 2026 20:47:10 GMT  
		Size: 149.0 MB (149020497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcbb52bca905fe002d461a148102e53ca6e903611a5acaba93a25d7d32d06bd`  
		Last Modified: Mon, 04 May 2026 20:47:06 GMT  
		Size: 7.8 MB (7750838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36ae47efb0d53fb32f5e4c12454cc32e6e134b05c1a85bef784eb507684afea`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd80fcc3aeb915756752c65896b29b020cf41c54482ca8554a6cad4aa952a0f`  
		Last Modified: Mon, 04 May 2026 20:47:07 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0cf244745299977376fe9920f55644ecafed11ed5481c9e3add306f9097a4c`  
		Last Modified: Mon, 04 May 2026 20:47:07 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c6112cf544ac55bafe9615466f77dd593dc7079251ff7d117360dd1275fe9`  
		Last Modified: Mon, 04 May 2026 20:47:08 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:a65f4c2331cf7e010d466e9986b7ce37871caded63bbef0714db5483da6fdd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33949f59fb18f8ec3498c96162932f49b063fcdc7e0bea7e1d39b5e5d2a3227b`

```dockerfile
```

-	Layers:
	-	`sha256:06c97c271d03cf1bd63d7739f6ca75898a9ca6aae12ba44dc12ddd6176c4b85b`  
		Last Modified: Mon, 04 May 2026 20:47:06 GMT  
		Size: 6.7 MB (6652281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb061e849b0bb0850273ffb9f7fa52a6ebb283d42052a1f6c100339f73a9fa5`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:71eedfe1c27bdab829645b27be58415a6983ac32009d7289eb97745ce150baf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243044051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11954d63cca26a823283b215f052485d7aed1006e04ca1ad738fdaa05d467089`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:24 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:24 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:50 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:47:03 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.6.tar.gz.asc crate-6.0.6.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.6.tar.gz.asc     && tar -xf crate-6.0.6.tar.gz -C /crate --strip-components=1     && rm crate-6.0.6.tar.gz # buildkit
# Mon, 04 May 2026 20:47:06 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:47:06 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:47:06 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:47:06 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:47:06 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:47:06 GMT
WORKDIR /data
# Mon, 04 May 2026 20:47:06 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:47:06 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:47:06 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:47:06 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-16T19:16:05.319443+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.6
# Mon, 04 May 2026 20:47:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:47:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:47:06 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2fb29370f1d8bb35e2d2cd7d7725eeaa5a9460517381edc86fc3a163d6ec8248`  
		Last Modified: Mon, 04 May 2026 20:40:41 GMT  
		Size: 67.2 MB (67153935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35380c232da6988620f3b068f79e8830391c6aeb8c5225d53176b965f3c1c162`  
		Last Modified: Mon, 04 May 2026 20:47:27 GMT  
		Size: 18.4 MB (18424036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf2d9c41b8e48f7bf1335f404c9e8d8e0d89e7cdf33c18ec56c0065cc04ec0`  
		Last Modified: Mon, 04 May 2026 20:47:30 GMT  
		Size: 149.7 MB (149712775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2bfd6c21ba797e6f453061bcd38436853312039da01c918cc65e22e9a4924d`  
		Last Modified: Mon, 04 May 2026 20:47:26 GMT  
		Size: 7.8 MB (7751428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705095e4d79b96ad166a8eff93aaa3cb4b3f2a0a841a0f9c53919b66ca22aa85`  
		Last Modified: Mon, 04 May 2026 20:47:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1785c85230d4cb9c6f8f0174df7ac23e713d6fae728d32aa4e64892521e767b`  
		Last Modified: Mon, 04 May 2026 20:47:27 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4419a2b75ea1a39150e82194af36592fc8900592b1c9941c3451d85f71688ed6`  
		Last Modified: Mon, 04 May 2026 20:47:27 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849ed0444999f7470cedd055552156f1031e19e4806e16dc8930cfb6905ee76d`  
		Last Modified: Mon, 04 May 2026 20:47:28 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.6` - unknown; unknown

```console
$ docker pull crate@sha256:b9c22421308e54b3a9a7a22b1555099aed393f5fcd694c57576659a742372cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83ef49b55f52896a224445cb267318c4db9f3801357a4ed8c3c1e1ddfa8406a`

```dockerfile
```

-	Layers:
	-	`sha256:b1556acb31172873e08bfd20875b23733617356bdee26d4665e1a6ea0b07ae39`  
		Last Modified: Mon, 04 May 2026 20:47:26 GMT  
		Size: 6.7 MB (6650193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19bc82c7038c5ec02518ea14ec2a0544d11f25795d3ac5535f1f601b4734a819`  
		Last Modified: Mon, 04 May 2026 20:47:25 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:3d0592b1d2db912c63ff87e5b2097c3cca1c7c2e7948c3ea1cdb33c434a5c70f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:0d5ce12325dad1ca22750d0273a01ccf3632b0d93ac9defaafcd806ea6bd5faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243840791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f6c8a164acf3ae7a096eb547eb32138243f97bf1dd6eab0f7539a219eb01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:53 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:29 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 04 May 2026 20:46:45 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:46:46 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:46:46 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:46:46 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:46:46 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:46:46 GMT
WORKDIR /data
# Mon, 04 May 2026 20:46:46 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:46:46 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:46:46 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:46:46 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 04 May 2026 20:46:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:46:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:46:46 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1f3c9b769bded38c7c4e291e2a502ac107500084472a144cb5542844ac4b66a8`  
		Last Modified: Mon, 04 May 2026 20:41:10 GMT  
		Size: 68.6 MB (68568777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ddea547c24e358e3f5324b130177cf964dd4246ca0b0603a78e3cf9dc5d03d`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 18.4 MB (18371106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c891bb5c1fc4353c8cfe052bdfca0992b5ecdd866edac4013d0f0f49db7ac62`  
		Last Modified: Mon, 04 May 2026 20:47:08 GMT  
		Size: 149.1 MB (149148241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf137907f3c88cfcd076a87b4d6c805b77e4e3f95cf3b49883967038cf5e058`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 7.8 MB (7750791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd34387dce372dec6c8050b63f6d0b954ca8b57a96661a803942932b3db1e71f`  
		Last Modified: Mon, 04 May 2026 20:47:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a5a51682d24d650f61c97b9446b7c87771fcff38bc91ae51c78e8ee6b7327f`  
		Last Modified: Mon, 04 May 2026 20:47:06 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53a81ce07e29a47283742a0a2af611f48c073176e3ed17e8887b6b13019c337`  
		Last Modified: Mon, 04 May 2026 20:47:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8acf2460be8682a7186fe5f65a44bfd5653c753984018db2ee700df421d6f2`  
		Last Modified: Mon, 04 May 2026 20:47:07 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:e367a3a12dcf5854182e321130885a0f8f3b1a5b13ba399f3b593dd350ccdc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7714efa72d4972a70a5ce9fb748efd97df19e1c6a0603f811c814b8471180c8`

```dockerfile
```

-	Layers:
	-	`sha256:5d8bc752f1d414e177c3b4afd2565597059b0e25203ba6344b895c7f994c842d`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 6.7 MB (6651065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4867ab62f01f6c3e47d65b41b9e9f9f3e9aa63566a2ddbdbc4439c553cb03015`  
		Last Modified: Mon, 04 May 2026 20:47:04 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:110cd17bbbac492c4fb1d67db3fd27bbd1cbc5cf3163be7cf1505c5dddcf618b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243169688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca2d9bbac5d66afb38a1b056ab7a4ceb7845a165b066a9bc31c297bac399f5a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:24 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:24 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 04 May 2026 20:47:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:47:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:47:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:47:01 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:47:01 GMT
WORKDIR /data
# Mon, 04 May 2026 20:47:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:47:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 04 May 2026 20:47:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:47:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2fb29370f1d8bb35e2d2cd7d7725eeaa5a9460517381edc86fc3a163d6ec8248`  
		Last Modified: Mon, 04 May 2026 20:40:41 GMT  
		Size: 67.2 MB (67153935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109f3d50101a4b177880cca22d85b3d3461acd81d6e7f24036faa5342de5847f`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 18.4 MB (18423925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dfabdcead6f1ce0a24460a3db84a0aea38962c53e008fd8c74f4a0d9e31d26`  
		Last Modified: Mon, 04 May 2026 20:47:24 GMT  
		Size: 149.8 MB (149838548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85855cdedb4774678931d8279c99a0ae18b47e5ca602567bfdf63661d462b2ce`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 7.8 MB (7751403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31717402ed35498f12d5855456cae99f15b14e80ce2c994f38faf39641fc8f81`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1288674c09871f0666f8bb9ef3f6899a87a4d099dda8b1c7a86a4da3bd02980`  
		Last Modified: Mon, 04 May 2026 20:47:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872f89f9a6c21d7c1b3284c471f85415ea361b558fc4255ded3babb336f632e6`  
		Last Modified: Mon, 04 May 2026 20:47:23 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158db29f2cf810045f0800deefa3598aa356b77dc169d3ba839d34a9ebc94baf`  
		Last Modified: Mon, 04 May 2026 20:47:23 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:b5da0b093c352580372020cb5688816e3133c03a963c3aaf3356a0fa1fa3c0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820241710e281db23c06327cf628290be52dc8e9724d0b15df5fa13dcbe64c8a`

```dockerfile
```

-	Layers:
	-	`sha256:bba61b464c9021307ceff1f2da169e14e58df5495a63eefd4c6fec425e6f6200`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 6.6 MB (6648977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4145830d3083d926adeafe413501c6895fbf8c5f2c0015aeca06598cfeb590d`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.4`

```console
$ docker pull crate@sha256:3d0592b1d2db912c63ff87e5b2097c3cca1c7c2e7948c3ea1cdb33c434a5c70f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.4` - linux; amd64

```console
$ docker pull crate@sha256:0d5ce12325dad1ca22750d0273a01ccf3632b0d93ac9defaafcd806ea6bd5faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243840791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f6c8a164acf3ae7a096eb547eb32138243f97bf1dd6eab0f7539a219eb01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:53 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:29 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 04 May 2026 20:46:45 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:46:46 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:46:46 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:46:46 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:46:46 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:46:46 GMT
WORKDIR /data
# Mon, 04 May 2026 20:46:46 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:46:46 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:46:46 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:46:46 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 04 May 2026 20:46:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:46:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:46:46 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1f3c9b769bded38c7c4e291e2a502ac107500084472a144cb5542844ac4b66a8`  
		Last Modified: Mon, 04 May 2026 20:41:10 GMT  
		Size: 68.6 MB (68568777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ddea547c24e358e3f5324b130177cf964dd4246ca0b0603a78e3cf9dc5d03d`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 18.4 MB (18371106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c891bb5c1fc4353c8cfe052bdfca0992b5ecdd866edac4013d0f0f49db7ac62`  
		Last Modified: Mon, 04 May 2026 20:47:08 GMT  
		Size: 149.1 MB (149148241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf137907f3c88cfcd076a87b4d6c805b77e4e3f95cf3b49883967038cf5e058`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 7.8 MB (7750791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd34387dce372dec6c8050b63f6d0b954ca8b57a96661a803942932b3db1e71f`  
		Last Modified: Mon, 04 May 2026 20:47:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a5a51682d24d650f61c97b9446b7c87771fcff38bc91ae51c78e8ee6b7327f`  
		Last Modified: Mon, 04 May 2026 20:47:06 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53a81ce07e29a47283742a0a2af611f48c073176e3ed17e8887b6b13019c337`  
		Last Modified: Mon, 04 May 2026 20:47:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8acf2460be8682a7186fe5f65a44bfd5653c753984018db2ee700df421d6f2`  
		Last Modified: Mon, 04 May 2026 20:47:07 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:e367a3a12dcf5854182e321130885a0f8f3b1a5b13ba399f3b593dd350ccdc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6672409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7714efa72d4972a70a5ce9fb748efd97df19e1c6a0603f811c814b8471180c8`

```dockerfile
```

-	Layers:
	-	`sha256:5d8bc752f1d414e177c3b4afd2565597059b0e25203ba6344b895c7f994c842d`  
		Last Modified: Mon, 04 May 2026 20:47:05 GMT  
		Size: 6.7 MB (6651065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4867ab62f01f6c3e47d65b41b9e9f9f3e9aa63566a2ddbdbc4439c553cb03015`  
		Last Modified: Mon, 04 May 2026 20:47:04 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:110cd17bbbac492c4fb1d67db3fd27bbd1cbc5cf3163be7cf1505c5dddcf618b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243169688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca2d9bbac5d66afb38a1b056ab7a4ceb7845a165b066a9bc31c297bac399f5a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:24 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:24 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:46 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.4.tar.gz.asc crate-6.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.4.tar.gz.asc     && tar -xf crate-6.1.4.tar.gz -C /crate --strip-components=1     && rm crate-6.1.4.tar.gz # buildkit
# Mon, 04 May 2026 20:47:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:47:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:47:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:47:01 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:47:01 GMT
WORKDIR /data
# Mon, 04 May 2026 20:47:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:47:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-17T09:35:33.883825+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.4
# Mon, 04 May 2026 20:47:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:47:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2fb29370f1d8bb35e2d2cd7d7725eeaa5a9460517381edc86fc3a163d6ec8248`  
		Last Modified: Mon, 04 May 2026 20:40:41 GMT  
		Size: 67.2 MB (67153935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109f3d50101a4b177880cca22d85b3d3461acd81d6e7f24036faa5342de5847f`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 18.4 MB (18423925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dfabdcead6f1ce0a24460a3db84a0aea38962c53e008fd8c74f4a0d9e31d26`  
		Last Modified: Mon, 04 May 2026 20:47:24 GMT  
		Size: 149.8 MB (149838548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85855cdedb4774678931d8279c99a0ae18b47e5ca602567bfdf63661d462b2ce`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 7.8 MB (7751403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31717402ed35498f12d5855456cae99f15b14e80ce2c994f38faf39641fc8f81`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1288674c09871f0666f8bb9ef3f6899a87a4d099dda8b1c7a86a4da3bd02980`  
		Last Modified: Mon, 04 May 2026 20:47:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872f89f9a6c21d7c1b3284c471f85415ea361b558fc4255ded3babb336f632e6`  
		Last Modified: Mon, 04 May 2026 20:47:23 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158db29f2cf810045f0800deefa3598aa356b77dc169d3ba839d34a9ebc94baf`  
		Last Modified: Mon, 04 May 2026 20:47:23 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.4` - unknown; unknown

```console
$ docker pull crate@sha256:b5da0b093c352580372020cb5688816e3133c03a963c3aaf3356a0fa1fa3c0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820241710e281db23c06327cf628290be52dc8e9724d0b15df5fa13dcbe64c8a`

```dockerfile
```

-	Layers:
	-	`sha256:bba61b464c9021307ceff1f2da169e14e58df5495a63eefd4c6fec425e6f6200`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 6.6 MB (6648977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4145830d3083d926adeafe413501c6895fbf8c5f2c0015aeca06598cfeb590d`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 21.5 KB (21469 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2`

```console
$ docker pull crate@sha256:05c2c33e342dbe7d4bcd9ec78fbd5e16473d2c0d455a6ec47f5fb7349d904e46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2` - linux; amd64

```console
$ docker pull crate@sha256:83c9156bc0778610cd6d6e5e39cd1c3d5252779139c96e3754e31e2397697a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc83d739a655a0a089531cab250413ea48a4c15571506f4b376d594ec3620fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:53 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 04 May 2026 20:46:35 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:46:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:46:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:46:35 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:46:35 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:46:35 GMT
WORKDIR /data
# Mon, 04 May 2026 20:46:35 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:46:35 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:46:35 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:46:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 04 May 2026 20:46:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:46:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:46:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1f3c9b769bded38c7c4e291e2a502ac107500084472a144cb5542844ac4b66a8`  
		Last Modified: Mon, 04 May 2026 20:41:10 GMT  
		Size: 68.6 MB (68568777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630f5d70af4110d206ab7b7c91e80cf03e3f335cafc52fe2e349c18f073c018e`  
		Last Modified: Mon, 04 May 2026 20:46:53 GMT  
		Size: 18.4 MB (18371183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3649066e129ab9370b95513053111a37c14095f8754d7ab5bdf1e1bf0bc545a`  
		Last Modified: Mon, 04 May 2026 20:46:56 GMT  
		Size: 151.3 MB (151317522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a986f4d9eca71e0c17e74a376ecd9c97ac6046473a06a83672692a831b3f9eba`  
		Last Modified: Mon, 04 May 2026 20:46:52 GMT  
		Size: 7.8 MB (7750890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c6b489af79660dbe521bc464e25694c6864d371ddf2c34618a1bd973ef095d`  
		Last Modified: Mon, 04 May 2026 20:46:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59b2cbd99db3c24d9683d42d97d848ed112bb30cc9a120f01ace233bbb7848a`  
		Last Modified: Mon, 04 May 2026 20:46:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e5d814478d8d5513af577654c171e884dd9678ab4e0625bffe0f27fdf005e`  
		Last Modified: Mon, 04 May 2026 20:46:54 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0aec35665533879e2410904bd6fcc6b3d2fd6ad1a30995908ead19d582182`  
		Last Modified: Mon, 04 May 2026 20:46:55 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:38dc81a3fb862e585506e5b8b84f023b5dcd74f4f9c7f07a3b76ec55d33616ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c226094b4549cb961a9717da3d3097d8697c791d9a06aa2f0ddce546560d29`

```dockerfile
```

-	Layers:
	-	`sha256:efbe43e81a248c3a557b3821eb17707c938dfa2d8a3c6cf5c3a6989c890103dc`  
		Last Modified: Mon, 04 May 2026 20:46:53 GMT  
		Size: 6.7 MB (6656889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48a0ca87a8a34e6876cdf5bfe0e93f9498315986023ce57a68407839d3aa544c`  
		Last Modified: Mon, 04 May 2026 20:46:52 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4c513050344b0a35cf3708c43c06aeb02179320806de86580ffd6a3ae80015ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242613846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8e761032d83031f70ea25ab90db9195fb3ea833a060c229dfeb75f7562ebbf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:24 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:24 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 04 May 2026 20:47:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:47:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:47:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:47:01 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:47:01 GMT
WORKDIR /data
# Mon, 04 May 2026 20:47:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:47:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 04 May 2026 20:47:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:47:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2fb29370f1d8bb35e2d2cd7d7725eeaa5a9460517381edc86fc3a163d6ec8248`  
		Last Modified: Mon, 04 May 2026 20:40:41 GMT  
		Size: 67.2 MB (67153935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6156d4127f0259c8447eebf4d4cea63e528c2d45792b06bc25da2795bb6c5b`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 18.4 MB (18424021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be26bfb67e704eee4e1e81c84c988b14d1e81742217243d4dcfb78f0b343fe7`  
		Last Modified: Mon, 04 May 2026 20:47:24 GMT  
		Size: 149.3 MB (149282724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca22f1c1f0575bc20071683c9ff34ff670d66de730e4c2b6cff69b78aacdc6e`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 7.8 MB (7751285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31717402ed35498f12d5855456cae99f15b14e80ce2c994f38faf39641fc8f81`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1ebd1bd1def487c9857da60544834f19833aba8ab6d2e66885221540bbeeb`  
		Last Modified: Mon, 04 May 2026 20:47:22 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5399666990fbc3dff9f29f89f4e08900186e7e47690457f741a8d1519e98a619`  
		Last Modified: Mon, 04 May 2026 20:47:22 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce23d0ec8131a950b835c53ab4c0040ce58e53f3b969b85c6820d0393b09d01`  
		Last Modified: Mon, 04 May 2026 20:47:23 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2` - unknown; unknown

```console
$ docker pull crate@sha256:af3a8cb4e24ff4d9f1663d43511106c737bf79c598b734ac7fbbde80476f6242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5621e546e9342a35ead5be48192f41e38beb1ebcddd00f62caf2e88756b452`

```dockerfile
```

-	Layers:
	-	`sha256:00def2d613724a74f1c791eb471d6faed3d642fa7a5757a2e30f928e484da944`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 6.7 MB (6654813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78da7855e3c09d6fce021df3ba484f0f105775e7128c778867b93a0f0aace196`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.2.7`

```console
$ docker pull crate@sha256:05c2c33e342dbe7d4bcd9ec78fbd5e16473d2c0d455a6ec47f5fb7349d904e46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.2.7` - linux; amd64

```console
$ docker pull crate@sha256:83c9156bc0778610cd6d6e5e39cd1c3d5252779139c96e3754e31e2397697a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc83d739a655a0a089531cab250413ea48a4c15571506f4b376d594ec3620fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:53 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 04 May 2026 20:46:35 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:46:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:46:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:46:35 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:46:35 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:46:35 GMT
WORKDIR /data
# Mon, 04 May 2026 20:46:35 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:46:35 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:46:35 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:46:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 04 May 2026 20:46:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:46:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:46:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1f3c9b769bded38c7c4e291e2a502ac107500084472a144cb5542844ac4b66a8`  
		Last Modified: Mon, 04 May 2026 20:41:10 GMT  
		Size: 68.6 MB (68568777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630f5d70af4110d206ab7b7c91e80cf03e3f335cafc52fe2e349c18f073c018e`  
		Last Modified: Mon, 04 May 2026 20:46:53 GMT  
		Size: 18.4 MB (18371183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3649066e129ab9370b95513053111a37c14095f8754d7ab5bdf1e1bf0bc545a`  
		Last Modified: Mon, 04 May 2026 20:46:56 GMT  
		Size: 151.3 MB (151317522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a986f4d9eca71e0c17e74a376ecd9c97ac6046473a06a83672692a831b3f9eba`  
		Last Modified: Mon, 04 May 2026 20:46:52 GMT  
		Size: 7.8 MB (7750890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c6b489af79660dbe521bc464e25694c6864d371ddf2c34618a1bd973ef095d`  
		Last Modified: Mon, 04 May 2026 20:46:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59b2cbd99db3c24d9683d42d97d848ed112bb30cc9a120f01ace233bbb7848a`  
		Last Modified: Mon, 04 May 2026 20:46:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e5d814478d8d5513af577654c171e884dd9678ab4e0625bffe0f27fdf005e`  
		Last Modified: Mon, 04 May 2026 20:46:54 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0aec35665533879e2410904bd6fcc6b3d2fd6ad1a30995908ead19d582182`  
		Last Modified: Mon, 04 May 2026 20:46:55 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.7` - unknown; unknown

```console
$ docker pull crate@sha256:38dc81a3fb862e585506e5b8b84f023b5dcd74f4f9c7f07a3b76ec55d33616ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c226094b4549cb961a9717da3d3097d8697c791d9a06aa2f0ddce546560d29`

```dockerfile
```

-	Layers:
	-	`sha256:efbe43e81a248c3a557b3821eb17707c938dfa2d8a3c6cf5c3a6989c890103dc`  
		Last Modified: Mon, 04 May 2026 20:46:53 GMT  
		Size: 6.7 MB (6656889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48a0ca87a8a34e6876cdf5bfe0e93f9498315986023ce57a68407839d3aa544c`  
		Last Modified: Mon, 04 May 2026 20:46:52 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.2.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4c513050344b0a35cf3708c43c06aeb02179320806de86580ffd6a3ae80015ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242613846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8e761032d83031f70ea25ab90db9195fb3ea833a060c229dfeb75f7562ebbf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:24 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:24 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 04 May 2026 20:47:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:47:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:47:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:47:01 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:47:01 GMT
WORKDIR /data
# Mon, 04 May 2026 20:47:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:47:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 04 May 2026 20:47:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:47:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2fb29370f1d8bb35e2d2cd7d7725eeaa5a9460517381edc86fc3a163d6ec8248`  
		Last Modified: Mon, 04 May 2026 20:40:41 GMT  
		Size: 67.2 MB (67153935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6156d4127f0259c8447eebf4d4cea63e528c2d45792b06bc25da2795bb6c5b`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 18.4 MB (18424021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be26bfb67e704eee4e1e81c84c988b14d1e81742217243d4dcfb78f0b343fe7`  
		Last Modified: Mon, 04 May 2026 20:47:24 GMT  
		Size: 149.3 MB (149282724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca22f1c1f0575bc20071683c9ff34ff670d66de730e4c2b6cff69b78aacdc6e`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 7.8 MB (7751285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31717402ed35498f12d5855456cae99f15b14e80ce2c994f38faf39641fc8f81`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1ebd1bd1def487c9857da60544834f19833aba8ab6d2e66885221540bbeeb`  
		Last Modified: Mon, 04 May 2026 20:47:22 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5399666990fbc3dff9f29f89f4e08900186e7e47690457f741a8d1519e98a619`  
		Last Modified: Mon, 04 May 2026 20:47:22 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce23d0ec8131a950b835c53ab4c0040ce58e53f3b969b85c6820d0393b09d01`  
		Last Modified: Mon, 04 May 2026 20:47:23 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.2.7` - unknown; unknown

```console
$ docker pull crate@sha256:af3a8cb4e24ff4d9f1663d43511106c737bf79c598b734ac7fbbde80476f6242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5621e546e9342a35ead5be48192f41e38beb1ebcddd00f62caf2e88756b452`

```dockerfile
```

-	Layers:
	-	`sha256:00def2d613724a74f1c791eb471d6faed3d642fa7a5757a2e30f928e484da944`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 6.7 MB (6654813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78da7855e3c09d6fce021df3ba484f0f105775e7128c778867b93a0f0aace196`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:05c2c33e342dbe7d4bcd9ec78fbd5e16473d2c0d455a6ec47f5fb7349d904e46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:83c9156bc0778610cd6d6e5e39cd1c3d5252779139c96e3754e31e2397697a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc83d739a655a0a089531cab250413ea48a4c15571506f4b376d594ec3620fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:53 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:20 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:32 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 04 May 2026 20:46:35 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:46:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:46:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:46:35 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:46:35 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:46:35 GMT
WORKDIR /data
# Mon, 04 May 2026 20:46:35 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:46:35 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:46:35 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:46:35 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 04 May 2026 20:46:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:46:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:46:35 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1f3c9b769bded38c7c4e291e2a502ac107500084472a144cb5542844ac4b66a8`  
		Last Modified: Mon, 04 May 2026 20:41:10 GMT  
		Size: 68.6 MB (68568777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630f5d70af4110d206ab7b7c91e80cf03e3f335cafc52fe2e349c18f073c018e`  
		Last Modified: Mon, 04 May 2026 20:46:53 GMT  
		Size: 18.4 MB (18371183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3649066e129ab9370b95513053111a37c14095f8754d7ab5bdf1e1bf0bc545a`  
		Last Modified: Mon, 04 May 2026 20:46:56 GMT  
		Size: 151.3 MB (151317522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a986f4d9eca71e0c17e74a376ecd9c97ac6046473a06a83672692a831b3f9eba`  
		Last Modified: Mon, 04 May 2026 20:46:52 GMT  
		Size: 7.8 MB (7750890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c6b489af79660dbe521bc464e25694c6864d371ddf2c34618a1bd973ef095d`  
		Last Modified: Mon, 04 May 2026 20:46:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59b2cbd99db3c24d9683d42d97d848ed112bb30cc9a120f01ace233bbb7848a`  
		Last Modified: Mon, 04 May 2026 20:46:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e5d814478d8d5513af577654c171e884dd9678ab4e0625bffe0f27fdf005e`  
		Last Modified: Mon, 04 May 2026 20:46:54 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0aec35665533879e2410904bd6fcc6b3d2fd6ad1a30995908ead19d582182`  
		Last Modified: Mon, 04 May 2026 20:46:55 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:38dc81a3fb862e585506e5b8b84f023b5dcd74f4f9c7f07a3b76ec55d33616ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c226094b4549cb961a9717da3d3097d8697c791d9a06aa2f0ddce546560d29`

```dockerfile
```

-	Layers:
	-	`sha256:efbe43e81a248c3a557b3821eb17707c938dfa2d8a3c6cf5c3a6989c890103dc`  
		Last Modified: Mon, 04 May 2026 20:46:53 GMT  
		Size: 6.7 MB (6656889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48a0ca87a8a34e6876cdf5bfe0e93f9498315986023ce57a68407839d3aa544c`  
		Last Modified: Mon, 04 May 2026 20:46:52 GMT  
		Size: 21.6 KB (21640 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4c513050344b0a35cf3708c43c06aeb02179320806de86580ffd6a3ae80015ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242613846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8e761032d83031f70ea25ab90db9195fb3ea833a060c229dfeb75f7562ebbf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 04 May 2026 20:40:24 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 04 May 2026 20:40:24 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:46:44 GMT
RUN dnf install --nodocs --assumeyes gzip python3 python3-pip shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 04 May 2026 20:46:58 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.7.tar.gz.asc crate-6.2.7.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.7.tar.gz.asc     && tar -xf crate-6.2.7.tar.gz -C /crate --strip-components=1     && rm crate-6.2.7.tar.gz # buildkit
# Mon, 04 May 2026 20:47:01 GMT
RUN python3 -m pip install 'crash==0.32.0' # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:47:01 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 04 May 2026 20:47:01 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 04 May 2026 20:47:01 GMT
VOLUME [/data]
# Mon, 04 May 2026 20:47:01 GMT
WORKDIR /data
# Mon, 04 May 2026 20:47:01 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 04 May 2026 20:47:01 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 04 May 2026 20:47:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-04-27T08:48:19.554044+00:00 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.7
# Mon, 04 May 2026 20:47:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:47:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:47:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2fb29370f1d8bb35e2d2cd7d7725eeaa5a9460517381edc86fc3a163d6ec8248`  
		Last Modified: Mon, 04 May 2026 20:40:41 GMT  
		Size: 67.2 MB (67153935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6156d4127f0259c8447eebf4d4cea63e528c2d45792b06bc25da2795bb6c5b`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 18.4 MB (18424021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be26bfb67e704eee4e1e81c84c988b14d1e81742217243d4dcfb78f0b343fe7`  
		Last Modified: Mon, 04 May 2026 20:47:24 GMT  
		Size: 149.3 MB (149282724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca22f1c1f0575bc20071683c9ff34ff670d66de730e4c2b6cff69b78aacdc6e`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 7.8 MB (7751285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31717402ed35498f12d5855456cae99f15b14e80ce2c994f38faf39641fc8f81`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1ebd1bd1def487c9857da60544834f19833aba8ab6d2e66885221540bbeeb`  
		Last Modified: Mon, 04 May 2026 20:47:22 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5399666990fbc3dff9f29f89f4e08900186e7e47690457f741a8d1519e98a619`  
		Last Modified: Mon, 04 May 2026 20:47:22 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce23d0ec8131a950b835c53ab4c0040ce58e53f3b969b85c6820d0393b09d01`  
		Last Modified: Mon, 04 May 2026 20:47:23 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:af3a8cb4e24ff4d9f1663d43511106c737bf79c598b734ac7fbbde80476f6242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5621e546e9342a35ead5be48192f41e38beb1ebcddd00f62caf2e88756b452`

```dockerfile
```

-	Layers:
	-	`sha256:00def2d613724a74f1c791eb471d6faed3d642fa7a5757a2e30f928e484da944`  
		Last Modified: Mon, 04 May 2026 20:47:21 GMT  
		Size: 6.7 MB (6654813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78da7855e3c09d6fce021df3ba484f0f105775e7128c778867b93a0f0aace196`  
		Last Modified: Mon, 04 May 2026 20:47:20 GMT  
		Size: 21.8 KB (21777 bytes)  
		MIME: application/vnd.in-toto+json
