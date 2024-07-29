## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:a3e4e3f777c87e4c36f157c0cebc437fe9abecc87e24acf882a53084f2dcf549
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2ad29574b4811e16faab21f4c7f409e81843d2fa468db8b76f711315f059808a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.9 MB (610886659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280cc66d1ff12df62db703bca8dea2d9241d9390ddcd02cba4979b6f8ba609ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 25 Jul 2024 19:41:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jul 2024 19:41:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 19:41:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jul 2024 19:41:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jul 2024 19:41:10 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_MAJOR=9
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 25 Jul 2024 19:41:10 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 25 Jul 2024 19:41:10 GMT
ENTRYPOINT []
# Thu, 25 Jul 2024 19:41:10 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jul 2024 15:54:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_VERSION=16.6.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.6.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_DOWNLOAD_SHA256=504e3fc3707d222d4a2be7c4e51e01242d4a7092380234d5076616d170390fe7
# Mon, 29 Jul 2024 15:54:10 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Mon, 29 Jul 2024 15:54:10 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jul 2024 15:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 15:54:10 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced013eec6cb5fa5c1146b85b09e19552a5b54474297bbaeba8a333739bbbbef`  
		Last Modified: Tue, 23 Jul 2024 01:09:03 GMT  
		Size: 47.3 MB (47280194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73663ebb99d0b0749c0e265014cd2e9a976615d5b102f5d5d69b141899661e7f`  
		Last Modified: Tue, 23 Jul 2024 01:08:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36083ab7049b9d911a90609cf0790cf4715c8edc0c0ec4a7447210b0f302e562`  
		Last Modified: Thu, 25 Jul 2024 17:30:44 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1712b240d8886fcd6756486de884748f855d613d8a262937d7ca6d689322fdf2`  
		Last Modified: Fri, 26 Jul 2024 19:51:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec0ca70282cddddf069e44e416a77ae11e281bbd02377cdaea65a134f6e3aa8`  
		Last Modified: Fri, 26 Jul 2024 19:51:14 GMT  
		Size: 12.4 MB (12402892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e3745fc67a1f455afac9802a3ea9b29493e8b302997bd61985905fb30aaa75`  
		Last Modified: Fri, 26 Jul 2024 19:51:14 GMT  
		Size: 210.8 KB (210770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9729a0c8ffb64de62c978c4759b6cb96f14f43ddf905cfc74ce3c649fff1aa`  
		Last Modified: Mon, 29 Jul 2024 18:57:22 GMT  
		Size: 194.3 MB (194291180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5139aacc0b2718aa01f909c3f71d3aa4cd525140245b6a03223ed7095e6fd28`  
		Last Modified: Mon, 29 Jul 2024 18:57:23 GMT  
		Size: 311.3 MB (311342424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb02bed8643eb00d9c7d7a78ebedb014ca569754077ec89ced0cf1696f0f85f`  
		Last Modified: Mon, 29 Jul 2024 18:57:19 GMT  
		Size: 1.0 MB (1011977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f01ad252f359054d83a09e6af38aae72ed9d02beebba24144c504d87f2941e`  
		Last Modified: Mon, 29 Jul 2024 18:57:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c3d90a862d74d4b9a63fcf14565ab1b1ded6c1adb2a40dfabeb3d010bc807`  
		Last Modified: Mon, 29 Jul 2024 18:57:20 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f6e9ac0451c825b2e701b314779f2216c501a53ae9bfee874beffef39b5226`  
		Last Modified: Mon, 29 Jul 2024 18:57:20 GMT  
		Size: 6.5 KB (6545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4815a2bda4c56013888a71667c27e08612b0e22fec4ec847b1b67d0cec78bff2`  
		Last Modified: Mon, 29 Jul 2024 18:57:21 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0aa2fe64e797266bde63d430db477d6afb3b68e7126d95ab8a13aea5c66c6195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8636906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3b104152642bf07eb2915d423e2e29245558a75b857f206c288fc087a15c97`

```dockerfile
```

-	Layers:
	-	`sha256:e81db0cdeb00d3f376a0ef4124c9d4ad83cbe511cf293c1c50c605391dd8f60c`  
		Last Modified: Mon, 29 Jul 2024 18:57:19 GMT  
		Size: 8.6 MB (8595631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13a4c7673d259f1197d5dac34c4310057135947d4530af59d20ac9ea2165978`  
		Last Modified: Mon, 29 Jul 2024 18:57:19 GMT  
		Size: 41.3 KB (41275 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:9115c643189e0179752bce1cb7633a2b8ee90626e744e88d5c0e9b207c44b4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.3 MB (591296481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3285b240917614f18abacbd4d15fe34c9c41cfb088c7586882c671013b07b15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 09:06:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jun 2024 09:06:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 09:06:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jun 2024 09:06:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 09:06:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jun 2024 09:06:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jun 2024 09:06:21 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_MAJOR=9
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_VERSION=9.0.91
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Wed, 26 Jun 2024 09:06:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT []
# Wed, 26 Jun 2024 09:06:21 GMT
CMD ["catalina.sh" "run"]
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 26 Jun 2024 09:06:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_VERSION=16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=0997ff4cfe16928996218963fad74d7a564c1aa75c7e8434e7cd25bd471ecd5a
# Wed, 26 Jun 2024 09:06:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e1b72ba4c1374ee7def94c45e1f16cacc330b2d3e90ca790d283de5db18cb8`  
		Last Modified: Tue, 23 Jul 2024 04:14:18 GMT  
		Size: 46.7 MB (46746369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e9b14b806a8f1a54d78e10962c1460615fa346fbea1aeb53c168a9807e5a7e`  
		Last Modified: Tue, 23 Jul 2024 04:14:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85331be2ec25884f920b5a4938bc420e89eddfe3915d32e7aab3ec5460a9adb`  
		Last Modified: Thu, 25 Jul 2024 17:46:26 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3b59b43989e28a2d54dbed5a37f1ee96bc284a19e6bc342d4ea05fd0a9f81b`  
		Last Modified: Fri, 26 Jul 2024 19:59:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95e47edbba305419b8b7ce85fa90c430b2a467bf8d1075387a5bd70259b31f9`  
		Last Modified: Fri, 26 Jul 2024 20:01:15 GMT  
		Size: 12.4 MB (12410361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf61c20da539f0280fc1e3831f6906faa148de4d5c43b512ef8687058435201`  
		Last Modified: Fri, 26 Jul 2024 20:01:15 GMT  
		Size: 211.4 KB (211403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6370d614bf96d1e0dc0786931749a72c6c93b913edb5bbf54b366a5839a17c00`  
		Last Modified: Fri, 26 Jul 2024 20:57:09 GMT  
		Size: 192.9 MB (192932233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b4a6e04dc8a751fbfbac86ec49f53ccf6825852c931a17f5edc9f3e976b396`  
		Last Modified: Fri, 26 Jul 2024 20:57:11 GMT  
		Size: 294.3 MB (294265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb6f641b2b440e19588cb8120b10866500e0c50899c2c7b6dc7c9c12700ec63`  
		Last Modified: Fri, 26 Jul 2024 20:57:04 GMT  
		Size: 1.0 MB (1011979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2960a031e085eae58bac7ffc2a37db9f419b40db60ca1aeb0fcdcf7e91d90516`  
		Last Modified: Fri, 26 Jul 2024 20:57:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76350d8f1c297fc8955e90ad66772fba7ddd597df743c04790be542375a0b68`  
		Last Modified: Fri, 26 Jul 2024 20:57:05 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3272418dc8240d03cc8d31d7e1cee94f4317715d8bba7e60cede0bdbc8c94fc`  
		Last Modified: Fri, 26 Jul 2024 20:57:05 GMT  
		Size: 6.5 KB (6528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eac3fe217134b09c75fe80cb7ba7adc2d23cfa58ed8559a43faf0922f2d8ef`  
		Last Modified: Fri, 26 Jul 2024 20:57:06 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:a546d15fe8d9265bbc693d27e5c8542f1525d286943beb76fa9010bbab5d5cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8633582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179860acf441d635fbab5cb6280403ecc16dad2c364ba031d399f7dc9b6d217f`

```dockerfile
```

-	Layers:
	-	`sha256:0166b458f306d4c6b4e42f5266d057510711bb5b3bdc45bc16b1e710e637b284`  
		Last Modified: Fri, 26 Jul 2024 20:57:04 GMT  
		Size: 8.6 MB (8591550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4339126a5cab689f0ad32ca80f71a60a30a5d1e732e4126f50c307677ccd5562`  
		Last Modified: Fri, 26 Jul 2024 20:57:04 GMT  
		Size: 42.0 KB (42032 bytes)  
		MIME: application/vnd.in-toto+json
