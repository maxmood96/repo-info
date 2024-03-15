## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:00ad41e83cea5028fac585ecb75ec1620509c40a5a5ccbfe980e9b17e386318a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:41559d75c223e763e064532a4009cc5794f3bf20e3d7455318fa8ccbae2d78c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.3 MB (595267229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ba4c6b6a8818a694de2d2b95548dc33d98ef9123ad61817e9ce5751ed3a3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:04:59 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 06:05:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 06:05:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 06:05:33 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:05:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:44:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Mar 2024 14:44:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:44:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Mar 2024 14:44:04 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Mar 2024 14:44:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 14:44:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 14:46:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 06 Mar 2024 14:46:31 GMT
ENV TOMCAT_MAJOR=9
# Fri, 08 Mar 2024 08:40:14 GMT
ENV TOMCAT_VERSION=9.0.87
# Fri, 08 Mar 2024 08:40:14 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Fri, 08 Mar 2024 08:40:14 GMT
COPY dir:40d6dbdce612cc991adb2ee5ce85320942841bbd0b1682a73533c868a43a5fcd in /usr/local/tomcat 
# Fri, 08 Mar 2024 08:40:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 08:40:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 08 Mar 2024 08:40:14 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 08:40:14 GMT
ENTRYPOINT []
# Fri, 08 Mar 2024 08:40:14 GMT
CMD ["catalina.sh" "run"]
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 08 Mar 2024 08:40:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_VERSION=15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=7333e4459754a78b655ed6bdf7633229a750dbe9e92f7dd46fa217f4cf817669
# Fri, 08 Mar 2024 08:40:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_VERSION=42.7.2
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_SHA256=0c244ac7d02cf89d8e29852eace6595d75bc4d78581b85b2768460081646a57b
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.2
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.2.jar
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.2.jar
# Fri, 08 Mar 2024 08:40:14 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Mar 2024 08:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 08:40:14 GMT
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
	-	`sha256:82ea8a9c87c8196d85ab8a4343e461ace37b26b163a68a6706201ccfd4129714`  
		Last Modified: Fri, 15 Mar 2024 01:49:15 GMT  
		Size: 179.3 MB (179291466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60c494daf5571cc9ba615069e2414995250190ac4d275a726396b29be0fb8dd`  
		Last Modified: Fri, 15 Mar 2024 01:49:18 GMT  
		Size: 307.0 MB (306998723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ce5d268df4d5e776aba009ab8c04e27d28b4d0a121a58195842b745aad1eb0`  
		Last Modified: Fri, 15 Mar 2024 01:49:11 GMT  
		Size: 1.0 MB (1011774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbadb7c31512a73b0667e76ba839168f3ad77af3c7161f6cdac67a5966b37cb0`  
		Last Modified: Fri, 15 Mar 2024 01:49:11 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34853bae0b306307a7570b412a19aca2259c8ad8ed8f028f8f37ee4cd9881ae2`  
		Last Modified: Fri, 15 Mar 2024 01:49:12 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8940a4c4563a21f7762017a3279d0e87d59124eb7c09d0dafcb625d837cdfc37`  
		Last Modified: Fri, 15 Mar 2024 01:49:12 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28a699ac6ed87984987c0ed416b4e34a4b0d1a1dfc2e8b0195f85630b15c5cc`  
		Last Modified: Fri, 15 Mar 2024 01:49:13 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:311344a9874ff71313044ef9a9e5730ce09f079e86d3c0fea0bd58d11eeeede9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59e79843739b67320cd0d5c23f279c0ab21e8e1203ab78c6b6653047b847e97`

```dockerfile
```

-	Layers:
	-	`sha256:efa654630d39b6fc5f46ce71659c689e5ee167ae03703d45f2e0fae270697253`  
		Last Modified: Fri, 15 Mar 2024 01:49:11 GMT  
		Size: 9.1 MB (9066319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:738a59a225cd401811912db8fa7e55571e83c1693ba1869814a5174839e51820`  
		Last Modified: Fri, 15 Mar 2024 01:49:11 GMT  
		Size: 41.5 KB (41473 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cd0b4e951806483979597ccc741ad21ea05e5774cf3adbfd6c0c214d8c267d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.1 MB (589137578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aded3a9f71dbf188c5d963cb2af664cce338ddfdfb0ccf7da1af8a7ed2cb1788`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:04:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:04:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:04:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 11:26:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Mar 2024 11:26:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 11:26:10 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Mar 2024 11:26:10 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Mar 2024 11:26:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 11:26:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 11:28:09 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 06 Mar 2024 11:28:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 08 Mar 2024 08:40:14 GMT
ENV TOMCAT_VERSION=9.0.87
# Fri, 08 Mar 2024 08:40:14 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Fri, 08 Mar 2024 08:40:14 GMT
COPY dir:a438b3922681c6646cb859c6691b163ee551beeceefb652b5380a78c74ba3266 in /usr/local/tomcat 
# Fri, 08 Mar 2024 08:40:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 08:40:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 08 Mar 2024 08:40:14 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 08:40:14 GMT
ENTRYPOINT []
# Fri, 08 Mar 2024 08:40:14 GMT
CMD ["catalina.sh" "run"]
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 08 Mar 2024 08:40:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_VERSION=15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=7333e4459754a78b655ed6bdf7633229a750dbe9e92f7dd46fa217f4cf817669
# Fri, 08 Mar 2024 08:40:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_VERSION=42.7.2
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_SHA256=0c244ac7d02cf89d8e29852eace6595d75bc4d78581b85b2768460081646a57b
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.2
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.2.jar
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.2.jar
# Fri, 08 Mar 2024 08:40:14 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Mar 2024 08:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 08:40:14 GMT
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
	-	`sha256:fa774a46917965174cd3aee75b24bd75d50bbb00d6c81ec17114bd8b0e27b527`  
		Last Modified: Fri, 15 Mar 2024 01:57:51 GMT  
		Size: 174.3 MB (174329932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6c540cfba58f6f1cc47b11231a5bb9b38dff38be9e1e9622b9c1a514eec83b`  
		Last Modified: Fri, 15 Mar 2024 02:01:42 GMT  
		Size: 307.0 MB (306998741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5273197581bcdab21ab133c687effb078ef46023b6efcabbf71e3fe137352fca`  
		Last Modified: Fri, 15 Mar 2024 02:01:35 GMT  
		Size: 1.0 MB (1011777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0729ab6f3bc4cba6a467bb994df8679cd4794453059eae09e82fa2e8f4d52cf4`  
		Last Modified: Fri, 15 Mar 2024 02:01:35 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3ce61c1f9e8b78ea4f6fcbc8a176823499b86def6d1bf21a46f77181f5255f`  
		Last Modified: Fri, 15 Mar 2024 02:01:35 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa86d1cf99908890f8e29b5831b754beea811363e77f3efd64b20d6c9ec016f3`  
		Last Modified: Fri, 15 Mar 2024 02:01:36 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1dc19292e0ae57750b5e53d93e2aff1f7da7258bd3388afe46a53783336337`  
		Last Modified: Fri, 15 Mar 2024 02:01:36 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:63b3a4d71434514e4f4a5ab018093c25c0d4135807e3b7db817f3776894e034a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9202765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6431b9cc262e7c94cb1dacfc486a293b2ebc0ecc6d45e73a1309b610ded81743`

```dockerfile
```

-	Layers:
	-	`sha256:ea863d25d9275d7e9b373b291d902c9692bb991aead17be3f6b128c35f1303a7`  
		Last Modified: Fri, 15 Mar 2024 02:01:35 GMT  
		Size: 9.2 MB (9162745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63de074d6c7a60dcc7874f84d4a9369ca48a9f42c0f63cc217840331dc7ef3f7`  
		Last Modified: Fri, 15 Mar 2024 02:01:34 GMT  
		Size: 40.0 KB (40020 bytes)  
		MIME: application/vnd.in-toto+json
