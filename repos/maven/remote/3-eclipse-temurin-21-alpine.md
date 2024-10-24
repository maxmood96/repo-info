## `maven:3-eclipse-temurin-21-alpine`

```console
$ docker pull maven@sha256:08dec4e8d04a4440cb22aa04d86a34c76d7cc02f437abf067617328ff1fb598b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:426f1cc6fb5f8b72ccd74ef05e1d233cee5f7ce6d60e8c7edea95315275b037d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196840510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca0bfb7c3b756f48cd62c7ff59f66995db6dc78dc71495c927c8b192d3f82e1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d261c61120750cb19b5bf351e17be8ac00173617f566054bdbd38eec29dffee7`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 23.0 MB (22953305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7043234fe874c842910e4944da3626930f5c7cc4dbd29b50f6a4f907a7d8feaf`  
		Last Modified: Thu, 24 Oct 2024 00:57:11 GMT  
		Size: 157.8 MB (157779374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859106f999588717f76b6609fe5d34f5d2c2fd62e7edbe86c9a8709b1954ba5`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc23d54cb8e8eb85a2d0b34c310691777d93c7b037f48f9063d4eb2bb338ee6`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe39b8f7d4f04b46a0f69c33d3df5f1a6475e8891097760ded1893a5777a6534`  
		Last Modified: Thu, 24 Oct 2024 02:55:31 GMT  
		Size: 3.3 MB (3310139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc912cea676b69651a44c99a83bdc777ffb46790dcecfcee952548d53031840d`  
		Last Modified: Thu, 24 Oct 2024 02:55:31 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da01be2733762047f620794642bd617b1682c0d6c1f5137b0aa03b450b96a78`  
		Last Modified: Thu, 24 Oct 2024 02:55:30 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922c82a8c9429bcd847b7a41a204e4f052cb60f63522c53fe5a7cdb66e1cc9c7`  
		Last Modified: Thu, 24 Oct 2024 02:55:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:0ee903b2c8e8a79e012167e80dd56c1d7303ffb1b756cdd0776f6a3517c4972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1215906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0db8285a464f40c89863a7f5ae882a84a57c33c79c7252131c95a0a67ceff7f`

```dockerfile
```

-	Layers:
	-	`sha256:e2d3148a5f261d9cf787706757eaad586eae52873248802a5dea35db615482ae`  
		Last Modified: Thu, 24 Oct 2024 02:55:30 GMT  
		Size: 1.2 MB (1196523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fce81488a47d4688f5eb4d518f2e4bbd1c178ff3a3284866c95d8c9ec3aebcc4`  
		Last Modified: Thu, 24 Oct 2024 02:55:30 GMT  
		Size: 19.4 KB (19383 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:09aaf2e6eb1ac1c85bec04ffcf697a2b3f552cc0e646fcbc20facae18a56e918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196160232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22820b4f80fcad852866a3209ebe47627a3e048636c8027565d70fa069d794ad`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5ab350b8ff57c75640d387c970dd2282464d9836a98c0f02d04ffe85d3db64`  
		Last Modified: Thu, 24 Oct 2024 01:14:18 GMT  
		Size: 23.7 MB (23731419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106ebdb43fd997ba88f0aac72b687792bf1eb78b471f3d80833b2478939280e5`  
		Last Modified: Thu, 24 Oct 2024 01:14:24 GMT  
		Size: 155.7 MB (155740142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880307f28a09156aa3f74cc0ead3743e36be7611be3e05201b44d035d0c53a8e`  
		Last Modified: Thu, 24 Oct 2024 01:14:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285861aa94b115f54d51eac6aa0cbba4672c4604eb4591b88d706a5874cfdb61`  
		Last Modified: Thu, 24 Oct 2024 01:14:17 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62ac9370e2cc2102a302614e2ba72d33f01e1d2645f09cb77ba38ef9b408276`  
		Last Modified: Thu, 24 Oct 2024 13:02:40 GMT  
		Size: 3.4 MB (3427132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a0bf26e443c2dd66d0ba8b117a74f05f2623af5673ab6b904f1abcae21c63d`  
		Last Modified: Thu, 24 Oct 2024 13:02:40 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd40254923f5244d5bf2543f78dbb4eddd86fb454456c563230ef794778060f4`  
		Last Modified: Thu, 24 Oct 2024 13:02:39 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9109e6aec4adfc144be0fbf679567fbf20d9870eed7c097ed5888d6a9735a759`  
		Last Modified: Thu, 24 Oct 2024 13:02:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:ac1153b01d4ee0b3448472c7580d36e5933420c5544166d5d69cf45dc3670674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1320755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e633b27bebe0f30d3a00290b90f4b87b19e2bdf521b11ece560c4302cb72909`

```dockerfile
```

-	Layers:
	-	`sha256:e0ea9ac6bdac3c51a6fe1365ae069138647cdd832d943a399dd838535112f43a`  
		Last Modified: Thu, 24 Oct 2024 13:02:40 GMT  
		Size: 1.3 MB (1301204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2777541c5906cc0b7bc859a8f7ae1f6b7345475ef341e7a49fa1d907df18604`  
		Last Modified: Thu, 24 Oct 2024 13:02:39 GMT  
		Size: 19.6 KB (19551 bytes)  
		MIME: application/vnd.in-toto+json
