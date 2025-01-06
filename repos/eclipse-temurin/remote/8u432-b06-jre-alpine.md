## `eclipse-temurin:8u432-b06-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:51b833beb63a4c7cc0af7aa5e21835174e26cdc6181fc12d89f96d8fa1c0c7bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u432-b06-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2a7b9380b99f8b6c6fd68dc1109a0cc3d3e06ca3c32d8e19ffbe0fae6d697c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63752368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c4cf392388c50fea0c793bffd08074dfc3b316c158a3b5fcb33679a2df71e5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7f7c265560dd5a42533bf282831d7d2f044a7ff7f4c310b40a0f9f8e19ff12e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4b7c30c1820c9c133a832f0a8d49c8ec80a0fae0e14f43a5ad689e0e015515`  
		Last Modified: Tue, 12 Nov 2024 02:38:45 GMT  
		Size: 18.3 MB (18307390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84baf871b60da2f118b5b82fb1fe0faee3207d3d4cdd6edc25a6b015a0522e0`  
		Last Modified: Tue, 12 Nov 2024 02:38:45 GMT  
		Size: 41.8 MB (41818665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fc6149f44e718c04f6bb6aa5194fe0f7a18b5abbc3abb3d792c8783c4108fe`  
		Last Modified: Tue, 12 Nov 2024 02:38:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4a770be924db61c88b2e37b8a011e0cdbc63d1fec513f642617c213e5d3d85`  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u432-b06-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9dfda478929be42d631c9d3eab8d3584c97d5a47d5313073c0d4e91ee33d6c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **932.9 KB (932913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c584373fa3de986195391d5eb012d133db28fdb99d33bd844614ed0abc382e`

```dockerfile
```

-	Layers:
	-	`sha256:7f5a2993e2b454fe2d433b173fad2b0808ea6251f4a85cd0e75b463d7d614b40`  
		Size: 914.7 KB (914662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a85affdc63125bfadadac1184249b25e2f28b8ba76288b4f8227526e13c8b72`  
		Last Modified: Tue, 12 Nov 2024 02:38:44 GMT  
		Size: 18.3 KB (18251 bytes)  
		MIME: application/vnd.in-toto+json
