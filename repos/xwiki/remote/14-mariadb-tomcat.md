## `xwiki:14-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:7861f5dec8e413a91655154c414e15797ab87278193d17e62bb45abca22f9688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:14-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:205628033fdff87224f61039640e5877979611b7468762fc73dcd9d274f63311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.0 MB (596036095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b954df6a655b16e4d86f93ab96478b866ed131f8f8420d8c32730b20af439bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 05 Dec 2023 14:34:12 GMT
ARG RELEASE
# Tue, 05 Dec 2023 14:34:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Dec 2023 14:34:12 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["/bin/bash"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 05 Dec 2023 14:34:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 05 Dec 2023 14:34:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_MAJOR=9
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_VERSION=9.0.85
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Tue, 05 Dec 2023 14:34:12 GMT
COPY dir:f4f1ec0066f8e22dbe18e524bdaa66d22964d314d16b2d4878c80d7fb4e8eb25 in /usr/local/tomcat 
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 05 Dec 2023 14:34:12 GMT
EXPOSE 8080
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT []
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["catalina.sh" "run"]
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 05 Dec 2023 14:34:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_VERSION=14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_DOWNLOAD_SHA256=c418601676d61893ccb9e066b1f2bcce56717b49e5c2456656b6960db6bd6e4c
# Tue, 05 Dec 2023 14:34:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_VERSION=3.3.0
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_SHA256=8262c79463e6b0932f60f55b61ca14087fdcafb117caa87259cd3a64409cd4fa
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.0
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 14:34:12 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec70d9e863c2b918442abf26eb84b0afbc4a2c5dda1c34857c51955e26a803c3`  
		Last Modified: Wed, 17 Jan 2024 07:20:58 GMT  
		Size: 47.1 MB (47149289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680d0df58130ac2dc6ee238ad0275c9652892eda90a334fd3ce02eedf7147963`  
		Last Modified: Wed, 17 Jan 2024 07:20:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73eedc84985754d22cc59527bee6b3fc0a39558017abcf0fe7ae531123dc84e`  
		Last Modified: Wed, 17 Jan 2024 07:20:52 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d1e1efd368e72c389dbb275ecfcbab50b1947efee25f89197359ea37a0c84`  
		Last Modified: Wed, 17 Jan 2024 11:15:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde25073223ef7971200346ba07792a2cbc6d8eb5aa846f4305d6184d270ac39`  
		Last Modified: Wed, 17 Jan 2024 11:22:00 GMT  
		Size: 12.4 MB (12404679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cafa28ad9d6c49c386348766658cff0214270deb1a170d7247496e756df683`  
		Last Modified: Wed, 17 Jan 2024 11:22:00 GMT  
		Size: 458.5 KB (458531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf3288bc25ea454de10d0b24c9bd7bcd4adfe139a10bd0b647800ee3293228`  
		Last Modified: Wed, 17 Jan 2024 11:21:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b623abd2a2036209ca3c4cd03debc66223d36516ee20e9481294114cc4d6285c`  
		Last Modified: Wed, 17 Jan 2024 22:44:47 GMT  
		Size: 178.3 MB (178348656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf12bd953786b058a27aa11a27cf3fb21f64817fcf394fb31357089dfdc4ed0`  
		Last Modified: Wed, 17 Jan 2024 22:44:51 GMT  
		Size: 309.2 MB (309150283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25efacd84701ff928d9d19967e89f91274e68b00fdae3e094983e6604176e883`  
		Last Modified: Wed, 17 Jan 2024 22:44:43 GMT  
		Size: 606.0 KB (605976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bf235f5a1afb26b49bca9e35604f65090d70e013f2be2bb303715e5fac706e`  
		Last Modified: Wed, 17 Jan 2024 22:44:43 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462e21bdb2b73c2c168c1e4ba43a86633dfbabcae8008b83bb631eeab13ff8f7`  
		Last Modified: Wed, 17 Jan 2024 22:44:44 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6513c898f826e506cf11aa9ff1e467fa6617847fcbbc655b4125d56b946d1a17`  
		Last Modified: Wed, 17 Jan 2024 22:44:44 GMT  
		Size: 6.1 KB (6131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3f1213a52698aabe412de588ace9993e42234956264536073105da5bd856dd`  
		Last Modified: Wed, 17 Jan 2024 22:44:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b7dc5e7cc21f4f03078cffae2c846c670db9564df0eb8006a9c7b2eaa81e7fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8063186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0718f1550df1931cc1dff382fb078baa9355b17e4115694e751d01095aaaea2b`

```dockerfile
```

-	Layers:
	-	`sha256:46e62ac8d8568446d730626433311bdf13a4e5eabea952797621bb3265400806`  
		Last Modified: Wed, 17 Jan 2024 22:44:44 GMT  
		Size: 8.0 MB (8022498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8144557db5e33a995b4b10a00f5c785afabde313437aaa57ec1416dfd3d1ca51`  
		Last Modified: Wed, 17 Jan 2024 22:44:43 GMT  
		Size: 40.7 KB (40688 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:14-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:477597698b0b1fc26b6691ca029b251658c2eb1abc1187930760d552e7774c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 MB (589909891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41cd31fdee2d1404842d09480c2020d6c59910b767a5df001e311ab04764721`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 05 Dec 2023 14:34:12 GMT
ARG RELEASE
# Tue, 05 Dec 2023 14:34:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Dec 2023 14:34:12 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["/bin/bash"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 05 Dec 2023 14:34:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 05 Dec 2023 14:34:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_MAJOR=9
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_VERSION=9.0.85
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Tue, 05 Dec 2023 14:34:12 GMT
COPY dir:1c285ad99d5400a62c515d0edc8da9bc0491088e5993df30403cdd5d434fbc0a in /usr/local/tomcat 
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 05 Dec 2023 14:34:12 GMT
EXPOSE 8080
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT []
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["catalina.sh" "run"]
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 05 Dec 2023 14:34:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_VERSION=14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_DOWNLOAD_SHA256=c418601676d61893ccb9e066b1f2bcce56717b49e5c2456656b6960db6bd6e4c
# Tue, 05 Dec 2023 14:34:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_VERSION=3.3.0
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_SHA256=8262c79463e6b0932f60f55b61ca14087fdcafb117caa87259cd3a64409cd4fa
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.0
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 14:34:12 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 14:34:12 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40ddacc22778a98794779fd2342df132ad4c2fb4cbfc8863316d31fd435b197`  
		Last Modified: Wed, 17 Jan 2024 07:02:40 GMT  
		Size: 46.6 MB (46624031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa70867b319793d597ac109e4ab08a1640a03419c64b02fc2a0f83d3fab963`  
		Last Modified: Wed, 17 Jan 2024 07:02:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb574f7d99aeb3b3f52602da29bf978d23b304f4233a2ea5587d6ae88cbd66`  
		Last Modified: Wed, 17 Jan 2024 07:02:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676d321c3a16eda4a2f342361460b3290f1270e6f89a4d3dea4f3e1b6b504c2a`  
		Last Modified: Wed, 17 Jan 2024 14:36:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35964d9c82059bc828da4495b32b7a5b3a228340ebeb409b7774dd029e4001f9`  
		Last Modified: Wed, 17 Jan 2024 14:43:50 GMT  
		Size: 12.4 MB (12412598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5dd66eedef4831ca2d1805f0a4e47f36bf9bf1fd03bc06d2ff39484a65e7a9`  
		Last Modified: Wed, 17 Jan 2024 14:43:49 GMT  
		Size: 457.3 KB (457266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4081678f3e603cdbf87adcc472987711822b96a55a07e07e83d82695b4ccd`  
		Last Modified: Wed, 17 Jan 2024 14:43:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e771a6062b68520e7e7ae513dddd2b646de56809a72b94c54ebcf82514423cf`  
		Last Modified: Thu, 18 Jan 2024 11:32:05 GMT  
		Size: 173.4 MB (173386603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a389292860808ffb36cad898c6bdc876df525fec5402c5d7a57c5e289e1712`  
		Last Modified: Thu, 18 Jan 2024 11:36:34 GMT  
		Size: 309.2 MB (309150306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199ebf7623be507a110b980797131a9f267fdb2505aadce3dd9680b4948717f5`  
		Last Modified: Thu, 18 Jan 2024 11:38:44 GMT  
		Size: 606.0 KB (605974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ff08912d065465b05d3e26128f9a34061997cda5086db203076fadc929e547`  
		Last Modified: Thu, 18 Jan 2024 11:38:44 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475810dc9c88bde598683da6f23757eaf947c569bad0b3ab3c6634328a774d32`  
		Last Modified: Thu, 18 Jan 2024 11:38:44 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ea2610f790eaeb3e4e1b19f816c1e9b661862bd48e3e61045c56b7befe5d1`  
		Last Modified: Thu, 18 Jan 2024 11:38:45 GMT  
		Size: 6.1 KB (6130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4ca060911d76d120f36ba388dc6da1d86771158f6a1044a0c50c770f6af6c5`  
		Last Modified: Thu, 18 Jan 2024 11:38:45 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b2c14cc3be0a288e7126f51e3e1a8869c51efde8b2379eb07d90de29999fcc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8145749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9adb33832e91e0205406f27acf424478c45bbe91de1d272166ab7e6c1412008a`

```dockerfile
```

-	Layers:
	-	`sha256:ef77c9d2bd0e5b2b0d452c7b45f5ee9a31dd674dd2c3fbfa01afe5c158b498aa`  
		Last Modified: Thu, 18 Jan 2024 11:38:45 GMT  
		Size: 8.1 MB (8106518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8aa8081472e39ef9eea6de0378d1f5344432882092f83d83131a12776bc333`  
		Last Modified: Thu, 18 Jan 2024 11:38:44 GMT  
		Size: 39.2 KB (39231 bytes)  
		MIME: application/vnd.in-toto+json
