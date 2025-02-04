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
