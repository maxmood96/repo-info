## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:c9df0ce31c44db2139b282477e844cd5a66db1e3f8c9747976fdae23055cec07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:911434de702af625625e392cea8f26fd194870577083ab8d9bf89945db0461ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85848482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a383a652666132c2e657a9ffa5401066a94c3f766c358420d7e3f6d97688261b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:52:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:52:59 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 08 Nov 2025 17:53:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Dec 2025 20:06:53 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 17 Dec 2025 20:06:54 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:06:54 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:06:54 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:06:54 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:06:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:06:54 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:06:54 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:06:54 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:06:54 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:06:54 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:06:54 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:06:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:06:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:06:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a0c5ed7112f5699c4ac207aaa6ff3f277cd53844121771dc304877183ab78c`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 16.3 MB (16289673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00e86805e496de548858bb7bc241431402e110f0ee0f8b305ec3fdadfa6d820`  
		Last Modified: Sat, 08 Nov 2025 17:53:32 GMT  
		Size: 52.6 MB (52637485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414a6f189f97323a29e1384a0017627bbd029f10c4f53f4e0a246317953e853`  
		Last Modified: Sat, 08 Nov 2025 17:53:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec39477cf2e25f9f8db348d31ff41dd8cc0c64cb6470887efe494699ba11718`  
		Last Modified: Sat, 08 Nov 2025 17:53:20 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a481c1d3b31ebd80b72aee6eba1da1276a9d8ffcda610fb6699e74862408c149`  
		Last Modified: Wed, 17 Dec 2025 20:07:09 GMT  
		Size: 3.8 MB (3803151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2076121342a9b7fc99644a222a677d3a6288abe79c02b44c603d13c8a8405a6`  
		Last Modified: Wed, 17 Dec 2025 20:07:09 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819979539764763963c24d7a3d7d1ddd93529cb93d0cfb58ecf3fe0f0f02e4c1`  
		Last Modified: Wed, 17 Dec 2025 20:07:08 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b97be67aaca68b268fb60b6f3e25da7d39c6722963b84c32835d4abeccbd87`  
		Last Modified: Wed, 17 Dec 2025 20:07:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:8c34756e5eb01c6bbaf3ff1ffe580e246f7d640abee0b44a51c43d35023a6b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1257702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3674e2557da6a4727b0c9524901d2d625fbdca058f7ebc00af005a9779b8ddc`

```dockerfile
```

-	Layers:
	-	`sha256:fe5f002b3786eac0405b009bf74470628abb9e95d22515d7cf536682ef20ed0b`  
		Last Modified: Wed, 17 Dec 2025 21:32:49 GMT  
		Size: 1.2 MB (1238372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:293104d45d19974b5ed95b03ea6259bdbbdb12c031123b8c6964566e932b1360`  
		Last Modified: Wed, 17 Dec 2025 21:32:49 GMT  
		Size: 19.3 KB (19330 bytes)  
		MIME: application/vnd.in-toto+json
