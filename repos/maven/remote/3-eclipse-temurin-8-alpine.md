## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:a177fbea9e37292bebe966541b816057964ff335844fe6bc02eef3a346e55a48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:d2f221ad2e05dc624b2afe3995ecd075a5e0c5dd7bc98cb912e2a71fa13b3138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136344443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbe9ea1c382b098bd3fd0a2afcd6af5b330de183f1a9448fb372982a4913c79`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='86071bc98901cae80c62745a64bb4486212985fe5b66b5aec36ce92e8a036a9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c838c9d71fbfa07585d45b8debfc5b680d9c8787ba580e1cd4e57c8a2d59e9f`  
		Last Modified: Tue, 12 Nov 2024 02:38:35 GMT  
		Size: 18.3 MB (18307453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a88318cbb807e0023c7ca8136f7b07514eb50f094bdba21159f3218f2d48c`  
		Last Modified: Tue, 12 Nov 2024 02:38:36 GMT  
		Size: 101.5 MB (101542486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee6ed989cd330cf39adf75bb5b9c82cd4c0fafbbf4244ae1e70127d75c88a09`  
		Last Modified: Tue, 12 Nov 2024 02:38:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bbc39eb27a46a707a33836de54b2b0542935fe61e33dcfa239431e794172e4`  
		Last Modified: Tue, 12 Nov 2024 02:38:34 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a45d874b4c284ee3ceb002e2061a5011577e7ec51cf8acd52e029fff1f9a74`  
		Last Modified: Tue, 03 Dec 2024 04:33:05 GMT  
		Size: 3.7 MB (3696687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1f3f4501216d7c19b50ddf9167dc1d141c506884b717d248e98d9cb3be4f85`  
		Last Modified: Tue, 03 Dec 2024 04:33:04 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dc3c82fec260d5a93134fd7eb7f2f750343377b1b25523543803aeee1c5891`  
		Last Modified: Tue, 03 Dec 2024 04:33:04 GMT  
		Size: 861.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f365ebff45705b2b6f80fa7ff1ebb17a2b666c99a7b1e639f47e2671e64cdc`  
		Last Modified: Tue, 03 Dec 2024 04:33:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:09944e05f2888a2dab9dfa5d126659bab1860feb49cd78316e77896f426896b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1240605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b12728320063f320ecdda3adcc546dfcf7c7647d69aae533f2750acce57748d`

```dockerfile
```

-	Layers:
	-	`sha256:c7c309eed4539cb92ca41199cba32def15699bf174c22e070db9e7df16bd7248`  
		Last Modified: Tue, 03 Dec 2024 04:33:04 GMT  
		Size: 1.2 MB (1221237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4bbd5fac6784e513d4be5882529d19d5c09cbb91d0f3b6e7d4d3968142f9cbd`  
		Last Modified: Tue, 03 Dec 2024 04:33:04 GMT  
		Size: 19.4 KB (19368 bytes)  
		MIME: application/vnd.in-toto+json
