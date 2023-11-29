## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:ed0c7cdc4708994f90bcaf3285f7120bf13f7fc901a15e4b2ae13f6cd6cbce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:22af20f0b0574c48cf0c73e2f571aea1e5f6bdcbce01bc290075d6383cd7e7a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597703245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50e3cb53fcbf4de6f4eb68cd6ef07ea0e8c465fdb38cc199ab512a4313e62da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:51:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 05:51:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 05:51:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:27:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:27:44 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:29:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:29:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:29:19 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:29:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 03:37:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 03:37:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:37:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 03:37:14 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 03:37:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:37:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:39:32 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 31 Oct 2023 03:39:32 GMT
ENV TOMCAT_MAJOR=9
# Fri, 17 Nov 2023 01:51:01 GMT
ENV TOMCAT_VERSION=9.0.83
# Fri, 17 Nov 2023 01:51:01 GMT
ENV TOMCAT_SHA512=3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04
# Fri, 17 Nov 2023 01:51:01 GMT
COPY dir:b6e1a8757fb2a3ef38131285ce5c3e899c192beceb72b241a4c35cd6322a0630 in /usr/local/tomcat 
# Fri, 17 Nov 2023 01:51:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Nov 2023 01:51:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 17 Nov 2023 01:51:28 GMT
EXPOSE 8080
# Fri, 17 Nov 2023 01:51:28 GMT
ENTRYPOINT []
# Fri, 17 Nov 2023 01:51:28 GMT
CMD ["catalina.sh" "run"]
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 17 Nov 2023 03:44:25 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 17 Nov 2023 03:46:15 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 28 Nov 2023 23:44:03 GMT
ENV XWIKI_VERSION=15.10
# Tue, 28 Nov 2023 23:44:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10
# Tue, 28 Nov 2023 23:44:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=6f8b932c2a2a82acad5695675e1846d4421207c1820e415006750385e0981ece
# Tue, 28 Nov 2023 23:44:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 28 Nov 2023 23:44:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 28 Nov 2023 23:44:44 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 28 Nov 2023 23:44:44 GMT
COPY file:98c6046d1b5e77229fc6e67481d24fd005196575f4e4fd725e7d3db07bd9601b in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 28 Nov 2023 23:44:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 28 Nov 2023 23:44:45 GMT
COPY file:9cbfa36f41bbf2137b768a707fab0bad1de6eef9a2d12e7c0fc0565ffdfeb1d4 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 28 Nov 2023 23:44:45 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Nov 2023 23:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Nov 2023 23:44:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4452d37e1e46888f8dbbf8283d09e03f1bec00021532334441fe00c95aa8b15`  
		Last Modified: Mon, 30 Oct 2023 23:36:06 GMT  
		Size: 17.5 MB (17454768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae6cc00f059e812c753a4a45b4a388d14bb714a104ec8b33c31436807f31055`  
		Last Modified: Mon, 30 Oct 2023 23:37:50 GMT  
		Size: 47.1 MB (47149391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaec5da5e638ca5d7247c8697d0721bdac4826945748d0239718f23f657abc5`  
		Last Modified: Mon, 30 Oct 2023 23:37:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7dcc43773c1bcab928db7ca63abd5a20c525148ae1b63c03bfdcdef7e03153`  
		Last Modified: Mon, 30 Oct 2023 23:37:44 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729bb2516f9ee1f23d3c6b1a60b651eb413c43b62cdc554de84df2590085216`  
		Last Modified: Tue, 31 Oct 2023 03:53:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abd3b406207b67cea45616a0f3398220a4b45a469f1f14f5c5bdef4b2f35e20`  
		Last Modified: Fri, 17 Nov 2023 02:09:18 GMT  
		Size: 12.4 MB (12391471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bea609136cd16081c1a3aaca29e377bb4b844074278006408baae7f88efd57`  
		Last Modified: Fri, 17 Nov 2023 02:09:17 GMT  
		Size: 3.0 MB (2970855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c81efba92eebab5d197fa544a2e5612bf514bd18f152836a57a5802f198041`  
		Last Modified: Fri, 17 Nov 2023 02:09:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbe24937e6c7cdb3133ecd0194e487a26e327aad8a189add9c573a48df65312`  
		Last Modified: Fri, 17 Nov 2023 03:52:40 GMT  
		Size: 179.5 MB (179517396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e28025cb1f0663c28adc905ab2a84a6ad77ad0c4fce7db3ff02eeb6834f17`  
		Last Modified: Tue, 28 Nov 2023 23:46:45 GMT  
		Size: 306.8 MB (306829686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf848987a7a9c7fd41f28584a74d21d9b7624202daedaa37f7996547f6e428`  
		Last Modified: Tue, 28 Nov 2023 23:46:29 GMT  
		Size: 936.8 KB (936845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c6403379cb5f221c54db1d41b2a8074653e949e62b19fc0499e51a29719483`  
		Last Modified: Tue, 28 Nov 2023 23:46:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e811a73292fd45c8059261a1ea079ab399a7fa89f8969e7ff3b8b2296bad962`  
		Last Modified: Tue, 28 Nov 2023 23:46:28 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d29a1dca374a875d055c41f072d67c4a265e25607ade3b3caf7cb301847985`  
		Last Modified: Tue, 28 Nov 2023 23:46:28 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befb42ba9de2622111026bd9174840f9f02c7190fe8297f9d3c8afdc397cd307`  
		Last Modified: Tue, 28 Nov 2023 23:46:28 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c65d498f650fee5ebebbee2929f9ade1f518c4cb6c2bdd55033818ef79a4bafc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.4 MB (591440498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4554d39d4f7b1e29514841632aa08f6e3a47110e90aa76443a2bc90a6c06bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:46:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 02:46:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 02:46:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:44:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:44:05 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:45:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:45:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:45:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:45:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 02:56:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 02:56:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 02:56:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 02:56:14 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 02:56:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 02:56:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 02:58:17 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 31 Oct 2023 02:58:17 GMT
ENV TOMCAT_MAJOR=9
# Fri, 17 Nov 2023 02:16:24 GMT
ENV TOMCAT_VERSION=9.0.83
# Fri, 17 Nov 2023 02:16:24 GMT
ENV TOMCAT_SHA512=3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04
# Fri, 17 Nov 2023 02:16:24 GMT
COPY dir:3d6975406d5c02f80e9cf7d7f1d0b3d166d08756088d7d8662050a94f9373d14 in /usr/local/tomcat 
# Fri, 17 Nov 2023 02:16:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Nov 2023 02:16:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 17 Nov 2023 02:16:29 GMT
EXPOSE 8080
# Fri, 17 Nov 2023 02:16:29 GMT
ENTRYPOINT []
# Fri, 17 Nov 2023 02:16:29 GMT
CMD ["catalina.sh" "run"]
# Fri, 17 Nov 2023 03:56:37 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 17 Nov 2023 03:56:37 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 17 Nov 2023 03:56:38 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 17 Nov 2023 03:56:38 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 17 Nov 2023 03:56:38 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 17 Nov 2023 03:56:38 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 17 Nov 2023 03:58:23 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 29 Nov 2023 00:12:56 GMT
ENV XWIKI_VERSION=15.10
# Wed, 29 Nov 2023 00:12:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10
# Wed, 29 Nov 2023 00:12:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=6f8b932c2a2a82acad5695675e1846d4421207c1820e415006750385e0981ece
# Wed, 29 Nov 2023 00:13:35 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 29 Nov 2023 00:13:38 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 29 Nov 2023 00:13:38 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 29 Nov 2023 00:13:38 GMT
COPY file:98c6046d1b5e77229fc6e67481d24fd005196575f4e4fd725e7d3db07bd9601b in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 29 Nov 2023 00:13:39 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 29 Nov 2023 00:13:39 GMT
COPY file:9cbfa36f41bbf2137b768a707fab0bad1de6eef9a2d12e7c0fc0565ffdfeb1d4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Nov 2023 00:13:39 GMT
VOLUME [/usr/local/xwiki]
# Wed, 29 Nov 2023 00:13:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Nov 2023 00:13:39 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f494a0917249ff640404cd9965fcd6a5ed5b7725fc21ff44518307f60c8e0a`  
		Last Modified: Mon, 30 Oct 2023 23:50:44 GMT  
		Size: 18.9 MB (18858788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf992ac9f7594e95247c785c373702afa5ebbf20db8b34fad80efa1ff3e0736`  
		Last Modified: Mon, 30 Oct 2023 23:52:03 GMT  
		Size: 46.6 MB (46623965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652d455f0a073aa4bc59de2e451f4c5a2ad6d6d9cb13538ef955d11e722e6c45`  
		Last Modified: Mon, 30 Oct 2023 23:51:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fce918b0b707b682534041104ace8701cb441f12b5ce2fb5e983bfe29694385`  
		Last Modified: Mon, 30 Oct 2023 23:51:58 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa512d8c7aada52b2d7bd906e3bae22e22f3025a7ed09a1f0adf9e2b9c7aaf6`  
		Last Modified: Tue, 31 Oct 2023 03:09:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0be96d9e26d4bdaa466f154ab63b4a65317928dc740d9487407598c11e3881`  
		Last Modified: Fri, 17 Nov 2023 02:31:17 GMT  
		Size: 12.4 MB (12398006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc049231212f55a65b295577715e3690a784553575cd5e5b272daa633ad31048`  
		Last Modified: Fri, 17 Nov 2023 02:31:16 GMT  
		Size: 2.8 MB (2812548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb37d870ea6b50484f6c05999bbe6fc08a9a027f71da0811fe80d6032245fa8c`  
		Last Modified: Fri, 17 Nov 2023 02:31:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccfc26177470c9fc569d65c23667a3bda7845b3ed9b76d1214a4c3e7db9d4aa`  
		Last Modified: Fri, 17 Nov 2023 04:04:33 GMT  
		Size: 174.6 MB (174575053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d3e5dd50b4c8b155f59b0c03eb078c4e023810e2d69000ea37b75abae55c5c`  
		Last Modified: Wed, 29 Nov 2023 00:15:44 GMT  
		Size: 306.8 MB (306829636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d1668521dce1d37cd515355dd35b2d6451a9cb3ad2b9f6452d56a53bd85c86`  
		Last Modified: Wed, 29 Nov 2023 00:15:30 GMT  
		Size: 936.8 KB (936846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755a5537322ff2c8d8f19d0e5d88ce4b6947c0058a8c5c2d64b0f15f4d6253e`  
		Last Modified: Wed, 29 Nov 2023 00:15:30 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d096be8c3f21d6bcc8c644ede2821e5d3ce9f366ae93720d9c5138629f3ea0ae`  
		Last Modified: Wed, 29 Nov 2023 00:15:30 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a034865df3e1d18740fa753752aab065f69e02a1afbc5307323ba4dbdd1f4c0`  
		Last Modified: Wed, 29 Nov 2023 00:15:30 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64b9bf4cfa065f865e065f719e4b1beef13a9a405e649789d9dab063cfa21b8`  
		Last Modified: Wed, 29 Nov 2023 00:15:29 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
