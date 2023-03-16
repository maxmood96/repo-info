## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:45a990848913f0260bfe1d4a8b7fc155fbcf633bb7260dd8dedc01a613ff7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:878074c9c5e8f38b1bf4105a181248c95a6380e95857048837c1051466e650b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.0 MB (590013680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc8e55b7654ce26ed6eef0dfef1aabc67715163398a49c5d88a929ac58ed1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:44:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:44:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:45:18 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:45:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:45:50 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 08:06:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 16 Mar 2023 08:06:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 08:06:48 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 16 Mar 2023 08:06:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 16 Mar 2023 08:06:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 08:06:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 08:09:22 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 16 Mar 2023 08:09:22 GMT
ENV TOMCAT_MAJOR=9
# Thu, 16 Mar 2023 08:09:22 GMT
ENV TOMCAT_VERSION=9.0.73
# Thu, 16 Mar 2023 08:09:22 GMT
ENV TOMCAT_SHA512=d43fbd6c5ae00bc0ffc2559743f91abd3547c827426cb0acdc8428e060e8659b6bb41b3877deb061ab6202980de39b9558525a4256725b647d5bff93e47a5664
# Thu, 16 Mar 2023 08:09:23 GMT
COPY dir:a8552bc0e6a9276ddef34306853d8898871794c0552934532613a7357b7e91a4 in /usr/local/tomcat 
# Thu, 16 Mar 2023 08:09:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 08:09:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 16 Mar 2023 08:09:28 GMT
EXPOSE 8080
# Thu, 16 Mar 2023 08:09:28 GMT
CMD ["catalina.sh" "run"]
# Thu, 16 Mar 2023 12:07:46 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 16 Mar 2023 12:07:46 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 16 Mar 2023 12:07:46 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 16 Mar 2023 12:07:46 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 16 Mar 2023 12:07:46 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 16 Mar 2023 12:07:46 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 16 Mar 2023 12:09:22 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 12:09:23 GMT
ENV XWIKI_VERSION=15.1
# Thu, 16 Mar 2023 12:09:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.1
# Thu, 16 Mar 2023 12:09:24 GMT
ENV XWIKI_DOWNLOAD_SHA256=a1c188552733f2b54775e2cf7647fea363954f02679453ffb431e381af52383b
# Thu, 16 Mar 2023 12:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 16 Mar 2023 12:10:04 GMT
ENV MYSQL_JDBC_VERSION=8.0.32
# Thu, 16 Mar 2023 12:10:04 GMT
ENV MYSQL_JDBC_SHA256=522329fe925980f02e5eb89b59d227245d345415ff0c08932a68c9765c13acc5
# Thu, 16 Mar 2023 12:10:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.32
# Thu, 16 Mar 2023 12:10:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.32.jar
# Thu, 16 Mar 2023 12:10:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.32.jar
# Thu, 16 Mar 2023 12:10:05 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 16 Mar 2023 12:10:05 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 16 Mar 2023 12:10:05 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 16 Mar 2023 12:10:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 16 Mar 2023 12:10:06 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 16 Mar 2023 12:10:06 GMT
VOLUME [/usr/local/xwiki]
# Thu, 16 Mar 2023 12:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 12:10:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cabe75b440d785eb2f20422368c248b28fd9c219a5d5db5aacb7de3d43f02c`  
		Last Modified: Thu, 16 Mar 2023 02:50:26 GMT  
		Size: 12.4 MB (12432056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3fc5460b4b76e852651fec42e4cde1337c4bf503657efbe5521f379b19748a`  
		Last Modified: Thu, 16 Mar 2023 02:52:30 GMT  
		Size: 46.6 MB (46635547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a8054900958099c4da9d407d5b7d023cf76df2b891f916546c0ddb7e26a697`  
		Last Modified: Thu, 16 Mar 2023 02:52:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28433e65ef6c711796f104c155386ec51d210e29e92ed4d7859db73e3c2cb719`  
		Last Modified: Thu, 16 Mar 2023 08:23:13 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9591a23e7f43ef5f6ab9df182b4ad5157b4259038072a68acb07701b3af89f1e`  
		Last Modified: Thu, 16 Mar 2023 08:25:30 GMT  
		Size: 12.2 MB (12218371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9947111ddcf080e941129dcddb9744219523f19e48baeb4c074716fd275dabd`  
		Last Modified: Thu, 16 Mar 2023 08:25:29 GMT  
		Size: 454.2 KB (454187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf0a40b1ae136e661d68eb761ac12ce7ddd311a11f7226c7b4132bd020715e3`  
		Last Modified: Thu, 16 Mar 2023 08:25:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187e576cdd94b9b840c169ccc06a628aa8a2451c41c61da396cee3ad90384d25`  
		Last Modified: Thu, 16 Mar 2023 12:14:20 GMT  
		Size: 178.3 MB (178327407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012c053b97d63a1c89da7c1da9f6d1c6c4a94a81c655c7f00ed361eceb22460d`  
		Last Modified: Thu, 16 Mar 2023 12:14:13 GMT  
		Size: 307.2 MB (307160938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e39fefaaeebb622a2a70ba4c74fd1d95377e085c2612eb8706840a4ddb3166b`  
		Last Modified: Thu, 16 Mar 2023 12:13:56 GMT  
		Size: 2.3 MB (2342578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df0d4eabb4ae2f2a2b5625725b82cbc3d6dc09179e1e1d745ec0229031e9f3f`  
		Last Modified: Thu, 16 Mar 2023 12:13:55 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c6e3905daadd32981c8c5b8f4f7e308f33eb3c32b0f811ec1a564926248e3`  
		Last Modified: Thu, 16 Mar 2023 12:13:55 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f1f46fe4632513492f3efb400058543f47511b08ae2d775bf8bb4c8e5cf48`  
		Last Modified: Thu, 16 Mar 2023 12:13:56 GMT  
		Size: 6.0 KB (6011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e1b1fc2729a098ef12f434fda1bc703783e107e1ebc2566af42210d377c5f4`  
		Last Modified: Thu, 16 Mar 2023 12:13:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:6d447b26f07b56895efd6c25ef3fd207c4d263e8599979d0aaf59055cd2d5131
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581298056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918d64a16e32484584c09111a958dbbf869ce9ff4879e8f477ea143767ccc2b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:52:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:52:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:53:41 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:54:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:54:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:27:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 16 Mar 2023 06:27:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:27:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 16 Mar 2023 06:27:32 GMT
WORKDIR /usr/local/tomcat
# Thu, 16 Mar 2023 06:27:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 06:27:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 06:29:35 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 16 Mar 2023 06:29:35 GMT
ENV TOMCAT_MAJOR=9
# Thu, 16 Mar 2023 06:29:35 GMT
ENV TOMCAT_VERSION=9.0.73
# Thu, 16 Mar 2023 06:29:35 GMT
ENV TOMCAT_SHA512=d43fbd6c5ae00bc0ffc2559743f91abd3547c827426cb0acdc8428e060e8659b6bb41b3877deb061ab6202980de39b9558525a4256725b647d5bff93e47a5664
# Thu, 16 Mar 2023 06:29:35 GMT
COPY dir:7e03a56dd94acccb20edfb991abe85f63c4c4cefc0964561979ef20c454c6f7f in /usr/local/tomcat 
# Thu, 16 Mar 2023 06:29:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:29:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 16 Mar 2023 06:29:40 GMT
EXPOSE 8080
# Thu, 16 Mar 2023 06:29:40 GMT
CMD ["catalina.sh" "run"]
# Thu, 16 Mar 2023 08:15:14 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 16 Mar 2023 08:15:14 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 16 Mar 2023 08:15:14 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 16 Mar 2023 08:15:14 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 16 Mar 2023 08:15:14 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 16 Mar 2023 08:15:14 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 16 Mar 2023 08:17:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 08:17:06 GMT
ENV XWIKI_VERSION=15.1
# Thu, 16 Mar 2023 08:17:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.1
# Thu, 16 Mar 2023 08:17:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=a1c188552733f2b54775e2cf7647fea363954f02679453ffb431e381af52383b
# Thu, 16 Mar 2023 08:17:46 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 16 Mar 2023 08:17:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.32
# Thu, 16 Mar 2023 08:17:49 GMT
ENV MYSQL_JDBC_SHA256=522329fe925980f02e5eb89b59d227245d345415ff0c08932a68c9765c13acc5
# Thu, 16 Mar 2023 08:17:49 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.32
# Thu, 16 Mar 2023 08:17:49 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.32.jar
# Thu, 16 Mar 2023 08:17:49 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.32.jar
# Thu, 16 Mar 2023 08:17:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 16 Mar 2023 08:17:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 16 Mar 2023 08:17:50 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 16 Mar 2023 08:17:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 16 Mar 2023 08:17:51 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 16 Mar 2023 08:17:51 GMT
VOLUME [/usr/local/xwiki]
# Thu, 16 Mar 2023 08:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 08:17:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35794a35c4aa2299e9a7a69f4eafa7f96eb1832e2a04b3d85773522111018ca6`  
		Last Modified: Thu, 16 Mar 2023 01:58:19 GMT  
		Size: 12.4 MB (12389767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26126947450108b9349ce5c70904451e6ada86d51dde32223e9d9de1e567f89f`  
		Last Modified: Thu, 16 Mar 2023 02:00:06 GMT  
		Size: 45.0 MB (44977990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a873c16c3848ad12697e893cb753bb353c55c7d09fbbcdb67983aafbbd885b`  
		Last Modified: Thu, 16 Mar 2023 02:00:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c171da1e14cae24bb7b0a542326df4c310966690ef3395e8a77f7387a3638df0`  
		Last Modified: Thu, 16 Mar 2023 06:42:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093a1ba7868819fc0eea09cb177737693f064f00ce71ef96182df8a7fe4014a5`  
		Last Modified: Thu, 16 Mar 2023 06:44:35 GMT  
		Size: 12.2 MB (12225294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318f6e8d20ce877573364770af5908e3ec1f0bfbba59af39c382661185b4c5d9`  
		Last Modified: Thu, 16 Mar 2023 06:44:35 GMT  
		Size: 453.3 KB (453258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66304ac768469e7ea723d940c65dc7b131721d00667081b2ab02c457fdda2c45`  
		Last Modified: Thu, 16 Mar 2023 06:44:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d81738a8533e747794d7efc4b481a28eecd25178deae1fb71c08933a865bec`  
		Last Modified: Thu, 16 Mar 2023 08:22:13 GMT  
		Size: 173.3 MB (173348069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00623febec97fa06c8f5cc6f9ee9078aca706c0cbde6f4f0ff0ba3adf552372d`  
		Last Modified: Thu, 16 Mar 2023 08:22:10 GMT  
		Size: 307.2 MB (307160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796199fdb04a2b81f1d6412bb6e1918d3f697350e46a2d9734daa1cde74838b6`  
		Last Modified: Thu, 16 Mar 2023 08:21:55 GMT  
		Size: 2.3 MB (2342575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95af6d319a94a5b833c687bb33002593fdb8352f92bbb726cf00611a7fa6435b`  
		Last Modified: Thu, 16 Mar 2023 08:21:55 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc426fe90611c0cefc27b5c1604a15eaea4392f7f28b967cd0b6b5cd852ba32`  
		Last Modified: Thu, 16 Mar 2023 08:21:55 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74d6d719312dbc282d411d2a031b957bc388fef99dfa6c77c1500a1787f222c`  
		Last Modified: Thu, 16 Mar 2023 08:21:55 GMT  
		Size: 6.0 KB (6007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1844f0c44e8df253e52ec16854c9f894563e3ac76b190f3a5d64fc075a58cd4`  
		Last Modified: Thu, 16 Mar 2023 08:21:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
