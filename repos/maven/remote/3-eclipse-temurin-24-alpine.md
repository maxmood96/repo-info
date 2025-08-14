## `maven:3-eclipse-temurin-24-alpine`

```console
$ docker pull maven@sha256:27969ecafc955610b5fb7b977f5b1472818d8e865d0f6b38cd179bab987dc1ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-24-alpine` - linux; amd64

```console
$ docker pull maven@sha256:e8dcbd95b2f8dde2588eb40bd810c27ffe47436f378093648155869c080d74a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127699286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f67eae9f5a49f944f6cf09ede82446f8b905e981122e9916e219c52c40072b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Jul 2025 06:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["jshell"]
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5ef2386be4a27ea92a01ef0263a3104d9355ac7f4fb22aa55e2a91eeee344e`  
		Last Modified: Mon, 04 Aug 2025 20:12:09 GMT  
		Size: 21.1 MB (21104348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eae701b9ed8b56a4df38c4ec9b72d1f048c6055ba56cff62e61db3768256810`  
		Last Modified: Mon, 04 Aug 2025 20:12:16 GMT  
		Size: 90.1 MB (90132918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939aba76ded566210b691bda00b92ffc2029071fc4984207e3c7d6dce00328d6`  
		Last Modified: Mon, 04 Aug 2025 19:25:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907d1c29ddd75894bbcf074eab7ed68afbe4634ea810f2cf54368a7eec0eb6bc`  
		Last Modified: Mon, 04 Aug 2025 19:25:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9ed8f520a5ddb73c9f42765604b95ed7b149fdb0f3ea32adca995591c61cc5`  
		Last Modified: Tue, 12 Aug 2025 18:08:54 GMT  
		Size: 3.4 MB (3416291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9116f724e4a5d5adb433d6ac7afceb9043871405e9cf86ce0bb95707b8194ca`  
		Last Modified: Tue, 12 Aug 2025 18:08:55 GMT  
		Size: 9.2 MB (9242583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b76ef49f5756930f305835c14ad984ce30f484884d0bdef2d1c73e2284277ac`  
		Last Modified: Tue, 12 Aug 2025 18:08:54 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22fc11e1305b98c8adc68114c223b6119166336b4394b02c560343bd50af7f9`  
		Last Modified: Tue, 12 Aug 2025 18:08:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:73787089cc518c5b828b4d4fac9ef1f9119d64ea2391e161016734b7dffa9f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1203138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64774cad359df738ba78098b6a6c84e0b8ed83e2e4cb13bf67bf2a8c0b0024a1`

```dockerfile
```

-	Layers:
	-	`sha256:465ac7f93a01785b46dd7c570cd37ea08971b1f5259dd5ca58a9b58fe573d381`  
		Last Modified: Tue, 12 Aug 2025 20:29:58 GMT  
		Size: 1.2 MB (1183754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b156518b7bb7cd5b0a68d78bac5816de1d84d74ff4a9bc6efacd6fac96b978`  
		Last Modified: Tue, 12 Aug 2025 20:29:59 GMT  
		Size: 19.4 KB (19384 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-24-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:13b0c112176f942c739c2316bac722cef2ef183f0f49ffa460f4ccb363e829d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127118615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a12d35c1ed20c1163170745b4edc7072cbc0cd440f128b98da5fe968c05a2b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Jul 2025 06:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["jshell"]
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a495748323e0cdac275f94a75856b53137d10e7dd79d59568fe601407fb00e`  
		Last Modified: Mon, 04 Aug 2025 19:31:51 GMT  
		Size: 21.1 MB (21148725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f503b83c17e606e525a15bdf8c088d8b510866bd192730491923c7e09021b161`  
		Last Modified: Mon, 04 Aug 2025 19:39:38 GMT  
		Size: 89.1 MB (89116820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e121434e3e7ced93721c74730970c4545f0d07a1ab8a3cb707d8d97621657a`  
		Last Modified: Mon, 04 Aug 2025 19:39:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94585305800850d7db8da0cf8b919141fa5eb89e43d0bf4133469159f0960634`  
		Last Modified: Mon, 04 Aug 2025 19:39:33 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025f5b025da0e64221b623a19a7eb889fe53606af55aa44fe3e17dcdd6e1ca3c`  
		Last Modified: Tue, 05 Aug 2025 11:44:04 GMT  
		Size: 3.5 MB (3476279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cd13e95ddc208e61d58adb55521fef5f613a0c50f29f81527b27eb61347394`  
		Last Modified: Tue, 05 Aug 2025 11:44:05 GMT  
		Size: 9.2 MB (9242590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccdc2c487af5525e8d8766a62289e79d15d08412a1a247c3d1f2aa662ea3a95`  
		Last Modified: Tue, 05 Aug 2025 11:44:03 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e8575900269a440efa1f92fcdd86adc8a229e0a26c3a1c3822ecbb9877da00`  
		Last Modified: Tue, 05 Aug 2025 11:44:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:4e82973597ae59fa0a940d5bc8ac54e9c0f69c5ef11a018037a0a613f025f5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1353270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407db134e5185b8f682cdaf1d8a87d21bc150f6d42d137c27652e93cea9de6b7`

```dockerfile
```

-	Layers:
	-	`sha256:90105738e6eddfadfc760e971d0914da883d77374919e061497b66106b5e4df9`  
		Last Modified: Wed, 13 Aug 2025 20:29:06 GMT  
		Size: 1.3 MB (1333753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72384f785dd680c4cb01f56800a92aa3a8d49981f0c8c5a08fdf6cff7a62e2cd`  
		Last Modified: Wed, 13 Aug 2025 20:29:07 GMT  
		Size: 19.5 KB (19517 bytes)  
		MIME: application/vnd.in-toto+json
