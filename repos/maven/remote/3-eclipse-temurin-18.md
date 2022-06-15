## `maven:3-eclipse-temurin-18`

```console
$ docker pull maven@sha256:30598e8786a7cdb1487921be309d425634a8d75568a511135515095fcddffcc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-eclipse-temurin-18` - linux; amd64

```console
$ docker pull maven@sha256:b1ccf0a99bf1fc0dba01e873052f0787f9a4218146b95a72724cd00f0fcdec4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271188000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774058353578a415ef004d3f657f8d9ae8c6f0afe805098e22fd511974e97b47`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:16:52 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 07 Jun 2022 00:17:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37ceaf232a85cce46bcccfd71839854e8b14bf3160e7ef72a676b9cae45ee8af';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='0ddec3c165ab0b662a57a845db3fdaeb840660b493f164696b03df76aadf61c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7c3376b4eb14a58d27816776e965f1b214c17c4c2e918dc9e996a0f30e76550e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='236dc78e698c21f258078661ab5c74b8cc7d38a1febb7aa7a6598bd3b999c0dc';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='16b1d9d75f22c157af04a1fd9c664324c7f4b5163c022b382a2f2e8897c1b0a2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:17:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:17:16 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 04:59:50 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 18:21:43 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:21:43 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:21:43 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:21:43 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:21:48 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:21:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:21:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:21:48 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:21:49 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:21:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:21:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160c99d3182b28de91f5c2c165e40fe309db075058fa23129c7dc2b4e2852b0e`  
		Last Modified: Tue, 07 Jun 2022 00:22:32 GMT  
		Size: 16.7 MB (16660695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab586f60b77dab6d4d61e3d169edd10885322e98db0e6fbda7f3d8764f8652b`  
		Last Modified: Tue, 07 Jun 2022 00:24:13 GMT  
		Size: 193.5 MB (193544164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ae9d3fd34a2b481f72d80fcedc0ae35b742bba65dab88ea02fb5c1a18edc8`  
		Last Modified: Tue, 07 Jun 2022 00:23:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e5923c7cad229b0d7bc491b5f713abb89f27a30fd00beb30f4febc0b1fe6b2`  
		Last Modified: Tue, 07 Jun 2022 05:05:54 GMT  
		Size: 21.8 MB (21818549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631c3391ee9e4b45072ab3e8eb419430f6cd03b6fb023fa27b486d65af2cd242`  
		Last Modified: Wed, 15 Jun 2022 18:28:51 GMT  
		Size: 8.7 MB (8739504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c76d22a258069878224846d32f228214ed21ab610c7dd3a8f6f99a3428cfb4c`  
		Last Modified: Wed, 15 Jun 2022 18:28:50 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b836c050061989d980bb4838fba57d582982d0a7f9d491ed0e375d90da4c97d`  
		Last Modified: Wed, 15 Jun 2022 18:28:50 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-18` - linux; arm variant v7

```console
$ docker pull maven@sha256:ab13876fd1f0521c867d20cad17ae97b885e0153ecacab064f0d1eafa5d977a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268595071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f8605ecd71e733dedc56f4e672872e0ebd4da3a9400ed7a6e43447bbe6030e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 07 Jun 2022 05:51:35 GMT
ADD file:26c86cfcbc153addbca421974e648a7af07234cb3f741bfb030aa0db90b6a7c6 in / 
# Tue, 07 Jun 2022 05:51:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 09:35:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 09:43:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 09:45:32 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 07 Jun 2022 09:45:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37ceaf232a85cce46bcccfd71839854e8b14bf3160e7ef72a676b9cae45ee8af';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='0ddec3c165ab0b662a57a845db3fdaeb840660b493f164696b03df76aadf61c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7c3376b4eb14a58d27816776e965f1b214c17c4c2e918dc9e996a0f30e76550e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='236dc78e698c21f258078661ab5c74b8cc7d38a1febb7aa7a6598bd3b999c0dc';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='16b1d9d75f22c157af04a1fd9c664324c7f4b5163c022b382a2f2e8897c1b0a2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 09:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 09:46:02 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 09:46:02 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 13:40:54 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 17:59:56 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 17:59:57 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 17:59:57 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 17:59:57 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:00:07 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:00:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:00:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:00:08 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:00:08 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:00:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:00:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5aeb313108e16ff98084efb2ae2830cbe915ea38b3e2fd1e32688dd9d8c11320`  
		Last Modified: Tue, 07 Jun 2022 05:56:03 GMT  
		Size: 27.0 MB (27017432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5390c30522c8a66ee1b5710a648276f1950fd75410a08d08df5699afb754d`  
		Last Modified: Tue, 07 Jun 2022 09:59:39 GMT  
		Size: 16.8 MB (16819038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171347462429bd99a996f741f6c7dca4acf3cf832f093488236b0924167f3eca`  
		Last Modified: Tue, 07 Jun 2022 10:04:58 GMT  
		Size: 190.7 MB (190657686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4562cbd23c4e3137a4418d5cf9b412a3aac57bad4d9705109c0cac9cffbc47a2`  
		Last Modified: Tue, 07 Jun 2022 10:03:45 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a9efa6a20ad7f5fbda3bd1190ed8248902a2636b2faef98a5eca6e7f467954`  
		Last Modified: Tue, 07 Jun 2022 13:48:04 GMT  
		Size: 25.4 MB (25360051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07ab50f2f9ca71a00670dc8e5e95474515c2484915ff01e2bc4d7109a8f3964`  
		Last Modified: Wed, 15 Jun 2022 18:05:09 GMT  
		Size: 8.7 MB (8739486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bca337368cd2c6b8cdfe520a079bd43e441b7be977acfcff2bc93e1f7ac9c67`  
		Last Modified: Wed, 15 Jun 2022 18:05:06 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2dec696e66f1e55d0bbc65c733d02f14f13790be824df697473a4053327db7`  
		Last Modified: Wed, 15 Jun 2022 18:05:07 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9135b7a4f572350d0fb8aaf367f4937731b1d51c1a42fab82df9c1bdbf344e8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269089805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4cdbb79e4dd7a442aa4cf5271d396bad2f7dca3c5cdf261575803dcba98283`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:32 GMT
ADD file:20805b983efd5443e34ebdfb7795010e5684eb1ca1ffea30a3e61e0089c0eee8 in / 
# Tue, 07 Jun 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:34:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 06:37:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:38:42 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 07 Jun 2022 06:38:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37ceaf232a85cce46bcccfd71839854e8b14bf3160e7ef72a676b9cae45ee8af';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='0ddec3c165ab0b662a57a845db3fdaeb840660b493f164696b03df76aadf61c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7c3376b4eb14a58d27816776e965f1b214c17c4c2e918dc9e996a0f30e76550e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='236dc78e698c21f258078661ab5c74b8cc7d38a1febb7aa7a6598bd3b999c0dc';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='16b1d9d75f22c157af04a1fd9c664324c7f4b5163c022b382a2f2e8897c1b0a2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:38:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:38:52 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 09:52:07 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 18:44:00 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:44:01 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:44:02 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:44:03 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:44:06 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:44:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:44:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:44:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:44:11 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:44:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:44:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ed02c6ade914c2962413c1ad2ccc86ed8d1512098f2c87fe7bafa8e1b5293185`  
		Last Modified: Thu, 02 Jun 2022 08:38:25 GMT  
		Size: 28.4 MB (28378212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05b1ade9954ed8f53cec97e324b11b1651b87e1cc39bcaa916ed2a7aacc6c4`  
		Last Modified: Tue, 07 Jun 2022 06:45:20 GMT  
		Size: 18.1 MB (18092093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9015ccd422173bcb85af63c5c0360d4dc351b33d74e505469396b73643e2bd`  
		Last Modified: Tue, 07 Jun 2022 06:47:16 GMT  
		Size: 192.4 MB (192377858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0e55136e5959dfddaf4e118116b9eba51219f798f09f83600b13413b0cde3e`  
		Last Modified: Tue, 07 Jun 2022 06:46:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dfbc708bfa6be6829a1f517d2c919c947edf45448970f9aac16132a8e77089`  
		Last Modified: Tue, 07 Jun 2022 09:59:18 GMT  
		Size: 21.5 MB (21500859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e0c8765dd42ec11dd83dec27bf526b99c102586b43d428e589ea5da77d98ab`  
		Last Modified: Wed, 15 Jun 2022 18:53:01 GMT  
		Size: 8.7 MB (8739441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2696ba0b2723bc8e7e1e474dc5f470367d614323891a8c08beda8307943484ee`  
		Last Modified: Wed, 15 Jun 2022 18:53:00 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9878617d92e806df4fdf505f9752ff3ac8f1430a3fa9aecdf549f18e1749961`  
		Last Modified: Wed, 15 Jun 2022 18:53:00 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-18` - linux; ppc64le

```console
$ docker pull maven@sha256:04858d32f0c554c5e50a1d6216a09b66915e25f2efc51f78421c03146951fa30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (295031597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e5f61ddccd29b822cf7cfbe0dc1f74052434c7ef3aff90ee945a1254e318f9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:28 GMT
ADD file:55691ac7d76af0fcfafc39ebd1e5a4f2d7018147d6db6f89812db33fbaffc2f9 in / 
# Fri, 29 Apr 2022 23:22:33 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:29:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Apr 2022 00:39:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 04 May 2022 18:18:34 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 04 May 2022 18:19:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37ceaf232a85cce46bcccfd71839854e8b14bf3160e7ef72a676b9cae45ee8af';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='0ddec3c165ab0b662a57a845db3fdaeb840660b493f164696b03df76aadf61c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7c3376b4eb14a58d27816776e965f1b214c17c4c2e918dc9e996a0f30e76550e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='236dc78e698c21f258078661ab5c74b8cc7d38a1febb7aa7a6598bd3b999c0dc';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='16b1d9d75f22c157af04a1fd9c664324c7f4b5163c022b382a2f2e8897c1b0a2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 04 May 2022 18:19:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 May 2022 18:19:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 04 May 2022 18:19:15 GMT
CMD ["jshell"]
# Wed, 04 May 2022 18:51:55 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 18:29:58 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:30:01 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:30:03 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:30:05 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:30:11 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:30:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:30:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:30:16 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:30:17 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:30:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:30:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e9c0a77cb9f0f7330e3fc62254e4c8ae89ed4bba21209fdc1088195250f950b9`  
		Last Modified: Fri, 29 Apr 2022 23:25:23 GMT  
		Size: 33.3 MB (33290661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78469566e7f98d05da9b7bb014ec6ce7170e52dbf51ed022fc29dbb9212a0e38`  
		Last Modified: Sat, 30 Apr 2022 00:47:36 GMT  
		Size: 21.7 MB (21692524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804a203bfc2159f5bdabd1ce28bd1736be67ec217ad81a8e03c559fa63d61564`  
		Last Modified: Wed, 04 May 2022 18:24:46 GMT  
		Size: 192.9 MB (192911548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972be1e1be17cab814c3185e0f99dfb8ed35074b247e45189ab403c52100e9b4`  
		Last Modified: Wed, 04 May 2022 18:24:24 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bef91f4ddb35d698916df92bfa2458c2790eedacaa62e97bbe7fb7cc33a8e0c`  
		Last Modified: Wed, 04 May 2022 18:54:44 GMT  
		Size: 38.4 MB (38395991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2ab9ba5acaa2587daab39f8a6d544dc390248eda9d0a420a09885c92127ca`  
		Last Modified: Wed, 15 Jun 2022 18:37:01 GMT  
		Size: 8.7 MB (8739498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e065d97ce0205b8a9debceb63dd1524512e6bc4f15ca37bc6c66a32b7d15c905`  
		Last Modified: Wed, 15 Jun 2022 18:37:00 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c041e1f26b6a7daac07f4b075e63d9fc3e64e42a9b09194fb203c48120b47`  
		Last Modified: Wed, 15 Jun 2022 18:37:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-18` - linux; s390x

```console
$ docker pull maven@sha256:bb312f28a74f8d610e238f0c760fd4a500a3fa5583feb955cd5bac18f8aaf59d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257233660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d67a2450fedff5ae5a40fd70296dbe2410741cfa37075e4c16e824b764fc4ae`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 07 Jun 2022 04:05:41 GMT
ADD file:5412b0d16961079a78b96411ca23f1838ac09c2fae839829476380b5389e49f8 in / 
# Tue, 07 Jun 2022 04:05:45 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:33:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 06:37:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:39:51 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 07 Jun 2022 06:40:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37ceaf232a85cce46bcccfd71839854e8b14bf3160e7ef72a676b9cae45ee8af';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='0ddec3c165ab0b662a57a845db3fdaeb840660b493f164696b03df76aadf61c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7c3376b4eb14a58d27816776e965f1b214c17c4c2e918dc9e996a0f30e76550e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='236dc78e698c21f258078661ab5c74b8cc7d38a1febb7aa7a6598bd3b999c0dc';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='16b1d9d75f22c157af04a1fd9c664324c7f4b5163c022b382a2f2e8897c1b0a2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:40:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:40:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:40:18 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 10:14:02 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 18:44:55 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:44:56 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:44:56 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:44:57 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:45:17 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:45:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:45:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:45:20 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:45:21 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:45:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:45:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6fa1296f44090f6150dfb96d6ae217a58b9d66c56d7a986c35657df6bd1a89f0`  
		Last Modified: Tue, 07 Jun 2022 04:08:13 GMT  
		Size: 28.6 MB (28638482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd8c93abff5baf988449855146fa80db180ea7004a449308cc565413cfd99c9`  
		Last Modified: Tue, 07 Jun 2022 06:44:14 GMT  
		Size: 16.4 MB (16427939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208b96bbb25ded5cea1d65791cf55fb0dc78de7b9d452b9d5f8a7ec9c850170`  
		Last Modified: Tue, 07 Jun 2022 06:45:32 GMT  
		Size: 181.5 MB (181473257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962cb96025c468ff4ec5c9b7a52bdbd1b13070511f3915880e2f923313475975`  
		Last Modified: Tue, 07 Jun 2022 06:45:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e81697dccccad6364e1e4fe016c6d553c5cd62e17098d5b15ab1128cff0b0b`  
		Last Modified: Tue, 07 Jun 2022 10:21:08 GMT  
		Size: 22.0 MB (21953096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6192fb0375580dbe4f863564e56b6bd4dd2b2dee787089ade7bd12cbd555eb5e`  
		Last Modified: Wed, 15 Jun 2022 18:53:58 GMT  
		Size: 8.7 MB (8739506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996adc04fe3df5a45fd88f166b15c27b31b82a3dde8ceaea4385741ff0329bda`  
		Last Modified: Wed, 15 Jun 2022 18:53:50 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa725366647f2f4a0e5bdd3b1bd39b69189b2f2a23e4e0a98faeeef61135719`  
		Last Modified: Wed, 15 Jun 2022 18:53:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
