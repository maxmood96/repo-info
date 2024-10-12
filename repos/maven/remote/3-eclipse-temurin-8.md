## `maven:3-eclipse-temurin-8`

```console
$ docker pull maven@sha256:ca61ea42805d8908f4a1bd2e38b01fef7d56e2df1a02cd4260e7ede5c30d3c71
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
$ docker pull maven@sha256:5f6d5e7907ca7e1b7c0612c9eb46f3f90dd44fae5d14102d87eed026b4a1121f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179730676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07d95e556da47e58ca13b95a117db62443d2dda8eba30f9865293025d66e261`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19ff092b07ec54ba33a1c50795a251bf6a0f8815acae6be50839968c8e90f2`  
		Last Modified: Fri, 11 Oct 2024 23:56:30 GMT  
		Size: 103.6 MB (103615814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557dcd3380e1c71b885c513e64a182739995a0c933e5d7dfd07776cf663225`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466b0407679cc9234e2005ca44b2274d0fe93891b6b285811c42cb5eac4843`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d5b38093615ccd197d1b69c222cb39fd49be44cef2cb08b80ef83e8a155b17`  
		Last Modified: Sat, 12 Oct 2024 01:55:16 GMT  
		Size: 22.6 MB (22556650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02c9f5fc30297bd355b8ab5bcd43f0d6c5dcf84ecb3150fea68824378123b9f`  
		Last Modified: Sat, 12 Oct 2024 01:55:16 GMT  
		Size: 9.2 MB (9170423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e316e682639accbfc60f9b4b721650e7abf2594c8f6b0f662bb0cc04d4104c89`  
		Last Modified: Sat, 12 Oct 2024 01:55:16 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56617f56e7ffa61af3d20b27ee0e6f431b69bd67ad434224ee26e8cf25bdbe85`  
		Last Modified: Sat, 12 Oct 2024 01:55:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:56c9f292599d15146c4d96cb89a2ec448755c111a5d8e43a74b7604e27f22305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4725599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fa4211cb5355b823c5d4b0e6fa1cb3db38f6622e73d471ae4204b925cff8af`

```dockerfile
```

-	Layers:
	-	`sha256:37bd0795d4cad84d264d58aa3f42b932fe202e23ee75014ac773315fb45fede1`  
		Last Modified: Sat, 12 Oct 2024 01:55:16 GMT  
		Size: 4.7 MB (4706005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1f0d6d552eb657eac9c1b6d35a106501c99a3b55852c107aaef2859e35cedc`  
		Last Modified: Sat, 12 Oct 2024 01:55:16 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm variant v7

```console
$ docker pull maven@sha256:68cff149edf85615478bfb14df1e30a856778cbd28096e61ff6b2ea87335dbe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176556832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa92bf1c3f4ff5106db168420fb690c5a1a69a64a065d65cca348deb1f3d91`
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
ADD file:a30667697f58d730cc31ae308b1ba41bf25987733d14114fca71a90447988801 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:ebc4eee72d0a91a5a59ea1b60758bd4ff0e56e71e15430000cf9a33bd0b45ca2`  
		Last Modified: Sat, 12 Oct 2024 00:33:04 GMT  
		Size: 27.7 MB (27734482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3d31f15da95226160d2c4d971d0721ec4463223129e41bcf869d34fcb64e5a`  
		Last Modified: Sat, 12 Oct 2024 00:33:02 GMT  
		Size: 13.1 MB (13135136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd859d8626614609efbc462b5dbb68e4f17c96a59c190f3c292fb6f2fe82a2a`  
		Last Modified: Sat, 12 Oct 2024 00:33:09 GMT  
		Size: 99.2 MB (99225322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca2842f7327f8a525c20339eae5972ac466dc91e51a7285f804c48e5a9ba41d`  
		Last Modified: Sat, 12 Oct 2024 00:33:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedfdba22cefc90d6c135c37ca8485d7959a505f41dfec43f8e86bca16e43657`  
		Last Modified: Sat, 12 Oct 2024 00:33:00 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5901bdac04390be257420c54cf792bb019af845443d403cc39932b79cccb3836`  
		Last Modified: Sat, 12 Oct 2024 02:09:17 GMT  
		Size: 27.3 MB (27288165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198886764caf11f7f5ba7263b52362e73143936478569e1bfe43bd55f7af21c`  
		Last Modified: Sat, 12 Oct 2024 02:09:17 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424f9dd5290599d168a74b036e19ae018f925c5b0238d2af0ffeddc42a986bfc`  
		Last Modified: Sat, 12 Oct 2024 02:09:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd252b28799afd7080475dc7a467a58d0a4320bb48ec5a8f5eaf71beec704e1`  
		Last Modified: Sat, 12 Oct 2024 02:09:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:1f23f065f455948216c824266f5d4dd744660b155094c7a5a6a21a969bafb029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4728037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b95c6191cee18c8d899c4995f346708b9c971f1f3e727586e47d28afb0d0c4`

```dockerfile
```

-	Layers:
	-	`sha256:1456e1ef1f1fe4b02f01874e147374df210447c34e8936e521bfe5eb36045755`  
		Last Modified: Sat, 12 Oct 2024 02:09:16 GMT  
		Size: 4.7 MB (4708328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f565d59068fcc043407d464713927007d8a30f058376448f22799a1cae4c44b6`  
		Last Modified: Sat, 12 Oct 2024 02:09:16 GMT  
		Size: 19.7 KB (19709 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ffb349ae68beb1be0648167361a5b913d437936c0c93e2cb07da1be81b4d8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178285300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60efcdc9f0ddcf506ef919809c6b36166e9ddca384f0e8c26d820ec1f718f9d4`
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
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f900b33601bc58f47cadfd8b5bb26dd0123e0fc3367f09849a81602b5e09c2aa`  
		Last Modified: Wed, 02 Oct 2024 01:25:21 GMT  
		Size: 102.7 MB (102732947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fee3a3896d40fbf36ee8b87e649b22374d9d81026f01e8ed8b8df9199a41cf`  
		Last Modified: Wed, 02 Oct 2024 01:25:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314c5e22b965c2288ea2c2695b764edaa6302e25ec3bfc90daf2a23b86c4799`  
		Last Modified: Wed, 02 Oct 2024 01:25:15 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc90509a2c9d35e56e2b1d00f906cc1905fd0e0c31f30a505d3327960419d588`  
		Last Modified: Wed, 02 Oct 2024 06:50:26 GMT  
		Size: 22.6 MB (22627874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06368b905a7f6855b0a2f9daeae63ff32e44183634106c05e595d0b4577e1034`  
		Last Modified: Wed, 02 Oct 2024 06:50:26 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fe24de30cf45ac7613132308206b6a522b16eab609dab4a88f486034b56e71`  
		Last Modified: Wed, 02 Oct 2024 06:50:25 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e080493d5e5158dad8c6e1f6847fea81c9e436cd2fa0690bd42b96d837e80c`  
		Last Modified: Wed, 02 Oct 2024 06:50:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:2a0ed5bf06e63cce7a29fe070cffd8c9ad50f067a0b16f0bca5d0a93ab7394c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4732290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f0a986c4000c0c297d7079f290d314610b91a8e171618cd96d5a53d47c3753`

```dockerfile
```

-	Layers:
	-	`sha256:3f74095091c6dcf4b5cb757d7000c0ddb071120f8d1c69b860a19b3c2566f12a`  
		Last Modified: Wed, 02 Oct 2024 06:50:25 GMT  
		Size: 4.7 MB (4712578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40baa294af42a077b60050c55754f14ab5fcbfc0699796f0ca8c87b3516f8880`  
		Last Modified: Wed, 02 Oct 2024 06:50:25 GMT  
		Size: 19.7 KB (19712 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; ppc64le

```console
$ docker pull maven@sha256:87d097b191d9f686529c0dbf440ebceb12e2d37d7ae462aacc4f700d30b1c98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187412090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9500bfce438733e4f7ec6b9a836ac4aa5f97dbeaba9493df404bb65cbe82fd37`
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
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8142fb4132be3efdcf8ea435bb4f9c7886f7dd7050b7ff796718a886a738003`  
		Last Modified: Wed, 02 Oct 2024 02:05:51 GMT  
		Size: 14.9 MB (14913665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772358c1726c3c8f45e8cdcada59f1e3b4e990228774720658530be9c985c982`  
		Last Modified: Wed, 02 Oct 2024 02:05:57 GMT  
		Size: 101.1 MB (101079859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcc6a5aa7a49e067c39a58ec32f438eb39c38d1bb391ab3ddf74cb8d0aaed61`  
		Last Modified: Wed, 02 Oct 2024 02:05:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da027e159150eff4f076178595a4201c5d9c35102cb5a05a256b4b87389a17e2`  
		Last Modified: Wed, 02 Oct 2024 02:05:47 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29fee0f8972831b06335c2fbba91c0eb1e326ae7f8210841a42d102c514b8d5`  
		Last Modified: Wed, 02 Oct 2024 04:59:45 GMT  
		Size: 26.7 MB (26726902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec55fc687ffbf04e4c21678bda5b2b95a7fdf6476d2b2ff3008ccdd585d0b4e`  
		Last Modified: Wed, 02 Oct 2024 04:59:45 GMT  
		Size: 9.2 MB (9170445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a984fb5528dea28e180b08e010c0ed3df288a55726f472cdd06345bfa5d969aa`  
		Last Modified: Wed, 02 Oct 2024 04:59:44 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25b5ba50be89fd4459c53f62e243153400710922a2bc6ab348399bce0cc468d`  
		Last Modified: Wed, 02 Oct 2024 04:59:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:ffc016b953b47c7ba561fa6732fe7e4659fdb8746d3dfb0f01e9f792a6d5a8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4730344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da14bc01fc24c83e2271fae7507240cb4305e6b735d2ba657f2c07ef4ce4f9ca`

```dockerfile
```

-	Layers:
	-	`sha256:17b79cbd4701ae07f1c4e2fb72b3b6be5fcdad202be63aadb62d142f9f06a022`  
		Last Modified: Wed, 02 Oct 2024 04:59:45 GMT  
		Size: 4.7 MB (4710715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ab51671b86627c4bc5424aa10fe8eb1e36ac16481b315687f8c4d8da1b41bc`  
		Last Modified: Wed, 02 Oct 2024 04:59:44 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json
