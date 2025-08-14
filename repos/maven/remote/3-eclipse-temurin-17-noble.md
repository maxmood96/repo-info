## `maven:3-eclipse-temurin-17-noble`

```console
$ docker pull maven@sha256:2490f24bcc21b108f850f7039049a9d7f37d6d10b46b0b77779f5d76c12fad64
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

### `maven:3-eclipse-temurin-17-noble` - linux; amd64

```console
$ docker pull maven@sha256:b9945723b0c4261e5a536be915cc5fa0a2508eb297e67699f9d3a7d8a66ed501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229177578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3d6c494fa5ef56ae5dd4e46b34694364986ab910c0d2496c0114079ed7c184`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc74333da4c494c38acb09c8b9a50cfd969bf81f5b317ee613f8aa6bce921fc`  
		Last Modified: Tue, 12 Aug 2025 17:24:54 GMT  
		Size: 23.0 MB (22958600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f0160053e602868c59033ccdd477c33155c1fa3247ad87fb79c8e836a937af`  
		Last Modified: Tue, 12 Aug 2025 17:52:02 GMT  
		Size: 144.7 MB (144709066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064c53302191c032453ab872775092dd32d7051751d039e8d32b3d95bf0407c3`  
		Last Modified: Tue, 12 Aug 2025 17:24:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bc75678de73925de23138592ac9b0e4876ccc7ef8b38dc0b19955dde37909f`  
		Last Modified: Tue, 12 Aug 2025 17:24:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f89ece7e254b1a4f1a071088319a58193c9fb23973124f798ca58633d7f4bed`  
		Last Modified: Tue, 12 Aug 2025 18:08:11 GMT  
		Size: 22.5 MB (22540529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb4969e14d9f53215a1692764e7f087d16d0beecd0c9374c97c6d5b8fa0e408`  
		Last Modified: Tue, 12 Aug 2025 18:08:10 GMT  
		Size: 9.2 MB (9242366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96099c5ff71163715e31a7d48d56d4bdfa2c1732fa3d16d9b837eeec85be0abf`  
		Last Modified: Tue, 12 Aug 2025 18:08:09 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c194aa64fb1bc12a4b861fd8723c6df2465dc6cc50809119e9881788b31747`  
		Last Modified: Tue, 12 Aug 2025 18:08:08 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7934e4694624b5dfb275f3bcdadb6a492fb24aa6e060c8ad04715f2a2c7af`  
		Last Modified: Tue, 12 Aug 2025 18:08:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:557f527f3740e559c2ef9ca4b2193831d6e9865df861ec9088a62ef61dd4700b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0824b1777f34fc4613b5f8d090b60bb22f31f05263210dd8b286d36119ce8ef1`

```dockerfile
```

-	Layers:
	-	`sha256:46cdc94436de2886de1208a558a19bf11821369640fda0f8e0719a7d2352360e`  
		Last Modified: Tue, 12 Aug 2025 20:29:31 GMT  
		Size: 5.0 MB (5044735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3368976c09812f407d12a1d0557fbcbb3e57b3e8cc1c4231ad8395e629191998`  
		Last Modified: Tue, 12 Aug 2025 20:29:32 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; arm variant v7

```console
$ docker pull maven@sha256:95ba84bca212d46c26dca75b354d4485eb322f77a960c6f9196d2b7faf3bb52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226934459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf702eb1d51595d052407c399c3aa63ee80a8192b2c97f5f43d9ba36dad5254`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 06:54:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:54:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:54:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:54:14 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:54:17 GMT
ADD file:3d0bcbe19ab589b9febc888a3f1e7d731d2ffc32ab216f5a65461d73e6542ece in / 
# Wed, 30 Jul 2025 06:54:18 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5775aaee0b6caf578e138eda76ce3385180e0796b81e02b9edf4909084017d62`  
		Last Modified: Wed, 30 Jul 2025 10:35:13 GMT  
		Size: 26.9 MB (26851072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42576fb14e0089a3dee0ca0e361cb6318f486dae33fa1d3fe13380aadc692857`  
		Last Modified: Tue, 12 Aug 2025 17:32:53 GMT  
		Size: 21.4 MB (21382351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cbddab3759d7c729dae7f5489a242e37449e1ff80cef894bc5330ebc51b60a`  
		Last Modified: Tue, 12 Aug 2025 18:15:50 GMT  
		Size: 142.2 MB (142181069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ecdd7bd1dbe7dd45d7f1d8eb45c43b2d9030f9eb69c01cbb068aa351d67b7`  
		Last Modified: Tue, 12 Aug 2025 17:32:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afe8e94422a72468f9ff20f7ce8b5292baa5b98cce2f31dc7a4dd05991f2102`  
		Last Modified: Tue, 12 Aug 2025 17:32:51 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47512de838721d80207e4264bab56b8da7b0fd1393b6f6c598195aebd0669c7`  
		Last Modified: Tue, 12 Aug 2025 18:43:53 GMT  
		Size: 27.3 MB (27273805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12f178fc0aadad8da8113b76ce36c040c842f44706ab6d53c84e5a0f6019537`  
		Last Modified: Tue, 12 Aug 2025 18:43:50 GMT  
		Size: 9.2 MB (9242361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa30c9062269d7fe9f14972546224a939f7b53ba0b2555f8539a925ae765f048`  
		Last Modified: Tue, 12 Aug 2025 18:43:48 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538e721f355023eedde51212df0e4c3d87800e68cbbff71543ffa53859a1327e`  
		Last Modified: Tue, 12 Aug 2025 18:43:49 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd176a3bee2baa8b3064d07da7c69661dd008f5045d497c82977a80c6217ce`  
		Last Modified: Tue, 12 Aug 2025 18:43:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:e6222eb986f3f21f091278337ac73b06f2c49131be25842e759d7b2f70a471e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5009290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3da0e74e65aa51b5c574d479f81326e3e38b0059388e507c0f15e3e6f5c973c`

```dockerfile
```

-	Layers:
	-	`sha256:aee2fd51abc51821620649e3db95041891e0cd9bb0422dcf72c1dcfff3947a76`  
		Last Modified: Tue, 12 Aug 2025 20:29:37 GMT  
		Size: 5.0 MB (4982984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e7b3ec87cfaab93b50cbb319b470ff47975ddbc81279502aaf639984412cf7f`  
		Last Modified: Tue, 12 Aug 2025 20:29:38 GMT  
		Size: 26.3 KB (26306 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:171169eb9ef40b05d49b14a7682b4ee5a9545e00f6ce82788d7587bcd5af5730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228430246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acd6cbdb346960c98e4b82394b853781276bc415514a39faf04668c8050dfde`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5ce41d5de7afb59affbe0233d7397418d2e57ed330589e31f1678f08a6fa5e`  
		Last Modified: Tue, 12 Aug 2025 18:36:42 GMT  
		Size: 24.2 MB (24165644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d55345c9f52c4aac86ef457e4fc0501d41b61587ea4a58378e7e8d1c61870`  
		Last Modified: Tue, 12 Aug 2025 21:15:05 GMT  
		Size: 143.6 MB (143551065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440c0b74cbaa80475e590bcf0acfbe03631e680d6d49d3fe0e5558c4889c4b31`  
		Last Modified: Tue, 12 Aug 2025 18:36:39 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0667e5bf8b32b0d2f27795e29fe215500d061c4ab51ac77a39ea29e0dc20706b`  
		Last Modified: Tue, 12 Aug 2025 18:36:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a52f79062d756555520c522804d23bbe3ed3cb3b0accff54f7e25124444a42`  
		Last Modified: Wed, 13 Aug 2025 01:46:50 GMT  
		Size: 22.6 MB (22606993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54062f20ba6b7e533ab8d35709016297070c0aa253d743571845babab041f42`  
		Last Modified: Wed, 13 Aug 2025 01:46:48 GMT  
		Size: 9.2 MB (9242364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484259b6d6637257b81416c378ada67da3647afd73e01301b01eae961f1a1f15`  
		Last Modified: Wed, 13 Aug 2025 01:46:49 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1435df9b7923f9cebe119ef2ccbf06472f3d0b21b64799416a638a0acee8e46`  
		Last Modified: Wed, 13 Aug 2025 01:46:49 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a5cd873e08c3346bbfa5eea6020360f5ba4ed1be58bb23738094490e0eab16`  
		Last Modified: Wed, 13 Aug 2025 02:23:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:16e0dd489c13ec7a25728b318d6fac37110e725c46af5b61f5ed5b87b7f8cebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5e944138d9cd78c7911e635214263f103b06877eba176b8413afa1a86f0865`

```dockerfile
```

-	Layers:
	-	`sha256:286f8a248b4ba341f7d6f5c16d3a94803bd8f60a3c9cf3c051c10ad0171dbeef`  
		Last Modified: Wed, 13 Aug 2025 02:27:49 GMT  
		Size: 5.2 MB (5182332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7f5e39fe392b69e101a1f5cc38c7129cabafd52f639adf6324b45fcbc00610`  
		Last Modified: Wed, 13 Aug 2025 02:27:49 GMT  
		Size: 26.4 KB (26351 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:04e73c1fd3a4a924c711ec4615d0ad7e0938efbddbf4d59ff5a59bb8d45c3d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238642057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ce18d5e885399f505732448270733584f662c86f2685800a368337d93a741a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dac22db2acf299562658bdbfc8f885fd4929a06be6ed9a37bc4736330fe91b`  
		Last Modified: Tue, 12 Aug 2025 17:39:59 GMT  
		Size: 24.1 MB (24101582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac82f6b68419b9b383232bce28f576fb943a2c90fab5a97a28b2613fd33c53`  
		Last Modified: Tue, 12 Aug 2025 18:16:20 GMT  
		Size: 144.4 MB (144376468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05719b1e9f11c62945452e51cd044b4b684342ff1fb1c39acc4b744579eeaff6`  
		Last Modified: Tue, 12 Aug 2025 17:39:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d92db65854b89b03eb6fccda8fee1d3261d8be523761e3c8b01ca4318c87d`  
		Last Modified: Tue, 12 Aug 2025 17:39:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e16b5ddb16f7214b636103b82267c002722fe019b47d1b818dba50b1686c9c3`  
		Last Modified: Wed, 13 Aug 2025 04:24:46 GMT  
		Size: 26.6 MB (26588193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fab241ac4657dc74166508d5acbd419a48e4974a9a0f9f11f001d0cdd0c68c5`  
		Last Modified: Wed, 13 Aug 2025 04:24:40 GMT  
		Size: 9.2 MB (9242361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71de91d361c9edaa4a2de82b88407644c75d3f234c75d53107fc4cfd7e5777e1`  
		Last Modified: Wed, 13 Aug 2025 04:24:39 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f312753163e265770c2a32df77b219e72b1076c6c7aa98ebc292b4b24bbbdd`  
		Last Modified: Wed, 13 Aug 2025 04:24:39 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332c7aa70a8d751f02808f17255b4e2ab63a59954795dd455f2310f0c566d034`  
		Last Modified: Wed, 13 Aug 2025 04:24:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:a9fb81f7071af19c1c59a6dee902e97bc3c4abb28e3773d3a97b6f3a818d7fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce630f938e61780af1a190bfbd1d47e70bc67cbc73a60722445db7676e0a72f8`

```dockerfile
```

-	Layers:
	-	`sha256:0a9a528c969c7a101d6a4a87106c882e312b28a5943dcb65603cada421ff0937`  
		Last Modified: Wed, 13 Aug 2025 05:27:47 GMT  
		Size: 5.1 MB (5095310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023c37b58b20eddcfc989e6e3b5b3179c3078c19db2428b8005c1c4db373d964`  
		Last Modified: Wed, 13 Aug 2025 05:27:48 GMT  
		Size: 26.2 KB (26214 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; riscv64

```console
$ docker pull maven@sha256:65b64b08c89dc03b680b94eff44329fa0c2a2859332f17fd027ff95d521ab416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229919655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f1e0f88e9c3561cf534a4a385c255cf2748c434638dca4da673a8fa53e7ad6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 07:17:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:17:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:17:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:17:52 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:18:34 GMT
ADD file:07f3c32dd2b7f6af0f399701257442794654b72aa96759b98cb033a715461739 in / 
# Wed, 30 Jul 2025 07:18:38 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b12e9b07091787c99b29dd2be63680c86c47e8be60a46566329007fb82cee41d`  
		Last Modified: Tue, 12 Aug 2025 17:05:53 GMT  
		Size: 31.0 MB (30951577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad34db99b8b6d3689c6e8a55f34d183fc435ecd3c12cf99054a4e88b66485262`  
		Last Modified: Tue, 12 Aug 2025 18:16:38 GMT  
		Size: 20.1 MB (20142191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c20b456828335156e9af29dddcb8d879f424e36c64d2f63e7cbfab734e9a24`  
		Last Modified: Tue, 12 Aug 2025 18:16:49 GMT  
		Size: 138.6 MB (138580518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9edf7e0149887bfaac6077f4100e32ec06f5bc2b62c4ab4588b8b4f82f1f92`  
		Last Modified: Tue, 12 Aug 2025 17:57:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab0ef07f935b052e7ff1e2bc8b513a33b344318312cdb54e1e72c42f1aa5f5`  
		Last Modified: Tue, 12 Aug 2025 17:57:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089e2318e6036645ecad8725d98c42793e815b36690042ec718910ebd7e6a4c9`  
		Last Modified: Wed, 13 Aug 2025 00:56:40 GMT  
		Size: 31.0 MB (30999195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7bd63c83f01261a0a1f10233f320f4af039da285fc0a1a93889dcb1c7053d1`  
		Last Modified: Wed, 13 Aug 2025 00:56:40 GMT  
		Size: 9.2 MB (9242370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0358f9947cb84ed518090753c6c4757665aaf6a121c2a1f7a4ee8b070a1cf7fe`  
		Last Modified: Wed, 13 Aug 2025 00:56:40 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa424173c42e009a9a277b854a9f6ab925f214b3388171cc6dc14d83604874e`  
		Last Modified: Wed, 13 Aug 2025 00:56:40 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061797fc28693b7504d8f3659f4605ec727f9b498c0549ef253992643d2ab45f`  
		Last Modified: Wed, 13 Aug 2025 00:56:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:fa4e8b085fc3159274a32ceb156924d53068eff7d7c0d60725cbbdc218b937d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2318fe89d8c98fba2fbde49d35390ccc0890b792abfcc221ed19126d5bfd947`

```dockerfile
```

-	Layers:
	-	`sha256:29db206a7b604adffe5ce0c8aa3ee59f0bff022fda7182a34528329dbedf2bd6`  
		Last Modified: Wed, 13 Aug 2025 02:27:58 GMT  
		Size: 5.1 MB (5146456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c29ebe9636bb3ce6eff9fcc264344d1d5eb5b9a723115dbca87b9763b121d54`  
		Last Modified: Wed, 13 Aug 2025 02:27:58 GMT  
		Size: 26.2 KB (26215 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; s390x

```console
$ docker pull maven@sha256:7f6f46a94acdfa3f6ad76f60b64b7a7591d3bf2646a5f0f297229d0c583eb02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219703444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a3afd3ff98f1e4875c60e74ab5b220a31968b70815b9d28fd9fa34b1437ff5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jul 2025 06:55:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:55:12 GMT
ADD file:f751959e6b8dae58a35017dc82c7271708f085c111710b59527373699b0784b5 in / 
# Wed, 30 Jul 2025 06:55:12 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 05 Aug 2025 09:41:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 05 Aug 2025 09:41:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Aug 2025 09:41:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 05 Aug 2025 09:41:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 05 Aug 2025 09:41:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Aug 2025 09:41:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Aug 2025 09:41:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Aug 2025 09:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1c5d0b18c745fadd2e177b54d4df793f25b01437577bc09c72ae52a0f3f9aeb3`  
		Last Modified: Wed, 30 Jul 2025 11:30:49 GMT  
		Size: 29.9 MB (29932680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca1d3019421a7aa66519824ce0e982b25db3c4e4004543099d050378dee3b89`  
		Last Modified: Tue, 12 Aug 2025 17:31:44 GMT  
		Size: 22.1 MB (22128620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ac1a7359dd83344dc45d57049f968f616ea9d59746e67a36832c70ea99fb51`  
		Last Modified: Tue, 12 Aug 2025 18:17:16 GMT  
		Size: 134.7 MB (134730198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cf3e0a0182170b8fb500dfe966cb78f3299261fdf5d4cd241f9cb72addf05e`  
		Last Modified: Tue, 12 Aug 2025 17:31:40 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b30f160eda60dc725b0682217d19a8e207f2e6f0031817c1b525226c8f8437`  
		Last Modified: Tue, 12 Aug 2025 17:31:41 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2964cc200ca1104ef619539d00da4a5e2969e4a0e57a69bde32bbf71a0620853`  
		Last Modified: Tue, 12 Aug 2025 22:37:08 GMT  
		Size: 23.7 MB (23665797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73da5afaffd774262f374e551375dcf7d16c94c71ebf59933c29ea72e958ce2e`  
		Last Modified: Tue, 12 Aug 2025 21:14:51 GMT  
		Size: 9.2 MB (9242349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956a3f7b2dc05da8b8d794b789395b296adf99bbbc529403953c40bc2fc81415`  
		Last Modified: Tue, 12 Aug 2025 21:14:57 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3fb2d624ff2ec1b3574fc3e6b08a90bd9a9aebdd8281b6d335bcb8cd38a85b`  
		Last Modified: Tue, 12 Aug 2025 21:15:01 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d666e53aa6ba0572a51f88c803bef9e289d14f30b663f73a0325bbd40531eea5`  
		Last Modified: Tue, 12 Aug 2025 21:15:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:b860e2cbcc4003a0c9e25b2b90eda591a1bde9cd402c5f358e25d4d5fdccf890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5016283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bb6b1542634e1284b274d9c271cc4c8e26be7e08fb18cecb1ee1d56784bb54`

```dockerfile
```

-	Layers:
	-	`sha256:ef61cab336e0a3dfeefb6d7aacd22f3cc3b3f00d1a0a9e43a1b1926ec33f0939`  
		Last Modified: Tue, 12 Aug 2025 23:28:18 GMT  
		Size: 5.0 MB (4990137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f172f90368602e0248711aa0a53636cef22f5e2d65a6ff367bfbb8ebd6bb20c`  
		Last Modified: Tue, 12 Aug 2025 23:28:19 GMT  
		Size: 26.1 KB (26146 bytes)  
		MIME: application/vnd.in-toto+json
