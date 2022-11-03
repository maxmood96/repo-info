## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:4fcc772a179ab286b83a676232553d1a805c011bb85fdc18c4f7051dbb98108f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b50efdfb647abea4752b639cd70ede854ab7e4ce8f0d6b44b61bc7afe2a48240
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.4 MB (573403522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724842a80c7d56ebd71971dc2a0d1fedf7c180bd2a5cef56854190a5223264fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:44:43 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 02 Nov 2022 18:45:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 02 Nov 2022 18:45:12 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 02 Nov 2022 21:33:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Nov 2022 21:33:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:33:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Nov 2022 21:33:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Nov 2022 21:33:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Nov 2022 21:33:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Nov 2022 21:38:06 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 02 Nov 2022 21:38:06 GMT
ENV TOMCAT_MAJOR=9
# Wed, 02 Nov 2022 21:38:06 GMT
ENV TOMCAT_VERSION=9.0.68
# Wed, 02 Nov 2022 21:38:06 GMT
ENV TOMCAT_SHA512=840b21c5cd2bfea7bbfed99741c166608fa1515bb00475ebd4eccfd4f3ed2a1be6bfffd590b2a6600003205b62f271b6ba0937e557fc65a536df61cb4f7b7c8f
# Wed, 02 Nov 2022 21:38:07 GMT
COPY dir:e63c5975fdb9f306a6f5cb6c414dd7eebee1419e16a1c1c1184fff59a16d74d8 in /usr/local/tomcat 
# Wed, 02 Nov 2022 21:38:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:38:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Nov 2022 21:38:12 GMT
EXPOSE 8080
# Wed, 02 Nov 2022 21:38:12 GMT
CMD ["catalina.sh" "run"]
# Wed, 02 Nov 2022 23:20:30 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 02 Nov 2022 23:20:30 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 02 Nov 2022 23:20:30 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 02 Nov 2022 23:20:30 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 02 Nov 2022 23:20:30 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 02 Nov 2022 23:20:31 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 02 Nov 2022 23:22:02 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 23:26:03 GMT
ENV XWIKI_VERSION=13.10.10
# Wed, 02 Nov 2022 23:26:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.10
# Wed, 02 Nov 2022 23:26:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=bae87a16d291d321d0848fcba55e455bfcd4b1890597cd9b735d98013cf44bad
# Wed, 02 Nov 2022 23:26:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 02 Nov 2022 23:27:40 GMT
ENV MARIADB_JDBC_VERSION=3.0.8
# Wed, 02 Nov 2022 23:27:40 GMT
ENV MARIADB_JDBC_SHA256=83697e1c44e77476123ab63cd8bb2ca96c1a349269f307c339f97caced2d0dd6
# Wed, 02 Nov 2022 23:27:40 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.8
# Wed, 02 Nov 2022 23:27:40 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.8.jar
# Wed, 02 Nov 2022 23:27:40 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.8.jar
# Wed, 02 Nov 2022 23:27:41 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 02 Nov 2022 23:27:41 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 02 Nov 2022 23:27:41 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 02 Nov 2022 23:27:42 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 02 Nov 2022 23:27:42 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 02 Nov 2022 23:27:42 GMT
VOLUME [/usr/local/xwiki]
# Wed, 02 Nov 2022 23:27:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 23:27:42 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04db4e9955234ee09d3841f061130e4786af3cb6eac54bee80fc90addfbdcfc5`  
		Last Modified: Wed, 02 Nov 2022 18:50:01 GMT  
		Size: 46.5 MB (46498554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64251325dc0523aef6d2542a1756af2f8fcf3f34eb9acd7deafbf1bbdd12ae98`  
		Last Modified: Wed, 02 Nov 2022 18:49:54 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f35b3e4644cfc48d4015afd1123bcd49c0519d404bded8d2bf79cabc87ad31e`  
		Last Modified: Wed, 02 Nov 2022 21:48:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7aee9dff2cc3602a2d3796724c828f2f01b4b449968dff34b9962946a401622`  
		Last Modified: Wed, 02 Nov 2022 21:52:57 GMT  
		Size: 12.2 MB (12192339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61bd71b6f38b377abeafe2c657195a29bca8aee8a4c25ce297c17ffcdf03f9a`  
		Last Modified: Wed, 02 Nov 2022 21:52:56 GMT  
		Size: 452.7 KB (452684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2529ce46c42e7023da805a9dba8ad644fd671f364e8a35c8bcc7997c11e0afa1`  
		Last Modified: Wed, 02 Nov 2022 21:52:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d80dc2aba4926947902c526968d04bdd54be6ce545d3fc8e40ba1fd9df98bd8`  
		Last Modified: Wed, 02 Nov 2022 23:29:02 GMT  
		Size: 178.3 MB (178345232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8777a9725e0806d8b42f60f75980f1781f3282d579667e6afa28e4f8b3217e`  
		Last Modified: Wed, 02 Nov 2022 23:32:23 GMT  
		Size: 292.5 MB (292492623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d385fb54b41d1b08cfb1fca4ebb7a1325bba313cbaabd51bfe4b841c79d3cb9c`  
		Last Modified: Wed, 02 Nov 2022 23:33:32 GMT  
		Size: 545.5 KB (545501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272eb2e32c9890318b11a2cef05ac8849a986f644846e36abbbdb1e073f92274`  
		Last Modified: Wed, 02 Nov 2022 23:33:31 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a9ff45e909aeb3dcf5d617ab60448ade7c7e77f237a2dfd7a519aa2afe9fab`  
		Last Modified: Wed, 02 Nov 2022 23:33:31 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b079f0ad5659696a121c2673e06ac882ee0ffac06b420f262b2e5e84fae7aa`  
		Last Modified: Wed, 02 Nov 2022 23:33:31 GMT  
		Size: 5.4 KB (5362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb4d2ddc7b2a872f733f7363eb818beb3da9fce0220a1f385ce8d03825d3dc3`  
		Last Modified: Wed, 02 Nov 2022 23:33:31 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:dd87e3b71238d3eee19415ba86b7c48ea54f9c8ab74c27037540b1c5d0c7e307
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.7 MB (564670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fa3cd328149cdafbc208cc887e9c746033cf98f4d9a52e80c55a8875de6bc4`
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
# Wed, 02 Nov 2022 23:05:44 GMT
ENV XWIKI_VERSION=13.10.10
# Wed, 02 Nov 2022 23:05:44 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.10
# Wed, 02 Nov 2022 23:05:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=bae87a16d291d321d0848fcba55e455bfcd4b1890597cd9b735d98013cf44bad
# Wed, 02 Nov 2022 23:06:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 02 Nov 2022 23:07:20 GMT
ENV MARIADB_JDBC_VERSION=3.0.8
# Wed, 02 Nov 2022 23:07:20 GMT
ENV MARIADB_JDBC_SHA256=83697e1c44e77476123ab63cd8bb2ca96c1a349269f307c339f97caced2d0dd6
# Wed, 02 Nov 2022 23:07:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.8
# Wed, 02 Nov 2022 23:07:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.8.jar
# Wed, 02 Nov 2022 23:07:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.8.jar
# Wed, 02 Nov 2022 23:07:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 02 Nov 2022 23:07:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 02 Nov 2022 23:07:21 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 02 Nov 2022 23:07:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 02 Nov 2022 23:07:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 02 Nov 2022 23:07:22 GMT
VOLUME [/usr/local/xwiki]
# Wed, 02 Nov 2022 23:07:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 23:07:22 GMT
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
	-	`sha256:ccdae64ffa5577f0378ea2ecfb96e3653fc188cb19102a23e0a06a05e0c5ccf1`  
		Last Modified: Wed, 02 Nov 2022 23:11:49 GMT  
		Size: 292.5 MB (292492636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b478e1502a7bb848a29c9c6127addfce746e8d8c67b7d368902309f8521f2d`  
		Last Modified: Wed, 02 Nov 2022 23:12:57 GMT  
		Size: 545.5 KB (545497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9d3ce3aceb954487ef12c2a04c19dfb0109276e3f872685a9b98c301d02a0e`  
		Last Modified: Wed, 02 Nov 2022 23:12:57 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f23174e404f5ada098265cac127899de193ea8ca590b6e03e033fdf36f9263`  
		Last Modified: Wed, 02 Nov 2022 23:12:56 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2fec73d26341d58e938ee68d032769aed535fdaf657a86e21a460f6fcea68c`  
		Last Modified: Wed, 02 Nov 2022 23:12:57 GMT  
		Size: 5.4 KB (5359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8c47b5992e9ac3b819c3ee6864d02a1da4bab37d4855af8c9002996a991866`  
		Last Modified: Wed, 02 Nov 2022 23:12:56 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
