## `eclipse-temurin:8-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:c426fdd751581bf7481e7eefac3b2f850dd8f4246394dde4f9dd3d30114f88b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:add1cf5601b3c28a30b454d62c526304f9414999f4cd933ac3d132d0e07912ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121164397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b9c72b63f04a6939f2a23cd61ca7dbe78e5dbff19923d6a3381e2a39592f17`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='86071bc98901cae80c62745a64bb4486212985fe5b66b5aec36ce92e8a036a9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe6dfd5a5e2f33448ac26d2a57c3f54ae2ccdf4daf44580748feb134ca9d018`  
		Last Modified: Tue, 07 Jan 2025 03:31:21 GMT  
		Size: 16.0 MB (16005492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89412a9591e0dd26815b7ea9db5a452352dd76998189f07abb56d784b1e1b1a5`  
		Last Modified: Tue, 07 Jan 2025 03:31:23 GMT  
		Size: 101.5 MB (101542475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4233d01232ab4d34c864cd6b3c052e216dd74eb06d21e79ce4dda95a8fe2cfd`  
		Last Modified: Tue, 07 Jan 2025 03:31:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f230d3f854701990cfaac714a5e83e61caeca6cc0efdab1d522bf78d0954d7e`  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:03a18e0189526854209301f3f890364c7df74f1c63c11ecd06a3513ef932279f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71718fc90f9fcf31b2b9a686f81f70e251d578022e6f8721ca483660ee8b3715`

```dockerfile
```

-	Layers:
	-	`sha256:8c330a7e361d2ee248f362d277fb9cda71e9aa23641b89a08ebfe1ceef733bdf`  
		Last Modified: Tue, 07 Jan 2025 03:31:20 GMT  
		Size: 1.1 MB (1083368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71004f7c962def573ccac2e3b6ceae882bcf5ff290523c2aad831bbc6b3d74d2`  
		Last Modified: Tue, 07 Jan 2025 03:31:20 GMT  
		Size: 18.7 KB (18719 bytes)  
		MIME: application/vnd.in-toto+json
