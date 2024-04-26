## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:5516656303e504cbee07c58956202f817dfccf641d3fe12d931b05619103a55e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:a207f7675e595132f2b2a05ff1c43d13cea1e8f432aec6caf067d24c90c89c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.8 MB (577838364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426bf9c02b3f015aad3e42d8ce352c3dbb5fe49eed3f12c9bcb7b75414879b01`
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
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
ENV TOMCAT_VERSION=9.0.88
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Mon, 25 Mar 2024 15:14:20 GMT
COPY dir:008c1e737cb1d7c32c9c864d02bf0b16431c32c3c39b5b68188e5f3c48a90ec8 in /usr/local/tomcat 
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
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7c5a42f2fad87126e0a61b4605e0b8b0b8100485fbffb0fa0e14e87400873`  
		Last Modified: Thu, 25 Apr 2024 22:13:22 GMT  
		Size: 12.9 MB (12905143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7fcad56b7f8a33a6681a9ae067f80cc8ad2a08502172c8dda569c1338752bc`  
		Last Modified: Thu, 25 Apr 2024 22:16:38 GMT  
		Size: 47.3 MB (47256188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75513697e6ba945551856344dc1f1c94b25b9b98458dd13e8f1a25811e2424cc`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e30da527722230ddaac2aa5e9ae62f333caa596c7853ae2b516c06d2d6f321f`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbe592fe48d6c084fee6f5aacb2b9e6f82e7ca9df70e0b07d90293f5b63c3ce`  
		Last Modified: Fri, 26 Apr 2024 02:41:36 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444245f0d6247cb9dad7dfebf1c48a211ada161bfe718b510dcff4ace7db8b3d`  
		Last Modified: Fri, 26 Apr 2024 02:44:24 GMT  
		Size: 12.4 MB (12423161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b89b597525467f9c190aacd6e15109dd30104ea9f42c0012416b47528154d5`  
		Last Modified: Fri, 26 Apr 2024 02:44:23 GMT  
		Size: 456.3 KB (456347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84795a15235ec76f356d76ebe4b2c1bead01104cfc31262df94c8abca13321e0`  
		Last Modified: Fri, 26 Apr 2024 02:44:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fc78e4d34e42854df5823fc3b6473bf9e76ea1a0e888597e351dfc7dc9ef44`  
		Last Modified: Fri, 26 Apr 2024 03:54:33 GMT  
		Size: 178.4 MB (178430158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d99c650305474d35e9224788546a09bc26a2c1cc36de0c9fec82b1f74ee4d7`  
		Last Modified: Fri, 26 Apr 2024 03:54:35 GMT  
		Size: 293.6 MB (293556785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dcf6e85f90b7d0416440a1dc9cc7a198ab5bc63b33e6423587f1eb5af084c9`  
		Last Modified: Fri, 26 Apr 2024 03:54:28 GMT  
		Size: 2.4 MB (2356956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0549b7e49fa908ddd0005d744abd1efcdbd1ab1b074a0481505c0c29573095`  
		Last Modified: Fri, 26 Apr 2024 03:54:28 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c82ded9f37011f59f736fff9ec88e040261eeaf99c438e81f8550dda53cdfda`  
		Last Modified: Fri, 26 Apr 2024 03:54:30 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e5fb3d8adec6f548bcad15a73a0e2c70d4ef1fd887bc6c80212b17550afbf7`  
		Last Modified: Fri, 26 Apr 2024 03:54:30 GMT  
		Size: 6.5 KB (6507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4c81b7fabb0f070a51fce2580f9550113d02a984bc4a8e649813c932fa74dc`  
		Last Modified: Fri, 26 Apr 2024 03:54:31 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:1cdbab3377f7de9142451c7d79dd3474fa51760d796019713786de4334a71392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8928603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9edcf134c480df256b0a512436dc1d8f71796b6b4497ba1f497c084de929ea`

```dockerfile
```

-	Layers:
	-	`sha256:ac393a7aa823e0a20890b6f0f5301735c7e8999c8f211563249d31c3ce62bcd6`  
		Last Modified: Fri, 26 Apr 2024 03:54:29 GMT  
		Size: 8.9 MB (8885561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b155eb41ab50e3aa09a5b3bb569d3e00d46a0a92986f284f926756776b75450a`  
		Last Modified: Fri, 26 Apr 2024 03:54:28 GMT  
		Size: 43.0 KB (43042 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0d0444b6233c41acb4230c31db568fa4aa27dc347a657c7ea888ca139f14dc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570263135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38451dfe5aa06c2919e12458c3dfe13f4e4f7adba097405cfdb5d3112249d555`
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
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
ENV TOMCAT_VERSION=9.0.88
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Mon, 25 Mar 2024 15:14:20 GMT
COPY dir:949b638e0bd71c40d1afd6181bc6d9f0fc46ee6d705abc4af012e6d15a18c62d in /usr/local/tomcat 
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
	-	`sha256:3f2c1192b5bb1308699492a4fd2fa7d8df5a4318874faee05303aecbe96c55c1`  
		Last Modified: Fri, 26 Apr 2024 10:17:34 GMT  
		Size: 173.5 MB (173485176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ff7542ced33b70b1859045e907017bf2c4477d4f39f7e975eda489d37d55e8`  
		Last Modified: Fri, 26 Apr 2024 10:17:36 GMT  
		Size: 293.6 MB (293556706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b6598c42bb3497c4b3b6f79b3231b13c15a331b5a162f7704e1bed0773c01b`  
		Last Modified: Fri, 26 Apr 2024 10:17:30 GMT  
		Size: 2.4 MB (2356949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e215da6867eacfc746f49bd6c724ded32ee3f79d20c8465b808ba067edf1504`  
		Last Modified: Fri, 26 Apr 2024 10:17:31 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de76fbb9fdb0198dbcbeefd9265f4695581451bbe36f222f8f39d2132ae87a60`  
		Last Modified: Fri, 26 Apr 2024 10:17:31 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd8ddd2420e90fd7b976298046715e7543ff3e18e2ea1ebe50b800155f59cdf`  
		Last Modified: Fri, 26 Apr 2024 10:17:32 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074b08abf531fba17005384ee5524596d563e5688e49785b8582211a852982dd`  
		Last Modified: Fri, 26 Apr 2024 10:17:32 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:87d33697082afb3699c70a43b49893e54e1365e16360c4c6d7d141e75bc56156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8929147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43497915ae0c087655ddc84ef1b5a215b8ffa3f87a26f9b2f10d8967a2f7646`

```dockerfile
```

-	Layers:
	-	`sha256:1ea104018cdb17f61e453094742a3e09aba36a37b5fb1ef57a4c9c239e16b304`  
		Last Modified: Fri, 26 Apr 2024 10:17:30 GMT  
		Size: 8.9 MB (8886080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5424dada95c42dbd65f2bdb8e36b463662acee8c0e75cbba85314e9a8f98d156`  
		Last Modified: Fri, 26 Apr 2024 10:17:30 GMT  
		Size: 43.1 KB (43067 bytes)  
		MIME: application/vnd.in-toto+json
