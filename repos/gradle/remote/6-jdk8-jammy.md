## `gradle:6-jdk8-jammy`

```console
$ docker pull gradle@sha256:edc7eb0b4938feab1c0a7796445df57c70e77282c51e0bc520b42901ffa865fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:6-jdk8-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:661fdc9525e3e994d18ce5831ceccd32e5a11e03ca6c14671ee7b4f1a98e81a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305333096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb977bcb48891452226e5cfe7d15284bf574e310087a82021a1e160b2ba6d3a`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:13:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:13:45 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:51 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 07 Jun 2022 04:17:10 GMT
CMD ["gradle"]
# Tue, 07 Jun 2022 04:17:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Jun 2022 04:17:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 07 Jun 2022 04:17:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Jun 2022 04:17:11 GMT
WORKDIR /home/gradle
# Tue, 07 Jun 2022 04:18:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 07 Jun 2022 04:22:06 GMT
ENV GRADLE_VERSION=6.9.2
# Tue, 07 Jun 2022 04:22:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Tue, 07 Jun 2022 04:22:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c045aca8dd90fbfb1afd1343ec6ce2e08ab62f20e8943d3e313dd745e22ee37`  
		Last Modified: Tue, 07 Jun 2022 00:19:41 GMT  
		Size: 12.1 MB (12116064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c983368473e0b821aebeadf218b942d61726ef9dc5e32b8b244fa813f183d9b8`  
		Last Modified: Tue, 07 Jun 2022 00:19:48 GMT  
		Size: 103.5 MB (103506652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc34dedd99747ed957445ccb67ebe18a2e4902f8c1b77913ea98ce0a5b3fc197`  
		Last Modified: Tue, 07 Jun 2022 00:19:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c446a310eb710eec5e01c6565665d24811beb33c666d01aa00a81b8f6dac79c2`  
		Last Modified: Tue, 07 Jun 2022 04:25:03 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03592785a2b8f89599aa637781b694218a5f7257e8fbc000b236f2d73208152`  
		Last Modified: Tue, 07 Jun 2022 04:25:13 GMT  
		Size: 51.6 MB (51591714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e680a823678af543c66db20c56a9e0e75bae9cf91632491d6989d25b67c24ad1`  
		Last Modified: Tue, 07 Jun 2022 04:30:33 GMT  
		Size: 107.7 MB (107690426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk8-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:06fd73bf52640656b20e737647d55da2be3725b2ad16c116b6a9cd4a8464200c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300960447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db97d63e8d6f74afcd9a20e3e3adc7fceca322dbe3df066dbd17b49571db8e6`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 29 Apr 2022 22:59:30 GMT
ADD file:78ae02cb00d8cc788584388eeb9fdc5ca6b45f502d33acd7f6efe7fc2a325683 in / 
# Fri, 29 Apr 2022 22:59:31 GMT
CMD ["bash"]
# Thu, 26 May 2022 21:58:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 26 May 2022 21:58:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 26 May 2022 21:58:58 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Thu, 26 May 2022 21:59:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 26 May 2022 21:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 May 2022 21:59:28 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 26 May 2022 22:35:42 GMT
CMD ["gradle"]
# Thu, 26 May 2022 22:35:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 26 May 2022 22:35:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 26 May 2022 22:35:44 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 26 May 2022 22:35:45 GMT
WORKDIR /home/gradle
# Thu, 26 May 2022 22:36:33 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 26 May 2022 22:41:20 GMT
ENV GRADLE_VERSION=6.9.2
# Thu, 26 May 2022 22:41:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Thu, 26 May 2022 22:41:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:5a3411c136d8a6da4e9d7d3abcbfc94f59ecb2935fd02cad49be6a79c899fcaa`  
		Last Modified: Fri, 29 Apr 2022 23:03:59 GMT  
		Size: 27.0 MB (27015834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f145b58c140123588858a670c723aae35865f6eec57f8f3bdf885d27838cbe`  
		Last Modified: Thu, 26 May 2022 22:10:02 GMT  
		Size: 13.5 MB (13500095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07119e4426d52d49941765578cc81f145e7fcb3ae2707b95739638cdffe9e305`  
		Last Modified: Thu, 26 May 2022 22:10:35 GMT  
		Size: 99.2 MB (99168137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bbc6f26cd8d16be9e758c9f7dccbdc5e1a0d86e243981bec6d5b0742445693`  
		Last Modified: Thu, 26 May 2022 22:09:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171083f1beefab01c8dbfb162612e1237460ee35c4a1d0084ab4ee71b6256403`  
		Last Modified: Thu, 26 May 2022 22:45:28 GMT  
		Size: 4.4 KB (4352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7127b8388cdebbc0a0e56b6a2819edeb0d2f5ab2663d3686a0a8b298c3f1334`  
		Last Modified: Thu, 26 May 2022 22:46:07 GMT  
		Size: 53.6 MB (53581504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8feffae767ec9dd6889a7afd95f5cb6cf2d119328c796d28a25072b87c365c86`  
		Last Modified: Thu, 26 May 2022 22:50:23 GMT  
		Size: 107.7 MB (107690365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk8-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6a0c5a6ca33dcf2c008e25dfcca557fafeaae0632b749c0c46d442060d5025b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301901308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91623256121ee55f4ab0c336e31bf93bb5e87482c73efefecd954c9dcf4c194c`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:32 GMT
ADD file:20805b983efd5443e34ebdfb7795010e5684eb1ca1ffea30a3e61e0089c0eee8 in / 
# Tue, 07 Jun 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:34:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 06:34:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:49 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:34:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:34:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:34:56 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 07 Jun 2022 07:02:04 GMT
CMD ["gradle"]
# Tue, 07 Jun 2022 07:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Jun 2022 07:02:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 07 Jun 2022 07:02:07 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Jun 2022 07:02:08 GMT
WORKDIR /home/gradle
# Tue, 07 Jun 2022 07:02:28 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 07 Jun 2022 07:07:47 GMT
ENV GRADLE_VERSION=6.9.2
# Tue, 07 Jun 2022 07:07:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Tue, 07 Jun 2022 07:07:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:ed02c6ade914c2962413c1ad2ccc86ed8d1512098f2c87fe7bafa8e1b5293185`  
		Last Modified: Thu, 02 Jun 2022 08:38:25 GMT  
		Size: 28.4 MB (28378212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05aeb470f3c462a081767db5b92aa49a956ba558fd0474c8aa38f2197af012ab`  
		Last Modified: Tue, 07 Jun 2022 06:42:05 GMT  
		Size: 12.1 MB (12078242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fe98d9c6472bbdc1a67f66de94b9d387450ec39305c7c0f84a5855c69a8014`  
		Last Modified: Tue, 07 Jun 2022 06:42:13 GMT  
		Size: 102.6 MB (102596147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1eaed03c5efc9ae466c26dfe91dcb7065b6452a56bcf142fcfd59f3ccd8d3e`  
		Last Modified: Tue, 07 Jun 2022 06:42:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0ee53a096e988ef5da1aadf73e1ea1e13c65467f7aa162b6a6802e275b34d`  
		Last Modified: Tue, 07 Jun 2022 07:12:31 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05744e96d971817313195fafd5a5e5cac6039c39d9543efa72aca208468e6fae`  
		Last Modified: Tue, 07 Jun 2022 07:12:40 GMT  
		Size: 51.2 MB (51153911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3762910242dd4555cca8d86eca104cab7afafc44036a456f6f3a2ec30078a5f1`  
		Last Modified: Tue, 07 Jun 2022 07:18:41 GMT  
		Size: 107.7 MB (107690358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk8-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:decd3fd5c51da7619e53d4fb810e13219a97ed0cea891f307cd5b9c51d189aac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.2 MB (333206634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487435997d1e8c5b49853757881dd383fa5a312fad439debab319d70e98f00b8`
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
# Thu, 05 May 2022 18:45:13 GMT
ENV GRADLE_VERSION=6.9.2
# Thu, 05 May 2022 18:45:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Thu, 05 May 2022 18:45:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
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
	-	`sha256:fa3bf6740a96dd939273d2364e2629db111212042e95cc92ece827a0a3051c89`  
		Last Modified: Thu, 05 May 2022 18:48:37 GMT  
		Size: 107.7 MB (107690398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
