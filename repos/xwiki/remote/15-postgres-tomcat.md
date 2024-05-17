## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:ad67c362aa336576fdcde0b0b9cd1fd145d2412621b1454f6cf0ae1914baf326
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0b850aa379ab14876f6b7628902c78f484ed1488d8d0f4f75fdc2f3099928453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.9 MB (590851183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8ae0d2757dec8673457893011ad638a7d3160e471ac58041d2a1176137cd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
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
# Thu, 02 May 2024 06:55:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 06:55:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 06:55:15 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 06:55:15 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 06:55:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 06:55:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 06:57:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 06:57:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 May 2024 21:39:27 GMT
ENV TOMCAT_VERSION=9.0.89
# Tue, 07 May 2024 21:39:27 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 07 May 2024 21:39:28 GMT
COPY dir:65d1d1b9512dfd4e1ebebbeb9b29b52484b09ce5380067ed2396b3f6fc00cfa9 in /usr/local/tomcat 
# Tue, 07 May 2024 21:39:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 21:39:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 May 2024 21:39:34 GMT
EXPOSE 8080
# Tue, 07 May 2024 21:39:34 GMT
ENTRYPOINT []
# Tue, 07 May 2024 21:39:35 GMT
CMD ["catalina.sh" "run"]
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 17 May 2024 15:09:58 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 May 2024 15:09:58 GMT
ENV XWIKI_VERSION=15.10.9
# Fri, 17 May 2024 15:09:58 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.9
# Fri, 17 May 2024 15:09:58 GMT
ENV XWIKI_DOWNLOAD_SHA256=279581bd5c733e8f3eeed31a405055987380cb1abb3303de38200d6d4db176b7
# Fri, 17 May 2024 15:09:58 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Fri, 17 May 2024 15:09:58 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 17 May 2024 15:09:58 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 17 May 2024 15:09:58 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 17 May 2024 15:09:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 17 May 2024 15:09:58 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 17 May 2024 15:09:58 GMT
VOLUME [/usr/local/xwiki]
# Fri, 17 May 2024 15:09:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 May 2024 15:09:58 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce394e5c05f6275f1a3d93ef078caadf4c6e88066e708ffa5cea964ded0c3c2`  
		Last Modified: Thu, 02 May 2024 01:15:30 GMT  
		Size: 12.9 MB (12905606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e026920ea2a9fd70b5b270aaa34672572276e0d92b9da71ce0b58a571ade52c5`  
		Last Modified: Thu, 02 May 2024 01:18:52 GMT  
		Size: 47.3 MB (47256136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d0df997d9c75c7ce45795a94101aa9b3c64050bf0b5c2ef92ecb36cfa36cdf`  
		Last Modified: Thu, 02 May 2024 01:18:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c863a9ccf459944a17dfde7fb73751761675f48f9812eff6de4bc2a9aefbb151`  
		Last Modified: Thu, 02 May 2024 01:18:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59f08f43fed42802bbfebcae0720c23a77bbd60a2e8e3716efe5c5cd6deb278`  
		Last Modified: Thu, 02 May 2024 07:06:41 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eb894602a902d45b213e7d1579f36329c60d39e5cec615c79ef038a7d0ec53`  
		Last Modified: Tue, 07 May 2024 21:50:19 GMT  
		Size: 12.4 MB (12436719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571c4bffcb717de1b493692ebb9539a2fcd7fd87393cb2431032dce8fc849299`  
		Last Modified: Tue, 07 May 2024 21:50:18 GMT  
		Size: 456.3 KB (456327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25773639f3fe3ece6167dea898bf49ea0bdf22b04aa055dd319c62dbc6821632`  
		Last Modified: Tue, 07 May 2024 21:50:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0333d0cd7fe18611046483656079b308a4b606243bfd7cfa66b625e9d8f50e5c`  
		Last Modified: Fri, 17 May 2024 18:15:40 GMT  
		Size: 179.4 MB (179376898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd3a7a8bf73b292b99595414f834dbe7c19baafa2376d067bdec3e97a8d2645`  
		Last Modified: Fri, 17 May 2024 18:15:44 GMT  
		Size: 307.0 MB (306954028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916b9f336712590a8609892d2a52c7f22cd00b246221d326491b43bb66cb963d`  
		Last Modified: Fri, 17 May 2024 18:15:36 GMT  
		Size: 1.0 MB (1011977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee187bd33e5c0eaccbd1a107f12f50c8d55abcf73af54561f00ca80fa959f253`  
		Last Modified: Fri, 17 May 2024 18:15:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a84b2cf6704f40e09dd974d27e367733d8e4c61fa44c3bf3bfd728bfec38be5`  
		Last Modified: Fri, 17 May 2024 18:15:37 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70541343ea2d7a5eec881be1079cc1da65c016e17932f3fb92432c1904b2ed03`  
		Last Modified: Fri, 17 May 2024 18:15:37 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100d84c456f57535f1ab5fb9d57bea7479a49359ec2abfbd8683a58aebe02c87`  
		Last Modified: Fri, 17 May 2024 18:15:38 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:87347913655c03165d7483e25d415fccbffdb76fcd72ed1f2ee282485577d5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8942666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d314abdd5c5351b25178d67faa12ab2d4dea96f4c8d0b956a597a4fecf064f`

```dockerfile
```

-	Layers:
	-	`sha256:536b27ed169f1668594602b96e891c8cc8f0393c2e22c7cc523ab6ccf0bb7183`  
		Last Modified: Fri, 17 May 2024 18:15:36 GMT  
		Size: 8.9 MB (8901189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147493a0e812874c3dd4db80a48ab3dda124bafec7ec392cc4dce52fa76644fa`  
		Last Modified: Fri, 17 May 2024 18:15:35 GMT  
		Size: 41.5 KB (41477 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:71a58f56c5f166cca0be0408e32578f34cccd16def8e07012959c7446a1052bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583270005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae3eb2d5fe722fd5a4eb3d9ff4811c8baaf7fc1b6c8b593ebafece721fccdc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
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
# Thu, 02 May 2024 07:35:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 07:35:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 07:35:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 07:35:19 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 07:35:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:35:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:37:25 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 07:37:25 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 May 2024 23:20:59 GMT
ENV TOMCAT_VERSION=9.0.89
# Tue, 07 May 2024 23:20:59 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 07 May 2024 23:20:59 GMT
COPY dir:b8a94ec840bab9d4d850a6a7ef270cb19e9c1b32145a4e7e11b2f30927118e58 in /usr/local/tomcat 
# Tue, 07 May 2024 23:21:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 23:21:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 May 2024 23:21:04 GMT
EXPOSE 8080
# Tue, 07 May 2024 23:21:04 GMT
ENTRYPOINT []
# Tue, 07 May 2024 23:21:04 GMT
CMD ["catalina.sh" "run"]
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 17 May 2024 15:09:58 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 17 May 2024 15:09:58 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 May 2024 15:09:58 GMT
ENV XWIKI_VERSION=15.10.9
# Fri, 17 May 2024 15:09:58 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.9
# Fri, 17 May 2024 15:09:58 GMT
ENV XWIKI_DOWNLOAD_SHA256=279581bd5c733e8f3eeed31a405055987380cb1abb3303de38200d6d4db176b7
# Fri, 17 May 2024 15:09:58 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Fri, 17 May 2024 15:09:58 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Fri, 17 May 2024 15:09:58 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 17 May 2024 15:09:58 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 17 May 2024 15:09:58 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 17 May 2024 15:09:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 17 May 2024 15:09:58 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 17 May 2024 15:09:58 GMT
VOLUME [/usr/local/xwiki]
# Fri, 17 May 2024 15:09:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 May 2024 15:09:58 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2472ac6840da0115175cae8b0be8d1b8c2b6b74acb5fc6bf185b0c9333b8a3`  
		Last Modified: Thu, 02 May 2024 04:17:28 GMT  
		Size: 12.8 MB (12847034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1725094f1f7082f023c1a047ec828bf8229f9aa4b95de8dfcf3433a5664a8625`  
		Last Modified: Thu, 02 May 2024 04:20:25 GMT  
		Size: 46.7 MB (46716197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e995ccba802f11ec98d823c76df9fc769ae179b10b0a6b239f526dcd74f907aa`  
		Last Modified: Thu, 02 May 2024 04:20:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7fbbe7faa2fd420d969dafb00e3a6a0cc66074e4786e50e8c8b4f22e7f754`  
		Last Modified: Thu, 02 May 2024 04:20:20 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9666217ba41c0c5a6f7ace07c942c84f4762d6f14221dbbc651bc4aef8b0243d`  
		Last Modified: Thu, 02 May 2024 07:45:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa318c02521aad75976eebafc1a135480719bf32cfe1e85c91c43535a1f2c137`  
		Last Modified: Tue, 07 May 2024 23:30:38 GMT  
		Size: 12.4 MB (12444605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e69e325416c906528142046036d641c4f764ca42dbb203daf7aac42870591e7`  
		Last Modified: Tue, 07 May 2024 23:30:37 GMT  
		Size: 455.6 KB (455595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c8d2caff2bed2338c1b405f807e72d6ab820ac3cedd1e6440ae4dc6c8ab34`  
		Last Modified: Tue, 07 May 2024 23:30:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e034703a89549cc43cbbbc1d02b04878faef653caea94932d8a2d436808fd5c`  
		Last Modified: Fri, 10 May 2024 19:19:55 GMT  
		Size: 174.4 MB (174425544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bdb3d0f387b130b66574398c527a4414be3406049df906bd123a805c422411`  
		Last Modified: Fri, 17 May 2024 19:42:39 GMT  
		Size: 307.0 MB (306954035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21baa5d2c9341ef7e5818ffaabc4353ca12924576bc800c0789d3c646b9382e`  
		Last Modified: Fri, 17 May 2024 19:42:31 GMT  
		Size: 1.0 MB (1011974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7756ee6c9b1a1b7314a966af17ccf37f494547ee6e734075e063cfb5d335e5`  
		Last Modified: Fri, 17 May 2024 19:42:30 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba51a8454813a39193a312af7bef8bc7ba66bf62942f3da368a8db12f5dbc1fd`  
		Last Modified: Fri, 17 May 2024 19:42:30 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e670241a7a5977c51518c050b1cf30c863957bcdbc11f1bd15d73cfdb236798e`  
		Last Modified: Fri, 17 May 2024 19:42:32 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9597dbdec0ae6d2b732656229100e7fda93b9b0e4979a4ccab3d73cf2a588ba`  
		Last Modified: Fri, 17 May 2024 19:42:32 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:675e7a7785e7e119e6b2b7c102fbf0295a46df7b34a2bf15753baf70d1495eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8941719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24298f4f9e39a7d6ad714beec6e0ed3d5aa5a7eab0785fe78151139728f8c0`

```dockerfile
```

-	Layers:
	-	`sha256:e2cff65f3f9c39da2c821e3ba929d118a79686a78c5a4dd135a97f6da25cfd12`  
		Last Modified: Fri, 17 May 2024 19:42:31 GMT  
		Size: 8.9 MB (8901696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37de986b088c004bf0e0398f8d6a05659328b4d9d3c3cdcfbb4667fd83582aaf`  
		Last Modified: Fri, 17 May 2024 19:42:30 GMT  
		Size: 40.0 KB (40023 bytes)  
		MIME: application/vnd.in-toto+json
