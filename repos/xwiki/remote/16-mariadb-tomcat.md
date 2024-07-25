## `xwiki:16-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:40ec71f498b9ec9ba4245e291dbc24bed979a4aaca7706e3bece5c6a99e46632
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:e1b5da862e7d192cf201fe45d7b43ce3ac3a3dc182c68fc953b9ed42ed9d2065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.6 MB (576615898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435af71ced5d85bdc7cc7d4cd642a0aa14fd8eb8bc66cd54d24d99728b6dc88c`
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
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccc9be229b8d310bdbc0c56be88a51fcc3fef5ae00018e0fd6bf858815b580f`  
		Last Modified: Tue, 23 Jul 2024 03:03:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53291f71fa4fa224a3226b40732d633057bff07aa88b9abc039444330c5ae954`  
		Last Modified: Tue, 23 Jul 2024 03:03:43 GMT  
		Size: 12.4 MB (12442361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88315142089f582df33ea249461d313af8d5e3fc61ea8bd3f487cd8915c3aa3d`  
		Last Modified: Tue, 23 Jul 2024 03:03:43 GMT  
		Size: 217.8 KB (217820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f71dc22b451cee2bd26d9aec4b3ef23846670a9bca42372e874e9c70d99e022`  
		Last Modified: Tue, 23 Jul 2024 06:13:35 GMT  
		Size: 178.4 MB (178443844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6632731fc979be48842f1b1aa3696fedfdee24ed99569bfb8f53edde60073b`  
		Last Modified: Tue, 23 Jul 2024 06:13:38 GMT  
		Size: 294.3 MB (294265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e4977ca202156616e312fffd7c4d2979ac7eef39cc86351d24afee099678e8`  
		Last Modified: Tue, 23 Jul 2024 06:13:31 GMT  
		Size: 640.6 KB (640643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c8cce5bb65539a66ceea39afdd6b9fe67b4078054795980dc42f42f1c54975`  
		Last Modified: Tue, 23 Jul 2024 06:13:31 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ad331e6cefe0f2298b98591e89633e76e356b258306375943cf54321f750b8`  
		Last Modified: Tue, 23 Jul 2024 06:13:32 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a5e69d0788b6a61f714a596c797d3682153e85e337a07f24ed5b4b09d169d5`  
		Last Modified: Tue, 23 Jul 2024 06:13:32 GMT  
		Size: 6.5 KB (6525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b214fda5dc8c33fb0900358382e1691d63f94c96ca4d4e94a7ba999349970`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:93ad38ef17860ba42845beee3edc5ce5793bb93b0eaa622cd10ce8a55b522c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9096548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d6b7e443b2e53181d7a015b4ad41e056d9fc70d4fb3ad5860becb133f85972`

```dockerfile
```

-	Layers:
	-	`sha256:24b4fd131fa4aa01e8ad349919a30635d8c53e353f42a6cbc220613bf98e322f`  
		Last Modified: Tue, 23 Jul 2024 06:13:31 GMT  
		Size: 9.1 MB (9055250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54abfe176b2508b6af081a62351a388f8ee1b33e5737ed2a66eced6324d6a3b2`  
		Last Modified: Tue, 23 Jul 2024 06:13:30 GMT  
		Size: 41.3 KB (41298 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:4bd18150d75a45b9ea04b3e4a15efa7c1fc112fe814bc6e82e77856b6f7537e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.0 MB (569024890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff1edb03e5f4ed1d168ba9e6c643192e7a60b2ab311020133e40a766e01ab55`
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
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bdf074211340aa0bb9e65f26324e0e9f0596e54d686991659e80e2234ac9cd`  
		Last Modified: Wed, 24 Jul 2024 18:04:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0f5e661e4a148b41bbe0330eab98b55075266a33d54d8e2246670c3a3254f0`  
		Last Modified: Wed, 24 Jul 2024 18:05:36 GMT  
		Size: 12.4 MB (12448789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4868e7292dd856872221725229694f0781b8ccceda4f1196e0be7a3cb52ec56c`  
		Last Modified: Wed, 24 Jul 2024 18:05:36 GMT  
		Size: 216.8 KB (216812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b64f5226088952f4f76821445906f138be63ee8e8639df9a3c458fde3c9307`  
		Last Modified: Wed, 24 Jul 2024 19:42:11 GMT  
		Size: 173.5 MB (173478123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0411c2404f52dcf7ab426a9bfbf948d8d0a0515ec967c61edc9d7d03c4bdfa`  
		Last Modified: Wed, 24 Jul 2024 19:42:30 GMT  
		Size: 294.3 MB (294265634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9f70da4611a33dcd4b9b3a9de2fcca4a945035623e4ac319ce0c578a83f41f`  
		Last Modified: Wed, 24 Jul 2024 19:44:56 GMT  
		Size: 640.7 KB (640651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39a5935208bddab2874c1951e2d209c1ff2448e77a6c49c103a3920a65ec871`  
		Last Modified: Wed, 24 Jul 2024 19:44:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72e5feb132486a3656293be5d6d343158b6ffee0ef5f9b51e5ac02d0d04e0b4`  
		Last Modified: Wed, 24 Jul 2024 19:44:56 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4b7ce3650a287ea44801cf8d8db844f0b5d195e500df7dfc22201c8d4d95d6`  
		Last Modified: Wed, 24 Jul 2024 19:44:56 GMT  
		Size: 6.5 KB (6529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee84d963dd797be89b043031c7f8c032faeeae00bdcef0ff22fd754f72e10b2`  
		Last Modified: Wed, 24 Jul 2024 19:44:56 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:e439ef85d739e1f5aa12f096902e999a9757a09a10fb8716c2a24edeb14a775d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9097771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2146f33ed9e38848a840c154cb465b727618c6090ddc75b55bbcd31523cdc610`

```dockerfile
```

-	Layers:
	-	`sha256:f52c23f4292cfd26c5cca52042e732554169d528f20e76321f2fc65320d4c4f5`  
		Last Modified: Wed, 24 Jul 2024 19:44:56 GMT  
		Size: 9.1 MB (9055824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:355877b665be3cedc0a9e2b6321e1d42d892f91b8a29159ebfafee6dcc9adc7f`  
		Last Modified: Wed, 24 Jul 2024 19:44:55 GMT  
		Size: 41.9 KB (41947 bytes)  
		MIME: application/vnd.in-toto+json
