## `tomcat:9-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:9f182bec6a262c3bdf143dbfaff0389b5473c9321fa649dcd05691d73b2e6d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:9-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:8151aea5b40bfc6f0609aea152f402e3491cacd5af28b9411b338505dc5853e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99005131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffe5f880211dbf9c43f5540bc51cdd7c00d1228c404e2e76475f2070f386dae`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:46:35 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Fri, 01 Oct 2021 04:46:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9951a36430c14548f78569135956e929db2554bfc706bb3fe0bf9a14acd28055';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0f242dc94b2c46f231e811427e30031cd1c7e5667979f8b403296008863d150e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:46:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:46:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 01 Oct 2021 09:03:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 09:03:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 09:03:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 09:03:36 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 09:03:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:03:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:09:17 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 01 Oct 2021 09:09:17 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Oct 2021 19:36:42 GMT
ENV TOMCAT_VERSION=9.0.54
# Wed, 06 Oct 2021 19:36:43 GMT
ENV TOMCAT_SHA512=83430f24d42186ce2ff51eeef2f7a5517048f37d9050c45cac1e3dba8926d61a1f7f5aba122a34a11ac1dbdd3c1f6d98671841047df139394d43751263de57c3
# Thu, 07 Oct 2021 20:20:16 GMT
COPY dir:77b731b7af8cb791ca4abfe37113f1f67cac433b9f4586e90c289be8bc43c038 in /usr/local/tomcat 
# Thu, 07 Oct 2021 20:20:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 20:20:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:20:22 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:20:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f24a6f1e7d19d72576ecfaf27c0e8b754641203d440283bc86e230740c74da`  
		Last Modified: Fri, 01 Oct 2021 04:50:00 GMT  
		Size: 41.7 MB (41711939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d61bf3d04f329f4836ad7b128e574fb6eb6b25d5f13433effdc50da1e26428`  
		Last Modified: Fri, 01 Oct 2021 04:49:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433bad2f747d47a2f2393f975ac250fe404586329a38d3e9949af2549f66a080`  
		Last Modified: Fri, 01 Oct 2021 09:30:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b337587e47245bc8599655c8e73d4e2b3e049e2a4c4a9222ada4e90f9f873e`  
		Last Modified: Thu, 07 Oct 2021 20:58:27 GMT  
		Size: 12.2 MB (12244999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff9b322e5298d373043c20690a9907d6bbf9380a4ef8498da45953783c41f80`  
		Last Modified: Thu, 07 Oct 2021 20:58:26 GMT  
		Size: 445.7 KB (445662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96ce1bac773d8ba8fae18d272cd69a84e7ee836b866efcaaa28fa17edf9b40b`  
		Last Modified: Thu, 07 Oct 2021 20:58:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:58f6d92db49d1797390e7b1fa08f0e7834d7511178f2a01f8a76d3c3dd0b0576
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96279890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5446be773fe1108dab2aa87333615fdaddc55f134f05aeebcc65ae668733380`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Fri, 01 Oct 2021 03:30:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9951a36430c14548f78569135956e929db2554bfc706bb3fe0bf9a14acd28055';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0f242dc94b2c46f231e811427e30031cd1c7e5667979f8b403296008863d150e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:03 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 13 Oct 2021 09:03:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 09:03:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 09:03:02 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 09:03:03 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 09:03:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:03:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:25:02 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 13 Oct 2021 09:25:03 GMT
ENV TOMCAT_MAJOR=9
# Wed, 13 Oct 2021 09:25:04 GMT
ENV TOMCAT_VERSION=9.0.54
# Wed, 13 Oct 2021 09:25:05 GMT
ENV TOMCAT_SHA512=83430f24d42186ce2ff51eeef2f7a5517048f37d9050c45cac1e3dba8926d61a1f7f5aba122a34a11ac1dbdd3c1f6d98671841047df139394d43751263de57c3
# Wed, 13 Oct 2021 09:25:07 GMT
COPY dir:d2a81565c97f638b90566b9e6af7b4d5b3b748afa16e713225938435ad9691df in /usr/local/tomcat 
# Wed, 13 Oct 2021 09:25:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 09:25:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:25:15 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:25:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb858a8ef47e865174d4c3dd7ab3ae7c523ba848a3d77bb284a6aca0c7c215`  
		Last Modified: Fri, 01 Oct 2021 03:33:57 GMT  
		Size: 40.7 MB (40743695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdd8b68a69037e3bf7636bf15e043a834909638440dab9e3773f5f3449a12d3`  
		Last Modified: Fri, 01 Oct 2021 03:33:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e289252978930a9d01b9adb20a989d5be3265e3c75cd2bf88b024c8483159a74`  
		Last Modified: Wed, 13 Oct 2021 10:37:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3f144e3e030a71c512ae3e55b68b7dff9e80fbdd2df49d6e2611ab947f6165`  
		Last Modified: Wed, 13 Oct 2021 10:50:45 GMT  
		Size: 12.3 MB (12259716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556020efd59a90a55c1acc50f486f57abb73894fc29f248c64ab5b1849eb8920`  
		Last Modified: Wed, 13 Oct 2021 10:50:44 GMT  
		Size: 208.6 KB (208553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:3c77388680ed7c1e813f844b9da038a643bbff6a1bab8b9a1cc59c733ba7c73a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104389242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6fd5a520cb2809f307327bf05bb2d78a84c631652b55218bb2421e570bcb2c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Oct 2021 12:59:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 13:00:01 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Tue, 05 Oct 2021 13:01:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9951a36430c14548f78569135956e929db2554bfc706bb3fe0bf9a14acd28055';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0f242dc94b2c46f231e811427e30031cd1c7e5667979f8b403296008863d150e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Oct 2021 13:01:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Oct 2021 13:01:22 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Oct 2021 15:28:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Oct 2021 15:28:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 15:28:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Oct 2021 15:28:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Oct 2021 15:28:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Oct 2021 15:29:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Oct 2021 16:07:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 06 Oct 2021 16:07:59 GMT
ENV TOMCAT_MAJOR=9
# Thu, 07 Oct 2021 09:12:28 GMT
ENV TOMCAT_VERSION=9.0.54
# Thu, 07 Oct 2021 09:12:30 GMT
ENV TOMCAT_SHA512=83430f24d42186ce2ff51eeef2f7a5517048f37d9050c45cac1e3dba8926d61a1f7f5aba122a34a11ac1dbdd3c1f6d98671841047df139394d43751263de57c3
# Thu, 07 Oct 2021 21:16:11 GMT
COPY dir:b70a88bf91b4fdfc37bf11a98da880cea7c6784cd17b1cbafb13afd87007a029 in /usr/local/tomcat 
# Thu, 07 Oct 2021 21:16:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 21:16:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 21:16:39 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 21:16:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d0f93d81b8713c3abad0c3080f3bf43c08c0392ff1e24e640afa4e8a5ab59a`  
		Last Modified: Tue, 05 Oct 2021 13:08:20 GMT  
		Size: 17.2 MB (17207545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8c1227d12fe95a38c195fcbb729b47e59a0f1faaf0934233181d10abb99217`  
		Last Modified: Tue, 05 Oct 2021 13:08:56 GMT  
		Size: 41.1 MB (41136935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530593b3c17c8006b2b3d2facc4817e84bcd1cae4aadd4ba0387a40b12e1c18e`  
		Last Modified: Tue, 05 Oct 2021 13:08:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98eff6be22bbb582cc1a79563bf8a1f6c537344bf578db1aa4416ba8614302e`  
		Last Modified: Wed, 06 Oct 2021 16:52:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1647da4d64f368825756a82be4557b444e4dc84f761f2fecf70e37c418e28046`  
		Last Modified: Thu, 07 Oct 2021 21:44:57 GMT  
		Size: 12.3 MB (12282097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6937b52e01566e7aa78e57293c09a532723fa4ce9227426cd8866ad9dec75545`  
		Last Modified: Thu, 07 Oct 2021 21:44:55 GMT  
		Size: 471.5 KB (471493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea153d23d534e5d204ea7ecc9a6629c4d3ee77163fe90f8312e510630838ffe6`  
		Last Modified: Thu, 07 Oct 2021 21:44:55 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
