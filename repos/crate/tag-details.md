<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.9`](#crate5109)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:433619fecc826f0cc4c001b74021d97790e99c864b2ab18fa1d7b571d9501a4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:f8b75c5398dcfd7d93f4287ead916a7b91eb36449a749a1b17313e7a21d5a1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234152850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213309da335c806853039944dc33bd7815399715666c95cbf47a57652f05ceeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 26 May 2025 12:14:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e721abbbcb58c29477a55c8d3d3b30cab0e2e8924454729683616bd8488c936c`  
		Last Modified: Wed, 11 Jun 2025 20:38:45 GMT  
		Size: 15.4 MB (15357879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d817f2dcf68a444aff0445c5c0c81db7f01842004d965b6cebfb02dd7ceac0f`  
		Last Modified: Wed, 11 Jun 2025 20:38:58 GMT  
		Size: 149.7 MB (149661544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf15ba17ff1596ed61a733be27c3d2e1a42cd923d39a35324d88b899aef1d486`  
		Last Modified: Wed, 11 Jun 2025 18:11:43 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b0df149301b226294672f6c3e285b35eca59c12d0f52efc097dc62d81b489d`  
		Last Modified: Wed, 11 Jun 2025 18:11:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b69c8ca518ff60df6ae5fade6713749e82608085596af9c285ae42404905c8`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a857f25fa4a78fcdf41c80a30476a16e5459e088c8982cb593a19391fa0dcf`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22574c8597ac178b56e1f1b276d62ea4028eaf660bbaf18febb3b13671bd3ed2`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:7b4611be72809687b46ea670d83b9cebe0ca3ce6119595db2d853accc4758ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9323e1812dce74fbcbfbab6957f12e55612ccdbb4af4a7fdabf572cda9b515`

```dockerfile
```

-	Layers:
	-	`sha256:28c69fb962f91294a732a6b4944fec9b147bd621e88b986f3d41be2920db4875`  
		Last Modified: Wed, 11 Jun 2025 20:38:20 GMT  
		Size: 5.2 MB (5183295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cc37bdcff6b6b8324392b45419020766a490e4fc0a53650b5f4f6b8f4ab727`  
		Last Modified: Wed, 11 Jun 2025 20:38:21 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e43b458826eeb1282a9cfbcf39c92da985b132afaff4c2c58f3d9126e158c56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233379705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511394d677e78ded40f69d0f71c6e523b897be243af58caa42b594583aecd626`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 26 May 2025 12:14:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:64ea4def3bd0a4dc5721f0a518e4753a76def8e8678ce5dc75311f784c5da1aa`  
		Last Modified: Wed, 11 Jun 2025 18:23:16 GMT  
		Size: 65.7 MB (65688045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975629a8e9c871567de319a634e165b3820062b282cf02f4b5f5d1e9a0f3a0f0`  
		Last Modified: Thu, 12 Jun 2025 06:12:43 GMT  
		Size: 15.4 MB (15409247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2c8a5e2f7c9eb89a17877cf97df6e8330a2787059e2c7838e94b75184cfb2a`  
		Last Modified: Thu, 12 Jun 2025 06:12:48 GMT  
		Size: 150.3 MB (150336903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d081feffd7838e79ea6988204a5dc17efb8ee2a4d27d3f8c905b104cdd30fa`  
		Last Modified: Thu, 12 Jun 2025 04:50:24 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da41847b7e7c73e14a860526be6e07f073a842fd79a844d6ed6091095016bf7c`  
		Last Modified: Thu, 12 Jun 2025 04:50:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3fa43e45dd7763bac117c9b62048989ffda5cdd3559341080377489c224a8d`  
		Last Modified: Thu, 12 Jun 2025 04:46:28 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899260b73b88bb3f633c071b1f0fcdad39379edb52c663a89293eb063d7d0e90`  
		Last Modified: Thu, 12 Jun 2025 04:46:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913be80c1ae410417ca1c52c8419254e5bacac531f56d3d7b6a723f3aeb258e`  
		Last Modified: Thu, 12 Jun 2025 04:46:36 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:93c73b244c5e618d71561ca8ef1805625a0d3b901434c2da1e86ca8000d67dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2c5e4c4887b379ad3f4af836dca9ff4d5095c5bb93664afa2cace34c866fa9`

```dockerfile
```

-	Layers:
	-	`sha256:58af19d623b826fa7c7566d982e5110c706b887880fe45f054ec42ccc4a3cbd9`  
		Last Modified: Thu, 12 Jun 2025 05:38:22 GMT  
		Size: 5.2 MB (5180603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc694f5f0f1e327d194d11c59046aebe9cc04f1969177d55a96e9e6f7ea70e8f`  
		Last Modified: Thu, 12 Jun 2025 05:38:23 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.9`

**does not exist** (yet?)

## `crate:5.9`

```console
$ docker pull crate@sha256:0c51896428e789e297c0c9d8ae0d086ba62d8408730bf2862bf55620b2ac47fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:5b4446f6465c45ec8b1d490dd978596ec48a0593aaea164500ebaa6e6433ac8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233500953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db96544d983dee5a0e34312c086a49add28a1de1dce76aa2764faa13e4d4fa14`
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
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51b65326593f93bdd91d295d7e557450e325451b3b3b1b93f6a40fb1963a36f`  
		Last Modified: Wed, 11 Jun 2025 23:19:32 GMT  
		Size: 15.4 MB (15357833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b9a7b725d7c5c227eaa66725d4602170e5bd2775ecc45d74e6b73de5a52413`  
		Last Modified: Wed, 11 Jun 2025 23:19:41 GMT  
		Size: 149.0 MB (149009698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a10eb670d32e35520cbddc7a9350633f3b91ce0c44f08a6c11ce115b500fca`  
		Last Modified: Wed, 11 Jun 2025 18:10:05 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d190e0a48abb2f0c93b39f6f891ebc627e5aba0f3bf302a4b7b5963d797fa14`  
		Last Modified: Wed, 11 Jun 2025 18:10:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10e918c1f6fd6245d53606186c00c196e41b38468b78d23d62b6108373707d7`  
		Last Modified: Wed, 11 Jun 2025 18:10:19 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a94e6e4cfc75c14691e52244fb83defb2b7552e499311ef8d82634218375f5f`  
		Last Modified: Wed, 11 Jun 2025 18:10:23 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22574c8597ac178b56e1f1b276d62ea4028eaf660bbaf18febb3b13671bd3ed2`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:4c4160f567b7e8d331e2a5736cb5f096bb9efba1091dd12c66aa7046314888c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5901757c1bcfb4fcb9f4c942783703a5a0f7feb7a18c1e9cfcb0a037e1244ef0`

```dockerfile
```

-	Layers:
	-	`sha256:5c9a4f0c90b41fd3ed3fabb7aa63dc9a6b160cfe85452c13ad2157706652b030`  
		Last Modified: Wed, 11 Jun 2025 20:38:26 GMT  
		Size: 5.2 MB (5181428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12aa68934dd28bbf5541eab122c195a8c33f9f8cd6b7aee38286d65c938cf924`  
		Last Modified: Wed, 11 Jun 2025 20:38:27 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:f45218332b08e96de0d23e578191189c92b7940316f59e9d46de5b1c1330dd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232751340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f6769cad003fb88285496c6585887754137d6be13201f4a0af51d99fa099c`
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
	-	`sha256:64ea4def3bd0a4dc5721f0a518e4753a76def8e8678ce5dc75311f784c5da1aa`  
		Last Modified: Wed, 11 Jun 2025 18:23:16 GMT  
		Size: 65.7 MB (65688045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975629a8e9c871567de319a634e165b3820062b282cf02f4b5f5d1e9a0f3a0f0`  
		Last Modified: Thu, 12 Jun 2025 06:12:43 GMT  
		Size: 15.4 MB (15409247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0df37ad3bbae4b3e1e8b5a5faa0300948774d6478f9a52187bf62c30f54a04`  
		Last Modified: Thu, 12 Jun 2025 12:18:24 GMT  
		Size: 149.7 MB (149708538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30edab8c2f093adc381d09a5b1148cba34b8ec89f24722402115da93555984ad`  
		Last Modified: Thu, 12 Jun 2025 04:55:32 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45fb1e67e41a5024490ce8019d771cad63228d8072b69ebecb114031e2854cc`  
		Last Modified: Thu, 12 Jun 2025 04:55:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd9865901db5cba0d95c8876983a6dcf0d269ee74547e1b3314e3df030e6346`  
		Last Modified: Thu, 12 Jun 2025 04:55:58 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfd3e2584488c3f049cabfadaee99b20ec04bd4f4953c4f829ca1dc44baa4a1`  
		Last Modified: Thu, 12 Jun 2025 04:56:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea497212c9651e773522151c6c295025f34d2c09fc5691e089c07a8778a6ee`  
		Last Modified: Thu, 12 Jun 2025 04:56:05 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:e3798d1e8aa55fc98021754792789818d986325f74568e49f50e8b39dbe2010f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a790b0660c3d88429a02b2847814e61ed26dc9d11e0b882e1727be9ad1e6e37c`

```dockerfile
```

-	Layers:
	-	`sha256:6d6d22f6af5777b254cb12620f7e4775513b114a31ae1bc0da288ce52627623a`  
		Last Modified: Thu, 12 Jun 2025 05:38:28 GMT  
		Size: 5.2 MB (5178724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce501395edc091051025a9100df132186c10868694956548f4cec682b45b301`  
		Last Modified: Thu, 12 Jun 2025 05:38:29 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:0c51896428e789e297c0c9d8ae0d086ba62d8408730bf2862bf55620b2ac47fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:5b4446f6465c45ec8b1d490dd978596ec48a0593aaea164500ebaa6e6433ac8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233500953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db96544d983dee5a0e34312c086a49add28a1de1dce76aa2764faa13e4d4fa14`
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
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51b65326593f93bdd91d295d7e557450e325451b3b3b1b93f6a40fb1963a36f`  
		Last Modified: Wed, 11 Jun 2025 23:19:32 GMT  
		Size: 15.4 MB (15357833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b9a7b725d7c5c227eaa66725d4602170e5bd2775ecc45d74e6b73de5a52413`  
		Last Modified: Wed, 11 Jun 2025 23:19:41 GMT  
		Size: 149.0 MB (149009698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a10eb670d32e35520cbddc7a9350633f3b91ce0c44f08a6c11ce115b500fca`  
		Last Modified: Wed, 11 Jun 2025 18:10:05 GMT  
		Size: 1.9 MB (1943629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d190e0a48abb2f0c93b39f6f891ebc627e5aba0f3bf302a4b7b5963d797fa14`  
		Last Modified: Wed, 11 Jun 2025 18:10:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10e918c1f6fd6245d53606186c00c196e41b38468b78d23d62b6108373707d7`  
		Last Modified: Wed, 11 Jun 2025 18:10:19 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a94e6e4cfc75c14691e52244fb83defb2b7552e499311ef8d82634218375f5f`  
		Last Modified: Wed, 11 Jun 2025 18:10:23 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22574c8597ac178b56e1f1b276d62ea4028eaf660bbaf18febb3b13671bd3ed2`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:4c4160f567b7e8d331e2a5736cb5f096bb9efba1091dd12c66aa7046314888c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5901757c1bcfb4fcb9f4c942783703a5a0f7feb7a18c1e9cfcb0a037e1244ef0`

```dockerfile
```

-	Layers:
	-	`sha256:5c9a4f0c90b41fd3ed3fabb7aa63dc9a6b160cfe85452c13ad2157706652b030`  
		Last Modified: Wed, 11 Jun 2025 20:38:26 GMT  
		Size: 5.2 MB (5181428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12aa68934dd28bbf5541eab122c195a8c33f9f8cd6b7aee38286d65c938cf924`  
		Last Modified: Wed, 11 Jun 2025 20:38:27 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:f45218332b08e96de0d23e578191189c92b7940316f59e9d46de5b1c1330dd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232751340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f6769cad003fb88285496c6585887754137d6be13201f4a0af51d99fa099c`
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
	-	`sha256:64ea4def3bd0a4dc5721f0a518e4753a76def8e8678ce5dc75311f784c5da1aa`  
		Last Modified: Wed, 11 Jun 2025 18:23:16 GMT  
		Size: 65.7 MB (65688045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975629a8e9c871567de319a634e165b3820062b282cf02f4b5f5d1e9a0f3a0f0`  
		Last Modified: Thu, 12 Jun 2025 06:12:43 GMT  
		Size: 15.4 MB (15409247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0df37ad3bbae4b3e1e8b5a5faa0300948774d6478f9a52187bf62c30f54a04`  
		Last Modified: Thu, 12 Jun 2025 12:18:24 GMT  
		Size: 149.7 MB (149708538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30edab8c2f093adc381d09a5b1148cba34b8ec89f24722402115da93555984ad`  
		Last Modified: Thu, 12 Jun 2025 04:55:32 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45fb1e67e41a5024490ce8019d771cad63228d8072b69ebecb114031e2854cc`  
		Last Modified: Thu, 12 Jun 2025 04:55:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd9865901db5cba0d95c8876983a6dcf0d269ee74547e1b3314e3df030e6346`  
		Last Modified: Thu, 12 Jun 2025 04:55:58 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfd3e2584488c3f049cabfadaee99b20ec04bd4f4953c4f829ca1dc44baa4a1`  
		Last Modified: Thu, 12 Jun 2025 04:56:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea497212c9651e773522151c6c295025f34d2c09fc5691e089c07a8778a6ee`  
		Last Modified: Thu, 12 Jun 2025 04:56:05 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:e3798d1e8aa55fc98021754792789818d986325f74568e49f50e8b39dbe2010f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a790b0660c3d88429a02b2847814e61ed26dc9d11e0b882e1727be9ad1e6e37c`

```dockerfile
```

-	Layers:
	-	`sha256:6d6d22f6af5777b254cb12620f7e4775513b114a31ae1bc0da288ce52627623a`  
		Last Modified: Thu, 12 Jun 2025 05:38:28 GMT  
		Size: 5.2 MB (5178724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce501395edc091051025a9100df132186c10868694956548f4cec682b45b301`  
		Last Modified: Thu, 12 Jun 2025 05:38:29 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:433619fecc826f0cc4c001b74021d97790e99c864b2ab18fa1d7b571d9501a4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:f8b75c5398dcfd7d93f4287ead916a7b91eb36449a749a1b17313e7a21d5a1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234152850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213309da335c806853039944dc33bd7815399715666c95cbf47a57652f05ceeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 26 May 2025 12:14:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:58feddb50fa4df86e3c09a7339672c0179129a5c57e4688b24ccf7b59ad809e3`  
		Last Modified: Wed, 11 Jun 2025 18:01:05 GMT  
		Size: 67.2 MB (67187916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e721abbbcb58c29477a55c8d3d3b30cab0e2e8924454729683616bd8488c936c`  
		Last Modified: Wed, 11 Jun 2025 20:38:45 GMT  
		Size: 15.4 MB (15357879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d817f2dcf68a444aff0445c5c0c81db7f01842004d965b6cebfb02dd7ceac0f`  
		Last Modified: Wed, 11 Jun 2025 20:38:58 GMT  
		Size: 149.7 MB (149661544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf15ba17ff1596ed61a733be27c3d2e1a42cd923d39a35324d88b899aef1d486`  
		Last Modified: Wed, 11 Jun 2025 18:11:43 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b0df149301b226294672f6c3e285b35eca59c12d0f52efc097dc62d81b489d`  
		Last Modified: Wed, 11 Jun 2025 18:11:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b69c8ca518ff60df6ae5fade6713749e82608085596af9c285ae42404905c8`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a857f25fa4a78fcdf41c80a30476a16e5459e088c8982cb593a19391fa0dcf`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22574c8597ac178b56e1f1b276d62ea4028eaf660bbaf18febb3b13671bd3ed2`  
		Last Modified: Wed, 11 Jun 2025 18:08:22 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:7b4611be72809687b46ea670d83b9cebe0ca3ce6119595db2d853accc4758ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9323e1812dce74fbcbfbab6957f12e55612ccdbb4af4a7fdabf572cda9b515`

```dockerfile
```

-	Layers:
	-	`sha256:28c69fb962f91294a732a6b4944fec9b147bd621e88b986f3d41be2920db4875`  
		Last Modified: Wed, 11 Jun 2025 20:38:20 GMT  
		Size: 5.2 MB (5183295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cc37bdcff6b6b8324392b45419020766a490e4fc0a53650b5f4f6b8f4ab727`  
		Last Modified: Wed, 11 Jun 2025 20:38:21 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e43b458826eeb1282a9cfbcf39c92da985b132afaff4c2c58f3d9126e158c56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233379705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511394d677e78ded40f69d0f71c6e523b897be243af58caa42b594583aecd626`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 26 May 2025 12:14:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 12:14:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.7.tar.gz.asc crate-5.10.7.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.7.tar.gz.asc     && tar -xf crate-5.10.7.tar.gz -C /crate --strip-components=1     && rm crate-5.10.7.tar.gz # buildkit
# Mon, 26 May 2025 12:14:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 12:14:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 26 May 2025 12:14:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 26 May 2025 12:14:57 GMT
VOLUME [/data]
# Mon, 26 May 2025 12:14:57 GMT
WORKDIR /data
# Mon, 26 May 2025 12:14:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 26 May 2025 12:14:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 26 May 2025 12:14:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-05-26T12:14:57.152937 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.7
# Mon, 26 May 2025 12:14:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 26 May 2025 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 May 2025 12:14:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:64ea4def3bd0a4dc5721f0a518e4753a76def8e8678ce5dc75311f784c5da1aa`  
		Last Modified: Wed, 11 Jun 2025 18:23:16 GMT  
		Size: 65.7 MB (65688045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975629a8e9c871567de319a634e165b3820062b282cf02f4b5f5d1e9a0f3a0f0`  
		Last Modified: Thu, 12 Jun 2025 06:12:43 GMT  
		Size: 15.4 MB (15409247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2c8a5e2f7c9eb89a17877cf97df6e8330a2787059e2c7838e94b75184cfb2a`  
		Last Modified: Thu, 12 Jun 2025 06:12:48 GMT  
		Size: 150.3 MB (150336903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d081feffd7838e79ea6988204a5dc17efb8ee2a4d27d3f8c905b104cdd30fa`  
		Last Modified: Thu, 12 Jun 2025 04:50:24 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da41847b7e7c73e14a860526be6e07f073a842fd79a844d6ed6091095016bf7c`  
		Last Modified: Thu, 12 Jun 2025 04:50:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3fa43e45dd7763bac117c9b62048989ffda5cdd3559341080377489c224a8d`  
		Last Modified: Thu, 12 Jun 2025 04:46:28 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899260b73b88bb3f633c071b1f0fcdad39379edb52c663a89293eb063d7d0e90`  
		Last Modified: Thu, 12 Jun 2025 04:46:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913be80c1ae410417ca1c52c8419254e5bacac531f56d3d7b6a723f3aeb258e`  
		Last Modified: Thu, 12 Jun 2025 04:46:36 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:93c73b244c5e618d71561ca8ef1805625a0d3b901434c2da1e86ca8000d67dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2c5e4c4887b379ad3f4af836dca9ff4d5095c5bb93664afa2cace34c866fa9`

```dockerfile
```

-	Layers:
	-	`sha256:58af19d623b826fa7c7566d982e5110c706b887880fe45f054ec42ccc4a3cbd9`  
		Last Modified: Thu, 12 Jun 2025 05:38:22 GMT  
		Size: 5.2 MB (5180603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc694f5f0f1e327d194d11c59046aebe9cc04f1969177d55a96e9e6f7ea70e8f`  
		Last Modified: Thu, 12 Jun 2025 05:38:23 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json
