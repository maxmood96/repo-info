## `xwiki:15-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:d7d02a65876b9121baed5507952fe149ad6c20dd948b89280008c74b6c747768
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b84d2d41aa46154627cb63707ab46e6a74b482ed921d1eb490e3fbb824833771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.7 MB (609652242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdc93e42bee031d1ca84d180bfa9d85aa5cb224b1682282d08b1acf4d4e7768`
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
# Tue, 03 Sep 2024 05:14:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Sep 2024 05:14:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 05:14:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Sep 2024 05:14:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Sep 2024 05:14:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 03 Sep 2024 05:14:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Sep 2024 05:14:18 GMT
ENTRYPOINT []
# Tue, 03 Sep 2024 05:14:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 03 Sep 2024 05:14:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_VERSION=15.10.12
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.12
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=bf9658d49dd1cb1735864f09b88d19b9b26a3df5d3fe73a003e2171fa07e327c
# Tue, 03 Sep 2024 05:14:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_VERSION=3.4.1
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_SHA256=f60e4b282f1f4bdb74f0a26436ba7078a5e480b6f6702f6a7b45d9ba5e604a24
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.1
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.1.jar
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.1.jar
# Tue, 03 Sep 2024 05:14:18 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 03 Sep 2024 05:14:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 05:14:18 GMT
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
	-	`sha256:c4728163afb9187d5750e424b7036f35e635b66717860195905890b50c67fd7f`  
		Last Modified: Wed, 18 Sep 2024 00:01:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b576bb465706f666c66c57588b72e514e874967edb392a5d1c381a309e79e5a`  
		Last Modified: Wed, 18 Sep 2024 00:01:27 GMT  
		Size: 13.4 MB (13378031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ddd183b95c46d915fe5d8cfa463c94d78600b6e2e7bc570693a947caf044ab`  
		Last Modified: Wed, 18 Sep 2024 00:01:26 GMT  
		Size: 212.3 KB (212297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d0157ddd654a5d31a02cb9ebd8646e5ae2799b014a3a066ecd00d271349846`  
		Last Modified: Wed, 18 Sep 2024 00:52:47 GMT  
		Size: 194.3 MB (194322301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299707dfa657995236aade80e2dfc7463ff7cc1e34289fceaf024314e66b67aa`  
		Last Modified: Wed, 18 Sep 2024 00:52:49 GMT  
		Size: 307.0 MB (307006976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921472573f6fe5beea4881a492b2ed6e09bd3c8e596551651da787ea4c0859d3`  
		Last Modified: Wed, 18 Sep 2024 00:52:45 GMT  
		Size: 648.5 KB (648528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24056ebaea464c1c934e766a6cccddaedf1995206b2a581f30ecd4d47248ba7d`  
		Last Modified: Wed, 18 Sep 2024 00:52:45 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5f93b145420d07eb9dc9bec43422fe515ee54d64590f267008ae04c9ab0bae`  
		Last Modified: Wed, 18 Sep 2024 00:52:46 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6092da8ae15497da62c02624f4460e18191ee443021066eaf2cb7470482d4ed5`  
		Last Modified: Wed, 18 Sep 2024 00:52:46 GMT  
		Size: 6.5 KB (6464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad8da7816ec732d2f14bda62b4a194ceb99c0de00ff6642104e1889a0220235`  
		Last Modified: Wed, 18 Sep 2024 00:52:46 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:e395d05f5c11f88a91872f23255c11aa697dfb2f58de30da5bfb22e2afbf2611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8638147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55af7f9037cf8f2aa9d85e693ebf28e7ca2175f0d8236028b44e11d5fa679aca`

```dockerfile
```

-	Layers:
	-	`sha256:cd213ed99144ef7a857ee07195dee47c5e25abc1e254dd581907fa198382aedb`  
		Last Modified: Wed, 18 Sep 2024 00:52:45 GMT  
		Size: 8.6 MB (8597157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8afb024ae33586d4d83bf095130e5ab5c3f307c832a326a1c21c38db1f12a4e`  
		Last Modified: Wed, 18 Sep 2024 00:52:45 GMT  
		Size: 41.0 KB (40990 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:357c334da2283a1ce440f7200f79094ae5fe1fe1319d1a170468d6f3bff490f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.9 MB (605947767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163ff2ce40c84813d942b1edd6816c082bd3e1cd9722c0c6313f1347ac0d39e0`
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
# Tue, 03 Sep 2024 05:14:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Sep 2024 05:14:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 05:14:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Sep 2024 05:14:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Sep 2024 05:14:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 03 Sep 2024 05:14:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Sep 2024 05:14:18 GMT
ENTRYPOINT []
# Tue, 03 Sep 2024 05:14:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 03 Sep 2024 05:14:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_VERSION=15.10.12
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.12
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=bf9658d49dd1cb1735864f09b88d19b9b26a3df5d3fe73a003e2171fa07e327c
# Tue, 03 Sep 2024 05:14:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_VERSION=3.4.1
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_SHA256=f60e4b282f1f4bdb74f0a26436ba7078a5e480b6f6702f6a7b45d9ba5e604a24
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.1
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.1.jar
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.1.jar
# Tue, 03 Sep 2024 05:14:18 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 03 Sep 2024 05:14:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 05:14:18 GMT
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
	-	`sha256:baac26d95b31ca8518f3c7bdbe63cdd4169865021fbe03c49e5f8a983c90f962`  
		Last Modified: Wed, 18 Sep 2024 02:09:01 GMT  
		Size: 13.4 MB (13386829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0724226eed5f20e24828f190b427ea98df49c5ed0539d0e9639b85594daa2c`  
		Last Modified: Wed, 18 Sep 2024 02:09:01 GMT  
		Size: 212.2 KB (212168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26d15b9f3691e6a28febd11ad81e6aec17a84befa87e777e473c6156634960`  
		Last Modified: Wed, 18 Sep 2024 02:52:14 GMT  
		Size: 192.0 MB (191967705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c63de6dc99f5a2d3311b7009619fe174656053cfab67887d8a3ea3b8421a`  
		Last Modified: Wed, 18 Sep 2024 02:55:02 GMT  
		Size: 307.0 MB (307006946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caea74df31dd35bcdb49812f08caa72ff1426f6bbfc93c9f34c17077315b723e`  
		Last Modified: Wed, 18 Sep 2024 02:56:22 GMT  
		Size: 648.5 KB (648530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1be8f6564fd3785736a7523a3e72cedf776e1e21e79d49cde01e256604868d7`  
		Last Modified: Wed, 18 Sep 2024 02:56:21 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c20819ef993ab24303d724fcaea052528c357378c5b90ec04f5d748a6fd8f`  
		Last Modified: Wed, 18 Sep 2024 02:56:21 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0527e2bae2da9d0823a93fc0d876401d7a3ac9072a3ead4e80e0071f4bdc675d`  
		Last Modified: Wed, 18 Sep 2024 02:56:21 GMT  
		Size: 6.5 KB (6463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d153f992f313cc02a36657982ca250131ad0feee814afc6ae559b9bddb0d4476`  
		Last Modified: Wed, 18 Sep 2024 02:56:22 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:93564e26f225ccd79816636400bce2cdd1bcc74906650d294e3e77229c7be7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8640145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8956b5b79585e36bc3f5ad36575ae2d0d219eecdf6f49e79299d308b302e168`

```dockerfile
```

-	Layers:
	-	`sha256:b4fc8c609657581d410d97bbf103cd2cba9db6bdb84653074e9f2155b26f8ded`  
		Last Modified: Wed, 18 Sep 2024 02:56:22 GMT  
		Size: 8.6 MB (8598516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9650ce24b1f42c06925ff76e0a0d2b88db64cbaee1c403e4e04762605601abfa`  
		Last Modified: Wed, 18 Sep 2024 02:56:21 GMT  
		Size: 41.6 KB (41629 bytes)  
		MIME: application/vnd.in-toto+json
