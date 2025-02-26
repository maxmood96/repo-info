## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:ab8b484ed3b362d45cff976e0f20806b12eb28d311ca42512615bdcf4ec6ebf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:7fa7371b4c775e13549cbbf49a5ab7c0051424c46be0319fa22259d8df9d69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.0 MB (637048154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1ca60f7f8b7e54150745922a919c1487a32e2b2796afc668a9d695ecf83e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 15:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 15:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_VERSION=10.1.36
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_SHA512=972a406263fd540b135efae4b375543781b26104acb07114c3e535fe31e5b0a5c87ae6dff055e0e47877a3861070c264bb236686cf08bc08d98b7541e5d743c7
# Tue, 18 Feb 2025 15:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 15:03:21 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 15:03:21 GMT
CMD ["catalina.sh" "run"]
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 25 Feb 2025 13:05:11 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
ENV XWIKI_VERSION=17.1.0
# Tue, 25 Feb 2025 13:05:11 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.1.0
# Tue, 25 Feb 2025 13:05:11 GMT
ENV XWIKI_DOWNLOAD_SHA256=ee59953e021b868faa6a254b321f28fbe1dd20eb2e7175d37f9a6d0a366d8e40
# Tue, 25 Feb 2025 13:05:11 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 25 Feb 2025 13:05:11 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
VOLUME [/usr/local/xwiki]
# Tue, 25 Feb 2025 13:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 13:05:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21fde7f674e1262f9a291fb3b148dce3986b16a6afe2b1077240af4411e8d`  
		Last Modified: Tue, 04 Feb 2025 04:40:13 GMT  
		Size: 17.0 MB (16962453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e1027cc04acbd0bbe96f77c4b07270e74687784095964c3f8e1145ed4062a0`  
		Last Modified: Tue, 04 Feb 2025 04:40:14 GMT  
		Size: 52.9 MB (52876121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb109d1b0266a0c777373e83c16fd3b583414425ea70ad73adbf43bf4b8a569e`  
		Last Modified: Tue, 04 Feb 2025 04:40:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f09a34126553bccc37644f98b45096297b0127f040e8492684976c77ec2b14a`  
		Last Modified: Tue, 04 Feb 2025 04:40:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1efd4859c501c0525fd38880aa57ac87cac7e6f7ebdcb6dc2c4e028a2ea15f0`  
		Last Modified: Wed, 19 Feb 2025 01:08:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570accbe11b3844c084b0e31bd7ca3d0ac6ca5dd4608ead3235bcb6dde387ef6`  
		Last Modified: Wed, 19 Feb 2025 01:08:18 GMT  
		Size: 13.8 MB (13827819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bbe363f0c5d9d54f6a8b9b0d3e4712b067cbed622305e031f2b82388fe9e3b`  
		Last Modified: Wed, 19 Feb 2025 01:08:18 GMT  
		Size: 12.8 MB (12832480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950770f2f9cd867adcb3cf66bd85792b4c8f19c7953ba2e501c8826ac9317484`  
		Last Modified: Tue, 25 Feb 2025 18:30:26 GMT  
		Size: 191.2 MB (191194683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c6f9edf68d7f41907e5c36f0b4775ad37594cd205fe9cb3c9e066bc0c3914`  
		Last Modified: Tue, 25 Feb 2025 18:30:27 GMT  
		Size: 317.2 MB (317150666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce138cd382feb5520dfd42c54b40869f59c1bd46e0ec5d582d05d57ba80d8bd9`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 2.4 MB (2434172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a973d937c5617404d096b46c34928f055b792406c2f7e400ad54d8c2d5fd662a`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97bebbf6e2db6cc9f6054bbbabb002100d64e1b8d24ab377d315f55aba7a4dd`  
		Last Modified: Tue, 25 Feb 2025 18:30:24 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f54dc9899803351e1506e5422d77cefd3adab963fc4debf000daa256870eccc`  
		Last Modified: Tue, 25 Feb 2025 18:30:24 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c862b01fb6ea7a7d915392d4b6b2270a4ca5de801ef8cc444a48809ced4de7`  
		Last Modified: Tue, 25 Feb 2025 18:30:25 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:ed4b0d46a68fb61d62dcaeae4a658085a1048fc8fbe063cb3114aec7314a6028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8809233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ae2719f3408eb317ea99106bd45fea367a19ad9e3488832f5374e50d2b8234`

```dockerfile
```

-	Layers:
	-	`sha256:7dbccf5ed2cf46dacf598948e8a18532b806220ffdd733b3a677b949f6f96732`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 8.8 MB (8767077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acee55674cbbfb7403233002d796011e184a2e7c77ba0869b2623dc4a871bf5`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 42.2 KB (42156 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:fe4729f5adee86caca2560d3cac56802b118ccbd844ab5259bfb64b2c98e0efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.8 MB (632829717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2300387c70cf7b6db218816c0d4d84f44cd25bd5c97d049df198b3ce51e4cd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 15:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 15:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_VERSION=10.1.36
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_SHA512=972a406263fd540b135efae4b375543781b26104acb07114c3e535fe31e5b0a5c87ae6dff055e0e47877a3861070c264bb236686cf08bc08d98b7541e5d743c7
# Tue, 18 Feb 2025 15:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 15:03:21 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 15:03:21 GMT
CMD ["catalina.sh" "run"]
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 25 Feb 2025 13:05:11 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 25 Feb 2025 13:05:11 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
ENV XWIKI_VERSION=17.1.0
# Tue, 25 Feb 2025 13:05:11 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.1.0
# Tue, 25 Feb 2025 13:05:11 GMT
ENV XWIKI_DOWNLOAD_SHA256=ee59953e021b868faa6a254b321f28fbe1dd20eb2e7175d37f9a6d0a366d8e40
# Tue, 25 Feb 2025 13:05:11 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 25 Feb 2025 13:05:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 25 Feb 2025 13:05:11 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Feb 2025 13:05:11 GMT
VOLUME [/usr/local/xwiki]
# Tue, 25 Feb 2025 13:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 13:05:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cbfadccc4ef79b758e18dd8d1708943e6c36b0c9c7e7b94a5d7ff99d3d28af`  
		Last Modified: Tue, 04 Feb 2025 09:25:48 GMT  
		Size: 52.1 MB (52058738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426c44160873d09bb23bdec752f80f9f6f3a7b054d0cd8a334eeb2c92fa0ed9`  
		Last Modified: Tue, 04 Feb 2025 09:25:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3daf2a897e045b94b8cf1d4c94f9dc6f09163273fbbf52afcd8dc60a445788`  
		Last Modified: Tue, 04 Feb 2025 09:25:47 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ee034a146c65a6d1fdfbfcc76a4dea8b9a3fc21563811d2cd9443e32f75a3`  
		Last Modified: Wed, 05 Feb 2025 04:43:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1350baf9745865144f00955defd89c5a56e9afda9c5d3740bda587e558aa12f`  
		Last Modified: Wed, 19 Feb 2025 02:12:29 GMT  
		Size: 13.8 MB (13830359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6173ab83da82bd8ec3b730076e3e9e077c733dbc7b21fa9e349b8c83696958`  
		Last Modified: Wed, 19 Feb 2025 02:12:29 GMT  
		Size: 12.6 MB (12601485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94489cae5f89238b3be23477fecc3ff776a4adab276eef52a6dc66e8efb090c`  
		Last Modified: Wed, 19 Feb 2025 03:10:37 GMT  
		Size: 188.9 MB (188867827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c981ab50e6205c33bf90ed6c46a30a0852fc5e99c335fe454413c50afcb1fac`  
		Last Modified: Wed, 26 Feb 2025 00:25:31 GMT  
		Size: 317.2 MB (317150668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a42ac64df774ce88fc1e19e7cb35432a7340555a864072adde188521b314216`  
		Last Modified: Wed, 26 Feb 2025 00:25:24 GMT  
		Size: 2.4 MB (2434174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015404555373eecf2302bde2bb3ea0bf472db8482cd3eb165076261c7256ae96`  
		Last Modified: Wed, 26 Feb 2025 00:25:24 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a88ea7216adc1714018f6f8036a91c9089e035c0f1327ee124967348d284b8`  
		Last Modified: Wed, 26 Feb 2025 00:25:24 GMT  
		Size: 2.4 KB (2368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58712576b3647b86e9acedbce98e7af7b4a47edde61e4fb492459308ab394811`  
		Last Modified: Wed, 26 Feb 2025 00:25:25 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0dab162870df2ea090dfb3d6747c7ff75a7b632dc416d9846826062557e4f6`  
		Last Modified: Wed, 26 Feb 2025 00:25:25 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:6e2e420dfeade5c7133c87a0070579f0ad5f10cc5295c0199561941b548f1640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f8774a6e00c2132028a8bb671b639a02dbb71ceba11e0374c40bca8b9a97cd`

```dockerfile
```

-	Layers:
	-	`sha256:cc5d4fb1f6e3f1b9b846f6d16cd9b122ac38cf9c810c5236ec517119a0b29407`  
		Last Modified: Wed, 26 Feb 2025 00:25:24 GMT  
		Size: 8.8 MB (8767890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a87f934f6d2f19e5f44a204e3a24474b3bdb12460ae8f259b4bbffa56a50fc98`  
		Last Modified: Wed, 26 Feb 2025 00:25:23 GMT  
		Size: 42.4 KB (42389 bytes)  
		MIME: application/vnd.in-toto+json
