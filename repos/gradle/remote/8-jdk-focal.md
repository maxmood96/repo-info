## `gradle:8-jdk-focal`

```console
$ docker pull gradle@sha256:ba7cf4cc61a30628d3ec8dd911e1b4bc351c61640ca2919af3d1c477e37b5d1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:8-jdk-focal` - linux; amd64

```console
$ docker pull gradle@sha256:99f7f21caee066499e9780485870765f22d9e12722d7b1159f896b78a18415aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (397950474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea519214b32f9770781527a8b3a13831a715ca9483c6a29286fe540f6a1559e0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER root
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a561288a64ce04c955cc2a899047873e9859e9750d9b10ca9fef14fd39c7333`  
		Last Modified: Thu, 02 May 2024 01:17:47 GMT  
		Size: 20.7 MB (20672110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bef26252a16bb42ac04415cbc6e61961698aefb6ff84300b0f59e4a0cb1969f`  
		Last Modified: Thu, 02 May 2024 01:17:56 GMT  
		Size: 145.1 MB (145102851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d4271e3e0ec1020bbb6707004968ed42f985445aabe248cd1e9144881ee37e`  
		Last Modified: Thu, 02 May 2024 01:17:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54303d91da2f1dce9bea715a3782e60576a9e02e5151cf7451e22de0324dd7a2`  
		Last Modified: Thu, 02 May 2024 01:17:44 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1904f92f853d9d2aefe7d333b7b5155fe392c6cacd96d989eb6bab9b6d9e23`  
		Last Modified: Mon, 03 Jun 2024 19:00:58 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20f1cb11adcd20a9a377a260ea0ecfb5c139519506068afcd1e595afc958c2b`  
		Last Modified: Mon, 03 Jun 2024 19:00:59 GMT  
		Size: 65.5 MB (65468496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632e7e7f32ba4a06c3186e21fc03dd34d27bcd420f849e98577bc86c97d4924d`  
		Last Modified: Mon, 03 Jun 2024 19:01:01 GMT  
		Size: 138.1 MB (138062554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8de4bc2beaeef1c804c29e3bd314b465df4389dada0093f0a146ec7eb5168d`  
		Last Modified: Mon, 03 Jun 2024 19:00:58 GMT  
		Size: 54.9 KB (54911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:0629372cb44a26a40ee2f49279dc59c53ec2109c10a24ae086b35d064a24f3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05c8f0d72e7158240237b867572e5fcae65a56bbbaf3564efba4867815a19c9`

```dockerfile
```

-	Layers:
	-	`sha256:c266fd543c1a1157afb3d5c0c4446f7d809c8d1f38adf4a475936cb2304f9d4a`  
		Last Modified: Mon, 03 Jun 2024 19:00:58 GMT  
		Size: 7.5 MB (7513330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:297ed9c62fc4311e0377a1d4ce64f9e4193eaf9a32bebbb190882ffa64d88402`  
		Last Modified: Mon, 03 Jun 2024 19:00:58 GMT  
		Size: 24.1 KB (24080 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:b99e3f3d8e2532580d808efee32254e665f857c486a7b449f41c6362ef28583d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 MB (381534199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57557fbb26fa28b9f0f13328535a55593ca00408e90a410f723744a07eb302ec`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 23 Mar 2024 20:25:42 GMT
ARG RELEASE
# Sat, 23 Mar 2024 20:25:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 23 Mar 2024 20:25:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 23 Mar 2024 20:25:42 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 23 Mar 2024 20:25:42 GMT
ADD file:5789980ed37544805bfc38f68255149cf4ceac7689ffcbcf606720b1b7170733 in / 
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["/bin/bash"]
# Sat, 23 Mar 2024 20:25:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 23 Mar 2024 20:25:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Mar 2024 20:25:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["jshell"]
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["gradle"]
# Sat, 23 Mar 2024 20:25:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 23 Mar 2024 20:25:42 GMT
WORKDIR /home/gradle
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENV GRADLE_VERSION=8.7
# Sat, 23 Mar 2024 20:25:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
# Sat, 23 Mar 2024 20:25:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
USER gradle
# Sat, 23 Mar 2024 20:25:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
USER root
```

-	Layers:
	-	`sha256:8bc6554297d271d6d4b2d1b92b5a4a9fc067e28e04c1d749f5fa99295fe0b1d9`  
		Last Modified: Thu, 02 May 2024 01:27:40 GMT  
		Size: 24.6 MB (24604686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1636df51260ebf7f03f89a36d83bec3b6e8f69b439e3dda92bb3bc53f0a856`  
		Last Modified: Thu, 02 May 2024 01:30:04 GMT  
		Size: 20.0 MB (19958354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ddb1a1a771b27d56a914a62480dcc69b7f16382c6e9d37fb6f26bbbe962c24`  
		Last Modified: Thu, 02 May 2024 01:30:14 GMT  
		Size: 142.6 MB (142579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c65bdcc26256a81f8c198532c9ae1032d2a36505f313af93e3ee7c8135e88a2`  
		Last Modified: Thu, 02 May 2024 01:30:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5a873fc91ade4af87a6bde724812c4c73e0c5c3c19467991d5ea2757e140f0`  
		Last Modified: Thu, 02 May 2024 01:30:01 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0b008d7a23f5226b833289bfaa42be302127846da6fbd6712373eaaaa0ec47`  
		Last Modified: Thu, 16 May 2024 21:40:14 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d3aa0ea7e4ceb2e65e245f39b573e6cefe7e7ff786ac7b9751bc34e93ea0b`  
		Last Modified: Thu, 16 May 2024 21:40:16 GMT  
		Size: 60.1 MB (60145310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5e2cd754171ec7b42139a3ba9ede98c5efdc65404411bf80d27673cfcfd938`  
		Last Modified: Thu, 16 May 2024 21:40:18 GMT  
		Size: 134.2 MB (134210007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd42514750bd36274031db88c50b1a36183d7b7c8b45f7eb267bb9b2022ae549`  
		Last Modified: Thu, 16 May 2024 21:40:15 GMT  
		Size: 31.3 KB (31295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:a19244769eb4a07e457afa86fbc919378df0b9f2258419060fb37907c9a09071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7457562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50f36d2acf25abf33c1942912ee3f2d11d43d08e6f3e0a56fb0a218190168ba`

```dockerfile
```

-	Layers:
	-	`sha256:138688fc942eaa640f972c33319f7fbf1c24749023987fc38daec3d61314e575`  
		Last Modified: Thu, 16 May 2024 21:40:13 GMT  
		Size: 7.4 MB (7432491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0445ec74a8f71c23d0b9dcaa97d5186ede9ddff017cfede86ff996712e90ed0`  
		Last Modified: Thu, 16 May 2024 21:40:12 GMT  
		Size: 25.1 KB (25071 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1add89813a7d049c1fc29a300e38216e5cfb1f5eaac9c78003edf2c4728c8c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.0 MB (392021441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4077abe17e336fd134eb329c3dd88a247f192525a469dc95e1ebe55f9add0ac7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 23 Mar 2024 20:25:42 GMT
ARG RELEASE
# Sat, 23 Mar 2024 20:25:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 23 Mar 2024 20:25:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 23 Mar 2024 20:25:42 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 23 Mar 2024 20:25:42 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["/bin/bash"]
# Sat, 23 Mar 2024 20:25:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 23 Mar 2024 20:25:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Mar 2024 20:25:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["jshell"]
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["gradle"]
# Sat, 23 Mar 2024 20:25:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 23 Mar 2024 20:25:42 GMT
WORKDIR /home/gradle
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENV GRADLE_VERSION=8.7
# Sat, 23 Mar 2024 20:25:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
# Sat, 23 Mar 2024 20:25:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
USER gradle
# Sat, 23 Mar 2024 20:25:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
USER root
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea79202db79da3bd9ee6809f42ca3ba5eee228dfcbe1a0b240b898b3a991a63`  
		Last Modified: Thu, 02 May 2024 04:19:26 GMT  
		Size: 21.4 MB (21375620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f17299686fe3d852e8e484fabdfbd4565233be6f8e2a876e00afae3eda5f06`  
		Last Modified: Thu, 02 May 2024 04:19:32 GMT  
		Size: 143.9 MB (143897010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5272442066df5d8cbbf4ff6e100f3871fd7eba368467d4a38215ab1ca39ed4d8`  
		Last Modified: Thu, 02 May 2024 04:19:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d769917d6209b484682591b021afab8ef9f901252031daf0e696ab86534a0c`  
		Last Modified: Thu, 02 May 2024 04:19:23 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb67c1b4ba7858d4279d22ac39b41b2207129928c52d7561755a38e2d8670dd7`  
		Last Modified: Fri, 17 May 2024 00:32:38 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec313547af3ba8cd1f7eb1aec788075e3b9158afd3fd362d2a06ef1b89e20a24`  
		Last Modified: Fri, 17 May 2024 00:32:41 GMT  
		Size: 65.3 MB (65267904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e9a38bef58a14be02161bd89c19d2f0b804ae1deb4a6a45474ca959e92f45d`  
		Last Modified: Fri, 17 May 2024 00:32:43 GMT  
		Size: 134.2 MB (134209990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cbc9bf2501af0f757294401b40da4925f197d5558d2247bfd0efc68439940f`  
		Last Modified: Fri, 17 May 2024 00:32:39 GMT  
		Size: 59.5 KB (59521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:e632b620dc2b89fd31e04607857696c6e2370da70e2018ae1bef59444af20277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804631834d1cf9af4331f9c63edf93dac98db135a96a5ccd66a3a5992978ff74`

```dockerfile
```

-	Layers:
	-	`sha256:905ae5f7659c3ce7e27227ecb5dcd29cb55fe7a47a99ecd0cedf84ea83572a60`  
		Last Modified: Fri, 17 May 2024 00:32:38 GMT  
		Size: 7.6 MB (7613153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f39dd751f920bfc5c9edebccf5068d8d8c7eb7fd2e9fce56012448d2e746468`  
		Last Modified: Fri, 17 May 2024 00:32:37 GMT  
		Size: 24.1 KB (24106 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:56f223253a496a2a60d477f9465634448dfe164da084b7fff90e37ab31d1042c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.9 MB (408911708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9513a377758552b54ecef7bdff4f37fe29299c87c62774e7eb151dd10f9dde7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 23 Mar 2024 20:25:42 GMT
ARG RELEASE
# Sat, 23 Mar 2024 20:25:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 23 Mar 2024 20:25:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 23 Mar 2024 20:25:42 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 23 Mar 2024 20:25:42 GMT
ADD file:de463dcd7b30faec6d782106816b443697c99747238015d4d992786da4888987 in / 
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["/bin/bash"]
# Sat, 23 Mar 2024 20:25:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 23 Mar 2024 20:25:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Mar 2024 20:25:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["jshell"]
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["gradle"]
# Sat, 23 Mar 2024 20:25:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 23 Mar 2024 20:25:42 GMT
WORKDIR /home/gradle
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENV GRADLE_VERSION=8.7
# Sat, 23 Mar 2024 20:25:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
# Sat, 23 Mar 2024 20:25:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
USER gradle
# Sat, 23 Mar 2024 20:25:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
USER root
```

-	Layers:
	-	`sha256:842f501e2541cf3af2b2c183cb8bc0e8ee178240b7a31e44ca04a5741c69410b`  
		Last Modified: Thu, 02 May 2024 01:51:19 GMT  
		Size: 33.3 MB (33316011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692945d393e71447ba077b664c21927d93361a3442474008a223f01cb1708c9`  
		Last Modified: Thu, 02 May 2024 01:53:57 GMT  
		Size: 22.7 MB (22716109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c1060363c9262d0c9273d48bede8df3a251307b1ce14dd09e296dd98333f5f`  
		Last Modified: Thu, 02 May 2024 01:54:04 GMT  
		Size: 144.8 MB (144794525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25413a2838302b99b09681ef95359ffe7c3cadb9c27cc275d715e697bbd87118`  
		Last Modified: Thu, 02 May 2024 01:53:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfd7a7a66e2cc8e119cb4464b65180f8f3d6addb53783309d265d4cde602379`  
		Last Modified: Thu, 02 May 2024 01:53:50 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc1126621202026311d53b68b16e88ddc6af460aa31cb7644040f1a2a5a8296`  
		Last Modified: Thu, 16 May 2024 21:31:53 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5750e0f428f452aa1f6a1b1d435c27fd88a8209477032bf92e53811c7380fc01`  
		Last Modified: Thu, 16 May 2024 21:31:57 GMT  
		Size: 73.8 MB (73834806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ee8e36f7375dc7bbed63748ebfc5d80bbe3311599b074a8d48e8cd9a2df78b`  
		Last Modified: Thu, 16 May 2024 21:31:59 GMT  
		Size: 134.2 MB (134210007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f09c13329c16cdf70362f608f58434b049af894a0dc0101f06f2bae1368544c`  
		Last Modified: Thu, 16 May 2024 21:31:55 GMT  
		Size: 35.0 KB (34997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:3b890d08acd809bc42aa6644cb4b13558e1741e60e56c1eb3f81018f42e29109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896459a2a66821143b5cf01f003ff6f2ec54514eccbf729e1dda259b50db328b`

```dockerfile
```

-	Layers:
	-	`sha256:6a865c758f539780966f574e954efd780466a5ad19da9c6a359f5f0ed4748e78`  
		Last Modified: Thu, 16 May 2024 21:31:53 GMT  
		Size: 7.5 MB (7544135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a06753c32656b7fe6a8719c30cfca1c1660eb6160e41cca1729632157a270a9d`  
		Last Modified: Thu, 16 May 2024 21:31:53 GMT  
		Size: 25.0 KB (24990 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-focal` - linux; s390x

```console
$ docker pull gradle@sha256:d68d1c2c68c3225ba858514d9d3f2507f5e1e283dfc38f2ac80bff3763bc7d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384366414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f73ec8cd0cd9ee82ebcf4147501d4a928db17cad6672647c011b7abcbe4c5f1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 13:33:19 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:33:19 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 13:33:21 GMT
ADD file:437329bc1595e1f595679a14cae312da49f4465fe0b6b7263e2831d77736f05d in / 
# Sat, 27 Apr 2024 13:33:21 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER root
```

-	Layers:
	-	`sha256:02df2f6f6361f3c4f25f62963fc222c930e83f14680ca06800140ca2374bc723`  
		Last Modified: Thu, 02 May 2024 01:33:18 GMT  
		Size: 27.0 MB (27013559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eee2ef7bfc92d6e8feebf03bfacacbc449c63abdd61e07021096955d893673`  
		Last Modified: Thu, 02 May 2024 01:45:43 GMT  
		Size: 20.1 MB (20142013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97c22ef716366492cb531021f111df350c0860a749d23b23ef09216a78a2567`  
		Last Modified: Thu, 02 May 2024 01:45:51 GMT  
		Size: 134.3 MB (134336984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a799b4392c867f5af90e794af1e14cb2544e27be5202b1b75cd8c084a50d4fe0`  
		Last Modified: Thu, 02 May 2024 01:45:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b43ce858328cf1fe04b818d296b07038b0343d8a25ed94dcaa33b562ee7af`  
		Last Modified: Thu, 02 May 2024 01:45:40 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a87a838339b3b3b3cd946772cd1767fa5c958be985adafbdfdf795a41eecc9`  
		Last Modified: Mon, 03 Jun 2024 19:36:55 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a4a8c334a51f37007dee8640a54eecead69e8daeb0242ef0e6ae5af5f446d`  
		Last Modified: Mon, 03 Jun 2024 19:36:57 GMT  
		Size: 64.8 MB (64805768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b976da071ab70a2cf40444a4b660ac0dac3c61924b1313deaed5f045e4d8a321`  
		Last Modified: Mon, 03 Jun 2024 19:36:58 GMT  
		Size: 138.1 MB (138062551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ac276efd8beffe29485835894c0a4002417bd36fd077791e2a2c155e98b48b`  
		Last Modified: Mon, 03 Jun 2024 19:36:55 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:109dd045b0087510016f320c3b36a5ac837b92e5833cf2795f29dc87751287bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909aa6159cfd7bfff6d0d163efd4814959da1d8ccdc7e4b55c084af6c4e61ecb`

```dockerfile
```

-	Layers:
	-	`sha256:dce1ee2296fdae7ddb6a34fbacbce949b03704ab887e735fbdb347979a4af59e`  
		Last Modified: Mon, 03 Jun 2024 19:36:56 GMT  
		Size: 7.4 MB (7440094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f3d50091143df73c130e7b33be0559f8ef1dd11b0cc6c3cf4270f05c41ae6`  
		Last Modified: Mon, 03 Jun 2024 19:36:55 GMT  
		Size: 24.1 KB (24078 bytes)  
		MIME: application/vnd.in-toto+json
