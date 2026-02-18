## `xwiki:17-postgres-tomcat`

```console
$ docker pull xwiki@sha256:22ae3175c7de135eeb3dc1c4622d53400186bff38b395ad897191f9d7584760f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:3ce1ce6cc7d9cbe49830d5770e28bff5017e2f2af99f2564ef3eaee8eb36dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.3 MB (638291360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be757c26f55140ee03a4ac6e289acff7fde12993af7d88462f007d9aac580692`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:20:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:20:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:20:23 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:55:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:55:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:55:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:55:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:55:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:55:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:55:43 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Feb 2026 21:55:43 GMT
ENV TOMCAT_VERSION=10.1.52
# Tue, 17 Feb 2026 21:55:43 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Tue, 17 Feb 2026 21:56:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:56:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:56:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:56:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:56:31 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:56:31 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Feb 2026 22:23:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 17 Feb 2026 22:23:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 17 Feb 2026 22:23:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 17 Feb 2026 22:23:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 17 Feb 2026 22:23:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 17 Feb 2026 22:23:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 17 Feb 2026 22:23:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:23:26 GMT
ENV XWIKI_VERSION=17.10.3
# Tue, 17 Feb 2026 22:23:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.3
# Tue, 17 Feb 2026 22:23:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=933b524e132bff6ab02bf801a85ac58f676795ab8c1fb3b48fa86023f7cf96fd
# Tue, 17 Feb 2026 22:23:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 17 Feb 2026 22:23:48 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Tue, 17 Feb 2026 22:23:48 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Tue, 17 Feb 2026 22:23:48 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Tue, 17 Feb 2026 22:23:48 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Tue, 17 Feb 2026 22:23:48 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Tue, 17 Feb 2026 22:23:48 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 17 Feb 2026 22:23:48 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 17 Feb 2026 22:23:48 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 17 Feb 2026 22:23:48 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 17 Feb 2026 22:23:48 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:23:48 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Feb 2026 22:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 22:23:48 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51024d09d55a0dd2db21ee0f8a82228dad25451936f15c7e5cb068e070498470`  
		Last Modified: Tue, 17 Feb 2026 20:20:39 GMT  
		Size: 17.0 MB (16980576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4247047ab404fa4e57d2dd23d30a1976f874414ce7c7fc6d40f81316270c411`  
		Last Modified: Tue, 17 Feb 2026 20:20:40 GMT  
		Size: 53.0 MB (52985486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23efddf26cd7c89f1e3c4284aaff43578b788402aad535c0d7582d61993ae0c`  
		Last Modified: Tue, 17 Feb 2026 20:20:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ec7c6edf1e7d89c9950ef904e2f16a2b5bb4e43375a62b8ebb6231dfa4eb96`  
		Last Modified: Tue, 17 Feb 2026 20:20:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477a6ec40f87af23842d29f2bca43453af69fdf3a3e04131c23ec2d5f927a005`  
		Last Modified: Tue, 17 Feb 2026 21:56:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4dec3e7a3bbe3578273238c2f2440ebeb1e6d0b9a286bf8e83771737a34726`  
		Last Modified: Tue, 17 Feb 2026 21:56:39 GMT  
		Size: 14.3 MB (14284416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fcdfacb5e2b63ec13fe71e47dc5ce6d8010918a5e57cc81eb46607219b4512`  
		Last Modified: Tue, 17 Feb 2026 21:56:39 GMT  
		Size: 224.8 KB (224756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0da48f992ce290b7406f99643215c137a6f647176c2c204c5106e7c16b5ec3`  
		Last Modified: Tue, 17 Feb 2026 22:24:32 GMT  
		Size: 192.3 MB (192309233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a941672df492894826b3c285a8dc3e64c60ee89232cb528c70e3b851c5436f`  
		Last Modified: Tue, 17 Feb 2026 22:24:35 GMT  
		Size: 330.7 MB (330704687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa7cd2de7edb933765f55a84acb6a5042ebe5a0946b067ea86c0c79852da3c`  
		Last Modified: Tue, 17 Feb 2026 22:24:25 GMT  
		Size: 1.1 MB (1055030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18ff61583f439023574a224be4d2e1a923603763ab6264f29fb960a7d032f62`  
		Last Modified: Tue, 17 Feb 2026 22:24:26 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88598db6bbba00ca57ee967d9e1a90ec6b7174cf47f9d46aad2f3076001121e3`  
		Last Modified: Tue, 17 Feb 2026 22:24:27 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c860dd6d7bf5e9885187ae62f3061573ca74724ada24796c9afc3f56c2adb983`  
		Last Modified: Tue, 17 Feb 2026 22:24:27 GMT  
		Size: 10.7 KB (10705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83c51632a98dac56065a14c7ace63dc827b859fa281909d0abdbae79556ea4`  
		Last Modified: Tue, 17 Feb 2026 22:24:28 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:ef5bcdc4735ab4cc81a45a6d39f153446d7a9ded27065f898cfa6e7c70160973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9220125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f47333444d3245f7c278f26526b236881c0ace8d38c9ec1a9356ea62d24fff5`

```dockerfile
```

-	Layers:
	-	`sha256:0a6d53e8d075dcbd878a5af8a3db3f724b3ec3f0f7d8b4ca3fa15561b7080cf2`  
		Last Modified: Tue, 17 Feb 2026 22:24:25 GMT  
		Size: 9.2 MB (9179700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5a7d925d1f8bf99cdabf321895bb95d6a1b03aec740d2f24f9e04a010301306`  
		Last Modified: Tue, 17 Feb 2026 22:24:25 GMT  
		Size: 40.4 KB (40425 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2d9a732339fcef6ff3eabee5267831a11d62142f39ed65770ca9d801762fcb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 MB (634227030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c250f343631283fd1e0a58eb7de178c7acfea9a190a477889becd8b720610ca0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:48 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:19:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:56:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:56:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:56:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:56:31 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:56:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:31 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Feb 2026 21:56:31 GMT
ENV TOMCAT_VERSION=10.1.52
# Tue, 17 Feb 2026 21:56:31 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Tue, 17 Feb 2026 21:56:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:56:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:56:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:56:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:56:39 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:56:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Feb 2026 22:14:34 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 17 Feb 2026 22:14:34 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 17 Feb 2026 22:14:34 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 17 Feb 2026 22:14:34 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 17 Feb 2026 22:14:34 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 17 Feb 2026 22:14:34 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 17 Feb 2026 22:14:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:14:34 GMT
ENV XWIKI_VERSION=17.10.3
# Tue, 17 Feb 2026 22:14:34 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.3
# Tue, 17 Feb 2026 22:14:34 GMT
ENV XWIKI_DOWNLOAD_SHA256=933b524e132bff6ab02bf801a85ac58f676795ab8c1fb3b48fa86023f7cf96fd
# Tue, 17 Feb 2026 22:15:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 17 Feb 2026 22:15:09 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Tue, 17 Feb 2026 22:15:09 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Tue, 17 Feb 2026 22:15:09 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Tue, 17 Feb 2026 22:15:09 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Tue, 17 Feb 2026 22:15:09 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Tue, 17 Feb 2026 22:15:10 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 17 Feb 2026 22:15:10 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 17 Feb 2026 22:15:10 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 17 Feb 2026 22:15:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 17 Feb 2026 22:15:10 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:15:10 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Feb 2026 22:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 22:15:10 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9a0a02907fdd6dd960abed9cafcbf879106f66849dda4f7a233bccb4434ec8`  
		Last Modified: Tue, 17 Feb 2026 20:19:14 GMT  
		Size: 17.0 MB (16994433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49ce0a2c26f9793abda89ce481106d5c6459e59db6ae2021f4155548525089d`  
		Last Modified: Tue, 17 Feb 2026 20:19:40 GMT  
		Size: 52.2 MB (52155649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19874336137573e037a93514b5a832458da45456d5638a41ab1eacfbd793fd4`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ef353aae734ae9d1def619d9120bd7093b573a0c56fc2db6fabefa3313b8c`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52ed4bcf62ca9f4672435f7b72ed8d2eae9bfb78de8c6198c4e403f5e1e8970`  
		Last Modified: Tue, 17 Feb 2026 21:56:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7655edb001eb586396ea1033971e28b9a0fa6c36503a055b924745837b8827f9`  
		Last Modified: Tue, 17 Feb 2026 21:56:49 GMT  
		Size: 14.3 MB (14288050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68708eb889667beddc5b8db265b052f3b060c0bc69fdfac27ab091c4d71f7067`  
		Last Modified: Tue, 17 Feb 2026 21:56:48 GMT  
		Size: 225.2 KB (225239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed22eea4ab7c59b61b76b1baaadc663a1ddf9b4c82dc04a8eda3910ed34da5a4`  
		Last Modified: Tue, 17 Feb 2026 22:15:50 GMT  
		Size: 189.9 MB (189919298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a41485ed146c9ff965031d3ca7dfa24d575da7869f89d75133d1f7bf2eeeb18`  
		Last Modified: Tue, 17 Feb 2026 22:15:53 GMT  
		Size: 330.7 MB (330704651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d686141dd44741ce2fbb5db263a5378fa7f772b78fb699241274fd1ef22e87`  
		Last Modified: Tue, 17 Feb 2026 22:15:44 GMT  
		Size: 1.1 MB (1055029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e318d92d8173ac4ddf8ed08f6bdefb2ecddad7bb5f6840ee686673a198782be3`  
		Last Modified: Tue, 17 Feb 2026 22:15:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73d9aa4ce274a8dc66cb6dd40113c07dc9925bd82ac9c78f3ca9da5ac2527ec`  
		Last Modified: Tue, 17 Feb 2026 22:15:46 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0baf1d688dfacbffcac6d5c2bc19fb9fbbdb4510bb7dc8b7e4128603b1170`  
		Last Modified: Tue, 17 Feb 2026 22:15:46 GMT  
		Size: 10.7 KB (10704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94226f6f0fd84c15a8cc4fd99c4f77ca9a4133d8466215c48a6bdfa1ed548e26`  
		Last Modified: Tue, 17 Feb 2026 22:15:47 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:c130ffbf29e8c867cce3570942588a44557d3e460af9b6a9933aa80499a984de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9221027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ef22023909813ac354f7ac74486ec5d1d6a0045134d2c4b5f736241eec4531`

```dockerfile
```

-	Layers:
	-	`sha256:707b3e735330cbf65ac022b1636af50ab46e4fa889021ace0d871365ca752590`  
		Last Modified: Tue, 17 Feb 2026 22:15:45 GMT  
		Size: 9.2 MB (9180441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c6c6b9b9da87b6af4549dc57ed0a22c2794e9275b7411e7712b3fc047a5e35f`  
		Last Modified: Tue, 17 Feb 2026 22:15:44 GMT  
		Size: 40.6 KB (40586 bytes)  
		MIME: application/vnd.in-toto+json
