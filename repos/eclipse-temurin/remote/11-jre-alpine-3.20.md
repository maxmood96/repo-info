## `eclipse-temurin:11-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:d1ba577b294ee788111a1840a022932500e3b3ebd7e5232bfc05cd6704fb6eb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:33dd55a6da22f684621a16f1e6cee862cd20b6320d16a37dc43e2cce29dd0ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62867473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1348c68cbc20c95ad8e11563dabc9f78b88c8a1ec4589febae11d8a7d33b74`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:37 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:37 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='a37e818c23e19a0f3f6a77827eac9c6dab572c22efafa6c0e888cce2555d39a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:57:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50b846002bdbb4923230214517072b58d299911f3b8fe6e3f015b1e63293c8e`  
		Last Modified: Thu, 08 Jan 2026 00:08:24 GMT  
		Size: 16.0 MB (16023377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64988317a48057f5c2db48ee041f184ea1efbf62da89ffc32bcfeedde850590`  
		Last Modified: Thu, 08 Jan 2026 00:08:26 GMT  
		Size: 43.2 MB (43214634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8f61d13d016d653e97b234b24291d163d84f8b021b0440e72f0e3145fcab46`  
		Last Modified: Thu, 08 Jan 2026 00:08:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e40f0076b1958bf548d47fb9f41c0d4377b6c8550cf695ee1525582c3ae1765`  
		Last Modified: Thu, 08 Jan 2026 00:08:24 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:80620556302f048026f89185b900dcf5b600d40b9b6c721126d458ad194179a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **918.9 KB (918942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561252355055adbefcf790a37b6096ca8077f6f1898d8b3bec9702ee34f8b740`

```dockerfile
```

-	Layers:
	-	`sha256:7d6558ceab5979eecb8af259dd1afdaafaa7b79748be633f42983f29e5864afb`  
		Last Modified: Fri, 16 Jan 2026 18:56:08 GMT  
		Size: 900.7 KB (900728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3979d449d76b9363274027ab8a5b2ef92f8060fe0a6f819f683f3040b92d9d`  
		Last Modified: Sat, 08 Nov 2025 17:57:50 GMT  
		Size: 18.2 KB (18214 bytes)  
		MIME: application/vnd.in-toto+json
