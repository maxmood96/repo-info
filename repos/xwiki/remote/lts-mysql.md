## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:37dfaca548dd21484cc0f2c27e87809cce15a2539ceff15e0c937eb060bd542d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:f7c4edd6a30da030ff8c92e5ff5280bfe1e22a0e889f88fd8ae17418ca3fce3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624865678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a346febff008dfa0fc86df5eb222b1e9af5a3e1c9c4772b2f76e5cb63fd6fb88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:24:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 01:24:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:24:38 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 01:24:38 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 01:24:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:24:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:24:38 GMT
ENV TOMCAT_MAJOR=9
# Fri, 14 Nov 2025 01:24:38 GMT
ENV TOMCAT_VERSION=9.0.112
# Fri, 14 Nov 2025 01:24:38 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Fri, 14 Nov 2025 01:24:38 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 01:24:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:24:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 01:24:45 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 01:24:45 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 01:24:45 GMT
CMD ["catalina.sh" "run"]
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 01 Dec 2025 19:17:01 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 19:17:01 GMT
ENV XWIKI_VERSION=16.10.15
# Mon, 01 Dec 2025 19:17:01 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.15
# Mon, 01 Dec 2025 19:17:01 GMT
ENV XWIKI_DOWNLOAD_SHA256=996a47663bdc3d5abe93f76bda73ceb670618d3602e67c7077cb5962db436819
# Mon, 01 Dec 2025 19:17:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 01 Dec 2025 19:17:20 GMT
ENV MYSQL_JDBC_VERSION=9.5.0
# Mon, 01 Dec 2025 19:17:20 GMT
ENV MYSQL_JDBC_SHA256=f2ca3dfaf00d4aa311470db7ea3051962944ba0cb60005a2f75467549c39f425
# Mon, 01 Dec 2025 19:17:20 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.5.0
# Mon, 01 Dec 2025 19:17:20 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.5.0.jar
# Mon, 01 Dec 2025 19:17:20 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.5.0.jar
# Mon, 01 Dec 2025 19:17:20 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 01 Dec 2025 19:17:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 01 Dec 2025 19:17:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 01 Dec 2025 19:17:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 01 Dec 2025 19:17:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 01 Dec 2025 19:17:21 GMT
VOLUME [/usr/local/xwiki]
# Mon, 01 Dec 2025 19:17:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 19:17:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f878172f1ac3121519dd1795c821097cda557a10d8ac4526d248f9fe1738b942`  
		Last Modified: Thu, 13 Nov 2025 23:21:35 GMT  
		Size: 17.0 MB (16972399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b92fa77023f1881e077b68fb149d30aade157324fdc1181dacf19b57e1313b9`  
		Last Modified: Thu, 13 Nov 2025 23:22:21 GMT  
		Size: 53.0 MB (52978772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1321ce5b3e3ab111f1a88d34df69fbf748e96e3338e9f3d403b062e3e26d99d9`  
		Last Modified: Thu, 13 Nov 2025 23:22:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0e444f3c26062a0908ef59f39a3b8894225b2faef3d5b877c11441d3a52713`  
		Last Modified: Thu, 13 Nov 2025 23:22:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbea165fc4ff35146a8adaa801544eedc2fcf0f1d703505de0850ab9b1bb227`  
		Last Modified: Fri, 14 Nov 2025 01:25:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfca27531378f413da530fbbc6091094dfca85a6098450b921bae0110a5bd9d`  
		Last Modified: Fri, 14 Nov 2025 01:25:00 GMT  
		Size: 13.7 MB (13731896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2da11d900d8bf5c88d6309f7a33318bc006a9518a019c65afef83404d618bc0`  
		Last Modified: Fri, 14 Nov 2025 01:24:59 GMT  
		Size: 224.7 KB (224725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4847126e00eee350cc6a233d68e7728667213a5b34f02df1a1e1303f8c6f9a2d`  
		Last Modified: Mon, 01 Dec 2025 22:08:32 GMT  
		Size: 191.2 MB (191163967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfb7472b9e0da5b92bca567b93f2182ed35f39222d5aa5c796c1e460dbdae1e`  
		Last Modified: Mon, 01 Dec 2025 22:08:32 GMT  
		Size: 317.6 MB (317612344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523dfea47561e564567d35c7fefdf435ed03a11988e18571d19ae3b650dd4743`  
		Last Modified: Mon, 01 Dec 2025 19:18:29 GMT  
		Size: 2.4 MB (2441394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aec72c9a7c62193bfe07c6ad4614aad858913a4b2125a1fd0e31169598a897`  
		Last Modified: Mon, 01 Dec 2025 19:18:29 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1c9d5fa1e1203ca742942e13e2fd77d3e76d124c6e7525c35918890f775fe3`  
		Last Modified: Mon, 01 Dec 2025 19:18:29 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911c688b0c067d29ed9c8dc01f753f59c0a7ae191069946d827269c0836464d5`  
		Last Modified: Mon, 01 Dec 2025 19:18:29 GMT  
		Size: 6.6 KB (6639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df714f9cceb519b304dac525a44aa03b08be6a1e82a6f8adab893c0249e44589`  
		Last Modified: Mon, 01 Dec 2025 19:18:29 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:ae6077b749a82377ebd8ec4e5d75652db6599c9ab76b1e90fb0fabe958481094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9152270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa319c50fd341615bf7ea507cbdf22ee96eba52380aa8f7edbf98e43374c37b7`

```dockerfile
```

-	Layers:
	-	`sha256:853ab473558e46f195061eae190efac5a62488feb1daa3d1ce44a5b40d421c57`  
		Last Modified: Mon, 01 Dec 2025 22:07:24 GMT  
		Size: 9.1 MB (9110772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69a905f92151881c0596d730b3f20ad1e536f0e48d15a41d76c2ab70ce9c8c8`  
		Last Modified: Mon, 01 Dec 2025 22:07:25 GMT  
		Size: 41.5 KB (41498 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:630437d45e14059908f29de033bad076467ca4726d61883bd36be11f00454af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.9 MB (620878479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b1b0e9feb8f5963d55c20c66a52c8a4bfdf0bb1caf2aa5c51c79caf3fe43d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:41:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 01:41:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:41:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 01:41:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 01:41:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:41:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:41:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 14 Nov 2025 01:41:09 GMT
ENV TOMCAT_VERSION=9.0.112
# Fri, 14 Nov 2025 01:41:09 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Fri, 14 Nov 2025 01:41:11 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 01:41:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:41:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 01:41:22 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 01:41:22 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 01:41:22 GMT
CMD ["catalina.sh" "run"]
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 01 Dec 2025 19:17:01 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 01 Dec 2025 19:17:01 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 19:17:01 GMT
ENV XWIKI_VERSION=16.10.15
# Mon, 01 Dec 2025 19:17:01 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.15
# Mon, 01 Dec 2025 19:17:01 GMT
ENV XWIKI_DOWNLOAD_SHA256=996a47663bdc3d5abe93f76bda73ceb670618d3602e67c7077cb5962db436819
# Mon, 01 Dec 2025 19:17:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 01 Dec 2025 19:17:21 GMT
ENV MYSQL_JDBC_VERSION=9.5.0
# Mon, 01 Dec 2025 19:17:21 GMT
ENV MYSQL_JDBC_SHA256=f2ca3dfaf00d4aa311470db7ea3051962944ba0cb60005a2f75467549c39f425
# Mon, 01 Dec 2025 19:17:21 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.5.0
# Mon, 01 Dec 2025 19:17:21 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.5.0.jar
# Mon, 01 Dec 2025 19:17:21 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.5.0.jar
# Mon, 01 Dec 2025 19:17:22 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 01 Dec 2025 19:17:22 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 01 Dec 2025 19:17:22 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 01 Dec 2025 19:17:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 01 Dec 2025 19:17:22 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 01 Dec 2025 19:17:22 GMT
VOLUME [/usr/local/xwiki]
# Mon, 01 Dec 2025 19:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 19:17:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e052f7b40adf3e6b8172dd9f3385e9469f4dcfbea63c3518933c4239901bcc`  
		Last Modified: Thu, 13 Nov 2025 23:21:05 GMT  
		Size: 17.0 MB (16989179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07df04fa133324a49bb96c54d2b02e9d4463a8a2ba701459d09aac3d20984431`  
		Last Modified: Thu, 13 Nov 2025 23:21:47 GMT  
		Size: 52.1 MB (52148635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3225358e001b3b4abaaa7eddcf1179402e80dd7e5627430be9ec054cf2e309`  
		Last Modified: Thu, 13 Nov 2025 23:21:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Thu, 13 Nov 2025 23:21:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d0874a2b3978833b9ffcbd93fd9270f7311b8ed83f76d0f52485dd4424f96`  
		Last Modified: Fri, 14 Nov 2025 01:41:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b7077ce17e0a1b9281156f6a644fa9a8e5e38797e44d0a0dd1aaeb12bce98`  
		Last Modified: Fri, 14 Nov 2025 01:41:44 GMT  
		Size: 13.7 MB (13740078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5491fceb91f2532aadb2d169c4176e6237efcc85178e19ee3bb52037f924c6f`  
		Last Modified: Fri, 14 Nov 2025 01:41:38 GMT  
		Size: 225.2 KB (225176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14e55e2acf80aab276b584a955730da0b681335491c3ba03bc4d0d65caf05ef`  
		Last Modified: Mon, 01 Dec 2025 22:16:14 GMT  
		Size: 188.8 MB (188844194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac798fb3a43f07881116dc00534329201e80037c4b42e0dabd0e2c3f8f5444`  
		Last Modified: Mon, 01 Dec 2025 22:16:26 GMT  
		Size: 317.6 MB (317612354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf585a99e737d2210dbd5a8935b233684866b4592bfa8ea0bc675a3715c4c63`  
		Last Modified: Mon, 01 Dec 2025 19:18:30 GMT  
		Size: 2.4 MB (2441395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae981925753263954566b4aef896ed6673625c4545a7ec8ea4d1384e1223808`  
		Last Modified: Mon, 01 Dec 2025 19:18:29 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccad4fbfd018e950b1a235498c8e395782b92b3bbc2501b883a45bbdd0b8bff`  
		Last Modified: Mon, 01 Dec 2025 19:18:29 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc259043ddc6a8c479a4dc15b857b130020812bb40c290cf193a933ef727e4b4`  
		Last Modified: Mon, 01 Dec 2025 19:18:30 GMT  
		Size: 6.6 KB (6641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995f2a3bc15be86b3af34fe9049933b3f5a587aaf3bd08e4d95b2ebc59600c7b`  
		Last Modified: Mon, 01 Dec 2025 19:18:29 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:5e2eec7a7d2314667b1542ced4a44fe89d15fbd2576f38cbe4324dcdb5b163c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9153268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a987cde54735f7e9c0d0566f0696599c6514ff902a853cedffb7dcecab450b6`

```dockerfile
```

-	Layers:
	-	`sha256:a554da092822301c55fad5af38d73a57831ba2ec1e5843fb88c72bf5782b7625`  
		Last Modified: Mon, 01 Dec 2025 22:07:34 GMT  
		Size: 9.1 MB (9111561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87af91924a8aa697043cb63c0b6511f0d81bd53897c57c77b0fc877c8da5c68`  
		Last Modified: Mon, 01 Dec 2025 22:07:34 GMT  
		Size: 41.7 KB (41707 bytes)  
		MIME: application/vnd.in-toto+json
