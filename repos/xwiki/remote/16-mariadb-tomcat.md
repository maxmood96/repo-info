## `xwiki:16-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:91893c018ba469a37be0989c89d6653818c0231cd67d9f0022564947309b8e7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:95a4e3076419bfd1f30ea554f5a0367c710d8d6986e4caa93dd3866c2419e923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.5 MB (576487347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5253242f552a013a22df93748baf5d4b24e0e6ecd3441ef3b1b84d77fac2fa`
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
ENV TOMCAT_VERSION=9.0.89
# Tue, 30 Apr 2024 13:35:01 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 30 Apr 2024 13:35:01 GMT
COPY dir:65d1d1b9512dfd4e1ebebbeb9b29b52484b09ce5380067ed2396b3f6fc00cfa9 in /usr/local/tomcat 
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
	-	`sha256:53b3457b74a540deefd3233542af85b89b4d69c4359a1d2e107a6c481ed52f19`  
		Last Modified: Tue, 07 May 2024 22:50:07 GMT  
		Size: 178.4 MB (178431477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48be3f709cc7d23a183a036738a6f1deb252bbc470105ed9b6b62a3382d8ad7a`  
		Last Modified: Tue, 07 May 2024 22:50:09 GMT  
		Size: 293.9 MB (293927661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff9ff182884d8470c57364bcfd564be42749882dcdf9e3ac03ae86f5a4742e1`  
		Last Modified: Tue, 07 May 2024 22:50:05 GMT  
		Size: 620.0 KB (619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906993f9b5cf67b11c794fd46a5e63e98bd99b149faa8b7a202b846bc4e3fa2d`  
		Last Modified: Tue, 07 May 2024 22:50:05 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b1cf8489fe2658dcde5525b5e67817275b17ea074ce34ecbb7433c138c3b40`  
		Last Modified: Tue, 07 May 2024 22:50:06 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7650ad5931a9b01e2156aee1a2d2e03ef2f7c62aeaaded5d9d946b01a0136`  
		Last Modified: Tue, 07 May 2024 22:50:06 GMT  
		Size: 6.5 KB (6493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6220ddce61b166998dbdabb311c4c2d84ff7aed2200f88dde423d70d18729c2a`  
		Last Modified: Tue, 07 May 2024 22:50:06 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:05177259317b40052b393e719aa79f8b03709005584e6651ea470263c937d4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8925509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf72ee472e3483b4a2ccfaf2d81b3e6f16cd03704df9bf233ecdc7ea5365ed02`

```dockerfile
```

-	Layers:
	-	`sha256:050109090ba9a55f763f36fd2a12885871ba46a3486ca7c5b771407644d7cad3`  
		Last Modified: Tue, 07 May 2024 22:50:05 GMT  
		Size: 8.9 MB (8883801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6076cea937a587833e5f1ac31a44d8fba859f06ee72cbfd422ca5f93d7351ce9`  
		Last Modified: Tue, 07 May 2024 22:50:05 GMT  
		Size: 41.7 KB (41708 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a11d2a3e3086d55967f4646834ece86807ac57f1d6318aec2fe85f3dc25c8215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.9 MB (568912603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5000637b95b3710da785d1cfc733d38aeaaa245a14df3efa2eff9ddd37b3e663`
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
ENV TOMCAT_VERSION=9.0.89
# Tue, 30 Apr 2024 13:35:01 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 30 Apr 2024 13:35:01 GMT
COPY dir:b8a94ec840bab9d4d850a6a7ef270cb19e9c1b32145a4e7e11b2f30927118e58 in /usr/local/tomcat 
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
	-	`sha256:f8845dba6c0aca8f2ccd30de3ffb3263f05006b084c58c34a0bdbd79b229c4f5`  
		Last Modified: Fri, 10 May 2024 19:19:28 GMT  
		Size: 293.9 MB (293927695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06d05db015d9fcd0205b842a39f00ee6744b459bbb31b547ded952a86cf43e8`  
		Last Modified: Fri, 10 May 2024 19:20:14 GMT  
		Size: 620.0 KB (619999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64321e1b56d9fa39ddfaea66837f29824c1c33822b840f7bb81f3286339aba1d`  
		Last Modified: Fri, 10 May 2024 19:20:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57ff8006bc83a8bcd5e3c7ed8d2163078c6272c52c340e1eaccafff3d497d1`  
		Last Modified: Fri, 10 May 2024 19:20:14 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8656d1c62865f837d6ae38b8f1eeb37b61cfc9123cc761aaf1d04ba12025fd`  
		Last Modified: Fri, 10 May 2024 19:20:14 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b100d1e6ce8f1735d1d9253944c05f181564aa9461562ebfa8cd68e0452591de`  
		Last Modified: Fri, 10 May 2024 19:20:15 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:31925fb8e11e22b42a61cca9d12dfa55abffc6697471c6658b4a0b87403534c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8924567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d043919162ab12318499dda686682b2cd70906ac340df50c461b15b49dd33570`

```dockerfile
```

-	Layers:
	-	`sha256:8bf5dcc388974605de9bf96062c61aacea0e0a1e182e799365082f81de7b66b4`  
		Last Modified: Fri, 10 May 2024 19:20:14 GMT  
		Size: 8.9 MB (8884310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c1a5255fed8f5e8dfefc223f532e2dfe0cc20577fb1bf5e68726072c633b86`  
		Last Modified: Fri, 10 May 2024 19:20:13 GMT  
		Size: 40.3 KB (40257 bytes)  
		MIME: application/vnd.in-toto+json
