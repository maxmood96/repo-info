<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.10`](#crate51010)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:8b7897295a1bc7257362a257b7783375efe6793d42a2612b6d5c0f06e4f64023
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:b703a2ac647d8372aaf9e3670e58ea5e9b96485a6f9827ecde5eef7ec06846fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233602846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f354d1d7b306d5b025adce6f3e80cd9f9d53cb8e9ac4c0e90aeb15f9411b210`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Jun 2025 13:21:27 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a8921e3a56e1a4cc06cb7da48fc229f2876ec325b449c8fc390063aaf1c0700d`  
		Last Modified: Wed, 09 Jul 2025 18:02:51 GMT  
		Size: 67.0 MB (66959755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589bed445a17f23939cf36bcdd44405eff26ac7d304baffa3e1e2cb6ae1f4d37`  
		Last Modified: Wed, 09 Jul 2025 20:38:39 GMT  
		Size: 15.0 MB (15033947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5afd619296f6821ca94d7e22be07b72838c4ff0394105346e7e7fd4dd59eda`  
		Last Modified: Wed, 09 Jul 2025 20:38:56 GMT  
		Size: 149.7 MB (149663642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcc984c5ab5a329b7f943d7ba09dfca4fdbbe3032e690853e453bd4bb85053b`  
		Last Modified: Wed, 09 Jul 2025 20:38:41 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede67530c72d8aba4b6d49fd39a5b7ab2622390a445067d9749cc64a91773573`  
		Last Modified: Wed, 09 Jul 2025 20:38:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d58805ea088a569ff359adcf4c50a53d289d711e6ecc9d8975486a43537bbb`  
		Last Modified: Wed, 09 Jul 2025 20:38:43 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc08e7737e51f3964bf49efc77cedbe686f12f161d2bf07abcb33d31c5ceb5c6`  
		Last Modified: Wed, 09 Jul 2025 20:38:43 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21069b5595d4b02757caa1f677e326d624fd24d0f4973c5947893856ca5130c1`  
		Last Modified: Wed, 09 Jul 2025 20:38:45 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:462bc13ec203f293a0ed2c0c085a1ba6100fa46b9b6ed83cee155a116eb94a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d79c26032725f6769293c8c3baaedf3f9fc8c20a5405a13d4eebdda659b356`

```dockerfile
```

-	Layers:
	-	`sha256:1d8d55bfec127dd2b46b20561250348270a2dad3d7714b40dfc6afa22b3f10e6`  
		Last Modified: Wed, 09 Jul 2025 20:38:23 GMT  
		Size: 5.2 MB (5184030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ad85c3ed886abae130fbc443ed7045e678fca8f8a57e1bb1bb6755a10fcf8c`  
		Last Modified: Wed, 09 Jul 2025 20:38:24 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:f49793088784507eb8213e571ab754089e6b55124569bb4d270a49c6fbdd338a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8573d505a2b644e38e94911549433502455c425b4ca07c8b8e38319c62bffb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Jun 2025 13:21:27 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:05b4d6cb1ce9c295698618994d5c709d00e4d52747dbc6db2e6386760e6a8490`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 65.5 MB (65450956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431bb707880e0b6b7b5b7a325fdcaf3b0e8cbf7e303d1bb39475b4da8fff4a67`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 15.1 MB (15090722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462386bbd109f1205b0f3a5f4a34b5e04d6e64e6c372f76fdc6b60e8c57ab737`  
		Last Modified: Wed, 09 Jul 2025 21:21:39 GMT  
		Size: 150.3 MB (150342612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dfb4e6e9d4ec71920400a123442dc2d3dbb1ea14ee31e24e0a0b0dc67ac80d`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a0577704a309fcc9a89983168f3554809e14348f34b70073d480d9e609f3ce`  
		Last Modified: Wed, 09 Jul 2025 20:21:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3c98bdf27f0201b2a0d2f7dd003ef7f02a02fc58d7403e2ba96ab1cb8c7485`  
		Last Modified: Wed, 09 Jul 2025 20:21:27 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33845a0ade81b8d8b06f4309beddcd23c850e56968d01da66768f7a7edd2529`  
		Last Modified: Wed, 09 Jul 2025 20:21:27 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b3b1a47758405fafd413589e44588692145625cd139acc1cf74f816bae7d2`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:02a8c1d8c38b56fa723e6a68022bfbdf14aa580e3e80328ae95f73522c3ac8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa59a4b8d9a029bbf0d072bf7bd872c05827219c597637c12ea50e6c9e074924`

```dockerfile
```

-	Layers:
	-	`sha256:175a5e7429773b90c9236b179c8e745c0a93c0fe83d0db3914fe9af093db902f`  
		Last Modified: Wed, 09 Jul 2025 20:38:29 GMT  
		Size: 5.2 MB (5181338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cd0c6f73ec4708aef2a1e4e983d9765d9c8650861d164f80218bdda535b1c1`  
		Last Modified: Wed, 09 Jul 2025 20:38:32 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.10`

```console
$ docker pull crate@sha256:8b7897295a1bc7257362a257b7783375efe6793d42a2612b6d5c0f06e4f64023
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.10` - linux; amd64

```console
$ docker pull crate@sha256:b703a2ac647d8372aaf9e3670e58ea5e9b96485a6f9827ecde5eef7ec06846fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233602846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f354d1d7b306d5b025adce6f3e80cd9f9d53cb8e9ac4c0e90aeb15f9411b210`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Jun 2025 13:21:27 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a8921e3a56e1a4cc06cb7da48fc229f2876ec325b449c8fc390063aaf1c0700d`  
		Last Modified: Wed, 09 Jul 2025 18:02:51 GMT  
		Size: 67.0 MB (66959755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589bed445a17f23939cf36bcdd44405eff26ac7d304baffa3e1e2cb6ae1f4d37`  
		Last Modified: Wed, 09 Jul 2025 20:38:39 GMT  
		Size: 15.0 MB (15033947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5afd619296f6821ca94d7e22be07b72838c4ff0394105346e7e7fd4dd59eda`  
		Last Modified: Wed, 09 Jul 2025 20:38:56 GMT  
		Size: 149.7 MB (149663642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcc984c5ab5a329b7f943d7ba09dfca4fdbbe3032e690853e453bd4bb85053b`  
		Last Modified: Wed, 09 Jul 2025 20:38:41 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede67530c72d8aba4b6d49fd39a5b7ab2622390a445067d9749cc64a91773573`  
		Last Modified: Wed, 09 Jul 2025 20:38:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d58805ea088a569ff359adcf4c50a53d289d711e6ecc9d8975486a43537bbb`  
		Last Modified: Wed, 09 Jul 2025 20:38:43 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc08e7737e51f3964bf49efc77cedbe686f12f161d2bf07abcb33d31c5ceb5c6`  
		Last Modified: Wed, 09 Jul 2025 20:38:43 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21069b5595d4b02757caa1f677e326d624fd24d0f4973c5947893856ca5130c1`  
		Last Modified: Wed, 09 Jul 2025 20:38:45 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.10` - unknown; unknown

```console
$ docker pull crate@sha256:462bc13ec203f293a0ed2c0c085a1ba6100fa46b9b6ed83cee155a116eb94a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d79c26032725f6769293c8c3baaedf3f9fc8c20a5405a13d4eebdda659b356`

```dockerfile
```

-	Layers:
	-	`sha256:1d8d55bfec127dd2b46b20561250348270a2dad3d7714b40dfc6afa22b3f10e6`  
		Last Modified: Wed, 09 Jul 2025 20:38:23 GMT  
		Size: 5.2 MB (5184030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ad85c3ed886abae130fbc443ed7045e678fca8f8a57e1bb1bb6755a10fcf8c`  
		Last Modified: Wed, 09 Jul 2025 20:38:24 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:f49793088784507eb8213e571ab754089e6b55124569bb4d270a49c6fbdd338a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8573d505a2b644e38e94911549433502455c425b4ca07c8b8e38319c62bffb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Jun 2025 13:21:27 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:05b4d6cb1ce9c295698618994d5c709d00e4d52747dbc6db2e6386760e6a8490`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 65.5 MB (65450956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431bb707880e0b6b7b5b7a325fdcaf3b0e8cbf7e303d1bb39475b4da8fff4a67`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 15.1 MB (15090722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462386bbd109f1205b0f3a5f4a34b5e04d6e64e6c372f76fdc6b60e8c57ab737`  
		Last Modified: Wed, 09 Jul 2025 21:21:39 GMT  
		Size: 150.3 MB (150342612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dfb4e6e9d4ec71920400a123442dc2d3dbb1ea14ee31e24e0a0b0dc67ac80d`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a0577704a309fcc9a89983168f3554809e14348f34b70073d480d9e609f3ce`  
		Last Modified: Wed, 09 Jul 2025 20:21:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3c98bdf27f0201b2a0d2f7dd003ef7f02a02fc58d7403e2ba96ab1cb8c7485`  
		Last Modified: Wed, 09 Jul 2025 20:21:27 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33845a0ade81b8d8b06f4309beddcd23c850e56968d01da66768f7a7edd2529`  
		Last Modified: Wed, 09 Jul 2025 20:21:27 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b3b1a47758405fafd413589e44588692145625cd139acc1cf74f816bae7d2`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.10` - unknown; unknown

```console
$ docker pull crate@sha256:02a8c1d8c38b56fa723e6a68022bfbdf14aa580e3e80328ae95f73522c3ac8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa59a4b8d9a029bbf0d072bf7bd872c05827219c597637c12ea50e6c9e074924`

```dockerfile
```

-	Layers:
	-	`sha256:175a5e7429773b90c9236b179c8e745c0a93c0fe83d0db3914fe9af093db902f`  
		Last Modified: Wed, 09 Jul 2025 20:38:29 GMT  
		Size: 5.2 MB (5181338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cd0c6f73ec4708aef2a1e4e983d9765d9c8650861d164f80218bdda535b1c1`  
		Last Modified: Wed, 09 Jul 2025 20:38:32 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9`

```console
$ docker pull crate@sha256:5cc29485dc6584230b49e8f82f76716cc2875c68a9f4e60cee1123d378b4cd23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:d1c34e74ba8b6b7735615cc43c7aa50b1f538511c93a5fe176c1e1191fb8f434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232948560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b820489ed668e675fcfbcba73257e17b6ca54a634ac1f84df86636fd4d570a1d`
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
	-	`sha256:a8921e3a56e1a4cc06cb7da48fc229f2876ec325b449c8fc390063aaf1c0700d`  
		Last Modified: Wed, 09 Jul 2025 18:02:51 GMT  
		Size: 67.0 MB (66959755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6670f6dfaf015e2f058d6fd7ea581a6039eaceea717fa35387a26071561b2ca`  
		Last Modified: Wed, 09 Jul 2025 22:16:36 GMT  
		Size: 15.0 MB (15033832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e48c55197c82da7b563bcbc3d35a17f726a20677c76109bdb309572b7c0de2`  
		Last Modified: Wed, 09 Jul 2025 22:16:52 GMT  
		Size: 149.0 MB (149009465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce1cbac5c04fb7e9e04d87655a5e09428f3138cb44426d5e0dfb8b78f9215e3`  
		Last Modified: Wed, 09 Jul 2025 22:16:40 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a4b24a562d2238011a5cf8094d5c2e675dd20809d2b5b7f8597846157073f7`  
		Last Modified: Wed, 09 Jul 2025 22:16:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f81986dd8ded961ca5e3eed54418603853c7113ffa6dbd32f9e47c69caff4e`  
		Last Modified: Wed, 09 Jul 2025 22:16:44 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacf4e84fb28bb7af5f8ecb2eeea731adfc2e2b7f8dd9b56bfcdc75fc07154a6`  
		Last Modified: Wed, 09 Jul 2025 22:16:45 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a199c7337211a43d075efbfa36754cd80c62ada61de0cc58e4ba414a7dd5632`  
		Last Modified: Wed, 09 Jul 2025 22:16:47 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:59cc548a7c61b2e5c6b6208d54db616646590c739c2712af4575690d46e54c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09fa7b3e6b2595da3c19e56128a75f2aa3a4408b9d1e9ba9aaa07636fdf096`

```dockerfile
```

-	Layers:
	-	`sha256:7fb4aac7612c987f45eba990ed9dac62e9a5da6c26d59e7036415557ea8ec6bd`  
		Last Modified: Wed, 09 Jul 2025 20:38:31 GMT  
		Size: 5.2 MB (5182095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cfa45b2bcce999b476a518f43e1f3006d28b31de3a7b0473f9b82ce809dd976`  
		Last Modified: Wed, 09 Jul 2025 20:38:32 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:2ddff1381fe4c4079a23ed19a7fbf6008fab47b81530a02da216d5e22b70a5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232195768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d33b53a50f3156d2c14d5c508e24b354087b07538e785f0fa92a54f3986dca7`
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
	-	`sha256:05b4d6cb1ce9c295698618994d5c709d00e4d52747dbc6db2e6386760e6a8490`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 65.5 MB (65450956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431bb707880e0b6b7b5b7a325fdcaf3b0e8cbf7e303d1bb39475b4da8fff4a67`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 15.1 MB (15090722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee23be934a33c0c81cd6cfd2daef691242a40c8dff73f60d1ee8e81c44975a`  
		Last Modified: Wed, 09 Jul 2025 22:17:45 GMT  
		Size: 149.7 MB (149708578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63deb25e06c4beb8e52f8e8e60a9bfc6a0a4e1514c691fcfe4e27e15bd9ee29e`  
		Last Modified: Wed, 09 Jul 2025 20:22:01 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47840383781747e5d76c1a4f4b722db23546d28bbd452a50f0bac063545569f8`  
		Last Modified: Wed, 09 Jul 2025 20:22:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447ffeb0095931431167256a1eb7341f19802fe129684cb0813cd0674ea222`  
		Last Modified: Wed, 09 Jul 2025 20:22:00 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479d227fb6d99c88175f1fc2c742c2fe073bd70af08a19f0924833f66b521fce`  
		Last Modified: Wed, 09 Jul 2025 20:22:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e6039660321860260a25c5f76efe48bf214ef3f0452b092a83cb26a617daf2`  
		Last Modified: Wed, 09 Jul 2025 20:22:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:4e5cab6dd0f598c436ec9202a5c096200b2f85df1ae9e8ff80b37b9b751f70ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682545915806062a9f96af330f845b3f072b968114d1b9fdf52fd81b5695b11c`

```dockerfile
```

-	Layers:
	-	`sha256:bbb1201750476cca4583be2b2599aae7d188b65ef0f0b0457106f45179e5fca9`  
		Last Modified: Wed, 09 Jul 2025 20:38:37 GMT  
		Size: 5.2 MB (5179391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f586b375deca916f4a7f1fa90e3b5b2d008da6df4451418433607cc52a695cd`  
		Last Modified: Wed, 09 Jul 2025 20:38:38 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:5cc29485dc6584230b49e8f82f76716cc2875c68a9f4e60cee1123d378b4cd23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:d1c34e74ba8b6b7735615cc43c7aa50b1f538511c93a5fe176c1e1191fb8f434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232948560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b820489ed668e675fcfbcba73257e17b6ca54a634ac1f84df86636fd4d570a1d`
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
	-	`sha256:a8921e3a56e1a4cc06cb7da48fc229f2876ec325b449c8fc390063aaf1c0700d`  
		Last Modified: Wed, 09 Jul 2025 18:02:51 GMT  
		Size: 67.0 MB (66959755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6670f6dfaf015e2f058d6fd7ea581a6039eaceea717fa35387a26071561b2ca`  
		Last Modified: Wed, 09 Jul 2025 22:16:36 GMT  
		Size: 15.0 MB (15033832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e48c55197c82da7b563bcbc3d35a17f726a20677c76109bdb309572b7c0de2`  
		Last Modified: Wed, 09 Jul 2025 22:16:52 GMT  
		Size: 149.0 MB (149009465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce1cbac5c04fb7e9e04d87655a5e09428f3138cb44426d5e0dfb8b78f9215e3`  
		Last Modified: Wed, 09 Jul 2025 22:16:40 GMT  
		Size: 1.9 MB (1943626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a4b24a562d2238011a5cf8094d5c2e675dd20809d2b5b7f8597846157073f7`  
		Last Modified: Wed, 09 Jul 2025 22:16:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f81986dd8ded961ca5e3eed54418603853c7113ffa6dbd32f9e47c69caff4e`  
		Last Modified: Wed, 09 Jul 2025 22:16:44 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacf4e84fb28bb7af5f8ecb2eeea731adfc2e2b7f8dd9b56bfcdc75fc07154a6`  
		Last Modified: Wed, 09 Jul 2025 22:16:45 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a199c7337211a43d075efbfa36754cd80c62ada61de0cc58e4ba414a7dd5632`  
		Last Modified: Wed, 09 Jul 2025 22:16:47 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:59cc548a7c61b2e5c6b6208d54db616646590c739c2712af4575690d46e54c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09fa7b3e6b2595da3c19e56128a75f2aa3a4408b9d1e9ba9aaa07636fdf096`

```dockerfile
```

-	Layers:
	-	`sha256:7fb4aac7612c987f45eba990ed9dac62e9a5da6c26d59e7036415557ea8ec6bd`  
		Last Modified: Wed, 09 Jul 2025 20:38:31 GMT  
		Size: 5.2 MB (5182095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cfa45b2bcce999b476a518f43e1f3006d28b31de3a7b0473f9b82ce809dd976`  
		Last Modified: Wed, 09 Jul 2025 20:38:32 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:2ddff1381fe4c4079a23ed19a7fbf6008fab47b81530a02da216d5e22b70a5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232195768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d33b53a50f3156d2c14d5c508e24b354087b07538e785f0fa92a54f3986dca7`
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
	-	`sha256:05b4d6cb1ce9c295698618994d5c709d00e4d52747dbc6db2e6386760e6a8490`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 65.5 MB (65450956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431bb707880e0b6b7b5b7a325fdcaf3b0e8cbf7e303d1bb39475b4da8fff4a67`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 15.1 MB (15090722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee23be934a33c0c81cd6cfd2daef691242a40c8dff73f60d1ee8e81c44975a`  
		Last Modified: Wed, 09 Jul 2025 22:17:45 GMT  
		Size: 149.7 MB (149708578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63deb25e06c4beb8e52f8e8e60a9bfc6a0a4e1514c691fcfe4e27e15bd9ee29e`  
		Last Modified: Wed, 09 Jul 2025 20:22:01 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47840383781747e5d76c1a4f4b722db23546d28bbd452a50f0bac063545569f8`  
		Last Modified: Wed, 09 Jul 2025 20:22:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447ffeb0095931431167256a1eb7341f19802fe129684cb0813cd0674ea222`  
		Last Modified: Wed, 09 Jul 2025 20:22:00 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479d227fb6d99c88175f1fc2c742c2fe073bd70af08a19f0924833f66b521fce`  
		Last Modified: Wed, 09 Jul 2025 20:22:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e6039660321860260a25c5f76efe48bf214ef3f0452b092a83cb26a617daf2`  
		Last Modified: Wed, 09 Jul 2025 20:22:00 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:4e5cab6dd0f598c436ec9202a5c096200b2f85df1ae9e8ff80b37b9b751f70ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682545915806062a9f96af330f845b3f072b968114d1b9fdf52fd81b5695b11c`

```dockerfile
```

-	Layers:
	-	`sha256:bbb1201750476cca4583be2b2599aae7d188b65ef0f0b0457106f45179e5fca9`  
		Last Modified: Wed, 09 Jul 2025 20:38:37 GMT  
		Size: 5.2 MB (5179391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f586b375deca916f4a7f1fa90e3b5b2d008da6df4451418433607cc52a695cd`  
		Last Modified: Wed, 09 Jul 2025 20:38:38 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:8b7897295a1bc7257362a257b7783375efe6793d42a2612b6d5c0f06e4f64023
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:b703a2ac647d8372aaf9e3670e58ea5e9b96485a6f9827ecde5eef7ec06846fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233602846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f354d1d7b306d5b025adce6f3e80cd9f9d53cb8e9ac4c0e90aeb15f9411b210`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Jun 2025 13:21:27 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a8921e3a56e1a4cc06cb7da48fc229f2876ec325b449c8fc390063aaf1c0700d`  
		Last Modified: Wed, 09 Jul 2025 18:02:51 GMT  
		Size: 67.0 MB (66959755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589bed445a17f23939cf36bcdd44405eff26ac7d304baffa3e1e2cb6ae1f4d37`  
		Last Modified: Wed, 09 Jul 2025 20:38:39 GMT  
		Size: 15.0 MB (15033947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5afd619296f6821ca94d7e22be07b72838c4ff0394105346e7e7fd4dd59eda`  
		Last Modified: Wed, 09 Jul 2025 20:38:56 GMT  
		Size: 149.7 MB (149663642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcc984c5ab5a329b7f943d7ba09dfca4fdbbe3032e690853e453bd4bb85053b`  
		Last Modified: Wed, 09 Jul 2025 20:38:41 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede67530c72d8aba4b6d49fd39a5b7ab2622390a445067d9749cc64a91773573`  
		Last Modified: Wed, 09 Jul 2025 20:38:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d58805ea088a569ff359adcf4c50a53d289d711e6ecc9d8975486a43537bbb`  
		Last Modified: Wed, 09 Jul 2025 20:38:43 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc08e7737e51f3964bf49efc77cedbe686f12f161d2bf07abcb33d31c5ceb5c6`  
		Last Modified: Wed, 09 Jul 2025 20:38:43 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21069b5595d4b02757caa1f677e326d624fd24d0f4973c5947893856ca5130c1`  
		Last Modified: Wed, 09 Jul 2025 20:38:45 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:462bc13ec203f293a0ed2c0c085a1ba6100fa46b9b6ed83cee155a116eb94a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d79c26032725f6769293c8c3baaedf3f9fc8c20a5405a13d4eebdda659b356`

```dockerfile
```

-	Layers:
	-	`sha256:1d8d55bfec127dd2b46b20561250348270a2dad3d7714b40dfc6afa22b3f10e6`  
		Last Modified: Wed, 09 Jul 2025 20:38:23 GMT  
		Size: 5.2 MB (5184030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ad85c3ed886abae130fbc443ed7045e678fca8f8a57e1bb1bb6755a10fcf8c`  
		Last Modified: Wed, 09 Jul 2025 20:38:24 GMT  
		Size: 23.2 KB (23217 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:f49793088784507eb8213e571ab754089e6b55124569bb4d270a49c6fbdd338a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8573d505a2b644e38e94911549433502455c425b4ca07c8b8e38319c62bffb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 30 Jun 2025 13:21:27 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["/bin/bash"]
# Mon, 30 Jun 2025 13:21:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.10.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.10.tar.gz.asc crate-5.10.10.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.10.tar.gz.asc     && tar -xf crate-5.10.10.tar.gz -C /crate --strip-components=1     && rm crate-5.10.10.tar.gz # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 13:21:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 30 Jun 2025 13:21:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
VOLUME [/data]
# Mon, 30 Jun 2025 13:21:27 GMT
WORKDIR /data
# Mon, 30 Jun 2025 13:21:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-06-30T13:21:27.513451 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.10
# Mon, 30 Jun 2025 13:21:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 30 Jun 2025 13:21:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 30 Jun 2025 13:21:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:05b4d6cb1ce9c295698618994d5c709d00e4d52747dbc6db2e6386760e6a8490`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 65.5 MB (65450956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431bb707880e0b6b7b5b7a325fdcaf3b0e8cbf7e303d1bb39475b4da8fff4a67`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 15.1 MB (15090722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462386bbd109f1205b0f3a5f4a34b5e04d6e64e6c372f76fdc6b60e8c57ab737`  
		Last Modified: Wed, 09 Jul 2025 21:21:39 GMT  
		Size: 150.3 MB (150342612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dfb4e6e9d4ec71920400a123442dc2d3dbb1ea14ee31e24e0a0b0dc67ac80d`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a0577704a309fcc9a89983168f3554809e14348f34b70073d480d9e609f3ce`  
		Last Modified: Wed, 09 Jul 2025 20:21:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3c98bdf27f0201b2a0d2f7dd003ef7f02a02fc58d7403e2ba96ab1cb8c7485`  
		Last Modified: Wed, 09 Jul 2025 20:21:27 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33845a0ade81b8d8b06f4309beddcd23c850e56968d01da66768f7a7edd2529`  
		Last Modified: Wed, 09 Jul 2025 20:21:27 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b3b1a47758405fafd413589e44588692145625cd139acc1cf74f816bae7d2`  
		Last Modified: Wed, 09 Jul 2025 20:21:28 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:02a8c1d8c38b56fa723e6a68022bfbdf14aa580e3e80328ae95f73522c3ac8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa59a4b8d9a029bbf0d072bf7bd872c05827219c597637c12ea50e6c9e074924`

```dockerfile
```

-	Layers:
	-	`sha256:175a5e7429773b90c9236b179c8e745c0a93c0fe83d0db3914fe9af093db902f`  
		Last Modified: Wed, 09 Jul 2025 20:38:29 GMT  
		Size: 5.2 MB (5181338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cd0c6f73ec4708aef2a1e4e983d9765d9c8650861d164f80218bdda535b1c1`  
		Last Modified: Wed, 09 Jul 2025 20:38:32 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.in-toto+json
