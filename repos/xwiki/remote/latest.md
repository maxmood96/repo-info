## `xwiki:latest`

```console
$ docker pull xwiki@sha256:1ef4adde7846c01232c0ed8398d7505ae69d45384d6aede01e4dfaa684330c07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:01d006342941ab8bc97a0f8785118c4f82fce0b5219fcd951fcad111bcf47247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.2 MB (649180960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b559b82bbd63574ee5d4ce02348d026256de2afa32bacb6df35509454644b88`
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
# Tue, 17 Feb 2026 22:23:16 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 17 Feb 2026 22:23:16 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 17 Feb 2026 22:23:16 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 17 Feb 2026 22:23:16 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 17 Feb 2026 22:23:16 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 17 Feb 2026 22:23:16 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 17 Feb 2026 22:23:16 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:23:16 GMT
ENV XWIKI_VERSION=18.0.1
# Tue, 17 Feb 2026 22:23:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.0.1
# Tue, 17 Feb 2026 22:23:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=1c37eebab186bb2e8441d8ef2dc7b20e2da53f9767627205a88fd2cdb50361e1
# Tue, 17 Feb 2026 22:23:40 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 17 Feb 2026 22:23:40 GMT
ENV MYSQL_JDBC_VERSION=9.5.0
# Tue, 17 Feb 2026 22:23:40 GMT
ENV MYSQL_JDBC_SHA256=f2ca3dfaf00d4aa311470db7ea3051962944ba0cb60005a2f75467549c39f425
# Tue, 17 Feb 2026 22:23:40 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.5.0
# Tue, 17 Feb 2026 22:23:40 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.5.0.jar
# Tue, 17 Feb 2026 22:23:40 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.5.0.jar
# Tue, 17 Feb 2026 22:23:40 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 17 Feb 2026 22:23:40 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 17 Feb 2026 22:23:40 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 17 Feb 2026 22:23:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 17 Feb 2026 22:23:40 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:23:40 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Feb 2026 22:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 22:23:40 GMT
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
	-	`sha256:1a523cb1d05756059f158885353bf273ba1be0d6821d10ff4746d11b1758db5c`  
		Last Modified: Tue, 17 Feb 2026 22:24:23 GMT  
		Size: 192.3 MB (192309907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b353ba173a454e3ad00c1d4cd9f90b8450e18dd267310dfc7489bde7f92fc433`  
		Last Modified: Tue, 17 Feb 2026 22:24:26 GMT  
		Size: 340.2 MB (340207062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71866cdae6ade21b0b5f852d0de6c464ad708f27be7b314bfb2bb84a1a38a7b`  
		Last Modified: Tue, 17 Feb 2026 22:24:16 GMT  
		Size: 2.4 MB (2441393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0123c8c7fef517df6b9304f10f2099621dc75350579a9866fd059badb505474`  
		Last Modified: Tue, 17 Feb 2026 22:24:16 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b60276e064007f5f37b8357dc745159e1329855a07355344ce1924357b06f7`  
		Last Modified: Tue, 17 Feb 2026 22:24:17 GMT  
		Size: 2.4 KB (2366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cd48c7589ab2c04ef0a875b9d008539264da307f99e656c5f8aa282b556b1a`  
		Last Modified: Tue, 17 Feb 2026 22:24:17 GMT  
		Size: 10.9 KB (10900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a489ebc4b689bb741acdedb06cfca2b0b0f74b89873f7cd5f031d1e8c0f5b63`  
		Last Modified: Tue, 17 Feb 2026 22:24:19 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:744d960d59d17ee2a130d60398210a15336894ab6079451146bfc80af2bf786c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9233355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c7cd10c0f00bac3b4f86d664ae063dd03a96356fa107bffda7631c6845036c`

```dockerfile
```

-	Layers:
	-	`sha256:91374f236466e6079200e4fccf078e362c84227fd14935f0a13b1039e7c6160f`  
		Last Modified: Tue, 17 Feb 2026 22:24:17 GMT  
		Size: 9.2 MB (9191252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f021a4d2aa54bb2c8a27945894833a0e913f0b16b82b23ede4e99150bc0990df`  
		Last Modified: Tue, 17 Feb 2026 22:24:16 GMT  
		Size: 42.1 KB (42103 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:latest` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:6724b63e1c2b0f6c7ccc18aa1b85d607de0f5851a09789e8f1eae58abefeebc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.1 MB (645116059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723f75d053d4b6bd28e3f1c2dc3ea448f58b688d25fc6fa256e7eb36dcaa82f2`
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
# Tue, 17 Feb 2026 22:14:22 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 17 Feb 2026 22:14:22 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 17 Feb 2026 22:14:22 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 17 Feb 2026 22:14:22 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 17 Feb 2026 22:14:22 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 17 Feb 2026 22:14:22 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 17 Feb 2026 22:14:22 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:14:22 GMT
ENV XWIKI_VERSION=18.0.1
# Tue, 17 Feb 2026 22:14:22 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.0.1
# Tue, 17 Feb 2026 22:14:22 GMT
ENV XWIKI_DOWNLOAD_SHA256=1c37eebab186bb2e8441d8ef2dc7b20e2da53f9767627205a88fd2cdb50361e1
# Tue, 17 Feb 2026 22:14:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 17 Feb 2026 22:14:48 GMT
ENV MYSQL_JDBC_VERSION=9.5.0
# Tue, 17 Feb 2026 22:14:48 GMT
ENV MYSQL_JDBC_SHA256=f2ca3dfaf00d4aa311470db7ea3051962944ba0cb60005a2f75467549c39f425
# Tue, 17 Feb 2026 22:14:48 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.5.0
# Tue, 17 Feb 2026 22:14:48 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.5.0.jar
# Tue, 17 Feb 2026 22:14:48 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.5.0.jar
# Tue, 17 Feb 2026 22:14:48 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 17 Feb 2026 22:14:48 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 17 Feb 2026 22:14:48 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 17 Feb 2026 22:14:48 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 17 Feb 2026 22:14:48 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:14:48 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Feb 2026 22:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 22:14:48 GMT
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
	-	`sha256:f02ee3e4b92e6a9d6feb82b202173bc37bcf6f47e827f8bb52bdc9f54dbc40b3`  
		Last Modified: Tue, 17 Feb 2026 22:15:27 GMT  
		Size: 189.9 MB (189919311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec66e4224ba5e8ecb3c3699630ed736ff445de49c96a4107604fd49c0f0876a4`  
		Last Modified: Tue, 17 Feb 2026 22:15:36 GMT  
		Size: 340.2 MB (340207099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e30cd08583440b4fdee590c97ee8608f6ecbe7aa71b21df8d63851891d0142`  
		Last Modified: Tue, 17 Feb 2026 22:15:22 GMT  
		Size: 2.4 MB (2441391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7b540cfab24261b2d3eb5f1c64cf27cb3383a461601021f7e11e36341ae40f`  
		Last Modified: Tue, 17 Feb 2026 22:15:22 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64178239fc215ddb46a749a46dc3c1fbb306da8bc9938fd4a841da0b5b8d208c`  
		Last Modified: Tue, 17 Feb 2026 22:15:23 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c298c495bd6bb93579c7f31fbcc1e5e729eb546c89ab13eae9a85e2d7f879a`  
		Last Modified: Tue, 17 Feb 2026 22:15:24 GMT  
		Size: 10.9 KB (10901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db24f8fa9321b617afa17ea1a7724a5a84608706a6b44de952c9070aaee1e9f`  
		Last Modified: Tue, 17 Feb 2026 22:15:25 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:de1f8fef734e2291d086a8e90e425636dfe482bc5d6afeb273149ceac8bea0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b9be291afa91627811e549d79adad552323c49178560d6ba10d599355fe34`

```dockerfile
```

-	Layers:
	-	`sha256:ac4887db34d94c9f91576f3b36cd4c55c7f5ccd9e839c64d9354da5d20a3b86f`  
		Last Modified: Tue, 17 Feb 2026 22:15:22 GMT  
		Size: 9.2 MB (9192065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d2ae38945bc4f8a0c15e8f62f1e5e8fbd0e8771e0be856a8b8d7d75bc9d0cc`  
		Last Modified: Tue, 17 Feb 2026 22:15:22 GMT  
		Size: 42.3 KB (42336 bytes)  
		MIME: application/vnd.in-toto+json
