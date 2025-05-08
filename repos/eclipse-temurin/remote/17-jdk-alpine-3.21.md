## `eclipse-temurin:17-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:ca5c0c9763d21cf1617cb68ef8c17228a202cd0358fa6d7510a1bbdbd49c74da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:18eb1389a1ed728d4eb6363d1c4458e4b10e5c523bebba1d2b018053132f808d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168371863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c32894dd61d34748aaa9fe970f82bd752258b3fea978d346af95fd7c16bfa4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c596f5c627f84cd801bd7a443cd0743304a6aabb7397e0fdbfad16a9517f7f98';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994661c98e4264bf53af5a49e1f142717665bd41915c9244d1f63dad7897149f`  
		Last Modified: Thu, 08 May 2025 17:04:54 GMT  
		Size: 21.0 MB (20951329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fac3e9314ebcc28feb6049f712a878479f900bc5f70456ecc2fc2fa3695d30`  
		Last Modified: Thu, 08 May 2025 17:05:08 GMT  
		Size: 143.8 MB (143775879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b9ea538182f9ba83b0f571df811bbc4de7f25b42ee9eb9733ce9d5851970f`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea44d309ec90a992e100ebb714b75633eea050267a3070b3db27c666fae34be2`  
		Last Modified: Thu, 08 May 2025 17:04:52 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ed9b21658f06055356ccec4e16eb1535248c6483b7259b245753fd01602d03f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1117713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d17d85e2e30cbac7dcca94fae201fbe82382bd9d05350fe6cefcdbe64acaf1`

```dockerfile
```

-	Layers:
	-	`sha256:16cb6b55d5fadf8c0d2adf5f925be8a63da86a2910ec400438d9268646da09ff`  
		Last Modified: Wed, 23 Apr 2025 16:31:42 GMT  
		Size: 1.1 MB (1097063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180b05312f1bffbc23bebfce8b23b4e165e6a31e75d7a28602e9798c95ed6b6c`  
		Last Modified: Wed, 23 Apr 2025 16:31:42 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json
