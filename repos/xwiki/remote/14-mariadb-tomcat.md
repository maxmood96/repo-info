## `xwiki:14-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:dd4ce7350c189546449b59dd9012ff9c101ca6ff59d9767b6ea19aca21ddad47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:14-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:282c16e7b60c0f232c5896bb55edae523c82dc18ab01ab892324888e5e1d9673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.1 MB (589093077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a975bbfc4a2e9b3f829974f4d5157c1831028b18c859cb4a7b5d616fb1276a4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.89
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 13 Feb 2024 09:10:03 GMT
COPY dir:65d1d1b9512dfd4e1ebebbeb9b29b52484b09ce5380067ed2396b3f6fc00cfa9 in /usr/local/tomcat 
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Tue, 13 Feb 2024 09:10:03 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
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
	-	`sha256:7d92dedf74c86581c9250c8efd40d4b31897f682e47b22c3b5454b2b4b700cc4`  
		Last Modified: Tue, 07 May 2024 22:50:11 GMT  
		Size: 178.4 MB (178431277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6828eedca7a3d6b5681bc4aa2f4aedfcde0d50ec2b14f2568165a907969c3354`  
		Last Modified: Tue, 07 May 2024 22:50:14 GMT  
		Size: 306.5 MB (306538805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ad34c2d0e55700b9cd328a5586a3b2683b440845020df97a46db243ccb1196`  
		Last Modified: Tue, 07 May 2024 22:50:09 GMT  
		Size: 615.1 KB (615142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cd519be43007cf4fed79fbdd1d482bdb0f45848ba3e66757539d1dbe3268d4`  
		Last Modified: Tue, 07 May 2024 22:50:09 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72acee0c8b3d46718bc222e1c312c622ddf6dc25e5cabb0000552bdd067d9f9`  
		Last Modified: Tue, 07 May 2024 22:50:10 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aeccd3d4f74a48bf365c8fc949b92aac794b5b0574dc97e1f44e5e14fa40a5`  
		Last Modified: Tue, 07 May 2024 22:50:10 GMT  
		Size: 6.1 KB (6135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6a7cb668ab7790ff2031b5e81f1ff11d2895618e72d23c5581c419a4dee44`  
		Last Modified: Tue, 07 May 2024 22:50:11 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:1654c47d0df3f1683817434436e9036a936381b5af28b9f7d7d19e5791ee57a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8920125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f13596496b33bc2446a8bc8b03d34939b51933e59e067cd3acad0e8b363155`

```dockerfile
```

-	Layers:
	-	`sha256:8550d75742db4866424ef8f5627cc65d41bc2bd86499229251f98c2290d15f43`  
		Last Modified: Tue, 07 May 2024 22:50:09 GMT  
		Size: 8.9 MB (8879429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ecd9dd6fc5ac2068abfd5b799eedd680135f2bd99c1363c453c1e98b791b527`  
		Last Modified: Tue, 07 May 2024 22:50:09 GMT  
		Size: 40.7 KB (40696 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:14-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:4a2c301e3aae4b04fdba7c9aed614cd34240ed2e4ab712db71996ef66cafe93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581518440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8821b4eef4ff7ef62c274cc2b89448a5b2865674994d290483d66328afc0c07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.89
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 13 Feb 2024 09:10:03 GMT
COPY dir:b8a94ec840bab9d4d850a6a7ef270cb19e9c1b32145a4e7e11b2f30927118e58 in /usr/local/tomcat 
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Tue, 13 Feb 2024 09:10:03 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
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
	-	`sha256:1299804ba64b9564a62051141359a8785e5c8fed7218c52739723927e4a3316f`  
		Last Modified: Fri, 10 May 2024 19:19:25 GMT  
		Size: 173.5 MB (173486519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d866cc746b93073b846712f89ae4a067c556aa8e9f39d6c3a5c53ba74c800d`  
		Last Modified: Fri, 10 May 2024 19:21:57 GMT  
		Size: 306.5 MB (306538757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8a42c8034324e7dace010f1eac1b38b3e95adb0ebc77ade242ddc2894cdd00`  
		Last Modified: Fri, 10 May 2024 19:22:48 GMT  
		Size: 615.1 KB (615140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac414bb727069299e170a0c37c186f00a32387bc0a275ed37ac317d16ec973a`  
		Last Modified: Fri, 10 May 2024 19:22:47 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937779930ed214fcc61c4ac701e9414c287a72abfb7d4faeb1656572c29798f`  
		Last Modified: Fri, 10 May 2024 19:22:47 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c1ed604a336975ddbef131942bd971a07811f924f1bc5685bc01d88337a956`  
		Last Modified: Fri, 10 May 2024 19:22:48 GMT  
		Size: 6.1 KB (6135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716f585c88a9a354cfe903732e8b5352e2dac275adf7151a8bb5f596cf9a278`  
		Last Modified: Fri, 10 May 2024 19:22:48 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:8d0741454628c9b4222cc5d43f74a5cdd768e3e5edb6fc62ec2a6205e2cb892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8919171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b7eabf53babbb1eeab46afbc17b771c1f89953583cdf073dd2a9054ab9269e`

```dockerfile
```

-	Layers:
	-	`sha256:8935abab5e1c3c9f16a114b86058bafc138f5f0daa8e8ce6120cabea90ba396d`  
		Last Modified: Fri, 10 May 2024 19:22:47 GMT  
		Size: 8.9 MB (8879932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b51d2047bd18fdbc664e4163c08332debd9abf95426bc1ecd2c7a6ac000d3a1`  
		Last Modified: Fri, 10 May 2024 19:22:47 GMT  
		Size: 39.2 KB (39239 bytes)  
		MIME: application/vnd.in-toto+json
