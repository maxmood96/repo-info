## `gradle:7-jdk11-jammy`

```console
$ docker pull gradle@sha256:d49372ac9ef98e3bf5a645ca26506725d7924a3e5679d12fefccde166d43f0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `gradle:7-jdk11-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:ca214a7ea248e2694e2ee65ca6148efb550bd09dc5d2632d81453f34fcba0ac4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.1 MB (404087758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfb30dae0e39c782849bcd5fae910893460165fcbe52bbad193fd6e0497c93f`
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
# Tue, 07 Jun 2022 00:14:36 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:14:46 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 04:19:07 GMT
CMD ["gradle"]
# Tue, 07 Jun 2022 04:19:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Jun 2022 04:19:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 07 Jun 2022 04:19:08 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Jun 2022 04:19:08 GMT
WORKDIR /home/gradle
# Tue, 07 Jun 2022 04:19:23 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 07 Jun 2022 04:19:23 GMT
ENV GRADLE_VERSION=7.4.2
# Tue, 07 Jun 2022 04:19:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Tue, 07 Jun 2022 04:19:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
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
	-	`sha256:efd1c42ec938ee3c53cfcbeb87e187080c9fc40508b0a17f9b08346ff4a11d8d`  
		Last Modified: Tue, 07 Jun 2022 00:21:14 GMT  
		Size: 194.1 MB (194084286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35541a1051f3873651101dff08aebd5d5c46f08af668b82814b8eef6800c1fc6`  
		Last Modified: Tue, 07 Jun 2022 00:21:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed9cbb94d87ef7326bbe33eddd1371703e440f4647b2e4dc7958dbb7a8aebc8`  
		Last Modified: Tue, 07 Jun 2022 04:26:07 GMT  
		Size: 4.4 KB (4363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d039277120442c99c2b668bd3eb7b49f9d2f4242b335f098ada38b169a9cc62a`  
		Last Modified: Tue, 07 Jun 2022 04:26:16 GMT  
		Size: 51.6 MB (51592181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f22605fa6f966078da416a36bca8f7ebeca84b3d14ab32136a254f3522e7e7`  
		Last Modified: Tue, 07 Jun 2022 04:26:14 GMT  
		Size: 115.9 MB (115866989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:66f6588154af94d957f2c41aef508b95761e4ffca139c6f4ef5edc37cd4d281f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391934400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cdca56c0d7a01acb4c63771502c123b8388b78d1d846d52e90fdaa0c7e11fc`
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
# Thu, 26 May 2022 22:00:45 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Thu, 26 May 2022 22:01:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 26 May 2022 22:01:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 May 2022 22:01:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 26 May 2022 22:01:17 GMT
CMD ["jshell"]
# Thu, 26 May 2022 22:37:06 GMT
CMD ["gradle"]
# Thu, 26 May 2022 22:37:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 26 May 2022 22:37:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 26 May 2022 22:37:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 26 May 2022 22:37:09 GMT
WORKDIR /home/gradle
# Thu, 26 May 2022 22:37:58 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 26 May 2022 22:37:59 GMT
ENV GRADLE_VERSION=7.4.2
# Thu, 26 May 2022 22:37:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Thu, 26 May 2022 22:38:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
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
	-	`sha256:9978a0050488d52787c3f8151d99f7d9aedf5045e20724a24ddc1a964cc206cc`  
		Last Modified: Thu, 26 May 2022 22:12:40 GMT  
		Size: 182.0 MB (181965589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df612a142ec7ffb8861b050c19f44b07d125e90228508bae6536429960bbe83`  
		Last Modified: Thu, 26 May 2022 22:11:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9d62846464a7e03d54fea04393954d093fbe0ea36267fc49eb087e3df1515c`  
		Last Modified: Thu, 26 May 2022 22:46:27 GMT  
		Size: 4.4 KB (4353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22dff316a2330018e9260e875466d37ebea866842d7d4c0474e3850c9a53a414`  
		Last Modified: Thu, 26 May 2022 22:47:05 GMT  
		Size: 53.6 MB (53581366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cfc0caa5fe1f69b48e31cf8a97e73eae0f2c7aff5ba9b689a359856cf07dd6`  
		Last Modified: Thu, 26 May 2022 22:47:00 GMT  
		Size: 115.9 MB (115867004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:aa1cb10acbeeb5dc610669c66a0710e4eff746018df36032dbc4235c5b7ae258
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.3 MB (398306396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0201279cde9dd54055dd9749d93050751fef41e4365a66efde7e0814165d8461`
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
# Tue, 07 Jun 2022 06:35:54 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:36:03 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 07:03:25 GMT
CMD ["gradle"]
# Tue, 07 Jun 2022 07:03:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Jun 2022 07:03:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 07 Jun 2022 07:03:28 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Jun 2022 07:03:29 GMT
WORKDIR /home/gradle
# Tue, 07 Jun 2022 07:03:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 07 Jun 2022 07:03:50 GMT
ENV GRADLE_VERSION=7.4.2
# Tue, 07 Jun 2022 07:03:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Tue, 07 Jun 2022 07:03:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
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
	-	`sha256:640e2d2b30f0a065c789ca75b2ebd9e91fbd62c9e357b1efa67023338fe10521`  
		Last Modified: Tue, 07 Jun 2022 06:43:54 GMT  
		Size: 190.8 MB (190824624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4432e71ad436a9505c269821b3bf94131913cea4637f15f6569599baae42f68`  
		Last Modified: Tue, 07 Jun 2022 06:43:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1feb964d72723b128ca3d9969175b3b1976a0ccd45eab1789e70830d5e4f200`  
		Last Modified: Tue, 07 Jun 2022 07:13:40 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2098836d08d8af5ec08446b080256975bb99220dd661da5315e1b2cd411129`  
		Last Modified: Tue, 07 Jun 2022 07:13:49 GMT  
		Size: 51.2 MB (51154060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e82e2b6ddcab3dee4d00de969003d243339a1b8640ff4e04303c7f8eeb2609`  
		Last Modified: Tue, 07 Jun 2022 07:13:48 GMT  
		Size: 115.9 MB (115866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:0b80f45009a997ee827611f0687f442b9c847386d572e16b7da7414fddebbe26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.4 MB (376441489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e46c1a718a835aeceb9d52df246c104c629ea38419f7f0db30e7945132d5636`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 07 Jun 2022 04:05:41 GMT
ADD file:5412b0d16961079a78b96411ca23f1838ac09c2fae839829476380b5389e49f8 in / 
# Tue, 07 Jun 2022 04:05:45 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:33:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 06:34:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:27 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:34:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:35:08 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 07:06:25 GMT
CMD ["gradle"]
# Tue, 07 Jun 2022 07:06:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Jun 2022 07:06:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 07 Jun 2022 07:06:26 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Jun 2022 07:06:26 GMT
WORKDIR /home/gradle
# Tue, 07 Jun 2022 07:06:51 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 07 Jun 2022 07:06:55 GMT
ENV GRADLE_VERSION=7.4.2
# Tue, 07 Jun 2022 07:06:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Tue, 07 Jun 2022 07:07:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:6fa1296f44090f6150dfb96d6ae217a58b9d66c56d7a986c35657df6bd1a89f0`  
		Last Modified: Tue, 07 Jun 2022 04:08:13 GMT  
		Size: 28.6 MB (28638482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b397e817b43cdbb81df1aadc82bc60111139c12d19d0d6207b714984154c982c`  
		Last Modified: Tue, 07 Jun 2022 06:43:05 GMT  
		Size: 12.2 MB (12162912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0b1941118b361325ae8bb908210e16032f32170839e847b8b06f0a0b0c78d4`  
		Last Modified: Tue, 07 Jun 2022 06:43:14 GMT  
		Size: 168.5 MB (168477745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ed72f73957ed466d2281dd79c895345bffab93eab88dfa3fff31c95c90eb6b`  
		Last Modified: Tue, 07 Jun 2022 06:43:03 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4a33f8b98aeafeca0374b55efb52194a4697bedbaff38e6e84fd5c362e4ddb`  
		Last Modified: Tue, 07 Jun 2022 07:17:41 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1338791ddd3035ef0e30afcf187b294da597c759d5c9faea59f071b1d7be6158`  
		Last Modified: Tue, 07 Jun 2022 07:17:50 GMT  
		Size: 51.3 MB (51290783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234be717e2823a754b4f1ff004601620ffb1ea006dc28414819f960d0085a536`  
		Last Modified: Tue, 07 Jun 2022 07:17:47 GMT  
		Size: 115.9 MB (115867038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
