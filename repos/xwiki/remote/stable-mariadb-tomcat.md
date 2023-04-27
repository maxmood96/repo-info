## `xwiki:stable-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:b469d2bc1f91fcbc16cc59a7ae76c2a1fdc41efc2fd151a7d13abdf63c79652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7885dda24d524317a268f45f37b4f23ccf48524006aa4343c0f14a370fb76218
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.4 MB (590351611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9c9e0555a8d133df1e3db2d3aa71f2acda6443a482135adf09930a4abdd6b0`
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
# Wed, 26 Apr 2023 19:21:22 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 26 Apr 2023 19:22:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Apr 2023 19:22:17 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 26 Apr 2023 21:37:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Apr 2023 21:37:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 21:37:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 26 Apr 2023 21:37:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Apr 2023 21:37:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Apr 2023 21:37:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 26 Apr 2023 21:39:48 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 26 Apr 2023 21:39:48 GMT
ENV TOMCAT_MAJOR=9
# Wed, 26 Apr 2023 21:39:48 GMT
ENV TOMCAT_VERSION=9.0.74
# Wed, 26 Apr 2023 21:39:48 GMT
ENV TOMCAT_SHA512=0e173fc2a76404c41c571c50a1956a2b867870d767200bd30f48d89bf04a4b6337f12e6577415da932cd2dfef9b4e9e9fdd52bd873afb06c6258b0e64244a44e
# Wed, 26 Apr 2023 21:39:49 GMT
COPY dir:5320b315c314b0e9f3cc6996868871dc8ed5e2b7036f98555dcf5deb36030170 in /usr/local/tomcat 
# Wed, 26 Apr 2023 21:39:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 21:39:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 26 Apr 2023 21:39:55 GMT
EXPOSE 8080
# Wed, 26 Apr 2023 21:39:55 GMT
CMD ["catalina.sh" "run"]
# Wed, 26 Apr 2023 23:27:30 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 26 Apr 2023 23:27:30 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 26 Apr 2023 23:27:30 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 26 Apr 2023 23:27:30 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 26 Apr 2023 23:27:30 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 26 Apr 2023 23:27:30 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 26 Apr 2023 23:29:06 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 23:29:07 GMT
ENV XWIKI_VERSION=15.3
# Wed, 26 Apr 2023 23:29:07 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Wed, 26 Apr 2023 23:29:07 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Wed, 26 Apr 2023 23:29:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 26 Apr 2023 23:31:16 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 26 Apr 2023 23:31:16 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 26 Apr 2023 23:31:16 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 26 Apr 2023 23:31:16 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 26 Apr 2023 23:31:16 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 26 Apr 2023 23:31:17 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 26 Apr 2023 23:31:17 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 26 Apr 2023 23:31:17 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 26 Apr 2023 23:31:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 26 Apr 2023 23:31:18 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 26 Apr 2023 23:31:18 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Apr 2023 23:31:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Apr 2023 23:31:18 GMT
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
	-	`sha256:bfbcf8099cd9542ade150b47ea122e9893483fa7b4eeb7cb77dcd4fce39e8daf`  
		Last Modified: Wed, 26 Apr 2023 19:31:33 GMT  
		Size: 46.7 MB (46666342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3863dc13d82a92b998a5173cbace3570e2ae1e307b6f15c1a615218421c75f7`  
		Last Modified: Wed, 26 Apr 2023 19:31:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604e9cacab100369ab7798fdac4858aa39492f22e4dc4aaa8f1be05b524bfc15`  
		Last Modified: Wed, 26 Apr 2023 21:51:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a016b39d8d26774e51e6a79fcb03c5f3206045b806b5f3609556773179d787ef`  
		Last Modified: Wed, 26 Apr 2023 21:53:17 GMT  
		Size: 12.2 MB (12233838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db258d59e12806948bf3e4af14a5d62d87e867a14562a0fba551388742906574`  
		Last Modified: Wed, 26 Apr 2023 21:53:16 GMT  
		Size: 3.0 MB (2967684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dce82d22e3a93205400ba38dc99d3f09142785886bd8d1b0b0f656e936bba7`  
		Last Modified: Wed, 26 Apr 2023 21:53:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7a163738aedd6a170822731b8a82a6768963eb6bec68f44fd6672fb36eb8f7`  
		Last Modified: Wed, 26 Apr 2023 23:33:42 GMT  
		Size: 178.8 MB (178803411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0515acaf9499c4279f40b03723634de1f5c7e31853c386099d24bceef4427`  
		Last Modified: Wed, 26 Apr 2023 23:33:35 GMT  
		Size: 306.2 MB (306214312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a56072a25afbf01b2e70cbf0866c3458d62a7c71ceb2420d958d70d5a80ca0`  
		Last Modified: Wed, 26 Apr 2023 23:34:53 GMT  
		Size: 591.4 KB (591380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86501b7750d528f27d91104f5807e2e1155d234661edbcf2ee6b54de00d07849`  
		Last Modified: Wed, 26 Apr 2023 23:34:53 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2de90956d2ba711d83d8439521fe72a48d7faa179b77b7243abef4885127e8d`  
		Last Modified: Wed, 26 Apr 2023 23:34:53 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fa0f98e2768b6c60630a0b65f8a574796a6b6b2d28d8d957728a5023d41181`  
		Last Modified: Wed, 26 Apr 2023 23:34:53 GMT  
		Size: 6.0 KB (6003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd621caf954b2d78643bb9637433c5b064bbe741c3d0e6328dcb7b444c97157`  
		Last Modified: Wed, 26 Apr 2023 23:34:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:9bcce733628b65c1d18b3e6061502fda39e748a9a2f14f9c8162337ac0e8a0a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579091791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e12d4e1698d8e438d0b44d4ba926935837f601f4b1f98cdec2d888357b4209b`
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
# Tue, 18 Apr 2023 18:52:07 GMT
ENV TOMCAT_VERSION=9.0.74
# Tue, 18 Apr 2023 18:52:07 GMT
ENV TOMCAT_SHA512=0e173fc2a76404c41c571c50a1956a2b867870d767200bd30f48d89bf04a4b6337f12e6577415da932cd2dfef9b4e9e9fdd52bd873afb06c6258b0e64244a44e
# Tue, 18 Apr 2023 18:52:07 GMT
COPY dir:b94dfbcf4858b330b226547924806e1b255c80d9eefd6f920f4f0b5c4e1f0250 in /usr/local/tomcat 
# Tue, 18 Apr 2023 18:52:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 18:52:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 18 Apr 2023 18:52:12 GMT
EXPOSE 8080
# Tue, 18 Apr 2023 18:52:12 GMT
CMD ["catalina.sh" "run"]
# Tue, 18 Apr 2023 19:17:25 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 18 Apr 2023 19:17:25 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 18 Apr 2023 19:17:25 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 18 Apr 2023 19:17:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 18 Apr 2023 19:17:25 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 18 Apr 2023 19:17:25 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 18 Apr 2023 19:19:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2023 20:04:18 GMT
ENV XWIKI_VERSION=15.3
# Mon, 24 Apr 2023 20:04:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.3
# Mon, 24 Apr 2023 20:04:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=fbe35bcc5c6cc5764f2a1da4aca7878531f93bae069d94f399fea7d9656da3b8
# Mon, 24 Apr 2023 20:04:59 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 26 Apr 2023 20:12:27 GMT
ENV MARIADB_JDBC_VERSION=3.1.3
# Wed, 26 Apr 2023 20:12:27 GMT
ENV MARIADB_JDBC_SHA256=11297ee6562426c49c81387c860153cbc131c4c3d042492d4f6d2d97ab3a1ca5
# Wed, 26 Apr 2023 20:12:27 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.3
# Wed, 26 Apr 2023 20:12:27 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.3.jar
# Wed, 26 Apr 2023 20:12:27 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.3.jar
# Wed, 26 Apr 2023 20:12:28 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Wed, 26 Apr 2023 20:12:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 26 Apr 2023 20:12:28 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 26 Apr 2023 20:12:29 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 26 Apr 2023 20:12:29 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 26 Apr 2023 20:12:29 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Apr 2023 20:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Apr 2023 20:12:29 GMT
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
	-	`sha256:edfb81f094e6a6a870ffea107549c3fc9e764c3a5b355bd9026647a4f6608361`  
		Last Modified: Tue, 18 Apr 2023 18:59:25 GMT  
		Size: 12.2 MB (12239983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527f1da0c7c14cb3fb1f4e53608e43bdef0d02e0d7fe7fe313555dfe7d81653c`  
		Last Modified: Tue, 18 Apr 2023 18:59:24 GMT  
		Size: 453.2 KB (453238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09937d2ad0d5f48261d3c08e0ce2c5f3780b680da57a3e392c91b9e741786373`  
		Last Modified: Tue, 18 Apr 2023 18:59:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a03b97228fd3e0465a1aaa6b21c9e190343955e6a218ab2f9059174bab8c23e`  
		Last Modified: Tue, 18 Apr 2023 19:24:00 GMT  
		Size: 173.8 MB (173824886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97beeee5f71e2e004de007330738b7841a32e5d90ca23c494d89836957dbe516`  
		Last Modified: Mon, 24 Apr 2023 20:06:34 GMT  
		Size: 306.2 MB (306214361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4517ddd4d4010e43d4baaf6e5262e4fbd8c01dd9fccdb2c8e3588a824ce13b6`  
		Last Modified: Wed, 26 Apr 2023 20:14:43 GMT  
		Size: 591.4 KB (591379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97238df0ffa0adec095885262536b968d1cb50290aeee7b3c679535066fed63b`  
		Last Modified: Wed, 26 Apr 2023 20:14:42 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bfdb5cc4e18227906fbacb775366f635f44bf511d3f7425baea6c661fa7202`  
		Last Modified: Wed, 26 Apr 2023 20:14:42 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431f3b6cb02cf91663e379127c5c6f6aaf4041c2a8413eec7de685fbfec3054`  
		Last Modified: Wed, 26 Apr 2023 20:14:42 GMT  
		Size: 6.0 KB (6004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee32407d58e410abf1cb578c410c2529897594d555a7bf1c0148db1a425fa0a9`  
		Last Modified: Wed, 26 Apr 2023 20:14:42 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
