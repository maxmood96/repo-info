## `maven:3-eclipse-temurin-17`

```console
$ docker pull maven@sha256:69603a88e254dc1241d21185a14bc6ef7ce4a8e0253ea1f995260d551fbe8587
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-eclipse-temurin-17` - linux; amd64

```console
$ docker pull maven@sha256:97c2d388d113925d80f81c5688a10136d7a839b278ecf06389f4d5a53df18f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228952241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e5ed9fe92c62ae9a68b0a1befcd104b096f6cb2c0f706aecc6a6a645e43b58`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8682892fc02965930b9022c066fa164dd6f458ef4a5dc262016aa28333b30f49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='0c17fa4f14c0d2cc9e9334f996fccdddc5da4459d768f3105c7ff0283c47bf62';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='e69d43be937e05dbccae4cc98f732ed86aa11993234bf5ad6e81c30475a78ce7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='d4e553c6fa7afdfe2577420c6e77a558db8113a3cef84e755384148f5610834e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='e7c82833a7381a05cae2be0e947c08e971bbae4f2e4142c6ec87bbd7530a5646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='1f824d7369dfd570dc561e2a56035fdcd2970c97cbd355f6deb6ed0e7c6bcb79';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313db22050d42cd07a15b2168ff499fc84b04c4b6c4136701187232dce2e62f6`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 22.9 MB (22947805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739b9a71c6b151c8be13cac0ccb0684a7ccf41ab4f740165fe66c996ed800b7c`  
		Last Modified: Thu, 24 Oct 2024 00:57:05 GMT  
		Size: 144.5 MB (144542187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f8b7e216e39158f7fbdf8e8668837fef346be4db788396cadff27571e5c70d`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c99e6e516a5474bebeee0593966c60a8c43c6b8abc8ab2e651bd4ae22aae858`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c28d9f196f6b66eeede4e78f4bd10f507bff9747fffc7e4dc64bc4e9bcc55f4`  
		Last Modified: Thu, 24 Oct 2024 01:57:11 GMT  
		Size: 22.5 MB (22537864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddd0f08eff576042f27c2bf61130db4fe2566f2efed5ef892ce0a7766c1f3cb`  
		Last Modified: Thu, 24 Oct 2024 01:57:10 GMT  
		Size: 9.2 MB (9170220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f932becb7c7b697f88ccac7a1fc5c2c2a39dace8735e42453edc0280797d6cd9`  
		Last Modified: Thu, 24 Oct 2024 01:57:10 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93d7f23ff27bfb585e1234740fca268b7206bd4e72d603c6530e6592c6bd1f`  
		Last Modified: Thu, 24 Oct 2024 01:57:10 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dafe46583c2c9eccbb0af87f46e81bd01e17011bda177ab5fd081662c34471`  
		Last Modified: Thu, 24 Oct 2024 01:57:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:d998b7219d9923391af36a3a67f4e335c95bde47e87141512b0f1e1d6c3f14f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4882643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21f39471a11eafcf0b5581089209e251e63095f26e3bd4ba66b55da9ad21d1b`

```dockerfile
```

-	Layers:
	-	`sha256:3f00726be2e8fa6ce825b8789f68f58e35ddf2f1b5af950527b1d2cb3e157ad6`  
		Last Modified: Thu, 24 Oct 2024 01:57:10 GMT  
		Size: 4.9 MB (4858172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff7504d83f35214ac0102676d06b36033b9088b1ab56cd541b01f9d889c535e0`  
		Last Modified: Thu, 24 Oct 2024 01:57:09 GMT  
		Size: 24.5 KB (24471 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; arm variant v7

```console
$ docker pull maven@sha256:b22983e331809117de75ce1d89fe850d18e6a305072787c745f5b13e700571d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226706526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4aa365cae5e781779d02581b4ea944cd6cac2e42ea699c2c2c6b2dd1205ea9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8682892fc02965930b9022c066fa164dd6f458ef4a5dc262016aa28333b30f49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='0c17fa4f14c0d2cc9e9334f996fccdddc5da4459d768f3105c7ff0283c47bf62';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='e69d43be937e05dbccae4cc98f732ed86aa11993234bf5ad6e81c30475a78ce7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='d4e553c6fa7afdfe2577420c6e77a558db8113a3cef84e755384148f5610834e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='e7c82833a7381a05cae2be0e947c08e971bbae4f2e4142c6ec87bbd7530a5646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='1f824d7369dfd570dc561e2a56035fdcd2970c97cbd355f6deb6ed0e7c6bcb79';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294541900adc45791c3d858c84adf6dd1064feea3d794bc9f8c64815e290a694`  
		Last Modified: Thu, 24 Oct 2024 01:12:52 GMT  
		Size: 21.4 MB (21377626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceed315b0da705f915594fe984dd09762ff7af95c8ea94ea9d2d3b637c747db`  
		Last Modified: Thu, 24 Oct 2024 01:12:55 GMT  
		Size: 142.0 MB (142021381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6cca761ae18378fc77274f43ccb470ce89f6c1c9e17b1df24646d5e06abdef`  
		Last Modified: Thu, 24 Oct 2024 01:12:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5d93017d23613180172afb68107e322b184db67ec7aeb85b0ed1a1f90fa5c7`  
		Last Modified: Thu, 24 Oct 2024 01:12:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71458cdc657315fa56f12a340c8b7c53dcb8b6f74898ed951637e3379c0ff657`  
		Last Modified: Thu, 24 Oct 2024 02:52:35 GMT  
		Size: 27.3 MB (27267453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96847063b830a3f2268172fc3d5f39e240f1bfbb7f3df9468887836f481eaa05`  
		Last Modified: Thu, 24 Oct 2024 02:52:35 GMT  
		Size: 9.2 MB (9170217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bc64426a32872e1c99c5fa5cd9b3434797a564dbe3cad47e95a0b538ee56fe`  
		Last Modified: Thu, 24 Oct 2024 02:52:34 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b654e79e26f68a8aaa81064061b0e26d4819917300d640bd4eb188a119a17cce`  
		Last Modified: Thu, 24 Oct 2024 02:52:34 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382e2d29ab7ad4d963e9d08867977ec8be1b3bc8efa947750891f533204784f7`  
		Last Modified: Thu, 24 Oct 2024 02:52:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:33cc6c44c27e71ecf5efcc070ec013dcac498d142804aad4c2e84d58c7da004b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4821294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5912a03364e74a85f0f3bfd33bde8b41ba3db767253097353ef988700dafc09f`

```dockerfile
```

-	Layers:
	-	`sha256:bb8f36f496f236fcee81fab7d18ac826092423fff4dea7204a0dea2cf63b2351`  
		Last Modified: Thu, 24 Oct 2024 02:52:34 GMT  
		Size: 4.8 MB (4796688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b933575d6bdf20c0da6184aeaf53b18ee5f37092261d94af576e8c98ba977761`  
		Last Modified: Thu, 24 Oct 2024 02:52:34 GMT  
		Size: 24.6 KB (24606 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b3ad492a84cdc67ade7b4db435c7a511fd80135e165d0ab6683529afad3e9cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228194170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818a39a5051cd05f4158c0db68fbf2a5bf732b9b8d5ecde89db2a725a35aa731`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8682892fc02965930b9022c066fa164dd6f458ef4a5dc262016aa28333b30f49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='0c17fa4f14c0d2cc9e9334f996fccdddc5da4459d768f3105c7ff0283c47bf62';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='e69d43be937e05dbccae4cc98f732ed86aa11993234bf5ad6e81c30475a78ce7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='d4e553c6fa7afdfe2577420c6e77a558db8113a3cef84e755384148f5610834e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='e7c82833a7381a05cae2be0e947c08e971bbae4f2e4142c6ec87bbd7530a5646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='1f824d7369dfd570dc561e2a56035fdcd2970c97cbd355f6deb6ed0e7c6bcb79';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004549c9d7e4108958645eea52f71a0e8ba6f18d72dd6dca3a47239ce74704dd`  
		Last Modified: Thu, 24 Oct 2024 01:10:35 GMT  
		Size: 24.2 MB (24159122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225cb5fd64f3a6f155a1301661e18261d430eba8637a6f7e08c50e2774434caa`  
		Last Modified: Thu, 24 Oct 2024 01:10:39 GMT  
		Size: 143.4 MB (143368198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc78492c245adcc54dde954f84b79e98d71c8ac11fe26c874e1b1347f88550e2`  
		Last Modified: Thu, 24 Oct 2024 01:10:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea5a28f7c23fb8f6b9e31e7612b3c542394162012defbebf1f640ad33a5b06`  
		Last Modified: Thu, 24 Oct 2024 01:10:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878f62a07109a4bc1c6e84f338d9c7d7472bd4ab79c45e369cc350d1be3b3ba8`  
		Last Modified: Thu, 24 Oct 2024 09:47:19 GMT  
		Size: 22.6 MB (22606984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba63355dfc695379f7f9b29e7583aabdb617a26027ae4b37d6bb782f8bb3f14a`  
		Last Modified: Thu, 24 Oct 2024 09:47:19 GMT  
		Size: 9.2 MB (9170216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ff8964aee50bcf46c1b6a4b4c9fb180c64e917a793571ba3c5b1d1a4481dd1`  
		Last Modified: Thu, 24 Oct 2024 09:47:18 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d1d7ad89e02201ce3dd818bf534d160a5b44d1e53b47e57ed29ccd17d5ab31`  
		Last Modified: Thu, 24 Oct 2024 09:47:18 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af42910298d8a6180fd68a7de28cf581859551fda87acf000b0142af306c8d0`  
		Last Modified: Thu, 24 Oct 2024 09:47:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:e6dff87aac6a71fc111b9ca27d200c5b405b5b921a5b3d793cad3edc50ab23c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5020539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520a4f5096a07b35160aa2017653fb5673a0b2274a11ca6802b2d0b91de53fb2`

```dockerfile
```

-	Layers:
	-	`sha256:d9721a2f788dde23da3ad7d55994504c31eb6be0a403e6d7d1f4e5010d10ded6`  
		Last Modified: Thu, 24 Oct 2024 09:47:18 GMT  
		Size: 5.0 MB (4995900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e004aa2940ceef9ed83ddf514eb0dd2b9b93976ae845b03a4ccafa40d687a9af`  
		Last Modified: Thu, 24 Oct 2024 09:47:18 GMT  
		Size: 24.6 KB (24639 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; ppc64le

```console
$ docker pull maven@sha256:3a19c0e761ae1b5a7adde0f7293d47c3562b2b806181ad96f14558d021979999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238592111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57687f6a1273861c5fd417a2f9c2fe612ea7c5ea4d1f5447dcabebe2da5641f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8682892fc02965930b9022c066fa164dd6f458ef4a5dc262016aa28333b30f49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='0c17fa4f14c0d2cc9e9334f996fccdddc5da4459d768f3105c7ff0283c47bf62';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='e69d43be937e05dbccae4cc98f732ed86aa11993234bf5ad6e81c30475a78ce7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='d4e553c6fa7afdfe2577420c6e77a558db8113a3cef84e755384148f5610834e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='e7c82833a7381a05cae2be0e947c08e971bbae4f2e4142c6ec87bbd7530a5646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='1f824d7369dfd570dc561e2a56035fdcd2970c97cbd355f6deb6ed0e7c6bcb79';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5015b6ce586c1324ac541be983626d7a9d0798228304371fa667facca7145f`  
		Last Modified: Thu, 24 Oct 2024 01:13:37 GMT  
		Size: 24.1 MB (24135598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79428199ee3768c72702be2623001eee0e71cafd6171114e8bb09cc3b9cdc1f2`  
		Last Modified: Thu, 24 Oct 2024 01:13:38 GMT  
		Size: 144.2 MB (144196134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4ee4451c9b7f35830a8825066bada2aa7b005ccf04084cbb742dfa45011e97`  
		Last Modified: Thu, 24 Oct 2024 01:13:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a08717df683ec07fa3d75ef0ef63c98a9597cbb56270ed3e0ae7e44aefa6f3`  
		Last Modified: Thu, 24 Oct 2024 01:13:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79f0de55c692b83885e83c981c605a3ca313009aa845fe74a53a5009b05809d`  
		Last Modified: Thu, 24 Oct 2024 05:49:03 GMT  
		Size: 26.7 MB (26697406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8443eb401229fda1c9c8aa9fa8d26f1c4b3e7dfccb4768066478a35b6fcc2f`  
		Last Modified: Thu, 24 Oct 2024 05:49:02 GMT  
		Size: 9.2 MB (9170202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93ca69f35c39ad24c16814d8d21aba0990484159ea921db8ae560809a4601ae`  
		Last Modified: Thu, 24 Oct 2024 05:49:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba91a1de86d8e33ffa6889259204696fe98166f6d372bcb5ea6df5e981b38831`  
		Last Modified: Thu, 24 Oct 2024 05:49:01 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113aad867a1afb2786b32abe9fe020fcb47b2f3471895292aafb76e6d7a7c459`  
		Last Modified: Thu, 24 Oct 2024 05:49:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:8ef46206fbcb51fd0ffe0c3791b3601fbc19acbe31c307de86f4b83e11ae9220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f8efd1ee38ab5b557781e32298f75062ef923e5f42e3fa0085d4c518d0f22c`

```dockerfile
```

-	Layers:
	-	`sha256:16bce48182a6c1bee9dba5d706964b255113aa378b0134886cdc0b2f30c7ff8b`  
		Last Modified: Thu, 24 Oct 2024 05:49:01 GMT  
		Size: 4.9 MB (4908983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e74694fa7c2a55442639b73c132e33d7a6e6257890b0b37db86537568df31b37`  
		Last Modified: Thu, 24 Oct 2024 05:49:01 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; riscv64

```console
$ docker pull maven@sha256:352737409acbaa944d0bcdf1778ad52db261037a77b66c118a19f864faeb25d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229591882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd52f65287caa068c96b5fad15e344650db641a3f22d4defd7ed93790310c25`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8682892fc02965930b9022c066fa164dd6f458ef4a5dc262016aa28333b30f49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='0c17fa4f14c0d2cc9e9334f996fccdddc5da4459d768f3105c7ff0283c47bf62';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='e69d43be937e05dbccae4cc98f732ed86aa11993234bf5ad6e81c30475a78ce7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='d4e553c6fa7afdfe2577420c6e77a558db8113a3cef84e755384148f5610834e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='e7c82833a7381a05cae2be0e947c08e971bbae4f2e4142c6ec87bbd7530a5646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='1f824d7369dfd570dc561e2a56035fdcd2970c97cbd355f6deb6ed0e7c6bcb79';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad1581c9aa53a3728149e757b765396bf63e7437bad2bf2ac1fc3d2bfb77849`  
		Last Modified: Thu, 24 Oct 2024 01:03:04 GMT  
		Size: 20.1 MB (20136424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96992892fcbc5ef9c9af32d864aad5abd78c894f79f35a185b6e021d946d7537`  
		Last Modified: Thu, 24 Oct 2024 01:03:21 GMT  
		Size: 138.3 MB (138338900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf089296b141293d9c2b7d5d694d27fa1488ccaafada5d43d4c1e3d7d438ebc`  
		Last Modified: Thu, 24 Oct 2024 01:03:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8853f215b35f18f7b3678fa0dd42c401c986d02ac27de1bcf209e3a8d373c9`  
		Last Modified: Thu, 24 Oct 2024 00:56:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5066016ee8685fea16fe3613893d96b660423e9d91d29373eed0ec51a6d614b`  
		Last Modified: Thu, 24 Oct 2024 02:47:48 GMT  
		Size: 31.0 MB (30990956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd85ef11bcc353a3f06e67f1e538674997333351fc5fb77639e2b0d888cda4d`  
		Last Modified: Thu, 24 Oct 2024 02:47:45 GMT  
		Size: 9.2 MB (9170204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2d928d88e535e72a2a62eb12f80fab09bba5d3e7dc09f501d405e2f6ed043a`  
		Last Modified: Thu, 24 Oct 2024 02:47:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e1685d6b2e47b6fd7d32440e786a2fed1e62d68f34064ec4f78360f76802c6`  
		Last Modified: Thu, 24 Oct 2024 02:47:43 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c73e2863f6784fc4e92e79d97446f3e1b3cd924f3e9193f8210f551245cdf8`  
		Last Modified: Thu, 24 Oct 2024 02:47:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:4f592f7e0c3560bc7671a3304afefaf91850a845d239b30710ef6d281ae62f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4985049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1144e414fe82e682c87885303043d8eea5b2971f42c7ecd768a80e2146c76c69`

```dockerfile
```

-	Layers:
	-	`sha256:10491910d63da5665f344e423f8dd44cb7354deea2886a20a89850a929673431`  
		Last Modified: Thu, 24 Oct 2024 02:47:44 GMT  
		Size: 5.0 MB (4960529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a224e6d7d98d22a420b25cb27678ae83c46c1d8dd58728fd61ee563882efbf2`  
		Last Modified: Thu, 24 Oct 2024 02:47:44 GMT  
		Size: 24.5 KB (24520 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; s390x

```console
$ docker pull maven@sha256:6eccc4248883a6aaec57d8a71ad63db3aa5558313acedd77e6ee501bef4d4795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216159864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee11f98593dee7402ce0ce3424b230c40cac40cd642867889aced766da0412a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0365f8f011adba5646c2f5892be4b464bc78f4f5c2ed54a9f046872c7a39de64`  
		Last Modified: Sat, 19 Oct 2024 04:03:12 GMT  
		Size: 18.7 MB (18733167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103bc9001d473219f9bcc06a4511dacdfecf71903e821f060d9c9ea697198a30`  
		Last Modified: Sat, 19 Oct 2024 04:03:13 GMT  
		Size: 134.4 MB (134408587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fbae76e4aafc8b2bcf8052da5173b3ab52b889a47aa0466c54501cb26aa30a`  
		Last Modified: Sat, 19 Oct 2024 04:03:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129b7cf8cb3903b5ef77b9608f2a0d2b3655b4509cbb5e46f47a2e3bd20adf48`  
		Last Modified: Sat, 19 Oct 2024 04:03:11 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b709df1319a0f61d9a7618c78385b715c546d504999df9ad37aaa85f5c1fc863`  
		Last Modified: Sat, 19 Oct 2024 06:43:24 GMT  
		Size: 23.8 MB (23824678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4246538388183755428abc38674b1460efa69887b290c9e1c2ec893d2ce1716d`  
		Last Modified: Sat, 19 Oct 2024 06:43:24 GMT  
		Size: 9.2 MB (9170195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748a33c585d77a3fa9826ea6bbb27ef314ed63e3b897452cedd4d92966f238aa`  
		Last Modified: Sat, 19 Oct 2024 06:43:24 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc6bc55d251b9e828af547c4fd0d663202e43db8b15685968f14d6ec0336810`  
		Last Modified: Sat, 19 Oct 2024 06:43:24 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732c49648ed348b4d7d7b8bf4b251aea16ce818eebf2626b6a9a0090bede4991`  
		Last Modified: Sat, 19 Oct 2024 06:43:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:529cd5a3072c174044341cd01247a4314d43ff95d679da0c5f41f04a22ed0964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4724849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8362ef262314c6f032c0dcf869c8f1a79a94cb1fd08a7965d72e550c023540ff`

```dockerfile
```

-	Layers:
	-	`sha256:4d1d6195ade0fd82fcf1c9e97b1612c9b0d11deb4f5cb6299556c4aa8153d59c`  
		Last Modified: Sat, 19 Oct 2024 06:43:24 GMT  
		Size: 4.7 MB (4700382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0ce701280d4870afd851c08fc77e59c984be20e23c9ba2b757bc25fc004db10`  
		Last Modified: Sat, 19 Oct 2024 06:43:23 GMT  
		Size: 24.5 KB (24467 bytes)  
		MIME: application/vnd.in-toto+json
