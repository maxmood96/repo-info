## `xwiki:stable-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:ec6254955423f23c685beda033c4e2bfe964e19c062778a6407567281f9631a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7ab20eeb14370694007315ff6f1856cee80b176c2a0a91710a1bf8d741bfdb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.5 MB (576472978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8bea1daa740d8f9c8c6fd317c1404e6296f3830f1bcd536366ef778cc7cdf7`
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
# Tue, 30 Apr 2024 13:35:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 30 Apr 2024 13:35:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Apr 2024 13:35:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 30 Apr 2024 13:35:01 GMT
WORKDIR /usr/local/tomcat
# Tue, 30 Apr 2024 13:35:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 30 Apr 2024 13:35:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 30 Apr 2024 13:35:01 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 30 Apr 2024 13:35:01 GMT
ENV TOMCAT_MAJOR=9
# Tue, 30 Apr 2024 13:35:01 GMT
ENV TOMCAT_VERSION=9.0.88
# Tue, 30 Apr 2024 13:35:01 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Tue, 30 Apr 2024 13:35:01 GMT
COPY dir:ebdb8f938135c02d6a60358a02680f5b0bf67eacca1c30775f85b1a7984edad0 in /usr/local/tomcat 
# Tue, 30 Apr 2024 13:35:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 13:35:01 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 30 Apr 2024 13:35:01 GMT
EXPOSE 8080
# Tue, 30 Apr 2024 13:35:01 GMT
ENTRYPOINT []
# Tue, 30 Apr 2024 13:35:01 GMT
CMD ["catalina.sh" "run"]
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 30 Apr 2024 13:35:01 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
ENV XWIKI_VERSION=16.3.0
# Tue, 30 Apr 2024 13:35:01 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.3.0
# Tue, 30 Apr 2024 13:35:01 GMT
ENV XWIKI_DOWNLOAD_SHA256=3d75d5d495ed89af2e76a6058fa347094be0efd4862f88814640cc18ef3e33ba
# Tue, 30 Apr 2024 13:35:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_VERSION=3.3.3
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Tue, 30 Apr 2024 13:35:01 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
VOLUME [/usr/local/xwiki]
# Tue, 30 Apr 2024 13:35:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 13:35:01 GMT
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
	-	`sha256:7a2e681f85013925f747d99ecdd813ecd2d9d0fad29b97b0bfbf426e578f43d5`  
		Last Modified: Thu, 02 May 2024 07:09:36 GMT  
		Size: 12.4 MB (12423147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2eb6018e14cc59f5d7ddccbd599e9691d3d249ca50f881379269f33868ccc3`  
		Last Modified: Thu, 02 May 2024 07:09:35 GMT  
		Size: 456.3 KB (456297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35304ffa265a9adcf59551997dd91595ebc48c7464439f782b90e7543a2da65c`  
		Last Modified: Thu, 02 May 2024 07:09:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fd5e326be3da142faa4ef16e33e16379e873e265595044ba5e9e8fca0a9010`  
		Last Modified: Thu, 02 May 2024 07:51:20 GMT  
		Size: 178.4 MB (178430677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b99a32788ca58ff1717f253446846427f722f2fb848551446b9bb339e32ccd`  
		Last Modified: Thu, 02 May 2024 07:51:22 GMT  
		Size: 293.9 MB (293927684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e15917582ff8f00c357ec97b26a360436a07ccb6042cc9f93b3eac6af4125`  
		Last Modified: Thu, 02 May 2024 07:51:16 GMT  
		Size: 620.0 KB (619999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5e6b81ddc34219042ff692964a4e91032a6785152dcd845c3f8d61a671bd7d`  
		Last Modified: Thu, 02 May 2024 07:51:15 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca6d1d01d927519b3f41dc3ea19707f978fa48dcad0991fcb15cc8ef0766380`  
		Last Modified: Thu, 02 May 2024 07:51:17 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa739e33528412591e829bbb4b21155d93c4318f0b5461983ec2129b1f8a3c98`  
		Last Modified: Thu, 02 May 2024 07:51:17 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa471e8571705af5a081ded7a57c4e416f731e1d89e012d8fa4872d91cc45d6`  
		Last Modified: Thu, 02 May 2024 07:51:18 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:87fc61134a3e5e7e58ab3da95fe75e39d89a5e62df6584afe5c77ae1e594baec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8925509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff23ec845ff02545b234108dfa4a70e9b5fc72443cf044d83b111aebd19b88a`

```dockerfile
```

-	Layers:
	-	`sha256:612707904b0057f0d1b88b121ef22c467a175716c6cc5596b6a5a541f7d40ae4`  
		Last Modified: Thu, 02 May 2024 07:51:16 GMT  
		Size: 8.9 MB (8883801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559ad2e2ba94492e095ac3c964465100046a5cc3a1724c33bee399aadd698590`  
		Last Modified: Thu, 02 May 2024 07:51:15 GMT  
		Size: 41.7 KB (41708 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:964782060d737f051e6443422af00b3a8471291f7b39abc9f25dc7468a974577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.9 MB (568896838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c85762af78e6543047e4b60283170f8783b68344ffc18d584a9433ec1a0ea8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
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
# Fri, 26 Apr 2024 02:02:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Apr 2024 02:02:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 02:02:05 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 26 Apr 2024 02:02:06 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Apr 2024 02:02:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Apr 2024 02:02:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Apr 2024 02:04:15 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 26 Apr 2024 02:04:15 GMT
ENV TOMCAT_MAJOR=9
# Fri, 26 Apr 2024 02:04:15 GMT
ENV TOMCAT_VERSION=9.0.88
# Fri, 26 Apr 2024 02:04:16 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Fri, 26 Apr 2024 02:04:16 GMT
COPY dir:949b638e0bd71c40d1afd6181bc6d9f0fc46ee6d705abc4af012e6d15a18c62d in /usr/local/tomcat 
# Fri, 26 Apr 2024 02:04:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 02:04:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 26 Apr 2024 02:04:21 GMT
EXPOSE 8080
# Fri, 26 Apr 2024 02:04:21 GMT
ENTRYPOINT []
# Fri, 26 Apr 2024 02:04:21 GMT
CMD ["catalina.sh" "run"]
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 30 Apr 2024 13:35:01 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 30 Apr 2024 13:35:01 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
ENV XWIKI_VERSION=16.3.0
# Tue, 30 Apr 2024 13:35:01 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.3.0
# Tue, 30 Apr 2024 13:35:01 GMT
ENV XWIKI_DOWNLOAD_SHA256=3d75d5d495ed89af2e76a6058fa347094be0efd4862f88814640cc18ef3e33ba
# Tue, 30 Apr 2024 13:35:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_VERSION=3.3.3
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Tue, 30 Apr 2024 13:35:01 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Tue, 30 Apr 2024 13:35:01 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Apr 2024 13:35:01 GMT
VOLUME [/usr/local/xwiki]
# Tue, 30 Apr 2024 13:35:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 13:35:01 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f037ef0398100188bd636ef3da1525cc5cc7f04347a802ecc28ba3240408631`  
		Last Modified: Thu, 25 Apr 2024 21:59:12 GMT  
		Size: 12.8 MB (12846901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a9d01cdbea836fa98a88c869097ca339c17dd29480bc1c936f937840fbde4d`  
		Last Modified: Thu, 25 Apr 2024 22:02:15 GMT  
		Size: 46.7 MB (46716123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659b60df2e1030cfa0f2df9583f9aab145276e83a37490b983bbcfa9322fde3`  
		Last Modified: Thu, 25 Apr 2024 22:02:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f320f164b70019d3de719bb4a4b380f596330be1d584f5d935f80a4344b5b48`  
		Last Modified: Thu, 25 Apr 2024 22:02:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a446eed99bcbdadbc8fe6082bd87759257142f6d07e8e65462a2afa53b44ae8b`  
		Last Modified: Fri, 26 Apr 2024 02:12:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b36432c64716cedc0b26bc0ac1a29cc3cbb5de0c2e6cb309bd8d77b43c8dff`  
		Last Modified: Fri, 26 Apr 2024 02:14:58 GMT  
		Size: 12.4 MB (12430989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fb8413e5a27c1d4ad9f81efe9ecb3ed87a3243ee0e336f72f37d4dd928bc12`  
		Last Modified: Fri, 26 Apr 2024 02:14:57 GMT  
		Size: 455.4 KB (455391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274afb70bd1a8e5276e866357759fb36d695550825e2aa970a162bd4fe46eef`  
		Last Modified: Fri, 26 Apr 2024 02:14:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6276f1e28c322732f53872584aeb670512f0a7883f459bd69f74dd63923173`  
		Last Modified: Tue, 30 Apr 2024 23:31:33 GMT  
		Size: 173.5 MB (173484973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dd9a11714ad771495421b86eb7339c6101d65b92d9e8b36441a58d93fd8335`  
		Last Modified: Tue, 30 Apr 2024 23:31:31 GMT  
		Size: 293.9 MB (293927665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16587059cc58334d10b5f71a6a06dfe4f4d2de686ffcd854fdf3508b1d7ec29f`  
		Last Modified: Tue, 30 Apr 2024 23:35:09 GMT  
		Size: 620.0 KB (620001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac378ac293c76d5dc859838612afe1f9c982b921ded7b8885e93d51153e59e`  
		Last Modified: Tue, 30 Apr 2024 23:35:09 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f49b59c4ab4a1ac29db559d6bdd4585b92863e760a887856312091368def854`  
		Last Modified: Tue, 30 Apr 2024 23:35:09 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aba47a7f817872f63dcc15e08664d1d3e74b4fc4f9a92fd131355ac8c747ac2`  
		Last Modified: Tue, 30 Apr 2024 23:35:09 GMT  
		Size: 6.5 KB (6498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09be894507ed688681702e4e1e46f588de3814858cfa3289d0f2401c35e37a6f`  
		Last Modified: Tue, 30 Apr 2024 23:35:10 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:771be786f8a734bf388b1fa23d9afc98d46f94ba05d22ba986f945331ec48d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8926001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eebcce89e278d04b0b243a1a797e4aaf8f306499a244501147710f2e1c76362`

```dockerfile
```

-	Layers:
	-	`sha256:5692b300110a214203ea096af4386455d3ef4c8397b7b816fb01bb4e37d104d3`  
		Last Modified: Tue, 30 Apr 2024 23:35:09 GMT  
		Size: 8.9 MB (8885744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95f5212dec758ba67d230977c48c22ed80b6b3d2f9992072423b30e00ea0ebd2`  
		Last Modified: Tue, 30 Apr 2024 23:35:09 GMT  
		Size: 40.3 KB (40257 bytes)  
		MIME: application/vnd.in-toto+json
