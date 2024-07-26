## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:cdcfa4e29ead3ffb8de480533e33c0167b0dd71fad6da053e8dfccdbe3b88b2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:db19f688581a2f9c70e879c1af2e0a73f642082b3166eb0bf4221d4360e16957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.6 MB (576616750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acba177242e7d7285ab63d8fef25e184f55805af0fbb4745a805f8d93aba2513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 26 Jun 2024 09:06:21 GMT
ARG RELEASE
# Wed, 26 Jun 2024 09:06:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 26 Jun 2024 09:06:21 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Wed, 26 Jun 2024 09:06:21 GMT
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_VERSION=16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=0997ff4cfe16928996218963fad74d7a564c1aa75c7e8434e7cd25bd471ecd5a
# Wed, 26 Jun 2024 09:06:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_VERSION=3.4.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_SHA256=d83970dcda3198ca480e59b38e9e7055df09833e40d898c8ec5778a1e767f93b
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.0.jar
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.0.jar
# Wed, 26 Jun 2024 09:06:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f05e0c470fe19918a4af17eda4c3c834422ca9ed93b2de24950e8aad0a0fff`  
		Last Modified: Thu, 25 Jul 2024 20:08:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdb07bfe42a20f2cd030c81fa9ad17c22dd69661de1b765db64b564c9d0953c`  
		Last Modified: Thu, 25 Jul 2024 20:08:45 GMT  
		Size: 12.4 MB (12442381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f193b178fdc20c06503220f2d211fc9970df5681afb5f3eaa7538f61e0811e6`  
		Last Modified: Thu, 25 Jul 2024 20:08:45 GMT  
		Size: 217.8 KB (217846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e799d0d37242b2191b490af006f53c21f624596c7233b40eb269ca9f6edfd96`  
		Last Modified: Thu, 25 Jul 2024 21:03:07 GMT  
		Size: 178.4 MB (178444229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f0ebc2943e63940715bff95df7b9dbe245a3dcb9d32e045596376f9cc16df3`  
		Last Modified: Thu, 25 Jul 2024 21:03:13 GMT  
		Size: 294.3 MB (294265713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2323adc505f58937b82ccc71016fac7b7b1645401e31854abe01afc6ce25e111`  
		Last Modified: Thu, 25 Jul 2024 21:03:04 GMT  
		Size: 640.6 KB (640644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6157fed603d40fd0ef92f3715673800bf240e207d42877fb5436a88aef2625`  
		Last Modified: Thu, 25 Jul 2024 21:03:04 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86a8e5de3d5d71aebf562e3c2f392ce8d75cbda5575f310363db218483669e4`  
		Last Modified: Thu, 25 Jul 2024 21:03:05 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bca501993ba7e44666d8853714a1d4f4b7ee4c7060c291694e3e148fbf5570`  
		Last Modified: Thu, 25 Jul 2024 21:03:05 GMT  
		Size: 6.5 KB (6526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d83f3d3f049bbd4eca444592c55d57d30964ca4c7485ec54b7197aef0f1bee`  
		Last Modified: Thu, 25 Jul 2024 21:03:06 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:6935cf80df622db7084f3fe859ad2649a10b1d60c5f6baa6ec2d1c37fc82d7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9096548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03638088428fd4b0a600b11826dd05a3ce1d32e5532f535b5cc627a620f1ca17`

```dockerfile
```

-	Layers:
	-	`sha256:1e42e2573263bce5d785ec889bae5b573a36a08bda5358ea19db992c42706481`  
		Last Modified: Thu, 25 Jul 2024 21:03:05 GMT  
		Size: 9.1 MB (9055250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3272522f3e3dd8ab3a809c488a56afe16a5163c0a80bec01da20241a24a4d184`  
		Last Modified: Thu, 25 Jul 2024 21:03:04 GMT  
		Size: 41.3 KB (41298 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b0338defdb8c702d129c1e1ea068589201f80afcfbcab0362f9c955ea2db838a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.0 MB (569025048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace055d752778d04409d7908c5e851176c6b9793d538fae97473a7f8efb5a27c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 26 Jun 2024 09:06:21 GMT
ARG RELEASE
# Wed, 26 Jun 2024 09:06:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 26 Jun 2024 09:06:21 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Wed, 26 Jun 2024 09:06:21 GMT
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_VERSION=16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=0997ff4cfe16928996218963fad74d7a564c1aa75c7e8434e7cd25bd471ecd5a
# Wed, 26 Jun 2024 09:06:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_VERSION=3.4.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_SHA256=d83970dcda3198ca480e59b38e9e7055df09833e40d898c8ec5778a1e767f93b
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.0.jar
# Wed, 26 Jun 2024 09:06:21 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.0.jar
# Wed, 26 Jun 2024 09:06:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3111de98c20040058bea11c27a5e778456de5a7ddfd95d12181ae4e957d00f`  
		Last Modified: Fri, 26 Jul 2024 02:21:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e06e0924efe8009d39115128b6ae083770ee28f8e31da8ca1414a54e65fa20`  
		Last Modified: Fri, 26 Jul 2024 02:22:27 GMT  
		Size: 12.4 MB (12448777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c670c389695106d88747dd0c5a114b40d724869dff39c8f3b76b6116e258a2`  
		Last Modified: Fri, 26 Jul 2024 02:22:26 GMT  
		Size: 216.8 KB (216777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c3101dbce77e8ae0799c890839e887b4f0d5f3eb029648034e35144160ce31`  
		Last Modified: Fri, 26 Jul 2024 03:13:04 GMT  
		Size: 173.5 MB (173477887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909b967a0901a6b4ea14eb376fde160fbfb8fa9232af77ed8fb5a260b1ddaaa0`  
		Last Modified: Fri, 26 Jul 2024 03:13:07 GMT  
		Size: 294.3 MB (294265650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d7c2b5caa3935d0637009c89c15b9a1860574808f2330b4981d505254f5a59`  
		Last Modified: Fri, 26 Jul 2024 03:15:38 GMT  
		Size: 640.7 KB (640652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c2fc03198e5889ecaa8fc7fda9a54a6c4b33e0b27101f9a4121674db821097`  
		Last Modified: Fri, 26 Jul 2024 03:15:38 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af681a93b8f2cb2dedf8f2aa0649f82afde977a3334b8879f5673f01484f5bb`  
		Last Modified: Fri, 26 Jul 2024 03:15:38 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de4b231dc77aa8481d059acfd54e796687fc7b118b3efb8ae495a981243883a`  
		Last Modified: Fri, 26 Jul 2024 03:15:38 GMT  
		Size: 6.5 KB (6529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c573922458006e6c54688adfbd6d6ab2dcc43d7dc31516be386dac3dc10a25ef`  
		Last Modified: Fri, 26 Jul 2024 03:15:39 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:bf398e32ef8570778b89318d3039ac17301ac35274b97334ff156960950a10df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9097771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bea26d53fbd25c34c4e363bccb367f92516429681de3aebb1fda03cf1cb5701`

```dockerfile
```

-	Layers:
	-	`sha256:768efe9deb2f3303c3e023c7d3feab93a5560e4037e8baec7f527bd39a02d018`  
		Last Modified: Fri, 26 Jul 2024 03:15:38 GMT  
		Size: 9.1 MB (9055824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336b1d723e188b114b2f7bc0c2d409bfa2a956c55c3a9b6e543efc950f181e31`  
		Last Modified: Fri, 26 Jul 2024 03:15:38 GMT  
		Size: 41.9 KB (41947 bytes)  
		MIME: application/vnd.in-toto+json
