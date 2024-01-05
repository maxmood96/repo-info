## `xwiki:14-postgres-tomcat`

```console
$ docker pull xwiki@sha256:da85d722edca3991d68d3f2153c2d24ebaaacbd15a4f0169df0ff36eed40515f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:14-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:e1924ea46dbeca6007413485df4b206b1ed9f1bfc6df9e65047c5d06b5d32f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597300569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6a61c669c0e168b8768ae2f3c3ec408cc6f1c1a606ee794247d112c5bbaab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 05 Dec 2023 14:34:12 GMT
ARG RELEASE
# Tue, 05 Dec 2023 14:34:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Dec 2023 14:34:12 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["/bin/bash"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 05 Dec 2023 14:34:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 05 Dec 2023 14:34:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_MAJOR=9
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_VERSION=9.0.84
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Tue, 05 Dec 2023 14:34:12 GMT
COPY dir:e3a76c94a246a1206356fe923c85a36b030f13bc6f6e832187da5052d71cee0e in /usr/local/tomcat 
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 05 Dec 2023 14:34:12 GMT
EXPOSE 8080
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT []
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["catalina.sh" "run"]
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 05 Dec 2023 14:34:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_VERSION=14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_DOWNLOAD_SHA256=c418601676d61893ccb9e066b1f2bcce56717b49e5c2456656b6960db6bd6e4c
# Tue, 05 Dec 2023 14:34:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc81f1b04d3d203216bfcc90d5a6429b5c33ec66e790e3ebf566431088f5212c`  
		Last Modified: Sat, 16 Dec 2023 16:24:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a603ca3ebf9e8f0eb997467ce50ef8dfd4e49196308c1a39f9c5c0c39d2846b`  
		Last Modified: Sat, 16 Dec 2023 16:27:49 GMT  
		Size: 12.4 MB (12398194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b70543ac62867c34368428a8432713e13dbcb451521adfe0879fc51c5cae2e`  
		Last Modified: Sat, 16 Dec 2023 16:27:48 GMT  
		Size: 458.4 KB (458432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a684fd03abd5ec4c3528f0458050f8b03af9c5a885783d748df8617d90250c6`  
		Last Modified: Sat, 16 Dec 2023 16:27:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfa5d7e94b57edaeda1f32aa65b71e95311b9ad2c28ee6a2fc18411f3f7a903`  
		Last Modified: Thu, 04 Jan 2024 19:58:27 GMT  
		Size: 179.3 MB (179291212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e0e84fbb4816fab4e530cff0c1da5ff690c12e729b91cb6c8eea274cba476`  
		Last Modified: Thu, 04 Jan 2024 19:58:31 GMT  
		Size: 309.2 MB (309150276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5121682765182b7d9069e5354b3972d5c29240805ee71a42bfde6b66a2b64f2c`  
		Last Modified: Thu, 04 Jan 2024 19:58:23 GMT  
		Size: 936.9 KB (936855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca99e1f5c4b73521d824a6394d45bc25c5aaecdbb2ee90232570adc07c8093c7`  
		Last Modified: Thu, 04 Jan 2024 19:58:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf36e74252779a15456663fd6c93defabff8d61fbea57d1394af91fecd5cd25c`  
		Last Modified: Thu, 04 Jan 2024 19:58:24 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84246ca944595c415c0b02004eaf9efc286671750afabbf13e825dfe9a64682e`  
		Last Modified: Thu, 04 Jan 2024 19:58:24 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8565a67a6fa944c714da85ec741102c0edb939f69c05f2c6bf6dbbf2c2a23f1f`  
		Last Modified: Thu, 04 Jan 2024 19:58:25 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:49f8673802dfe4a62ea7022245dd3fdef7d9b902f2905b3b8faa3315a913f02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8069850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1198421c991f97835522d27d24edca9ecdec511e29428488a7d45995d0b2348`

```dockerfile
```

-	Layers:
	-	`sha256:aee395db876f14dc1bb57607d92310dc9c0f97c8e57357342ce9be994114b41a`  
		Last Modified: Thu, 04 Jan 2024 19:58:23 GMT  
		Size: 8.0 MB (8030692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fb37a40b4090b49130f17665778853518de4d77c829baed3e58dddd7f571f6`  
		Last Modified: Thu, 04 Jan 2024 19:58:22 GMT  
		Size: 39.2 KB (39158 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:14-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d436bc9fac4631433639c8a1fe25dcd059b131bf46ff6b4451fdd8b7beaa289e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.2 MB (591178460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bf670cfa60d98d6a6891728a44667c3207c906add5a9b1f328f7665850c304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 05 Dec 2023 14:34:12 GMT
ARG RELEASE
# Tue, 05 Dec 2023 14:34:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Dec 2023 14:34:12 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["/bin/bash"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 05 Dec 2023 14:34:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 14:34:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 05 Dec 2023 14:34:12 GMT
WORKDIR /usr/local/tomcat
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 05 Dec 2023 14:34:12 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_MAJOR=9
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_VERSION=9.0.84
# Tue, 05 Dec 2023 14:34:12 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Tue, 05 Dec 2023 14:34:12 GMT
COPY dir:14fe7e4b8e31f53a38fe02615c860260f06f1bfa5d55349e5c610bb0eaaf3673 in /usr/local/tomcat 
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 14:34:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 05 Dec 2023 14:34:12 GMT
EXPOSE 8080
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT []
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["catalina.sh" "run"]
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 05 Dec 2023 14:34:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 05 Dec 2023 14:34:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_VERSION=14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.20
# Tue, 05 Dec 2023 14:34:12 GMT
ENV XWIKI_DOWNLOAD_SHA256=c418601676d61893ccb9e066b1f2bcce56717b49e5c2456656b6960db6bd6e4c
# Tue, 05 Dec 2023 14:34:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 Dec 2023 14:34:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 05 Dec 2023 14:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Dec 2023 14:34:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fdc1608413c55e6f71ba5c11e8a186c5cdf1ffd462d135094650174976fd36`  
		Last Modified: Sat, 16 Dec 2023 15:13:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040f9b1d3ea5ed9193ca2803556daa46af53b68c910758193f72f2d9ea7583f6`  
		Last Modified: Sat, 16 Dec 2023 15:16:19 GMT  
		Size: 12.4 MB (12407499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b105fa48bd69dab1ec528eb0a9cdaf37f46e8af363a642b3f44e619e7751d4ed`  
		Last Modified: Sat, 16 Dec 2023 15:16:18 GMT  
		Size: 458.5 KB (458463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b656c2cf87b11b1a6165fa929daa3b987a92d55dd64f4151810c4a9d3ee4cd8`  
		Last Modified: Sat, 16 Dec 2023 15:16:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad8cbcd4f987ca9cf12f0a953f77431d0521b9cbe56057ca8d578d08bba2656`  
		Last Modified: Thu, 04 Jan 2024 22:14:37 GMT  
		Size: 174.3 MB (174329706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d8f525c6301b869bfb25a4eabe1584c70da2693a64d8ef52c73b056165f7b7`  
		Last Modified: Thu, 04 Jan 2024 22:18:24 GMT  
		Size: 309.2 MB (309150262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59bae687546e112f8d2baf40995be5424e804976584043ad9e2a0a32145bb29`  
		Last Modified: Thu, 04 Jan 2024 22:18:16 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a4ad490e48e5cd09d574925f218b390c803714284bf7d10b2ab78d3daef268`  
		Last Modified: Thu, 04 Jan 2024 22:18:15 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eddc0dd6144bbe8a114ce45ab50693f3c90d4cba6a66c1c44bf6adc2e29a3a`  
		Last Modified: Thu, 04 Jan 2024 22:18:16 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5143eb8077d6bc4ce59f686c825cb1ed4f4fdd54eecee8f3c814bab1ef0ca07`  
		Last Modified: Thu, 04 Jan 2024 22:18:16 GMT  
		Size: 6.1 KB (6129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72de93bb3f3f7f4bb851c1240174a81b02c6b8336b78f32f10437e7985aea5ac`  
		Last Modified: Thu, 04 Jan 2024 22:18:17 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:7618bd04069e3e4c37b6a40c630c777e23fa407c51e00a544b2476051803259f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8152413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe04580cfeb943dc2e1800166d4ed96904b6b108661413df259737e7553a0df`

```dockerfile
```

-	Layers:
	-	`sha256:61668253c73b31d385787eab6712cb7b47d5d801dfdf133efb62142739a35b48`  
		Last Modified: Thu, 04 Jan 2024 22:18:15 GMT  
		Size: 8.1 MB (8114712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f1157733c0b8222a1e5056e60fb47d983089c74e0c3b046f193cd623d93769`  
		Last Modified: Thu, 04 Jan 2024 22:18:15 GMT  
		Size: 37.7 KB (37701 bytes)  
		MIME: application/vnd.in-toto+json
