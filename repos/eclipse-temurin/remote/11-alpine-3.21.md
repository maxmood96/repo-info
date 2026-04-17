## `eclipse-temurin:11-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:46a8b739b4062fb236ff335e8de22b62592517c0eefc71918640f973da9aa4af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:454c8accf751c9261d630cf10d5dca8723ef92bb48274c34361fbfdfea3bc077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160764523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9abff9dd8f57417d3d95874cc2888a5139712d099b791e58e32fc9bcb920090`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:23:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:23:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:23:48 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:23:48 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Fri, 17 Apr 2026 00:23:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 17 Apr 2026 00:23:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:23:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f626a4372544292efce3f2950d918272fff8b720623c969220a89bf94d44f6f6`  
		Last Modified: Fri, 17 Apr 2026 00:24:10 GMT  
		Size: 16.2 MB (16198614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6bfbc5f17c579b1a88f0152a8895e7954660d2ed12d93007033a570c6c0f34`  
		Last Modified: Fri, 17 Apr 2026 00:24:13 GMT  
		Size: 140.9 MB (140916625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d4f2b909ce50a64cf954fd76f444bb461ecc8e724564c0c84a9d97a76f0e7`  
		Last Modified: Fri, 17 Apr 2026 00:24:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a672ed9405ecd3d4c26cb2f0a08ee28aeb1dde15de2a20053d5d718a903360ee`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8dcd71801116a4a84ffa5c132ce67c6785299aa3db7ce2963ff191abfad348ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1019234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9422a99d9565fb56f0dbfd866c62e998813126ab3e70081f31ca3b14a44d4dff`

```dockerfile
```

-	Layers:
	-	`sha256:25e96ffc2eae0677967f7e3ab53a5b58ce1f50e5e2fe3ac379aee6159b85702d`  
		Last Modified: Fri, 17 Apr 2026 00:24:10 GMT  
		Size: 1000.1 KB (1000064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42823630787148fd46d0e40098faee23c90651b2847aea9d6dc34468daaf344`  
		Last Modified: Fri, 17 Apr 2026 00:24:10 GMT  
		Size: 19.2 KB (19170 bytes)  
		MIME: application/vnd.in-toto+json
