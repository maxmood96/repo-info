## `tomcat:jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:23e3b6aec00e8956519599ac741d07b08dd506589c87d612dc6129ab7a0496f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:07a61a59e3c491481ba1862195c1cf0c9078a6fbe7c3f3efd40d0cc4fc73228a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99318683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd63863cd2c2e2e89621cccb65cbaf9f00c07aa1307bcd4008f240c25803bec`
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
# Fri, 01 Oct 2021 09:03:36 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 01 Oct 2021 09:03:37 GMT
ENV TOMCAT_MAJOR=10
# Wed, 06 Oct 2021 19:19:53 GMT
ENV TOMCAT_VERSION=10.0.12
# Wed, 06 Oct 2021 19:19:53 GMT
ENV TOMCAT_SHA512=e084fc0cc243c0a9ac7de85ffd4b96d00b40b5493ed7ef276d91373fe8036bc953406cd3c48db6b5ae116f2af162fd1bfb13ecdddf5d64523fdd69a9463de8a3
# Thu, 07 Oct 2021 20:17:50 GMT
COPY dir:d192f97796da6c645bab6d9c0dabe08573263e9b61e040fdc00b7cef654eadc5 in /usr/local/tomcat 
# Thu, 07 Oct 2021 20:17:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 20:17:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:17:56 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:17:57 GMT
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
	-	`sha256:514c61a8dd27f41d137b9565e6facce8370e046ee41b935a85469f0b43f7ed5f`  
		Last Modified: Thu, 07 Oct 2021 20:56:26 GMT  
		Size: 12.6 MB (12558544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68eb94764c46540fa0d5b9efea384402c2cb7e55451a3b994f2206bfa3c9c304`  
		Last Modified: Thu, 07 Oct 2021 20:56:25 GMT  
		Size: 445.7 KB (445669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d622438583ee446ea618d9c3ff7cbba7fda233bc6180a170c5c0bcef73a90a`  
		Last Modified: Thu, 07 Oct 2021 20:56:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:1d92b4929a0574e7106169a70d9108cb40c25d2fd1b4a27f8b6af631432a3d32
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96595196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cbdc4afc367f06daf5957c6226adaef782a802a5c4f8ffe5aea5190cbaffa8`
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
# Wed, 13 Oct 2021 09:03:06 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 13 Oct 2021 09:03:07 GMT
ENV TOMCAT_MAJOR=10
# Wed, 13 Oct 2021 09:03:08 GMT
ENV TOMCAT_VERSION=10.0.12
# Wed, 13 Oct 2021 09:03:09 GMT
ENV TOMCAT_SHA512=e084fc0cc243c0a9ac7de85ffd4b96d00b40b5493ed7ef276d91373fe8036bc953406cd3c48db6b5ae116f2af162fd1bfb13ecdddf5d64523fdd69a9463de8a3
# Wed, 13 Oct 2021 09:03:11 GMT
COPY dir:f2a045c4a1e3ee42c78e804821f76bcdfa9fc7ad55cc522829015a4d086d541e in /usr/local/tomcat 
# Wed, 13 Oct 2021 09:03:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 09:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:03:19 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:03:20 GMT
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
	-	`sha256:504b3a18fdfdf1235de410758b95f0b85c29130e54acaab924765557bfb7e6a0`  
		Last Modified: Wed, 13 Oct 2021 10:37:56 GMT  
		Size: 12.6 MB (12575019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58b72847dfc500ef170b3f2af7bf5d5f1a1be5bde904ae3ff39aba3bbfd8bb8`  
		Last Modified: Wed, 13 Oct 2021 10:37:54 GMT  
		Size: 208.6 KB (208556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:7a1215ff5e6b91bd538cdfdf462e62588fb4c65ddd68ebc085e4cf2c36a3ccb2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104705580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6bb2be39de75a010ad8a693e03de84eb9212f0c3b3e4fa9a62b702f60bb1911`
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
# Wed, 06 Oct 2021 15:29:04 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 06 Oct 2021 15:29:10 GMT
ENV TOMCAT_MAJOR=10
# Thu, 07 Oct 2021 08:52:36 GMT
ENV TOMCAT_VERSION=10.0.12
# Thu, 07 Oct 2021 08:52:42 GMT
ENV TOMCAT_SHA512=e084fc0cc243c0a9ac7de85ffd4b96d00b40b5493ed7ef276d91373fe8036bc953406cd3c48db6b5ae116f2af162fd1bfb13ecdddf5d64523fdd69a9463de8a3
# Thu, 07 Oct 2021 21:07:57 GMT
COPY dir:d52a6bcaca2b32e99cd1f20d98013aa5218dfa99403747fcaf0475b5abe12a1f in /usr/local/tomcat 
# Thu, 07 Oct 2021 21:08:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 21:08:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 21:08:43 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 21:08:44 GMT
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
	-	`sha256:7b5369badd6a2a6715b80016db95abbedf61eb5886a1895d9f392a83d4ab617d`  
		Last Modified: Thu, 07 Oct 2021 21:43:42 GMT  
		Size: 12.6 MB (12598458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53661805202c7410c2a71000d635eef815b2ac192b4a8e2fa85e6ef360a5631d`  
		Last Modified: Thu, 07 Oct 2021 21:43:40 GMT  
		Size: 471.5 KB (471470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6447e42de87995c7836fac8f0a9085e443a43a85cd9beed3b769a019f5073799`  
		Last Modified: Thu, 07 Oct 2021 21:43:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
