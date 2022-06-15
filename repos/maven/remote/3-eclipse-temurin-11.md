## `maven:3-eclipse-temurin-11`

```console
$ docker pull maven@sha256:eeb499f2e7874b55c53b908c28a2fb858cf85d0ee35d6053a465c9ae1316eaa3
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
$ docker pull maven@sha256:66aa51957dc3edb7d5df3a52566bd6aa771e61255c94cffb01fd0528259f8911
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267181054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf767ce53792114a517d21b3575ebd98f0c80701405b051701740dab5173cfca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 07 Jun 2022 04:58:51 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 18:20:51 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:20:51 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:20:52 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:20:52 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:21:00 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:21:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:21:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:21:00 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:21:00 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:21:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:21:00 GMT
CMD ["mvn"]
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
	-	`sha256:5736dd48da19497a4e00af87289580bb939875c21f9ca6bba9cdbe84ed4b882b`  
		Last Modified: Tue, 07 Jun 2022 05:04:24 GMT  
		Size: 21.8 MB (21816125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17fc020638a1418a84dc8902eb31b826ddf758bd7a9d8ef64d2fcccfed8dce0`  
		Last Modified: Wed, 15 Jun 2022 18:27:09 GMT  
		Size: 8.7 MB (8739491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3cee47475e8e2b1c60652e875c14ad3465052bb9b8eb6854120e625c9f13fd`  
		Last Modified: Wed, 15 Jun 2022 18:27:09 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334969d51a41b1c146a183640c2cfd55970abd9ec9f84a5e1bee6a453ca17558`  
		Last Modified: Wed, 15 Jun 2022 18:27:09 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; arm variant v7

```console
$ docker pull maven@sha256:d077999167759a9ab843c0eb9a6af368d56453c22e5668f35f89587999776138
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254795397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef05ff7c7d0c8f54d1ebd1104336b0691899b55ca9125351384ae71024d0f7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 07 Jun 2022 05:51:35 GMT
ADD file:26c86cfcbc153addbca421974e648a7af07234cb3f741bfb030aa0db90b6a7c6 in / 
# Tue, 07 Jun 2022 05:51:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 09:35:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 09:35:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 09:39:14 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 09:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 09:39:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 09:39:42 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 09:39:43 GMT
CMD ["jshell"]
# Tue, 07 Jun 2022 13:37:31 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 17:58:14 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 17:58:14 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 17:58:15 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 17:58:15 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 17:58:20 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 17:58:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 17:58:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 17:58:21 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 17:58:22 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 17:58:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 17:58:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5aeb313108e16ff98084efb2ae2830cbe915ea38b3e2fd1e32688dd9d8c11320`  
		Last Modified: Tue, 07 Jun 2022 05:56:03 GMT  
		Size: 27.0 MB (27017432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e86f99b55853443ad37a84176e0b454887e7e14e159111d0f3497767d20bb6`  
		Last Modified: Tue, 07 Jun 2022 09:51:59 GMT  
		Size: 11.7 MB (11713497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bea7a86c86ec90ec4749e118891a2f0eb58e1e0b10051309411e8d8c4367a9`  
		Last Modified: Tue, 07 Jun 2022 09:56:28 GMT  
		Size: 182.0 MB (181965581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bcf417553f092271b711562db068ec9e056908f7c661d29dca9efed85a9c90`  
		Last Modified: Tue, 07 Jun 2022 09:55:18 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7dd587fc419d267993a3a71676febca2f43ad76c6566b77ffeff71cb49d16f`  
		Last Modified: Tue, 07 Jun 2022 13:45:22 GMT  
		Size: 25.4 MB (25358017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c924c398c8bd500bc1ee907d6ddc88de284d508f009b2705349fe90c610c6b8`  
		Last Modified: Wed, 15 Jun 2022 18:03:20 GMT  
		Size: 8.7 MB (8739495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccf58db9dae46b3bd6252e7031a87b0b2cc799bce50b162d394efac4bb77abc`  
		Last Modified: Wed, 15 Jun 2022 18:03:17 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2d09255bcf16273fae4679340b83b2b3727b134c6425212d0a8b11c43457b5`  
		Last Modified: Wed, 15 Jun 2022 18:03:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9d791bfa380fc5657473d6bb405579a116b5c18e4945e83e30a07c5228c341b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261520430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b3674d3a29e9419d4fa4d7925526271c25b7a3d52a394c35edc3f14ec17e78`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 07 Jun 2022 09:49:49 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 18:42:36 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:42:36 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:42:37 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:42:38 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:42:41 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:42:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:42:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:42:45 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:42:46 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:42:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:42:47 GMT
CMD ["mvn"]
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
	-	`sha256:b168d5510eb72ef79dbb6d24841c17636e3cad128690798a6ecb54e6caf2afd0`  
		Last Modified: Tue, 07 Jun 2022 09:57:38 GMT  
		Size: 21.5 MB (21498549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fad99472301711c8a7d6b32c5f47596bc629f7c89d4ef4f1cafeb4d81ab46ed`  
		Last Modified: Wed, 15 Jun 2022 18:51:30 GMT  
		Size: 8.7 MB (8739462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e751e7df85820a7ec69618958737cedc02c303456a35043a1f8c003b2f2422d`  
		Last Modified: Wed, 15 Jun 2022 18:51:28 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56791e881b2b4f521dec704fe30576179819a2ed2245dc0b66f96e8d394cd26b`  
		Last Modified: Wed, 15 Jun 2022 18:51:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; ppc64le

```console
$ docker pull maven@sha256:52097bb9a748bf862fe318c48ca38de79c8165a9df98c249bffc4c7aa9d39fa1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273599084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d488b8bf03fefb840b8adee3c5a075360c41e4cab94c18e002cb91700db814ee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:28 GMT
ADD file:55691ac7d76af0fcfafc39ebd1e5a4f2d7018147d6db6f89812db33fbaffc2f9 in / 
# Fri, 29 Apr 2022 23:22:33 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:29:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Apr 2022 00:32:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:49 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Sat, 30 Apr 2022 00:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Apr 2022 00:34:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 00:34:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 30 Apr 2022 00:34:23 GMT
CMD ["jshell"]
# Sat, 30 Apr 2022 05:00:25 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 18:27:22 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:27:24 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:27:26 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:27:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:27:38 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:27:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:27:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:27:43 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:27:44 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:27:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:27:47 GMT
CMD ["mvn"]
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
	-	`sha256:5ad5133555776fbfb879be6c17f3d1bc09704bf41d6fe10992d20d1701860ee8`  
		Last Modified: Sat, 30 Apr 2022 00:46:50 GMT  
		Size: 176.0 MB (175969009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba9bdf8fa43c8ee68cd00fd9a61517cb39541fa41dda33fb8a64da5f31fe668`  
		Last Modified: Sat, 30 Apr 2022 00:46:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb0075a272673870bc08fd1790b2dd1fc202b5f12bcfc999c0c98bb398d7c1`  
		Last Modified: Sat, 30 Apr 2022 05:12:56 GMT  
		Size: 38.4 MB (38394414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d002b9a8eb1395b89ef0b5cadc8db987ee9abc174dc678dd7baa0b91eecb4ee`  
		Last Modified: Wed, 15 Jun 2022 18:35:23 GMT  
		Size: 8.7 MB (8739512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a7bb1f92da40a8a93f400d878a3a4d25dfa7b5534fd54cdec370d6eb4f22c8`  
		Last Modified: Wed, 15 Jun 2022 18:35:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ba81106fd1e825573ad24985dbc614ed5edbc0a6b41ef328301ba7b9f1dacc`  
		Last Modified: Wed, 15 Jun 2022 18:35:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; s390x

```console
$ docker pull maven@sha256:5749182cdabcca650164e90f7e1a187499139bbfc8f308e1c68a336db3283ec2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239971086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a873b244cf6a5c404e8f1fb4b8d2ac42618c3614889f73d71cfa74155ab164d8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 07 Jun 2022 10:09:38 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 15 Jun 2022 18:42:22 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:42:23 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:42:23 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:42:24 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:42:48 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:42:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:42:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:42:50 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:42:51 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:42:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:42:52 GMT
CMD ["mvn"]
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
	-	`sha256:dd4630026e707f2b08b50bd2df1c4e9e74bda3a37b3e0ab8a361281057606109`  
		Last Modified: Tue, 07 Jun 2022 10:19:44 GMT  
		Size: 22.0 MB (21951088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810a7f1641b39804615f3caa66094dcf151c9b41216c367133478cd1dd05ab52`  
		Last Modified: Wed, 15 Jun 2022 18:49:10 GMT  
		Size: 8.7 MB (8739481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756b765f0f3b3b1028d3244e986e2aa975db68307e19de08ed1cbd395985cfcb`  
		Last Modified: Wed, 15 Jun 2022 18:49:05 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da88cef6ea4afb0720f77e38cec6ac878c1ceea73ef2a495768948559b7a90`  
		Last Modified: Wed, 15 Jun 2022 18:49:05 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
