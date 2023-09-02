## `tomcat:10-jre17-temurin`

```console
$ docker pull tomcat@sha256:0337c5478c1774d7d0b3874e3d658edba43fdea193372c0c07ae905be8f08653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:10-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:13f7fcf35b9135ecbec1295a6c1ca08f7263ccbaa4487302c2d73ddc31c680f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107771651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6680c6ac09353e76b355ea2555fff07a436ab058c2d024295ab21ab9da357ade`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:39:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 15:39:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 15:39:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 15:40:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:24:02 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:25:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:25:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:25:09 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:25:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 22:28:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Aug 2023 22:28:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 22:28:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 31 Aug 2023 22:28:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Aug 2023 22:28:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:28:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:28:52 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 31 Aug 2023 22:28:52 GMT
ENV TOMCAT_MAJOR=10
# Thu, 31 Aug 2023 22:28:52 GMT
ENV TOMCAT_VERSION=10.1.13
# Thu, 31 Aug 2023 22:28:52 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Thu, 31 Aug 2023 22:28:53 GMT
COPY dir:eb1291745200d42d9ab8842d15883eab70869cf20f27334147d4a1c16de52879 in /usr/local/tomcat 
# Thu, 31 Aug 2023 22:28:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 22:28:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 31 Aug 2023 22:28:58 GMT
EXPOSE 8080
# Thu, 31 Aug 2023 22:28:58 GMT
ENTRYPOINT []
# Thu, 31 Aug 2023 22:28:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5980221a1ce1b53ecf2261f165c9bf6a24b845a2418dcf3c7aaf2f3f9e43f2a`  
		Last Modified: Wed, 16 Aug 2023 15:44:40 GMT  
		Size: 17.5 MB (17456341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead612da80830f54db1bf14a89e7949d387f06b604d9b00ea670ed5538a6eeda`  
		Last Modified: Thu, 31 Aug 2023 20:32:28 GMT  
		Size: 47.2 MB (47209809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01003f4f890000b41a2694af879d44ec9c63bc8a84bba0ca84be2f2aae1becba`  
		Last Modified: Thu, 31 Aug 2023 20:32:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2a6749e2c7ade859f74148ee754bd4889ac27d13724e882fd92951731a5fd`  
		Last Modified: Thu, 31 Aug 2023 20:32:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981aa7554e8e58bc1483e5cfe15aea286428aa691496ee3399276acadee77aee`  
		Last Modified: Thu, 31 Aug 2023 22:40:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f120b881cb10344dd082b7480e1c50f04ecfe90e9a45645a8e86c0fe9ce133c`  
		Last Modified: Thu, 31 Aug 2023 22:40:16 GMT  
		Size: 12.2 MB (12207956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52e421eb9aa5ec2400ef29e5e19e6cf4e5e21c6f874763d43d73544f8503203`  
		Last Modified: Thu, 31 Aug 2023 22:40:15 GMT  
		Size: 458.4 KB (458388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141fb210d7568f41e794c03d8187ce8aa670afd9f77a2effb3cac8a7e3a37ab4`  
		Last Modified: Thu, 31 Aug 2023 22:40:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:9979a7f7e38504d28b0bbe7d5bf5f854508faf3ff9da72a2299040535e45b529
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101952203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9692996c2ef6741e0773456487c99b5fe420a1dcbe09d237fb10a4a9e64c23`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:08:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:08:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:08:32 GMT
ADD file:e61c6bbfc8728cb119b4cfd4a35d1e5aad76e84c0ac8f2ff9850a7ceec9f3dc5 in / 
# Wed, 16 Aug 2023 06:08:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:34:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Sep 2023 23:34:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Sep 2023 23:34:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Sep 2023 23:36:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:36:59 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 01 Sep 2023 23:37:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 01 Sep 2023 23:37:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 01 Sep 2023 23:37:23 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Sep 2023 23:37:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 00:29:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 00:29:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:29:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 00:29:32 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 00:29:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 00:29:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 00:29:33 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 02 Sep 2023 00:29:33 GMT
ENV TOMCAT_MAJOR=10
# Sat, 02 Sep 2023 00:29:33 GMT
ENV TOMCAT_VERSION=10.1.13
# Sat, 02 Sep 2023 00:29:33 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Sat, 02 Sep 2023 00:29:34 GMT
COPY dir:f650008cc5e5080d982c7d56cb019b6d205df847e350b9465d2c3b07f0fc381c in /usr/local/tomcat 
# Sat, 02 Sep 2023 00:29:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:29:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 00:29:39 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 00:29:39 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 00:29:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5987bac23899c422dbd7b7045113aa103f4d6856141a3f9098850e6328563e42`  
		Last Modified: Wed, 16 Aug 2023 13:31:19 GMT  
		Size: 27.0 MB (27027892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e9acc4ff89dd25ddc04510a1667d2cf420b52814b7c376e3b25c38dbf201ac`  
		Last Modified: Fri, 01 Sep 2023 23:39:04 GMT  
		Size: 17.6 MB (17587964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18ab784f328592b09d0ca3a26d5a8bce4c571a22d8289ef2103d482fbf21cd4`  
		Last Modified: Fri, 01 Sep 2023 23:39:30 GMT  
		Size: 44.7 MB (44720390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33ff0f9f97ebabcc3e2f9cba35d2d63cab31ddb8204d8a0ad2bae8745792684`  
		Last Modified: Fri, 01 Sep 2023 23:39:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbbaa3e1f96a5afce2f13479511ce8271a558cd1a341a748dcebe052160b737`  
		Last Modified: Fri, 01 Sep 2023 23:39:23 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25ae046a9e60561359a20a61933594213ace12db6d62777a4f279b93ec3137c`  
		Last Modified: Sat, 02 Sep 2023 00:37:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c89cea1728cc9619b77a31c373c0c9047fb892fd9b1029d4b2dcc27ff439ace`  
		Last Modified: Sat, 02 Sep 2023 00:37:02 GMT  
		Size: 12.2 MB (12182551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517d8a9df439569d69d2551914923db0639ded3af7ed8cf8783b9df0e83cac5e`  
		Last Modified: Sat, 02 Sep 2023 00:37:00 GMT  
		Size: 432.2 KB (432213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4794a5c5bf12d2c9411c162334cb862f8335ec9fb81586db8f436b2705ba3d68`  
		Last Modified: Sat, 02 Sep 2023 00:37:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:34ca2a65a1ce80aa48c3dcd461ea6e1d07fb637b4c0b609049cfbab008c6e211
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106584316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523a6b4b27210e6e27b1d1d0b807a8dd856299cb69abadda4a0c400d0ad68953`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:28:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Sep 2023 23:28:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Sep 2023 23:28:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Sep 2023 23:30:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:30:13 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 01 Sep 2023 23:30:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 01 Sep 2023 23:30:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 01 Sep 2023 23:30:40 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Sep 2023 23:30:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 02:01:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 02:01:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 02:01:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 02:01:29 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 02:01:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:01:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:01:29 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 02 Sep 2023 02:01:29 GMT
ENV TOMCAT_MAJOR=10
# Sat, 02 Sep 2023 02:01:29 GMT
ENV TOMCAT_VERSION=10.1.13
# Sat, 02 Sep 2023 02:01:29 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Sat, 02 Sep 2023 02:01:29 GMT
COPY dir:eacee1db627332768197d2a3ef4fcaa6e5d7584f5d76bdcf2ba996e529d2fd0c in /usr/local/tomcat 
# Sat, 02 Sep 2023 02:01:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 02:01:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 02:01:34 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 02:01:34 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 02:01:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bccb525aef23b375cbcff84a9e7861c44ea0c0abcb727d4a15c43403b3bf22`  
		Last Modified: Fri, 01 Sep 2023 23:33:13 GMT  
		Size: 18.9 MB (18859695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7073102534bbdab86f9064e784ab0da9e714df01832daf28c9a0e0879b9766`  
		Last Modified: Fri, 01 Sep 2023 23:33:39 GMT  
		Size: 46.7 MB (46662517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95dea0a414858e69744d7a1b6f6cae01c0b221d826f8d5223b911fe75719ec06`  
		Last Modified: Fri, 01 Sep 2023 23:33:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752397543fbdf2a53040baf81807321724c9cb178fa38e5ee410e4fe6032bb68`  
		Last Modified: Fri, 01 Sep 2023 23:33:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21e7a379eb196fa5e4b61d11c0cc3e01a04dfe11d367b46efb8d32fa39c992c`  
		Last Modified: Sat, 02 Sep 2023 02:09:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e15d345c3ca026604a49ba4086733183cb42999b61ef062e54359fe531737f9`  
		Last Modified: Sat, 02 Sep 2023 02:09:22 GMT  
		Size: 12.2 MB (12208652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880879a5408b008c6722f1358addc6c48f88f290b445b24912452cc148039655`  
		Last Modified: Sat, 02 Sep 2023 02:09:21 GMT  
		Size: 459.3 KB (459279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b9099c926dbac5b085aa5a9ff389c624a858fa5e41f7af8e3d0bcb1b6ab502`  
		Last Modified: Sat, 02 Sep 2023 02:09:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:228d4eb03b883a96b4e9f0806911f712d583c2e5b3b110d917e2b5881c0352ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114201699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a6a156b57ba8c0ba3955d10a840104601e1e798a6e9b2ca9c5300ac72e43f5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:03:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 00:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:03:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Sep 2023 00:06:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:06:41 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Sat, 02 Sep 2023 00:07:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Sep 2023 00:07:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 02 Sep 2023 00:07:41 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Sep 2023 00:07:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 02:16:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 02:16:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 02:16:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 02:16:47 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 02:16:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:16:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:16:48 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 02 Sep 2023 02:16:48 GMT
ENV TOMCAT_MAJOR=10
# Sat, 02 Sep 2023 02:16:49 GMT
ENV TOMCAT_VERSION=10.1.13
# Sat, 02 Sep 2023 02:16:49 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Sat, 02 Sep 2023 02:16:50 GMT
COPY dir:beb30acd294a561bc14a99d94dd9d216c13a0e39f8471a9f6388e7b245c47626 in /usr/local/tomcat 
# Sat, 02 Sep 2023 02:17:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 02:17:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 02:17:05 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 02:17:06 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 02:17:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5d4cfc5435802883c4aaa9fa4afcc1b07f40e20bee68f058f0671804ab6bc3a0`  
		Last Modified: Sat, 02 Sep 2023 00:08:58 GMT  
		Size: 35.7 MB (35705651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cf6ea565778c3d8bea7e7e22e09a388b4e63b84893d5323563a7fb240485b0`  
		Last Modified: Sat, 02 Sep 2023 00:10:54 GMT  
		Size: 18.7 MB (18729609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3340461a79a4d9bffef028dea64af59cd1e93ccfb6a5baec05e5554f84b6abba`  
		Last Modified: Sat, 02 Sep 2023 00:11:40 GMT  
		Size: 47.1 MB (47054882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a02e00b3d8990b397d714688a4a656fbe67c93745fc43a6209a57a468a47fb9`  
		Last Modified: Sat, 02 Sep 2023 00:11:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e852b42b680d46d59d1c29633809e7da4869fa8886c262a39a20ac3215a5850b`  
		Last Modified: Sat, 02 Sep 2023 00:11:29 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e56abbfdffad4d7e17a4b208f6cac967f6f5ee60748860ba6d90cc15b1445b`  
		Last Modified: Sat, 02 Sep 2023 02:39:01 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3ec023f47a4b781358acc7e52f08effbb97005d20f209713fa0ae6a7b53f9`  
		Last Modified: Sat, 02 Sep 2023 02:39:02 GMT  
		Size: 12.2 MB (12220778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f0385812203e54a54c7f0aefe9b9caac09a4d51c03a91b10c2e9a8e3126430`  
		Last Modified: Sat, 02 Sep 2023 02:39:01 GMT  
		Size: 489.6 KB (489582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c23441edf3f4164d29b44869884aa826e1e1a17e1becc61e9a5f562611c429c`  
		Last Modified: Sat, 02 Sep 2023 02:39:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:f0346a1a7d641b5dacbece017dda2e560b78ca8a208f0ad750c9efd69729781b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102432289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea1aa55cae7341e909d7642ac27bed21536b915d1d0d0dd3c50a8aeb84611ba`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:26:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Sep 2023 23:26:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Sep 2023 23:26:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Sep 2023 23:27:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:27:38 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 01 Sep 2023 23:28:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 01 Sep 2023 23:28:26 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 01 Sep 2023 23:28:26 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Sep 2023 23:28:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 00:28:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 00:28:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:28:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 00:28:30 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 00:28:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 00:28:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 00:28:30 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 02 Sep 2023 00:28:30 GMT
ENV TOMCAT_MAJOR=10
# Sat, 02 Sep 2023 00:28:30 GMT
ENV TOMCAT_VERSION=10.1.13
# Sat, 02 Sep 2023 00:28:30 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Sat, 02 Sep 2023 00:28:31 GMT
COPY dir:bdb2e0b554034276631b35f0abe85f7408bf8c6da899ded9828f308c94dffbb9 in /usr/local/tomcat 
# Sat, 02 Sep 2023 00:28:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:28:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 00:28:37 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 00:28:38 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 00:28:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e19a32372cc8a39496c7cbc80d6c7213997c1b24d50309e770a59738f35c719d`  
		Last Modified: Fri, 01 Sep 2023 23:23:30 GMT  
		Size: 28.6 MB (28645834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351bc6a2ce88dd5072fe74c40fe5a76147b4c44751fb62974f74bd1eaf40aafb`  
		Last Modified: Fri, 01 Sep 2023 23:29:38 GMT  
		Size: 17.3 MB (17255550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47038c1ad39d71dbbafe6c35f26aa34765647d8fbe02d71c73dc80ab22dbe0ed`  
		Last Modified: Fri, 01 Sep 2023 23:30:01 GMT  
		Size: 43.9 MB (43861255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc75b4cca7acde8cda5f7536df6c8a48695c8ae1905d60fe900f7be894296ca2`  
		Last Modified: Fri, 01 Sep 2023 23:29:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba2fb6df7c842dc604e4626020a401063dcf743892d8bbad2e31d74dae2a007`  
		Last Modified: Fri, 01 Sep 2023 23:29:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e191d963a094da6304a57a701f56643a2e2aaf7c157be1044514f1d45815b85d`  
		Last Modified: Sat, 02 Sep 2023 00:36:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b032815aa227791777335ef5c13a416065915e66cb3c11743cc8a0bffa3e2f`  
		Last Modified: Sat, 02 Sep 2023 00:36:02 GMT  
		Size: 12.2 MB (12208618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95f6efc8369a301f20bf18d1a94c87f7d0f0711a8808cfad0a7e6e50a985173`  
		Last Modified: Sat, 02 Sep 2023 00:36:02 GMT  
		Size: 459.8 KB (459836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d2041ec1334184e8040c64c18171736a92dbeb50243bc6f509580443c223d2`  
		Last Modified: Sat, 02 Sep 2023 00:36:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
