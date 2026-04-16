## `eclipse-temurin:21-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:bcc7ec7e8fef937ba9f01ee5f810361d722c6b5dbe19ac188ab7b25c1a4dd2c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d702e2d534819da0573af42ee880bfddf6f3497b9e7a3a9f5288a127b231b619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183301377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b34f4018688a3fea68c7f2a7ad840c90203fa6f1fd1b301f6abd247c56a099`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:52 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ef2c34364d42e41eb14af65c85cfcd9ba8407f18b51bde4f6428bff92388a2`  
		Last Modified: Wed, 15 Apr 2026 20:34:17 GMT  
		Size: 21.3 MB (21315853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136a888652a1277373c20061d1c0d79e332ba8eece5ba04c0c24fce61ce8940d`  
		Last Modified: Wed, 15 Apr 2026 20:34:20 GMT  
		Size: 158.1 MB (158118925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b440bedad35bcaf95f5c16474e5bcdc67677eca1377bc3b6bd9a64aa13552d0`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c1bb0b54884876ce179c9ad3683a68d7689b97597df8b1b2dfeeaaf5e7b60e`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:718c911b8968dca54a6786401e32fe41cb2c4333cbf655c971cd848a1fe805ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1128902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16769bde4d42c730f0b353414203364345bdf1d8176114301e1ae16c338a3fbd`

```dockerfile
```

-	Layers:
	-	`sha256:76ab5f6c9afe4742887ec52dcb0c151f52c7d07d863bcce4ca0cf264dabd95de`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 1.1 MB (1107486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b853497a8a7f60ca8e579cd89d56169d9ab3036988a0d96d9231bbb728f14967`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 21.4 KB (21416 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-alpine-3.23` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7b49ac35fd33ae41870941b9e14ad62076bc9fae665da65527f2d060daf348dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181635681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916a23b3d1524acff441ade33e2b0d5a261dad5d898405c09e5ff002057e81c7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:55 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaacc5fcb81aaf4c24ca62b7c7d748d4925abc4199e39981b80b93898777d06`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 21.3 MB (21303504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea8e162f72eb44c19a73f38e10d121143bdee45dc7426f76cb9f2b16ab73763`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 156.1 MB (156129898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37767c9371d4e03127e4bbe85929010c025d7d442785d1805b213575c0a75fd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12d0e0cbded327c9df870505ef20a84efb14dd8ccbe2a48a63e4120f61b65ba`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2a52d87efcea147a30d34b557c279ec5e7b6bdac0c0442e5c85aa2868501e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22416a9c77dc88272b9c2f8eec06fea0f5add3c16f1131eaa0b9194490478af1`

```dockerfile
```

-	Layers:
	-	`sha256:fc1d17eb4701ac81f4c96311546a581447669569726e7d2d7083374d07f59d37`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 1.3 MB (1256874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17c71d047379195fe3e856220286c59e2e8a1f71449d72e65b1341dd8c6e93b8`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 21.6 KB (21576 bytes)  
		MIME: application/vnd.in-toto+json
