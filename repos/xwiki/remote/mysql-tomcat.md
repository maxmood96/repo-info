## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:d8e0844f747c85acac10a38c602579081de881a555960eafe2f794c5b1b16242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:122960fbaf83861f5c51719ac4563406c7416ea04dc5b79010fbabeeb62f5252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.6 MB (595554801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a3656f54b57513d789de02f0d9b5026a9244b8272bf12c1a683eb9e1d05cbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Feb 2024 13:14:55 GMT
ARG RELEASE
# Mon, 26 Feb 2024 13:14:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 26 Feb 2024 13:14:55 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 13:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Feb 2024 13:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Feb 2024 13:14:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 26 Feb 2024 13:14:55 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 26 Feb 2024 13:14:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 26 Feb 2024 13:14:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Feb 2024 13:14:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 26 Feb 2024 13:14:55 GMT
WORKDIR /usr/local/tomcat
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 26 Feb 2024 13:14:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 26 Feb 2024 13:14:55 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_MAJOR=9
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_VERSION=9.0.87
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Mon, 26 Feb 2024 13:14:55 GMT
COPY dir:40d6dbdce612cc991adb2ee5ce85320942841bbd0b1682a73533c868a43a5fcd in /usr/local/tomcat 
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 26 Feb 2024 13:14:55 GMT
EXPOSE 8080
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT []
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["catalina.sh" "run"]
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 26 Feb 2024 13:14:55 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_VERSION=16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=e236fc101710a0bfefed2328cc66652e265f21ab40dd30e6b7ce52300da744d5
# Mon, 26 Feb 2024 13:14:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Mon, 26 Feb 2024 13:14:55 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2670537dcebc0b445ca47e68b31667f3572b8758b8388e24d8a6770e860ecc8`  
		Last Modified: Wed, 06 Mar 2024 06:09:59 GMT  
		Size: 17.5 MB (17456336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c059ccfa41820fb3f1472c4358304407b00e3eed15933f067b1d4957a40bfc3`  
		Last Modified: Wed, 06 Mar 2024 06:10:45 GMT  
		Size: 47.2 MB (47163248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23d33d59f2ab52fa44e6fbd4e629813614bb753bb3ccac98940e981a3b13c4e`  
		Last Modified: Wed, 06 Mar 2024 06:10:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a648f54390edf0b921f43c547b5d6d6b937e58728be46796f6aefcd4735fb`  
		Last Modified: Wed, 06 Mar 2024 06:10:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abdfee857c0074fe5c75f39fbbf37551ccbc0d9509a3a5fea060b4beafa4ec7`  
		Last Modified: Wed, 06 Mar 2024 15:02:53 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d3bf9e34aeb06417cc1a650b47db29515ca39161db2741c569aa8693558c5`  
		Last Modified: Fri, 15 Mar 2024 00:35:00 GMT  
		Size: 12.4 MB (12421982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ae216fbbd9f86d3022a270437e1fdbf1bf3eacbe277feebc7fd116a074ab31`  
		Last Modified: Fri, 15 Mar 2024 00:34:59 GMT  
		Size: 458.5 KB (458549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e4d00229948d26a05477214e037e219aa38ee6ee20539d3c8f4f2f094ba1f4`  
		Last Modified: Fri, 15 Mar 2024 00:34:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e994715238e38f18958cda60e6714e31e311d70ef08c3bca00e33ecce596a2c9`  
		Last Modified: Fri, 15 Mar 2024 01:49:12 GMT  
		Size: 178.3 MB (178349610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3031e10c4b0f3f91a4de598d6e11ef7ec8cb3d9c00fcfab2df4884c3d603f3bf`  
		Last Modified: Fri, 15 Mar 2024 01:49:15 GMT  
		Size: 306.9 MB (306883031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb66204c31ecdc591fe8a315cc6fb855bc287b27fa0aba5680e6f5cf66fee00`  
		Last Modified: Fri, 15 Mar 2024 01:49:10 GMT  
		Size: 2.4 MB (2356948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d7aa0829f0b9a8b0a5ac423bfbe47e456c6c5e91932e3a7749b6da70cdc59c`  
		Last Modified: Fri, 15 Mar 2024 01:49:10 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7138f62a46f5379d04e6d7b6dd53f20a8ccf630319793ee8b3fbb362f19d7c7b`  
		Last Modified: Fri, 15 Mar 2024 01:49:11 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372fe7d000b62397c9567efad26dc3ac272889c7b4eaf76664e9b5395931325`  
		Last Modified: Fri, 15 Mar 2024 01:49:11 GMT  
		Size: 6.4 KB (6408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c629c2e51dca5dc05f91dc81299ef12e9203929f2ff5e247ddf116068b369`  
		Last Modified: Fri, 15 Mar 2024 01:49:12 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:651eff398cf6517c33eea20b218c7e961476276231a5f9657455548758824fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9099847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d5917059e612384d5b72a8963858a54f23a97ce7513ddc1a2a98e210c645af`

```dockerfile
```

-	Layers:
	-	`sha256:e709929169b219b41f835036673d27f167f98e586bccd5788da87a8160864e8e`  
		Last Modified: Fri, 15 Mar 2024 01:49:10 GMT  
		Size: 9.1 MB (9056848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70fdb68ceb0215fe5fccca39f7547c80cd0094a2f0d34ecb67c941a84416a97a`  
		Last Modified: Fri, 15 Mar 2024 01:49:10 GMT  
		Size: 43.0 KB (42999 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:e2f725a531c22a5aa5ffd8d44580ca5a05c80bcbcf4c70a0a0f1b707da50be73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589425370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee89e20eb6f5ff70b53e5b071810dab006989ac6158ae3d7523e8fffe7e09e72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Feb 2024 13:14:55 GMT
ARG RELEASE
# Mon, 26 Feb 2024 13:14:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 26 Feb 2024 13:14:55 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 13:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Feb 2024 13:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Feb 2024 13:14:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 26 Feb 2024 13:14:55 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 26 Feb 2024 13:14:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 26 Feb 2024 13:14:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Feb 2024 13:14:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 26 Feb 2024 13:14:55 GMT
WORKDIR /usr/local/tomcat
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 26 Feb 2024 13:14:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 26 Feb 2024 13:14:55 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_MAJOR=9
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_VERSION=9.0.87
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Mon, 26 Feb 2024 13:14:55 GMT
COPY dir:a438b3922681c6646cb859c6691b163ee551beeceefb652b5380a78c74ba3266 in /usr/local/tomcat 
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 26 Feb 2024 13:14:55 GMT
EXPOSE 8080
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT []
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["catalina.sh" "run"]
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 26 Feb 2024 13:14:55 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_VERSION=16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=e236fc101710a0bfefed2328cc66652e265f21ab40dd30e6b7ce52300da744d5
# Mon, 26 Feb 2024 13:14:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Mon, 26 Feb 2024 13:14:55 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d0bd9f41adcd95029b57f6f8cd737a7f7d062a793bf0806caf980bca1af9c1`  
		Last Modified: Wed, 06 Mar 2024 11:41:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e281f727be7fd28fba4819ffdd9ce87f32b51125b9ec925007964e5de10120`  
		Last Modified: Fri, 15 Mar 2024 01:03:45 GMT  
		Size: 12.4 MB (12428440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eac2aa3387dedf25ad21372bea13d10b6f0a6fed373df59d31ad8f5b09de7e5`  
		Last Modified: Fri, 15 Mar 2024 01:03:44 GMT  
		Size: 457.3 KB (457321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684ab03dff227b5ec8e230cdb2d0fd458f091d52e3d8ee4b703fba7694aa2187`  
		Last Modified: Fri, 15 Mar 2024 01:03:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555f2f2efb411e6fb4cdc817013317dd9a304f3b366e6759cf86919293dffa22`  
		Last Modified: Fri, 15 Mar 2024 01:55:48 GMT  
		Size: 173.4 MB (173388300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ba967c5130211c007fa344d7fd198e690a3531033260a6120aa2ecc42e3420`  
		Last Modified: Fri, 15 Mar 2024 01:55:52 GMT  
		Size: 306.9 MB (306883025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde818be4b95ccdb61136c8a1c50d6ff45f0f26cb6582214d53259ad8038fca6`  
		Last Modified: Fri, 15 Mar 2024 01:55:46 GMT  
		Size: 2.4 MB (2356948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685efd44c279a54dc432df4d2bf520fd390afc45f481a3d80c7d9cccb6abd563`  
		Last Modified: Fri, 15 Mar 2024 01:55:45 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fab57f8d72549c86ff2a37772da2109456cf4d14278e2b4f1190fc9c7578193`  
		Last Modified: Fri, 15 Mar 2024 01:55:47 GMT  
		Size: 2.4 KB (2374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93fb4770bee910455c4fea45f4707ef0eaf4ad2508c2b2208ed8ab3e559644d`  
		Last Modified: Fri, 15 Mar 2024 01:55:47 GMT  
		Size: 6.4 KB (6409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2d826746e84e38c8b5800490687f63a522017aa115ec375ed4e17332ff0592`  
		Last Modified: Fri, 15 Mar 2024 01:55:48 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:bc592053dc0128b230108de2184f329fd523d863922d1d93b1dbefc1fed56de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9196309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa3ba9c0d9e0f348f44fbc277a5eaaaaa57650cab8bfa53b9a1a8d9fff2911f`

```dockerfile
```

-	Layers:
	-	`sha256:2775863fb00f4d8e22281d98c1da79f6819c12706b3ffba39d686e4e80e903f4`  
		Last Modified: Fri, 15 Mar 2024 01:55:45 GMT  
		Size: 9.2 MB (9153286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fde81538bff61de4b2deff68e961dd9a412cec58eb3b5e2bbd7ed60d9b6a9ab6`  
		Last Modified: Fri, 15 Mar 2024 01:55:44 GMT  
		Size: 43.0 KB (43023 bytes)  
		MIME: application/vnd.in-toto+json
