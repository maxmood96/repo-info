## `xwiki:14-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:b70f992972e84ca2e708e887209ecb3b8ab80eed0aafe3e8ef8dc6bf28dcd2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:3d8b937679b4d91c6945914438dda015457782e5ead78c8f292553523b8a3251
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592047559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47607807f8f4c06bed98efe3ff1bf85e5da09c6f78ec44bcf8d8950359a2cb61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:27:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 17:27:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 17:27:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 17:28:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 17:28:59 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Tue, 25 Oct 2022 17:29:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Oct 2022 17:29:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Oct 2022 23:44:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Oct 2022 23:44:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 23:44:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Oct 2022 23:44:22 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Oct 2022 23:44:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Oct 2022 23:44:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 26 Oct 2022 23:52:17 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 26 Oct 2022 23:52:17 GMT
ENV TOMCAT_MAJOR=9
# Wed, 26 Oct 2022 23:52:17 GMT
ENV TOMCAT_VERSION=9.0.68
# Wed, 26 Oct 2022 23:52:17 GMT
ENV TOMCAT_SHA512=840b21c5cd2bfea7bbfed99741c166608fa1515bb00475ebd4eccfd4f3ed2a1be6bfffd590b2a6600003205b62f271b6ba0937e557fc65a536df61cb4f7b7c8f
# Wed, 26 Oct 2022 23:52:18 GMT
COPY dir:dcff92a27f2d50b1eb220560589edf710336a78b6a89edba1ace73129b7cf16d in /usr/local/tomcat 
# Wed, 26 Oct 2022 23:52:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 23:52:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 26 Oct 2022 23:52:23 GMT
EXPOSE 8080
# Wed, 26 Oct 2022 23:52:23 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Oct 2022 00:56:37 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 27 Oct 2022 00:56:37 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 27 Oct 2022 00:56:37 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 27 Oct 2022 00:56:38 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 27 Oct 2022 00:56:38 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 27 Oct 2022 00:56:38 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 27 Oct 2022 00:59:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 27 Oct 2022 00:59:03 GMT
ENV XWIKI_VERSION=14.9
# Thu, 27 Oct 2022 00:59:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.9
# Thu, 27 Oct 2022 00:59:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a8639b590b2612c1603ac6788fe83b4d79dbaad484cc5c60230c00f16781460
# Thu, 27 Oct 2022 00:59:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 27 Oct 2022 01:01:23 GMT
ENV MARIADB_JDBC_VERSION=3.0.8
# Thu, 27 Oct 2022 01:01:23 GMT
ENV MARIADB_JDBC_SHA256=83697e1c44e77476123ab63cd8bb2ca96c1a349269f307c339f97caced2d0dd6
# Thu, 27 Oct 2022 01:01:24 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.8
# Thu, 27 Oct 2022 01:01:24 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.8.jar
# Thu, 27 Oct 2022 01:01:24 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.8.jar
# Thu, 27 Oct 2022 01:01:25 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Thu, 27 Oct 2022 01:01:25 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 27 Oct 2022 01:01:25 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 27 Oct 2022 01:01:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 27 Oct 2022 01:01:26 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Oct 2022 01:01:26 GMT
VOLUME [/usr/local/xwiki]
# Thu, 27 Oct 2022 01:01:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Oct 2022 01:01:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4688df200b56af3e7b12bd48807e851b1a3717379161a295d43dd3184abec55e`  
		Last Modified: Wed, 26 Oct 2022 16:43:13 GMT  
		Size: 12.4 MB (12442357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718682ba85da99179194681dc4f4a79880ef8e04829f70aeddc8e43275506085`  
		Last Modified: Wed, 26 Oct 2022 16:45:30 GMT  
		Size: 46.5 MB (46498610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d030909c11444dd48421e92fb65275fccf474ec59fa8530a4fb3cfd9bf36e649`  
		Last Modified: Wed, 26 Oct 2022 16:45:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22bc586e00dcd70b47cf9d79f2eb00512ade1ff0a777bb798602ef75bd2f3f0`  
		Last Modified: Thu, 27 Oct 2022 00:06:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293551d1ea9cf34e154b7baa107ba930a417483190196e459358afe887173769`  
		Last Modified: Thu, 27 Oct 2022 00:12:31 GMT  
		Size: 12.2 MB (12192399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b35b457d2c60567f08d5dd1c41d0a717d722b7893f71c6fc8e270089d9c657e`  
		Last Modified: Thu, 27 Oct 2022 00:12:30 GMT  
		Size: 452.6 KB (452644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f35c608db7b8c968b3d08feda4f5af9873cc8476a93b7184c9bf86ba61dd0ec`  
		Last Modified: Thu, 27 Oct 2022 00:12:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656c93008c018b8f98231982c366abd07c3c2941201e1088671ba8b3c6275830`  
		Last Modified: Thu, 27 Oct 2022 01:06:15 GMT  
		Size: 178.8 MB (178807041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd697cbbb4ba18b9a4a21d1f1f7cfea312aa82ad72fe30ede3150b6ecaa2cf3`  
		Last Modified: Thu, 27 Oct 2022 01:06:07 GMT  
		Size: 310.7 MB (310670019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff461eaabc29971758f591c7471b24988c3021a975a37def990fbd99bc64486`  
		Last Modified: Thu, 27 Oct 2022 01:07:44 GMT  
		Size: 545.5 KB (545500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8f16e43476f5dfdfda7a544305e6330e4f2f1f13a2429a480d83d192407a54`  
		Last Modified: Thu, 27 Oct 2022 01:07:44 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ae4abc95e016e6d48eee1b3e8f57749d7712bd724afb8d34927a9de09ba202`  
		Last Modified: Thu, 27 Oct 2022 01:07:44 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd460afe33e4d5369431c707bb1b5ba445bee235ab0535ddb8f46ff261e08e63`  
		Last Modified: Thu, 27 Oct 2022 01:07:44 GMT  
		Size: 6.0 KB (5997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682a62592b23924cb12da118d7e955a134d699be90e51eddac98bdfd2cf96735`  
		Last Modified: Thu, 27 Oct 2022 01:07:44 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:fcc7ca7b8d7ebfc87131c17cbcfb63c212da47fdaaba4fa69322b694d2d8e584
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.8 MB (582848540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f743adb5012998ac119645924d87d8e18325356666eb5262a830115f1e75db0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:44:58 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 02 Nov 2022 19:45:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 02 Nov 2022 19:45:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 02 Nov 2022 21:30:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Nov 2022 21:30:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:30:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Nov 2022 21:30:55 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Nov 2022 21:30:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Nov 2022 21:30:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Nov 2022 21:34:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 02 Nov 2022 21:34:20 GMT
ENV TOMCAT_MAJOR=9
# Wed, 02 Nov 2022 21:34:20 GMT
ENV TOMCAT_VERSION=9.0.68
# Wed, 02 Nov 2022 21:34:20 GMT
ENV TOMCAT_SHA512=840b21c5cd2bfea7bbfed99741c166608fa1515bb00475ebd4eccfd4f3ed2a1be6bfffd590b2a6600003205b62f271b6ba0937e557fc65a536df61cb4f7b7c8f
# Wed, 02 Nov 2022 21:34:20 GMT
COPY dir:fedf67b23b61dcf03be24e36436f26cdcc138797468e53a383dc0bbba51820d8 in /usr/local/tomcat 
# Wed, 02 Nov 2022 21:34:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:34:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Nov 2022 21:34:25 GMT
EXPOSE 8080
# Wed, 02 Nov 2022 21:34:25 GMT
CMD ["catalina.sh" "run"]
# Wed, 02 Nov 2022 22:58:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 02 Nov 2022 22:58:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 02 Nov 2022 22:58:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 02 Nov 2022 22:58:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 02 Nov 2022 22:58:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 02 Nov 2022 22:58:24 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 02 Nov 2022 23:00:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 23:00:27 GMT
ENV XWIKI_VERSION=14.9
# Wed, 02 Nov 2022 23:00:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.9
# Wed, 02 Nov 2022 23:00:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a8639b590b2612c1603ac6788fe83b4d79dbaad484cc5c60230c00f16781460
# Wed, 02 Nov 2022 23:01:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 02 Nov 2022 23:02:39 GMT
ENV MARIADB_JDBC_VERSION=3.0.8
# Wed, 02 Nov 2022 23:02:39 GMT
ENV MARIADB_JDBC_SHA256=83697e1c44e77476123ab63cd8bb2ca96c1a349269f307c339f97caced2d0dd6
# Wed, 02 Nov 2022 23:02:40 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.8
# Wed, 02 Nov 2022 23:02:40 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.8.jar
# Wed, 02 Nov 2022 23:02:40 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.8.jar
# Wed, 02 Nov 2022 23:02:40 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 02 Nov 2022 23:02:40 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 02 Nov 2022 23:02:41 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 02 Nov 2022 23:02:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 02 Nov 2022 23:02:41 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 02 Nov 2022 23:02:41 GMT
VOLUME [/usr/local/xwiki]
# Wed, 02 Nov 2022 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 23:02:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a23053ec7db1b2114e648a1fdd75a0c318db47d50b2d59c14df3b2fde7d1526`  
		Last Modified: Wed, 02 Nov 2022 19:49:36 GMT  
		Size: 44.8 MB (44824603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756118ab994dacaae5f6c8d8deb6266a31d4f2cf15ef824efc08e12b5ae2a348`  
		Last Modified: Wed, 02 Nov 2022 19:49:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e306b813ce43b862f29cf530b7787a3acf0a110848f57a03ac2efc22dabafd0`  
		Last Modified: Wed, 02 Nov 2022 21:44:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f83fb657864365d330e953cba86cec10ea68dc7fe79aca26951db0ed612db21`  
		Last Modified: Wed, 02 Nov 2022 21:48:50 GMT  
		Size: 12.2 MB (12200330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d0d39acf6e78b3c8e88372b7c01bab06c7c8328c3280a11ec43d24cb8b1052`  
		Last Modified: Wed, 02 Nov 2022 21:48:49 GMT  
		Size: 452.0 KB (451997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf28aa1ec7e5441de9a641dd0dd4155e35df8d263616aa2315b9f86f90ba096`  
		Last Modified: Wed, 02 Nov 2022 21:48:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992b650cf3aeddeee80734f363ff02c0b53ba4e4956ed7b2a744402bdd42d376`  
		Last Modified: Wed, 02 Nov 2022 23:08:34 GMT  
		Size: 173.4 MB (173365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fea34f3ba8a0cfdd82c3496c9c075c86e3c25e8687d0ec817fcbb721d29012`  
		Last Modified: Wed, 02 Nov 2022 23:08:30 GMT  
		Size: 310.7 MB (310670008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143e32200725e1e0ff2f61e7fb1f1f9555777b3a3d5251740cfdeef6c8e6db28`  
		Last Modified: Wed, 02 Nov 2022 23:09:58 GMT  
		Size: 545.5 KB (545498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad05c62d399c8d521c2b3794d86adac7ad1598ddd15afec31a7cdcda9f1d9327`  
		Last Modified: Wed, 02 Nov 2022 23:09:58 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd14fb3ca240aadc666b1a5c3b6c9319ea0227346c6e2833012d3939d3fb98b5`  
		Last Modified: Wed, 02 Nov 2022 23:09:58 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef9dd132f82bcd8e7bf1a53ee18b7011946a09cddedf4a2eead9eb8642faffc`  
		Last Modified: Wed, 02 Nov 2022 23:09:58 GMT  
		Size: 6.0 KB (5999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19a46a917dbf26f56a35ab874c681282b5d6a85b3c1e4230a51dabfb3834d9b`  
		Last Modified: Wed, 02 Nov 2022 23:09:58 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
