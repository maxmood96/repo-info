## `crate:latest`

```console
$ docker pull crate@sha256:d365066e52d57a8925bafa1f019de86299d426a8bfe788f58ce33886e8d0548b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:7acb1748d3d57135b8eb6d41f153d4e6b643e925eeb318daf8b04d32c579dcfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244172878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdb345c7729db55f7a048718bd87afcc582a209e0746160b551c2df556cf887`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-amd64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:05:52 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.8.tar.gz.asc crate-5.9.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.8.tar.gz.asc     && tar -xf crate-5.9.8.tar.gz -C /crate --strip-components=1     && rm crate-5.9.8.tar.gz # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:05:52 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 21 Jan 2025 19:05:52 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
VOLUME [/data]
# Tue, 21 Jan 2025 19:05:52 GMT
WORKDIR /data
# Tue, 21 Jan 2025 19:05:52 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 21 Jan 2025 19:05:52 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-21T19:05:52.767882 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.8
# Tue, 21 Jan 2025 19:05:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:05:52 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:e60c9fe2676d1fc11442d4ccd62ed958bdeb07c2a637cbdc10e2eef235b66814`  
		Last Modified: Mon, 18 Nov 2024 21:05:52 GMT  
		Size: 79.1 MB (79078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e3f5e43d37253d3cf12240e79b7b5e0df2b8cdd165757f2d71643a41a6db13`  
		Last Modified: Tue, 28 Jan 2025 01:28:30 GMT  
		Size: 14.1 MB (14148775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2318c2983ce3913b9da191229cda1648489530759a22e746d1a80bec87881db3`  
		Last Modified: Tue, 28 Jan 2025 01:28:33 GMT  
		Size: 149.0 MB (148999618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3529ddf294b9e7a881e41e312d97e129f7b019d04f4619e69f0f655f6aac58`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72134be31d913e2710260ecaac8c329573d0ea5d10e289e5ec57d5dd78a85454`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37533422f6b1f66d8a88cf8ddd51383b628b18680c4163e002675c56e6241c99`  
		Last Modified: Tue, 28 Jan 2025 01:28:30 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930da96d4e47ac2b4fb1e59b5406d3252fe56adae4289ec20042c0068c5cff2a`  
		Last Modified: Tue, 28 Jan 2025 01:28:30 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ee12be64f6d5f76c34989874ff073ff788396f07f0be0a3462eba682617fbd`  
		Last Modified: Tue, 28 Jan 2025 01:28:30 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:15d4875abb868c8c38f95e2b6a68fc227f9cabc45383d693b19a6e8fcf451b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcf1ac902821fb12b70b265a4ac9ad16eafc1071fe3a1a8dc27d949b440fc90`

```dockerfile
```

-	Layers:
	-	`sha256:f218c2744997f275bf110328a141612b07505abadec3adc792218d117aceb796`  
		Last Modified: Tue, 28 Jan 2025 01:28:30 GMT  
		Size: 6.3 MB (6316964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf4606c90a120a2a0365ada494c2c49e76c5e0c012cc78886220a3939c8cffe`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:b7e558cbce424818ddae714023db0981fadff093b85ede60df8b1e169b1da5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243820713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5366cda0937bc490ae68368cb3e0cbfc80bf613a8b0556942d276ae37fb39e51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 18 Nov 2024 19:36:06 GMT
ADD almalinux-9-default-arm64.tar.xz / # buildkit
# Mon, 18 Nov 2024 19:36:06 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:05:52 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.8.tar.gz.asc crate-5.9.8.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.8.tar.gz.asc     && tar -xf crate-5.9.8.tar.gz -C /crate --strip-components=1     && rm crate-5.9.8.tar.gz # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:05:52 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 21 Jan 2025 19:05:52 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
VOLUME [/data]
# Tue, 21 Jan 2025 19:05:52 GMT
WORKDIR /data
# Tue, 21 Jan 2025 19:05:52 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Tue, 21 Jan 2025 19:05:52 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-01-21T19:05:52.767882 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.8
# Tue, 21 Jan 2025 19:05:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 21 Jan 2025 19:05:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:05:52 GMT
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
	-	`sha256:422b4c365f0b910d750ae4bb20a9232fcb1910f2ae3a2b822b6433920dd7da5f`  
		Last Modified: Tue, 28 Jan 2025 01:40:23 GMT  
		Size: 149.7 MB (149692849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c735d9a0800e485461052a27a007d4f0c7969b0bb22811ca081a80d13a8faeff`  
		Last Modified: Tue, 28 Jan 2025 01:40:20 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1c3735fdfd1ce74e60a67551be58660e5d538aeef091acefea6f9f86baf0bf`  
		Last Modified: Tue, 28 Jan 2025 01:40:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a05bb378720c1cca0b122c6a56d0aa7ca73704f6cf8c24e49e97c92733099df`  
		Last Modified: Tue, 28 Jan 2025 01:40:20 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583e0146e3db0e4948bfcf0478602c5bda5e3621ec1b32537e8bdaeed5919062`  
		Last Modified: Tue, 28 Jan 2025 01:40:21 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc733db94431990ad2573076a957ea672bc6300f378e3adc3e8d7e5a7cc383f9`  
		Last Modified: Tue, 28 Jan 2025 01:40:21 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:8b7425766d0ffc6934136e62c563a3a28e09090d8c278d9993c7ddc3b0c332d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6336932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c017ef48aa1cfd3febf86e05787d504ed14dff0adb18c3a32fd2618d0419ba7`

```dockerfile
```

-	Layers:
	-	`sha256:6bd8b8ddc9ca96a01e896c532ab8f730539baf23cfbc571b8571cf6d867f4185`  
		Last Modified: Tue, 28 Jan 2025 01:40:20 GMT  
		Size: 6.3 MB (6313673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83acca7c6f38209d9e32ecab7b7d91540ab48753e5a3f649bb52ee672826c260`  
		Last Modified: Tue, 28 Jan 2025 01:40:19 GMT  
		Size: 23.3 KB (23259 bytes)  
		MIME: application/vnd.in-toto+json
