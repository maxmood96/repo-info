<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.11`](#crate51011)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:69900032a012bfede119312a590d32299d43b881966f85bfa7bedd80e2bab7f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:774a353db69ca1364ed0d3708a101a1e2f45b3fe4e21e7689d1c3a51ecc1afa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233177749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ad10e3e4bc0712a4d4ad6314705b3fa94f5042d8688f1b031d07f554015393`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebe3f271970e178e26876800a7c41607423b3ff9f559848402e0b9b16a2b95`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 14.5 MB (14534329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b28ac24bd515f19d07208d51683779161b11b8079af1a7e667afe84a0614eb6`  
		Last Modified: Tue, 09 Sep 2025 23:39:16 GMT  
		Size: 149.7 MB (149668861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f63f59f2e3633256115b9281d55f7ebb2a247e9de1f5e40f6cbf2000da6be`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e80fce4922d1ee74280eaa12c78555f35227f64767962c11c800743c583f3e`  
		Last Modified: Tue, 09 Sep 2025 21:10:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d960590d6474e40d920419956b89360da4bcbaa0d0e3e884bf14841b1fbd3c0`  
		Last Modified: Tue, 09 Sep 2025 21:10:00 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20604c9aa141bc682228b574f40567c0e89f598b47aad44f2a948d87c107e4e`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cde2f5aa0948d8e3c07b114ebc63d6305173fe5a4fc789e159705fe1d5a2e8`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:c17a6ca0ca96545f0f7e5e53f44ca816bf61102633fe1194241476922a35a735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496bc29621f83b2d18bf6e1595da8be6cc8bba21e7e7fe262007a669ee552081`

```dockerfile
```

-	Layers:
	-	`sha256:aea6ff84ba5ccb54880a270c51ef29c4f137cdcb054dddb832c08436f904a90c`  
		Last Modified: Tue, 09 Sep 2025 23:38:23 GMT  
		Size: 5.2 MB (5188425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5005a475a54839eb3bff0b29e77d55a22d1869d4bbb9ccb19307b827b76668a2`  
		Last Modified: Tue, 09 Sep 2025 23:38:24 GMT  
		Size: 23.2 KB (23216 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e262c44268b005ac161f5bb78743d55fcc0a1ef7758bc1ef2076b0a21ce40f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232394685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff76026bd48650e02cb6b8344bde76e92ece705cc5a5f3493a9c4de3df15ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a621df3cef737ec5f897bb4ce7f93176dfc2ed3d192143daa0b25f665d59875`  
		Last Modified: Tue, 09 Sep 2025 21:12:17 GMT  
		Size: 14.6 MB (14585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d03e5a23c57071269e2c08c9c0bfc33211dbeb4e4284255e59c3381a58d0b1`  
		Last Modified: Tue, 09 Sep 2025 21:27:43 GMT  
		Size: 150.3 MB (150345634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a372a9f4cb3903dcf61ce4288f9fc8eb6ddc0efbdf7d189590e3a02f4b33fbe`  
		Last Modified: Tue, 09 Sep 2025 21:27:15 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852151834362117b6ea0af08cb6f6f58089b7b05ece1d7983f4e6cfa92894dd5`  
		Last Modified: Tue, 09 Sep 2025 21:27:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af50fed053716253dc344abf511a6e9887c131eabb9bd46038549b1f1f2a448`  
		Last Modified: Tue, 09 Sep 2025 21:27:15 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e9eeb51513545c8ac0cab29c4220c719a89391c06ac76b52a2a352001d5774`  
		Last Modified: Tue, 09 Sep 2025 21:27:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0d6110ec66b53dd73a00d6d859a3083d4142c15b4084c2c31032c6c08bf97`  
		Last Modified: Tue, 09 Sep 2025 21:27:15 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:30e85ef1d884ffca44a8d14168e25b6d0a2dd6f99c412becd9f6653d05cebb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a652f38489cec447f171b9ec0a96e7f6eae7418bf982081ca3339e293cbfd3`

```dockerfile
```

-	Layers:
	-	`sha256:c6a9d44ed5d56cd75ed71c9a19f3531028cb873b8874cfecbf79dc7c73287193`  
		Last Modified: Tue, 09 Sep 2025 23:38:29 GMT  
		Size: 5.2 MB (5185733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6994459e936f5011f6ff2d3c161dffb5bbc89eacbed7da3ed0c023a04da719`  
		Last Modified: Tue, 09 Sep 2025 23:38:30 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.11`

```console
$ docker pull crate@sha256:69900032a012bfede119312a590d32299d43b881966f85bfa7bedd80e2bab7f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.11` - linux; amd64

```console
$ docker pull crate@sha256:774a353db69ca1364ed0d3708a101a1e2f45b3fe4e21e7689d1c3a51ecc1afa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233177749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ad10e3e4bc0712a4d4ad6314705b3fa94f5042d8688f1b031d07f554015393`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebe3f271970e178e26876800a7c41607423b3ff9f559848402e0b9b16a2b95`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 14.5 MB (14534329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b28ac24bd515f19d07208d51683779161b11b8079af1a7e667afe84a0614eb6`  
		Last Modified: Tue, 09 Sep 2025 23:39:16 GMT  
		Size: 149.7 MB (149668861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f63f59f2e3633256115b9281d55f7ebb2a247e9de1f5e40f6cbf2000da6be`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e80fce4922d1ee74280eaa12c78555f35227f64767962c11c800743c583f3e`  
		Last Modified: Tue, 09 Sep 2025 21:10:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d960590d6474e40d920419956b89360da4bcbaa0d0e3e884bf14841b1fbd3c0`  
		Last Modified: Tue, 09 Sep 2025 21:10:00 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20604c9aa141bc682228b574f40567c0e89f598b47aad44f2a948d87c107e4e`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cde2f5aa0948d8e3c07b114ebc63d6305173fe5a4fc789e159705fe1d5a2e8`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.11` - unknown; unknown

```console
$ docker pull crate@sha256:c17a6ca0ca96545f0f7e5e53f44ca816bf61102633fe1194241476922a35a735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496bc29621f83b2d18bf6e1595da8be6cc8bba21e7e7fe262007a669ee552081`

```dockerfile
```

-	Layers:
	-	`sha256:aea6ff84ba5ccb54880a270c51ef29c4f137cdcb054dddb832c08436f904a90c`  
		Last Modified: Tue, 09 Sep 2025 23:38:23 GMT  
		Size: 5.2 MB (5188425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5005a475a54839eb3bff0b29e77d55a22d1869d4bbb9ccb19307b827b76668a2`  
		Last Modified: Tue, 09 Sep 2025 23:38:24 GMT  
		Size: 23.2 KB (23216 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.11` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e262c44268b005ac161f5bb78743d55fcc0a1ef7758bc1ef2076b0a21ce40f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232394685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff76026bd48650e02cb6b8344bde76e92ece705cc5a5f3493a9c4de3df15ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a621df3cef737ec5f897bb4ce7f93176dfc2ed3d192143daa0b25f665d59875`  
		Last Modified: Tue, 09 Sep 2025 21:12:17 GMT  
		Size: 14.6 MB (14585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d03e5a23c57071269e2c08c9c0bfc33211dbeb4e4284255e59c3381a58d0b1`  
		Last Modified: Tue, 09 Sep 2025 21:27:43 GMT  
		Size: 150.3 MB (150345634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a372a9f4cb3903dcf61ce4288f9fc8eb6ddc0efbdf7d189590e3a02f4b33fbe`  
		Last Modified: Tue, 09 Sep 2025 21:27:15 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852151834362117b6ea0af08cb6f6f58089b7b05ece1d7983f4e6cfa92894dd5`  
		Last Modified: Tue, 09 Sep 2025 21:27:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af50fed053716253dc344abf511a6e9887c131eabb9bd46038549b1f1f2a448`  
		Last Modified: Tue, 09 Sep 2025 21:27:15 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e9eeb51513545c8ac0cab29c4220c719a89391c06ac76b52a2a352001d5774`  
		Last Modified: Tue, 09 Sep 2025 21:27:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0d6110ec66b53dd73a00d6d859a3083d4142c15b4084c2c31032c6c08bf97`  
		Last Modified: Tue, 09 Sep 2025 21:27:15 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.11` - unknown; unknown

```console
$ docker pull crate@sha256:30e85ef1d884ffca44a8d14168e25b6d0a2dd6f99c412becd9f6653d05cebb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a652f38489cec447f171b9ec0a96e7f6eae7418bf982081ca3339e293cbfd3`

```dockerfile
```

-	Layers:
	-	`sha256:c6a9d44ed5d56cd75ed71c9a19f3531028cb873b8874cfecbf79dc7c73287193`  
		Last Modified: Tue, 09 Sep 2025 23:38:29 GMT  
		Size: 5.2 MB (5185733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6994459e936f5011f6ff2d3c161dffb5bbc89eacbed7da3ed0c023a04da719`  
		Last Modified: Tue, 09 Sep 2025 23:38:30 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:f76e157c87e2faf64c2a2aec835d99f498d19d913e9db89973c04940366263da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:20b4b8e0a312da518bb4a848b30bec4b613149c9131076250d61979994fafbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232518442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db8072eca1255bfa491975f8538e58317b63f9efb648755ad61592a161cff8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6034873a173ecc5b803c7e0bcd3aa2929069b487d0d35a1cecc313fb9ecf07d9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 14.5 MB (14534314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2881fbab7c44f8bd8730bc7a5258bf9bd5392df9a38a344bae0d12b59baba184`  
		Last Modified: Tue, 09 Sep 2025 21:10:18 GMT  
		Size: 149.0 MB (149009568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9995a0bdb2820e6c7631c1eb37bb323f8ea39ab8d7801fff92baca64817c5`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0116236db205c62b93b40d5bdc738761656cd981a911e10a6a1cf015cef0300`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ed4583831751086a65d172aec1d9d20e6aab77cf5920bcfc9a5a5b225b3e88`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d234b7aaa1e65f7c10bb072135e88363be03349c42aeb4ca6ead2ae362fa47`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30a8925465300e4bf20123c80723d7ff3e408f6d78b5c3c9a40d66f7c2bd601`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:f6cade60f0be48c0d9246d7414b3ea20e6844ebc370b6b8ce4112694f497aae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd8bae646d5875e727812f2aeb460b0a66055da91d96b9dd47ee08bff8311a`

```dockerfile
```

-	Layers:
	-	`sha256:a5bd7bbd74b593174bd051244a00519a345bdce9153dbf39632e493c7560da50`  
		Last Modified: Tue, 09 Sep 2025 23:38:34 GMT  
		Size: 5.2 MB (5186490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5bd97fa1ee90113bd942f0273ef5bd2044e61af676ffb2c4b2feb908e79c69`  
		Last Modified: Tue, 09 Sep 2025 23:38:35 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1f3d3eb3131c72f61dc106f72f445b1dbd1ae0d9b436fa65a869ea5cb36b471f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231757583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7929c4381435ac835f9a713cfa4204d0066560b5c09e2d4493b79f35da60f0d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a621df3cef737ec5f897bb4ce7f93176dfc2ed3d192143daa0b25f665d59875`  
		Last Modified: Tue, 09 Sep 2025 21:12:17 GMT  
		Size: 14.6 MB (14585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab91292c150cdb2300f1abcfb0881099b851c47e02021cdae60fc675eb754c7b`  
		Last Modified: Tue, 09 Sep 2025 21:12:26 GMT  
		Size: 149.7 MB (149708537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f47ce5519f7375e4c9c252ea859d1cad0f67a0848bd209cf5fe85422c6a908`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd3bcfe0b0f8320b4bb03aea983cd7b354ef366827eb2afc361501eaf0a50da`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fac8ce0957b7933cd4595886d0a44bbe476ad84e4e5e15a7a4e51f9af7f15f`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b066bdefd095d937f5226d4f023debb4f343d471754f30d890c825209a329`  
		Last Modified: Tue, 09 Sep 2025 21:12:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f5d6781ea7fc53d798962aa744939bc04cc7c3079126db853bd9261724e427`  
		Last Modified: Tue, 09 Sep 2025 21:12:11 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:9114b67622502217f2e0d846dc1b0d43b37b954054652d4ee27857d684218b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b51803f41e6cd2c493426a57c77b7971417769ce3c1aea71b1eeadf96d39b3`

```dockerfile
```

-	Layers:
	-	`sha256:0700bff935177de8e6dc1ac74d186792235f7661d62d2b12603cf8badb68e679`  
		Last Modified: Tue, 09 Sep 2025 23:38:40 GMT  
		Size: 5.2 MB (5183786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359270dd6674a0395407ee457ecc0335582c0fa1d22f0e1a288b56241fc516fe`  
		Last Modified: Tue, 09 Sep 2025 23:38:41 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:f76e157c87e2faf64c2a2aec835d99f498d19d913e9db89973c04940366263da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:20b4b8e0a312da518bb4a848b30bec4b613149c9131076250d61979994fafbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232518442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db8072eca1255bfa491975f8538e58317b63f9efb648755ad61592a161cff8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6034873a173ecc5b803c7e0bcd3aa2929069b487d0d35a1cecc313fb9ecf07d9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 14.5 MB (14534314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2881fbab7c44f8bd8730bc7a5258bf9bd5392df9a38a344bae0d12b59baba184`  
		Last Modified: Tue, 09 Sep 2025 21:10:18 GMT  
		Size: 149.0 MB (149009568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9995a0bdb2820e6c7631c1eb37bb323f8ea39ab8d7801fff92baca64817c5`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0116236db205c62b93b40d5bdc738761656cd981a911e10a6a1cf015cef0300`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ed4583831751086a65d172aec1d9d20e6aab77cf5920bcfc9a5a5b225b3e88`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d234b7aaa1e65f7c10bb072135e88363be03349c42aeb4ca6ead2ae362fa47`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30a8925465300e4bf20123c80723d7ff3e408f6d78b5c3c9a40d66f7c2bd601`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:f6cade60f0be48c0d9246d7414b3ea20e6844ebc370b6b8ce4112694f497aae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd8bae646d5875e727812f2aeb460b0a66055da91d96b9dd47ee08bff8311a`

```dockerfile
```

-	Layers:
	-	`sha256:a5bd7bbd74b593174bd051244a00519a345bdce9153dbf39632e493c7560da50`  
		Last Modified: Tue, 09 Sep 2025 23:38:34 GMT  
		Size: 5.2 MB (5186490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5bd97fa1ee90113bd942f0273ef5bd2044e61af676ffb2c4b2feb908e79c69`  
		Last Modified: Tue, 09 Sep 2025 23:38:35 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:1f3d3eb3131c72f61dc106f72f445b1dbd1ae0d9b436fa65a869ea5cb36b471f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231757583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7929c4381435ac835f9a713cfa4204d0066560b5c09e2d4493b79f35da60f0d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a621df3cef737ec5f897bb4ce7f93176dfc2ed3d192143daa0b25f665d59875`  
		Last Modified: Tue, 09 Sep 2025 21:12:17 GMT  
		Size: 14.6 MB (14585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab91292c150cdb2300f1abcfb0881099b851c47e02021cdae60fc675eb754c7b`  
		Last Modified: Tue, 09 Sep 2025 21:12:26 GMT  
		Size: 149.7 MB (149708537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f47ce5519f7375e4c9c252ea859d1cad0f67a0848bd209cf5fe85422c6a908`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd3bcfe0b0f8320b4bb03aea983cd7b354ef366827eb2afc361501eaf0a50da`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fac8ce0957b7933cd4595886d0a44bbe476ad84e4e5e15a7a4e51f9af7f15f`  
		Last Modified: Tue, 09 Sep 2025 21:12:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b066bdefd095d937f5226d4f023debb4f343d471754f30d890c825209a329`  
		Last Modified: Tue, 09 Sep 2025 21:12:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f5d6781ea7fc53d798962aa744939bc04cc7c3079126db853bd9261724e427`  
		Last Modified: Tue, 09 Sep 2025 21:12:11 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:9114b67622502217f2e0d846dc1b0d43b37b954054652d4ee27857d684218b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b51803f41e6cd2c493426a57c77b7971417769ce3c1aea71b1eeadf96d39b3`

```dockerfile
```

-	Layers:
	-	`sha256:0700bff935177de8e6dc1ac74d186792235f7661d62d2b12603cf8badb68e679`  
		Last Modified: Tue, 09 Sep 2025 23:38:40 GMT  
		Size: 5.2 MB (5183786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359270dd6674a0395407ee457ecc0335582c0fa1d22f0e1a288b56241fc516fe`  
		Last Modified: Tue, 09 Sep 2025 23:38:41 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:69900032a012bfede119312a590d32299d43b881966f85bfa7bedd80e2bab7f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:774a353db69ca1364ed0d3708a101a1e2f45b3fe4e21e7689d1c3a51ecc1afa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233177749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ad10e3e4bc0712a4d4ad6314705b3fa94f5042d8688f1b031d07f554015393`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:47ddd4eac00b7279cb3e28b3cbb175c16bd2c8f79f5bb87fce12ea4e87f754c5`  
		Last Modified: Tue, 09 Sep 2025 20:18:51 GMT  
		Size: 67.0 MB (67029052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebe3f271970e178e26876800a7c41607423b3ff9f559848402e0b9b16a2b95`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 14.5 MB (14534329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b28ac24bd515f19d07208d51683779161b11b8079af1a7e667afe84a0614eb6`  
		Last Modified: Tue, 09 Sep 2025 23:39:16 GMT  
		Size: 149.7 MB (149668861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f63f59f2e3633256115b9281d55f7ebb2a247e9de1f5e40f6cbf2000da6be`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e80fce4922d1ee74280eaa12c78555f35227f64767962c11c800743c583f3e`  
		Last Modified: Tue, 09 Sep 2025 21:10:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d960590d6474e40d920419956b89360da4bcbaa0d0e3e884bf14841b1fbd3c0`  
		Last Modified: Tue, 09 Sep 2025 21:10:00 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20604c9aa141bc682228b574f40567c0e89f598b47aad44f2a948d87c107e4e`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cde2f5aa0948d8e3c07b114ebc63d6305173fe5a4fc789e159705fe1d5a2e8`  
		Last Modified: Tue, 09 Sep 2025 21:10:01 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:c17a6ca0ca96545f0f7e5e53f44ca816bf61102633fe1194241476922a35a735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496bc29621f83b2d18bf6e1595da8be6cc8bba21e7e7fe262007a669ee552081`

```dockerfile
```

-	Layers:
	-	`sha256:aea6ff84ba5ccb54880a270c51ef29c4f137cdcb054dddb832c08436f904a90c`  
		Last Modified: Tue, 09 Sep 2025 23:38:23 GMT  
		Size: 5.2 MB (5188425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5005a475a54839eb3bff0b29e77d55a22d1869d4bbb9ccb19307b827b76668a2`  
		Last Modified: Tue, 09 Sep 2025 23:38:24 GMT  
		Size: 23.2 KB (23216 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e262c44268b005ac161f5bb78743d55fcc0a1ef7758bc1ef2076b0a21ce40f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232394685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff76026bd48650e02cb6b8344bde76e92ece705cc5a5f3493a9c4de3df15ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Jul 2025 10:46:22 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["/bin/bash"]
# Mon, 14 Jul 2025 10:46:22 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.11.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.11.tar.gz.asc crate-5.10.11.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.11.tar.gz.asc     && tar -xf crate-5.10.11.tar.gz -C /crate --strip-components=1     && rm crate-5.10.11.tar.gz # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jul 2025 10:46:22 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 14 Jul 2025 10:46:22 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
VOLUME [/data]
# Mon, 14 Jul 2025 10:46:22 GMT
WORKDIR /data
# Mon, 14 Jul 2025 10:46:22 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-07-14T10:46:22.534581 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.11
# Mon, 14 Jul 2025 10:46:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 14 Jul 2025 10:46:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 14 Jul 2025 10:46:22 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bd8ea6f470495e95ac9ba70801dd6d46b9cae2f713269ebbdd43f06368799802`  
		Last Modified: Tue, 09 Sep 2025 20:21:52 GMT  
		Size: 65.5 MB (65518001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a621df3cef737ec5f897bb4ce7f93176dfc2ed3d192143daa0b25f665d59875`  
		Last Modified: Tue, 09 Sep 2025 21:12:17 GMT  
		Size: 14.6 MB (14585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d03e5a23c57071269e2c08c9c0bfc33211dbeb4e4284255e59c3381a58d0b1`  
		Last Modified: Tue, 09 Sep 2025 21:27:43 GMT  
		Size: 150.3 MB (150345634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a372a9f4cb3903dcf61ce4288f9fc8eb6ddc0efbdf7d189590e3a02f4b33fbe`  
		Last Modified: Tue, 09 Sep 2025 21:27:15 GMT  
		Size: 1.9 MB (1943636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852151834362117b6ea0af08cb6f6f58089b7b05ece1d7983f4e6cfa92894dd5`  
		Last Modified: Tue, 09 Sep 2025 21:27:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af50fed053716253dc344abf511a6e9887c131eabb9bd46038549b1f1f2a448`  
		Last Modified: Tue, 09 Sep 2025 21:27:15 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e9eeb51513545c8ac0cab29c4220c719a89391c06ac76b52a2a352001d5774`  
		Last Modified: Tue, 09 Sep 2025 21:27:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0d6110ec66b53dd73a00d6d859a3083d4142c15b4084c2c31032c6c08bf97`  
		Last Modified: Tue, 09 Sep 2025 21:27:15 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:30e85ef1d884ffca44a8d14168e25b6d0a2dd6f99c412becd9f6653d05cebb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a652f38489cec447f171b9ec0a96e7f6eae7418bf982081ca3339e293cbfd3`

```dockerfile
```

-	Layers:
	-	`sha256:c6a9d44ed5d56cd75ed71c9a19f3531028cb873b8874cfecbf79dc7c73287193`  
		Last Modified: Tue, 09 Sep 2025 23:38:29 GMT  
		Size: 5.2 MB (5185733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6994459e936f5011f6ff2d3c161dffb5bbc89eacbed7da3ed0c023a04da719`  
		Last Modified: Tue, 09 Sep 2025 23:38:30 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json
