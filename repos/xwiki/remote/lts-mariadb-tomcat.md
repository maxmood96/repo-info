## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:250d57b1f4279377b2bfcd7392aaaecfbb31c3918f18b9cf0141a3e40f39c339
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7e181ada92e9bcd8dc9669ffb178317f38ff666adf7703d302e9472b2e1baeda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589512042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66fd1d2869eab6e6893ac7e2884641dadf4b50c3ae8cdccb0331e19815f3a53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 May 2024 13:30:04 GMT
ARG RELEASE
# Mon, 27 May 2024 13:30:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 May 2024 13:30:04 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 27 May 2024 13:30:04 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 27 May 2024 13:30:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 May 2024 13:30:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 27 May 2024 13:30:04 GMT
WORKDIR /usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_MAJOR=9
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_VERSION=9.0.89
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Mon, 27 May 2024 13:30:04 GMT
COPY dir:0b3a96ac60d75fdf26c7de1d52191df4fd550034e1462b3aee30307d4473afec in /usr/local/tomcat 
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 27 May 2024 13:30:04 GMT
EXPOSE 8080
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT []
# Mon, 27 May 2024 13:30:04 GMT
CMD ["catalina.sh" "run"]
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 27 May 2024 13:30:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_VERSION=15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=fda9b5b4c1f471dc47e8cf2cb72b7550dbe6d6772887201be94c522a13b6078e
# Mon, 27 May 2024 13:30:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_VERSION=3.3.3
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Mon, 27 May 2024 13:30:04 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 27 May 2024 13:30:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 27 May 2024 13:30:04 GMT
VOLUME [/usr/local/xwiki]
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 May 2024 13:30:04 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee59ca42def8dda96caccd58b671902e65195492ee8e5daa263e1e948033adc3`  
		Last Modified: Wed, 05 Jun 2024 05:01:21 GMT  
		Size: 47.3 MB (47256057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce2282f972ff7152adb0a2c757ddd63cf0c38d489c7d7952d7aa88ab1804bc5`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a9e456ba828f8cfc067a64b3717c10e4c0709fc1f0b95e5a5efd3ee816e643`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf4892f7e4550fc70dba9049d20a75e7eee29216fc7246e9610f72a3bfc77ce`  
		Last Modified: Wed, 05 Jun 2024 08:23:47 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a52c16c9d1baa051c919c53cbd2983dffbeb42c5654bc64c1c0e6459b6bab7`  
		Last Modified: Wed, 05 Jun 2024 08:26:45 GMT  
		Size: 12.4 MB (12436429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada98b1788f7769dac54217993e85011083578a04978203315d894fd2a0b6ce6`  
		Last Modified: Wed, 05 Jun 2024 08:26:44 GMT  
		Size: 456.3 KB (456302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2924b1a39c5ab975ebf002293359197f56ebd98fee88f805581087395bd292c4`  
		Last Modified: Wed, 05 Jun 2024 08:26:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec6cc90f87b8b01a7daf2c2b725d37aad67d982ce81128394e81bbc10e3b927`  
		Last Modified: Wed, 05 Jun 2024 09:07:31 GMT  
		Size: 178.4 MB (178436728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592de513b5b71e8524f7171013ed4239a58fed8eca82073cd0b07dd7160bff70`  
		Last Modified: Wed, 05 Jun 2024 09:07:33 GMT  
		Size: 306.9 MB (306948756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a37fc4edbc2d3e03c141f5be592a48fc6f48bf03ca97c67c11dd7fd78585d5a`  
		Last Modified: Wed, 05 Jun 2024 09:07:28 GMT  
		Size: 620.0 KB (619999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8d4f928feacb437455b9d84b27feff9a4cd9c28d29cf5a7dc6329dbba760c8`  
		Last Modified: Wed, 05 Jun 2024 09:07:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844d450723cd5e0b00e4267634fa1e1038ff21a90a5c4e4d98e88df7a2f39e3d`  
		Last Modified: Wed, 05 Jun 2024 09:07:29 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8c9ae16d3dc67c36dfea228d33e1650bd51ca0c6b54748761aa968f715f31`  
		Last Modified: Wed, 05 Jun 2024 09:07:29 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928d8e8449776552d02aaeb0ce584793160ae650c8c03f97177a9c8b11d2795f`  
		Last Modified: Wed, 05 Jun 2024 09:07:30 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:690cd486b65d708e1b129e0aa32fb0692d4c89f4d241dc9b80913f49a24a942a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03e71279e7177d1bac8b265ce9ac7aeea9b38daeee5bf6224e1316ebac91504`

```dockerfile
```

-	Layers:
	-	`sha256:3c8b6c6050229dd13c86f3f3cfe5e4a5e83fc6c948e170fe53af3794fadf7770`  
		Last Modified: Wed, 05 Jun 2024 09:07:28 GMT  
		Size: 8.9 MB (8892898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f552a245a7d1b2fcd148721071812dd4480c742bff7f39de07e3854907a70e`  
		Last Modified: Wed, 05 Jun 2024 09:07:28 GMT  
		Size: 39.9 KB (39937 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cdf539bfc7ee159180bd46d85fcfd42dca6f3971a13b00d8837b7a78a32feffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.9 MB (581936514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b00ccd1809f87025c258608798542ed702c649e841a3694c6d86f28a6acf4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 May 2024 13:30:04 GMT
ARG RELEASE
# Mon, 27 May 2024 13:30:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 May 2024 13:30:04 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 27 May 2024 13:30:04 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 27 May 2024 13:30:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 May 2024 13:30:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 27 May 2024 13:30:04 GMT
WORKDIR /usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_MAJOR=9
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_VERSION=9.0.89
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Mon, 27 May 2024 13:30:04 GMT
COPY dir:58ad55bab575cab028cf8b426107fdedda2ac4d0f3638bd518c64d50c26f920e in /usr/local/tomcat 
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 27 May 2024 13:30:04 GMT
EXPOSE 8080
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT []
# Mon, 27 May 2024 13:30:04 GMT
CMD ["catalina.sh" "run"]
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 27 May 2024 13:30:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_VERSION=15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=fda9b5b4c1f471dc47e8cf2cb72b7550dbe6d6772887201be94c522a13b6078e
# Mon, 27 May 2024 13:30:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_VERSION=3.3.3
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Mon, 27 May 2024 13:30:04 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Mon, 27 May 2024 13:30:04 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 27 May 2024 13:30:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 27 May 2024 13:30:04 GMT
VOLUME [/usr/local/xwiki]
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 May 2024 13:30:04 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa963c04773e39efb3eb3c080a80fe1bccbf8410a480f24229a7a06fc307c532`  
		Last Modified: Wed, 05 Jun 2024 04:57:44 GMT  
		Size: 46.7 MB (46716398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382cfd76d96df44a0a5e200f1841a3fc8d1bdbfa5fb655a2f2795bc3b4e16ec3`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0792dc21c67221e401d3c4b78ebea1705a045fbcc6461558ac50bfbe911989a`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d9376e25e5ba92936ed244a6a17f40e0e94193fe0dc8f60206086fbde34bd1`  
		Last Modified: Wed, 05 Jun 2024 07:34:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5691ecc99a8f77b5bbea731a32ed78a6cc766bfe44b2e3f4eeab129e2f2daf83`  
		Last Modified: Wed, 05 Jun 2024 07:37:16 GMT  
		Size: 12.4 MB (12444380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1b63586cd37b618e234ed2a73da7b1c927b4c63791efcfdb630d22109cdedb`  
		Last Modified: Wed, 05 Jun 2024 07:37:15 GMT  
		Size: 456.8 KB (456815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da359c1a7d5b25cd7c2be940e7d189a81733ec484209e3da051054b173bde3`  
		Last Modified: Wed, 05 Jun 2024 07:37:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46756eb83dcd276f59cb6351aa3127f42354d456260ce2f53e6fd522884960c1`  
		Last Modified: Wed, 05 Jun 2024 18:22:38 GMT  
		Size: 173.5 MB (173486358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caeca50a2f8e31a3c63607285daeda11adb5fecefa75c7f1d5fc11f60b94b5c3`  
		Last Modified: Wed, 05 Jun 2024 18:26:29 GMT  
		Size: 306.9 MB (306948747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1280e67045e1af271b445342aadffebfe4ce663fe35fc5f19def242446af96`  
		Last Modified: Wed, 05 Jun 2024 18:28:28 GMT  
		Size: 620.0 KB (620001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b562c76b89a0ce568e11509192b8d8e5854fe6cd707f25a0bdf7d5e933ec32`  
		Last Modified: Wed, 05 Jun 2024 18:28:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235208567af2c90216632d492484152bef0e662108c1cc6a5fbdbabe872c5327`  
		Last Modified: Wed, 05 Jun 2024 18:28:28 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaa0bef7a5d4874a56c4c533342ba5a7541b431c9ad88623e0a753f938ef26d`  
		Last Modified: Wed, 05 Jun 2024 18:28:29 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba72ab1a4dfb82dbf2369fd2a4452de1b607e5d5fc648be39ffe8c495d9d1f`  
		Last Modified: Wed, 05 Jun 2024 18:28:29 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:97a82f77b56650e7afb2eba24d201d00c3a0266271fee56797a2d0d18acb541f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8933712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371fb1ef9f48712cb067be4071aec7097b459f14297236a092a08f0478af9cbc`

```dockerfile
```

-	Layers:
	-	`sha256:06d454721698353ba678902608f3b5d26c6d46394ecb436c2cda3da9abce9819`  
		Last Modified: Wed, 05 Jun 2024 18:28:29 GMT  
		Size: 8.9 MB (8893460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2719f7a52b9001be7c874967ae43d850830fd043aeaa9fe090e99d5fcc873be4`  
		Last Modified: Wed, 05 Jun 2024 18:28:28 GMT  
		Size: 40.3 KB (40252 bytes)  
		MIME: application/vnd.in-toto+json
