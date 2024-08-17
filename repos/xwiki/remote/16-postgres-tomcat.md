## `xwiki:16-postgres-tomcat`

```console
$ docker pull xwiki@sha256:a8fa047de798b215fe2d8a85cbf613be2c2154e6cd3c080c8d64c078dc5bb94c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:410f26fc78573d46862b4ebda4e5361aeb7fe75c39ad98b3e25e88b32a001104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.3 MB (611272231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7501128edb66c1964fca561ca37b3ff0f45c641d952a86044b7dc0ef8e38b445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 29 Jul 2024 15:54:10 GMT
ARG RELEASE
# Mon, 29 Jul 2024 15:54:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Jul 2024 15:54:10 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Mon, 29 Jul 2024 15:54:10 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 29 Jul 2024 15:54:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Jul 2024 15:54:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 15:54:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jul 2024 15:54:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jul 2024 15:54:10 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_MAJOR=9
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_VERSION=9.0.93
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Mon, 29 Jul 2024 15:54:10 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 29 Jul 2024 15:54:10 GMT
ENTRYPOINT []
# Mon, 29 Jul 2024 15:54:10 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jul 2024 15:54:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_VERSION=16.6.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.6.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_DOWNLOAD_SHA256=504e3fc3707d222d4a2be7c4e51e01242d4a7092380234d5076616d170390fe7
# Mon, 29 Jul 2024 15:54:10 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Mon, 29 Jul 2024 15:54:10 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jul 2024 15:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 15:54:10 GMT
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
	-	`sha256:d2b130d2f8217e924f4a3db7bfe6fcda23f9c6a06c95c84d150e50d43eff7c84`  
		Last Modified: Sat, 17 Aug 2024 05:00:22 GMT  
		Size: 194.3 MB (194312579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2152c917d264cdf7133d8dc30f685dd3bb7a9eee9dcb31df6019081ea7791123`  
		Last Modified: Sat, 17 Aug 2024 05:00:23 GMT  
		Size: 311.3 MB (311342352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7444a067dd69f441d78db65da60eefb84625c3a17c7caeaf318f91884597e712`  
		Last Modified: Sat, 17 Aug 2024 05:00:19 GMT  
		Size: 1.0 MB (1011975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685b485e26ba885fab631805acbc116616b10c5207bad2cd09701f659bfab641`  
		Last Modified: Sat, 17 Aug 2024 05:00:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dd671cff7bd943769be5dbf4b2e37bf19580d88c0ad6a0668d1bc04cb11483`  
		Last Modified: Sat, 17 Aug 2024 05:00:20 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62e066221dfe844dc533b2e4f87916183868f1b2a97179a89e1c9306ecee0ae`  
		Last Modified: Sat, 17 Aug 2024 05:00:20 GMT  
		Size: 6.5 KB (6543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec873650c2a4e2a3977fab975323f2286ada9bcdd6d4d39102f88729f599175`  
		Last Modified: Sat, 17 Aug 2024 05:00:20 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:2e5fb59624911dffc202cc7826b0d686f944e15851500ce08c4ccc35815e0a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8639509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f3e512eab927a7fcfc28239b1ec896476e3f0661ff0c89e43d215c20ec01d8`

```dockerfile
```

-	Layers:
	-	`sha256:dda87056ab411cd7b2728662169f32072dda294580f485200050a70a364ac6d5`  
		Last Modified: Sat, 17 Aug 2024 05:00:19 GMT  
		Size: 8.6 MB (8598235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e49f501f7e8323e3812df66fb06782e7a78fd817f08b8740cc6d8ecdd5f937e`  
		Last Modified: Sat, 17 Aug 2024 05:00:19 GMT  
		Size: 41.3 KB (41274 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:27862fcebcbd763d2cf6c9d83bf2d7e45c20ffa72aa2f3094ff5e2cdbbd83667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.8 MB (607772550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5e8d438b1bb12b12c959268612b0e6f4226d2d32f262d88cb0cf14f8063f3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 29 Jul 2024 15:54:10 GMT
ARG RELEASE
# Mon, 29 Jul 2024 15:54:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Jul 2024 15:54:10 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Mon, 29 Jul 2024 15:54:10 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 29 Jul 2024 15:54:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Jul 2024 15:54:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 15:54:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jul 2024 15:54:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jul 2024 15:54:10 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_MAJOR=9
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_VERSION=9.0.93
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Mon, 29 Jul 2024 15:54:10 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 29 Jul 2024 15:54:10 GMT
ENTRYPOINT []
# Mon, 29 Jul 2024 15:54:10 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jul 2024 15:54:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_VERSION=16.6.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.6.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_DOWNLOAD_SHA256=504e3fc3707d222d4a2be7c4e51e01242d4a7092380234d5076616d170390fe7
# Mon, 29 Jul 2024 15:54:10 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Mon, 29 Jul 2024 15:54:10 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Mon, 29 Jul 2024 15:54:10 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jul 2024 15:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 15:54:10 GMT
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
	-	`sha256:9c52cf792c0a377eb718dfd62147cebad0c34366f28346eceb5ba374ca0b5bd5`  
		Last Modified: Sat, 17 Aug 2024 14:53:13 GMT  
		Size: 192.0 MB (191964506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ae09be82284e536c3000070ca82ed74c2cbbabedffc41b0a1817ea20d145cf`  
		Last Modified: Sat, 17 Aug 2024 14:53:15 GMT  
		Size: 311.3 MB (311342338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bb563427e5070ec74808df26851dafc5e3a22c01bbbad89b0835db353880fb`  
		Last Modified: Sat, 17 Aug 2024 14:53:53 GMT  
		Size: 1.0 MB (1011976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebc7384fdb77787766af9ac20cd3babcd55b4dae43d1ba374005c903cf9a684`  
		Last Modified: Sat, 17 Aug 2024 14:53:53 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f4dbf3aeee20a33cbade420e8871f17545ec093ae185b6757e4705e67e82f`  
		Last Modified: Sat, 17 Aug 2024 14:53:53 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc4dfaa99669e0436d860c19fccb0908d46e6023b1562872d8cad08839204a6`  
		Last Modified: Sat, 17 Aug 2024 14:53:53 GMT  
		Size: 6.5 KB (6543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a009dcae074b355d7ae5616d65b8e3300d5f054afb08d0bb68e8a4a362818c5`  
		Last Modified: Sat, 17 Aug 2024 14:53:54 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:a0caa8fc306505dbb712e76cafe1578e51a926b16d140cc3ce119640227eb8a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8641530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51320072a5f37efdb61b679bd38f6f7c8a029c2e678ee3e2a9d9a928e6046c5c`

```dockerfile
```

-	Layers:
	-	`sha256:f33299c2a0dd990fc9cd9b8176f4d93d290dc33fed92b839299ac98b898d3205`  
		Last Modified: Sat, 17 Aug 2024 14:53:53 GMT  
		Size: 8.6 MB (8599606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3edf0f8f402c163a65ef8d248a81f2c095d0ec9f2e761db288ff1a60f234d6`  
		Last Modified: Sat, 17 Aug 2024 14:53:53 GMT  
		Size: 41.9 KB (41924 bytes)  
		MIME: application/vnd.in-toto+json
