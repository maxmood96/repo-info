## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:3005f31a351a266374b6808f7462d2a7cd63ba939992428ca4bd0ab116c0b6ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:c67ac7878db346f8f00b71b210ec090eef3b7ac45b835cffa520401a204e207a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.4 MB (609392383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686df944bfd1cebd8ee0b3e0c36306c4b4b243eefd4b165fda3778f00e34cf56`
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
ENV TOMCAT_VERSION=9.0.94
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
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
ENV POSTGRES_JDBC_VERSION=42.7.4
# Tue, 03 Sep 2024 05:14:18 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Tue, 03 Sep 2024 05:14:18 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Tue, 03 Sep 2024 05:14:18 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Tue, 03 Sep 2024 05:14:18 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Tue, 03 Sep 2024 05:14:18 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:0ca156f4a2c920b86442db36a671b2e5c8afe6469740cf050fa67def089553d7`  
		Last Modified: Tue, 17 Sep 2024 03:57:27 GMT  
		Size: 194.3 MB (194322298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3231f808cb2860eca737057c6ec2e6465dbd9332a99b6a197abd07d7db22270`  
		Last Modified: Tue, 17 Sep 2024 03:57:30 GMT  
		Size: 307.0 MB (307006983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03362a70b9a08ec5e739f6b93e638f59e5779bdcaf183964a975c478a36b197a`  
		Last Modified: Tue, 17 Sep 2024 03:57:23 GMT  
		Size: 1.0 MB (1013641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115cb13b9f48e56d077c35f62d8ff1e8863c490628b28107b38125cc062d2f05`  
		Last Modified: Tue, 17 Sep 2024 03:57:23 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8fc74e35a78e45f49ae5572d40071039445c30bc776f627fb310a6a06dd79`  
		Last Modified: Tue, 17 Sep 2024 03:57:24 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b36c3ef7c796e6be5e1bd4aaa36e5be51627cad695e3570270a4daf96080f51`  
		Last Modified: Tue, 17 Sep 2024 03:57:24 GMT  
		Size: 6.5 KB (6465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7996e31e7387ce303a09df34abf756da9fe730919501fc562f0839ce684c9fab`  
		Last Modified: Tue, 17 Sep 2024 03:57:25 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b5960a1d423a54da2e82333a8f2e9f87933e5afb5a54a8e9d9cd9cf77c16575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ea70f7789573476b775ec6da08cf9a82a2762707f641a89fbde4cbed8b5492`

```dockerfile
```

-	Layers:
	-	`sha256:9c84a56003fbb44189cc747cca6f40233e57c28c623f2e0c8a40fe99984e1045`  
		Last Modified: Tue, 17 Sep 2024 03:57:22 GMT  
		Size: 2.7 KB (2651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb28d62599c0970c87371200e70348703673de448a588e7a3e80fbc640296643`  
		Last Modified: Tue, 17 Sep 2024 03:57:22 GMT  
		Size: 41.0 KB (40967 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0bbfc11958cc797fd6f0ab309a8fdf9734582eb9b851098e21ff66a377c4ae0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.7 MB (605690634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb41aa988ce33107a46db0a566c107c749e52a106f389535aef3b066850ffc9c`
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
ENV TOMCAT_VERSION=9.0.94
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
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
ENV POSTGRES_JDBC_VERSION=42.7.4
# Tue, 03 Sep 2024 05:14:18 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Tue, 03 Sep 2024 05:14:18 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Tue, 03 Sep 2024 05:14:18 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Tue, 03 Sep 2024 05:14:18 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Tue, 03 Sep 2024 05:14:18 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:76ceb0797bdbc663865edbc8452497a66d7b77bb203175c4668194a5d47ff886`  
		Last Modified: Tue, 17 Sep 2024 10:56:05 GMT  
		Size: 307.0 MB (307006917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f307adb5d914fc8b86ebc9f13d6aa555bb2698c1575d13c456c11e6031ddd581`  
		Last Modified: Tue, 17 Sep 2024 10:56:48 GMT  
		Size: 1.0 MB (1013638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdf15cd4d6f7b4d81ab03436c3185aeecddaf6538dfef026c3ba319dbd4e28b`  
		Last Modified: Tue, 17 Sep 2024 10:56:48 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170b614b8f01f187830e3fdba68055478e0bd3f8c06f2c8322a21229e1f7f16b`  
		Last Modified: Tue, 17 Sep 2024 10:56:48 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0708774037da3d0810d5438739cc0f82106edaf38e9bebbc8a1647aaf6c8893b`  
		Last Modified: Tue, 17 Sep 2024 10:56:49 GMT  
		Size: 6.5 KB (6460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2abe01d7622edbf4a39d2d57cf4b2d42e5139b78e54b62b56206a933b1e279c`  
		Last Modified: Tue, 17 Sep 2024 10:56:49 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:098f84b6548da1e14719b165a71b96e20653c1a6978ef3e7bb813e71ad4620ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8640101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3575c0a8a6c56b59072eb4b0ce974f1a3830fdec7b1c8bcdc5bc6689b2e15800`

```dockerfile
```

-	Layers:
	-	`sha256:c497ec0562939311fc9545c6b314b019d0f1c78f4374db928d37d26dd7bfb944`  
		Last Modified: Tue, 17 Sep 2024 10:56:48 GMT  
		Size: 8.6 MB (8598498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637600de10635e07d910efe5ea2998d2588712ece414e2ecd0d2b6e935f4d458`  
		Last Modified: Tue, 17 Sep 2024 10:56:47 GMT  
		Size: 41.6 KB (41603 bytes)  
		MIME: application/vnd.in-toto+json
