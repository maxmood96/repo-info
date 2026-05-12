## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:a62695d5f0b7db3c1c4ce8ea8a12001b3a1d18abb837f1e111326aa7864a434d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2360b1cfd7b81458214e9d0209d17665e596fbe34e515f93a75774fe5071d34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62993263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fe2066dfe98eee4ea955236fac5a5fc28d94f69e848395ec0b30c82083027`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:25:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 12 May 2026 21:25:27 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='82b74dc9042ce6735624a1ca9585e6a43c44f0f6093a7f2088b0a622f304d62c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 21:25:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776749de15cd34aec65aefc69f6fd7bf89310f5e68eba07206963775f4f632e0`  
		Last Modified: Tue, 12 May 2026 21:25:42 GMT  
		Size: 16.9 MB (16857135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d038b7b5b167a3e7569b5e96b52bb6bbf4924ee6208b875e43b255587ee39ee`  
		Last Modified: Tue, 12 May 2026 21:25:43 GMT  
		Size: 42.3 MB (42269351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070cab8a0446f6d8c9d1075928509b6164b4c48e727b5ba48bda493142ae988c`  
		Last Modified: Tue, 12 May 2026 21:25:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c24c35f3a8c1056186d6afb9159614d3ed90a970aa88d1e5c8b7193c56211b6`  
		Last Modified: Tue, 12 May 2026 21:25:41 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cc39bed3a3e6fe490abc20d328f7e22bb8e494c761e939c04cf925723bad915d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.2 KB (952220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6732723872d41a33e680500871e24fdbb7403772e13851db1ccc7f0615b8bdfd`

```dockerfile
```

-	Layers:
	-	`sha256:ff22ed66e0a424fcca6f1f5cd18f1e1576f2a0da538f7348d8cb053d33731ad0`  
		Last Modified: Tue, 12 May 2026 21:25:42 GMT  
		Size: 933.4 KB (933361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e74af3781ddf188d0f43b973b6c549dcf8055546b429c6647a7c502214a26584`  
		Last Modified: Tue, 12 May 2026 21:25:41 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.in-toto+json
