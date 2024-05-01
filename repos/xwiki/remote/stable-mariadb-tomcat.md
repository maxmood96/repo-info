## `xwiki:stable-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:d2e4aee9472d8e50380585741022088a497fd408b6180c74ca8dbce195be29df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5fba04cb72248dbad370b09f0f22d7d32b96e8c9279b66ccabf2bfc1a1befd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.5 MB (576473190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b4ab32e2ebbee0b6461113f6dd96258dcc5e9ae2b154733e46192276e7105e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
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
# Fri, 26 Apr 2024 02:29:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Apr 2024 02:29:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 02:30:00 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 26 Apr 2024 02:30:00 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Apr 2024 02:30:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Apr 2024 02:30:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Apr 2024 02:32:41 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 26 Apr 2024 02:32:41 GMT
ENV TOMCAT_MAJOR=9
# Fri, 26 Apr 2024 02:32:41 GMT
ENV TOMCAT_VERSION=9.0.88
# Fri, 26 Apr 2024 02:32:41 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Fri, 26 Apr 2024 02:32:42 GMT
COPY dir:008c1e737cb1d7c32c9c864d02bf0b16431c32c3c39b5b68188e5f3c48a90ec8 in /usr/local/tomcat 
# Fri, 26 Apr 2024 02:32:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 02:32:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 26 Apr 2024 02:32:49 GMT
EXPOSE 8080
# Fri, 26 Apr 2024 02:32:49 GMT
ENTRYPOINT []
# Fri, 26 Apr 2024 02:32:49 GMT
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
	-	`sha256:9bc90a49ab5d5aa39d793a7bf9730a0860d9802ada6d7fdf297a1c9b2ba213dc`  
		Last Modified: Tue, 30 Apr 2024 21:51:39 GMT  
		Size: 178.4 MB (178431148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1716d0051b7acc29c805381c5967f727fe2fd72fc36f0e75b2dde416d0d888`  
		Last Modified: Tue, 30 Apr 2024 21:51:40 GMT  
		Size: 293.9 MB (293927689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa34bde8d61a7114e76e50453b6db26b1039feaf4e24ff1e6c4c64a4589074cd`  
		Last Modified: Tue, 30 Apr 2024 21:51:34 GMT  
		Size: 620.0 KB (619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f2f9cc859fd53322b746e63e20ce4c02cc6bd78847eb5c2352d7eb6adb807e`  
		Last Modified: Tue, 30 Apr 2024 21:51:33 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81b3443927aec2ab0d620d88df13eeca5c5353f2194ae13b522d360ea114eee`  
		Last Modified: Tue, 30 Apr 2024 21:51:35 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570c02bf6209c3c90bd6aa0778bfb19edc444aff213e44605e7ec3ddf2874a03`  
		Last Modified: Tue, 30 Apr 2024 21:51:35 GMT  
		Size: 6.5 KB (6494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930d4e3e19cdcfade51243caaf3aacbc0f6ec7826f2ac57fbe792d8c14d8b91`  
		Last Modified: Tue, 30 Apr 2024 21:51:36 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:7c01560d1f2d38d25ecd3580fe2e59de1603b9084e68c3d90e0a6857e49448b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8926943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df9108e2f42763085337ca1242ec29898168dcbbec72b31e63acebf29627c32`

```dockerfile
```

-	Layers:
	-	`sha256:4aae996d0836ca79ed28fa46bc3000d1f29b5460774cdb6a4643ffe8b2dfcceb`  
		Last Modified: Tue, 30 Apr 2024 21:51:34 GMT  
		Size: 8.9 MB (8885235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7261c28b6cef551a740751bfc355d46278b264f15423412e36baadd6453ae8f`  
		Last Modified: Tue, 30 Apr 2024 21:51:33 GMT  
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
