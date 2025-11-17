## `crate:latest`

```console
$ docker pull crate@sha256:f9817ce5321f7bebb8cedb7173c0695b25ab87c97f1b0d656627f9f3bf440602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:0bdf38da9b5ed5fbad8334f56b4d9cbf97cbf742b6e8cb9bcffb720ea11ec534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232941747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a3c9f8388d4e955fdcd316eb96d7b9b78fd9583a960071a6da21497fe1b5ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:17 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:10:31 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:10:33 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:10:33 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:10:33 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:10:33 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:10:33 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:10:34 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 17 Nov 2025 19:10:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:10:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:10:34 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d30243396b69114a2abed81d7615648f3210d3b088c3f3ac3e89f5319084da6`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 14.5 MB (14512789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c276eb189c1af5d3bf0fd0cefd24a060d8a6550383d13462b6fb3e6fa0d5ae`  
		Last Modified: Mon, 17 Nov 2025 21:38:51 GMT  
		Size: 149.0 MB (149025676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b05b562a6fd9228ae7d82b2e7793a76011314b3a356341edac73b85ca5afd6`  
		Last Modified: Mon, 17 Nov 2025 19:11:11 GMT  
		Size: 1.9 MB (1943625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0095ebb24b8d759dd20faba6a5b334ad4e6bfe298152724494ede8d5bd299260`  
		Last Modified: Mon, 17 Nov 2025 19:11:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d331a5bb2bce80dd171a3b04d2fe75436c16570c57c282614ca56fbea6e5fa05`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6867a1b2a95053b959557200f693b34c8e0bae64ee6eb93b5d4619f335fb373f`  
		Last Modified: Mon, 17 Nov 2025 19:11:13 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559c9bea6e2e15503cf1339ebbec6faec7884bb9904f0baab6fe40f337cac67c`  
		Last Modified: Mon, 17 Nov 2025 19:11:12 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:1abc8a49d2ef58112da1c9c5684873939b91fc44bd6258482d3b19a5b2db1ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddc34abb05d97eb36ff501a71807fb80d4b232cf97dee06032a688a3a0963b8`

```dockerfile
```

-	Layers:
	-	`sha256:199b497c6f7f19f6a77f20290d79fdb58bcaffdbc750adb69e69547acdd19df2`  
		Last Modified: Mon, 17 Nov 2025 21:38:32 GMT  
		Size: 5.2 MB (5192280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bd724ee2ae808d82272bf96baad7d5358c4bfc0c12289fb6aa0253e93b02b4`  
		Last Modified: Mon, 17 Nov 2025 21:38:33 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:b99c41fe836ddbdf065725bccfc1f19b94b8c6bdc8e306025695fbeda84761a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232170117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f13a65e9e5abe5adf2921c3ce056d19c89c37130024bb5fe0ef06c3331b300b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:10:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 17 Nov 2025 19:10:41 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.3.tar.gz.asc crate-6.0.3.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.3.tar.gz.asc     && tar -xf crate-6.0.3.tar.gz -C /crate --strip-components=1     && rm crate-6.0.3.tar.gz # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 19:10:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 17 Nov 2025 19:10:42 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
VOLUME [/data]
# Mon, 17 Nov 2025 19:10:42 GMT
WORKDIR /data
# Mon, 17 Nov 2025 19:10:42 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 17 Nov 2025 19:10:42 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-10-13T15:42:38.643735 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.3
# Mon, 17 Nov 2025 19:10:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 17 Nov 2025 19:10:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 19:10:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc949e01002c33c0a4b000fb7e7b5c129ace63b14dcfff4ebf546b40b296d25d`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 14.6 MB (14567800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e94961dd5362a0f3f453e4e58213c94de87c8795dfa95d6086f5fa5375edaa5`  
		Last Modified: Mon, 17 Nov 2025 21:49:09 GMT  
		Size: 149.7 MB (149713818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feeed2533dfd110495dcfa1b70a91a18966271bdc0bcc32c212dec68f85d94e`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c1092f6284b549a5a6965163d3672be80cee960a64632d7664f66921b503b4`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6b08be77882453720be84648d36927bdf4bc975f54017e0671ab578f2b15fb`  
		Last Modified: Mon, 17 Nov 2025 19:11:17 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c2d3cb43bf253ec906622b1938ec4baf68119a8e372df4e780b0e4494fe0d`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f485f0a96ae712069ab1cba0a1c6cf8b7524477011ac9dd448bf88cbebbe4e6`  
		Last Modified: Mon, 17 Nov 2025 19:11:16 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:7512135d603bf980beee0e1e18f7bec5766d157bdfc9c48660c3d0d5fc9c959d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6ecdeefed9c7c057dc6a6bb9246306761a979754487230215941c91513a2e6`

```dockerfile
```

-	Layers:
	-	`sha256:daafe8ffaba6b98b107ddcac59b468b6ee6592312ae2e776fb164be9db2d6040`  
		Last Modified: Mon, 17 Nov 2025 21:38:38 GMT  
		Size: 5.2 MB (5190199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9f2f0bf59a880c080ac68e721bd9a6643b38a5a093f16d5f2ebad1d808e555`  
		Last Modified: Mon, 17 Nov 2025 21:38:39 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
