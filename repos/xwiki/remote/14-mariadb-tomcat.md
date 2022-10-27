## `xwiki:14-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:86fd55d056f2e430bce719743bd3bf0137cb7ccc25677b907870e3cd6f78956d
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
$ docker pull xwiki@sha256:599c4eb7a98d9cfcff1d9b4237a2b89c8a53e2ddf0ffc8e88e1909823b9d87f8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583321591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95ba82440b5f402b5a5e7a74c6e3e17232eecb0dba54323c228419b0ccb1215`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:08:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 01:08:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 01:08:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Oct 2022 01:09:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 01:10:29 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 26 Oct 2022 01:11:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Oct 2022 01:11:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Oct 2022 17:11:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Oct 2022 17:11:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 17:11:05 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Oct 2022 17:11:05 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Oct 2022 17:11:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Oct 2022 17:11:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 26 Oct 2022 17:19:37 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 26 Oct 2022 17:19:37 GMT
ENV TOMCAT_MAJOR=9
# Wed, 26 Oct 2022 17:19:37 GMT
ENV TOMCAT_VERSION=9.0.68
# Wed, 26 Oct 2022 17:19:37 GMT
ENV TOMCAT_SHA512=840b21c5cd2bfea7bbfed99741c166608fa1515bb00475ebd4eccfd4f3ed2a1be6bfffd590b2a6600003205b62f271b6ba0937e557fc65a536df61cb4f7b7c8f
# Wed, 26 Oct 2022 17:19:38 GMT
COPY dir:19b70270aa9cf6d706cd5db112445c59eb2a1298cc73e91aab9918f3461b4435 in /usr/local/tomcat 
# Wed, 26 Oct 2022 17:19:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 17:19:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 26 Oct 2022 17:19:42 GMT
EXPOSE 8080
# Wed, 26 Oct 2022 17:19:42 GMT
CMD ["catalina.sh" "run"]
# Wed, 26 Oct 2022 18:58:51 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 26 Oct 2022 18:58:51 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 26 Oct 2022 18:58:51 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 26 Oct 2022 18:58:51 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 26 Oct 2022 18:58:52 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 26 Oct 2022 18:58:52 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 26 Oct 2022 18:59:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 18:59:56 GMT
ENV XWIKI_VERSION=14.9
# Wed, 26 Oct 2022 18:59:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.9
# Wed, 26 Oct 2022 18:59:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a8639b590b2612c1603ac6788fe83b4d79dbaad484cc5c60230c00f16781460
# Wed, 26 Oct 2022 19:00:36 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 26 Oct 2022 19:02:07 GMT
ENV MARIADB_JDBC_VERSION=3.0.8
# Wed, 26 Oct 2022 19:02:07 GMT
ENV MARIADB_JDBC_SHA256=83697e1c44e77476123ab63cd8bb2ca96c1a349269f307c339f97caced2d0dd6
# Wed, 26 Oct 2022 19:02:07 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.8
# Wed, 26 Oct 2022 19:02:07 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.8.jar
# Wed, 26 Oct 2022 19:02:07 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.8.jar
# Wed, 26 Oct 2022 19:02:08 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 26 Oct 2022 19:02:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 26 Oct 2022 19:02:08 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 26 Oct 2022 19:02:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 26 Oct 2022 19:02:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 26 Oct 2022 19:02:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Oct 2022 19:02:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 19:02:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d33b973dbba18a894c3b9064cedfece84e92985bce6e3be86a5efef3afdea8`  
		Last Modified: Wed, 26 Oct 2022 01:16:34 GMT  
		Size: 12.4 MB (12400371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6960b661b00d7e89ea4da7f8c5d2b571d0fd35007d448e17a2d178931aa42`  
		Last Modified: Wed, 26 Oct 2022 01:19:26 GMT  
		Size: 44.8 MB (44824650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d046e5da0a7155986a366554538db9c6dc0dc232da3c7371c4a7f8820c766739`  
		Last Modified: Wed, 26 Oct 2022 01:19:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2b7e8ec1dfcdbb8e5a9b2d91a66efd6e7890187e39b81ae20b3e7cdcd34fcd`  
		Last Modified: Wed, 26 Oct 2022 17:35:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4faa8a44e55bcf121db0d88d2c2c46596dead61108d821af57ed2cd29027445`  
		Last Modified: Wed, 26 Oct 2022 17:42:49 GMT  
		Size: 12.2 MB (12200353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c86ceac19f6bc02db83ad0acfe2ab7352de33d019ba1b9c9255ae48cce51489`  
		Last Modified: Wed, 26 Oct 2022 17:42:48 GMT  
		Size: 452.0 KB (452025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c1d8957962e1a8cc040e5ae2ae5ae95f438b443ba81a3cf40fa90f1795475c`  
		Last Modified: Wed, 26 Oct 2022 17:42:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25ebb686f00443c8cd847abee8fe08d4717be2c9adcd14f2aa6f3d12ae0d3f1`  
		Last Modified: Wed, 26 Oct 2022 19:06:42 GMT  
		Size: 173.8 MB (173833567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2102515b2842423faa98e4254ac0183876f9d28a6c79a15f5d27f64f29148e4`  
		Last Modified: Wed, 26 Oct 2022 19:06:38 GMT  
		Size: 310.7 MB (310670005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f72306e366b117bec27eb61987c9c548012deb38c34d2a8250f78eac547976`  
		Last Modified: Wed, 26 Oct 2022 19:08:06 GMT  
		Size: 545.5 KB (545498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf1ad2655ec9d8389c27d2fbc8adfadf301e72a1ff8c3efdb73985cfb0a8f00`  
		Last Modified: Wed, 26 Oct 2022 19:08:06 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90a93a719e6521f8281f47a380f31a01ced3c3427c2cf9b39342faa1c69e453`  
		Last Modified: Wed, 26 Oct 2022 19:08:06 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff2c69e683c8426a6da4ba019a2a5b421a687ee84263d830ddd7ec58bac51d`  
		Last Modified: Wed, 26 Oct 2022 19:08:06 GMT  
		Size: 6.0 KB (6002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b06a13ab092d80c1639d7670e514bc49474cf815c3e123af2129aeccd6d2975`  
		Last Modified: Wed, 26 Oct 2022 19:08:06 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
