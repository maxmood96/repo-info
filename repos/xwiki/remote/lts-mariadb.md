## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:41015316e463d57de352e87c2040386d42b77b396563dc8d3ef53c264fa39d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:d395437941e3edb163c09d304ab32fefb2ee6a36fd5ea43fe0a9b964a692536d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.6 MB (573563835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106b06be88ff178e966bd53df69efbff74c273aedd7fb1ac6b702b782fb25fba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:20 GMT
ADD file:6cd2e13356aa5339c1f2abd3c210a52f6ed74fae05cd61aa09f37b6a4764f65c in / 
# Tue, 04 Oct 2022 23:35:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 16:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 16:59:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 17:00:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:01:31 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 05 Oct 2022 17:02:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 05 Oct 2022 17:02:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 06 Oct 2022 05:18:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Oct 2022 05:18:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 05:18:33 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 06 Oct 2022 05:18:33 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Oct 2022 05:18:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Oct 2022 05:18:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Oct 2022 05:25:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Oct 2022 05:25:51 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Oct 2022 00:08:04 GMT
ENV TOMCAT_VERSION=9.0.68
# Sat, 08 Oct 2022 00:08:04 GMT
ENV TOMCAT_SHA512=840b21c5cd2bfea7bbfed99741c166608fa1515bb00475ebd4eccfd4f3ed2a1be6bfffd590b2a6600003205b62f271b6ba0937e557fc65a536df61cb4f7b7c8f
# Sat, 08 Oct 2022 00:08:04 GMT
COPY dir:e73e3631cb353a0953a6b8788956ed401a34aaa6d3cbf09074d5766c2961573c in /usr/local/tomcat 
# Sat, 08 Oct 2022 00:08:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 08 Oct 2022 00:08:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 08 Oct 2022 00:08:10 GMT
EXPOSE 8080
# Sat, 08 Oct 2022 00:08:10 GMT
CMD ["catalina.sh" "run"]
# Sat, 08 Oct 2022 00:41:45 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Sat, 08 Oct 2022 00:41:45 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Sat, 08 Oct 2022 00:41:45 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Sat, 08 Oct 2022 00:41:45 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Sat, 08 Oct 2022 00:41:45 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Sat, 08 Oct 2022 00:41:46 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Sat, 08 Oct 2022 00:42:38 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 08 Oct 2022 00:48:39 GMT
ENV XWIKI_VERSION=13.10.9
# Sat, 08 Oct 2022 00:48:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.9
# Sat, 08 Oct 2022 00:48:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=ad57639016b1bfd1cdf84de764b310a65416832645c6bbfd933ec26fd977bb6a
# Sat, 08 Oct 2022 00:49:17 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 08 Oct 2022 00:50:16 GMT
ENV MARIADB_JDBC_VERSION=3.0.7
# Sat, 08 Oct 2022 00:50:16 GMT
ENV MARIADB_JDBC_SHA256=96c7bb2e6228ccbdf88dd4b071346979fa1216196a24aca3d1fb9e4199698bef
# Sat, 08 Oct 2022 00:50:16 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.7
# Sat, 08 Oct 2022 00:50:16 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.7.jar
# Sat, 08 Oct 2022 00:50:16 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.7.jar
# Sat, 08 Oct 2022 00:50:17 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Sat, 08 Oct 2022 00:50:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 08 Oct 2022 00:50:17 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 08 Oct 2022 00:50:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 08 Oct 2022 00:50:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 08 Oct 2022 00:50:18 GMT
VOLUME [/usr/local/xwiki]
# Sat, 08 Oct 2022 00:50:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 00:50:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:cf92e523b49ea3d1fae59f5f082437a5f96c244fda6697995920142ff31d59cf`  
		Last Modified: Tue, 04 Oct 2022 03:04:01 GMT  
		Size: 30.4 MB (30428928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4c7f172af2471a1945e9feb3dab4254026b8c38f20c75ae781436a4495e6db`  
		Last Modified: Wed, 05 Oct 2022 17:07:10 GMT  
		Size: 12.4 MB (12442343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521599bc479fb2b0da911ac0f7237ba1dd87823d0d2b609de333aef4766022a0`  
		Last Modified: Wed, 05 Oct 2022 17:09:25 GMT  
		Size: 46.5 MB (46498622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd90861fe76e553b9447451baf69d735ce869c254ee2968b0e893c35bd7a38`  
		Last Modified: Wed, 05 Oct 2022 17:09:19 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba416a4250746409b3c6db8225e8a0b0e59fcac990b18d4e524f989705055f9`  
		Last Modified: Thu, 06 Oct 2022 05:39:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aefc9ef78986ecc1379e087a1a553201a82680cf5f2503b61d69b96c80492ee`  
		Last Modified: Sat, 08 Oct 2022 00:19:39 GMT  
		Size: 12.2 MB (12192002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b673e50fff974c40ac161c0b405fb0aee5481f6df19da4980bcf939adf2fcc`  
		Last Modified: Sat, 08 Oct 2022 00:19:38 GMT  
		Size: 452.6 KB (452644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026cbea7dd95773d548c970dca685fc3ad9346a738d8245cf9f123833c18bfeb`  
		Last Modified: Sat, 08 Oct 2022 00:19:38 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104d29f3d11d9a454dd20c685a5969c038d89d4ca179a064f10ce5eae5455e6b`  
		Last Modified: Sat, 08 Oct 2022 00:51:37 GMT  
		Size: 178.3 MB (178317644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910d32ed23bb022dc22977105c9f9007d694a7749d3e7197aeb71473e6d529aa`  
		Last Modified: Sat, 08 Oct 2022 00:54:56 GMT  
		Size: 292.7 MB (292675757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d2aea275d6d0118150f998df034bf331cbb4f0e1d499e1b70ede85b14775c6`  
		Last Modified: Sat, 08 Oct 2022 00:56:06 GMT  
		Size: 543.9 KB (543936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52abd7617baf93dc75646fa84f66c620fd6c15d56cbd69886a4a170358c728`  
		Last Modified: Sat, 08 Oct 2022 00:56:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ea5e0afacd521d54a42b49acdc4a9f5ed3d61dbc3a3b73b11e3839a3c003d`  
		Last Modified: Sat, 08 Oct 2022 00:56:06 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d95c61bb7779e15aeb9da1e85447299097cbcf87afd8bc8be529119b819fc74`  
		Last Modified: Sat, 08 Oct 2022 00:56:06 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2129c8a5fdb7c24171a7eb10377f4ec9e886feafb76f56de041a20fa5e20a2cd`  
		Last Modified: Sat, 08 Oct 2022 00:56:06 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ac935da70b19b573c63473cc3b84489da01edf3ed2a7d93db3975a004d3aa9f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564581722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d84e4df9bdfa7f3340b1f052d1d32815aaa3609797f1ed1407b51ce9239b241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 15:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 15:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 15:44:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 15:44:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 15:45:34 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 05 Oct 2022 15:46:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 05 Oct 2022 15:46:13 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 06 Oct 2022 04:22:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Oct 2022 04:22:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 04:22:57 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 06 Oct 2022 04:22:58 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Oct 2022 04:22:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Oct 2022 04:23:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Oct 2022 04:34:36 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Oct 2022 04:34:36 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Oct 2022 00:58:32 GMT
ENV TOMCAT_VERSION=9.0.68
# Sat, 08 Oct 2022 00:58:32 GMT
ENV TOMCAT_SHA512=840b21c5cd2bfea7bbfed99741c166608fa1515bb00475ebd4eccfd4f3ed2a1be6bfffd590b2a6600003205b62f271b6ba0937e557fc65a536df61cb4f7b7c8f
# Sat, 08 Oct 2022 00:58:34 GMT
COPY dir:fa49e39ae2f475dac28f72274dea16e700c8bcfd6cfca9cc001aca56b6128b56 in /usr/local/tomcat 
# Sat, 08 Oct 2022 00:58:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 08 Oct 2022 00:58:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 08 Oct 2022 00:58:43 GMT
EXPOSE 8080
# Sat, 08 Oct 2022 00:58:44 GMT
CMD ["catalina.sh" "run"]
# Sat, 08 Oct 2022 01:56:37 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Sat, 08 Oct 2022 01:56:37 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Sat, 08 Oct 2022 01:56:38 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Sat, 08 Oct 2022 01:56:39 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Sat, 08 Oct 2022 01:56:40 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Sat, 08 Oct 2022 01:56:41 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Sat, 08 Oct 2022 01:57:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 08 Oct 2022 02:02:53 GMT
ENV XWIKI_VERSION=13.10.9
# Sat, 08 Oct 2022 02:02:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.9
# Sat, 08 Oct 2022 02:02:54 GMT
ENV XWIKI_DOWNLOAD_SHA256=ad57639016b1bfd1cdf84de764b310a65416832645c6bbfd933ec26fd977bb6a
# Sat, 08 Oct 2022 02:03:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 08 Oct 2022 02:05:06 GMT
ENV MARIADB_JDBC_VERSION=3.0.7
# Sat, 08 Oct 2022 02:05:07 GMT
ENV MARIADB_JDBC_SHA256=96c7bb2e6228ccbdf88dd4b071346979fa1216196a24aca3d1fb9e4199698bef
# Sat, 08 Oct 2022 02:05:07 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.7
# Sat, 08 Oct 2022 02:05:08 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.7.jar
# Sat, 08 Oct 2022 02:05:09 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.7.jar
# Sat, 08 Oct 2022 02:05:11 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Sat, 08 Oct 2022 02:05:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 08 Oct 2022 02:05:13 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 08 Oct 2022 02:05:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 08 Oct 2022 02:05:15 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 08 Oct 2022 02:05:15 GMT
VOLUME [/usr/local/xwiki]
# Sat, 08 Oct 2022 02:05:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 02:05:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02ffb58034794e0992216f802a3c5320c4b6b9cc80080bdd07eb7afa7db54bd`  
		Last Modified: Wed, 05 Oct 2022 15:52:13 GMT  
		Size: 12.4 MB (12397643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43382a3a0a564d75227f823ea20a3578b988363d9b096c1ac1c03114e9a90ea2`  
		Last Modified: Wed, 05 Oct 2022 15:54:38 GMT  
		Size: 44.8 MB (44824352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22de3b9e20aee6838f6495f86ab838f266c1a8a643586fa3020e111e3559d283`  
		Last Modified: Wed, 05 Oct 2022 15:54:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a35f750fc20e703152b852090896888ff46a0f8426adf60a0368838db583d9a`  
		Last Modified: Thu, 06 Oct 2022 04:57:51 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f376944d44c69cfb7778730de75142261973a0ca11995dd57e3ccdbf63e8fa`  
		Last Modified: Sat, 08 Oct 2022 01:17:16 GMT  
		Size: 12.2 MB (12199808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b35b1dacef52a0d2e4d886eaf5963c75c976b63545bbf38ff858581fca005d0`  
		Last Modified: Sat, 08 Oct 2022 01:17:15 GMT  
		Size: 214.3 KB (214348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51db575290309c95fa6457233dd51b7c4e2615395cd6c12a3cbaccc64d7f243`  
		Last Modified: Sat, 08 Oct 2022 02:07:18 GMT  
		Size: 173.3 MB (173331708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e69bea0449f0f3a0bed2d8497f5a0502eb2bea09f2740d9cdd2e044ffdb60`  
		Last Modified: Sat, 08 Oct 2022 02:11:14 GMT  
		Size: 292.7 MB (292675882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4634391b3c5cf9dd07976563b97b9e072832422ff5f866444f5185272e68220e`  
		Last Modified: Sat, 08 Oct 2022 02:12:43 GMT  
		Size: 543.9 KB (543935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e034f1a87cb2448a70aaa2eb165d3604150965753dad5a1f8783fc583bbd4a0`  
		Last Modified: Sat, 08 Oct 2022 02:12:42 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9717c0ec251e877087fbc62cf1c17137cb729be9828a0f446e3785096e7c4e59`  
		Last Modified: Sat, 08 Oct 2022 02:12:42 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0a5bd6b29aaf48ced186aef31811f0aeac7dc9c94a1b9eae08cb898aa887e9`  
		Last Modified: Sat, 08 Oct 2022 02:12:43 GMT  
		Size: 5.3 KB (5336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df206e9c4a740e7f9a23978c815e4121d88f11ebcbebc8fd6677654d062a0129`  
		Last Modified: Sat, 08 Oct 2022 02:12:42 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
