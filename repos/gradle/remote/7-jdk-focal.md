## `gradle:7-jdk-focal`

```console
$ docker pull gradle@sha256:e1a23d621437ebe19ef725339ad39ab2cc41880552df52ae8795f5ccda09b736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:7-jdk-focal` - linux; amd64

```console
$ docker pull gradle@sha256:51b4f470abafb9ca79ea2ce5d0fbdb47c25eb0fdbd3d292f64bd001cf657367c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.4 MB (382355752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ec1e77760dfd168655b4bbc4e667bd9e9a016a0c2d5a0027ef39f6b8f41fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:41:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:41:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:41:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:44:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:44:32 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 02 Feb 2024 07:44:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 07:44:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 07:44:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:44:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 07:44:42 GMT
CMD ["jshell"]
# Fri, 02 Feb 2024 16:40:01 GMT
CMD ["gradle"]
# Fri, 02 Feb 2024 16:40:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Feb 2024 16:40:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Feb 2024 16:40:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Feb 2024 16:40:02 GMT
WORKDIR /home/gradle
# Fri, 02 Feb 2024 16:40:23 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 06 Feb 2024 08:32:35 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 06 Feb 2024 08:32:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 06 Feb 2024 08:32:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Tue, 06 Feb 2024 08:32:40 GMT
USER gradle
# Tue, 06 Feb 2024 08:32:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Tue, 06 Feb 2024 08:32:41 GMT
USER root
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cda026f111795ebd512080c1256f21ecd05b7ae0d155c104abe0f60fc168ff`  
		Last Modified: Fri, 02 Feb 2024 07:49:48 GMT  
		Size: 20.7 MB (20668589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276661600bf82016e796ef3c730ed0615c29dc62c3d76898043d1c302939275f`  
		Last Modified: Fri, 02 Feb 2024 07:49:56 GMT  
		Size: 144.9 MB (144901558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df9bc2b9e5ab2e805ee9366b86a1bdfc47a2dba56c5b74c614bb15a0d26ea3`  
		Last Modified: Fri, 02 Feb 2024 07:49:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055140fc60fd644c5db5a50dcdd7ab44b3b88e055fe860794d4708cc22d4e533`  
		Last Modified: Fri, 02 Feb 2024 07:49:44 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187812dbe9369749662191cd1408498f574fffc89c90bea45bbc363660c3f30`  
		Last Modified: Fri, 02 Feb 2024 16:47:48 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e21cc151040e0435f8199e7c784eba4829f87e0918ec84bceb98a0644756ba2`  
		Last Modified: Fri, 02 Feb 2024 16:47:59 GMT  
		Size: 65.5 MB (65465488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6002fe0bfd64d18deed920ddb654cc4e340041e533bcd5583d66325703ff3c`  
		Last Modified: Tue, 06 Feb 2024 08:38:03 GMT  
		Size: 122.7 MB (122730216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6825560f4bfe700fe83411107b70c7829c3904da11a66ae81741903ff160948b`  
		Last Modified: Tue, 06 Feb 2024 08:37:57 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:c08b6deebc26685c45f206b5239209185d286d56e8a9cda2a78b05a1d7bbc93f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 MB (369727324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12136cce17f93dc4196b59521b3bf9530fcc37e2629d4e24b1db6314ed6b5ec8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:14:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 02:14:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:14:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:20:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:20:04 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 02:20:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 02:20:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 02:20:23 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 02:20:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 02:20:23 GMT
CMD ["jshell"]
# Wed, 06 Mar 2024 03:20:28 GMT
CMD ["gradle"]
# Wed, 06 Mar 2024 03:20:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Mar 2024 03:20:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 06 Mar 2024 03:20:31 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Mar 2024 03:20:32 GMT
WORKDIR /home/gradle
# Wed, 06 Mar 2024 03:21:07 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Mar 2024 03:22:52 GMT
ENV GRADLE_VERSION=7.6.4
# Wed, 06 Mar 2024 03:22:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Wed, 06 Mar 2024 03:23:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 06 Mar 2024 03:23:00 GMT
USER gradle
# Wed, 06 Mar 2024 03:23:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 06 Mar 2024 03:23:05 GMT
USER root
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d555e2c31568b7b481f2aa727b2fdcf652e9c4e4b93ca28ed5add2c3cd06645`  
		Last Modified: Wed, 06 Mar 2024 02:25:41 GMT  
		Size: 20.0 MB (19956639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ec048d9fa9ad171dd54ef0a5f117d22f1e2bed4548e473c7d566ef12a77b59`  
		Last Modified: Wed, 06 Mar 2024 02:25:55 GMT  
		Size: 142.3 MB (142339252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c469bff39279f9882015db25667bcf12782c8ecae85a24055ec351e847074e55`  
		Last Modified: Wed, 06 Mar 2024 02:25:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8541780b040ca0b71d7d5b5a27041b53d46ecee1d71515f59d27eca5b0bfa3`  
		Last Modified: Wed, 06 Mar 2024 02:25:35 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82927d9b7a0ec11a53e64c31b357b5ad779fd894e203e6b314d1e3f7a7d23654`  
		Last Modified: Wed, 06 Mar 2024 03:30:20 GMT  
		Size: 4.3 KB (4350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b628d45ad48112b4d94063fbc0ade2da85a51c8131b83d02ce18c9f6331dc9`  
		Last Modified: Wed, 06 Mar 2024 03:30:36 GMT  
		Size: 60.1 MB (60094414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38139b0dffb607970ec0ed6320cbdd2010059a6048b0e2cf0d6179230d6c2dc`  
		Last Modified: Wed, 06 Mar 2024 03:34:02 GMT  
		Size: 122.7 MB (122730249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd6109e2184a3e2ea3225063e763a926d4f37ced72ffda1e2406f83910c95bb`  
		Last Modified: Wed, 06 Mar 2024 03:33:52 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:48eaabdc77be8101ec143cc4d8f06f157e644a11279694c4619749065e54c177
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 MB (380277969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dec5d73f315bbca50aac05cd966fb49a875d082fcfb3d1826a9088c169910d5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:09:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:09:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:09:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:11:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:11:40 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 02 Feb 2024 02:11:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 02:11:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 02:11:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:11:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 02:11:50 GMT
CMD ["jshell"]
# Fri, 02 Feb 2024 09:48:26 GMT
CMD ["gradle"]
# Fri, 02 Feb 2024 09:48:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Feb 2024 09:48:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Feb 2024 09:48:26 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Feb 2024 09:48:26 GMT
WORKDIR /home/gradle
# Fri, 02 Feb 2024 09:48:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 06 Feb 2024 00:24:03 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 06 Feb 2024 00:24:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 06 Feb 2024 00:24:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Tue, 06 Feb 2024 00:24:08 GMT
USER gradle
# Tue, 06 Feb 2024 00:24:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Tue, 06 Feb 2024 00:24:09 GMT
USER root
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f526d63e28c06d1a61394f2dc7fae5588f1b413456899b31feaa627e1f14b495`  
		Last Modified: Fri, 02 Feb 2024 02:16:19 GMT  
		Size: 21.4 MB (21380580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e33f656387b7abac51b4d18ae2c98c25f7ba4803657d1f8b8c02e6a980818e7`  
		Last Modified: Fri, 02 Feb 2024 02:16:26 GMT  
		Size: 143.7 MB (143724284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fbba69e9bb6695e152f726202911e59dc73407c99e2afebfb15092ef73ac59`  
		Last Modified: Fri, 02 Feb 2024 02:16:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ca80af753b61d7d80de7bbfe06a31a6b4661fc10be78349d199a2457146952`  
		Last Modified: Fri, 02 Feb 2024 02:16:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9aebaf534dd4ebd88798a85e67c4cd2c860c1dd9840ffff2628afdf6d573510`  
		Last Modified: Fri, 02 Feb 2024 09:55:06 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca0bc90aeb7866a8f6e117af44096be642b67fe3c0da4dc92cb7d8314e07070`  
		Last Modified: Fri, 02 Feb 2024 09:55:14 GMT  
		Size: 65.2 MB (65232373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf21373d17593d857d36859481bc771e9d16cc9849cdcff32f67415f04e36a1c`  
		Last Modified: Tue, 06 Feb 2024 00:28:03 GMT  
		Size: 122.7 MB (122730228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51e194ee2ae71f8011b0ce6508b7cdfd7872252188c8a0ef0081c755f0f7197`  
		Last Modified: Tue, 06 Feb 2024 00:27:58 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:1448764e94631db99dcba66687a1843af8c37ccdc2518b65f788159d1a619944
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.2 MB (397234973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d336c5f3b154d42d6914d2b46034f059e87acf15ec35e482bd3a2f3f407f5e7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:37:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:37:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:42:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:42 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 02 Feb 2024 02:42:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 02:43:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 02:43:03 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:43:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 02:43:04 GMT
CMD ["jshell"]
# Fri, 02 Feb 2024 06:42:28 GMT
CMD ["gradle"]
# Fri, 02 Feb 2024 06:42:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Feb 2024 06:42:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Feb 2024 06:42:36 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Feb 2024 06:42:38 GMT
WORKDIR /home/gradle
# Fri, 02 Feb 2024 06:43:43 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Mon, 05 Feb 2024 23:30:34 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 23:30:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 23:30:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Mon, 05 Feb 2024 23:30:44 GMT
USER gradle
# Mon, 05 Feb 2024 23:30:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Mon, 05 Feb 2024 23:30:48 GMT
USER root
```

-	Layers:
	-	`sha256:235f35baf74b5944d6dbafa8498b4e2ba58703a9be506a8a9008f01bb6d54cff`  
		Last Modified: Fri, 02 Feb 2024 01:44:37 GMT  
		Size: 33.3 MB (33316035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4298d9a47a47fc29515db7b13aa3ff0282d301e1843a5695e0654ba1cd763f`  
		Last Modified: Fri, 02 Feb 2024 02:49:27 GMT  
		Size: 22.7 MB (22713265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f364339b2ee21827bf58fa62d0683665ff7204290ed31826bd8fa85eac426128`  
		Last Modified: Fri, 02 Feb 2024 02:49:36 GMT  
		Size: 144.6 MB (144634636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec06ebe35bfe0a91d8beeb446f663dbd2565e899fd0c45b46de76fc26999dd5d`  
		Last Modified: Fri, 02 Feb 2024 02:49:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5661122f18daa3310ab19119ab35a47e645fc2bd87cf4e2666f794d46ecacfd`  
		Last Modified: Fri, 02 Feb 2024 02:49:22 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1509bd8f02a5c5fac70d32ad65b9ef82a5da525404910a647bce2e978a3f7e`  
		Last Modified: Fri, 02 Feb 2024 06:53:40 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00df80848c95bf9b4c8722df8cc7e0486715215c9cf7ab7926b3d058f9755fa5`  
		Last Modified: Fri, 02 Feb 2024 06:53:52 GMT  
		Size: 73.8 MB (73835381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26ae55c447439fd1991584e9c40b4c7e8de56133f4cd1743a6f62b74cec98b1`  
		Last Modified: Mon, 05 Feb 2024 23:35:12 GMT  
		Size: 122.7 MB (122730215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbf7d9799297e18678d0ab40e23a914a54bee395605560d8b318c526e70143a`  
		Last Modified: Mon, 05 Feb 2024 23:35:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk-focal` - linux; s390x

```console
$ docker pull gradle@sha256:5eceef8fa7b1f74780ee29ea31557ec383c614163773a0703f0a9973e0bd97c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368913807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2cf1a310d1332c46f0014ab85558a3b9c167de7cb556ed67a65e50dd52de76`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:50:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 01:50:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 01:50:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 01:59:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:59:34 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 02 Feb 2024 01:59:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 01:59:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 01:59:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 01:59:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 01:59:50 GMT
CMD ["jshell"]
# Fri, 02 Feb 2024 09:12:08 GMT
CMD ["gradle"]
# Fri, 02 Feb 2024 09:12:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Feb 2024 09:12:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Feb 2024 09:12:09 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Feb 2024 09:12:09 GMT
WORKDIR /home/gradle
# Fri, 02 Feb 2024 09:12:29 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 06 Feb 2024 00:09:54 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 06 Feb 2024 00:09:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 06 Feb 2024 00:10:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Tue, 06 Feb 2024 00:10:02 GMT
USER gradle
# Tue, 06 Feb 2024 00:10:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Tue, 06 Feb 2024 00:10:03 GMT
USER root
```

-	Layers:
	-	`sha256:a682f62754950fac591750632706a670049f0e9f7ee2bcc2b26407d9c264ed76`  
		Last Modified: Fri, 02 Feb 2024 01:33:16 GMT  
		Size: 27.0 MB (27016265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1a8ba97d3781c129d91af9ffaf5d1b75bba5f9490364ac10735bf03e6247c5`  
		Last Modified: Fri, 02 Feb 2024 02:15:25 GMT  
		Size: 20.1 MB (20147896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a1012c5cfdd2a17dcf728dd95af84ce7506e2b5f24a1cbbb10a8784f005789`  
		Last Modified: Fri, 02 Feb 2024 02:15:33 GMT  
		Size: 134.2 MB (134212629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c14bb37eaf11643618eb4dca6d788151f9bfac7561fedc9ce76de222a820a0d`  
		Last Modified: Fri, 02 Feb 2024 02:15:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710cec61eb9be8c415b95d831432d39a7507aa25198b969c6dc681d0a642b4ff`  
		Last Modified: Fri, 02 Feb 2024 02:15:22 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ac6844abc4a89e60b219c930ae32225cf0af63ab820d407bd5e2a64bec5606`  
		Last Modified: Fri, 02 Feb 2024 09:27:22 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72097a87da63d6cdc8b5dc3b424b63b0573304f2095a7ffd1d5b30ea069630d5`  
		Last Modified: Fri, 02 Feb 2024 09:27:32 GMT  
		Size: 64.8 MB (64801361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a96a849d3271bbabed6461c9383e438f0a3100b385b5a222e328c69b6b6b37c`  
		Last Modified: Tue, 06 Feb 2024 00:18:51 GMT  
		Size: 122.7 MB (122730215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb75fb653699851d26acfdb698f6cb00097cc4db256095c447dc4360fd6e16cc`  
		Last Modified: Tue, 06 Feb 2024 00:18:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
