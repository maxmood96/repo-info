## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:6aa7edc6105bf37a4c5e8783991e7535e6f7eb7bd00b94239f332e985153b1e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:06fbbed2117a3264adab8a0bca04d26c7f5fca460ec63011bf44c8c0b82b955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.9 MB (607893531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377eb3cd3ae4262457476e2397c2e40436b8ec486b19a97e6ff0ccd62755f09c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 27 Jun 2024 13:08:28 GMT
ARG RELEASE
# Thu, 27 Jun 2024 13:08:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 13:08:28 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 27 Jun 2024 13:08:28 GMT
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f3240f14b29df5bc95bc46182be5743c59dcd9622a24ab9c977c50e3112a5e`  
		Last Modified: Sat, 17 Aug 2024 01:13:41 GMT  
		Size: 47.3 MB (47280219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b595e1190ec8667726b2bf5ee7d325cd07181c0b309a5100d0162213115a7cb`  
		Last Modified: Sat, 17 Aug 2024 01:13:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197e18a2a290f7c94f0e1ee91964278e287248b72f64580646c08f7fae19af12`  
		Last Modified: Sat, 17 Aug 2024 01:13:35 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9346c9ccb16f641b3b62dd3bb1d23c9dfbc476ac93ff0b27955fede0934bf4f1`  
		Last Modified: Sat, 17 Aug 2024 04:07:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9e42050476a9210cc10aaae5e6afe3f60662fa8aec461ee5c3eb9ce7e0dbc1`  
		Last Modified: Sat, 17 Aug 2024 04:07:37 GMT  
		Size: 12.8 MB (12764993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a82503fd791a476dab48b415ca161bc5ce6db497e52db75a5ccadf76bee7ca`  
		Last Modified: Sat, 17 Aug 2024 04:07:37 GMT  
		Size: 210.8 KB (210757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdbe4d88fb39ab7de74c7b0476c5a9af0cb8533034758f1acc346231c267119`  
		Last Modified: Sat, 17 Aug 2024 05:00:20 GMT  
		Size: 195.3 MB (195308130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f2e5db0c76e721ebecafa539697b5847563d3ed2c1e7328744238fe5f34a7`  
		Last Modified: Sat, 17 Aug 2024 05:00:24 GMT  
		Size: 307.0 MB (306968199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b4982874645780bc1b1eb9cab64d433f13a58e99761559d547159af1588561`  
		Last Modified: Sat, 17 Aug 2024 05:00:18 GMT  
		Size: 1.0 MB (1011976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb5cd1c15a1e7195aa8b67d8fff19cafe7bc45d834aef6667d624c18678055a`  
		Last Modified: Sat, 17 Aug 2024 05:00:18 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff3a968d91637d3db425653c3b6d222fae33fa056f8304d3d92aea12f3d43f`  
		Last Modified: Sat, 17 Aug 2024 05:00:19 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf89c99ba1b17bd16532f00f3dee32cab7af7c8d0c06c2a336aa48c7030cc52d`  
		Last Modified: Sat, 17 Aug 2024 05:00:19 GMT  
		Size: 6.4 KB (6430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c178f152e84f1716b7009a0941c75a17b966a9eaaca410ac17cb72b2d4578611`  
		Last Modified: Sat, 17 Aug 2024 05:00:19 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:d8a3931c354585e809624744274b15e262a82e52a2ad86176bf1fcd12e84744f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8644600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06303ec026c2fe126c76edab5a63be049798bd55f615e688f05de6707f77aaea`

```dockerfile
```

-	Layers:
	-	`sha256:cd832ad5e9205e340476217cbdc790b6e280a5171dc47a5724fcb4566bf57539`  
		Last Modified: Sat, 17 Aug 2024 05:00:18 GMT  
		Size: 8.6 MB (8603525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe3055cb4afce41e0cb5e5f6e97443fded9cd8418500976573044abdde24170`  
		Last Modified: Sat, 17 Aug 2024 05:00:18 GMT  
		Size: 41.1 KB (41075 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:6e55549a530b0a3cf1705933acd3ef9d103d13b5854e1b2190fa2614e65d5916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604389801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cb220a2106a70e83d3de1106104f0ae276972aa0c957b9030c27912be96fa7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 27 Jun 2024 13:08:28 GMT
ARG RELEASE
# Thu, 27 Jun 2024 13:08:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 13:08:28 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 27 Jun 2024 13:08:28 GMT
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151f61f79738faea794be69163a840a5fe9134932adf08d15e3d5ebb38924ed9`  
		Last Modified: Sat, 17 Aug 2024 01:36:25 GMT  
		Size: 46.7 MB (46746363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c7f0bf0755dc5879a47b869ca41b59f0bf14893cb8f129d64b37687b61dc79`  
		Last Modified: Sat, 17 Aug 2024 01:36:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0e0a5bd6de285f3d8b20e89ba1ffdf12683a5db287ebf9c8bf487734a12e1d`  
		Last Modified: Sat, 17 Aug 2024 01:36:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136fb3b3c4261f779aaab8c67b20cfa2dafcbcf8bc0b98b1c05eec8ff28def4`  
		Last Modified: Sat, 17 Aug 2024 12:46:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c197bfd61c0cc559afb65607fe7df6595652f7aeb44e757329d29d71fe6b4b19`  
		Last Modified: Sat, 17 Aug 2024 12:49:18 GMT  
		Size: 12.8 MB (12774986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d1a98876bbf331af965cb8eee014be664b71f6d2e50eed5d9a69070396ae5`  
		Last Modified: Sat, 17 Aug 2024 12:49:18 GMT  
		Size: 211.5 KB (211457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8f3e563d06f9b6007855edab0dad82b95c81ddccbf9fd43df83869d1822295`  
		Last Modified: Sat, 17 Aug 2024 14:57:46 GMT  
		Size: 193.0 MB (192956027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee06f54ce4bb67e92cab8f98a7b9d2106b0fe37f485e67d167f59f57de65fb3`  
		Last Modified: Sat, 17 Aug 2024 14:57:47 GMT  
		Size: 307.0 MB (306968162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3386b456530a50ad5888d984b150e86d8ee2b5db8d720e31abc395136296eb`  
		Last Modified: Sat, 17 Aug 2024 14:57:42 GMT  
		Size: 1.0 MB (1011980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40b6ca0716b3ce94bb544e97e08054ed5954dc9fdbe2e6ceb9fd662fbe0ecda`  
		Last Modified: Sat, 17 Aug 2024 14:57:41 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a08a10330dd98c933059d9b37112bf1b24b24de5ed1f518109f98cc2654f6a`  
		Last Modified: Sat, 17 Aug 2024 14:57:42 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525d4796f83bec20f1ca5b14305570ea89933ebd9d308ce2278b0bae56175ce`  
		Last Modified: Sat, 17 Aug 2024 14:57:43 GMT  
		Size: 6.4 KB (6431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b33ecf6efa04f4e3fe209adca8ce8bfe79413ec37d74a2dba6173941775a73e`  
		Last Modified: Sat, 17 Aug 2024 14:57:43 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0b0d4c30c6ebefa70e4b4673bdc5719793c124a88c6feb81d095513d928a1453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8646595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9757f0b46b348acb0e41b0d5878087bd811c4349ef8ac182cd6af736f47abe`

```dockerfile
```

-	Layers:
	-	`sha256:dcdfb47ca0c5a81d93772d22556496f7964740bb1819a2036bcf24883352be7c`  
		Last Modified: Sat, 17 Aug 2024 14:57:41 GMT  
		Size: 8.6 MB (8604884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b3fd2138752e95f98bb7fb7b4abcf923527704036c3232d6d320c299e4f5bc`  
		Last Modified: Sat, 17 Aug 2024 14:57:41 GMT  
		Size: 41.7 KB (41711 bytes)  
		MIME: application/vnd.in-toto+json
