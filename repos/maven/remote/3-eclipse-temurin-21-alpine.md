## `maven:3-eclipse-temurin-21-alpine`

```console
$ docker pull maven@sha256:a24c967778799ee42665a84d9f94e170ae6dc35788c8d2e218071a086b601768
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:8ace0445701d9586b99bd8db0b913d66ee1b2228594acb68f40e58c4f2ba7167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196207517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a777c6e2c65997f8eb178794e1afcac11baaa23a1324988fc5fa9ffcafa0223`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:52 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:02 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 18:10:11 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 21 Apr 2026 18:10:11 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:10:11 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:10:11 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:10:11 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:10:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:10:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:10:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:10:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:10:11 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:10:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:10:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:10:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ef2c34364d42e41eb14af65c85cfcd9ba8407f18b51bde4f6428bff92388a2`  
		Last Modified: Wed, 15 Apr 2026 20:34:17 GMT  
		Size: 21.3 MB (21315853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136a888652a1277373c20061d1c0d79e332ba8eece5ba04c0c24fce61ce8940d`  
		Last Modified: Wed, 15 Apr 2026 20:34:20 GMT  
		Size: 158.1 MB (158118925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b440bedad35bcaf95f5c16474e5bcdc67677eca1377bc3b6bd9a64aa13552d0`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c1bb0b54884876ce179c9ad3683a68d7689b97597df8b1b2dfeeaaf5e7b60e`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec354788b61a99c7c37615960b02711e51663972618af1a2dedb8c485bc8528b`  
		Last Modified: Tue, 21 Apr 2026 18:10:20 GMT  
		Size: 3.6 MB (3592931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f44712aefe0681a0629fabc4834b6e155c708970f81825aaefeb7530dcca31`  
		Last Modified: Tue, 21 Apr 2026 18:10:20 GMT  
		Size: 9.3 MB (9312197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7ec3b586ad974cc28bf56b5ea046329486240caa5069a0e77c18bf5bb86d83`  
		Last Modified: Tue, 21 Apr 2026 18:10:20 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65428c24d9f296aa01615dbd0ff479e4b18cc65f7616481e782e4cab1832dd0b`  
		Last Modified: Tue, 21 Apr 2026 18:10:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:5c5257813c4ca6de54079cb95b8941377111f629efb4843c0ba7c9107f788b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1261095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56112720d692ad6186099572abe1c265b5202f04e2f8a0a897a2a17fe922c4f9`

```dockerfile
```

-	Layers:
	-	`sha256:a636d4a9e5c9543fba3a0d90e3bd802ba134de15fb4b9a6d10aa981d2adb4d94`  
		Last Modified: Tue, 21 Apr 2026 18:10:20 GMT  
		Size: 1.2 MB (1244052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b32dd973680203b285f44621ae08e535d56c6e09ce33734c339ac5c38dac92`  
		Last Modified: Tue, 21 Apr 2026 18:10:20 GMT  
		Size: 17.0 KB (17043 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:529f1458db3b365da0a72661005cd0557b54f260afb0612a4362db4851b23f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194621105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36172eb7235cf6198ddc7072b3c4b0b07df7494d82f932efdbe0067ffd356371`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:55 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:05 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 18:10:09 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 21 Apr 2026 18:10:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:10:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:10:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:10:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:10:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:10:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:10:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:10:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:10:09 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:10:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:10:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:10:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaacc5fcb81aaf4c24ca62b7c7d748d4925abc4199e39981b80b93898777d06`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 21.3 MB (21303504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea8e162f72eb44c19a73f38e10d121143bdee45dc7426f76cb9f2b16ab73763`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 156.1 MB (156129898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37767c9371d4e03127e4bbe85929010c025d7d442785d1805b213575c0a75fd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12d0e0cbded327c9df870505ef20a84efb14dd8ccbe2a48a63e4120f61b65ba`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf6bc55af9dd8233fcb852c4f1a625bcaecff85d57d26c1802de1d58cb12790`  
		Last Modified: Tue, 21 Apr 2026 18:10:17 GMT  
		Size: 3.7 MB (3672154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea333e78c285ad04b6d01851d76a594b5074326b26ce664a80403c2f2cecfa6`  
		Last Modified: Tue, 21 Apr 2026 18:10:17 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acabb030bce065f71fe745fdcda9a0acd07deaf2e9a66442837fb039220c132`  
		Last Modified: Tue, 21 Apr 2026 18:10:17 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb18c25e27b407f5c258471f814b722f61fc3ebea35b9b14b951820017ff5723`  
		Last Modified: Tue, 21 Apr 2026 18:10:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:e068d0ce28b69169d955bfbb0f77048cdb7938a5e2fa0057b9d9a581b077b723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1410580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb26afdc448b9e7e8996f99889a3efa1589d1866f9e3564d7e69ffc5b54ed51`

```dockerfile
```

-	Layers:
	-	`sha256:7322aca0d94087f62432b685b5a6efd8823197f762cb0e851f7e1b98e6be3b9a`  
		Last Modified: Tue, 21 Apr 2026 18:10:17 GMT  
		Size: 1.4 MB (1393404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934737a5c5c687a0e8c4e39a5df9c44a5e4ee169ffc9d1f0e74682c106c54cec`  
		Last Modified: Tue, 21 Apr 2026 18:10:17 GMT  
		Size: 17.2 KB (17176 bytes)  
		MIME: application/vnd.in-toto+json
