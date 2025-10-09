## `eclipse-temurin:8-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:7d7466d79bb34acf2a3f4721c58954d4d31cf99317dd173819de98ff6a4898a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:83e429ba32f69566a43169347390157be5cd9867a9b76fcec929d56c4bfffc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61646033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7544ebd829c26bdd98b59ef9f225b9ec85f50f852ed19a26b23af1df7569adbd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='fb10b6185c76cb48bdcbb76e466adc319b37ffc0b1cf89708a1f13e94adcc12c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4512b1690d5e061c5da51dd24b31a4d3bf934cb381adc713b1104ffb777758`  
		Last Modified: Wed, 08 Oct 2025 23:02:06 GMT  
		Size: 16.2 MB (16174547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f5c19e5615344d787b4dff7b2f4ccb4ba61c1325fc883a9ada4e753831fec4`  
		Last Modified: Wed, 08 Oct 2025 23:02:11 GMT  
		Size: 41.8 MB (41826511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f60edd2122bcec926af61f2ac2a623248f150cf8fc5de6bcc1c0537c963657`  
		Last Modified: Wed, 08 Oct 2025 23:02:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014e6af7dc1e371bef31eea964bea7f81db235392ede078588e28f845a889560`  
		Last Modified: Wed, 08 Oct 2025 23:02:02 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9b73e397e5442e3f5e9ad156d90eca3fb1a0f9f152a967ff2e471560e9d2a722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.1 KB (945077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e5dbbe16ba61677bea32b7f863482685a93b9d9330c5d720aca0e7be67836f`

```dockerfile
```

-	Layers:
	-	`sha256:42006d34b2a0ad27c7101e7c82b00276b3034c46c55191c4c3af41bb72fb4c7b`  
		Last Modified: Thu, 09 Oct 2025 00:18:57 GMT  
		Size: 926.8 KB (926847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9ced3516cdf73612e8c7ed588fd24929bc63205aa6242f7184dc36c8721d07`  
		Last Modified: Thu, 09 Oct 2025 00:18:57 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json
