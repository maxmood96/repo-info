## `tomcat:jre17-temurin`

```console
$ docker pull tomcat@sha256:f4589bbd9a7daf975bbcb34f87460ac9897b68a66e9ba2bf48f8d28ec32732c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:5c096dd1199078ff3257a4dfa76f92789684b17d3319596e8f8ebfca48808e2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107857897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443a82c8c29456789be8c5fbcb067f4923e31d18c70b8cc7b2ba032c197b5666`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:48:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2024 04:48:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:48:48 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2024 04:48:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2024 04:48:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 04:48:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 04:48:49 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 16 Feb 2024 04:48:49 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Feb 2024 04:48:49 GMT
ENV TOMCAT_VERSION=10.1.18
# Fri, 16 Feb 2024 04:48:49 GMT
ENV TOMCAT_SHA512=56d1478501bd63945aae08d9f7c1fd37e14761dd9606a3bf5996870256b542b561a354fb89c4693c5695d0f13fa217028115b311d50b4ecec03acc7785006638
# Fri, 16 Feb 2024 04:48:49 GMT
COPY dir:c19ef26617704a5fd61dcd1db55a8ef0a362d74a540ee3b310face7e902cd2d5 in /usr/local/tomcat 
# Fri, 16 Feb 2024 04:48:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:48:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2024 04:48:55 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 04:48:55 GMT
ENTRYPOINT []
# Fri, 16 Feb 2024 04:48:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b633af09da77b3268755d4a1d9c430a50ad0a131e1b2ecdb997e3ee6a86978f`  
		Last Modified: Fri, 16 Feb 2024 05:02:20 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23b62d3ea113be6dc4b0d74998dd079074ec0c5307df0954b3c22e578e9a4a5`  
		Last Modified: Fri, 16 Feb 2024 05:02:21 GMT  
		Size: 12.3 MB (12326300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0442e01198f87a4a25b72c84da5fff5296a137944e4b86558d75d24410cab7a`  
		Last Modified: Fri, 16 Feb 2024 05:02:20 GMT  
		Size: 458.6 KB (458594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fa94b93a037d7ad22784c87df330230a814d3956826948c73f38dd70e32909`  
		Last Modified: Fri, 16 Feb 2024 05:02:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:4caa3db5eb4feb524a236c37fe9ae5e6a92f6f15e46526dea5d94539553847ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102657971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680af7aba4fe183fc8f94add04c22eaaa1b2982b7993aed2357870f88667e903`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:00 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:20 GMT
ADD file:6767efafdb51cef2acde13d723fa618ffb3cd2155983115496c43ae730e762e6 in / 
# Tue, 13 Feb 2024 10:08:21 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 07:39:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:39:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:39:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 07:41:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 07:41:19 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 07:41:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 07:41:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 07:41:48 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 07:41:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 09:50:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2024 09:50:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 09:50:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2024 09:50:08 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2024 09:50:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 09:50:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 09:50:09 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 16 Feb 2024 09:50:10 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Feb 2024 09:50:10 GMT
ENV TOMCAT_VERSION=10.1.18
# Fri, 16 Feb 2024 09:50:10 GMT
ENV TOMCAT_SHA512=56d1478501bd63945aae08d9f7c1fd37e14761dd9606a3bf5996870256b542b561a354fb89c4693c5695d0f13fa217028115b311d50b4ecec03acc7785006638
# Fri, 16 Feb 2024 09:50:11 GMT
COPY dir:e5d0510aa86144d1bd9a5702a511be902e0d5b8fde2880014618b0091d8368dd in /usr/local/tomcat 
# Fri, 16 Feb 2024 09:50:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 09:50:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2024 09:50:21 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 09:50:21 GMT
ENTRYPOINT []
# Fri, 16 Feb 2024 09:50:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:469ff1e358fe0665e6d5ee032bad43f71c0f28f2231f273ce387dcaaaabf733e`  
		Last Modified: Wed, 14 Feb 2024 02:35:21 GMT  
		Size: 27.5 MB (27532464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e772b5c9a5ba5b718084e53d8d023f0ae531de7e351cc19a4982c01a4b41a76`  
		Last Modified: Fri, 16 Feb 2024 07:43:40 GMT  
		Size: 17.6 MB (17592912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b022ee625596e3739bd37edce11492ee30b887ee03ecfda347adad2d41e3719`  
		Last Modified: Fri, 16 Feb 2024 07:44:08 GMT  
		Size: 44.8 MB (44798876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d14fff6bad669ccfd42b40ec388261e0966a749c42eff32e55ec9aae647673e`  
		Last Modified: Fri, 16 Feb 2024 07:44:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5bd39c66ca3c30eb63a02eff2092ca19b8d79a0898c55db23b7f3b194f910e`  
		Last Modified: Fri, 16 Feb 2024 07:44:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ce0364bd4edca128bfd0a83a84713b5576a90a4d2eed28c79ae17605780bbc`  
		Last Modified: Fri, 16 Feb 2024 10:02:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32496d6965949ad810f1d1cff39475b82a81f82251fe7ff011390e8d782aadd`  
		Last Modified: Fri, 16 Feb 2024 10:02:26 GMT  
		Size: 12.3 MB (12298990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e987da07eb563ac05566c93d2aaa2638755a8f380dfd6888daf77933c1f64c2f`  
		Last Modified: Fri, 16 Feb 2024 10:02:24 GMT  
		Size: 433.5 KB (433534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad9a5e25e58c5e5354fccc82672be8ee65f44e5381672cf294343d1c7748c95`  
		Last Modified: Fri, 16 Feb 2024 10:02:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:01dd50af8c027957bb390ebb5f82485ee0b3c54fe9e8177e533a127e7b514e8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106685882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce252e191a4d1e569a255869f3d40c361b1ebabe14c64d81a468fa854f6c02a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:51:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 04:51:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:51:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 04:52:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:52:49 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 04:53:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 04:53:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 04:53:10 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 04:53:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 07:29:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2024 07:29:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:29:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2024 07:29:56 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2024 07:29:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 07:29:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 07:29:56 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 16 Feb 2024 07:29:56 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Feb 2024 07:29:56 GMT
ENV TOMCAT_VERSION=10.1.18
# Fri, 16 Feb 2024 07:29:56 GMT
ENV TOMCAT_SHA512=56d1478501bd63945aae08d9f7c1fd37e14761dd9606a3bf5996870256b542b561a354fb89c4693c5695d0f13fa217028115b311d50b4ecec03acc7785006638
# Fri, 16 Feb 2024 07:29:56 GMT
COPY dir:37bef54b63f121fc5b1981c6eccbe5ef4cb2537f3714ee4280292dcc186b2c04 in /usr/local/tomcat 
# Fri, 16 Feb 2024 07:30:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 07:30:01 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2024 07:30:02 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 07:30:02 GMT
ENTRYPOINT []
# Fri, 16 Feb 2024 07:30:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bac6b544c281c39df6cde20776732e9b89dbfbbbb49870c60c9af5ef1df471`  
		Last Modified: Fri, 16 Feb 2024 04:55:46 GMT  
		Size: 18.9 MB (18860590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244992bb9e51f456f3e5c927182054789a275d47eba65099182705a8e1952dc2`  
		Last Modified: Fri, 16 Feb 2024 04:56:12 GMT  
		Size: 46.6 MB (46639325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e543faa97f71ea4edea5a6153e1b82e4e9143354356435ca0a085c427b9b07e`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b734e973751dd4636bc278f0ef5ee31fc8e10cc65a07ebd5ef57aa728870187`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834bcd95e101783ee58afe3b6ea7c1050d27b18b749f6b70e0bcbce490b2298e`  
		Last Modified: Fri, 16 Feb 2024 07:41:13 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e72f420782b5f3144ca5322b8451e05714bab3c79f29d5408bfc14027e8d58`  
		Last Modified: Fri, 16 Feb 2024 07:41:14 GMT  
		Size: 12.3 MB (12327323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ab3a95a1554a420258daff3aab0b40f1c855953a21792e9fb508c7d62e9ad4`  
		Last Modified: Fri, 16 Feb 2024 07:41:13 GMT  
		Size: 457.1 KB (457126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c259946cd410878046f55268686f54e32a90acfcd2ecc46fac41bfc4887d8d4`  
		Last Modified: Fri, 16 Feb 2024 07:41:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:27bc298744cb5891e341c2ca2785efebe1786edef51618328849d7e7900d7783
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114197167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546b6e9df82a173ae425c3b6cf44df7eb8a7823c91165e3f5e5678eda3316b6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 03:01:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 03:01:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 03:03:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:03:54 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 03:04:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 03:04:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 03:04:41 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 03:04:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:56:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2024 04:56:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:56:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2024 04:56:19 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2024 04:56:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 04:56:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 04:56:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 16 Feb 2024 04:56:20 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Feb 2024 04:56:20 GMT
ENV TOMCAT_VERSION=10.1.18
# Fri, 16 Feb 2024 04:56:20 GMT
ENV TOMCAT_SHA512=56d1478501bd63945aae08d9f7c1fd37e14761dd9606a3bf5996870256b542b561a354fb89c4693c5695d0f13fa217028115b311d50b4ecec03acc7785006638
# Fri, 16 Feb 2024 04:56:21 GMT
COPY dir:5ff969023c91d75abe33b819647d6d622f3e3aeab5254d0977e2a37f1f0a5ffc in /usr/local/tomcat 
# Fri, 16 Feb 2024 04:56:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:56:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2024 04:56:31 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 04:56:31 GMT
ENTRYPOINT []
# Fri, 16 Feb 2024 04:56:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc402319b10feb1c6820fa2bc7cfba7869a3473e27191ab283db519e7e6da50`  
		Last Modified: Fri, 16 Feb 2024 03:08:21 GMT  
		Size: 18.7 MB (18726189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f9bec281d586fe857a730cd40136459428c7ccefda7ad98a1e0c5194e2d295`  
		Last Modified: Fri, 16 Feb 2024 03:08:53 GMT  
		Size: 47.0 MB (47012472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64d28cb5695f590c46c7d223348d7d58bfba0e23dec221f5343b0dca7a09bcb`  
		Last Modified: Fri, 16 Feb 2024 03:08:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77aabc96be0541477c14b4c395f0cedb75eb6388609833afb6cb0da3a3b182c7`  
		Last Modified: Fri, 16 Feb 2024 03:08:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a515b8f2ec4e0019840dbf53bb6403e487fe611bd65a8ad1a6cab8513ac76088`  
		Last Modified: Fri, 16 Feb 2024 05:20:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba613b2e2341d842b98b448ff124cb29d1f246adaceb17f2f465e8f1e7a48c4f`  
		Last Modified: Fri, 16 Feb 2024 05:20:26 GMT  
		Size: 12.3 MB (12338746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e45d5964bf39ac7f50b8d1e56c7c87c62659fa8a206213b92bfaab017469d4`  
		Last Modified: Fri, 16 Feb 2024 05:20:25 GMT  
		Size: 489.7 KB (489725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591fff9c30965b54f70b8d396a4ea285c46b690fe70de80046792df9f699db2c`  
		Last Modified: Fri, 16 Feb 2024 05:20:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:022601f27fe0ef921ce635c6971b7b9e0f2c1da4ef18249c7f85da1fc536c565
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102454870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a2a398b133c93785a188ac25efc1b6fe31f92444c3897761a5326b43fab9fb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 07:19:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 07:27:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 07:27:10 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 07:30:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 07:30:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 07:30:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 07:30:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 13:38:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2024 13:38:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 13:38:33 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2024 13:38:33 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2024 13:38:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 13:38:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 13:38:33 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 16 Feb 2024 13:38:33 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Feb 2024 13:38:33 GMT
ENV TOMCAT_VERSION=10.1.18
# Fri, 16 Feb 2024 13:38:34 GMT
ENV TOMCAT_SHA512=56d1478501bd63945aae08d9f7c1fd37e14761dd9606a3bf5996870256b542b561a354fb89c4693c5695d0f13fa217028115b311d50b4ecec03acc7785006638
# Fri, 16 Feb 2024 13:38:34 GMT
COPY dir:19cf6c4c04292dab74fa59e1de910cc43599cbcad9ff9b8c427f72586b510671 in /usr/local/tomcat 
# Fri, 16 Feb 2024 13:38:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 13:38:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2024 13:38:38 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 13:38:38 GMT
ENTRYPOINT []
# Fri, 16 Feb 2024 13:38:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06439c312d07b9a9a2b1abe400a875c694ea9d34abcd938043094f9fa832631d`  
		Last Modified: Fri, 16 Feb 2024 07:38:53 GMT  
		Size: 17.3 MB (17261530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75a98bc508a0ab498758127e894ef7be31f835c290ca2eb4bf51d33dcd69f3b`  
		Last Modified: Fri, 16 Feb 2024 07:39:16 GMT  
		Size: 43.8 MB (43765973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc62b1194733a4e6d63c34bbe6cb119a73c7ee7312f4f386a1257fbcacd6971`  
		Last Modified: Fri, 16 Feb 2024 07:39:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95477c395ccdd2f62b54717915da0157b15ffcd321dcfa0747ae0d633fa98db1`  
		Last Modified: Fri, 16 Feb 2024 07:39:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ef76cb7bac71df7b3cb7f311f8518f152108ffbb778e0bd486905727750d38`  
		Last Modified: Fri, 16 Feb 2024 14:12:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71915c2d4892cfdcaed868d85fb87738ca89f888cc0ed91a928597119a2acc8`  
		Last Modified: Fri, 16 Feb 2024 14:12:53 GMT  
		Size: 12.3 MB (12327539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2073881a394f67d794a490ae691b257a10de6c394bc843674eae72e3465a966b`  
		Last Modified: Fri, 16 Feb 2024 14:12:52 GMT  
		Size: 459.9 KB (459907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b3fa319f0f625e0f2dc86d71cf0a7648dc95c09c08e5ce09b5a9f69891327a`  
		Last Modified: Fri, 16 Feb 2024 14:12:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
