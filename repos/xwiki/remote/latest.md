## `xwiki:latest`

```console
$ docker pull xwiki@sha256:68a20c2bfa846af1cf3ea4453bb04c27c900ba87884025f00f1de7c1d7969a3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:0784e2e825fcce8149272bc69138430a1328804a7f66239a04bf859577b1546a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615295649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba8796065a143df8b13771d9a9ba52c262263f32088254b1dff62424fc26332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
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
# Thu, 05 Sep 2024 09:53:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Sep 2024 09:53:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 09:53:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Sep 2024 09:53:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Sep 2024 09:53:24 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_VERSION=9.0.94
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Thu, 05 Sep 2024 09:53:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Sep 2024 09:53:24 GMT
ENTRYPOINT []
# Thu, 05 Sep 2024 09:53:24 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 05 Sep 2024 09:53:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_VERSION=16.7.1
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.7.1
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_DOWNLOAD_SHA256=c1df8c9c0abd0f06fec4414202c25f1c0a48d810f0efe802deb633edf25090c0
# Thu, 05 Sep 2024 09:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_VERSION=9.0.0
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_SHA256=a221c4106b7fe68a45912cdbf8351f1b43ad3c53a43c3bc966181cc14f86fa30
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.0.0
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.0.0.jar
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.0.0.jar
# Thu, 05 Sep 2024 09:53:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
VOLUME [/usr/local/xwiki]
# Thu, 05 Sep 2024 09:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 09:53:24 GMT
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
	-	`sha256:5734b76ede6bbfbf10204abc21dfddced667743463470612d6199748fc082967`  
		Last Modified: Tue, 17 Sep 2024 03:57:28 GMT  
		Size: 194.3 MB (194322368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e904893550457b34f8d27d27de26f5cb31951614c25b446fd995726004b63ee0`  
		Last Modified: Tue, 17 Sep 2024 03:57:30 GMT  
		Size: 311.5 MB (311496184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd931a76761a266488d2a2cf7dd147be008659f00fde4c51715c18f06b4e8746`  
		Last Modified: Tue, 17 Sep 2024 03:57:26 GMT  
		Size: 2.4 MB (2427539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ddc7c31ecc22507345b0548a87ad249d80cdb84105cf48bd3e5ac5daf59c0c`  
		Last Modified: Tue, 17 Sep 2024 03:57:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe225eb61c0a2d27f9cd9014cbf98d15143ccd156817889f3451ed9e81cba5c`  
		Last Modified: Tue, 17 Sep 2024 03:57:26 GMT  
		Size: 2.4 KB (2374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8dff29f4cd82a6fec01decb6bb6fee40b6a26157ac599ee6f413c8544213ea`  
		Last Modified: Tue, 17 Sep 2024 03:57:27 GMT  
		Size: 6.6 KB (6562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75932b847e21e002df5f89927da3190bd65c75a624d14b9589b40645607863`  
		Last Modified: Tue, 17 Sep 2024 03:57:27 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:eb0ddd96bae8ccb2b8e5ef96f1c1526694a25f75286f43ff5b8ab05d279f0fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8645864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4986a6757b24bddcb663e6f19d9ec734d04966ba141405d236d2b48ed62d07`

```dockerfile
```

-	Layers:
	-	`sha256:366f72722bac72d3479bf1645594360c2916a40127d05b70fec4ab6fb62b346c`  
		Last Modified: Tue, 17 Sep 2024 03:57:26 GMT  
		Size: 8.6 MB (8603231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f0213f7841879a8f0cc4844a7ebef070e78ae2f0b2c2dc91c6fd5dda5f900a`  
		Last Modified: Tue, 17 Sep 2024 03:57:25 GMT  
		Size: 42.6 KB (42633 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:latest` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:04aa95d00714665bedd8689edad09ce4ee667fb583fbd76b3ec6a9b93a2b0765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.6 MB (611593871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fc48511667738c08299d838af8361b9a72ca1d4e3cc381bbe258c9e37e5a83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
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
# Thu, 05 Sep 2024 09:53:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Sep 2024 09:53:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 09:53:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Sep 2024 09:53:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Sep 2024 09:53:24 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_VERSION=9.0.94
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Thu, 05 Sep 2024 09:53:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Sep 2024 09:53:24 GMT
ENTRYPOINT []
# Thu, 05 Sep 2024 09:53:24 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 05 Sep 2024 09:53:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_VERSION=16.7.1
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.7.1
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_DOWNLOAD_SHA256=c1df8c9c0abd0f06fec4414202c25f1c0a48d810f0efe802deb633edf25090c0
# Thu, 05 Sep 2024 09:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_VERSION=9.0.0
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_SHA256=a221c4106b7fe68a45912cdbf8351f1b43ad3c53a43c3bc966181cc14f86fa30
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.0.0
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.0.0.jar
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.0.0.jar
# Thu, 05 Sep 2024 09:53:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
VOLUME [/usr/local/xwiki]
# Thu, 05 Sep 2024 09:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 09:53:24 GMT
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
	-	`sha256:5889730e909a56730e676ab97e52735ee462ebfaa7b90cac808eeef98a6f4045`  
		Last Modified: Tue, 17 Sep 2024 10:53:18 GMT  
		Size: 192.0 MB (191968273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6707fcbaf62884923617188f0df5581dcc3a0c50f214de2ad62d76e06e84f0b1`  
		Last Modified: Tue, 17 Sep 2024 10:53:22 GMT  
		Size: 311.5 MB (311496139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62f26ee38ba45f8bdae18aca62f393ce6e76e399cc3423406a030a0d1720c86`  
		Last Modified: Tue, 17 Sep 2024 10:53:14 GMT  
		Size: 2.4 MB (2427540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c6745b9c49dc8f33765b5a55b326b8fd2818d58d49fe3683dc4807b362a45`  
		Last Modified: Tue, 17 Sep 2024 10:53:14 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b03da369e9f678e9f2c4daf05677abfb059052eba3d61da77a858a3c1d35bc6`  
		Last Modified: Tue, 17 Sep 2024 10:53:15 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff792a615b3768ba1bb0a4994117683dc04d112a379ea3cde1e6559d5226cec`  
		Last Modified: Tue, 17 Sep 2024 10:53:15 GMT  
		Size: 6.6 KB (6560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804b013686db09fea84e94e210f95af5758c6f2504707bdb8579b0c6ed16c23`  
		Last Modified: Tue, 17 Sep 2024 10:53:16 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:1af9e62c4e4fbb14d208ed2888607b85646fbb2fa3e6ed7a3c39636b69680088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8648004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da210ec76c59cfa3580fbc3cf7269e71b1faa8ade36648d076ffdc9bddc77c4`

```dockerfile
```

-	Layers:
	-	`sha256:7512d9977147c80455e6c8a42e54e4ed9ee1a72bd53a4b28967adb848271fc08`  
		Last Modified: Tue, 17 Sep 2024 10:53:14 GMT  
		Size: 8.6 MB (8604662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc6d6da9b75263ee58ea0c6cdd3198a9ff67e7e177812285e302263a8b48c08`  
		Last Modified: Tue, 17 Sep 2024 10:53:13 GMT  
		Size: 43.3 KB (43342 bytes)  
		MIME: application/vnd.in-toto+json
