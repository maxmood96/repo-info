## `xwiki:16-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:391cf7316cf8420b0c17c169c32b421b60951892890dc6934ae38415d5725b7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8d61bc30c6b5ea262b1e449fd9d830997ee150b021a3cfa2902a47eebe79a219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.1 MB (576101348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f276886c7a7acf3eaa5144766283c752579da1520e6c4d99255f232d8a8be505`
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
ENV MARIADB_JDBC_VERSION=3.3.3
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Mon, 25 Mar 2024 15:14:20 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:58391a98568fac0cb5437bdc1d8d22ff13f326ff0a6260a1a9ab92d03f7f206e`  
		Last Modified: Fri, 26 Apr 2024 03:51:52 GMT  
		Size: 178.4 MB (178430350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a47f0788f88b5b782d03b97af8d47282400db97eadad5161c17212a7b449f9`  
		Last Modified: Fri, 26 Apr 2024 03:51:52 GMT  
		Size: 293.6 MB (293556629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d288c00a7fa3a1c496e9efd30bc8b3a7064ba3ab8c16b95ec761910c038505f`  
		Last Modified: Fri, 26 Apr 2024 03:51:47 GMT  
		Size: 620.0 KB (620003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd6f818f909be8232eeec6014e2477f728a8eb73326958b3187143a95469304`  
		Last Modified: Fri, 26 Apr 2024 03:51:47 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd88147d76b43d968c84b25d7af13e3e5aed19634d3f7506699b5464f7ba8f1`  
		Last Modified: Fri, 26 Apr 2024 03:51:48 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc22c8d1c7365422edbe696cc6df0f9c8fd48c1d6f6b20ad6c83780c47062a7`  
		Last Modified: Fri, 26 Apr 2024 03:51:48 GMT  
		Size: 6.5 KB (6512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3f4ccb52c937767b2710f46065926aa0f9cf577639f8622e00b5b13470cc38`  
		Last Modified: Fri, 26 Apr 2024 03:51:49 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b2d0650d61483fb65530d85ddfd527ccfeeeaa8fb73949188aecade1a4872eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8925811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0032da0d066f522fc4ea1918c4498096b0acf4067503e64b99cd9406013ebab5`

```dockerfile
```

-	Layers:
	-	`sha256:e0db79ec5cc98562ba172bf8a1c03a7e1f7661d940d34f0520e4bec0f8d55d63`  
		Last Modified: Fri, 26 Apr 2024 03:51:48 GMT  
		Size: 8.9 MB (8884103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d32a54a7f6f8f2107d0b6223bd200a2c1c9eac1981b652bb64b236604e25d6af`  
		Last Modified: Fri, 26 Apr 2024 03:51:47 GMT  
		Size: 41.7 KB (41708 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:48764cc00ce0f64372a1a05255238235f78e724fae25f593144dcd1c8ccf029f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.4 MB (568449016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022491805196b8c67e594319d73115310f5bbc001a0ebe19577c6238ebcf7d07`
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
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
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
ENV TOMCAT_VERSION=9.0.88
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Mon, 25 Mar 2024 15:14:20 GMT
COPY dir:ba3e33ed23284380cd070ee082efc56bd4e069281d5d61e5fd722562420f4b69 in /usr/local/tomcat 
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
ENV MARIADB_JDBC_VERSION=3.3.3
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Mon, 25 Mar 2024 15:14:20 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9331e6965ccd210b6fd21419523ddc450c72626bd5ca5b0672bb8c0a1cb596ad`  
		Last Modified: Tue, 16 Apr 2024 02:58:28 GMT  
		Size: 46.6 MB (46639080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af58a4038ec765397b1ef467a9d6da1d336353f28df5cc32c5516aa471e4bb4e`  
		Last Modified: Tue, 16 Apr 2024 02:58:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8322d102061cd226429f20602d322142091650639e707df1fc051fbc869c138e`  
		Last Modified: Tue, 16 Apr 2024 02:58:22 GMT  
		Size: 732.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e02da29e0dc36cfae157626956d709192018538adafffbf45caf04e6a5125bc`  
		Last Modified: Tue, 16 Apr 2024 08:41:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05628a793e4710e8b8b6ff5020fc155e6fb4b9f57abb6a53107c4a9063206fd2`  
		Last Modified: Wed, 17 Apr 2024 01:03:32 GMT  
		Size: 12.4 MB (12430998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80252592221cd05095a4d105203d89f19cca649dfcbdd8fa72e81b2032a32a25`  
		Last Modified: Wed, 17 Apr 2024 01:03:31 GMT  
		Size: 455.7 KB (455662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2f7057439ac6773bf8cae77e2fb8b772c8eb0dbcc9e4ec133d1d9642a32b1`  
		Last Modified: Wed, 17 Apr 2024 01:03:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cae0fda705047354692cc1a8f026d0611d4f05e02a33f2d60cc610292093d1`  
		Last Modified: Thu, 18 Apr 2024 18:48:47 GMT  
		Size: 173.5 MB (173485383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc0c14a4e6cee8a4c7d99421234e4ced39f71a45b73a93c0c3745ec579ae38`  
		Last Modified: Thu, 18 Apr 2024 18:48:50 GMT  
		Size: 293.6 MB (293556685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25b20b9f17b4716aecb1db4fa4c4ee3fcb86a0ce58db2a898eef7472063793e`  
		Last Modified: Thu, 18 Apr 2024 18:49:35 GMT  
		Size: 620.0 KB (620003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0063b0a47bf4a3cab8b9694ff48bf771a1c4b69859757132ec47702cced85ba`  
		Last Modified: Thu, 18 Apr 2024 18:49:35 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a25d7f257d7d37eee4bc6069f472481cb99a4fc8ac0761827246b80180cff7`  
		Last Modified: Thu, 18 Apr 2024 18:49:35 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0224e6b85489278b5b9156449ff1985f619846e2e6cda834735a4195e1b5f3`  
		Last Modified: Thu, 18 Apr 2024 18:49:35 GMT  
		Size: 6.5 KB (6511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6670917dd83b9baee7fbf13853936bd0cbd50bf3c43d403e0aa19e16dc48f72e`  
		Last Modified: Thu, 18 Apr 2024 18:49:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:8e91309e24171088bb34e20f5afc97ca5f6a192c62d13a3542ebae3fc59b6497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8923435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1a6936ecb57be1ca944b9489298f58b461d5e5e7960f30783762ba0d4d240b`

```dockerfile
```

-	Layers:
	-	`sha256:869fd00bfe5d142ff97452383fb643aa2397b1d50882e61dd00e0b123288cf62`  
		Last Modified: Thu, 18 Apr 2024 18:49:35 GMT  
		Size: 8.9 MB (8883178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c242b157d91d747ed9bac57f9298987d9c9994af2d1ee04eb32887f62e47c36`  
		Last Modified: Thu, 18 Apr 2024 18:49:35 GMT  
		Size: 40.3 KB (40257 bytes)  
		MIME: application/vnd.in-toto+json
