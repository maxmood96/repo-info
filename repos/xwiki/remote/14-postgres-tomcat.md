## `xwiki:14-postgres-tomcat`

```console
$ docker pull xwiki@sha256:0652c4c56e572b448f49b602ac95765b66444faa37ddc628e5dee093dfd6de8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:14-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:51cd114755045e2df51915a40a08076fd51ea6b303762e9e0d8a1c1216981569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.9 MB (609891105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e2dd5c09a51e0fb4fe6d96fc1ce0e34348e4059ab5538f6489eefffdea8776`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.94
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Tue, 13 Feb 2024 09:10:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a316f85472e42ddf39be81d37cefcaa87cad98b7ca1710864ef2b8e67e9713b`  
		Last Modified: Tue, 17 Sep 2024 01:07:39 GMT  
		Size: 16.2 MB (16177262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc61f93074679710412ad3cef2fc06379271ccc3fe6224c6048a7940bcd3e31`  
		Last Modified: Tue, 17 Sep 2024 01:10:41 GMT  
		Size: 47.3 MB (47280241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40a8ba9b9816e6e92a048771912e0203fb0c2366490934aebed10ad169c831`  
		Last Modified: Tue, 17 Sep 2024 01:10:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b1b7b9b07ec925dc69ff02361ed98cf596d711625c013abe78af64e96f6d36`  
		Last Modified: Tue, 17 Sep 2024 01:10:35 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74c7748f81e9957dece0791d7ffe42e5baebbcf83496f1e16d3e2d81654ec5`  
		Last Modified: Tue, 17 Sep 2024 03:02:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43994888b2baf451c32ae192b6f75007e0b596af9dd1278a4b828a2d8d6df3e`  
		Last Modified: Tue, 17 Sep 2024 03:02:30 GMT  
		Size: 12.8 MB (12752965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75ee5c1849cbd8ac35d037a2528aa988f0c255d4bba411f8767957b5d280c0e`  
		Last Modified: Tue, 17 Sep 2024 03:02:30 GMT  
		Size: 212.3 KB (212282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a204a8da0e2b56f17cad74a8cd7b97204d9ccffafa9bac184510dc4b2cbd4b8b`  
		Last Modified: Tue, 17 Sep 2024 03:57:31 GMT  
		Size: 195.3 MB (195314214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2261a2e3f5a3dc4620a1136e623b2e66d8c3ae503a7f0eb78a1da01945ed8148`  
		Last Modified: Tue, 17 Sep 2024 03:57:32 GMT  
		Size: 306.5 MB (306538757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1412e95c6b23b0afa99c56810ebc2ee1524b1aaf38be5b3ddb19f5ff58d57462`  
		Last Modified: Tue, 17 Sep 2024 03:57:28 GMT  
		Size: 989.0 KB (988987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d81f451e5a9a5b253835cd13ee35cc2c49f8c1a32f65975114416cf9f5523ac`  
		Last Modified: Tue, 17 Sep 2024 03:57:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8c356de64e7f679f8a742e3f5a81b9b6e4fc161ae73eed9894c6ffa9592ba1`  
		Last Modified: Tue, 17 Sep 2024 03:57:29 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732a07d68269d6518666559de711cadc80ad5a46ffd88c710c6a6cd2a4a71736`  
		Last Modified: Tue, 17 Sep 2024 03:57:29 GMT  
		Size: 6.1 KB (6137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583b9a7c17889a11e7ddfa5c82aaed029962367e0123b709fe7f19b19cea87d`  
		Last Modified: Tue, 17 Sep 2024 03:57:29 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:d8ac2fc725281cd1f972575ff75fb5631e730b2553d426597efa07a636d520f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8630881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ae50ff3d67cefbef28997d149fd0786cf9eb39f4aa35f8e454bd74ef9a3ef1`

```dockerfile
```

-	Layers:
	-	`sha256:68151b2fec94132e6c409a06da797112516d2cd0d5564168a7a99a39a72ee14b`  
		Last Modified: Tue, 17 Sep 2024 03:57:28 GMT  
		Size: 8.6 MB (8592126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abea40ddfbbb02d219b48490bff3ea9fd58a8d6c2acaef30ea95415a20e31874`  
		Last Modified: Tue, 17 Sep 2024 03:57:28 GMT  
		Size: 38.8 KB (38755 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:14-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ecf53cdc69e25a184712a3fa3026f3b4f8b01ca966f274c47a23c96542ef81e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.2 MB (606192001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a203ddb04efeb9253ddb9c9ff249298c2f281cacdf7e040d5be16f10731a0f7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.94
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Tue, 13 Feb 2024 09:10:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10c682b9856cc71f6540269cbf6510c4d5c4b07d334875eb836c645d4cd40c`  
		Last Modified: Tue, 17 Sep 2024 01:37:44 GMT  
		Size: 16.0 MB (16010924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5717cce9082839b9cfb5f9b7614bc727f29f41b61f4f2feaaf9d55458acf33a`  
		Last Modified: Tue, 17 Sep 2024 01:40:18 GMT  
		Size: 46.7 MB (46746410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abec6865e9dddd9444d0e2eca0f0eb03af187efef87b0481c225769487e02a5b`  
		Last Modified: Tue, 17 Sep 2024 01:40:13 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f03107128f2014deac55fbb63e2c5001daf5fc478434cc12956f8b3e6e9fc7`  
		Last Modified: Tue, 17 Sep 2024 01:40:13 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3985e20664facef15e0968e68c03e74f1f65a521d1bc9c483dc6b33cfd1f99`  
		Last Modified: Tue, 17 Sep 2024 09:57:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882665212796c77e28caa72810efe39c3614d30d5625e724cf72d8bc8d76f1c1`  
		Last Modified: Tue, 17 Sep 2024 10:00:33 GMT  
		Size: 12.8 MB (12763962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c4fa6ae8d3e0dc53e0a7214dc2b4dccba5975586f242228209c79082c803f3`  
		Last Modified: Tue, 17 Sep 2024 10:00:33 GMT  
		Size: 212.2 KB (212161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868d7b8be0335ed53d889d623c76627c8e98de928d7e7469adc79938d2d1f77a`  
		Last Modified: Tue, 17 Sep 2024 11:03:30 GMT  
		Size: 193.0 MB (192962747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d95581214fcbd3047017439925969e92b245d8af146a36828cc0f5e7affe`  
		Last Modified: Tue, 17 Sep 2024 11:03:32 GMT  
		Size: 306.5 MB (306538754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea907ca0c863fea35fe37aa736e1e66e943a224b7e698bde67e5fcd657bb31ba`  
		Last Modified: Tue, 17 Sep 2024 11:03:26 GMT  
		Size: 989.0 KB (988992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ff4d39c8219eebce8e0fdd6e055e5e0c59ae80e1b386a664c8b77e9241cca2`  
		Last Modified: Tue, 17 Sep 2024 11:03:25 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf882ba117daa985c18f3587f1f62f345e789481f8abe4401c20ce505483bf8`  
		Last Modified: Tue, 17 Sep 2024 11:03:26 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf524b707485866de4c7f728f776d54d7316565847aca318eb8eb8ccbc4e6df`  
		Last Modified: Tue, 17 Sep 2024 11:03:27 GMT  
		Size: 6.1 KB (6137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476508c382bde1aa6a52482c1c6d10ff6186443b074b882a814f950e8d15cf24`  
		Last Modified: Tue, 17 Sep 2024 11:03:27 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:9523cd2b706ae14fa73be717a02811926b9024e77f5d2f4ee9064493bbb821f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8632830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a608f3831f6fb69426cd69f46652bb447f65eca4f945efc1c53783dd20caeb5`

```dockerfile
```

-	Layers:
	-	`sha256:77b19380a34370323dad8c8e6db246d6e116376eb55a57009a8def7bc43b9ab2`  
		Last Modified: Tue, 17 Sep 2024 11:03:26 GMT  
		Size: 8.6 MB (8593461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411e844250ff2b9b19799d7c1ddf4802462b00da8cb7c7d8d822cf65723e4032`  
		Last Modified: Tue, 17 Sep 2024 11:03:25 GMT  
		Size: 39.4 KB (39369 bytes)  
		MIME: application/vnd.in-toto+json
