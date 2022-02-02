## `gradle:jdk8`

```console
$ docker pull gradle@sha256:f34b5463801af6072bf0a0373258c8b987d9be8cbf33e35ea61a0c3eb7d2ad08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:92a677b6726f46a5ba3b1232342db2b405c1fa8e13cf94418f37cb6077d1e832
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329696017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd40051c4428afe57dfd2ac2de036226d31623bc986bf1e4be13c8ab562e99d`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:20 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 02:58:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42ed3ff5a859f9015a1362fb7e650026b913d688eab471714f795651120be173';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c7cc9c5b237e9e1f1e3296593aba427375823592e4604fadf89a8c234c2574e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d62362a78c9412766471b05253507a4cfc212daea5cdf122860173ce902400e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:58:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:58:30 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 09:41:19 GMT
CMD ["gradle"]
# Wed, 02 Feb 2022 09:41:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 02 Feb 2022 09:41:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 02 Feb 2022 09:41:20 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 02 Feb 2022 09:41:21 GMT
WORKDIR /home/gradle
# Wed, 02 Feb 2022 09:41:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 02 Feb 2022 09:41:42 GMT
ENV GRADLE_VERSION=7.3.3
# Wed, 02 Feb 2022 09:41:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
# Wed, 02 Feb 2022 09:41:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddf3188a5bd879fce8ce2931923122e956d76f5bf6964de93536fc2c91e778e`  
		Last Modified: Wed, 02 Feb 2022 03:02:05 GMT  
		Size: 103.7 MB (103656405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d2a1172db70af720594a52b8be0aebe43baef16e9cf93b4aa84b2b0f36eaa`  
		Last Modified: Wed, 02 Feb 2022 03:01:56 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9477db5f137da1c12c13ae4034f493fa6d57c4e33214200001fa58320fa01`  
		Last Modified: Wed, 02 Feb 2022 09:44:21 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a22f4266b62df06c38fb743e66e04e00131524c17443fd54bd605d4885250f`  
		Last Modified: Wed, 02 Feb 2022 09:44:31 GMT  
		Size: 56.9 MB (56871293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed790aff643080a75f2e60f9b18fd9e9978de84aa63148d4faa90d74e15f4411`  
		Last Modified: Wed, 02 Feb 2022 09:44:28 GMT  
		Size: 115.8 MB (115785039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; arm variant v7

```console
$ docker pull gradle@sha256:f0bdf67ed36f8fed059426cd34a7134160c31a7a78435149ce98e1bfd09fe71f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314095552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f86501d1ac4bf293ad626c90215870dc5c97d27c49842446470e1c95bac1cb`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:25 GMT
ADD file:ac83e0dc7e48a0dc1805c0fd7b71b8eb119b3eeafd1fdcab93e11fbc9c0bcda0 in / 
# Fri, 07 Jan 2022 02:26:26 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:24:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 03:25:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:25:23 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 07 Jan 2022 03:25:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='87ff502eba3008cac71edeb9595398a73dc14883fe3072d152e731bf0877897e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u312b07.tar.gz';          ;;        armhf|arm)          ESUM='5a9e72c6c20373aa380554a6d7191a258540d2a0399d842223b8d5eb0f74b298';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u312b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ddce3f067eab6fd98bb2a8ea3d18de6b09ea41d10382c76ad22bd3e7895951cf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u312b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='699981083983b60a7eeb511ad640fae3ae4b879de5a3980fe837e8ade9c34a08';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u312b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 03:25:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 03:25:52 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 07 Jan 2022 06:12:36 GMT
CMD ["gradle"]
# Fri, 07 Jan 2022 06:12:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 07 Jan 2022 06:12:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 07 Jan 2022 06:12:39 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 07 Jan 2022 06:12:39 GMT
WORKDIR /home/gradle
# Fri, 07 Jan 2022 06:13:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 07 Jan 2022 06:13:26 GMT
ENV GRADLE_VERSION=7.3.3
# Fri, 07 Jan 2022 06:13:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
# Fri, 07 Jan 2022 06:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:9b8080fa0945580f29aa3abed4664f8ab849229eca04510b5d259a9e29616064`  
		Last Modified: Fri, 07 Jan 2022 02:30:39 GMT  
		Size: 24.1 MB (24064434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6e4c0409024952682215eb90badafc7748ba973c9a2d5b93c8c3148ce34ee5`  
		Last Modified: Fri, 07 Jan 2022 03:33:32 GMT  
		Size: 23.1 MB (23071830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f8f3a43f71dd3efce0ab46cf3530aa311a769a8d385a03df5fdc85d085f70b`  
		Last Modified: Fri, 07 Jan 2022 03:33:59 GMT  
		Size: 99.3 MB (99274932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b370572cca8dccdc7d29848ca4bd331ea50c630b8ff21a51dfb46cc13d2752e`  
		Last Modified: Fri, 07 Jan 2022 03:33:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515666d7375057ebf2be2f1e1f5e5d31f42c41239a8e9cb498b96b7b79365d9b`  
		Last Modified: Fri, 07 Jan 2022 06:20:32 GMT  
		Size: 4.3 KB (4340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0d69526c403a21ad8b7828d5724c779411b20f79cdb85fbb1b100576251dd7`  
		Last Modified: Fri, 07 Jan 2022 06:21:08 GMT  
		Size: 51.9 MB (51894839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3296212aa9afcd81353ab02a5d0545e071b904de195510558c9a3f5ee792c42`  
		Last Modified: Fri, 07 Jan 2022 06:21:05 GMT  
		Size: 115.8 MB (115785017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3678634ded2f67972f74fe9baf4a1e16aabc4bc00a9251a01c5b609d5f5bdfd4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326961418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844ef734136d33f4b2e5ca48498339c9c664b091c3ed10087d89b58ef611830e`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:01:54 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:02:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42ed3ff5a859f9015a1362fb7e650026b913d688eab471714f795651120be173';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c7cc9c5b237e9e1f1e3296593aba427375823592e4604fadf89a8c234c2574e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d62362a78c9412766471b05253507a4cfc212daea5cdf122860173ce902400e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:02:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 07:16:45 GMT
CMD ["gradle"]
# Wed, 02 Feb 2022 07:16:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 02 Feb 2022 07:16:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 02 Feb 2022 07:16:48 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 02 Feb 2022 07:16:49 GMT
WORKDIR /home/gradle
# Wed, 02 Feb 2022 07:17:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 02 Feb 2022 07:17:11 GMT
ENV GRADLE_VERSION=7.3.3
# Wed, 02 Feb 2022 07:17:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
# Wed, 02 Feb 2022 07:17:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78de24c392eac2b43acb5121cd67869312f331b26790c5c5ec2b2cc400d35b92`  
		Last Modified: Wed, 02 Feb 2022 05:06:34 GMT  
		Size: 102.7 MB (102746632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfe14947f376156bd7da68a5aeffc9bbbe3f77ef14d909a267abb135e57830a`  
		Last Modified: Wed, 02 Feb 2022 05:06:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49481d2767c1a2c128cc71dec05cc744715a4847dce9b0cf2eca7ee760c59e12`  
		Last Modified: Wed, 02 Feb 2022 07:20:28 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165614dddfc6d9b8b04dc53be250355328d9681bf18c36798d1ec3eb5f8e5d58`  
		Last Modified: Wed, 02 Feb 2022 07:20:38 GMT  
		Size: 56.5 MB (56493267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff9fa0c97e680357967d6890d23815c5be85df4e28d910e56e1a7073235ba9f`  
		Last Modified: Wed, 02 Feb 2022 07:20:41 GMT  
		Size: 115.8 MB (115784714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:9eaaea5562c701b986304dd826fad9603040a83dded4aeb0a99e4442da143377
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341439265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae95b46ce13463d5462a73e96a1a06f0e4133c69c9bf17a0b6cf6257ea6d05f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:15:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 03:16:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Feb 2022 22:16:40 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 01 Feb 2022 22:17:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42ed3ff5a859f9015a1362fb7e650026b913d688eab471714f795651120be173';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c7cc9c5b237e9e1f1e3296593aba427375823592e4604fadf89a8c234c2574e1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d62362a78c9412766471b05253507a4cfc212daea5cdf122860173ce902400e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 01 Feb 2022 22:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Feb 2022 22:17:12 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Feb 2022 22:47:34 GMT
CMD ["gradle"]
# Tue, 01 Feb 2022 22:47:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 01 Feb 2022 22:47:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 01 Feb 2022 22:47:50 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 01 Feb 2022 22:47:53 GMT
WORKDIR /home/gradle
# Tue, 01 Feb 2022 22:49:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 01 Feb 2022 22:49:32 GMT
ENV GRADLE_VERSION=7.3.3
# Tue, 01 Feb 2022 22:49:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
# Tue, 01 Feb 2022 22:49:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b586e04868a22fd817c8971330fec37e298f3242eb85c374181b12d637f80302
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e359e3ea7dc58d4487bc585c0d8fcd27011690cd1135560fbab69fb8eb51ca7`  
		Last Modified: Fri, 07 Jan 2022 03:24:37 GMT  
		Size: 26.6 MB (26642914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc07e11f4fb9bbd77d5e73f7c132536d709b1e02f13d37db1e5ed6ffc257c09`  
		Last Modified: Tue, 01 Feb 2022 22:26:48 GMT  
		Size: 101.1 MB (101145776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea1f0a8baed1597417fc1ec6b9cdcef09b7bbd86a8a8f383e2e318023724e01`  
		Last Modified: Tue, 01 Feb 2022 22:26:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3034c59741ac27c4725ac4f7e649537391574fb235f72d14b23ca53831564792`  
		Last Modified: Tue, 01 Feb 2022 22:58:21 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0364a0c722c1b6ca10038b53cf3ad66c206524f36442703050ea9f49ec95fd4b`  
		Last Modified: Tue, 01 Feb 2022 22:58:35 GMT  
		Size: 64.6 MB (64574139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be30b56dd68024d3a21901674af4a865620d6cd20f218c2de340f43cd1a77489`  
		Last Modified: Tue, 01 Feb 2022 22:58:31 GMT  
		Size: 115.8 MB (115785019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
