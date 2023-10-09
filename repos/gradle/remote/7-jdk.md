## `gradle:7-jdk`

```console
$ docker pull gradle@sha256:c9be33dbbf9b692b0f36e4b832a1f1022a6876e03c1bdf369f21c2311bab1a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:7-jdk` - linux; amd64

```console
$ docker pull gradle@sha256:be61b109e3f1d5a7d42e8aa593df7cfc53ca9989e0ee9b4d36896fb1fb380b2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366583577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4658e98e5c694e5d142c9079207cba32e464d2a9caff5624ff87df5d3638aa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:11:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 05:11:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 05:11:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 05:13:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:13:30 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 05:13:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 05:13:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 05:13:41 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 05:13:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 05:13:41 GMT
CMD ["jshell"]
# Tue, 03 Oct 2023 07:00:02 GMT
CMD ["gradle"]
# Tue, 03 Oct 2023 07:00:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Oct 2023 07:00:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 03 Oct 2023 07:00:03 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Oct 2023 07:00:03 GMT
WORKDIR /home/gradle
# Tue, 03 Oct 2023 07:00:18 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 06 Oct 2023 01:13:48 GMT
ENV GRADLE_VERSION=7.6.3
# Fri, 06 Oct 2023 01:13:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Fri, 06 Oct 2023 01:13:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 06 Oct 2023 01:13:53 GMT
USER gradle
# Fri, 06 Oct 2023 01:13:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 06 Oct 2023 01:13:54 GMT
USER root
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e560b9ae2a605cbabd174647e334b0807409ab4cdb14e3ffa28655f8e033811`  
		Last Modified: Tue, 03 Oct 2023 05:17:36 GMT  
		Size: 17.5 MB (17455429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a200e428b29b17c8b134286a64173f5831f00680858051961b5ca7505306d59`  
		Last Modified: Tue, 03 Oct 2023 05:17:45 GMT  
		Size: 144.8 MB (144778433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc43ecfdc127e5008009135350763c92b0750409668ab2304125d4e657891ef`  
		Last Modified: Tue, 03 Oct 2023 05:17:34 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef680a12b1abdae0115a150b78eb9007d4d676c8bd48ddd8a63b50a1f58df57`  
		Last Modified: Tue, 03 Oct 2023 05:17:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3336aac7641834ee464fc1ca10f25df598ef659aae0c5ac51f3f96073417160a`  
		Last Modified: Tue, 03 Oct 2023 07:06:50 GMT  
		Size: 4.4 KB (4364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92385c6b273f24d2ce04246a4dbb09c587583c035371050091452c917ab6087b`  
		Last Modified: Tue, 03 Oct 2023 07:06:59 GMT  
		Size: 51.6 MB (51556476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c42efd790326f4116894365ebbd3710d6d66403f0d2969650351edf2cc32dc5`  
		Last Modified: Fri, 06 Oct 2023 01:27:12 GMT  
		Size: 122.3 MB (122346930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d0de6d435a84fcff125320030d9ded96a2b960ce11d95f22829e40dc1fce0`  
		Last Modified: Fri, 06 Oct 2023 01:27:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk` - linux; arm variant v7

```console
$ docker pull gradle@sha256:ea40c64ae7b847baba9bab9a6d323115f51c4bfb8efb0d2908a602a9141968f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363408934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3f38b0f9e2a99d12a8f64895532bc087f170918a6e1732201db7bde3248d3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 25 Sep 2023 10:19:15 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:19:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:19:18 GMT
ADD file:0008d56422c09f73afbcd40ace46d311e36ba0d60eef05198ea3665172ba3433 in / 
# Mon, 25 Sep 2023 10:19:18 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:00:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 06:00:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:00:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 06:02:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:02:50 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 06:03:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 06:03:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 06:03:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:03:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 06:03:04 GMT
CMD ["jshell"]
# Tue, 03 Oct 2023 06:44:40 GMT
CMD ["gradle"]
# Tue, 03 Oct 2023 06:44:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Oct 2023 06:44:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 03 Oct 2023 06:44:41 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Oct 2023 06:44:41 GMT
WORKDIR /home/gradle
# Tue, 03 Oct 2023 06:44:56 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 06 Oct 2023 00:02:17 GMT
ENV GRADLE_VERSION=7.6.3
# Fri, 06 Oct 2023 00:02:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Fri, 06 Oct 2023 00:02:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 06 Oct 2023 00:02:22 GMT
USER gradle
# Fri, 06 Oct 2023 00:02:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 06 Oct 2023 00:02:24 GMT
USER root
```

-	Layers:
	-	`sha256:7271b2c80df6c73d794550b50f57d78c6fd5b85da7934c6506c76ea706087280`  
		Last Modified: Tue, 26 Sep 2023 02:07:56 GMT  
		Size: 27.5 MB (27515498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a42f949007cfbde4e09ba505ced26b019abd8a7ea5591c2ee0c80fe213191ee`  
		Last Modified: Tue, 03 Oct 2023 06:05:16 GMT  
		Size: 17.6 MB (17587273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8cb2c36aabb6e51e5cb39d9ab060ca54e69d03596ee2fb3f3a2013aa6949b`  
		Last Modified: Tue, 03 Oct 2023 06:05:26 GMT  
		Size: 142.1 MB (142064196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f283f5a680dae88eb915b9ed36820132a65dd6d02068dec9c2217211bf3600a0`  
		Last Modified: Tue, 03 Oct 2023 06:05:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb39d0c5347dc505dfd2a2b89a3972c4c610328559f92df055be0d6d90b5ef`  
		Last Modified: Tue, 03 Oct 2023 06:05:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1645a9ffce50ab06cc69c152cbf85005bba59e5e7423d6aa7922d4e25afe398e`  
		Last Modified: Tue, 03 Oct 2023 06:48:42 GMT  
		Size: 4.4 KB (4351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f317e0b1ccbca72b6bbbdfc307d4570c5091ed2450e005b467f4141e9b2425`  
		Last Modified: Tue, 03 Oct 2023 06:48:52 GMT  
		Size: 53.9 MB (53889606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e80fb9dee79ace153d06e6827a77ec188562a4eeb4fc1f7f0ce2716bbaf46`  
		Last Modified: Fri, 06 Oct 2023 00:10:10 GMT  
		Size: 122.3 MB (122346932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed8f455dc34c85e798f7458a69884d104d880071140e678dc7302e8f027f68`  
		Last Modified: Fri, 06 Oct 2023 00:10:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8e2d05e8df2164220d7143fa64584cb48b33c38392c041b8118ce9d58c5fb0e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364280412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29d15f368d12d961439d1f6c0365d1d1d36e3da9624e41a8bf16ec89947607d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 06:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:06:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 06:08:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:08:17 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 06:08:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 06:08:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 06:08:29 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:08:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 06:08:29 GMT
CMD ["jshell"]
# Tue, 03 Oct 2023 06:57:38 GMT
CMD ["gradle"]
# Tue, 03 Oct 2023 06:57:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Oct 2023 06:57:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 03 Oct 2023 06:57:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Oct 2023 06:57:38 GMT
WORKDIR /home/gradle
# Tue, 03 Oct 2023 06:57:51 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 05 Oct 2023 23:41:41 GMT
ENV GRADLE_VERSION=7.6.3
# Thu, 05 Oct 2023 23:41:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Thu, 05 Oct 2023 23:41:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 05 Oct 2023 23:41:46 GMT
USER gradle
# Thu, 05 Oct 2023 23:41:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 05 Oct 2023 23:41:47 GMT
USER root
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba2aefbab3334adfc4bfa89dd448c89bc452ab89a02053172fb42a8e5288ba3`  
		Last Modified: Tue, 03 Oct 2023 06:11:30 GMT  
		Size: 18.9 MB (18859718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753b98fc35cd82fe89ecc7d11b833688e92102be27567d036bb1ead5eec98ed5`  
		Last Modified: Tue, 03 Oct 2023 06:11:37 GMT  
		Size: 143.6 MB (143553841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e5167f5e56a4dc905a342ae65372a5b2d6d6947e1d47086302582aa91263e`  
		Last Modified: Tue, 03 Oct 2023 06:11:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580f4b189461fdb8b41219e07a2c3ea5531b35d7e2b6e4768a911c12cff95029`  
		Last Modified: Tue, 03 Oct 2023 06:11:27 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356253a20dfe92ea3e4a1d86673d16def45e5e207485b8a2e3142384f71fb645`  
		Last Modified: Tue, 03 Oct 2023 07:02:20 GMT  
		Size: 4.4 KB (4370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef15e1f76aeeaf74fc5b079ac7892d2bf51d8e3d54e583dda66379b1ce071c2`  
		Last Modified: Tue, 03 Oct 2023 07:02:26 GMT  
		Size: 51.1 MB (51122415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188033571731756f54d4f8c59344b1d8d7ece3e69fb1cddc49fa0d2f846f10dd`  
		Last Modified: Thu, 05 Oct 2023 23:51:51 GMT  
		Size: 122.3 MB (122346924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b8f2ae3353fc9f3816b0feb80d0af875cc83ec845b864d696e7a58cc337ad5`  
		Last Modified: Thu, 05 Oct 2023 23:51:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk` - linux; ppc64le

```console
$ docker pull gradle@sha256:c1c748d71c10624e843f7f4856f2bafdc6391532fb8f0df477bfb2c9e748358d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 MB (376977881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d1550bfbd5a1ffa8c4d24af86d28b83d4893646a88e99d1ed9192c8b544989`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 25 Sep 2023 10:20:46 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:20:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:20:49 GMT
ADD file:4e52928c778d7e98d90ccfcaacd039ae1fdde494dfa310adbe229d7051c30918 in / 
# Mon, 25 Sep 2023 10:20:49 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 08:16:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:16:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:16:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 08:20:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 08:20:14 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 08:20:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 08:20:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 08:20:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 08:20:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 08:20:45 GMT
CMD ["jshell"]
# Tue, 03 Oct 2023 11:12:02 GMT
CMD ["gradle"]
# Tue, 03 Oct 2023 11:12:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Oct 2023 11:12:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 03 Oct 2023 11:12:06 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Oct 2023 11:12:07 GMT
WORKDIR /home/gradle
# Tue, 03 Oct 2023 11:12:55 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 06 Oct 2023 01:33:02 GMT
ENV GRADLE_VERSION=7.6.3
# Fri, 06 Oct 2023 01:33:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Fri, 06 Oct 2023 01:33:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 06 Oct 2023 01:33:15 GMT
USER gradle
# Fri, 06 Oct 2023 01:33:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 06 Oct 2023 01:33:19 GMT
USER root
```

-	Layers:
	-	`sha256:8098558aeb0337452acaa8c74f02401dc8e9bc5a2c048e4c82c013b483a11f11`  
		Last Modified: Tue, 03 Oct 2023 07:57:52 GMT  
		Size: 35.7 MB (35702863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a1a71044263240e812a6d7b84068cd0594360ef4157124e4c3783bf7297cfa`  
		Last Modified: Tue, 03 Oct 2023 08:24:00 GMT  
		Size: 18.7 MB (18728975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d725de9c6f916836b123cc2ea3b4ebecfb5c8388201eb76feae3cb3e6fafeb6`  
		Last Modified: Tue, 03 Oct 2023 08:24:14 GMT  
		Size: 144.5 MB (144496099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d856cdd68f3bc215ba942b0fbfa954581c297d2ac0655a536fc081561d0ebd09`  
		Last Modified: Tue, 03 Oct 2023 08:23:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342d7c29a897667460f0f83749bec15165419530c3036ba8a0668058ef08f9fa`  
		Last Modified: Tue, 03 Oct 2023 08:23:54 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42364b30f2aaf598f28040787b0469f0b64dde7872e6a23d3dcc4529da2fd17a`  
		Last Modified: Tue, 03 Oct 2023 11:18:10 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9605a337630e3cc0277e38de59ce6c4dd10be560a70b2cfd59355ae948aec8d5`  
		Last Modified: Tue, 03 Oct 2023 11:18:26 GMT  
		Size: 55.7 MB (55697546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703315f0e28851fc54845cd98edf5ee6d9b9a230b95314c3acb4025cb2ec517`  
		Last Modified: Fri, 06 Oct 2023 01:42:30 GMT  
		Size: 122.3 MB (122346953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2ac85692e8e8bd74d8837813896684a83b970249480e0cbe30eb36ecdcd196`  
		Last Modified: Fri, 06 Oct 2023 01:42:19 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk` - linux; s390x

```console
$ docker pull gradle@sha256:ea35e81ed123833c36055d6def7f3e2590803400adf4f3b27c8680c05f5aa5e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.8 MB (353760226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd07206c643b67934e458bf6003b9d16f65198cbc712aac703d3fc6b452d9f8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:26 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:28 GMT
ADD file:78683f2464233172a7cd0d6adc4c7d9fb3ef05fa67ca22e6fbaca0325496a536 in / 
# Mon, 25 Sep 2023 10:17:28 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 09:08:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 09:08:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 09:08:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 09:10:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 09:10:20 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 09:10:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 09:10:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 09:10:40 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 09:10:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 09:10:40 GMT
CMD ["jshell"]
# Tue, 03 Oct 2023 11:02:49 GMT
CMD ["gradle"]
# Tue, 03 Oct 2023 11:02:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Oct 2023 11:02:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 03 Oct 2023 11:02:51 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Oct 2023 11:02:52 GMT
WORKDIR /home/gradle
# Tue, 03 Oct 2023 11:03:26 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Mon, 09 Oct 2023 16:19:17 GMT
ENV GRADLE_VERSION=7.6.3
# Mon, 09 Oct 2023 16:19:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Mon, 09 Oct 2023 16:19:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Mon, 09 Oct 2023 16:19:34 GMT
USER gradle
# Mon, 09 Oct 2023 16:19:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Mon, 09 Oct 2023 16:19:36 GMT
USER root
```

-	Layers:
	-	`sha256:b6ba488997f9924c9473e547d56b3d4ae74495b1092ca3c613243185ee5d5151`  
		Last Modified: Tue, 03 Oct 2023 08:59:45 GMT  
		Size: 28.7 MB (28651983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54dc9f25198df234360ea82a24de7bf823b55e6000600bc0f095d05fc103b78`  
		Last Modified: Tue, 03 Oct 2023 09:13:17 GMT  
		Size: 17.3 MB (17254775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe5a46c26186cc78210b95c057ee4a99f1f3a4e5b0b0821ffddfa0fb505b367`  
		Last Modified: Tue, 03 Oct 2023 09:13:26 GMT  
		Size: 134.2 MB (134217540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0017d46d2028880f3e495629e9b1e9b32bc3e8334a057f52838dab2eb9f214f0`  
		Last Modified: Tue, 03 Oct 2023 09:13:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be756ac3d82b87574c183d45db95b8ec1a7d188426c9ee2d4acdd87841a0d4a`  
		Last Modified: Tue, 03 Oct 2023 09:13:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b4a5559d95f3fc5782ea1383b766d62caac35066129fbfc8061cc10f1e6ffb`  
		Last Modified: Tue, 03 Oct 2023 11:09:38 GMT  
		Size: 4.4 KB (4370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb54b979b64f219b962bc75eaeeba4a21d81e88e5c08f811a67164b4188728e8`  
		Last Modified: Tue, 03 Oct 2023 11:09:47 GMT  
		Size: 51.3 MB (51283570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52b964b884aecf1fc64eb3aea4af35af99f761fb2b141be1fddabce98cd01a1`  
		Last Modified: Mon, 09 Oct 2023 16:27:11 GMT  
		Size: 122.3 MB (122346912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033ace6735464d9ecfd066e95d3021048d9f09fae77187ddcf5ecb4adeb1719c`  
		Last Modified: Mon, 09 Oct 2023 16:27:06 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
