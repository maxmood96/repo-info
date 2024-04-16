## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:3c2268a8a3c27bed5f2df00935cc860bacfddc5fc88a09aa80653afee3c025c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:9545c7b4a97bca302290f3138fbd2efc942f15891cc6a2fe52a3140219e77938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577745261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1532d31fa4a977a2c199096dc222e8148448835dc5f24e217c90e646167797e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 25 Mar 2024 15:14:20 GMT
ARG RELEASE
# Mon, 25 Mar 2024 15:14:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Mar 2024 15:14:20 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["/bin/bash"]
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Mar 2024 15:14:20 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_MAJOR=9
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_VERSION=9.0.87
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Mon, 25 Mar 2024 15:14:20 GMT
COPY dir:02fcf5fddc0d509575aac0f258b8d0dd9791c34841d8f89045db868df7d275ef in /usr/local/tomcat 
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Mar 2024 15:14:20 GMT
EXPOSE 8080
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT []
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["catalina.sh" "run"]
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 25 Mar 2024 15:14:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_VERSION=16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=7d355ae1c88691b19af9658e3f042083d57c08d5e52e1ade25536536ad72fb3f
# Mon, 25 Mar 2024 15:14:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Mon, 25 Mar 2024 15:14:20 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
VOLUME [/usr/local/xwiki]
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dddff65ed2408fb8512cf4a5e475bc56396102dc76b9968c1f68a06414767b`  
		Last Modified: Tue, 16 Apr 2024 04:03:41 GMT  
		Size: 12.9 MB (12905145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1799e72eec6b835f4f493ec08eef7c0de31e3d1e4b3265db1d346a5282630e16`  
		Last Modified: Tue, 16 Apr 2024 04:06:54 GMT  
		Size: 47.2 MB (47163386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e489940d10c0f286533ea7999e045f2ff1188baa6aad2d676349e3e72c5e8b`  
		Last Modified: Tue, 16 Apr 2024 04:06:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34382f6b019ca012a4b3f974b3039a24f169585e6ae8fa737cf539791d51ea1f`  
		Last Modified: Tue, 16 Apr 2024 04:06:48 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3fe4efe3c3e9e7b9015cc8ea7e8520be3c126dc915b4987e9d8ab966fa0faf`  
		Last Modified: Tue, 16 Apr 2024 10:17:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3201e53b092426b22acbdac77348317958250542389726ab64297a080cfff2`  
		Last Modified: Tue, 16 Apr 2024 10:20:44 GMT  
		Size: 12.4 MB (12422012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fe89699442c19a7aaec012e3078afaf1a2e8c0a0edfcc92e53dbc80489154b`  
		Last Modified: Tue, 16 Apr 2024 10:20:43 GMT  
		Size: 456.3 KB (456304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2a23b9a44b245f77c5f55aaa48e1fe7c70c80a2feffcfb010764c2cc44da39`  
		Last Modified: Tue, 16 Apr 2024 10:20:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d876c9793813b34ffc3679ad5466d51ceb29eb89a5a0746cfc2505c1c3cd1d77`  
		Last Modified: Tue, 16 Apr 2024 15:32:48 GMT  
		Size: 178.4 MB (178431029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63371ae27a24b311364b88f1a59c24c643343982d979268c95bad38e923dc57f`  
		Last Modified: Tue, 16 Apr 2024 15:32:50 GMT  
		Size: 293.6 MB (293556771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ed8bcec70c8771ec76406cd63c050a319e6ac268b63eaaeac9be887e1e283`  
		Last Modified: Tue, 16 Apr 2024 15:32:44 GMT  
		Size: 2.4 MB (2356948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a4915983fb41f38abb15948a4d9165069894ec20094c166ae1551df03ad13`  
		Last Modified: Tue, 16 Apr 2024 15:32:43 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683f7e69bd96d7687f93fa47b0ff2400cdd31aa019c1ac9bb72b95707eec397b`  
		Last Modified: Tue, 16 Apr 2024 15:32:45 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad25020b2187c7e835e5da2fb445435cf77d9c79e5d96d972fd931f3a4166dcc`  
		Last Modified: Tue, 16 Apr 2024 15:32:45 GMT  
		Size: 6.5 KB (6507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bcc00ab2737614dc2c1cc392aea04e54c3471471cb311eb9fd34a081b012ab`  
		Last Modified: Tue, 16 Apr 2024 15:32:46 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:1ea7aadfff019af5c179472491108f83a37215e26a8a7fcdebf1402d6c507693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8927100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366ea4f44f3befddfc50b19ee4cde7c9bcdbc75e48ccae15bfb544bc8403d7f5`

```dockerfile
```

-	Layers:
	-	`sha256:d688b4e627073aeb383ca208303e363786a941eb4819f10d0dc1c64dcf72ee4d`  
		Last Modified: Tue, 16 Apr 2024 15:32:44 GMT  
		Size: 8.9 MB (8884062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691eab99f59571c5a67b20a281fcb5f45a9d5b933ac57e0ba4a73d42a660df66`  
		Last Modified: Tue, 16 Apr 2024 15:32:43 GMT  
		Size: 43.0 KB (43038 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ed237594fd1f854710bd743649cc735189b31e4e2420b6bcd1e26c116fe1d9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.1 MB (570108950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e4919314ec80e6b654dbae691863c09a1226ba5749092850301435144307da`
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
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Mar 2024 15:14:20 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_MAJOR=9
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_VERSION=9.0.87
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Mon, 25 Mar 2024 15:14:20 GMT
COPY dir:8bcf10de83e5c9461a50d63527d8bbd9f4b31ffd5258e2fe36c0035642b68b10 in /usr/local/tomcat 
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Mar 2024 15:14:20 GMT
EXPOSE 8080
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT []
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["catalina.sh" "run"]
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 25 Mar 2024 15:14:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_VERSION=16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=7d355ae1c88691b19af9658e3f042083d57c08d5e52e1ade25536536ad72fb3f
# Mon, 25 Mar 2024 15:14:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Mon, 25 Mar 2024 15:14:20 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
VOLUME [/usr/local/xwiki]
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2168560270786452bc1288278f5b8a7831c90a490efa55dc798deec8e871311a`  
		Last Modified: Thu, 28 Mar 2024 00:48:42 GMT  
		Size: 12.8 MB (12846303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6274ee4a91612c77ed0ab2ea4b1df4f10d29a3c2881d2d8b564571694cd9f69`  
		Last Modified: Thu, 28 Mar 2024 00:54:00 GMT  
		Size: 46.6 MB (46639100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f6d824ccd2521a065aa5ce5d027e0f7b027066e53446b20eaa7793a0bce51b`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754a82fa6b427b86617d873030d69cf741994674dcdcb02c137f9489c28e29c5`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539624d11ec8306e1980224e20640bf423bca84a7896fc4292ac0d60d97f3155`  
		Last Modified: Thu, 28 Mar 2024 03:18:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dbe414680b86fa37ae92fb3589adf419b3fe6720adbdc6a1164ac919930b6d`  
		Last Modified: Thu, 28 Mar 2024 03:20:55 GMT  
		Size: 12.4 MB (12428534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b41cf461b24710b11579d5cf03310e9f28fd578dcfbaaeb9bb61ebb45e1d658`  
		Last Modified: Thu, 28 Mar 2024 03:20:54 GMT  
		Size: 478.7 KB (478682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa9163075c103aabdd4a10296be353fed3964676a8a29a72b97a6f8a8d644a`  
		Last Modified: Thu, 28 Mar 2024 03:20:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b80a13dc72a7fbefde7bc273c163a11191e0ed271603e91fe32d924cc5fc574`  
		Last Modified: Thu, 28 Mar 2024 20:00:14 GMT  
		Size: 173.4 MB (173388060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173c296ee6951d629f5223126e927f4aaffc55b621ec25973a3b862297163a6`  
		Last Modified: Thu, 28 Mar 2024 20:00:17 GMT  
		Size: 293.6 MB (293556784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c38f9ad5dfbcd880414496e8a17a6dc490852c60f94377b0b49672d3ada3fa7`  
		Last Modified: Thu, 28 Mar 2024 20:00:11 GMT  
		Size: 2.4 MB (2356949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280cb311b4f10e3db01d10371b44013467919b7b6024e651c5365f684acf9a82`  
		Last Modified: Thu, 28 Mar 2024 20:00:11 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eb6b24d753d9c1521c082f4ab4d04cb0a9283f506fd737b9063584d07c1156`  
		Last Modified: Thu, 28 Mar 2024 20:00:12 GMT  
		Size: 2.4 KB (2375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ca8e89b3836cda47dc94a799cb2d9a4cd7a8497f7c1abfb48d15b1d0bb294f`  
		Last Modified: Thu, 28 Mar 2024 20:00:12 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef45396bff2d89b6ff6a2469b44a9f33968ed6f26b6a1de9b51b12e51c7a1894`  
		Last Modified: Thu, 28 Mar 2024 20:00:13 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:71c870fd6670954a82330cd6979e2ceb4ace10e2495940d156c323545ffabd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8927577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba53813ade957f9a249ee8aeea4960b9ba0701d0d05e466e8cf1a27baf790e8a`

```dockerfile
```

-	Layers:
	-	`sha256:ec95b632a6449a13aa2a22ce36d3c0552b3877af979667b9142be4bd377d6ad0`  
		Last Modified: Thu, 28 Mar 2024 20:00:10 GMT  
		Size: 8.9 MB (8885979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b2c31a0cca16e8954baff56a72185a8cea2055feb9eda4de0e9555f4aef99e`  
		Last Modified: Thu, 28 Mar 2024 20:00:09 GMT  
		Size: 41.6 KB (41598 bytes)  
		MIME: application/vnd.in-toto+json
