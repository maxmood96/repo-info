## `xwiki:lts`

```console
$ docker pull xwiki@sha256:0e9477888ce135ee3e42aa6187481d32a13da74e3e54313693a6b7177c924861
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:a71f1ce6b951a30ff051fe38d46e8c465ba14f7c6d280d97d66d4deaffd13aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.6 MB (595598412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efded61cd77b18d802ecd1ae79de2d8048b7b8381dff1313942bbc2cf1da8a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:16:34 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 17 Jan 2024 07:17:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 07:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 07:17:07 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 07:17:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 10:38:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 17 Jan 2024 10:38:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 10:38:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 17 Jan 2024 10:38:26 GMT
WORKDIR /usr/local/tomcat
# Wed, 17 Jan 2024 10:38:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 10:38:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 10:41:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 17 Jan 2024 10:41:00 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Jan 2024 10:41:00 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 17 Jan 2024 10:41:01 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 17 Jan 2024 10:41:01 GMT
COPY dir:f4f1ec0066f8e22dbe18e524bdaa66d22964d314d16b2d4878c80d7fb4e8eb25 in /usr/local/tomcat 
# Wed, 17 Jan 2024 10:41:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 10:41:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 17 Jan 2024 10:41:07 GMT
EXPOSE 8080
# Wed, 17 Jan 2024 10:41:07 GMT
ENTRYPOINT []
# Wed, 17 Jan 2024 10:41:08 GMT
CMD ["catalina.sh" "run"]
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 17 Jan 2024 13:37:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_VERSION=15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=3775334377ae7fb8bcf6a21e6eb099a8cfbea43044dc0716c01cb3b5117988a2
# Wed, 17 Jan 2024 13:37:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_VERSION=8.2.0
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_SHA256=06f14fbd664d0e382347489e66495ca27ab7e6c2e1d9969a496931736197465f
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.2.0
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.2.0.jar
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.2.0.jar
# Wed, 17 Jan 2024 13:37:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
VOLUME [/usr/local/xwiki]
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec70d9e863c2b918442abf26eb84b0afbc4a2c5dda1c34857c51955e26a803c3`  
		Last Modified: Wed, 17 Jan 2024 07:20:58 GMT  
		Size: 47.1 MB (47149289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680d0df58130ac2dc6ee238ad0275c9652892eda90a334fd3ce02eedf7147963`  
		Last Modified: Wed, 17 Jan 2024 07:20:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73eedc84985754d22cc59527bee6b3fc0a39558017abcf0fe7ae531123dc84e`  
		Last Modified: Wed, 17 Jan 2024 07:20:52 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d1e1efd368e72c389dbb275ecfcbab50b1947efee25f89197359ea37a0c84`  
		Last Modified: Wed, 17 Jan 2024 11:15:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde25073223ef7971200346ba07792a2cbc6d8eb5aa846f4305d6184d270ac39`  
		Last Modified: Wed, 17 Jan 2024 11:22:00 GMT  
		Size: 12.4 MB (12404679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cafa28ad9d6c49c386348766658cff0214270deb1a170d7247496e756df683`  
		Last Modified: Wed, 17 Jan 2024 11:22:00 GMT  
		Size: 458.5 KB (458531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf3288bc25ea454de10d0b24c9bd7bcd4adfe139a10bd0b647800ee3293228`  
		Last Modified: Wed, 17 Jan 2024 11:21:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07ef9a27ed52d447c98ae5e7b8fed7946e08db5a3d7f658f38d4e209266ede`  
		Last Modified: Wed, 17 Jan 2024 22:44:42 GMT  
		Size: 178.3 MB (178348906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00433a0c8e1a5f9a50aa7678b15438d3f6e440e2f92da65625e62f67220a538`  
		Last Modified: Wed, 17 Jan 2024 22:44:44 GMT  
		Size: 307.0 MB (306966986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95893b2a56aa3a2d64bbf89288ae981251c93ad39db10385c7f9941de70160b`  
		Last Modified: Wed, 17 Jan 2024 22:44:39 GMT  
		Size: 2.4 MB (2350957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee61029be5f7042bcb9c6a8de1c32a1728f6039d1313de8ecbd048d22cbb2942`  
		Last Modified: Wed, 17 Jan 2024 22:44:39 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1369a572c753d402c915ee18965eb5216fec4c20859a217df9c5a5c3f5ba52b1`  
		Last Modified: Wed, 17 Jan 2024 22:44:40 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796413ce5daf6c30dda245f7e8afec2fcf10506e3c4ecc6d09c778bab449c4a8`  
		Last Modified: Wed, 17 Jan 2024 22:44:40 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497312a1259bb8e58ea630bb43d70e975bea0a26ad1e43abb0e25cf849f5ddd7`  
		Last Modified: Wed, 17 Jan 2024 22:44:41 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:c4149636a6baf7f560aa9dc76afeb711c500a6a719c0a5f19b6e4efa4695f344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8083491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006d16024934aa44518ec572d5a022c53dce189d5f18272ac56c854113f456b0`

```dockerfile
```

-	Layers:
	-	`sha256:299f501eb8bdde1e110ab1058ec0dd8f522af3f545b3b95f0a9c3aaf03cc595b`  
		Last Modified: Wed, 17 Jan 2024 22:44:38 GMT  
		Size: 8.0 MB (8039574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a705c0729f642439c63304cd37c7a9d3f13fd4475ed2abec970a7b33fabbd8ef`  
		Last Modified: Wed, 17 Jan 2024 22:44:38 GMT  
		Size: 43.9 KB (43917 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0c6afb764cd8f94dea17fe72a24b9657529af6949998f1cd39f48f58dbc03ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589472001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0de3850ab447a18a1e053a252a24c8d44915c25048d4dea1ea37634ba585e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 06:59:06 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 17 Jan 2024 06:59:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 06:59:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 06:59:33 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 06:59:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 13:37:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 17 Jan 2024 13:37:13 GMT
WORKDIR /usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 17 Jan 2024 13:37:13 GMT
COPY dir:1c285ad99d5400a62c515d0edc8da9bc0491088e5993df30403cdd5d434fbc0a in /usr/local/tomcat 
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 17 Jan 2024 13:37:13 GMT
EXPOSE 8080
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT []
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 17 Jan 2024 13:37:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_VERSION=15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=3775334377ae7fb8bcf6a21e6eb099a8cfbea43044dc0716c01cb3b5117988a2
# Wed, 17 Jan 2024 13:37:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_VERSION=8.2.0
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_SHA256=06f14fbd664d0e382347489e66495ca27ab7e6c2e1d9969a496931736197465f
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.2.0
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.2.0.jar
# Wed, 17 Jan 2024 13:37:13 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.2.0.jar
# Wed, 17 Jan 2024 13:37:13 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
VOLUME [/usr/local/xwiki]
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40ddacc22778a98794779fd2342df132ad4c2fb4cbfc8863316d31fd435b197`  
		Last Modified: Wed, 17 Jan 2024 07:02:40 GMT  
		Size: 46.6 MB (46624031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa70867b319793d597ac109e4ab08a1640a03419c64b02fc2a0f83d3fab963`  
		Last Modified: Wed, 17 Jan 2024 07:02:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb574f7d99aeb3b3f52602da29bf978d23b304f4233a2ea5587d6ae88cbd66`  
		Last Modified: Wed, 17 Jan 2024 07:02:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676d321c3a16eda4a2f342361460b3290f1270e6f89a4d3dea4f3e1b6b504c2a`  
		Last Modified: Wed, 17 Jan 2024 14:36:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35964d9c82059bc828da4495b32b7a5b3a228340ebeb409b7774dd029e4001f9`  
		Last Modified: Wed, 17 Jan 2024 14:43:50 GMT  
		Size: 12.4 MB (12412598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5dd66eedef4831ca2d1805f0a4e47f36bf9bf1fd03bc06d2ff39484a65e7a9`  
		Last Modified: Wed, 17 Jan 2024 14:43:49 GMT  
		Size: 457.3 KB (457266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4081678f3e603cdbf87adcc472987711822b96a55a07e07e83d82695b4ccd`  
		Last Modified: Wed, 17 Jan 2024 14:43:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e771a6062b68520e7e7ae513dddd2b646de56809a72b94c54ebcf82514423cf`  
		Last Modified: Thu, 18 Jan 2024 11:32:05 GMT  
		Size: 173.4 MB (173386603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932aacebe0146724d847a8dbe061dd032878991c3ec952689ea059699ec1815f`  
		Last Modified: Thu, 18 Jan 2024 11:32:09 GMT  
		Size: 307.0 MB (306967045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304d63f21c52b2f263246e326df1091bc499b65fc82d80bd9a37863fa3e3102e`  
		Last Modified: Thu, 18 Jan 2024 11:32:01 GMT  
		Size: 2.4 MB (2350947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e61a20073dfa0f414e1ebdde6664286f2713c9b4c5fe8c6405804da997e559`  
		Last Modified: Thu, 18 Jan 2024 11:32:01 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fa20c72ff9a5abf5c579cdf5e0172ea89220b2c92c23e20d96b221bc1d3963`  
		Last Modified: Thu, 18 Jan 2024 11:32:02 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7f03d771fa7f5e3cae63a45135ed0582fc93ed2c5110bdb91e6f76767158d3`  
		Last Modified: Thu, 18 Jan 2024 11:32:02 GMT  
		Size: 6.4 KB (6412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a39e8f76ef4aa91715c6aeeedaf84160cb50b2388836a60c89704790977ca3d`  
		Last Modified: Thu, 18 Jan 2024 11:32:03 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:f84d5113ac892d6c8bc0fdfb7a7a5c77b70452f06ceee947783cbe5dc971f74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef4cefd6ade6c43fac70c9a6b9ef9b6d40a7f508f8583a48be6929b2a246b2c`

```dockerfile
```

-	Layers:
	-	`sha256:9218ac1b4c59cedcf6429ce07087415695d148943f0cc466d1aaafd60d458072`  
		Last Modified: Thu, 18 Jan 2024 11:32:00 GMT  
		Size: 8.1 MB (8123616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d09645f5797238cd600f357e5b3f6a5ef81d2580b9d4f5003948b6d950c8a16`  
		Last Modified: Thu, 18 Jan 2024 11:31:59 GMT  
		Size: 43.9 KB (43947 bytes)  
		MIME: application/vnd.in-toto+json
