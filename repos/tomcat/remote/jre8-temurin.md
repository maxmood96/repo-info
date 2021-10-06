## `tomcat:jre8-temurin`

```console
$ docker pull tomcat@sha256:190b596a0a7f51c34af0156d8499f7e8410442ca29594ff7e1a0f25c70eda83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:jre8-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:29ffee145ce438596ffb88ae2f055ee2d39518a103c05690b949c8278abff894
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99346043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16808c432654eedf27cd8d646126e9264603174855c56797397b22999e107fd6`
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
# Fri, 01 Oct 2021 09:03:37 GMT
ENV TOMCAT_VERSION=10.0.11
# Fri, 01 Oct 2021 09:03:37 GMT
ENV TOMCAT_SHA512=16e1879490bb0e5843059e3a475558f1990b03f897a7d5cce5788d6983598ec30cbf3749e30c18fb799f5068cab8407d04e9e6e9705700b152f90a3dc8bc0cb5
# Fri, 01 Oct 2021 09:03:38 GMT
COPY dir:4e9c533e3b83595c96125e01195223002d4eded30659ed702cae676a55cdb1ff in /usr/local/tomcat 
# Fri, 01 Oct 2021 09:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 09:03:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 01 Oct 2021 09:03:44 GMT
EXPOSE 8080
# Fri, 01 Oct 2021 09:03:44 GMT
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
	-	`sha256:1e1272924bb915d4827c64432253ce59fba54847026e072ee6ae9903dce8d4ba`  
		Last Modified: Fri, 01 Oct 2021 09:30:56 GMT  
		Size: 12.6 MB (12585902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36762be965edd67f3e5de2f09388b4c6486a57bafbdb24d51cfce8d8e4c090a`  
		Last Modified: Fri, 01 Oct 2021 09:30:56 GMT  
		Size: 445.7 KB (445672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee82a631bdc981c0e94cfed8c9535703ba041229ab464536bcba395b2848cc4c`  
		Last Modified: Fri, 01 Oct 2021 09:30:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9bd20e4e81e9714d3ba915c8c50493a243197d12f9afe9bd37b5ad2529da63b8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96860146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505d2ca6774048e9071a3038262a71d1f4139d97b883478de00a5438db57023`
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
# Fri, 01 Oct 2021 06:37:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 06:37:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 06:37:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 06:37:41 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 06:37:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 06:37:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 06:37:42 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 01 Oct 2021 06:37:42 GMT
ENV TOMCAT_MAJOR=10
# Fri, 01 Oct 2021 06:37:42 GMT
ENV TOMCAT_VERSION=10.0.11
# Fri, 01 Oct 2021 06:37:42 GMT
ENV TOMCAT_SHA512=16e1879490bb0e5843059e3a475558f1990b03f897a7d5cce5788d6983598ec30cbf3749e30c18fb799f5068cab8407d04e9e6e9705700b152f90a3dc8bc0cb5
# Fri, 01 Oct 2021 06:37:43 GMT
COPY dir:cbe500fe5476cb4073d78eac7ee4d3e72231211955da692533ac68e489c730ec in /usr/local/tomcat 
# Fri, 01 Oct 2021 06:37:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:37:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 01 Oct 2021 06:37:50 GMT
EXPOSE 8080
# Fri, 01 Oct 2021 06:37:50 GMT
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
	-	`sha256:cd578346043324cbe935bd45e310df0e0306ef0764bcbe57caefe416fd359564`  
		Last Modified: Fri, 01 Oct 2021 07:23:01 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ed0d73c97c8a3315d76e9cd80c9235c3977e546118e31c6c1342d5b783b2ff`  
		Last Modified: Fri, 01 Oct 2021 07:23:01 GMT  
		Size: 12.6 MB (12602143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1cbb421bf7cab671e8d917c1d2940b030553808dfdb07265d2d253475c55ea`  
		Last Modified: Fri, 01 Oct 2021 07:23:00 GMT  
		Size: 446.2 KB (446217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59cec2f66b34605ae50ec7765ada98c18e58ebc7073ee9d3a1bb57bf0b3e40`  
		Last Modified: Fri, 01 Oct 2021 07:23:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:597f3da7b07f9a2b7c67d6ec7000b14cd4fd90d36765082dd315b666f5ad862b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104732547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37f3b1fb66a28f21532c079cee44a3a23bb78b59a60d1874ee3544e36cd4651`
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
# Wed, 06 Oct 2021 15:29:14 GMT
ENV TOMCAT_VERSION=10.0.11
# Wed, 06 Oct 2021 15:29:16 GMT
ENV TOMCAT_SHA512=16e1879490bb0e5843059e3a475558f1990b03f897a7d5cce5788d6983598ec30cbf3749e30c18fb799f5068cab8407d04e9e6e9705700b152f90a3dc8bc0cb5
# Wed, 06 Oct 2021 15:29:20 GMT
COPY dir:cb5dbf38d0d1408078c1c74fe6e5ae23192d6301be030ae789e27ecd0cdae103 in /usr/local/tomcat 
# Wed, 06 Oct 2021 15:29:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 15:30:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Oct 2021 15:30:04 GMT
EXPOSE 8080
# Wed, 06 Oct 2021 15:30:06 GMT
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
	-	`sha256:0a2bdbcbbe2295a5b284414b0b5d4d38e54f7b8484020acdadf8891ace0a88a5`  
		Last Modified: Wed, 06 Oct 2021 16:52:31 GMT  
		Size: 12.6 MB (12625425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652bd54c8a83a3b4c1fc1a326f5efd1a8d9f85b6070ea54eebec933384be4bac`  
		Last Modified: Wed, 06 Oct 2021 16:52:30 GMT  
		Size: 471.5 KB (471472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ddbba277fbae407749e1bd14757ffb8820233f8c2fa7a8fdb8ed71c83d2f04`  
		Last Modified: Wed, 06 Oct 2021 16:52:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
