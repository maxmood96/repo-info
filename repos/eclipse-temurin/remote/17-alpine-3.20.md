## `eclipse-temurin:17-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:6c96fdaf7f47ee3bc230a7db0c720ed52d638a2716dbf4a0f2066fbe91dfdaa2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:967aef6ea11959b98007f166cc7ef9b28cc8f4458e8932b6b4ad84cfe05416e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168287409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7829e85db98d78f10536fc1cb33c2b584ba9660db78b5795fe4abe308ae06d6a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:00 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:09 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4dfea527f66034c5b6f4ca26afe692ae292fd267fd3b295c7f54f6461c65fd33';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:58:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e961ba03c11caf747e9f5c12d49d0e94f536d90c6c7b3c4a061dc4b1b84013`  
		Last Modified: Sat, 08 Nov 2025 17:58:25 GMT  
		Size: 20.7 MB (20668276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262951093642e53fbcd757230bb022dfe1bce8b4bae42794030ba6c6af154fce`  
		Last Modified: Thu, 08 Jan 2026 13:26:32 GMT  
		Size: 144.0 MB (143989669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ec5ee6c36d39a092b42a2404e0ff2d0be5a011c5375dee69a438810babd7ff`  
		Last Modified: Sat, 08 Nov 2025 17:58:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516d242d85cf4b1ae63ad8864fc9011bdb48d48c8ceed0dd06e411d9fc983743`  
		Last Modified: Wed, 07 Jan 2026 20:08:08 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8106605ddcf488bbb8b82e6d076f0d312691e2ff4712694e670123708f0a4f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c177f08c5aac3a4c85be8caecaf53ddb565208dc0902c82157c6fda90fcebf`

```dockerfile
```

-	Layers:
	-	`sha256:c74cd9b18f9c89eff3a160c0472029846da09afd7afc8d5ef7c0f0bc924b5954`  
		Last Modified: Fri, 16 Jan 2026 18:48:15 GMT  
		Size: 1.1 MB (1069547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3ffe7a12fe3e91d925679a2e6af06229cd08d85ca08b25f73cc5325503833a`  
		Last Modified: Sat, 08 Nov 2025 17:58:24 GMT  
		Size: 19.6 KB (19621 bytes)  
		MIME: application/vnd.in-toto+json
