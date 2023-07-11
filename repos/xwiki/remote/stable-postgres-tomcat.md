## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:143482a096b13073c1d9d59fde125210cd6009c4fb253a6d30cf5eaf8481fc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4741e9d9b24c00013903dbabf718e61ef5c4b23fd41a283067988225a4ea60ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586784502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1f265f59dcb2e5a6888c86ef11b46a92e4d498dcf98b2ab1f05735021fa2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:35:02 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 20:35:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:35:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 08:22:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 08:22:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 08:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 08:22:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 08:22:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:22:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 08:25:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 08:25:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 00:16:14 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 00:16:15 GMT
COPY dir:8ddeace4a16f09a0d97488e225c7b2e4a48c9a93484d24b46a09759f52800501 in /usr/local/tomcat 
# Tue, 11 Jul 2023 00:16:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:16:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 00:16:20 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 00:16:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 04:38:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 04:38:07 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 04:41:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 04:41:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 04:42:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 04:42:05 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 04:42:05 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 04:42:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 04:42:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 04:42:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 04:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:42:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bb55fbcae928d7e6c08d6618580d2b27ce6e46083f861bbed1e01db41c20b`  
		Last Modified: Tue, 04 Jul 2023 20:41:01 GMT  
		Size: 46.7 MB (46666353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c6e3f57ee032a3cc5f0fd28b52687129e7a1e6485aea12aff08cb6620071e`  
		Last Modified: Tue, 04 Jul 2023 20:40:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b01f5ab5b71b356d93dff08f5037af8e8a03b4657f1fd303052261161ebd8`  
		Last Modified: Wed, 05 Jul 2023 08:37:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6051a2b9ffe906ea99b555033966c877468da73cd19fd793c86099d0af531`  
		Last Modified: Tue, 11 Jul 2023 00:38:45 GMT  
		Size: 12.3 MB (12274167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aaed1f6a3460fc256e262b462c1180ccef1b0665ffd50f900d1ef9c19f1d24`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 454.7 KB (454674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b809bf54ada009dfd91afa6ad239f7a791807f2928941b7f969493ec38246be`  
		Last Modified: Tue, 11 Jul 2023 00:38:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd305e7867896df13faced03525a0f25bf1ac1b2a2c93e60382cdfd41c08e16`  
		Last Modified: Tue, 11 Jul 2023 04:45:43 GMT  
		Size: 179.3 MB (179276407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bfb758076cf011f5df9081f31dfbcf656cd98cd11b65f53f3684ec1e485c8f`  
		Last Modified: Tue, 11 Jul 2023 04:45:37 GMT  
		Size: 304.2 MB (304236708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f8ccc8af30dd82bb4657bfdb7193ed23e8dc8823df1eaea8b1c8e4ab85d60`  
		Last Modified: Tue, 11 Jul 2023 04:45:20 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822e7d00d75f2a5b9a34edd0741b7e19410deb191f96800278c2921b043c81cb`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3137d80fef0218e2aaa65df38833a3e9d79b0d6e0b8d441376edbc36190ab`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02045e3c19030183c43f79b2c5e3a2f244dda96d11e96014e91d90e85f6e3a9`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91afad54a0c6d44f603953379c22801e4dbc9f2c282eaa00e94946d1d77dc3a4`  
		Last Modified: Tue, 11 Jul 2023 04:45:19 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:30799eeac6bc3f0efeefaf95f4161eeea6298cf60983391d2b7789735d58fa07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578094027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc026cfcc219f16306961c1815044f7a63d5f49577815243d20c27d2d823d48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Tue, 04 Jul 2023 15:34:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 15:34:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Jul 2023 02:55:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jul 2023 02:55:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 02:55:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jul 2023 02:55:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jul 2023 02:56:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 02:56:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jul 2023 03:00:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jul 2023 03:00:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Jul 2023 01:18:24 GMT
ENV TOMCAT_VERSION=9.0.78
# Tue, 11 Jul 2023 01:18:25 GMT
ENV TOMCAT_SHA512=c9f2e60489d07f25b53f715918f4b082c5bb69dbc497e0a9d3d5e3a0d351ff2e0ec8dfc5657de840ee5b3dea6174b27630033b38e36fa4c06b08664e70dec8df
# Tue, 11 Jul 2023 01:18:25 GMT
COPY dir:1743191a9534b9e7d795d3bf9ad18535d99e75967877447e17d7b63574d878d5 in /usr/local/tomcat 
# Tue, 11 Jul 2023 01:18:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Jul 2023 01:18:29 GMT
EXPOSE 8080
# Tue, 11 Jul 2023 01:18:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Jul 2023 05:20:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Jul 2023 05:22:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_VERSION=15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.5
# Tue, 11 Jul 2023 05:22:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=e552586d371da33b012cfbd974b3ba80d1b147a5c892ad6cf989960212cdaa02
# Tue, 11 Jul 2023 05:23:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Jul 2023 05:23:21 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Jul 2023 05:23:21 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Jul 2023 05:23:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Jul 2023 05:23:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Jul 2023 05:23:22 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Jul 2023 05:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 05:23:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e11a5919e5746092b2a288f71090ffdb0d3544b7b54c31ed0137e6d5d4735`  
		Last Modified: Tue, 04 Jul 2023 15:38:37 GMT  
		Size: 45.0 MB (45009079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80987dc89da28aa5ceec7a86ea74e13cee06ecd9304cf4c92d8f382c79eb4f2`  
		Last Modified: Tue, 04 Jul 2023 15:38:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de67c7824eef053da628456fe8aba244c4150024af9454dd4091763920d836c`  
		Last Modified: Wed, 05 Jul 2023 03:14:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f07e56c3d3019cd346deaeacbe572b15b26a924c19b6386877b47123a89e`  
		Last Modified: Tue, 11 Jul 2023 01:39:24 GMT  
		Size: 12.3 MB (12283700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2422cddd65b0ff63d783c999d005c42281720b8615f5872e1e8fdb32dd9981d9`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 455.1 KB (455052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b023f0d964d565a960e567dcaaa605fdff6da02b54971f4d0693506b481b8c`  
		Last Modified: Tue, 11 Jul 2023 01:39:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968d46d099e01403854799f31b6235698a474c27fd58b0172b1eb3889cd5067f`  
		Last Modified: Tue, 11 Jul 2023 05:26:50 GMT  
		Size: 174.3 MB (174313369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2894444c04152ca46b568422ea482a66ed3763028ff87cc82d80132ea0e4cdd`  
		Last Modified: Tue, 11 Jul 2023 05:26:46 GMT  
		Size: 304.2 MB (304236690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77118bb73ac2d6b789413d31beabdbb72e88543cca5b3e6406076fd10d40d8d3`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eb9df1942e9402403596582620c7fb14dbdd8e12de634c88e080cc5795a812`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23fb311f1a568af6e8b96dcb8cfb10d4d96a88aee4243256a3e73f4727fa318`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd3c555379bf5bd7f8d13501bb806b6b5ffb4c2ecb169ce4485f1cbf0d26b9a`  
		Last Modified: Tue, 11 Jul 2023 05:26:32 GMT  
		Size: 6.0 KB (6006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254381348a57ea56306a83d8f2a89630202f393f54d6102b5652be9cfa10f8f`  
		Last Modified: Tue, 11 Jul 2023 05:26:33 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
