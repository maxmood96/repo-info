## `gradle:jdk8`

```console
$ docker pull gradle@sha256:5341d85dc65fd3473faed2cc264c728df5672b69d38de6899d4683c656919f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:4545d66bff85b7835ffdb001c1df96bb8a7ae27013441e2fc6ba677b05ce534c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329618669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc265010a056032a81de326a54e79508bdb3beefaa972be51e76172b4a096f23`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Apr 2022 00:22:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 05 May 2022 18:27:10 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Thu, 05 May 2022 18:27:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 05 May 2022 18:27:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 May 2022 18:27:23 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 05 May 2022 18:52:09 GMT
CMD ["gradle"]
# Thu, 05 May 2022 18:52:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 May 2022 18:52:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 05 May 2022 18:52:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 May 2022 18:52:10 GMT
WORKDIR /home/gradle
# Thu, 05 May 2022 18:52:43 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 05 May 2022 18:52:44 GMT
ENV GRADLE_VERSION=7.4.2
# Thu, 05 May 2022 18:52:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Thu, 05 May 2022 18:52:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e94d254f3c4d0b302d167dc31edd456d3f663ed337bc99fdd2fd0a21025340e`  
		Last Modified: Sat, 30 Apr 2022 00:26:11 GMT  
		Size: 16.0 MB (16030310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef23661879700ba6a9edf6791b943ef9ffd5b7937549760dbc0d7cdee19677`  
		Last Modified: Thu, 05 May 2022 18:30:10 GMT  
		Size: 103.5 MB (103506650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef342c79cf430f29b09a40d61452fcb33c0a48506d08682f1c9df1ca4708d44`  
		Last Modified: Thu, 05 May 2022 18:30:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdd99bbe80f73719abb86c319456ac0a2589fa729c95c3a2672e1c523b29467`  
		Last Modified: Thu, 05 May 2022 18:54:28 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab8a5878f43ba9d0815d9ff323c64713094a3b85f3a2d3546f6a9314579672f`  
		Last Modified: Thu, 05 May 2022 18:54:39 GMT  
		Size: 65.6 MB (65643960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee463584a1b8df69dd3fe12d11bffc44e1706176e12cf7224ea77c2e296d5d8`  
		Last Modified: Thu, 05 May 2022 18:54:34 GMT  
		Size: 115.9 MB (115867000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; arm variant v7

```console
$ docker pull gradle@sha256:da70c60322a3be6177a91642fce0ab0682e28ab4cad02309923e0885b215cb01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314051206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da60da870c56ae58936d92f80d37867f3f1d577d291788ce12de40a135c4078`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:56:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 29 Apr 2022 23:56:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 05 May 2022 17:57:50 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Thu, 05 May 2022 17:58:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 05 May 2022 17:58:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 May 2022 17:58:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 05 May 2022 18:24:45 GMT
CMD ["gradle"]
# Thu, 05 May 2022 18:24:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 May 2022 18:24:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 05 May 2022 18:24:48 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 May 2022 18:24:48 GMT
WORKDIR /home/gradle
# Thu, 05 May 2022 18:25:40 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 05 May 2022 18:25:41 GMT
ENV GRADLE_VERSION=7.4.2
# Thu, 05 May 2022 18:25:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Thu, 05 May 2022 18:25:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142d50dc2d1479b31402efb7588259cffeca2de60159fa16b540aa20dcf0cd3f`  
		Last Modified: Sat, 30 Apr 2022 00:04:04 GMT  
		Size: 14.9 MB (14901951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94a0f212c6806a29bc6ad2be1402045849592d1ad06d82a499e2bbcb17e8c51`  
		Last Modified: Thu, 05 May 2022 18:03:24 GMT  
		Size: 99.2 MB (99172198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902d1ec012df2369c11ba97a2b494c4796d13fd4aab1745349276c73f1509d52`  
		Last Modified: Thu, 05 May 2022 18:02:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f2bb404ab2e331ab28075e586aea336a0658c5b4944f25cf3f4985c78cdbfe`  
		Last Modified: Thu, 05 May 2022 18:30:31 GMT  
		Size: 4.3 KB (4350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c46aef73f654b94e9b429e749242144753fa2d88008fad4a4a2a3a725c4267`  
		Last Modified: Thu, 05 May 2022 18:31:14 GMT  
		Size: 60.0 MB (60031862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39626a9ff581739ff798fa7dbf7dfec9996d33dda36fd6c3d564453d213d911`  
		Last Modified: Thu, 05 May 2022 18:31:04 GMT  
		Size: 115.9 MB (115867035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:08b85f45981a0e3ba75072f3831ae542b161e8771b4052e601fd313982141d06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326889297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862dbccb5f91e64f602bd0e3239232063a62c67b3b05b11163cae0c060a2bbf`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:28:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 29 Apr 2022 23:28:52 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 05 May 2022 17:44:46 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Thu, 05 May 2022 17:44:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 05 May 2022 17:44:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 May 2022 17:44:56 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 05 May 2022 18:13:56 GMT
CMD ["gradle"]
# Thu, 05 May 2022 18:13:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 May 2022 18:13:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 05 May 2022 18:13:58 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 May 2022 18:13:59 GMT
WORKDIR /home/gradle
# Thu, 05 May 2022 18:14:22 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 05 May 2022 18:14:23 GMT
ENV GRADLE_VERSION=7.4.2
# Thu, 05 May 2022 18:14:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Thu, 05 May 2022 18:14:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce33c7cb386794b97371bf23d6db512379e04036ae033b076a599f51f6416b6`  
		Last Modified: Fri, 29 Apr 2022 23:33:40 GMT  
		Size: 15.9 MB (15897301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec1cfd34aa22f977718cadf96e6977bfdd53c6325143c9a04a8825df80fc9c9`  
		Last Modified: Thu, 05 May 2022 17:48:32 GMT  
		Size: 102.6 MB (102596125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74dc687d0163b45e6e77464343692f39a47992c93fd1605df9090cb46e1debf`  
		Last Modified: Thu, 05 May 2022 17:48:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebffa0f0ff0f568918d4b54f5d809f50621325da7b0173354b9f271ce18dbb1`  
		Last Modified: Thu, 05 May 2022 18:16:31 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11cdc194b41a30b5766d4a805cc768375042526d6560686c9fe830693ceea8c`  
		Last Modified: Thu, 05 May 2022 18:16:42 GMT  
		Size: 65.4 MB (65355227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddabbccc27fc02b33e9b98e34d6df987bac484ed85f2dc54bcda77e0b8b89d2d`  
		Last Modified: Thu, 05 May 2022 18:16:39 GMT  
		Size: 115.9 MB (115866816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:f9a57241bd97cb4a099d99ec393cc790454323a4844fd7ee7f22d9c728b8899d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341383195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca2897eb671f2d48d44474d0506e02f01577404e9999816035cd7e66de043cc`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:28 GMT
ADD file:55691ac7d76af0fcfafc39ebd1e5a4f2d7018147d6db6f89812db33fbaffc2f9 in / 
# Fri, 29 Apr 2022 23:22:33 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:29:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Apr 2022 00:32:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 05 May 2022 18:16:57 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Thu, 05 May 2022 18:17:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 05 May 2022 18:17:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 May 2022 18:17:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 05 May 2022 18:41:23 GMT
CMD ["gradle"]
# Thu, 05 May 2022 18:41:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 May 2022 18:41:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 05 May 2022 18:41:44 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 May 2022 18:41:51 GMT
WORKDIR /home/gradle
# Thu, 05 May 2022 18:43:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 05 May 2022 18:44:09 GMT
ENV GRADLE_VERSION=7.4.2
# Thu, 05 May 2022 18:44:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Thu, 05 May 2022 18:44:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:e9c0a77cb9f0f7330e3fc62254e4c8ae89ed4bba21209fdc1088195250f950b9`  
		Last Modified: Fri, 29 Apr 2022 23:25:23 GMT  
		Size: 33.3 MB (33290661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a436aa11f9f1d03225e672ec1f60e82ddcff2d3b267d9904213f0f01ed5eeba5`  
		Last Modified: Sat, 30 Apr 2022 00:45:44 GMT  
		Size: 17.2 MB (17204116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64577efdc58bfd75c4e990ca918a28f97813f3fa7cafea8a725edde383f1c24`  
		Last Modified: Thu, 05 May 2022 18:23:47 GMT  
		Size: 101.0 MB (101003875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0ce2b433ee6700be1d481ffec265e4438c13832881c0fa71851e55b3d8e845`  
		Last Modified: Thu, 05 May 2022 18:23:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcd3ba05688bd7826cde35fefbdb14e4921eafbaf49588df09aa048841fd92c`  
		Last Modified: Thu, 05 May 2022 18:47:35 GMT  
		Size: 4.4 KB (4372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74555c9555a9397853c61af7771155d5ddd40f237132242857b36d5de3e2d705`  
		Last Modified: Thu, 05 May 2022 18:47:50 GMT  
		Size: 74.0 MB (74013052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f98ed08aad287fd1d8850458418dcaeb53ca483d110d3efbafbc585f2078f8`  
		Last Modified: Thu, 05 May 2022 18:47:45 GMT  
		Size: 115.9 MB (115866959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
