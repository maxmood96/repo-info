## `crate:latest`

```console
$ docker pull crate@sha256:36cb3767c2403ddc7fff864e4a61d296f0168347ee5c985c174b4a1ad9f91249
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:a499674bf64b02c81fcf49e9d597e5df328ac416f39b89ba915fde524a060f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233815987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76a9a95054d545c2f98372b6c61f95657ba0216aa42e8c1a2f9eba6e5555d81`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:48:23 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:48:23 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:16:40 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 06 Mar 2026 18:16:54 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.2.tar.gz.asc crate-6.2.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.2.tar.gz.asc     && tar -xf crate-6.2.2.tar.gz -C /crate --strip-components=1     && rm crate-6.2.2.tar.gz # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:16:55 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 06 Mar 2026 18:16:55 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
VOLUME [/data]
# Fri, 06 Mar 2026 18:16:55 GMT
WORKDIR /data
# Fri, 06 Mar 2026 18:16:55 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 06 Mar 2026 18:16:55 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-03T07:00:43.350890 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.2
# Fri, 06 Mar 2026 18:16:55 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:16:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:16:55 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:1df64ef8e0fcb636b739cd5956ab24b4d2cdcdd52b80b4191e0b4d2bbeea8606`  
		Last Modified: Fri, 27 Feb 2026 22:48:39 GMT  
		Size: 67.5 MB (67519802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d42d1df61c8c2adee7880e339bb2e124cd1cbcb11b5ab020fb89bd58bab5eb`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 13.1 MB (13051148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7173979866676d5e0789bd96c60fddc420e9ed7673ca28ce77d882e4fbf43d2`  
		Last Modified: Fri, 06 Mar 2026 18:17:16 GMT  
		Size: 151.3 MB (151299527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81ca6896638763ef003121d60922fc11d7c1e7ae1d7fbcadfcf003b0c499ac1`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60ab311bbce78472dc2f56e1d8ad2a2278449323e25c41eefccd7cad74e71d`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d3e66a9903d0b0fbdf320cdb9b769177b59050874bc052bd72a525050532d9`  
		Last Modified: Fri, 06 Mar 2026 18:17:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d33be94b10eba090d1e942b9daf0ebc34b33558395eec9cdff3722d32ff1d6a`  
		Last Modified: Fri, 06 Mar 2026 18:17:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccb71e1d4e87b54ba418ad25b2cd92fc2d8a7f24a5645511ae500d9a0c348d3`  
		Last Modified: Fri, 06 Mar 2026 18:17:15 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:a03aa2c04e05136b7329c25aea398509fb38e488f4ecd4fa89fe040c25ffe9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d70993efa875744a8d6594da736dd5122a87786cdc82499784005a4a0387c3b`

```dockerfile
```

-	Layers:
	-	`sha256:4d61d67630d9fefe9f84d591581129f1e15ab4c59c2676895559e16fd11860a2`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 5.2 MB (5156500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af05c066a22fa5cd225786881484865ec2531bb64e138c160997166cbf3b512f`  
		Last Modified: Fri, 06 Mar 2026 18:17:13 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:09960e34d2389e3b4647796b37ac2e27c5ac76f1e92d0ed6073d78a732c30f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230419274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82521b5f7aad1a3028dcad2a2468a2726cb70c876b02ccd1e2d1f3f68bb05221`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Fri, 27 Feb 2026 22:47:04 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Fri, 27 Feb 2026 22:47:04 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:16:33 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Fri, 06 Mar 2026 18:16:46 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.2.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.2.2.tar.gz.asc crate-6.2.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.2.2.tar.gz.asc     && tar -xf crate-6.2.2.tar.gz -C /crate --strip-components=1     && rm crate-6.2.2.tar.gz # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:16:47 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 06 Mar 2026 18:16:47 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
VOLUME [/data]
# Fri, 06 Mar 2026 18:16:47 GMT
WORKDIR /data
# Fri, 06 Mar 2026 18:16:47 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Fri, 06 Mar 2026 18:16:47 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2026-03-03T07:00:43.350890 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.2.2
# Fri, 06 Mar 2026 18:16:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:16:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:16:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:072f0818ab959c85fe58ba512de79e00deb9ad5e22de355466e78028bc4924aa`  
		Last Modified: Fri, 27 Feb 2026 22:47:20 GMT  
		Size: 66.1 MB (66099982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb9966dd80a3c898b0ab4dfdf34be280f5e8f2797e33791b371a24ad52e1673`  
		Last Modified: Fri, 06 Mar 2026 18:17:06 GMT  
		Size: 13.1 MB (13104611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa64a45453b88dd2dfbce5e53084242d601bfaaec48593efc67cc3761f5b21d2`  
		Last Modified: Fri, 06 Mar 2026 18:17:09 GMT  
		Size: 149.3 MB (149269172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77638d5af0c1c9c9b26f5ff46cd1fd8d1aa2d96a4cf850770943183966a463d`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9b6226a425c7b05f2722d7fffb61971d74036000d49566cafd5b793c92d3e2`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd466f939c44100b794f11ec968e922144a624039be67f43ce20edce1aeb79`  
		Last Modified: Fri, 06 Mar 2026 18:17:07 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb5261e92a29a5a3f4631919be5c9d3cae4e08fac50bf6c800caa10f33837d6`  
		Last Modified: Fri, 06 Mar 2026 18:17:06 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c19ec6771d12a701007f67fefd01143bdf2369ee39ed697f2bd9dda68ae235`  
		Last Modified: Fri, 06 Mar 2026 18:17:07 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:6f85ca3a9ae8b6d3c087cf44808bc8541ffa1472a6f6503c76c2c5358d8a6bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5177696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8e8c27058f8de779676de200459c45dfeda64bb61d03238a0c28ba2b076134`

```dockerfile
```

-	Layers:
	-	`sha256:83daa76baf0914e0cd92f6026b8a04d477a1045eb33c18ff55b8f14e4bf6cedc`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 5.2 MB (5154419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4824ec79e890e47441646d72de5b24ac5ead97d18f186a28ce35f3c057390eb`  
		Last Modified: Fri, 06 Mar 2026 18:17:05 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
