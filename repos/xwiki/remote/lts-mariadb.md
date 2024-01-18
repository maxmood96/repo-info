## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:224d8e661d3f9688740ad6d21d924cbb041b206e0e2439ab1e954be91fb74206
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:5f960134b75e26f196bd02468153109368a348b53c0d5005c11cb0d95b3b05d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.9 MB (593862632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302bc2ce8eab2d9211b262a0d2fdccd851cd4b3d077045f798650aec13a2b876`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:16:34 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 17 Jan 2024 07:17:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 07:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 07:17:07 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 07:17:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 10:38:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 17 Jan 2024 10:38:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 10:38:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 17 Jan 2024 10:38:26 GMT
WORKDIR /usr/local/tomcat
# Wed, 17 Jan 2024 10:38:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 10:38:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 10:41:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 17 Jan 2024 10:41:00 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Jan 2024 10:41:00 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 17 Jan 2024 10:41:01 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 17 Jan 2024 10:41:01 GMT
COPY dir:f4f1ec0066f8e22dbe18e524bdaa66d22964d314d16b2d4878c80d7fb4e8eb25 in /usr/local/tomcat 
# Wed, 17 Jan 2024 10:41:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 10:41:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 17 Jan 2024 10:41:07 GMT
EXPOSE 8080
# Wed, 17 Jan 2024 10:41:07 GMT
ENTRYPOINT []
# Wed, 17 Jan 2024 10:41:08 GMT
CMD ["catalina.sh" "run"]
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 17 Jan 2024 13:37:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_VERSION=15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=3775334377ae7fb8bcf6a21e6eb099a8cfbea43044dc0716c01cb3b5117988a2
# Wed, 17 Jan 2024 13:37:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Wed, 17 Jan 2024 13:37:13 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
VOLUME [/usr/local/xwiki]
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
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
	-	`sha256:076715b02204bd8d178c45ba9789fa1b127e52a5ca1a310c07037e1678c05151`  
		Last Modified: Wed, 17 Jan 2024 22:44:46 GMT  
		Size: 178.3 MB (178348979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543358904e2594e8818e5c9142afb54d559829fe2ea1b4ca31c2b8707f1ee0f0`  
		Last Modified: Wed, 17 Jan 2024 22:44:51 GMT  
		Size: 307.0 MB (306967053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5b4b20da0ea9fed2da49efa3f776f80d2aa58d6c634e40acf4613577a969d4`  
		Last Modified: Wed, 17 Jan 2024 22:44:43 GMT  
		Size: 615.1 KB (615139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6fce39db66ba3230e8789024b6179c8103ad5ec69a5450afeb1ce573cfd27b`  
		Last Modified: Wed, 17 Jan 2024 22:44:43 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bad50e9a4079d8c4c3fd14f22ea79b79fde1ee8bf1d09b343b400f37ad5394`  
		Last Modified: Wed, 17 Jan 2024 22:44:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151f7c9edc2c16f90f975d457b4cbfa99914cb4d04d331495136c550b05f036`  
		Last Modified: Wed, 17 Jan 2024 22:44:44 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5724b5f900fcf832b05c260b4f8cb1f8254033241c5e24b7fb60972429a4095`  
		Last Modified: Wed, 17 Jan 2024 22:44:45 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:bb6dca07b180ef71b5dd6f402a361d0991b595902a6e2818f576084691a10390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8080079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfccd4ad5ddbb7d0bb93bad1c56af7413434973007f25abb3dbcb615bb0cb2d`

```dockerfile
```

-	Layers:
	-	`sha256:0aaf2e26f1c67e445b9e46310392cdb27947d09a3c953670348a8f1448f7f3f9`  
		Last Modified: Wed, 17 Jan 2024 22:44:43 GMT  
		Size: 8.0 MB (8037823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89cc49b213ed49a21ab35a2149798a2b4a9c35a895e01085aaa8a934bd44109f`  
		Last Modified: Wed, 17 Jan 2024 22:44:43 GMT  
		Size: 42.3 KB (42256 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:036c438a7d9fbb1b9b85b701bcae171503cc4587bc7ca693a8bc581e8c974f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.7 MB (587736336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc79347f5b1835ab0a8ddc67cc5f88f60a5660cc54d9b80a67140c905b3b8b52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 14:58:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 14:58:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 14:58:16 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 14:58:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 14:58:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 15:00:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 16 Dec 2023 15:00:13 GMT
ENV TOMCAT_MAJOR=9
# Wed, 03 Jan 2024 14:50:08 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 03 Jan 2024 14:50:08 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 03 Jan 2024 14:50:08 GMT
COPY dir:09ec1a41519e5f472323f13ea118ab3b9fa15443e7cef602383f9cce6831413f in /usr/local/tomcat 
# Wed, 03 Jan 2024 14:50:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 14:50:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Jan 2024 14:50:08 GMT
EXPOSE 8080
# Wed, 03 Jan 2024 14:50:08 GMT
ENTRYPOINT []
# Wed, 03 Jan 2024 14:50:08 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 03 Jan 2024 14:50:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_VERSION=15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=8c1bb157f03b714255305aadc0904d35e87ae38df998dcfb5117de3d395d473c
# Wed, 03 Jan 2024 14:50:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Wed, 03 Jan 2024 14:50:08 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 03 Jan 2024 14:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jan 2024 14:50:08 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fdc1608413c55e6f71ba5c11e8a186c5cdf1ffd462d135094650174976fd36`  
		Last Modified: Sat, 16 Dec 2023 15:13:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b25d4c7eacf3804aea1d5c1bc2fc145721664b617149a1bb7a8d79c0a0e33`  
		Last Modified: Tue, 09 Jan 2024 23:24:33 GMT  
		Size: 12.4 MB (12412590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3365d79ae16022e118700cf407965f3ea009e0d246e4f646c5cb61e4a1f30c`  
		Last Modified: Tue, 09 Jan 2024 23:24:33 GMT  
		Size: 458.4 KB (458439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd48ede90a8f4bce37f6a17e9f84e06a1357544057cd16f43920d92dc540708a`  
		Last Modified: Tue, 09 Jan 2024 23:24:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cbc65b3d7483b733ef1431e94ce6dc8e4653ae2baa53c9d01f1bd66c3a5b76`  
		Last Modified: Wed, 10 Jan 2024 01:08:34 GMT  
		Size: 173.4 MB (173388154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f0ac73e47ce66456cbeb7a7542243bf9ca22b0660c49021c3c7a7c44ac6671`  
		Last Modified: Wed, 10 Jan 2024 01:08:37 GMT  
		Size: 307.0 MB (306966188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d375e4c708fc5a6bbaa3cb61340249b54e191108f898d81b374e20f77d78c`  
		Last Modified: Wed, 10 Jan 2024 01:11:10 GMT  
		Size: 615.1 KB (615143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4215569bc50bc9faf9ff863a0399bf7f0e6b4cb7756ec4b7dc22bb4db17933`  
		Last Modified: Wed, 10 Jan 2024 01:11:10 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13765dc56995fc81723377f224869c03043dc557ca0fdc0b5d3145a4de9a9e`  
		Last Modified: Wed, 10 Jan 2024 01:11:10 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c05a1465ffd38c719ad884a26c628d0903f7d4b7f8aedf9a9427f9d20c2d3f`  
		Last Modified: Wed, 10 Jan 2024 01:11:10 GMT  
		Size: 6.4 KB (6417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5351b1c46fe132bddb22d6bca435a913ef731366b6d3c02ff7e9f7be27e1725b`  
		Last Modified: Wed, 10 Jan 2024 01:11:11 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:4f06ba26c3d96f0275774d74e45c55327f96cc08b2adb7fd2fb9e37da63469eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8162198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2a033a03c3f0ca2fafcf0793346d679325d5608d1274552913221a5a098017`

```dockerfile
```

-	Layers:
	-	`sha256:da4600a1084fd76da15ed5ee59128698fa4a7dd8143b3473ca94868fb16ce17e`  
		Last Modified: Wed, 10 Jan 2024 01:11:10 GMT  
		Size: 8.1 MB (8121389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45645c7af78053ba9cc90c7367d2354a70e9a0bfeb5cb059558f80d28e9cc0bb`  
		Last Modified: Wed, 10 Jan 2024 01:11:09 GMT  
		Size: 40.8 KB (40809 bytes)  
		MIME: application/vnd.in-toto+json
