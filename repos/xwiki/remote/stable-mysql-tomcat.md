## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:e6f2cd0949ae35596dffeafbb8fcc740735a864f00aa6415a5f74ca188fae12a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:07b92d56d35747c2b05b341fd1f34a38480594101f4a42760de5d7309a728caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.2 MB (614194427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da693c62ef99f0669842bdb92e6f220e504a76e2b91729630ccf846d587a07c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 01 Oct 2024 13:05:18 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:05:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:05:18 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 01 Oct 2024 13:05:18 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:05:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 01 Oct 2024 13:05:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:05:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 01 Oct 2024 13:05:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 01 Oct 2024 13:05:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 01 Oct 2024 13:05:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT []
# Tue, 01 Oct 2024 13:05:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 01 Oct 2024 13:05:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_VERSION=16.8.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.8.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=7eca55bbe56a45f34b81e9884bb4f190af24306db3da9032c27126d3cf11f4f1
# Tue, 01 Oct 2024 13:05:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_VERSION=9.0.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_SHA256=a221c4106b7fe68a45912cdbf8351f1b43ad3c53a43c3bc966181cc14f86fa30
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.0.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.0.0.jar
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.0.0.jar
# Tue, 01 Oct 2024 13:05:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 13:05:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a5bfb8d4474120f18cd4e2e21c2fb6e7d9144d3bfb8f8fdf9016d706eebb88`  
		Last Modified: Fri, 11 Oct 2024 23:57:59 GMT  
		Size: 47.3 MB (47280244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14688e11a21ea2eaa960947d01105ba680fe07492d6eac637d88f964f9396719`  
		Last Modified: Fri, 11 Oct 2024 23:57:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057686f76905cbfe0bc06f7c1af90d04d9dd676958004abc9661ee80c48c23db`  
		Last Modified: Fri, 11 Oct 2024 23:57:53 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f8e1dc9ad840b7ff5db6a0455823fbc33ee9cd46410852b9a48a1860cc1e3a`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83a82029587f307c6cab896483c8e22068999617c22a3f5d8701ef0498e3ac3`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 13.4 MB (13374008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d6c6358d2334c88eef14624b92a02ce40a6d51cf8135b31b06a01c688974bc`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 212.9 KB (212918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70086adc348b90ada1c8d21b9cea8ebfce8f69e53631efb2944211e39a1d35ca`  
		Last Modified: Sat, 12 Oct 2024 02:54:28 GMT  
		Size: 194.7 MB (194659197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cef49df6e1686fe71aac4b49ee7cccc17151cbe5a5fac1e289d893c085cc77`  
		Last Modified: Sat, 12 Oct 2024 02:54:27 GMT  
		Size: 311.8 MB (311840794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a355cc7d42d3fae86b13e42b78f15097c71dd4c50d8518584c0e6705fd0cd9`  
		Last Modified: Sat, 12 Oct 2024 02:54:21 GMT  
		Size: 2.4 MB (2427528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e13328bdae95ba5b5e0c3e6b5a80cddddeed730ba5f26d46a2c6468de6825a2`  
		Last Modified: Sat, 12 Oct 2024 02:54:20 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed67cde0deea30e6b408459b64b019f38a49789c1e2ddcf88d9ee5b4e06906b`  
		Last Modified: Sat, 12 Oct 2024 02:54:21 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a24d5b866f416449e05c44a0ab1f35592b1820970c8e139facf7f6b054f75b`  
		Last Modified: Sat, 12 Oct 2024 02:54:22 GMT  
		Size: 6.6 KB (6560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b9ea28f203c0da8c9ca66cd7646a2cea6c6d6c73ea8e11a0a0086f58dd1fc2`  
		Last Modified: Sat, 12 Oct 2024 02:54:22 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:d7b58393dc2fd93399f65915411fa8fcb8ae26383f4ac3fac239b26356942134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8712417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66915f40b947986ec17c633dbf4679c06f626653fae0bd848cdb4cb2449d6240`

```dockerfile
```

-	Layers:
	-	`sha256:1435830c2525fdce2790626f9485a282e53fe9f2a862605de6c2620397e2f646`  
		Last Modified: Sat, 12 Oct 2024 02:54:21 GMT  
		Size: 8.7 MB (8669746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f5433298f4fe13fb82514b8ac59fd74924a26b2fbc0f5d745ff6d9e7ad73300`  
		Last Modified: Sat, 12 Oct 2024 02:54:20 GMT  
		Size: 42.7 KB (42671 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2965a93440de891b106d1973f88e32923e77546c7e1cb51e055243680603dbeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.7 MB (610691664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d6eb912f206f12ccb8e9f99582ee3689a4a663eb6d9434a3e4fdd25a556113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:05:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 01 Oct 2024 13:05:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:05:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 01 Oct 2024 13:05:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 01 Oct 2024 13:05:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 01 Oct 2024 13:05:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT []
# Tue, 01 Oct 2024 13:05:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 01 Oct 2024 13:05:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_VERSION=16.8.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.8.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=7eca55bbe56a45f34b81e9884bb4f190af24306db3da9032c27126d3cf11f4f1
# Tue, 01 Oct 2024 13:05:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_VERSION=9.0.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_SHA256=a221c4106b7fe68a45912cdbf8351f1b43ad3c53a43c3bc966181cc14f86fa30
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.0.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.0.0.jar
# Tue, 01 Oct 2024 13:05:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.0.0.jar
# Tue, 01 Oct 2024 13:05:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 13:05:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef2dea2cc9c0dbe3c64710e5ffdcfb21a0f8380212beac56d44e94e1a2802c`  
		Last Modified: Wed, 02 Oct 2024 01:28:02 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97ec3778b444f1bb64b53a5f58cb73e31648e1389c755d55b65d2c634c1cd2f`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f4ca8e8b83ad911aeec2a1f3687e6b549782de3f86048819e24bbc9604a9fd`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a048a6e5e950d28537247e59cee0c1b682511903da99d5f3a1e2674d985a8651`  
		Last Modified: Wed, 02 Oct 2024 07:53:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7157fedaaa56ad98d02439cf1b6a861c07b92f87328d36de94964d5a5b4153`  
		Last Modified: Wed, 09 Oct 2024 01:26:58 GMT  
		Size: 13.4 MB (13386543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f83cdf1ac7005f33b5e42c9ec66734a2fedcd6f93b757212dd61fa9a5a38d91`  
		Last Modified: Wed, 09 Oct 2024 01:26:58 GMT  
		Size: 212.2 KB (212216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f6a11738a4d7f591a1d541c49f36f1cc36f56b55f73e4731632db95c2eb283`  
		Last Modified: Wed, 09 Oct 2024 01:55:49 GMT  
		Size: 192.3 MB (192312275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a181ef7b7117043173c9d78b387871ec9086f90deaf0f7fa7235d10a9b7c2db8`  
		Last Modified: Wed, 09 Oct 2024 01:55:51 GMT  
		Size: 311.8 MB (311840723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1f134c160048dc98f8aa31a41ce53f1769b6101ce69391a32c7ece731f60ca`  
		Last Modified: Wed, 09 Oct 2024 01:55:45 GMT  
		Size: 2.4 MB (2427542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0c53d9aa43c48b4f7ba0d2f45957575cd3eb0527f6cd04f3ce3606ed6c33d9`  
		Last Modified: Wed, 09 Oct 2024 01:55:45 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd41a9cdb09b1ee9e8d49eb6cd97d4e4cf84bf589c991d58ae17d13801aa9c49`  
		Last Modified: Wed, 09 Oct 2024 01:55:46 GMT  
		Size: 2.4 KB (2374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c520c8a73fafe5def1f9a76343b8f2fb29bebcbe193a763112749587f45542c`  
		Last Modified: Wed, 09 Oct 2024 01:55:46 GMT  
		Size: 6.6 KB (6565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed855b918a8d5cefd0ead3ccea9902d5559a16782514a0c4f00a2a46b725a25`  
		Last Modified: Wed, 09 Oct 2024 01:55:47 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:5154d889a72eb670ba18e92882a5c4bffd2aee2c3b8c5c05aca256549ac48bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8262b1716cf45e372990697cf6ab99fb14f138c4c3e581813782157f8682fe`

```dockerfile
```

-	Layers:
	-	`sha256:2be4a10fd932556ca2397d4920ca903fa43a937fe8269e3a87bcbe1e08592e97`  
		Last Modified: Wed, 09 Oct 2024 01:55:45 GMT  
		Size: 8.7 MB (8670546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a1f393963fecc5c15cd87ffcbbc0112d685fd1d0d1acdd7f9484b1f7ff1994c`  
		Last Modified: Wed, 09 Oct 2024 01:55:44 GMT  
		Size: 43.1 KB (43111 bytes)  
		MIME: application/vnd.in-toto+json
