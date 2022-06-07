## `tomcat:9-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:43cb7102b59d106dbf32a348371ed3fd822ea942843ffba7601bee034177488b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:9-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:ad19c4ee69427b51bacb6de3c9d9d9c30b40c39e54406be589a8b1129d4bfdc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99085679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71ce7ee4bca8928bed226b09f12c7e623d00d3379ee26ef63da2d7fc7bcbac9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 07 Jun 2022 06:33:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:33:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:33:57 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:33:57 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:33:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:33:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:37:04 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:37:04 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 Jun 2022 06:37:04 GMT
ENV TOMCAT_VERSION=9.0.63
# Tue, 07 Jun 2022 06:37:05 GMT
ENV TOMCAT_SHA512=4b905018164026756bd36ab9fde8f6b21c886acb8e5255d93f8938491e4d375dd18b9fc58ee23e3d78b16e8b81271c1c998e5592beedcac632567c2ca9411c69
# Tue, 07 Jun 2022 06:37:05 GMT
COPY dir:20f764a2b35c7b34cb1367137b1fea5e5b275e6ff8224964dca39e5bf84bbbba in /usr/local/tomcat 
# Tue, 07 Jun 2022 06:37:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:37:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 Jun 2022 06:37:11 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 06:37:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fe291dee2402fdf3bf5d490f07785767d7babf6fc8e1475b2593994e2f738d`  
		Last Modified: Tue, 07 Jun 2022 06:51:50 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac20220ce082f2f8e8bdc1b578ebad3b5bbc0a6db8102f5fa70701190e1eda3b`  
		Last Modified: Tue, 07 Jun 2022 06:54:40 GMT  
		Size: 12.2 MB (12238347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93c7f6750d355f1e4dac83076077c3d9c5f1a8d2e87469240301452f47433a`  
		Last Modified: Tue, 07 Jun 2022 06:54:39 GMT  
		Size: 445.5 KB (445457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f81c75903b4ad6e26a7dc2e86fcaae5ff5feebc1f5f8e292a2a4303631b33`  
		Last Modified: Tue, 07 Jun 2022 06:54:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:8620b2315a3c8cf4db6658e23f2d99283b4fe5f6e393543a2cc3de2989520229
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91638960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fedb0945e5e531474bc9425fe19c27fe0eeb1ef2cf1dd64fc580698fab0d71e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 09:33:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 09:34:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 09:34:27 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 09:36:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 09:36:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 09:37:00 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 07 Jun 2022 14:04:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 14:04:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 14:05:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 14:05:01 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 14:05:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 14:05:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 14:11:14 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 14:11:15 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 Jun 2022 14:11:15 GMT
ENV TOMCAT_VERSION=9.0.63
# Tue, 07 Jun 2022 14:11:16 GMT
ENV TOMCAT_SHA512=4b905018164026756bd36ab9fde8f6b21c886acb8e5255d93f8938491e4d375dd18b9fc58ee23e3d78b16e8b81271c1c998e5592beedcac632567c2ca9411c69
# Tue, 07 Jun 2022 14:11:18 GMT
COPY dir:6a52970de0de8772660f7ce1c9ff54c8473b9cca67fc43989b15cecb10374d15 in /usr/local/tomcat 
# Tue, 07 Jun 2022 14:11:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 14:11:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 Jun 2022 14:11:32 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 14:11:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ae1d24c2862f98f09de4a24a053161044e470b33c4e92d9f9807726bf4d12d`  
		Last Modified: Tue, 07 Jun 2022 09:51:03 GMT  
		Size: 14.9 MB (14902076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf6fe02b53ccc8b78deef863b7b26d03b14913108901ebc6d8cd5cc1400eadf`  
		Last Modified: Tue, 07 Jun 2022 09:53:10 GMT  
		Size: 39.5 MB (39529944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0620a426f0f8f6d12f5672750f4f4959e9860c44da5ba54f4c057e0bbe7dd5`  
		Last Modified: Tue, 07 Jun 2022 09:52:48 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b9690293dff2f1daa7d1b0457bba4e0cd23756ed5cd526c3b1e677c0d596e3`  
		Last Modified: Tue, 07 Jun 2022 14:33:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096b6c8e61db42ae5a6680d513b477a73fe16b8a32d7758f30a06fcaf3f03350`  
		Last Modified: Tue, 07 Jun 2022 14:37:01 GMT  
		Size: 12.2 MB (12190775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136c37e0b61c3cb8370582d80703bd37d999a290e292f49cf710f96f853bb4d3`  
		Last Modified: Tue, 07 Jun 2022 14:36:56 GMT  
		Size: 423.1 KB (423062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb47a6374dadd5aa96dd804864ce584e06eabd3142cb6759b23b46904c7a4083`  
		Last Modified: Tue, 07 Jun 2022 14:36:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:46d657052481c63b0b48ad8fd19c9f4a99dcad27bfd802729cc5bc9fa18af540
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96339380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf24979741e08b81b1d77a77b29c097fd08afa7e26eba8bfb0f1ae3d2d952b3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 07 Jun 2022 10:55:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:55:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:55:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:55:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:55:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:55:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 11:01:14 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 11:01:15 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 Jun 2022 11:01:16 GMT
ENV TOMCAT_VERSION=9.0.63
# Tue, 07 Jun 2022 11:01:17 GMT
ENV TOMCAT_SHA512=4b905018164026756bd36ab9fde8f6b21c886acb8e5255d93f8938491e4d375dd18b9fc58ee23e3d78b16e8b81271c1c998e5592beedcac632567c2ca9411c69
# Tue, 07 Jun 2022 11:01:19 GMT
COPY dir:25ef455a6539541f805f14df3b4164eba364983637d3903836e9d775bf21ec94 in /usr/local/tomcat 
# Tue, 07 Jun 2022 11:01:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 11:01:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 Jun 2022 11:01:28 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 11:01:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a7f247e9cd3d2cf93714ef85ee591a156a2bb21a7b0e38ff07dcdee1da5b10`  
		Last Modified: Tue, 07 Jun 2022 11:27:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1679cbc1e88fa616645fbc98a022317cac8175d090c36dbd5f3e36e898f253`  
		Last Modified: Tue, 07 Jun 2022 11:31:18 GMT  
		Size: 12.3 MB (12254867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072f682bdf5b5d789582d156b6f9d76bd66b5d75994b98a6c610014639a8bb62`  
		Last Modified: Tue, 07 Jun 2022 11:31:17 GMT  
		Size: 208.8 KB (208819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:026f458d3b6e5fc8a55bd3722907653ad257eb8d035b74a607971596be08fdaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106527261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d74c61bff1094c37a1733095296a3d471f88153d9717bfd9fe28c46811e7f9`
-	Default Command: `["catalina.sh","run"]`

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
# Thu, 05 May 2022 18:19:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 05 May 2022 18:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 May 2022 18:19:18 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 05 May 2022 19:09:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 May 2022 19:09:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 May 2022 19:09:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 05 May 2022 19:09:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 May 2022 19:09:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 May 2022 19:09:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 May 2022 19:15:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 May 2022 19:15:06 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 May 2022 06:52:15 GMT
ENV TOMCAT_VERSION=9.0.63
# Wed, 18 May 2022 06:52:19 GMT
ENV TOMCAT_SHA512=4b905018164026756bd36ab9fde8f6b21c886acb8e5255d93f8938491e4d375dd18b9fc58ee23e3d78b16e8b81271c1c998e5592beedcac632567c2ca9411c69
# Wed, 18 May 2022 06:52:23 GMT
COPY dir:9df5c9eaa0bef11229a25e7a7aa98a3b3d387d29724bdb884ed670bc50e24598 in /usr/local/tomcat 
# Wed, 18 May 2022 06:52:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 May 2022 06:53:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 18 May 2022 06:53:05 GMT
EXPOSE 8080
# Wed, 18 May 2022 06:53:08 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:f52806fb57ec020c802a4f4cb502d02e7fe9f9e523ee2589b220cf2255dbaf21`  
		Last Modified: Thu, 05 May 2022 18:24:39 GMT  
		Size: 41.2 MB (41205891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c927ffc56d7be25073d4bf077485eea398ae7e563143fec34567a832e0bc4a24`  
		Last Modified: Thu, 05 May 2022 18:24:32 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddd318375d0abc69921071bad194d598355a079821bf6806470a863ff9e7495`  
		Last Modified: Thu, 05 May 2022 19:28:45 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3149364d703344c9d425bba640c32f2bcad237fb8fb959470767c45e93bdf6`  
		Last Modified: Wed, 18 May 2022 07:08:26 GMT  
		Size: 12.3 MB (12278016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a320ff9b44160f2a2741a8971afb9cb2ba40d7d439f5e1dc236357463232d81`  
		Last Modified: Wed, 18 May 2022 07:08:25 GMT  
		Size: 2.5 MB (2548112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbee80d4a0afc2f56fa7297f03dd4a2453513a461ce1c67c08eabf0b95721cf2`  
		Last Modified: Wed, 18 May 2022 07:08:24 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
