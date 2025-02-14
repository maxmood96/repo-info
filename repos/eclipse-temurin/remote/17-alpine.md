## `eclipse-temurin:17-alpine`

```console
$ docker pull eclipse-temurin@sha256:b16e661d76d3af0d226d0585063dbcafe7fb8a4ef31cfcaaec71d39c41269420
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9d8e2d4ff09a8b2beaa423b51814a3779469a5322208bfe6b6c4e86414576153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168310838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e074d8dc1a714d59cb1ef988b8bc46cf3da3643ec18c87d44589a751d62297`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='259c85e16f7bbfdfb3e0a2ec1c5d6e2063300d413422286583265a9d8a882358';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005dedaf12fb87fde98fc3799c94d82baad509672097fa595795ade7db4dbb8f`  
		Last Modified: Fri, 14 Feb 2025 20:34:17 GMT  
		Size: 20.9 MB (20949824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b93bccf647f23c56b988b134e0f24ce8aed01ba9162e974330b45abc9f2b21`  
		Last Modified: Fri, 14 Feb 2025 20:34:29 GMT  
		Size: 143.7 MB (143716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c444d2c2cdf16cd81d9bded68ea50c3e23f3bdfb487b1e8eee9d03a206c05142`  
		Last Modified: Fri, 14 Feb 2025 20:34:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c67efadec52153c3e21caad3dc817dc99704b643bec8d9324830842d5d29b6`  
		Last Modified: Fri, 14 Feb 2025 20:34:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:59b8744ee508fd8dee9af85bff80da19d6dcca60003a2ed6f08fea8b8ed9532f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1117091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71d2427bfe18facacf1c1a7c37276b184ea1a4b728d9bc82b28426f6a128964`

```dockerfile
```

-	Layers:
	-	`sha256:f7a9e3382c578b1c896aba7784ccb0d8e8582474bc747f9583e564fe0ec7cfa9`  
		Last Modified: Fri, 14 Feb 2025 22:13:16 GMT  
		Size: 1.1 MB (1096441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b797676b546a5ab9508d910c8bce9d8e80559252470466c1beb3e40470f772`  
		Last Modified: Fri, 14 Feb 2025 22:13:16 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json
