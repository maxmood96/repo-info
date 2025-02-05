## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:a92cfc400fca0251a5a6545f3e311fbb1841d2c54b7f8da9efcd708f3aa55ae5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:77796ed5bf1b4e04044d947c0534342a218ea5199650b58a04354df373ea40e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621696522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1592931add65b48de8e3d10de4f040d613df3e29e9503cb1dd792f7b79fe4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jan 2025 23:11:14 GMT
ARG RELEASE
# Mon, 06 Jan 2025 23:11:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 06 Jan 2025 23:11:14 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=10
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=10.1.34
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=e29c4d0e26295d64dfeee399e7719b5baac2682ac0e7b53702f26d630fea761f93ddf60674dfe87c41ddd9b79d4938a6a533a280bb3d7fb83c2a1b7cd5da6b09
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jan 2025 17:13:32 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_VERSION=17.0.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.0.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd4d25b42c5645d87f7ed242967161ccb2648688948de93649a5ca11a1845c34
# Tue, 28 Jan 2025 17:13:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Tue, 28 Jan 2025 17:13:32 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 17:13:32 GMT
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
	-	`sha256:8f34f38d467d39341d9a2307c185fc6cc9f3e5851137e5d1ef373311f8695637`  
		Last Modified: Tue, 04 Feb 2025 06:16:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e5cb3201e2c15e9247982f369f84a2130da37df3937e2c586ca876e2aed5c9`  
		Last Modified: Tue, 04 Feb 2025 06:16:14 GMT  
		Size: 13.7 MB (13654261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a55df4873587f0b16cc0fb4642fa00c71c8580674ba51f1e8d85a332ff55d04`  
		Last Modified: Tue, 04 Feb 2025 06:16:13 GMT  
		Size: 223.6 KB (223636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3dd7ba97157ae598d5324fcb8277ec9502356eceb24d17f222e70ff5ba4fc`  
		Last Modified: Tue, 04 Feb 2025 07:15:09 GMT  
		Size: 191.2 MB (191192541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c607a938e8ee6191b22fd614672c8e68ab6e83c9567422ae68b80b183895d0db`  
		Last Modified: Tue, 04 Feb 2025 07:15:11 GMT  
		Size: 316.3 MB (316336616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755ac4568d7f53328537b873cf4412d4e78e758cdb8f0db46e8e09a0bf6d2d7b`  
		Last Modified: Tue, 04 Feb 2025 07:15:04 GMT  
		Size: 681.3 KB (681259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f46b521947575c88ddcbb9c46b8d7b7f9c0fd5db366f5478dc802a1326e4d`  
		Last Modified: Tue, 04 Feb 2025 07:15:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959bd3d05983a4e053e80ca416a0ddc8c59e2bf346f46fa40db6f3abaddb7ae5`  
		Last Modified: Tue, 04 Feb 2025 07:15:05 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b54a2806c17299f96b4871670b6b7533811744b859ab1d1084853795a00709`  
		Last Modified: Tue, 04 Feb 2025 07:15:05 GMT  
		Size: 6.6 KB (6583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe20b546ac1ca95f27e637c53f9966ec65b2f1ff6503f70388726de31768a200`  
		Last Modified: Tue, 04 Feb 2025 07:15:06 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:ee985160b70a60fbbf3eac2c6befc7ef77ebd2ad9799689ab4404bec0c71fc1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8808271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f313b53fb61c3efbd4d50500029790c3942f2057f9a265a70d9472ca11b7b2`

```dockerfile
```

-	Layers:
	-	`sha256:0db45742f6fc94a1bbeb102d55ae2ee59d42933e79f19036d26d8c39a5bb50ca`  
		Last Modified: Tue, 04 Feb 2025 07:15:04 GMT  
		Size: 8.8 MB (8767470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf9f22f31bb9eebc01d0bc18c1ff4a682629ff85bb41dfae9af9465697afe74`  
		Last Modified: Tue, 04 Feb 2025 07:15:04 GMT  
		Size: 40.8 KB (40801 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bf5524af91f9bb85b703beeacd602b7d16d93ae080733c3ee9b3dfd893416bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617709270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5593f6c6e227fc6979080c41a477e52229be3c6085ab11af3ee770f1b967efa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jan 2025 23:11:14 GMT
ARG RELEASE
# Mon, 06 Jan 2025 23:11:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 06 Jan 2025 23:11:14 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=10
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=10.1.34
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=e29c4d0e26295d64dfeee399e7719b5baac2682ac0e7b53702f26d630fea761f93ddf60674dfe87c41ddd9b79d4938a6a533a280bb3d7fb83c2a1b7cd5da6b09
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jan 2025 17:13:32 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_VERSION=17.0.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.0.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd4d25b42c5645d87f7ed242967161ccb2648688948de93649a5ca11a1845c34
# Tue, 28 Jan 2025 17:13:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Tue, 28 Jan 2025 17:13:32 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 17:13:32 GMT
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
	-	`sha256:f449e02b0a373027d1a8760ed912ecba3625c37b1fa3c2313a778e74d4b31460`  
		Last Modified: Wed, 05 Feb 2025 04:44:55 GMT  
		Size: 13.7 MB (13657752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377f41d4534cf5b90263153dc8b0ff0c3513bab1a0d1a1703a4fe718dbc7349`  
		Last Modified: Wed, 05 Feb 2025 04:44:55 GMT  
		Size: 224.2 KB (224197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2ef0ed9d169e92af3778073ad4630d63c0e6f9b9b17190742bc8f74f1b0881`  
		Last Modified: Wed, 05 Feb 2025 13:46:57 GMT  
		Size: 188.9 MB (188864385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a08ba3da94f2ba608e176f2b2567c08f663b14c655abc9d44f79962121128c`  
		Last Modified: Wed, 05 Feb 2025 13:46:56 GMT  
		Size: 316.3 MB (316336582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566b81d2c1e900451605821da4e343db2ac3676d68d7e2f19f96418c5287eaf2`  
		Last Modified: Wed, 05 Feb 2025 13:48:19 GMT  
		Size: 681.3 KB (681261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b9c6d2b552c8dd20d9ba62c711f8eaad07f1239d6581e55bd290c64dc9e407`  
		Last Modified: Wed, 05 Feb 2025 13:48:19 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71196bb3faeb6eff7b6554d7de7b25539c10979397af31ace253d275c4cdcf0c`  
		Last Modified: Wed, 05 Feb 2025 13:48:19 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3b9082eab9493faffa0a2bf584e176f26a31fa6613a7a97bdefb5e84998661`  
		Last Modified: Wed, 05 Feb 2025 13:48:18 GMT  
		Size: 6.6 KB (6586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1bff23b6ef4a4581beab9f68f23082d1feaff6609d2eeaf354d5ceba63a6ae`  
		Last Modified: Wed, 05 Feb 2025 13:48:20 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:7a6df04f973bfc479a9052a9f2e05b968b8600385fc6b196e5e9d898def89090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8809197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c899dd25b63d27a2c72dbe3da356ff3c8eca891cbd1aaac3f21b86e56e4ed1`

```dockerfile
```

-	Layers:
	-	`sha256:8bcfcbe9330c2fb80f0b112b0eddd08f38b9684699f62722b648a6443171c1ad`  
		Last Modified: Wed, 05 Feb 2025 13:48:19 GMT  
		Size: 8.8 MB (8768223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99fb7ca765c0c4cc565076c9b00b0551ef61e94e4a15e4bae8a9f9dd6af2b03d`  
		Last Modified: Wed, 05 Feb 2025 13:48:18 GMT  
		Size: 41.0 KB (40974 bytes)  
		MIME: application/vnd.in-toto+json
