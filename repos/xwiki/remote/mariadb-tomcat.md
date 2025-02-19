## `xwiki:mariadb-tomcat`

```console
$ docker pull xwiki@sha256:d4f9f3c5e0fd4bde9e63feec9f98c8e4d4b57883d52ae15542465432e73d3e25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7fa3078b57576bb45eaa27adcf37373dee51c43814f542a6c5737a65e00852be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634482940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765330a0817c3fe39245a73b62607ee3287447905b5801054ae860c628a61ff9`
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
# Tue, 28 Jan 2025 17:13:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 17:13:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:13:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 17:13:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2025 17:13:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:13:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 17:13:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_MAJOR=10
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_VERSION=10.1.36
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_SHA512=972a406263fd540b135efae4b375543781b26104acb07114c3e535fe31e5b0a5c87ae6dff055e0e47877a3861070c264bb236686cf08bc08d98b7541e5d743c7
# Tue, 28 Jan 2025 17:13:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT []
# Tue, 28 Jan 2025 17:13:32 GMT
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
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21fde7f674e1262f9a291fb3b148dce3986b16a6afe2b1077240af4411e8d`  
		Last Modified: Tue, 04 Feb 2025 07:16:41 GMT  
		Size: 17.0 MB (16962453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e1027cc04acbd0bbe96f77c4b07270e74687784095964c3f8e1145ed4062a0`  
		Last Modified: Tue, 04 Feb 2025 07:28:42 GMT  
		Size: 52.9 MB (52876121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb109d1b0266a0c777373e83c16fd3b583414425ea70ad73adbf43bf4b8a569e`  
		Last Modified: Tue, 04 Feb 2025 07:20:28 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f09a34126553bccc37644f98b45096297b0127f040e8492684976c77ec2b14a`  
		Last Modified: Tue, 04 Feb 2025 07:24:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1efd4859c501c0525fd38880aa57ac87cac7e6f7ebdcb6dc2c4e028a2ea15f0`  
		Last Modified: Wed, 19 Feb 2025 01:08:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570accbe11b3844c084b0e31bd7ca3d0ac6ca5dd4608ead3235bcb6dde387ef6`  
		Last Modified: Wed, 19 Feb 2025 01:08:36 GMT  
		Size: 13.8 MB (13827819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bbe363f0c5d9d54f6a8b9b0d3e4712b067cbed622305e031f2b82388fe9e3b`  
		Last Modified: Wed, 19 Feb 2025 01:08:36 GMT  
		Size: 12.8 MB (12832480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e99b358316206f0c907a04200b2368c83a57503a571af25eaec8b2587d3a080`  
		Last Modified: Wed, 19 Feb 2025 04:09:40 GMT  
		Size: 191.2 MB (191196602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f575b835993e70a5fe756d41a8a092bbc54100bedd98e6731b37cc2d46126bf2`  
		Last Modified: Wed, 19 Feb 2025 04:09:44 GMT  
		Size: 316.3 MB (316336571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e5c8d58e15221c093a2892bcef6649b07229f0579727db7d51e74ed02bb48`  
		Last Modified: Wed, 19 Feb 2025 02:09:51 GMT  
		Size: 681.3 KB (681251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9785727ca6c9b4e98f09410e33db3109d2a8ed02579f20bbb9cbac6a24fba818`  
		Last Modified: Wed, 19 Feb 2025 02:09:51 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6194763616ccda5a80797a11b1f24f2296be9aaeb25de31950b0ec5031aa`  
		Last Modified: Wed, 19 Feb 2025 02:09:51 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36badc9e046b703ee82bdbb7e27d39f3c0cb58a1365319168adab8adcbdd176e`  
		Last Modified: Wed, 19 Feb 2025 02:09:51 GMT  
		Size: 6.6 KB (6582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e40dc43a39876408969153bbaf0fd98fa1307e0f72fc63c7bb171c39ebc0d1`  
		Last Modified: Wed, 19 Feb 2025 02:09:50 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:73daaac744b77af1b74a798258dd4f67cb3e68bb2e43630b6eb85f75497802a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8806340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c1e7e09dbcb44afb3c11c29e843ac82700dbbbbee0789e8ad7eb1a0a5a20fa`

```dockerfile
```

-	Layers:
	-	`sha256:a00df3fbe88920be66c5aa301c42293e81990fea4ab671cd75f92dfd2e1743c0`  
		Last Modified: Wed, 19 Feb 2025 04:08:56 GMT  
		Size: 8.8 MB (8765523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babd36ec9a48ca3042cb3291d60aaede7ce75f698e92c5f54388df8dd38196ef`  
		Last Modified: Wed, 19 Feb 2025 04:08:56 GMT  
		Size: 40.8 KB (40817 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2ff8477c3de01b702d899d6a68124df09f90dd1d59aa340712abf066df4d6422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.3 MB (630262618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cf7a66725d0e635787f9e01195e775baed1bcd391ea9f815cf521a7e815347`
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
# Tue, 28 Jan 2025 17:13:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 17:13:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:13:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 17:13:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2025 17:13:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:13:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 17:13:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_MAJOR=10
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_VERSION=10.1.36
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_SHA512=972a406263fd540b135efae4b375543781b26104acb07114c3e535fe31e5b0a5c87ae6dff055e0e47877a3861070c264bb236686cf08bc08d98b7541e5d743c7
# Tue, 28 Jan 2025 17:13:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT []
# Tue, 28 Jan 2025 17:13:32 GMT
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
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 10:15:57 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cbfadccc4ef79b758e18dd8d1708943e6c36b0c9c7e7b94a5d7ff99d3d28af`  
		Last Modified: Tue, 04 Feb 2025 14:22:53 GMT  
		Size: 52.1 MB (52058738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426c44160873d09bb23bdec752f80f9f6f3a7b054d0cd8a334eeb2c92fa0ed9`  
		Last Modified: Tue, 04 Feb 2025 10:53:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3daf2a897e045b94b8cf1d4c94f9dc6f09163273fbbf52afcd8dc60a445788`  
		Last Modified: Tue, 04 Feb 2025 13:37:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ee034a146c65a6d1fdfbfcc76a4dea8b9a3fc21563811d2cd9443e32f75a3`  
		Last Modified: Wed, 05 Feb 2025 06:42:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1350baf9745865144f00955defd89c5a56e9afda9c5d3740bda587e558aa12f`  
		Last Modified: Wed, 19 Feb 2025 02:12:52 GMT  
		Size: 13.8 MB (13830359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6173ab83da82bd8ec3b730076e3e9e077c733dbc7b21fa9e349b8c83696958`  
		Last Modified: Wed, 19 Feb 2025 02:13:02 GMT  
		Size: 12.6 MB (12601485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94489cae5f89238b3be23477fecc3ff776a4adab276eef52a6dc66e8efb090c`  
		Last Modified: Wed, 19 Feb 2025 04:16:57 GMT  
		Size: 188.9 MB (188867827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11096535c14a4c8784bb6730682f7d9b7ec831c20122f6ec456407fdd146f2aa`  
		Last Modified: Wed, 19 Feb 2025 04:16:52 GMT  
		Size: 316.3 MB (316336607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab6a7a4da318575dce33cb45210d1af37ecf1c498701e65465281319184f527`  
		Last Modified: Wed, 19 Feb 2025 03:12:11 GMT  
		Size: 681.3 KB (681258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1a90124d4ea00fcb63a5ea83d869c5f44cd99c09ff4ea005eb5fd2f4eba4e8`  
		Last Modified: Wed, 19 Feb 2025 03:12:05 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8893a16a08ef3b976d3358de0c60fcef44de1eb8d8ab1bb8ad7beb96a268a2ef`  
		Last Modified: Wed, 19 Feb 2025 03:12:06 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6330d2460d56d83cf6f7bb183b2ff512575d9130e6c5f4d2374af926768fc7ef`  
		Last Modified: Wed, 19 Feb 2025 03:12:06 GMT  
		Size: 6.6 KB (6585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eca41ee579e2d01c66f6908f6d2008237e2bc791950daba6a9b38b0128f21c6`  
		Last Modified: Wed, 19 Feb 2025 03:12:07 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b29ddd94be0caebcf4f7d11475fe689142a279c1c11667af946011683087d63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8807266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173046eb9c142b5f4b0cc38e3ff2188bcfd0da6c247d4bea40d415c3251f690a`

```dockerfile
```

-	Layers:
	-	`sha256:9bb4f1560742b585ece9035cc85528879360e9a60401422add4365d26db9aa6e`  
		Last Modified: Wed, 19 Feb 2025 04:09:01 GMT  
		Size: 8.8 MB (8766276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7824a57c2a573aa47adc521f2ca7524498d5c98e2856a4d3025f37b6e6e8f805`  
		Last Modified: Wed, 19 Feb 2025 04:09:01 GMT  
		Size: 41.0 KB (40990 bytes)  
		MIME: application/vnd.in-toto+json
