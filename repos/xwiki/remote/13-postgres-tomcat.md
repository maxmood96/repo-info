## `xwiki:13-postgres-tomcat`

```console
$ docker pull xwiki@sha256:b250edc19f4cc72d051ff836bc6a66dad2884231ad972b66018917572d37c35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:638d7630646963b18a849058a847b7caab4ded28712b60b0d6d1900f56b0c537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562304923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cad287c34ddcfc1a8b8fa8c65cb34197ee741da2b4c8d387d6e0ad78009ec9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:30:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:30:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 06:30:41 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 06:30:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:30:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 06:35:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 06:35:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:18:07 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:18:07 GMT
COPY dir:360b17da945f7a5c4dcdc8b0602904442d98c06d17157280c607532ec8b6edaa in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:18:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:18:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:18:13 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:18:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:23:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:26:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 03:09:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 03:09:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 03:10:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 03:10:28 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 03:10:28 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 03:10:29 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 03:10:29 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 03:10:29 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 03:10:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:10:29 GMT
CMD ["xwiki"]
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
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246089a07769500a0adb027d1dc0efbb1254ee07d75dcdc6f8a3ceb8bae3e95f`  
		Last Modified: Tue, 07 Jun 2022 06:48:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636fe8b4383f769da39b4c598b1e98b53b6d528e34e9d20fac5c17cfefcd866`  
		Last Modified: Fri, 10 Jun 2022 00:40:50 GMT  
		Size: 12.2 MB (12247499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a0fd2a02961d2a1725c94d0c0f5670c51d5f5f9bad820a96e45791a5d7a32`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 445.5 KB (445476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba28f927b0599e17785c8f69b8373e61c14da42247f7683f924f80ecae1439`  
		Last Modified: Fri, 10 Jun 2022 00:40:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657eec0a2bb289006e136ad46dbd1d85e8ff10712e1477c0fcacb617a19bb242`  
		Last Modified: Wed, 22 Jun 2022 04:31:12 GMT  
		Size: 168.3 MB (168293438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136be306a609540683e370b2425b4d3703542a79224441c6337af82ee1698ca2`  
		Last Modified: Fri, 24 Jun 2022 03:12:46 GMT  
		Size: 292.6 MB (292641286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3769fbd23a38bb2c2737d30cd4a790f8ad775a99a63e6591de2df21d750f52`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155517bc4fff02081a754dd1ac5674da90d74db9792a871f64983196cbd2b573`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9d584cf5548a2a612999b7b8fb340c4a38d8e9b31fd9ab73ca09cb173eb0f`  
		Last Modified: Fri, 24 Jun 2022 03:12:28 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2330650c98390edb3e1e7bd4d667c7b4e344da794f180c208aa1c92872db10cc`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9458af98469686b7341e974f7343a72938ca0fa6984c887bb8d0a160375881ee`  
		Last Modified: Fri, 24 Jun 2022 03:12:29 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bb8443f4c39a1e5e1eaa389c87f32b928bccad2f727705a2e02afcc1b98ac2bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.8 MB (554784337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d205394842fb0b6709b682ff9d39e01d0ade2e25f08c11c4c8c766f9ccd182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 10:50:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Jun 2022 10:50:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 10:50:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 07 Jun 2022 10:50:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Jun 2022 10:50:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:50:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Jun 2022 10:59:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 07 Jun 2022 10:59:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:28:14 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:28:16 GMT
COPY dir:1fb0204bb532a7d63a0dd2d2677d66a70be0285454d27afba6780853636ba1ef in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:28:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:28:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:28:25 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:28:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 22 Jun 2022 04:09:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 22 Jun 2022 04:09:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 22 Jun 2022 04:09:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 22 Jun 2022 04:09:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 22 Jun 2022 04:11:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 08:11:28 GMT
ENV XWIKI_VERSION=13.10.7
# Fri, 24 Jun 2022 08:11:29 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Fri, 24 Jun 2022 08:11:30 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Fri, 24 Jun 2022 08:12:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 24 Jun 2022 08:12:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 24 Jun 2022 08:12:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 24 Jun 2022 08:12:15 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 24 Jun 2022 08:12:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 24 Jun 2022 08:12:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 24 Jun 2022 08:12:17 GMT
VOLUME [/usr/local/xwiki]
# Fri, 24 Jun 2022 08:12:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 08:12:19 GMT
CMD ["xwiki"]
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
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa4900f44b9e3e20168d54fda3a0b78e62d572de1796db20345b70b1d8b3ca`  
		Last Modified: Tue, 07 Jun 2022 11:23:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796806c88914990f15047665e74a4ea1fb933bdf7b8ebf39b1f2a82b723e044`  
		Last Modified: Fri, 10 Jun 2022 02:03:21 GMT  
		Size: 12.3 MB (12264791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca37469fc5a6ebbc5f1a764aabd4ba48b92a85d1396b644e1139994fad2fa34e`  
		Last Modified: Fri, 10 Jun 2022 02:03:20 GMT  
		Size: 208.8 KB (208841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf4753a12af2d02fd26a953119f6843f7e381cfec0d679d92b04b4e4f5a3d6a`  
		Last Modified: Wed, 22 Jun 2022 04:18:08 GMT  
		Size: 164.2 MB (164164156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdad91995b0da375c92d6651576276e78123cfbb080e5444a094fc5033c930c`  
		Last Modified: Fri, 24 Jun 2022 08:15:36 GMT  
		Size: 292.6 MB (292641359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ecfd793c7e54308d1c7a22f36e2e098e8fdae31cecb75339bfa7f0a8b7af6`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27ddaa528e0298945c5eca4aa5235bd761f13f40e2b35de068a7977434e571d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edb1eb483f19a886fd0fcf80dc5c21e5ef36163eb1e8df94a3b80f508fbeff8`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d9ff4c9416279f5b0a9e42bf517e29f15992d0a7a0c5d3361f7fbc8472c12d`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be06063b865aaeadaa012c84711685856110099c19fa07ac1af19e12fa08cce`  
		Last Modified: Fri, 24 Jun 2022 08:15:14 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
