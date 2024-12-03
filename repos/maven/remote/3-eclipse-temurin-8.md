## `maven:3-eclipse-temurin-8`

```console
$ docker pull maven@sha256:6463e6f8b6ca9db29e7ad306b5ea1e5b57f20fb8b9e7fb253a674913aa673d13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-eclipse-temurin-8` - linux; amd64

```console
$ docker pull maven@sha256:b64af8c6dfe7f6a25c9e25bcf3b0666afa92ff08d3bd5d9db22c9646a52afbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182058092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487ba234fb9e0c675e1cebc56d638ec7bbbfd45350a1bce9455031cf7cfbd135`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f4ace5897523a1a5f235b03291ebbca78294e7d42b4f1425abd38b17701303`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 17.0 MB (16966378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6e2fd4158ef247a4fe5c04d362fd5595c2dc33f06cf9ba2bb74c89568085e5`  
		Last Modified: Tue, 03 Dec 2024 02:30:22 GMT  
		Size: 103.6 MB (103632853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc6481c0f3d295d0d446995ffc41a6315dfcf19f5a7ddae1815ef95e4b9ef6b`  
		Last Modified: Tue, 03 Dec 2024 02:30:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1559309569d4ae3c3e5925400c9677ba1e4fba6ec1256bb50e56450568393`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c941466b76c5b9219b32cc8e455f8a2fd934debdf03205e81d88014eb60fe3`  
		Last Modified: Tue, 03 Dec 2024 04:33:13 GMT  
		Size: 22.5 MB (22532980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe26e856d64a8b2875ecbd201f35866b3ed4fe264e21c00a587316f04fa7805`  
		Last Modified: Tue, 03 Dec 2024 04:33:13 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f9e2f589613002234ed135afaa0710c7d0f77d1c3be49bd62670cc332d73df`  
		Last Modified: Tue, 03 Dec 2024 04:33:13 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c9a1fe1c0445ee2ce1a9bd690c9b3f31e143b74556f7292f8e3fb7e41359f8`  
		Last Modified: Tue, 03 Dec 2024 04:33:13 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:e55825e74ba9322e9effc5a1eeec2c8dc7fe4c16b2b31bea428a27a71353853e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4851180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be70889a7dc4fecd59fabe70de0784aa310e1e15eb7f4c000661e9379090fd8`

```dockerfile
```

-	Layers:
	-	`sha256:f832848be54c4f9cae496c5b0eba5d710093b4faf89b6240c2edbf29e9f772fb`  
		Last Modified: Tue, 03 Dec 2024 04:33:13 GMT  
		Size: 4.8 MB (4831583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67e82fd6cd108078b92cab737d2afab1cd404d7aac8a5f89512e78cbdab64edb`  
		Last Modified: Tue, 03 Dec 2024 04:33:13 GMT  
		Size: 19.6 KB (19597 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm variant v7

```console
$ docker pull maven@sha256:55c832c6087cb7059b4a8504007d976d8341edb27c3b33de3749a5e4b570d4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178628402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27910713e64e2f8b0a4ee58f5d175d8b33b625d1a4fa1a9972651036b0060c61`
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
ADD file:9ba898ef47e3bf423fea81a90820aff75f6eed50ba716f3cba79e91e03e5cbbb in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:bca51b985bec22ed70905f426f055641ef48b89c81b90c99246fed6ff752a789`  
		Last Modified: Wed, 16 Oct 2024 12:48:18 GMT  
		Size: 26.9 MB (26869468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0e06a3aba6dfcad3a58df65f1de2a74e2f113618dade1cf05ae642689132f2`  
		Last Modified: Sat, 16 Nov 2024 02:58:14 GMT  
		Size: 16.3 MB (16299616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4479bec4ba0080da66032209b37f99c24f53b2d8534f7a2247cb150d5c96fb`  
		Last Modified: Sat, 16 Nov 2024 02:58:16 GMT  
		Size: 99.0 MB (99021605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89907ce7de4ff1e6f006392f53c84dfc017ee289d1b96b09686a67eb8e052d8b`  
		Last Modified: Sat, 16 Nov 2024 02:58:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3a7d51433ee20363a60077a52192c9ff267b9fcc91991ef8307266d1a992ae`  
		Last Modified: Sat, 16 Nov 2024 02:58:13 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127297c4d4042a5f3f51349fd0b54fa321f8814446f34df7d6acb209cfa03a53`  
		Last Modified: Sat, 16 Nov 2024 05:05:01 GMT  
		Size: 27.3 MB (27263808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217c802e1a992e27baae51e7a01cbaf631a7dfb423b8ddbd6e70e1e90b6c20b9`  
		Last Modified: Sat, 16 Nov 2024 05:05:00 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a84257b997c204970a3da8f9b367493d6c1838aa5466af7af4ee44a21cb4bb`  
		Last Modified: Sat, 16 Nov 2024 05:05:00 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5877ffb4495ff83225512ac38ea10c86f93adc34a6da5fe0fc8537a1798866df`  
		Last Modified: Sat, 16 Nov 2024 05:05:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:d1c62014f340dc47251891265d0f4c0c2c506e6a138333c404eaedc67e01b344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4853700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03370d329f0cedb71d7d9875cfdb99f802b97c96a029ae0dee66b7f05bdaf078`

```dockerfile
```

-	Layers:
	-	`sha256:d9dfba8cc1836da3946dba8ec0aae59fafba813ef20e7b8c58bea94d10d4fdce`  
		Last Modified: Sat, 16 Nov 2024 05:05:00 GMT  
		Size: 4.8 MB (4834006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f202171713d4b380c26d67a0a448f1001fc0f2b701016881e57a927373a426`  
		Last Modified: Sat, 16 Nov 2024 05:04:59 GMT  
		Size: 19.7 KB (19694 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2db88f69b2cadfacfcf7d49bf215f6182bc41fb61870531c8816b20aff50603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180397773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d9a7aabd33d0abe91bd8e7c2e051aad3839b5ad1779d6d1a38340e63885e9`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bc18bc29eb715bf1a5f404a45956786287384c81d8f10b7a98a9c7b8ff8c11`  
		Last Modified: Sat, 16 Nov 2024 03:07:33 GMT  
		Size: 17.0 MB (16980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d76fffdb04d20b9c075a2641f5964ac85f8dad2c187ae6d28e18a655f3e37`  
		Last Modified: Sat, 16 Nov 2024 03:07:34 GMT  
		Size: 102.7 MB (102747231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b4032b59b8784137a850c3cbf3c2b9424617698a737cc64c127d8ba361b65e`  
		Last Modified: Sat, 16 Nov 2024 03:07:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01d9222dbd88fa138f6460175b7d0e3d1dc5fa603744008af1c25480739f3e9`  
		Last Modified: Sat, 16 Nov 2024 03:07:32 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b438fc6c69417d404b9cc73de6539156da256793bf6efe351e3506c3f02f5490`  
		Last Modified: Sat, 16 Nov 2024 07:34:30 GMT  
		Size: 22.6 MB (22603230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960bf05015e1f3eb524ffe7ce397f86cf84082278c836082010948c5b35d9a63`  
		Last Modified: Sat, 16 Nov 2024 07:34:30 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf27147cb942f154afae9d542cb735fbcbfcaaa2d661a9e7d7484e11a737739`  
		Last Modified: Sat, 16 Nov 2024 07:34:29 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cc46ed03793c2cd87296e1a76d9dd49aa7a7ed99985bc4f148466ca2ecfcc`  
		Last Modified: Sat, 16 Nov 2024 07:34:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:35470958327bc921c6477edd4b2b31959d6be2aabc516ca561529ec606bc6787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4858508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c812a65b168438649dab4c657a5c94a3dd192a2cc8f7b51be4e0b40694b1d6`

```dockerfile
```

-	Layers:
	-	`sha256:263c69e26d5fa13cebc0affd920c97e854fc0f3b1f5783ffd6f159ace5a01270`  
		Last Modified: Sat, 16 Nov 2024 07:34:29 GMT  
		Size: 4.8 MB (4838779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:607f297eb8abc0021e42f166d0d7a1673f8ec848a9d568a254bdca43804639ba`  
		Last Modified: Sat, 16 Nov 2024 07:34:29 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; ppc64le

```console
$ docker pull maven@sha256:0942e64ff46b4287580ec75187adaf8756db64fa8995d6045b1d44becfc47f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190198829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d08aeb2855f10c21d52f89b80bc8052d7c37dfec5376c92b7dff298e9625b10`
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
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4ad667811bd0f6cf0781e97a793020501b77190fe2f1e993ed8ff99f2f6957`  
		Last Modified: Sat, 16 Nov 2024 02:58:20 GMT  
		Size: 18.8 MB (18845383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ed60ad1d954840e3ec54d8979f02c70b22e746ad6f5904f3904348ddbe4c16`  
		Last Modified: Sat, 16 Nov 2024 02:58:24 GMT  
		Size: 101.1 MB (101097509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80c0670f70978c476606eb8faf8abb01acfa7ffe9fbea2f0bd3f00e70ce644b`  
		Last Modified: Sat, 16 Nov 2024 02:58:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34aeedb7149ffdbead3d4f1680f9d327bc2b414fb02bc6842cf7d51f629455c`  
		Last Modified: Sat, 16 Nov 2024 02:58:18 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ad7ee3e8078071be7b96876eb2c7295bd229090bfc27507c744e002a06ef1d`  
		Last Modified: Sat, 16 Nov 2024 05:15:14 GMT  
		Size: 26.7 MB (26693221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d15e53b4a27d56d259b9cd8ea2c5f991cd2ab4da1d9b4736f6d6882e9b5218c`  
		Last Modified: Sat, 16 Nov 2024 05:15:14 GMT  
		Size: 9.2 MB (9170425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906ecbbc941a10e2c9a646eddd4fb84bd36a7a4d1655ea2c603e1ab6d017a6dc`  
		Last Modified: Sat, 16 Nov 2024 05:15:13 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfc5507a3d1937611fde1ba436d2ccbadf123035a99396fcbe67f94401f92f`  
		Last Modified: Sat, 16 Nov 2024 05:15:13 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:64c29f5a65a20579896dea62930b0e22ca4238d6fe302bf0bee418ad8ebf91e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4856583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098b6cbdf1a4e6a750abc2a6c90f9489661e955edb315f967dab7b061df3c940`

```dockerfile
```

-	Layers:
	-	`sha256:ddf03f0819d632231826f9e5b303f4ee642130b3fff289449242ab6faadd7e53`  
		Last Modified: Sat, 16 Nov 2024 05:15:14 GMT  
		Size: 4.8 MB (4836938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a04c7cbd3540be3a70aef6c7d0b418d029d2da1ede16171eb4641a566866ead5`  
		Last Modified: Sat, 16 Nov 2024 05:15:13 GMT  
		Size: 19.6 KB (19645 bytes)  
		MIME: application/vnd.in-toto+json
