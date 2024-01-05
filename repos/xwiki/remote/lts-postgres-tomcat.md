## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:f2ef2777baeed794af43f478d3e59a1f28144401fec6bb115d69200ff59f22f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1b9583ae1a425ee63573ee4e63ecb8bc52550b80a48a40c38e5f266465b91b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 MB (595116889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e1e2b82231570eba07658bc4961e4c153317ac90425262df52656b0c9f5d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 16:07:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 16:07:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 16:07:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 16:07:07 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 16:07:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 16:07:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 16:09:32 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 16 Dec 2023 16:09:32 GMT
ENV TOMCAT_MAJOR=9
# Sat, 16 Dec 2023 16:09:32 GMT
ENV TOMCAT_VERSION=9.0.84
# Sat, 16 Dec 2023 16:09:32 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Sat, 16 Dec 2023 16:09:32 GMT
COPY dir:e3a76c94a246a1206356fe923c85a36b030f13bc6f6e832187da5052d71cee0e in /usr/local/tomcat 
# Sat, 16 Dec 2023 16:09:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 16:09:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 16 Dec 2023 16:09:38 GMT
EXPOSE 8080
# Sat, 16 Dec 2023 16:09:38 GMT
ENTRYPOINT []
# Sat, 16 Dec 2023 16:09:38 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 03 Jan 2024 14:50:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_VERSION=15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=8c1bb157f03b714255305aadc0904d35e87ae38df998dcfb5117de3d395d473c
# Wed, 03 Jan 2024 14:50:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 03 Jan 2024 14:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jan 2024 14:50:08 GMT
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
	-	`sha256:47e54015b78f4696b9db541353eb71ee15c3b3fc678ba8c9d004357d287ab67b`  
		Last Modified: Thu, 04 Jan 2024 19:58:07 GMT  
		Size: 179.3 MB (179291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5ba66f006c960a6c2ec5af141137a725b10322d6275ca14bb0b48f6b377be5`  
		Last Modified: Thu, 04 Jan 2024 19:58:10 GMT  
		Size: 307.0 MB (306966407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2f04b722ba57c490fe9ca93f658037acbd80c7569041af522256f9ea33ccde`  
		Last Modified: Thu, 04 Jan 2024 19:58:04 GMT  
		Size: 936.8 KB (936848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6d5f5cf66aa124dd41bd5c25ed3818ae15b2c968656d6141cd0572627cb9e4`  
		Last Modified: Thu, 04 Jan 2024 19:58:04 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d4954ec4050351e7eecd39bf57cb159b971fe7346293184bdebc9e183ac147`  
		Last Modified: Thu, 04 Jan 2024 19:58:05 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c06ddad96f7c40b3a17e4b0facad2c39fb92b00ad4d635cf6ea11dfb848bdd`  
		Last Modified: Thu, 04 Jan 2024 19:58:06 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e96276a9344db36510d589131c628b6dd4333b9d7306ef1144a0ddf83a8fa0`  
		Last Modified: Thu, 04 Jan 2024 19:58:06 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:18c009583b89753d831578cfb47b00520f257d655eb060473a7166ac75115859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8086759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249f98fbb1c01babdcb4c2321c2c3e4abd8efdbdeec09d42bfbc0096915be631`

```dockerfile
```

-	Layers:
	-	`sha256:fae7e0ea83a04034d6bc310357765cb116e265345ea33b4542bf08e0ec5315e2`  
		Last Modified: Thu, 04 Jan 2024 19:58:05 GMT  
		Size: 8.0 MB (8046027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d74b8067e57259e13321d26c2f2a0750246dbaa1bde4ed9bde257170bd6885b2`  
		Last Modified: Thu, 04 Jan 2024 19:58:04 GMT  
		Size: 40.7 KB (40732 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:56294880176aa23b0b6b9021ed094999dfbd151ef9064fa40c8e1a29ac977655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.0 MB (588994873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239c48aacad734caf92dfb668073a0100ab114ce3a915a49026c83cbe07fe13e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 14:58:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 14:58:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 14:58:16 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 14:58:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 14:58:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 15:00:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 16 Dec 2023 15:00:13 GMT
ENV TOMCAT_MAJOR=9
# Sat, 16 Dec 2023 15:00:13 GMT
ENV TOMCAT_VERSION=9.0.84
# Sat, 16 Dec 2023 15:00:13 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Sat, 16 Dec 2023 15:00:13 GMT
COPY dir:14fe7e4b8e31f53a38fe02615c860260f06f1bfa5d55349e5c610bb0eaaf3673 in /usr/local/tomcat 
# Sat, 16 Dec 2023 15:00:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:00:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 16 Dec 2023 15:00:18 GMT
EXPOSE 8080
# Sat, 16 Dec 2023 15:00:18 GMT
ENTRYPOINT []
# Sat, 16 Dec 2023 15:00:18 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 03 Jan 2024 14:50:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_VERSION=15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=8c1bb157f03b714255305aadc0904d35e87ae38df998dcfb5117de3d395d473c
# Wed, 03 Jan 2024 14:50:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 03 Jan 2024 14:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jan 2024 14:50:08 GMT
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
	-	`sha256:a910edd91617f5b01f025c4876c262408049502167afe0d00ad85e94cf642707`  
		Last Modified: Thu, 04 Jan 2024 22:14:39 GMT  
		Size: 307.0 MB (306966388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2ba9e2b155161bd989e03ba67fc7960944bc222535daed3ec81df69903bb6c`  
		Last Modified: Thu, 04 Jan 2024 22:14:33 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc48cd872e6eebd4e89ee8c12c5b73528ce3518e9209d063028bbeb068c2d548`  
		Last Modified: Thu, 04 Jan 2024 22:14:33 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5428cc88d5c64813c0e57e245ef3be9c0c25c6cc4326b69f474d45110ae25846`  
		Last Modified: Thu, 04 Jan 2024 22:14:34 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2bad58728bc9394ef5c369de6a322331b9ef4cba579077e756fcc03a9d2e45`  
		Last Modified: Thu, 04 Jan 2024 22:14:34 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a9c0c3e2946545699931806acd549aed1e15e907a96a357bc7b06bd1ac7dbb`  
		Last Modified: Thu, 04 Jan 2024 22:14:35 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:679697ee6ac527eb6aad0aa391f8a2723993abff441acb1c3d84caef60320c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8169342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58139a2fd86b35989605231620eb5e2a0c8835ce76ac2b64083ade8ebd17ab89`

```dockerfile
```

-	Layers:
	-	`sha256:aa3076d3f7c128081501bd495ca216552505b3ff456b5962e903f4f982f1e80e`  
		Last Modified: Thu, 04 Jan 2024 22:14:33 GMT  
		Size: 8.1 MB (8130057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ee9d8e56003b8a03ad08336bdd19ed6d653ed21bd3ddfbe8e9a17cdacc934b`  
		Last Modified: Thu, 04 Jan 2024 22:14:32 GMT  
		Size: 39.3 KB (39285 bytes)  
		MIME: application/vnd.in-toto+json
