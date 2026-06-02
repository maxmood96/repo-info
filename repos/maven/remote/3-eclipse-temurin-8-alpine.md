## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:ccfc18ca41d1213d3a77459473dd79bba7949339476ca6c3bcef55f11a8ded2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:667db1b9bfef10efe3ad8c20c51bba5f39f3d82b464fc0964fc0bd89c78dd9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86673660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c48ef6c857e4aad5511cb36f6038f6d393cf32e6433183ae8eb7a3edd015bf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:54 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 12 May 2026 21:24:54 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:24:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='5db39d393a0c3c5c8bb0c639e6f74edc474a13c84d3caf33dc9ba3bba0097a49';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 21:24:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:24:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:24:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:22:14 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 02 Jun 2026 10:22:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:22:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:22:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:22:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:22:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:22:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:22:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:22:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:22:14 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:22:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:22:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:22:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da768393bd1fd01f1eb6c504dff19511d9e30c336b824982cfaa816d7ae3bdc4`  
		Last Modified: Tue, 12 May 2026 21:25:09 GMT  
		Size: 16.9 MB (16857066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805e08e2635133b31c002e70773f34ca1d11e644912952dedd445645df358cbe`  
		Last Modified: Tue, 12 May 2026 21:25:10 GMT  
		Size: 53.1 MB (53080117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058485af113ceb7c1eb1d8ad0c051356cb888365a4b326efbc1f02420996a473`  
		Last Modified: Tue, 12 May 2026 21:25:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da3b2c25d4119dc7bdb3820a5b39c43fedfd01438b0158496000c4fe4625c1e`  
		Last Modified: Tue, 12 May 2026 21:25:09 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2003c5fe3322bb4cdddd4cd810c086e3b7006c99dc3627228490f354f80952da`  
		Last Modified: Tue, 02 Jun 2026 10:22:22 GMT  
		Size: 3.5 MB (3508708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d453cee8155d58c69addccb4b77410a6cb043dd8b9e48b9ff6cb0ffd0d9d5`  
		Last Modified: Tue, 02 Jun 2026 10:22:23 GMT  
		Size: 9.4 MB (9359958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc8bbcc0aa9fffb68af30cb25b3619a3043f57285f7cb566990af9d6f10e9e5`  
		Last Modified: Tue, 02 Jun 2026 10:22:22 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eec3c7e36ce252016bcbd0ebb1b34364b26b00ba88eb865e64a3e883db9f5a`  
		Last Modified: Tue, 02 Jun 2026 10:22:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:0b17a86e3de4f3db81fc73b022a5d5c7c2bee9ef1b1c2ca64667e9cb708a458a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a76d60a8068d1d43bd776af10566a6d1a97fedb1722ee646bcb45dfbd92393`

```dockerfile
```

-	Layers:
	-	`sha256:f4c6cfbfbe0d6f3b8769026d5c76d728d3a490b1d3158ef66aca75f2b0eba15f`  
		Last Modified: Tue, 02 Jun 2026 10:22:22 GMT  
		Size: 1.2 MB (1242620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f179c8c70e5355a6b625b2d7a8f9b2cf8349e6771ba4f3fcbc1966046ae151bd`  
		Last Modified: Tue, 02 Jun 2026 10:22:22 GMT  
		Size: 17.0 KB (17022 bytes)  
		MIME: application/vnd.in-toto+json
