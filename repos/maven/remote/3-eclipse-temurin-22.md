## `maven:3-eclipse-temurin-22`

```console
$ docker pull maven@sha256:24650ecbf1335046b43e80a657f3fcffe4e7d87112ae12504ac4c7ea908f894d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-eclipse-temurin-22` - linux; amd64

```console
$ docker pull maven@sha256:9183dbfe5feb5b1ae479308ff4af062cfb44f5cbe13d3eecf39305d7b44ff560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233082183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31830a488dc47d527fd8970326382ba57a1a809d388d105b3777b284b73ad03`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 14:25:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 28 Mar 2024 14:25:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 28 Mar 2024 14:25:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 28 Mar 2024 14:25:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31e36bca11a3dc3a0c7d2e5d4656928537deb0d7cec7e4e4eb08d9d17b75dab`  
		Last Modified: Tue, 16 Apr 2024 04:07:50 GMT  
		Size: 16.3 MB (16337609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b9f1fa8bcf0d68f947e97661090e95c2c415ad20d3a9e2e79f042a754de0a4`  
		Last Modified: Wed, 24 Apr 2024 19:18:37 GMT  
		Size: 156.7 MB (156718125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5affb9e2ba3f1d576c3e8c285a4164f3603dbacd4b8df539da41602f360e68b`  
		Last Modified: Wed, 24 Apr 2024 19:18:24 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea31b3da51f302b7667893ae645797f78c4d70e1e8cc56b83eae6cce61178fc`  
		Last Modified: Wed, 24 Apr 2024 19:18:24 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83addac326e4e1deeffb0ae80de6baea25cc3f208447b1a881bd3afeebf3a51b`  
		Last Modified: Wed, 24 Apr 2024 22:05:51 GMT  
		Size: 20.1 MB (20104475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54781e78e9368b358e7c03b0cd3fcdafe5c63bf102dcba0ebd7661f94c4a782e`  
		Last Modified: Wed, 24 Apr 2024 22:05:49 GMT  
		Size: 9.5 MB (9479949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dd8c87d4032aa0256ee7902eddc7729564a14c8973a4d0b903beacbfdca890`  
		Last Modified: Wed, 24 Apr 2024 22:05:48 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea2a5810d6d44adf0e455574ec6fa6c4659791056993969087d7aaa62013940`  
		Last Modified: Wed, 24 Apr 2024 22:05:48 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cb5699fa8ccc7a21de0b9f74f37dc8cb97e5316c31d74429cf73fa0b724bff`  
		Last Modified: Wed, 24 Apr 2024 22:05:48 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-22` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7fa1e6fd69ca74b32c74b5de2efb1282fe1568cb671d3a0bddefe780b8fe0eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230470056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d63b543ac14072c80c65ad0e23f44c1af2e31b847ce9e2df22351f08ea48089`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 14:25:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 28 Mar 2024 14:25:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 28 Mar 2024 14:25:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 28 Mar 2024 14:25:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ed6356befcb3f3e3f2dbe4ed0457e6f2e017191ad3f4f999da71660803fb42`  
		Last Modified: Tue, 16 Apr 2024 02:59:21 GMT  
		Size: 17.8 MB (17753415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c7c00a6bbbd321cd9413d399416da05e45fa855c65dda044f0318e737051`  
		Last Modified: Wed, 24 Apr 2024 18:02:41 GMT  
		Size: 154.7 MB (154738542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56297c614df7362f973f0fbdef0f15e85cfe0657d2464b2542d763ed698fae1`  
		Last Modified: Wed, 24 Apr 2024 18:02:32 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1830e08259efadc1579b8211eb357982609b98bfea278a366e25b7e4b1dacf7`  
		Last Modified: Wed, 24 Apr 2024 18:02:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b7a84db6f75948bbd91c6a070dcfce3eefc4d3b236856fe7af485979099ca`  
		Last Modified: Wed, 24 Apr 2024 18:57:15 GMT  
		Size: 20.1 MB (20095604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02938d01c6cfa34cd78409df43ca3a1ad26a817fea63313c9ad08583532f127`  
		Last Modified: Wed, 24 Apr 2024 18:57:13 GMT  
		Size: 9.5 MB (9479954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725bff816e558b66cb2d3a82562e75a2664770ded4b6c6c1d9f086b5d5d28f63`  
		Last Modified: Wed, 24 Apr 2024 18:57:12 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924fc78bb5fce0259788bc68eb89e8224307c57ebe5a5f3ed3aff516c3659290`  
		Last Modified: Wed, 24 Apr 2024 18:57:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d6918d9af585b47f74dbf0151a84b3043aafcec2a37e03170149e2cf01de7b`  
		Last Modified: Wed, 24 Apr 2024 18:57:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-22` - linux; ppc64le

```console
$ docker pull maven@sha256:62071a5900a5e8cddf930a83bfd5f8b832cd605efe1a3023ef51e8d9c97b9deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242576621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcdc8f5cd61ad607126134c797dc5cc05c07afb4989bb14bc9a1c21866ef3cd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 14:25:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 28 Mar 2024 14:25:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 28 Mar 2024 14:25:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 28 Mar 2024 14:25:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a859b671b1bd1453f092960bc3b3302cdd600e00a807b3a931c9bcb5103d97`  
		Last Modified: Tue, 16 Apr 2024 02:54:35 GMT  
		Size: 17.3 MB (17331532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ef4793dadbf5e41a6f1efe0979c8698c32341e6ac3ed155dc2ab0c1de10b4f`  
		Last Modified: Wed, 24 Apr 2024 17:51:35 GMT  
		Size: 156.7 MB (156695318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fdac5facfcbb3879b2f3f882a8f572950edc7e1d049dc824be2e86cc9e65dd`  
		Last Modified: Wed, 24 Apr 2024 17:51:19 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec22d5de37f0652d6f13dc26e6565637fbfc2809c46af36151d199f18d4cb07`  
		Last Modified: Wed, 24 Apr 2024 17:51:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6127bb7631e8658976118fbf929188bb9b6f7d389280e8e71255d36a34e1568`  
		Last Modified: Wed, 24 Apr 2024 18:44:32 GMT  
		Size: 23.5 MB (23480335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9972cae55a777c4120730d79f8a5fce9fb8a05beec4e991b588bfeccbf071042`  
		Last Modified: Wed, 24 Apr 2024 18:44:27 GMT  
		Size: 9.5 MB (9479940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc505b5e474965a0813b826c6303b313c747cbee8a737e0e091146227501774`  
		Last Modified: Wed, 24 Apr 2024 18:44:26 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a3a8ab96917988338f6690b392e88024f0f07c185b88d2b6f307c4e511dc05`  
		Last Modified: Wed, 24 Apr 2024 18:44:27 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91371315927a03f027721a28b5a1a3da5977cd84dc9ed562bcfe23a828845efb`  
		Last Modified: Wed, 24 Apr 2024 18:44:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
