## `gradle:8-jdk8-focal`

```console
$ docker pull gradle@sha256:6114956713a5797033088405320f6e25beb69e4fd0712e61deae32378c7d5c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:8-jdk8-focal` - linux; amd64

```console
$ docker pull gradle@sha256:8364f2bade9cf601ee46f07e96a61b9d2773ff2016c0cbd2a47c5e186fcd698d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.1 MB (347121272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8bd6d289ea54966daece05b7b58b234979bbf992f6ffccf2bb091145ad755f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:31:16 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 20:31:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 24 Jan 2024 20:31:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 25 Jan 2024 19:31:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 19:31:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 23:01:18 GMT
CMD ["gradle"]
# Thu, 25 Jan 2024 23:01:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 25 Jan 2024 23:01:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 25 Jan 2024 23:01:19 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 25 Jan 2024 23:01:19 GMT
WORKDIR /home/gradle
# Thu, 25 Jan 2024 23:02:26 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 25 Jan 2024 23:02:27 GMT
ENV GRADLE_VERSION=8.5
# Thu, 25 Jan 2024 23:02:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Thu, 25 Jan 2024 23:02:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 25 Jan 2024 23:02:32 GMT
USER gradle
# Thu, 25 Jan 2024 23:02:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 25 Jan 2024 23:02:34 GMT
USER root
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e04bb698dc078030e24e6a5241678fca5fd8aa1a009a2ca3ddbd537f187eba`  
		Last Modified: Wed, 24 Jan 2024 20:40:13 GMT  
		Size: 103.6 MB (103603243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3691da2cfaf479170639ab8e455e909e6a6ef2966f18aadcef9d6f2e4a9e4f0f`  
		Last Modified: Wed, 24 Jan 2024 20:40:05 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a456afd5bd8db6d9456e209a6435ae1d76d1ae586efb50257dd29b8680f96d1e`  
		Last Modified: Thu, 25 Jan 2024 19:34:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eff38068bc6c481d0906b07f0ea921387d371e4066b8363f2830e8c6dd10428`  
		Last Modified: Thu, 25 Jan 2024 23:09:51 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab265a833300fba1125d5caa64a004bce3f22a0297705880ba23bc00639ad2d`  
		Last Modified: Thu, 25 Jan 2024 23:10:01 GMT  
		Size: 65.5 MB (65463703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeef658f1f8690819d3465b556cd76e50c8f2a8a071504294d21fbb34a6f364`  
		Last Modified: Thu, 25 Jan 2024 23:09:58 GMT  
		Size: 132.5 MB (132544677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4828936788f54e6b7d5ea74262477b7fc117e09dc5e223da97a9d80a6fa0ba`  
		Last Modified: Thu, 25 Jan 2024 23:09:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:8-jdk8-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:7e4e4950fbbf6ba19d708be89abe532efc007e03238e2ccaaa82b93b13fd1e26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.1 MB (332138644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cfe0c1c7c726b19a6ef052f8637862407caf665f2e93ee1aa8e551dcf266ae`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:39:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 23:39:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 23:39:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 23:40:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:40:12 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 01 Feb 2024 23:40:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Feb 2024 23:40:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 01 Feb 2024 23:40:24 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 01 Feb 2024 23:40:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 00:50:25 GMT
CMD ["gradle"]
# Fri, 02 Feb 2024 00:50:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Feb 2024 00:50:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Feb 2024 00:50:26 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Feb 2024 00:50:26 GMT
WORKDIR /home/gradle
# Fri, 02 Feb 2024 00:51:23 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 02 Feb 2024 00:51:24 GMT
ENV GRADLE_VERSION=8.5
# Fri, 02 Feb 2024 00:51:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Fri, 02 Feb 2024 00:51:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 02 Feb 2024 00:51:32 GMT
USER gradle
# Fri, 02 Feb 2024 00:51:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 02 Feb 2024 00:51:35 GMT
USER root
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972e83713c2c5331099c3dd566b25ba1fbeb2eb2f765f916ef9c22e030e22b26`  
		Last Modified: Thu, 01 Feb 2024 23:45:08 GMT  
		Size: 15.7 MB (15663395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a9970024c4fc0591bbd4d50e73db50ff65e623c32c0dbc117abc0067b8083`  
		Last Modified: Thu, 01 Feb 2024 23:45:14 GMT  
		Size: 99.2 MB (99231891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0203f9ed27192fbd21a514e449395e08bbdef3a4d2c19a5881e0c89985276f62`  
		Last Modified: Thu, 01 Feb 2024 23:45:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a0ee1b2d7eb0f14cc84935a132dcc9537cfbf141b046bc24cb9900b8e9a781`  
		Last Modified: Thu, 01 Feb 2024 23:45:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ea4f2ff8671c551de8709b300c93bee5cb9f3996ecfa25ea2d81c78e6db06`  
		Last Modified: Fri, 02 Feb 2024 01:01:07 GMT  
		Size: 4.4 KB (4351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e47a33b3203673695a2da2c928586c0eb13160c0aec6531cfb97b779e375099`  
		Last Modified: Fri, 02 Feb 2024 01:01:30 GMT  
		Size: 60.1 MB (60090918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff9ca12f4d1e58a32417e98b8dc95b47d067c884062b3a510b15bca1001d10c`  
		Last Modified: Fri, 02 Feb 2024 01:01:23 GMT  
		Size: 132.5 MB (132544682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72363b2bfb758dc1f62352f90973de4789a61d991c6a75bb617e3b3815a584d1`  
		Last Modified: Fri, 02 Feb 2024 01:01:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:8-jdk8-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:64c600424e4e0a5b2392600560d0a51ea54aadc13e3bd6c911922927252e0084
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344459919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3fb0ca999d729b95a65e22223872bd895aee1721425f95cd000dfb62495988`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:39:34 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 20:39:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 24 Jan 2024 20:39:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 25 Jan 2024 19:39:33 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 19:39:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 22:42:09 GMT
CMD ["gradle"]
# Thu, 25 Jan 2024 22:42:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 25 Jan 2024 22:42:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 25 Jan 2024 22:42:09 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 25 Jan 2024 22:42:09 GMT
WORKDIR /home/gradle
# Thu, 25 Jan 2024 22:42:48 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 25 Jan 2024 22:42:50 GMT
ENV GRADLE_VERSION=8.5
# Thu, 25 Jan 2024 22:42:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Thu, 25 Jan 2024 22:42:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 25 Jan 2024 22:42:54 GMT
USER gradle
# Thu, 25 Jan 2024 22:42:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 25 Jan 2024 22:42:55 GMT
USER root
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92d063a596b094c98c056d4e8b04e613020c4bbf415c675eebdb31705314036`  
		Last Modified: Wed, 24 Jan 2024 20:46:18 GMT  
		Size: 102.7 MB (102707135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65df2d28723646346952fac0cea8530ebe9293e3a6dd610342986dd4608532ba`  
		Last Modified: Wed, 24 Jan 2024 20:46:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cd9d21d04ab964524a6e9242f30a8f38936d287d57fe2acc77b22e5f05c162`  
		Last Modified: Thu, 25 Jan 2024 19:41:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb586eadf448903a27f77b7592fb69dff717e76c1ff91fe0bd4cf9cea767dd`  
		Last Modified: Thu, 25 Jan 2024 22:48:43 GMT  
		Size: 4.4 KB (4370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d08be4c9775570174bc4592645baba704df73b9d60e2f2a3b5ef0261374a260`  
		Last Modified: Thu, 25 Jan 2024 22:48:51 GMT  
		Size: 65.2 MB (65230482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e77cbe09adf3b0a15bb089166adbafc343a04e229806815112f84f1953df15d`  
		Last Modified: Thu, 25 Jan 2024 22:48:48 GMT  
		Size: 132.5 MB (132544694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262c855328cf3e8e6cdc07e84fe265a593025af34eb9a960d4f2514e21600f77`  
		Last Modified: Thu, 25 Jan 2024 22:48:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:8-jdk8-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:4acdce6dbaef2e36cf20414f134e30e43fb393d267788fe09adc2328619b9952
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (358985241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe5414ace1653d591c3e4f1905135f9d8f936bfe5c24a1ca798114e6a05df54`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:36:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:36:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:36:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:37:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:27 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 20:33:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 24 Jan 2024 20:33:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 25 Jan 2024 19:25:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 19:25:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 19:47:55 GMT
CMD ["gradle"]
# Thu, 25 Jan 2024 19:47:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 25 Jan 2024 19:47:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 25 Jan 2024 19:48:00 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 25 Jan 2024 19:48:01 GMT
WORKDIR /home/gradle
# Thu, 25 Jan 2024 19:49:07 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 25 Jan 2024 19:49:11 GMT
ENV GRADLE_VERSION=8.5
# Thu, 25 Jan 2024 19:49:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Thu, 25 Jan 2024 19:49:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 25 Jan 2024 19:49:22 GMT
USER gradle
# Thu, 25 Jan 2024 19:49:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 25 Jan 2024 19:49:25 GMT
USER root
```

-	Layers:
	-	`sha256:3cdeaacd390f730da6f0fb692f91fa6acafd7c373cd75524447a25371b6cf3b5`  
		Last Modified: Sat, 16 Dec 2023 10:34:06 GMT  
		Size: 33.3 MB (33314320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed67c1e92d231797f6ccdb5b8dfc66523da0505bda01ed804febc7f69bbc165`  
		Last Modified: Sat, 16 Dec 2023 10:43:55 GMT  
		Size: 18.2 MB (18215112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130b42b60a381135f1d4829948d753059545774d1d2ececb93e9563254769780`  
		Last Modified: Wed, 24 Jan 2024 20:47:32 GMT  
		Size: 101.1 MB (101070874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31cfc0fe2560f7fe4a5265b70da2d243887dc453e6a9785bae844411a4dde63`  
		Last Modified: Wed, 24 Jan 2024 20:47:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b00bb3cce5d3738b3cfdb31f1e44c6076ed0f166190a00f111950031b881d63`  
		Last Modified: Thu, 25 Jan 2024 19:27:59 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50619e85e7a227cc2aff9f2115e7339fdd3cd3676b1483a7a480cc0a638f6849`  
		Last Modified: Thu, 25 Jan 2024 20:01:06 GMT  
		Size: 4.4 KB (4377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af00cd3460e47a83028b859ae28fa7cc6f5727a5c6e5cb8921576798ce17cec`  
		Last Modified: Thu, 25 Jan 2024 20:01:19 GMT  
		Size: 73.8 MB (73834829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa8ab818a4ecfe2d995d16b4fc0ab53f4161bbeaebdd73b4ccd21d1b91f4a8e`  
		Last Modified: Thu, 25 Jan 2024 20:01:13 GMT  
		Size: 132.5 MB (132544665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc031f6847234e19c3add8a79f90972869dde51b8fd601d975d93e1f2f156fb`  
		Last Modified: Thu, 25 Jan 2024 20:01:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
