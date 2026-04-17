## `eclipse-temurin:8u482-b08-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:ef50c3eca0b3091a5aa19e4629793e7fd892a8eba05adc9a1bf4983a859c792f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:16be9a6a4153a98eb31806467c448ae1383958017c5758ab98107d16e2d379f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62104386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffd84fa5a46723803c2303371af86c5246490a0bc5ba7288e37ffbd48f1a97f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:23:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:23:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:23:47 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:23:47 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Fri, 17 Apr 2026 00:23:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c1b64ab1d2c96ac0fd89c60377396cc4457f954ee7ce931f3a0e547f701e6595';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 17 Apr 2026 00:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:23:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f52e3c58746f4d68fdefe19c2892e592a4e4dcbe641197726bac0024ceef1`  
		Last Modified: Fri, 17 Apr 2026 00:23:59 GMT  
		Size: 16.2 MB (16198619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b737f2b70650358adaa5cedf1f0004ba07227529afab5ec5f6ac9e81dfe159`  
		Last Modified: Fri, 17 Apr 2026 00:24:00 GMT  
		Size: 42.3 MB (42256485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5b5ceffed5b5092f1827dbf0bf30d509a3d76ac588a845f6ec38674bd33337`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a672ed9405ecd3d4c26cb2f0a08ee28aeb1dde15de2a20053d5d718a903360ee`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6abbcd9ba8f773871a958b6b813865e3b32469f4789b466476f9cca48f50f56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (944986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618078d902d050d2496fa43ab91b579b37ebab3ffd544b6d7e7d3be89395a236`

```dockerfile
```

-	Layers:
	-	`sha256:66b7cbc95638249188c44acdd42fbfa54ecba8497e88d5d5fd83ac6702c34152`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 926.8 KB (926799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688be359f9313ad8e19f241579877ddcb4fd319436624352a9552bc585ca18d0`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
