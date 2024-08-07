## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:b5675426f492362724be336346d9a5520e7da8c7fd320dc93029882612bf1617
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:e070415ac0d0e34d121ccdddea9f2f03a053819444de73df1dbfda08bc24e4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.9 MB (609872254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7959a0fc06d6a490016ef84fd8477c88aede5ca9d327d5ebda897a43732bcb`
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
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_MAJOR=9
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_VERSION=9.0.93
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Thu, 27 Jun 2024 13:08:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT []
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 27 Jun 2024 13:08:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_VERSION=3.4.0
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_SHA256=d83970dcda3198ca480e59b38e9e7055df09833e40d898c8ec5778a1e767f93b
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.0
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.0.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.0.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
VOLUME [/usr/local/xwiki]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
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
	-	`sha256:6ebabd9dd3d661f4337c34c5c71db0a66af37e77d4d71c329df277ac865d32be`  
		Last Modified: Wed, 07 Aug 2024 00:52:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f15828f7294e3f654d8b020b16edabf41374164a0fc02b82961903abf3e3a53`  
		Last Modified: Wed, 07 Aug 2024 00:52:27 GMT  
		Size: 12.8 MB (12764999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2147aea82d8ede0ba5901aa23b2642c7ef9ad82d0fc2e4a997b58cb972afff0e`  
		Last Modified: Wed, 07 Aug 2024 00:52:27 GMT  
		Size: 3.0 MB (3011450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02e400462a094a0e719283b42df8fb283890b7bbf12f2961307b90eaec3b5d7`  
		Last Modified: Wed, 07 Aug 2024 01:52:37 GMT  
		Size: 194.9 MB (194859815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc5024c5af9a103d8af6a0bc8c54ef469a36ea46d49d07c667b514e871e153`  
		Last Modified: Wed, 07 Aug 2024 01:52:42 GMT  
		Size: 307.0 MB (306968159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4626100c5b6fbd5ab88c7967d2f1412d490ba1945cc0f386e556f1a64cc77414`  
		Last Modified: Wed, 07 Aug 2024 01:52:32 GMT  
		Size: 640.7 KB (640651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e455680e9036cb2ba82291c63fbeb733c7eadfa8c57b4856237aa4311d8018`  
		Last Modified: Wed, 07 Aug 2024 01:52:32 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fefaa6d52d148b7f0e7544e4cfed541c7b3667930a48dce28b540e37ba0774`  
		Last Modified: Wed, 07 Aug 2024 01:52:33 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72043912c9963f68995dc1769f1365df4b2ad154b7dea0564ab98c31020e8835`  
		Last Modified: Wed, 07 Aug 2024 01:52:33 GMT  
		Size: 6.4 KB (6433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681acc61defa3f7c8a4dd17b319cf917113ae18cdfa249df60088e7b948509c9`  
		Last Modified: Wed, 07 Aug 2024 01:52:34 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:f4841cd553bb4f43a6d5bbc95cbebfa28a991f90335c2a8e56a6b0d022cecc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8634757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c72cd1fc1edb2c4253baeecc962e950aa24950c9a385143b8e05c2c3d233f3`

```dockerfile
```

-	Layers:
	-	`sha256:b237443aa578ffc585c289d2cefbee7d89dbe0ece42b6750108d462d0e03ce3d`  
		Last Modified: Wed, 07 Aug 2024 01:52:33 GMT  
		Size: 8.6 MB (8593757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a126c950aecf1ead036d787a321ebbd300e4d7dd257feb3c0a347d7948b8a8e3`  
		Last Modified: Wed, 07 Aug 2024 01:52:32 GMT  
		Size: 41.0 KB (41000 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:1f7b01cf3a67e8058496a84d20bbee9ea2329de2ce9263eadffc2564a28855c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.2 MB (606157154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10acc11a6cc05eed302b746931f0229d877178731904e1d5f376058c8c54d864`
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
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_MAJOR=9
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_VERSION=9.0.93
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Thu, 27 Jun 2024 13:08:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT []
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 27 Jun 2024 13:08:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_VERSION=3.4.0
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_SHA256=d83970dcda3198ca480e59b38e9e7055df09833e40d898c8ec5778a1e767f93b
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.0
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.0.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.0.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
VOLUME [/usr/local/xwiki]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
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
	-	`sha256:81398c802f855559cf2a149120cb1b1bc1efaaaaae72c3a69a349a5191f1f0a8`  
		Last Modified: Wed, 07 Aug 2024 00:56:36 GMT  
		Size: 12.8 MB (12775005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372eb4e20c3ab8ffc9facc92d72985a4a495b48d2cbfaa334a74ec54930e85f1`  
		Last Modified: Wed, 07 Aug 2024 00:56:35 GMT  
		Size: 2.8 MB (2812902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873895de3d45d9444bd636414343b105216b3a3fdb39607ad4aff14f9aab777e`  
		Last Modified: Wed, 07 Aug 2024 01:57:35 GMT  
		Size: 192.5 MB (192495926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15f2a684524ba88fdc6be50fdb498cc8520c0603431c09f62749dfe344883a6`  
		Last Modified: Wed, 07 Aug 2024 02:00:27 GMT  
		Size: 307.0 MB (306968128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de50e112bc2086ed706f8bce61e739bda442fba248da1abcca92760a5a9015f3`  
		Last Modified: Wed, 07 Aug 2024 02:03:04 GMT  
		Size: 640.6 KB (640647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef5c10a38d87f7cf707cdf778778c7ce34f11bb2f4cc55777df78c31612cee6`  
		Last Modified: Wed, 07 Aug 2024 02:03:04 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227ed93eb7fec4670280b598e0d4f6829cec357623e1c8cf41a507e4557aa799`  
		Last Modified: Wed, 07 Aug 2024 02:03:04 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b965f4b5f7fda12f1e4b84da3c64a522180f866a46c47dfddbf69e97553929`  
		Last Modified: Wed, 07 Aug 2024 02:03:05 GMT  
		Size: 6.4 KB (6431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d8ed54e32763241654f0e6144b86ca76ff44f2936acc2c2de2a909537de60a`  
		Last Modified: Wed, 07 Aug 2024 02:03:05 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:fac259ce3c47a66ddbd4a2610ce1d053de4400f8603fcdcef8fcdcaf9da8d2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8636753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1981d281ac928bcd4fae2c74bb8ccbd2accc16e098d25e66a2c7f1692127c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:657ec6edcba1088457779628cc0c7fb02369eb43dfb255ef72dca466671ef64b`  
		Last Modified: Wed, 07 Aug 2024 02:03:04 GMT  
		Size: 8.6 MB (8595116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990367033b44e8f743da6c9cbd0fa79ff1de169204b78efa1f1cc3def9813bc9`  
		Last Modified: Wed, 07 Aug 2024 02:03:04 GMT  
		Size: 41.6 KB (41637 bytes)  
		MIME: application/vnd.in-toto+json
