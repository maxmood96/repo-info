## `eclipse-temurin:26-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:c4a22bec4f4368636abb9b6fe2b2350fd7fae1ec0d3bf43fcaae1be720c3bbd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:26-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d73556b008b2a7c9d24cc9d8407d9b4df99c0f1e39aa2bba5ff1ca60db1dd1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77018080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d54258a27d017a1e8664bdd3afc0d6a0dff1430fa958856cac9a7f1ad23531`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:49 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:49 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 22 Jun 2026 19:57:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='3106f091aad558977d890b0f6639beacd2815ea051a75a23733b3b16fee6ca55';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='d218b359f735122cadeb9cbb226c4ddff8746c46a8d5b833809aedff85bd48a6';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:57:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72cfb9f33e585f6eab0277cb695cc78dc8b0ae8b6cc7d30c159ad966a4884c4`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 9.4 MB (9394450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ad146414baf7af2fbb4875a95795a0c8631d5e682541e4d193e307ebacd18f`  
		Last Modified: Mon, 22 Jun 2026 19:58:08 GMT  
		Size: 63.8 MB (63776618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb8a5603b582710f22a8c77f726c3adbb110ee1926e000bdba6b919885db69`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f794e94355907e9d4c3b9ac7bf794fdcc22add314a4fcd8d3c9ee0e9afed5a2`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1e2144fd40ddeee9814bb3b511a817281a7b243656e6c9620f45f2117f8ca2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **802.7 KB (802724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a53445ef5bba04a13d44b4b7c3bd9ac311565c487d4c28b6b884d3931e9152`

```dockerfile
```

-	Layers:
	-	`sha256:2e4ce0bf7de89a3b40b5f93cf3a0b76be5a952094858bb47b30ab7f1d3697593`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 782.9 KB (782931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf698f9a715da063f044e3725d3b298437cbf94317fa815f7209d403168a03f4`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 19.8 KB (19793 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:f1330062e83fbc1a7fb7d0ce5a4296616d2d974e8348a74a4f222116a32b54e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76266119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0661e59e443a328a394f3f6fb04b8f25dcd1ff610ea419dc3a78b63440412e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:58:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:58:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:58:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:58:36 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:58:36 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 22 Jun 2026 19:58:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='3106f091aad558977d890b0f6639beacd2815ea051a75a23733b3b16fee6ca55';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='d218b359f735122cadeb9cbb226c4ddff8746c46a8d5b833809aedff85bd48a6';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:58:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6504315607ebc3a6ba768ca11b16aebc961edf16510dff34d2dc4dfcdb254e`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 9.4 MB (9424357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8568e08d213ee16bc37e79a7fa06a6f76352eef4794547168e465ab3840b7f`  
		Last Modified: Mon, 22 Jun 2026 19:58:56 GMT  
		Size: 62.7 MB (62657314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0c16a8977a031a2e361c818a8f60c65436f30f960fcb6ac328acb74bbc17b`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc11d0ce0b8621a6767402b1deb3e7b0a65fa7b6dddcad54bd3a64fc7246d7ec`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:19b3a8d3e56c81a083f7de6aeec9065fe5799c522b24eb4fcef176c9f1eda5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **801.6 KB (801642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ebf49da0b6d3db0f672bf1980bebb7064a2907d1fefe5adcea0e33204c22a4`

```dockerfile
```

-	Layers:
	-	`sha256:9686fb7bf469661449b4d696ea70596179abc5662231700d2523b7ef54727d22`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 781.7 KB (781716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f20e78cfe7f0dd6b475fba128a7352f76aae874110fc9363c21593330c7552c`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 19.9 KB (19926 bytes)  
		MIME: application/vnd.in-toto+json
