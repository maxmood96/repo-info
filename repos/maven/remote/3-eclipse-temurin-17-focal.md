## `maven:3-eclipse-temurin-17-focal`

```console
$ docker pull maven@sha256:b3ce394919af531fc4de6d7a6d4ce3056a417a24abac7cf99b7df47a0e622a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-eclipse-temurin-17-focal` - linux; amd64

```console
$ docker pull maven@sha256:958fb22cc41ea9d3d251cc2831a8aaacd958bfade9efa8eac861f6941eeb3fb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280667471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8164d4ce061c37227e540bf15301b5b24f69ee78406bffb16240ea8a5c1acb1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:45:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 18:45:47 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 24 Jan 2023 18:45:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 24 Jan 2023 18:45:59 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 24 Jan 2023 18:45:59 GMT
CMD ["jshell"]
# Tue, 24 Jan 2023 22:27:33 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 22:27:33 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 24 Jan 2023 22:27:33 GMT
ARG USER_HOME_DIR=/root
# Tue, 24 Jan 2023 22:27:33 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 24 Jan 2023 22:27:33 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 24 Jan 2023 22:27:41 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 24 Jan 2023 22:27:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 24 Jan 2023 22:27:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 24 Jan 2023 22:27:42 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 24 Jan 2023 22:27:42 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 24 Jan 2023 22:27:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 24 Jan 2023 22:27:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b0873b98ac8f32b151346adbb3bebb71422b7f4d491cef4fe8fa08d19bf076`  
		Last Modified: Fri, 09 Dec 2022 01:52:23 GMT  
		Size: 20.1 MB (20086897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913a94f7995a71a3b1494175b51281deca94259b3f33d1b889b6828a43bc4847`  
		Last Modified: Tue, 24 Jan 2023 18:53:46 GMT  
		Size: 192.4 MB (192447964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1814c42b0b96a6e17caef6e17636e6a2f4e79f91c150dee053df82dae54847`  
		Last Modified: Tue, 24 Jan 2023 18:53:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c62599bfb33056ad719f5484d9e87ec17996a4e9d1143068c1d5a5bc9b23f53`  
		Last Modified: Tue, 24 Jan 2023 22:30:50 GMT  
		Size: 31.2 MB (31203192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9012d8af7a1875ff942b982fa9e36db0ab7bde775be1773a4d092693b9c55d39`  
		Last Modified: Tue, 24 Jan 2023 22:30:46 GMT  
		Size: 8.4 MB (8351149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620be72c8c5c66e34992c9cfd73f1c73cfb4301ff6f72d053f3f01a95dd4eabc`  
		Last Modified: Tue, 24 Jan 2023 22:30:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148d145f44a14fb2ba5f71cfca090684743e2a92844165b4f57e2e2de8f0e25e`  
		Last Modified: Tue, 24 Jan 2023 22:30:45 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17-focal` - linux; arm variant v7

```console
$ docker pull maven@sha256:f0f9625e4900941575d1c688d7c31951f339a314659b09ddf6f347c888b2131b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269177258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce29950702e0b38c911c751d99887af02898923204943c52a0994cff816a2052`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 13:35:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:35:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:35:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:35:44 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:35:48 GMT
ADD file:6566d63937dd1808d3a4ea5591d4369b9083772d48fad60626fb91243a9f3f53 in / 
# Thu, 26 Jan 2023 13:35:49 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:54:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 18:54:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 18:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:58:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:58:11 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 31 Jan 2023 18:58:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 31 Jan 2023 18:58:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 31 Jan 2023 18:58:40 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 21:26:08 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 21:26:09 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 21:26:09 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 21:26:09 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 21:26:09 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 21:26:11 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 21:26:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 21:26:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 21:26:11 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 21:26:12 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 21:26:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 21:26:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:316383d79e03258e1fee780854f6da78da364194ded4ace8bff50687070e1c8f`  
		Last Modified: Sat, 28 Jan 2023 04:40:09 GMT  
		Size: 24.6 MB (24586318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59020c95c698b069ad035790b31d5e8574a7bb26babb8d738b030d57b30a69dd`  
		Last Modified: Tue, 31 Jan 2023 19:07:00 GMT  
		Size: 19.5 MB (19461566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb80340d86ea0e5c443144221d3d615ad5010d757e7a1a0ee234506fdb8ab46`  
		Last Modified: Tue, 31 Jan 2023 19:07:17 GMT  
		Size: 189.5 MB (189466708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e389aec4ec05918cb5c95352af985f1a507eea88ef1b09eef83b9588f1b626`  
		Last Modified: Tue, 31 Jan 2023 19:06:56 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242674503ed1282e81db9e844c2c46a7abd557262120ec1dfae1d43a5fb35177`  
		Last Modified: Tue, 31 Jan 2023 21:30:18 GMT  
		Size: 27.3 MB (27310148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef5aaa7c530e09023f4b39d8a49b7c704e565cf53b23ad579d636c6b4ed3ac4`  
		Last Modified: Tue, 31 Jan 2023 21:30:14 GMT  
		Size: 8.4 MB (8351130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15814ca89bef1fd864897d36bbc27f143db78dc268c22e9e5b6e38d525d6350e`  
		Last Modified: Tue, 31 Jan 2023 21:30:14 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28c8ac91675903f379095e56536ee638db9495e6cf8535aaca7f4d561765ba8`  
		Last Modified: Tue, 31 Jan 2023 21:30:14 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17-focal` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:47c72c648bf0a85fe53efafc7e5d7547eb697385f613939ecd651dd1b9c8725c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278851788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a27e9e8f97cde27f1ccaba5c67de90edee8a2d76b2a4d2ef90cfdb7bee7a3b7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:46:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:46:22 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 31 Jan 2023 17:46:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 31 Jan 2023 17:46:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 31 Jan 2023 17:46:44 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 22:05:50 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 22:05:51 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 22:05:51 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 22:05:51 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 22:05:51 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 22:05:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 22:05:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 22:05:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 22:05:57 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 22:05:57 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 22:05:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 22:05:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0d033864bdd7e6f8ce77794561b894a3182f3ad98291a8fbb57cfa287b05fc`  
		Last Modified: Tue, 31 Jan 2023 17:52:30 GMT  
		Size: 20.8 MB (20801392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7884a3ca5391adf5987a081f6aa024caf2daff1edc65da3adc8abc72fb0e6a1d`  
		Last Modified: Tue, 31 Jan 2023 17:52:40 GMT  
		Size: 191.3 MB (191267132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e4a62d03f5b6740085a5d6deafe9d0ef9dfcc5963023df7abc3bab16110fa0`  
		Last Modified: Tue, 31 Jan 2023 17:52:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a5a5d0730b9a5b3e6d03f5d6e587eb6d36b47365e9fc63acac6538c0372449`  
		Last Modified: Tue, 31 Jan 2023 22:09:28 GMT  
		Size: 31.2 MB (31236994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec79f2f2cfba555f1433d5c78aedd69e144e7f0ebbd8d16c1cc01a18126b110d`  
		Last Modified: Tue, 31 Jan 2023 22:09:25 GMT  
		Size: 8.4 MB (8351146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b588222a90d3343522cbb61cabcb6310694ea811016100ddc21ffeaa97ee1839`  
		Last Modified: Tue, 31 Jan 2023 22:09:24 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0a857f2c547eda254081b715b8c68afb08b4a40e19e33389a357f568f932d`  
		Last Modified: Tue, 31 Jan 2023 22:09:24 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17-focal` - linux; ppc64le

```console
$ docker pull maven@sha256:0db757f657755e028a8a0e5c15bc231a5f2c8992b2e884bdc56a6e54a6bfa5ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293943804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e9de1285702501393f1a4523ce37b6c33fa7c8d79abd8db48692f1ead899a2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 13:47:16 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:47:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:47:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:47:17 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:47:20 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Thu, 26 Jan 2023 13:47:20 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:22:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 18:22:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 18:22:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:26:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:26:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 31 Jan 2023 18:27:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 31 Jan 2023 18:27:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 31 Jan 2023 18:27:38 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 21:53:58 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 21:53:59 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 21:54:00 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 21:54:00 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 21:54:00 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 21:54:02 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 21:54:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 21:54:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 21:54:03 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 21:54:03 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 21:54:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 21:54:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321de75711a5e61ead0c176aa407094831cd0f968a12501dbf313197b0cc7db`  
		Last Modified: Tue, 31 Jan 2023 18:38:30 GMT  
		Size: 22.1 MB (22059654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8538a095d02d1deba63d0bd1d951b885a9ab8dc59f095ad63f0eca45e6a013a`  
		Last Modified: Tue, 31 Jan 2023 18:38:49 GMT  
		Size: 191.8 MB (191803994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897ebc0f4b0db70973fc2276cf1192bd5d5dc9144c8d9bd24ebe31850c7bd9aa`  
		Last Modified: Tue, 31 Jan 2023 18:38:24 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36ea66ad8e8cce2214627a7749e644563d311bf8b86369b364785381f2e232a`  
		Last Modified: Tue, 31 Jan 2023 22:01:17 GMT  
		Size: 38.4 MB (38427284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b62078bad6e378bab0c97d98a2f558ba216cad04260d6904dffda31dda3357`  
		Last Modified: Tue, 31 Jan 2023 22:01:08 GMT  
		Size: 8.4 MB (8351146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc730804d70d5c0eea50ead35bf6542c55a6b0cb7fe78b0438dd3bd8372a4ace`  
		Last Modified: Tue, 31 Jan 2023 22:01:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abb35236a965e59fab0c21a0b8d8b2aa49f5d2ca284b3c18d554cb461ddc24f`  
		Last Modified: Tue, 31 Jan 2023 22:01:07 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17-focal` - linux; s390x

```console
$ docker pull maven@sha256:80d6ee3ce22ad93edd9c4d467211835db85d5818012ceae7ec06f07cbe2bd019
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265910597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d614bcb62a52e03017df32fb7a1fc123265819398b7e79cfbd9017d1e8144`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 13:21:27 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:21:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:21:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:21:27 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:21:29 GMT
ADD file:4d5fa9b68af51e9c8cd7b25fb55ddd47256efb0b2eda9432507b72b7c1a17053 in / 
# Thu, 26 Jan 2023 13:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:58:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:58:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:58:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:00:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:00:26 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 31 Jan 2023 18:00:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='fe4d0c6d5bb8cf7f59f7ff82c0c1fd988bbe5cccf3bc7377dc8ae50740b46c82';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 31 Jan 2023 18:00:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 31 Jan 2023 18:00:40 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 19:46:45 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:46:46 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 19:46:47 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 19:46:47 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 19:46:47 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 19:46:56 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 19:46:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 19:46:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 19:46:56 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 19:46:57 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 19:46:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 19:46:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cbc0e1117f61ba365a9a02263b82c04f704d5d162aa31b25a9326797dd1c7084`  
		Last Modified: Tue, 31 Jan 2023 17:54:46 GMT  
		Size: 27.0 MB (27016130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a084dcc675ae7466af74202ec658f9b4c6bb684da36940b582a734cdbf94e0`  
		Last Modified: Tue, 31 Jan 2023 18:06:18 GMT  
		Size: 19.5 MB (19525912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2723fd9ff7a7c34ab13d715863a5a81fc78fffefe7acbec85b03691613f29017`  
		Last Modified: Tue, 31 Jan 2023 18:06:27 GMT  
		Size: 180.3 MB (180293734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84062b099902766b4e7baff19533207a4c46f6625a684baa209ffdad4074115`  
		Last Modified: Tue, 31 Jan 2023 18:06:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddf24ea83710d099b0204de5352c5b89277331b1d9ee0e0d9d0c854994e92a8`  
		Last Modified: Tue, 31 Jan 2023 19:51:22 GMT  
		Size: 30.7 MB (30722283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6261a72dd533111975e097abfb380ced711467add881ba977e58dbf2db98fa`  
		Last Modified: Tue, 31 Jan 2023 19:51:19 GMT  
		Size: 8.4 MB (8351149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc5dc9cb39bb3767d8cd45bb5d41b94aa082075abddb434812e67f825bdfba7`  
		Last Modified: Tue, 31 Jan 2023 19:51:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a549c74ac310fd6a5fcf4fc885c8295277fdcabce74651e749e4453cdaa7e56`  
		Last Modified: Tue, 31 Jan 2023 19:51:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
