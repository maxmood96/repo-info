## `eclipse-temurin:24-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:41e9656f86cd335f0f30d63291adb1128e7a3c071a8a19b0c14638ca70317827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:24-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5d26953821d89647d356e1b2547ffcefc270db28b1fa7bb1605b6a7259a3a651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c786e0e0f7290503848a3d5a54e13e646459200df7f75627b0f1277402219d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='389100187cf328c7b6b6b390fc0f5071ab38e93e8a6c06beb11e59363d2fd0d0';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='b63b888d2415828168c4d35a62d88f385a5532a20b7391e30a5d5d0a9a73b892';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070d4c581807e3a28a5ac94aafb7b95332ad446867ea5cee7e94810b42d29010`  
		Last Modified: Mon, 04 Aug 2025 21:39:45 GMT  
		Size: 16.2 MB (16162870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65de10b9c1ab463b820f7ba548c73c7f198bf6b548805289931c69cc7b785032`  
		Last Modified: Mon, 04 Aug 2025 21:39:47 GMT  
		Size: 61.1 MB (61053847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ccc84b20da1cb028b74533c83dda213181992a026bdf0b51cb37ca4a49b357`  
		Last Modified: Mon, 04 Aug 2025 21:39:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98824a67d305d19102a22819b5e28bbfc7861bd13514a3c6fef67889ec77e`  
		Last Modified: Mon, 04 Aug 2025 19:57:09 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:30d809228e386eef234b9fab6de8637e1bdda163367188ea995af1d0002e5c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.4 KB (921390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9681125c29618ce39f2b7386e5898cdcb3e40e1e629d367b4056d8682414589d`

```dockerfile
```

-	Layers:
	-	`sha256:08955c562f2810b0e2e62ef2d70f9c8b3e3151ea65072650654911fcdf8c84ad`  
		Last Modified: Mon, 04 Aug 2025 21:26:03 GMT  
		Size: 902.3 KB (902322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cec1f9ee25985fe20a170cf35bac8c6bcf79798ae3cbb9bc2c375e1d305e14`  
		Last Modified: Mon, 04 Aug 2025 21:26:04 GMT  
		Size: 19.1 KB (19068 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:aa3f8580c00c9e2c63257040f15521d3ef00ee7a8b5594e7a6fe68f0f93296ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80169079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6240273769081cf21b6ba9905e82855d6ac7080110dfb9c049a14b368ee11e93`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='389100187cf328c7b6b6b390fc0f5071ab38e93e8a6c06beb11e59363d2fd0d0';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='b63b888d2415828168c4d35a62d88f385a5532a20b7391e30a5d5d0a9a73b892';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe7a243e393b0e786543dd9f5baddfc1b85c7bef5e769f84ae7021986cd2b05`  
		Last Modified: Mon, 04 Aug 2025 19:35:25 GMT  
		Size: 16.1 MB (16135229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0ea66623ff8fd153881444ea3419314ad932c14bee87511a8cbc960db941d9`  
		Last Modified: Mon, 04 Aug 2025 19:42:25 GMT  
		Size: 60.0 MB (60044506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2a96ae60edcaeb52836e6367cf769746afc458ddc07d363c5967e53d5e5c16`  
		Last Modified: Mon, 04 Aug 2025 19:42:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34753dc6c669f76d6fb8b5463fe038c66fb4fcdc11c131cfdf8b35a6e0c73d2`  
		Last Modified: Mon, 04 Aug 2025 19:42:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ad91c7928bf6ff379074ea6dc793a4323c7600f90fbb4de706a22e305075c17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.9 KB (920911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffb7dab722671e85bf8479d1533c39b428cda7fece584ffca8001451599b238`

```dockerfile
```

-	Layers:
	-	`sha256:f4e4f3f9cd6a4fe66e558a9c6ae9f337d8d755947e8f10e05ed0691cbf64c3d6`  
		Last Modified: Mon, 04 Aug 2025 21:26:08 GMT  
		Size: 901.7 KB (901733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7254736938456e91f7e18a472e13667a5933c2707c0f6e5e0562ea618702168b`  
		Last Modified: Mon, 04 Aug 2025 21:26:08 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json
