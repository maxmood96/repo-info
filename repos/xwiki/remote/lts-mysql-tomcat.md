## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:263a7d239ab76a2025eaabaecf28027dca7a9e11b98bd54867edfa4dd4bac7ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:e5bdf6c98c1631d138a17d69a2f14c700ad5db7ad131c0f63b0c9a7882cb361a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.6 MB (595643285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778f33b72468a75f23e67666770673639dffafd5709381589e1d8835957bdbbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 09 Feb 2024 16:20:44 GMT
ARG RELEASE
# Fri, 09 Feb 2024 16:20:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Feb 2024 16:20:44 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Fri, 09 Feb 2024 16:20:44 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 16:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Feb 2024 16:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 16:20:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 16:20:44 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 09 Feb 2024 16:20:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 09 Feb 2024 16:20:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 09 Feb 2024 16:20:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 16:20:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 09 Feb 2024 16:20:44 GMT
WORKDIR /usr/local/tomcat
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 09 Feb 2024 16:20:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 09 Feb 2024 16:20:44 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_MAJOR=9
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_VERSION=9.0.86
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Fri, 09 Feb 2024 16:20:44 GMT
COPY dir:a1b18cd4173fc89867b3684c0bcb6ed5fd2f800394449b55a0ac4e5f96c33c28 in /usr/local/tomcat 
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 09 Feb 2024 16:20:44 GMT
EXPOSE 8080
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT []
# Fri, 09 Feb 2024 16:20:44 GMT
CMD ["catalina.sh" "run"]
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 09 Feb 2024 16:20:44 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_VERSION=15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=1491cbfd91d8fe7362c65d01ade6ce36ce7a8adfa4b99e4f339783771d8ab675
# Fri, 09 Feb 2024 16:20:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Fri, 09 Feb 2024 16:20:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
VOLUME [/usr/local/xwiki]
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 16:20:44 GMT
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
	-	`sha256:7e5f7b6e8ca72c71914be68652c1d9d21fe4d11d3258c55cbfbd7f43e6427a55`  
		Last Modified: Wed, 06 Mar 2024 15:06:00 GMT  
		Size: 12.4 MB (12411761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73969ab971ee89d66abcc9270b522fac62871788fcc65712f84c2ef0c7962f0`  
		Last Modified: Wed, 06 Mar 2024 15:05:59 GMT  
		Size: 458.6 KB (458590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1831643cd49257da268e364edf6c6b53b8fe8ced3e3095325777f16866823d8`  
		Last Modified: Wed, 06 Mar 2024 15:05:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5454ebcca639593d54a6dca9fa1177708be6ffe1669ed221e62b1e6156ec8bfb`  
		Last Modified: Wed, 06 Mar 2024 15:49:34 GMT  
		Size: 178.4 MB (178350108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc850f0effc21b3422d3179b6e3af39b7ba4991c538a803184ff4b3ae5b05c9e`  
		Last Modified: Wed, 06 Mar 2024 15:49:35 GMT  
		Size: 307.0 MB (306981183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06d55acbdaa018dbd6fb6aa657360129a878807c6a2b51d94c2f533d0cfb505`  
		Last Modified: Wed, 06 Mar 2024 15:49:31 GMT  
		Size: 2.4 MB (2356954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d6b74db3c5745332d8baed30cdafc45b99bf037ccabd39a983c49849b7e96d`  
		Last Modified: Wed, 06 Mar 2024 15:49:32 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1266a2b12d7bf3ef6a0d887ab026553f8cd22276827374d7ca343d3ea68af2`  
		Last Modified: Wed, 06 Mar 2024 15:49:32 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e16477364869bbc212b3fca39344c6d46deb7eeb851a7e7691e02c2d7287053`  
		Last Modified: Wed, 06 Mar 2024 15:49:32 GMT  
		Size: 6.4 KB (6417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4845800f353f6b8ff5178c10b837a19a3cb46242454042d34dfcf162efac5e3d`  
		Last Modified: Wed, 06 Mar 2024 15:49:33 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:69450a2e48c5a08ef3aafad6f5dc7bbf0a1a68c1e9ad8be9a79b34a6401d9b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9100571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c18a2df56f5486db62934effb2606d272b66ce295517e8813e6283e5d2dce9`

```dockerfile
```

-	Layers:
	-	`sha256:d031e5675e860bc993e02bf8d89ff6bd199e7b7df8dc41976960c8b033f2cc95`  
		Last Modified: Wed, 06 Mar 2024 15:49:32 GMT  
		Size: 9.1 MB (9058180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9900c37c437497b732dc561faa77b263b83a9a855e8e93a7ccde1857dcc72a35`  
		Last Modified: Wed, 06 Mar 2024 15:49:31 GMT  
		Size: 42.4 KB (42391 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:06ad680b4f9865181cd97c66dfc3ea851da01ad312882cfd7f94cb73270accfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589513881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3146172851c4ef367c5a62394fe3010ae57fc8d5f556b92df8ae0966cd7e7897`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 09 Feb 2024 16:20:44 GMT
ARG RELEASE
# Fri, 09 Feb 2024 16:20:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Feb 2024 16:20:44 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Fri, 09 Feb 2024 16:20:44 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 16:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Feb 2024 16:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 16:20:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 16:20:44 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 09 Feb 2024 16:20:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 09 Feb 2024 16:20:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 09 Feb 2024 16:20:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 16:20:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 09 Feb 2024 16:20:44 GMT
WORKDIR /usr/local/tomcat
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 09 Feb 2024 16:20:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 09 Feb 2024 16:20:44 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_MAJOR=9
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_VERSION=9.0.86
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Fri, 09 Feb 2024 16:20:44 GMT
COPY dir:52aed3e3fb48dd428e971cb85f8f92f0846f944a70308bc72289f696b56b8f42 in /usr/local/tomcat 
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 09 Feb 2024 16:20:44 GMT
EXPOSE 8080
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT []
# Fri, 09 Feb 2024 16:20:44 GMT
CMD ["catalina.sh" "run"]
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 09 Feb 2024 16:20:44 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_VERSION=15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=1491cbfd91d8fe7362c65d01ade6ce36ce7a8adfa4b99e4f339783771d8ab675
# Fri, 09 Feb 2024 16:20:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Fri, 09 Feb 2024 16:20:44 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
VOLUME [/usr/local/xwiki]
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 16:20:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bac6b544c281c39df6cde20776732e9b89dbfbbbb49870c60c9af5ef1df471`  
		Last Modified: Fri, 16 Feb 2024 04:55:46 GMT  
		Size: 18.9 MB (18860590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244992bb9e51f456f3e5c927182054789a275d47eba65099182705a8e1952dc2`  
		Last Modified: Fri, 16 Feb 2024 04:56:12 GMT  
		Size: 46.6 MB (46639325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e543faa97f71ea4edea5a6153e1b82e4e9143354356435ca0a085c427b9b07e`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b734e973751dd4636bc278f0ef5ee31fc8e10cc65a07ebd5ef57aa728870187`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834bcd95e101783ee58afe3b6ea7c1050d27b18b749f6b70e0bcbce490b2298e`  
		Last Modified: Fri, 16 Feb 2024 07:41:13 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08260b115c6a7540dd9078e15a0b3abe0c1e3d241dd8efd8ff6fe43840322f9`  
		Last Modified: Wed, 21 Feb 2024 02:43:35 GMT  
		Size: 12.4 MB (12418084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df99f020bb771bfb916b40a084c375b7b9d6aba87791b0679dd27408096b7e7`  
		Last Modified: Wed, 21 Feb 2024 02:43:34 GMT  
		Size: 457.1 KB (457128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41fe064b4c9bb6147a50153ae6ce913ccec8ecefc141098f8cfa404dccfe968`  
		Last Modified: Wed, 21 Feb 2024 02:43:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f942220408c5601f78916ffb6c0b523503ae28b04b2f8ffa2416021fb769ec`  
		Last Modified: Wed, 21 Feb 2024 05:54:58 GMT  
		Size: 173.4 MB (173386551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3bba94a1776c21cc8d3e5df0f4e9e11430dc99b9eec437284a8fca9a3fd0ee`  
		Last Modified: Wed, 21 Feb 2024 05:59:14 GMT  
		Size: 307.0 MB (306981145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f2c4263228713e00e4fe66929ab5aee56aa14f9d32a030abc871ecd2307e17`  
		Last Modified: Wed, 21 Feb 2024 05:59:07 GMT  
		Size: 2.4 MB (2356949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2fc02669add9167e6c1868266cf72da615306046fd30191f558d791f751cf8`  
		Last Modified: Wed, 21 Feb 2024 05:59:07 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d2b5a316579e3a103e39409b176fe4ba4458baf797413de468a56d58d88767`  
		Last Modified: Wed, 21 Feb 2024 05:59:07 GMT  
		Size: 2.4 KB (2366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdce494ad80c573ae212fee23a119f3aafcf44be706e33231c5b3dda2141a0e`  
		Last Modified: Wed, 21 Feb 2024 05:59:08 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fe65d141d1731d1bda830e5c4231dd0fa2ff705539ae7a54615ccfc023a4da`  
		Last Modified: Wed, 21 Feb 2024 05:59:08 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:fbbb0725819f09a3e37cad184da476c8a9c7414e554e9a70fad32cc7d54b3679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9195560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51af57643699bd4f8784ec8e953d68f9884143e99a400b9eb5b9cd7bd9ebad68`

```dockerfile
```

-	Layers:
	-	`sha256:e764ababd6885befb479c0cf158c6185e40dddee0b85dd53acbe575733f3be4d`  
		Last Modified: Wed, 21 Feb 2024 05:59:08 GMT  
		Size: 9.2 MB (9154614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42ea8b2dc350bc77552377cd331e5ea7f375be8fd805cddec5b4c35c205bd14`  
		Last Modified: Wed, 21 Feb 2024 05:59:07 GMT  
		Size: 40.9 KB (40946 bytes)  
		MIME: application/vnd.in-toto+json
