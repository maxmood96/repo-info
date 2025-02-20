## `gradle:8-jdk17-noble`

```console
$ docker pull gradle@sha256:deb3ed64f189e9b326e4147de66335286eea9f8b6677e53514af62370cbf7a4a
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

### `gradle:8-jdk17-noble` - linux; amd64

```console
$ docker pull gradle@sha256:1dcc699a1915de771ca8e27771ef842f4b7e8aa0699e1dd9935e440334d7f9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.8 MB (399796290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3d99694b0608dc5ca650184f36a707c41d88a72b844080aae6516d34381c8f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 06 Feb 2025 02:49:08 GMT
CMD ["gradle"]
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Feb 2025 02:49:08 GMT
WORKDIR /home/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_VERSION=8.12.1
# Thu, 06 Feb 2025 02:49:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER gradle
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER root
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ff804eb32a079e6f9a54eb31c0f43d9d6c56fc09c7735ec59e2ad948fc6af6`  
		Last Modified: Tue, 04 Feb 2025 07:14:04 GMT  
		Size: 22.9 MB (22942779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5768705e3b7e7e3c61f95a6ed0478a61076d084e1adedfe24e09ce95d5c433`  
		Last Modified: Tue, 04 Feb 2025 07:13:40 GMT  
		Size: 144.6 MB (144576191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4fff2c206cae13745f200704b38134105ac3a4bcf862dc0d04d08f6aa9d2ce`  
		Last Modified: Tue, 04 Feb 2025 07:19:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2700d3f64bcbf1b67ccf65a715330aa34cb16c0c1e8c9146c15011233d6fc4`  
		Last Modified: Tue, 04 Feb 2025 07:13:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e037f8532411bf880dadcf993deb47817d04f5ff1ce96494e992894be26571b2`  
		Last Modified: Fri, 07 Feb 2025 09:20:00 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110845c6a320394011c51206cf93dc4745e4a968e59fa92913e69492ec85c9a1`  
		Last Modified: Fri, 07 Feb 2025 09:20:03 GMT  
		Size: 65.9 MB (65902437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58636d5a38d820cf718a5490ab95b48b40d4c72935892dc8873a5dfe709d13`  
		Last Modified: Fri, 07 Feb 2025 09:20:43 GMT  
		Size: 136.6 MB (136561917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742e68c63bd30c047cf01070feace8c87578a4a341133e8b6301d40a4817fb12`  
		Last Modified: Fri, 07 Feb 2025 09:20:00 GMT  
		Size: 54.9 KB (54919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:f393cda623ceda953348527de09736e1b366c42d6dbb89f6c65b63131dea88a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7142709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccf5de7788636c6a2d9d896326ee6ae3a5de2001365cb2246637cc6f7d0f461`

```dockerfile
```

-	Layers:
	-	`sha256:168163a38a3416d301a2190ddddcfba7cd44cc5388a90fc8b1a5a04cb0fe07e3`  
		Last Modified: Sat, 08 Feb 2025 04:00:39 GMT  
		Size: 7.1 MB (7119535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99278556ecb1d44ac9e03f6990e67489513991a317805df5a0444db1e146c188`  
		Last Modified: Fri, 07 Feb 2025 12:05:03 GMT  
		Size: 23.2 KB (23174 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-noble` - linux; arm variant v7

```console
$ docker pull gradle@sha256:635927b67a8d78b3560f2d408ee3808ce7cd2d9d601d2d7cceaf831f84b1511a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.1 MB (395054197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b717c5128f1bea2da5ed9d83420a3e7a770fd9a47170774ef75c889b1ad97fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:14 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:14 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:18 GMT
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Mon, 27 Jan 2025 04:14:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 06 Feb 2025 02:49:08 GMT
CMD ["gradle"]
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Feb 2025 02:49:08 GMT
WORKDIR /home/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_VERSION=8.12.1
# Thu, 06 Feb 2025 02:49:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER gradle
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER root
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Tue, 04 Feb 2025 08:31:36 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a5feca48d6d52ff9ef30651ab2fd330f7df213f49a2e8c1d802233ca080dc8`  
		Last Modified: Tue, 04 Feb 2025 23:24:31 GMT  
		Size: 21.4 MB (21372885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833c6bc8f928a67ecef0b46f949f694a60a7e196f6f0704a06a727e12abadfbc`  
		Last Modified: Tue, 04 Feb 2025 15:16:00 GMT  
		Size: 142.1 MB (142054855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396068d15b13caa66c2782b7168c539c408e5b5b1538cb708f9da8a8f00648de`  
		Last Modified: Tue, 04 Feb 2025 15:16:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa9004b1c56b65f3255b579cd72d29c9582472fb986711f92dff3ae1f0c3c6`  
		Last Modified: Tue, 04 Feb 2025 15:16:44 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16ab55b401f9c70b0978d4504592fc3cdc46cba56eed4dc12844288729f518`  
		Last Modified: Sat, 08 Feb 2025 04:00:39 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa8d0ab31afe0d4be64ff8433b1f814f9c2cc5213681704e6d08a414d5acda6`  
		Last Modified: Fri, 07 Feb 2025 12:05:33 GMT  
		Size: 68.2 MB (68185482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5eb6d26cafcf25a6814c632c3869920387695582ddcc1d0efa3462d1efa3f6`  
		Last Modified: Fri, 07 Feb 2025 12:05:49 GMT  
		Size: 136.6 MB (136561943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9883f44d33caedcaf4661294fd39377bc2c2082e4c3801241d10ba3ac0f8ef59`  
		Last Modified: Sat, 08 Feb 2025 04:00:39 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:a49aea9d6ca90b56cf4877e3d6e9280cd10960ea50007b69886a43918a0e6236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d31e7001acfcead46fa1fdbb56610a7594e22c411c5f635175e5d9563b6da20`

```dockerfile
```

-	Layers:
	-	`sha256:ccca5f3eb310f0025b40549151485e76bbc9b19b6c84aaf8e67a39234864bb6f`  
		Last Modified: Fri, 07 Feb 2025 12:05:53 GMT  
		Size: 7.1 MB (7058505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43ec6ba816d77bed1cf86bc29027ba0681566ab809bb3a2a5a4db148fa07a1c1`  
		Last Modified: Fri, 07 Feb 2025 12:05:54 GMT  
		Size: 23.3 KB (23319 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d2900e5708887206591172fe95df1d4bb88a206aab8ab452178afe29d7b6d990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398446743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7797831d91fa69e9f179cd3d77bc60c17465892e8c693925999f1be501ec4a7f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 06 Feb 2025 02:49:08 GMT
CMD ["gradle"]
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Feb 2025 02:49:08 GMT
WORKDIR /home/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_VERSION=8.12.1
# Thu, 06 Feb 2025 02:49:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER gradle
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER root
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc2f1e9953cd78876e5c047eaef6baf6407597113cd49d27cbee3d3eb57d11e`  
		Last Modified: Tue, 04 Feb 2025 11:31:15 GMT  
		Size: 24.2 MB (24153905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f5f70da64d3cfa33a66961fee477351b067301f124a76aec3532966a7fb1f8`  
		Last Modified: Tue, 04 Feb 2025 13:38:09 GMT  
		Size: 143.5 MB (143461842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b835032ff5a4a87eeb8c35796ca4985bc225bee2a303c6363d38dfbb8cc3004`  
		Last Modified: Tue, 04 Feb 2025 10:38:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08000320ad8b126a6e08ce05141beb6870c3289fbf0d83b0427c71da2e26200`  
		Last Modified: Tue, 04 Feb 2025 11:00:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3609b8a5e65e9adc035ae8b9d2419f179ef186c70e59a9ff56c057a5780486ee`  
		Last Modified: Fri, 07 Feb 2025 09:48:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b26e44964b1483465d8a116b6a3067b7d6849166a79cfb47e0b99299f4d23d`  
		Last Modified: Fri, 07 Feb 2025 09:48:35 GMT  
		Size: 65.3 MB (65312161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5623927161c38390228aa8d779b9a6492f695c78fd4544b1faf137072d90516e`  
		Last Modified: Fri, 07 Feb 2025 10:09:07 GMT  
		Size: 136.6 MB (136561942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adffffb01d86b26dbfe41209c870d8108fd7b81775fb83e800343bc7a180a8b9`  
		Last Modified: Fri, 07 Feb 2025 09:48:33 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:9f4a502404bf3a570b8adbe6368731c72ba18b423047bce97b130e24f3e64def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7280627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cca648e6878e4f17f17447eec26bd06e8fc0221033a3a5d04e3523fd6becc03`

```dockerfile
```

-	Layers:
	-	`sha256:f477a6d5a28028ad0fcadbb471988823ac0c2bac70360c5cf4252fc4d885cfcd`  
		Last Modified: Fri, 07 Feb 2025 12:06:42 GMT  
		Size: 7.3 MB (7257256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f82ce8fecff421300483662cd304d4bb2d5282f02fa5af2211a035b0bfeaafc`  
		Last Modified: Sat, 08 Feb 2025 06:36:11 GMT  
		Size: 23.4 KB (23371 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-noble` - linux; ppc64le

```console
$ docker pull gradle@sha256:107b3f0c37d01c80d88ba3fb3af6f21b4fb2cd8d0f6c1b5023a97c63f941125f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.5 MB (410539281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ef67854ff7840d53056192c5201e10db075690d7a9d0e8f8fd8a217ec37531`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 06 Feb 2025 02:49:08 GMT
CMD ["gradle"]
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Feb 2025 02:49:08 GMT
WORKDIR /home/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_VERSION=8.12.1
# Thu, 06 Feb 2025 02:49:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER gradle
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER root
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dd9d1b7ea01dff2ab580e6320a587b1adc67cea22a1f4d2e67127ca693646d`  
		Last Modified: Tue, 04 Feb 2025 16:14:01 GMT  
		Size: 24.1 MB (24107411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b935de70b38f6190f9e9edf6b409ffe906868fe431405592a2f5ffc916c991`  
		Last Modified: Tue, 04 Feb 2025 17:22:08 GMT  
		Size: 144.2 MB (144219941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f048f8a18afbd7593ac0f1982333c47d71cfe39c1909972382be413e96fafe`  
		Last Modified: Tue, 04 Feb 2025 16:26:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e059096bbd194b86c37274409ecff5a58c8ab3f2f843f0fc6e6486f199b7b5`  
		Last Modified: Tue, 04 Feb 2025 20:44:09 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a48d0dbf712d9de070f11303d7c63d516229e64aee70c9af5de68a5e0e3f3`  
		Last Modified: Sat, 08 Feb 2025 04:00:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a493b06395ae288035577fb9ed80696912855f4be0f3e414950791ebbbecb018`  
		Last Modified: Fri, 07 Feb 2025 12:07:16 GMT  
		Size: 71.3 MB (71256105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91978a927f769f34e4fbb44145d8f7f54ac87cb1b8953471b1f30b54ba31d12`  
		Last Modified: Fri, 07 Feb 2025 12:07:38 GMT  
		Size: 136.6 MB (136561941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f1e36c364144e3cc51850947f1392116117d72b040688b7937edac425f2ad2`  
		Last Modified: Sat, 08 Feb 2025 04:00:41 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:c02fd1cc9552537277e4976aa645ef121c53437c177705f6589e403eafe94206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d7c34bc76de6b85c830719188ee6172145af28e4914215c0c8f218f8710242`

```dockerfile
```

-	Layers:
	-	`sha256:b5e0adeb978c25f172730b2dd7ebbad8c964ddd12fdafefa5e10d3638bcc8a41`  
		Last Modified: Sat, 08 Feb 2025 06:47:40 GMT  
		Size: 7.2 MB (7170879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e0c12b75a9d1b60d2495e5ff202283991451e0e48a3b72ae513655791e456b4`  
		Last Modified: Fri, 07 Feb 2025 12:07:42 GMT  
		Size: 23.2 KB (23246 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-noble` - linux; riscv64

```console
$ docker pull gradle@sha256:e75d8fd7032c87bfc9c6e540d7278b6a3067a51e0231b72174bdb21e84ccf5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.0 MB (399965842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77187b037fd637ff2197d0dc0ba7f5297736c54bec26e84b45ef6da808cb7a5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 27 Jan 2025 04:46:38 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:46:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:47:10 GMT
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Mon, 27 Jan 2025 04:47:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Wed, 19 Feb 2025 02:55:56 GMT
CMD ["gradle"]
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 19 Feb 2025 02:55:56 GMT
WORKDIR /home/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_VERSION=8.12.1
# Wed, 19 Feb 2025 02:55:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER gradle
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER root
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Tue, 04 Feb 2025 07:00:41 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a116124a0e7b20219e18554d3546d2013703e5da91b9df632ebcd5e027f6af4`  
		Last Modified: Tue, 04 Feb 2025 22:04:05 GMT  
		Size: 20.1 MB (20135431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a5a118bdeaf726687041177a60f88ac756ae930a777e38b432687113ba20e`  
		Last Modified: Tue, 04 Feb 2025 19:04:29 GMT  
		Size: 138.4 MB (138437583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cc4ae66fc71e58d63974f1129907240137a19c2184aed63e360e8599e16ff0`  
		Last Modified: Wed, 05 Feb 2025 05:43:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feca01857b497f12c8c5d068ef46bad5efb49fdc819d84a213285db3d23415e2`  
		Last Modified: Tue, 04 Feb 2025 15:02:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788010f1bbdae77acccfb136f14b89e035047cdab51f26d8f10fbe2927297c46`  
		Last Modified: Wed, 19 Feb 2025 21:50:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d895d35aa528a4743a95c233a6a0dd639b6058eb0080380a3100c33fdc9983b`  
		Last Modified: Wed, 19 Feb 2025 21:50:49 GMT  
		Size: 73.8 MB (73842915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b12dd437935212195b37348ba2d5a83fe25feb33ecc20b7cabac26cea72603`  
		Last Modified: Thu, 20 Feb 2025 04:01:08 GMT  
		Size: 136.6 MB (136561942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62152d0ef6bdeff48b1bc06d0955e79de362e6e6dd286066fc88351c0b7647d8`  
		Last Modified: Wed, 19 Feb 2025 21:50:27 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:35e05a1eb959775eaa7782a6298f41566d3817ed153db6ceb9309332fe9d4c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7245163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5d5956140c489d069ddf9167d4ac157a83d5b645f7bc01b4f2f223c7c1fb56`

```dockerfile
```

-	Layers:
	-	`sha256:70667c36f367b4d1e29180f3dc72bd61486ae426a754b87d7c24ef7a85535000`  
		Last Modified: Thu, 20 Feb 2025 00:35:16 GMT  
		Size: 7.2 MB (7221917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6824943d31ae14378e8f469f4a0b1f6b79a87b2d66360fef050bbd3099688383`  
		Last Modified: Thu, 20 Feb 2025 00:35:16 GMT  
		Size: 23.2 KB (23246 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-noble` - linux; s390x

```console
$ docker pull gradle@sha256:9d4a53dbad024c382baa4f74d408da4c53ce025091d5431d27625ad8195d8d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.2 MB (391154738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaa1fd410925da2318fe24287d3fe785fa467ff5c30d926ba180a3d81e5fb4e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 27 Jan 2025 04:15:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:15:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:15:20 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Mon, 27 Jan 2025 04:15:20 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 06 Feb 2025 02:49:08 GMT
CMD ["gradle"]
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Feb 2025 02:49:08 GMT
WORKDIR /home/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_VERSION=8.12.1
# Thu, 06 Feb 2025 02:49:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER gradle
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER root
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Tue, 04 Feb 2025 08:21:20 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e861bff15ace5229469756101c0dfe916c9eb38c8a5cd02670f910ae5f61ca43`  
		Last Modified: Tue, 04 Feb 2025 22:48:27 GMT  
		Size: 22.1 MB (22132598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66edfe61b7bee16cfe328c7c38f7e2bff79edcdacf57f6b0b978ced78df727b`  
		Last Modified: Wed, 05 Feb 2025 01:05:30 GMT  
		Size: 134.6 MB (134623288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d432f939d5dba41c58721164d5612144df12ed5f24b53cf8538d16028d364a4`  
		Last Modified: Tue, 04 Feb 2025 17:30:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b6199f471cb128d3009b41eb5f6bedeb97eeba0612c58a6e0a5e35b280d6d8`  
		Last Modified: Tue, 04 Feb 2025 16:10:10 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b839457d312e16ea579670356acfce948f89a5091a8c95666ea0bf2f354bfa6b`  
		Last Modified: Mon, 10 Feb 2025 16:35:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a674c50b0118175bfabcecf40c81f28d339e9e5d3f8ba42b958250a06b9c6ea2`  
		Last Modified: Fri, 07 Feb 2025 12:08:17 GMT  
		Size: 67.8 MB (67805302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ac705eac832645bc20434e9870f94a48fef8bc907736abde3c65a47405a40`  
		Last Modified: Mon, 10 Feb 2025 16:35:07 GMT  
		Size: 136.6 MB (136561941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a248b4e234b26f3e1329946b927d29c07f29bcc295d29766596aa157d4f94a`  
		Last Modified: Fri, 07 Feb 2025 12:08:38 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:d896131bbbb103d67e2a09206c651f768eeef221b7b9cd845aa0681449091170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7088414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad9e5c4ac10c628733a6e7bebe6466d0d50aa9397148a4bf3b309249d8c220`

```dockerfile
```

-	Layers:
	-	`sha256:c5293356c78343e90f8dbf6fcd8f22093ba79949d1f056a0c1cfe172c1927ef1`  
		Last Modified: Sat, 08 Feb 2025 06:58:44 GMT  
		Size: 7.1 MB (7065242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61c16ba918c91f6c03c0beb2fe1169361c14db09d5258c7887421ff7dde3986`  
		Last Modified: Fri, 07 Feb 2025 12:08:40 GMT  
		Size: 23.2 KB (23172 bytes)  
		MIME: application/vnd.in-toto+json
