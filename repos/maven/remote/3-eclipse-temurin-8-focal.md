## `maven:3-eclipse-temurin-8-focal`

```console
$ docker pull maven@sha256:a6eb8fd709a706f77041c38d83efcb0ea43af7c30ae84fffc8146503a3c85964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-eclipse-temurin-8-focal` - linux; amd64

```console
$ docker pull maven@sha256:fee3a3e95506786ed626763d9e4780340d1e9b25cf661f68fb4bc10ef3302e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186731382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef705ffe5973713d3b7d7691d0d966c8c66d65d6acdaa4f2a60c91b1d84440`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf168757422d85fc784edd9f8eab4082cd0da552a3faa4294d478d5faf0594d`  
		Last Modified: Tue, 16 Apr 2024 04:03:22 GMT  
		Size: 16.9 MB (16920620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0ab59b8ed3e298c9d2c6c066cac2970c9ad8f93c6b26511f074831755017ca`  
		Last Modified: Wed, 24 Apr 2024 19:07:04 GMT  
		Size: 103.6 MB (103602703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee77726f4d24a2c93d3ef6966270267af3c8d32968d48effd979f2a955c0a9d5`  
		Last Modified: Wed, 24 Apr 2024 19:06:56 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08d5d59446b4701bd709e9be09e30c42143d0c40bb011dea618c1c6b6924c9`  
		Last Modified: Wed, 24 Apr 2024 19:06:56 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4374818d93fa1abb72b0f0b2a40ae39c41658546400abd1e56f1b35a09ace36`  
		Last Modified: Wed, 24 Apr 2024 22:06:48 GMT  
		Size: 28.1 MB (28141327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c6903114bec0283bce75dcc5735d6be64af8e762c126581f26c6c494bd7290`  
		Last Modified: Wed, 24 Apr 2024 22:06:45 GMT  
		Size: 9.5 MB (9479958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e313ec175452d2c5943c8651e7f060302358bdb70e0ece0f21ed414cbe79a615`  
		Last Modified: Wed, 24 Apr 2024 22:06:44 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc351e72d441e33eaca22559ec330d8e73b123392fc0347e4be02adf206ecfca`  
		Last Modified: Wed, 24 Apr 2024 22:06:44 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c45a96acecb3352ce741d36d66b86d91aa7966a773b92a6510f2e08fb66d3b`  
		Last Modified: Wed, 24 Apr 2024 22:06:44 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-8-focal` - linux; arm variant v7

```console
$ docker pull maven@sha256:875d4c6982fc9fdc0db7a591018248093ccd251483c68446d93ef0ea760175c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173799303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a53922b75e14ac238880225ab3cb6e92b8a89dde85e5d177f09019bde04f9f1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d12b682cbcc5b59bbe1432d30883570b4dd781fd2260db8ec9fc50b11db15d2`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 15.7 MB (15664712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a38dfef8efb1c0286819ff113a40e99674a79c2694eec4dc63283c61869bdf`  
		Last Modified: Wed, 24 Apr 2024 18:12:35 GMT  
		Size: 99.2 MB (99229775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a0e9a38a12b4d4e1c43159c6fdc4902d43e79f39e6c88ffd86cb17fa91d20e`  
		Last Modified: Wed, 24 Apr 2024 18:12:24 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75588c85a5fcf56e5788fe902fa49278d4f001b03d09cc2e9e7d4a1611cf75c5`  
		Last Modified: Wed, 24 Apr 2024 18:12:24 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6528f1ef4d9c3057c21a230d72c829bbf23755847fc351141a6c37ff70b0743a`  
		Last Modified: Wed, 24 Apr 2024 18:43:35 GMT  
		Size: 24.8 MB (24819963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303309cf8bfe30e1c45726cbddbe67ecb811ffa19c13759516293407acf8ddbf`  
		Last Modified: Wed, 24 Apr 2024 18:43:31 GMT  
		Size: 9.5 MB (9479961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fa114acf7cde4cfe6a40ef067acd0eed95d61b1c15c5edccc33534a6cefdfa`  
		Last Modified: Wed, 24 Apr 2024 18:43:31 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af77392a93e105a0e875cef3c9fc6b911568b1548dc30584a142ccb8f888d6d`  
		Last Modified: Wed, 24 Apr 2024 18:43:31 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89dc78d6f033de0092fddd51f4b4e7cb1da159aa967e3017e4ac12990b9af62`  
		Last Modified: Wed, 24 Apr 2024 18:43:30 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-8-focal` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:271388a1f670b2b0cb407601eaf40320852d5159306d389aca7aab30527a44a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184354582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b415b3dd1fe53d30389a2d31b94e06b02f9f28026f615287f5e2ae283354997`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2f0d048c4dc921b108e92215dcba18b91b316fdaad6521463665d94fdab64c`  
		Last Modified: Tue, 16 Apr 2024 02:55:17 GMT  
		Size: 16.8 MB (16777181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4910f9b0d85f00f8d3fa97de873eb42473a197b2acaa65d87345b84f0175725a`  
		Last Modified: Wed, 24 Apr 2024 17:53:50 GMT  
		Size: 102.7 MB (102704809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea736a14d47ce7710ed990d162057b68ab0020a451debe738bd41f5eb18faf5`  
		Last Modified: Wed, 24 Apr 2024 17:53:43 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10545c467a700a81395c4835f0177bd339e702317d85d21dafcf570bc9891ee`  
		Last Modified: Wed, 24 Apr 2024 17:53:43 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384b615b1a9b827dd47da201d50ca3842b076b0519ebdd02392e67a07fd15af0`  
		Last Modified: Wed, 24 Apr 2024 18:57:59 GMT  
		Size: 28.2 MB (28185382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4522de6b547851921bddc8e547321d35c1e11853e8bdeac46dcf3f0c7556d9`  
		Last Modified: Wed, 24 Apr 2024 18:57:56 GMT  
		Size: 9.5 MB (9479956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad21b7c57221f05a4acf3270cac9932eaf2de6abb2eff92334eb952d8a86f02`  
		Last Modified: Wed, 24 Apr 2024 18:57:55 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53061faea3d1848953690b781b05f99c6489374d8a8284373900a793bcc7074`  
		Last Modified: Wed, 24 Apr 2024 18:57:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37c8e8a3976f5d1ab61d3a796682b4018c787035129d45753a6c3d95e55510f`  
		Last Modified: Wed, 24 Apr 2024 18:57:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-8-focal` - linux; ppc64le

```console
$ docker pull maven@sha256:101e04cc060916d55cd455cfa18ce58529cb637b52d1aba40cf84a31cebb8a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196582564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e071f08a72ebee7e9f92ba3589591de4f4f3ad0bf153960506546b3712df50`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 19:04:56 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:04:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:04:59 GMT
ADD file:8efe37e124c3eb7c9e2b3ba1f33a019526490b9a49cbe8997abf72caf6bb7ece in / 
# Wed, 10 Apr 2024 19:04:59 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0c372adcddc32347cef56486050a9e3f15243cd4c6b2ef3b7de6d5d6f7bf9ef1`  
		Last Modified: Tue, 16 Apr 2024 02:49:17 GMT  
		Size: 33.3 MB (33315676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf2659681487961e24fc1b8f8f4a0ce1842d1f26fd5bcb1498c53ad86d1d942`  
		Last Modified: Tue, 16 Apr 2024 02:49:16 GMT  
		Size: 18.2 MB (18222412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f724edb5c840afb3b2e7c96397762d5012bfb7ad805e058b73ec6c342320e156`  
		Last Modified: Wed, 24 Apr 2024 17:41:20 GMT  
		Size: 101.1 MB (101070811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5714a575b0ecb1c4f2a790dac4a5ab36a6720aad20a3f0a266d39bcc3cea860`  
		Last Modified: Wed, 24 Apr 2024 17:41:10 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8b2f5c9612a60e32a0d990ec5f27cf268db1c42227976c1ccfbd853447ca3b`  
		Last Modified: Wed, 24 Apr 2024 17:41:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b63c373ee4c7fc9808683f353b778d964d4efbd91779f050197dd3d39d2abfb`  
		Last Modified: Wed, 24 Apr 2024 18:45:18 GMT  
		Size: 34.5 MB (34491453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02e11d23ba90b5284225dfdfbbb1add0af95d1e8d9df8aa95c9e40ab91bb1f2`  
		Last Modified: Wed, 24 Apr 2024 18:45:12 GMT  
		Size: 9.5 MB (9479939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f98370f680523d212895169cacdbd47a61a31551416d100037184cf6c3b9581`  
		Last Modified: Wed, 24 Apr 2024 18:45:11 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6a5dd6b4989becc777eb243017e0eb912045ac3a349ca99b959d255aa879f`  
		Last Modified: Wed, 24 Apr 2024 18:45:11 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c69e56cda0d7a963ef2f342a530fc0379777ef5f058373b42fd915ebfd1c28`  
		Last Modified: Wed, 24 Apr 2024 18:45:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
