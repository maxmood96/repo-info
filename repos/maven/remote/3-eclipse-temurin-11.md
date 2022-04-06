## `maven:3-eclipse-temurin-11`

```console
$ docker pull maven@sha256:0ef47ecd30672789f6b852b613698d5566b7687175fde1b393e78293ad6e13b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-eclipse-temurin-11` - linux; amd64

```console
$ docker pull maven@sha256:f8b4e5bfc202d2757f78eaf689a090aa6d3699cc4517716a6b782a2d9ff99db1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278454256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693a19e2511eecc2a8f65d936ae5e094c262ef11a7fd04caca0c764113df1c62`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:32 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 23:06:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 05 Apr 2022 23:06:41 GMT
CMD ["jshell"]
# Wed, 06 Apr 2022 04:56:55 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:56:55 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 04:56:55 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 04:56:55 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 04:56:55 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 04:56:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 04:56:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 04:56:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 04:56:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 04:56:58 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 04:56:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 04:56:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d0de1fd7e00dfcdf4a2d54da1c52a815c8aa5ed6413395fd7179d6224fd58c`  
		Last Modified: Tue, 05 Apr 2022 23:10:32 GMT  
		Size: 193.9 MB (193949675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b638505435dc117b189689beca3fadbb7a897a1ff5c015f59cfbeeefffdf2c4a`  
		Last Modified: Tue, 05 Apr 2022 23:10:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4362a7a59f20cedfaa5d16027ffd40a9550e8c283a4e382a3334b249ad822148`  
		Last Modified: Wed, 06 Apr 2022 05:01:09 GMT  
		Size: 31.2 MB (31170468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0779482a7674d3c987c7ddc879161c017cf1c7e273a15893dc22e360b62e8b`  
		Last Modified: Wed, 06 Apr 2022 05:01:04 GMT  
		Size: 8.7 MB (8736373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b509bea33fb96a5069d17cc7146c7060d8549a48c05d22ae0b919a4c60ae6aed`  
		Last Modified: Wed, 06 Apr 2022 05:01:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa7330e99ede3bd643d248b9671cce95c8409ba7b83359d1fd510464749eae7`  
		Last Modified: Wed, 06 Apr 2022 05:01:03 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; arm variant v7

```console
$ docker pull maven@sha256:ddce160903dc689b7c074549612f22de64be68058f04beb0ee7423835f1fb000
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256838787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd2d106fd1b2909f7d41c6203dd3db98b233c42485fb23988af98566fe0805e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Mar 2022 07:32:41 GMT
ADD file:2e353e40ad52bb1b5a10aafb7912657744b02d096925b5bfc6e925ebf7cddede in / 
# Fri, 18 Mar 2022 07:32:42 GMT
CMD ["bash"]
# Sun, 20 Mar 2022 06:32:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 20 Mar 2022 06:33:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sun, 20 Mar 2022 06:34:42 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Sun, 20 Mar 2022 06:35:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sun, 20 Mar 2022 06:35:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 06:35:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sun, 20 Mar 2022 06:35:07 GMT
CMD ["jshell"]
# Fri, 01 Apr 2022 05:13:43 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 02:40:01 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 02:40:02 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 02:40:02 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 02:40:02 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 02:40:06 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 02:40:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 02:40:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 02:40:07 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 02:40:08 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 02:40:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 02:40:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:260b2dce5be1e0d17bf9e2ec2bbde587e5023ab1b48278ddf8396dcfc8eb7e99`  
		Last Modified: Fri, 18 Mar 2022 07:36:23 GMT  
		Size: 24.1 MB (24073481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53338e80157a2d8d75acf73c7d6a401a71fb6f4b5d452c1922a2452a516efef`  
		Last Modified: Sun, 20 Mar 2022 06:40:48 GMT  
		Size: 14.9 MB (14902387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45420463ad28b786d692e2857cddca64d70ffe3d1b6342131f725fc27835bcdd`  
		Last Modified: Sun, 20 Mar 2022 06:43:18 GMT  
		Size: 181.8 MB (181831167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d447409cf799b10d04d1f14cd4f69f7ea1db4914d01c127808300bdd96657a`  
		Last Modified: Sun, 20 Mar 2022 06:42:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765f5da2ebb7b7b78c0db38472b4a75740056f9ccf50e9128828af068d7f6c45`  
		Last Modified: Wed, 06 Apr 2022 02:42:54 GMT  
		Size: 27.3 MB (27294009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07163b376d68afeb7e723f38cd91b9c9e6c85ed58b3246cf8254dbcc19c40541`  
		Last Modified: Wed, 06 Apr 2022 02:42:40 GMT  
		Size: 8.7 MB (8736367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854777959aaf2667a2ff9c7155678945e31882a0145fd6a12aadfc26eacd11de`  
		Last Modified: Wed, 06 Apr 2022 02:42:37 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f20623cf0aa59f3bfdcb76e898a3d19a2648b4a81599d8034d6d9ab9683f52`  
		Last Modified: Wed, 06 Apr 2022 02:42:37 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c038bd8bcea6e7c36ce3a67dedd20758bc2ed181f53bc09ce97d535166e6c71b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273454462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc766aecb82be5f0c1d51628ccae2023df4a823f56cbb33f99fcf090fde8caf1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:28:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 15:28:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:29:09 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Sat, 19 Mar 2022 15:29:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 15:29:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 15:29:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Mar 2022 15:29:22 GMT
CMD ["jshell"]
# Tue, 05 Apr 2022 18:36:27 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 18:36:28 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 05 Apr 2022 18:36:28 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Apr 2022 18:36:29 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 05 Apr 2022 18:36:30 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 05 Apr 2022 18:36:33 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 05 Apr 2022 18:36:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Apr 2022 18:36:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Apr 2022 18:36:37 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 05 Apr 2022 18:36:38 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 05 Apr 2022 18:36:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Apr 2022 18:36:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c236902da3463f4b33e5af2f3ff655994cbe47d5e8380294ee6d6a5957b77710`  
		Last Modified: Sat, 19 Mar 2022 15:32:57 GMT  
		Size: 15.9 MB (15897447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7dc3547484b64c4e922a4709e02db6324a87b63660901bf8fb0644d12f7fda`  
		Last Modified: Sat, 19 Mar 2022 15:34:01 GMT  
		Size: 190.7 MB (190684900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbff2a01ded49509bb7fb35d499d93b6c36f7e70c5bbeee8719351d3fa8a82a`  
		Last Modified: Sat, 19 Mar 2022 15:33:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166782ddda9973793d6d1646f65266e31428985c57c113a22fefe3313b8de7e5`  
		Last Modified: Tue, 05 Apr 2022 18:47:17 GMT  
		Size: 31.0 MB (30964826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1010c393a2df3b068d7cb5fe7ecefef86ddf95434911fb9c865407788c97ebd2`  
		Last Modified: Tue, 05 Apr 2022 18:47:14 GMT  
		Size: 8.7 MB (8736329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c6a390fe35827ed54f60ccd4866a830561e9610efdb2e0534d3896efae4686`  
		Last Modified: Tue, 05 Apr 2022 18:47:12 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83688488525307027c67d46055bcc1f2a31ece307848ef6e7394f5d0b08d083`  
		Last Modified: Tue, 05 Apr 2022 18:47:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; ppc64le

```console
$ docker pull maven@sha256:749c96b02b22a339f5f19a50af2d717a0c87cf8a01397adb1f6477a414e0d6fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273454153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25253a99e2b3c70c1ff85abea354f68f2baffbd6568a18185b44d785c3e9b118`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:11:44 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Sat, 19 Mar 2022 20:12:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:12:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:12:14 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Mar 2022 20:12:16 GMT
CMD ["jshell"]
# Thu, 31 Mar 2022 21:30:37 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 02:59:23 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 02:59:25 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 02:59:28 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 02:59:33 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 02:59:58 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 03:00:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 03:00:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 03:00:09 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 03:00:11 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 03:00:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 03:00:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290111b271d10a11cbde09871151fa934ac77eba5c738ce396f0b8c6e42b6e8d`  
		Last Modified: Sat, 19 Mar 2022 20:19:26 GMT  
		Size: 175.8 MB (175842566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95de4a35bc94bb4395ae495ff58485bc040cd1460c0444bf59ec252cb1b15e3`  
		Last Modified: Sat, 19 Mar 2022 20:19:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8f1cc28fe0fe27ddbb947e5d8758aefc3af16cc82248fc3022231162acf8ca`  
		Last Modified: Wed, 06 Apr 2022 03:08:01 GMT  
		Size: 38.4 MB (38376141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e8a1e4ed6d0085debbca60dfadc17f2e85daca13a373115fe89613e94fa703`  
		Last Modified: Wed, 06 Apr 2022 03:07:31 GMT  
		Size: 8.7 MB (8736376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a3b18fe21c950789512b17eb98b6dff9487eae6be10bc85a01e504e07d3445`  
		Last Modified: Wed, 06 Apr 2022 03:07:30 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac91b7b89acf45346424eaaf1a886e052f1268d574f2b04668d7897196225af7`  
		Last Modified: Wed, 06 Apr 2022 03:07:30 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; s390x

```console
$ docker pull maven@sha256:55207992a404ca24a645da19b991dcb40910b9e96466bdaf8ddfc42fd27e17ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250601617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644ffb6ab04f8d1baf4d1b92a8754e3a2f8b47adeb9b53f768d1fc0106c57da`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:59:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 22:59:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:59:43 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 22:59:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79572f5172c6a040591d34632f98a20ed148702bbce2f57649e8ac01c0d2e3db';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='f4d53a1753cdde830d7872c6a1279df441f3f9aeb5d5037a568b3a392ebce9c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9750e11721282a9afd18a07743f19c699b2b71ce20d02f3f0a906088b9ae6d9a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a27a4dc23dff38a5c21e5ba9b7efcf0aa5e14ace1a3b19bec53e255c487521';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43fb84f8063ad9bf6b6d694a67b8f64c8827552b920ec5ce794dfe5602edffe7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 22:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 22:59:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 05 Apr 2022 22:59:56 GMT
CMD ["jshell"]
# Wed, 06 Apr 2022 00:10:25 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:10:27 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 00:10:27 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 00:10:27 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 00:10:27 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 00:10:30 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 00:10:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 00:10:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 00:10:31 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 00:10:31 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 00:10:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 00:10:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51699acdfda16fb15da1b4991b6dfd17e93efc6061b51d2928578f56536bea0`  
		Last Modified: Tue, 05 Apr 2022 23:02:31 GMT  
		Size: 15.7 MB (15738318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40c71e9ecb72258f588c920e09d3f38dba846c508212115ab5a288e2b8c87d8`  
		Last Modified: Tue, 05 Apr 2022 23:02:40 GMT  
		Size: 168.4 MB (168352456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af7111e355ff2773cf2699134b7226dd9220485bb4633003f640a9c9b6f543`  
		Last Modified: Tue, 05 Apr 2022 23:02:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c2326095daf4e8907a15bdfef938e1e7a68154ece6290cd0bf93cdce0b9c80`  
		Last Modified: Wed, 06 Apr 2022 00:14:17 GMT  
		Size: 30.7 MB (30688198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9121476c381b3d3e272ba5d90f0121b7baea82497b084a378b82dca197c55696`  
		Last Modified: Wed, 06 Apr 2022 00:14:14 GMT  
		Size: 8.7 MB (8736360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21a27910e4345ad2cfb32c78628b67a117fbf68525d15ef75bdec995d0d98ef`  
		Last Modified: Wed, 06 Apr 2022 00:14:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b450f7b23ad9434c9fa828b648c40010ccfa1bb8c1b34bdb2447221220fba43`  
		Last Modified: Wed, 06 Apr 2022 00:14:13 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
