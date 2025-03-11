## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:66457a4df17f1f17b3265a3f0951a27001b302d95d53899e2fce3275293beacf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:3d63560fca0f6dab73ad652ae9b7ceffd7795ee9eaa1f26aee375079f1d872c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 MB (637394302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32841de1e5f493fc75a9d2b9684432bc87d0242a02aff6a63771ab48d5cb65b6`
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
# Thu, 06 Mar 2025 15:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Mar 2025 15:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_VERSION=9.0.102
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_SHA512=cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a
# Thu, 06 Mar 2025 15:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Mar 2025 15:03:40 GMT
ENTRYPOINT []
# Thu, 06 Mar 2025 15:03:40 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Mar 2025 16:16:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_VERSION=16.10.5
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.5
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=ecc2d3e639273eff8ecb441aa55a8baefb87ec02826d178fb1e3aff1223dee4d
# Tue, 11 Mar 2025 16:16:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_VERSION=3.5.2
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_SHA256=f2f3c3c1a3bdaca69dd1d4e1cd8aed075242fc72ae41463ddb82e367b388f6ad
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.2
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.2.jar
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.2.jar
# Tue, 11 Mar 2025 16:16:28 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Mar 2025 16:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 16:16:28 GMT
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
	-	`sha256:000d4b416c74ab4fde052644e71cad79a21090a1e74c298e469d3c498a63f8e7`  
		Last Modified: Thu, 06 Mar 2025 19:09:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5354a9a4a8462f2b4987b1622f9171f0f396864fda95a47fb925204addd2b0a3`  
		Last Modified: Thu, 06 Mar 2025 19:09:11 GMT  
		Size: 13.5 MB (13470152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e6e358a2b7c3839e7a4d977fe2cef386b8428a69cc235dd7b239ecfa0119b6`  
		Last Modified: Thu, 06 Mar 2025 19:09:11 GMT  
		Size: 15.6 MB (15641723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8776b3ec2d4299463bd0e3aba91aa4dc9a4173c96ac1fb5b21a07f12b4667d4`  
		Last Modified: Tue, 11 Mar 2025 17:11:18 GMT  
		Size: 191.2 MB (191195545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afd5911ecc82287c7986bb457757d6bc12102af5959af29e1bef48f089558a1`  
		Last Modified: Tue, 11 Mar 2025 17:11:22 GMT  
		Size: 316.8 MB (316789905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3470f615bcef5ee8d57551b1efb8d21a4d311b872019ff294af7196636fb114e`  
		Last Modified: Tue, 11 Mar 2025 17:11:15 GMT  
		Size: 688.7 KB (688720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091483ca41e33660caa201d3cadfbabedd4f402b31922d6b2d4b80ac9248ec61`  
		Last Modified: Tue, 11 Mar 2025 17:11:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7daadbf26d9ce1d6f76ed13cb9e083461d79df551cc0703a674294ed9586d26`  
		Last Modified: Tue, 11 Mar 2025 17:11:16 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1e863dad2491caa47a9c26f0ac0ece2f9dcb1c9e42de3e5f212cdb15665c90`  
		Last Modified: Tue, 11 Mar 2025 17:11:16 GMT  
		Size: 6.6 KB (6624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e77902a8045f27636f9c2de4c860af6445c0a0e76535bb899fb1282a2dd474`  
		Last Modified: Tue, 11 Mar 2025 17:11:17 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:d09cb8302f7877f241eb495fbe8865f2275946f2c19da45212836e080917b7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8798733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdf87adf98ec06a227e35cfa162b82eb1ceffd1178acde9a4617bf4884827b2`

```dockerfile
```

-	Layers:
	-	`sha256:f67565db92224e0d153a6ea46a01853bc9388a6b8712a69725dcc335c1c7181e`  
		Last Modified: Tue, 11 Mar 2025 17:11:15 GMT  
		Size: 8.8 MB (8758235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb7baf4cb69157fe50001491c1382ff0428543c1c5e7731092216cbb4556216`  
		Last Modified: Tue, 11 Mar 2025 17:11:15 GMT  
		Size: 40.5 KB (40498 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:3fd85bb3a15a304cc76f92f77536bc8dc2c1e12da5686e2cdeaf346136d6a23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 MB (632979710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712166ecacc7f24fae130365bc3fbf6618194e997f5996101063ec2818bfb12d`
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
# Thu, 06 Mar 2025 15:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Mar 2025 15:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_VERSION=9.0.102
# Thu, 06 Mar 2025 15:03:40 GMT
ENV TOMCAT_SHA512=cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a
# Thu, 06 Mar 2025 15:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 06 Mar 2025 15:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Mar 2025 15:03:40 GMT
ENTRYPOINT []
# Thu, 06 Mar 2025 15:03:40 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Mar 2025 16:16:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_VERSION=16.10.5
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.5
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=ecc2d3e639273eff8ecb441aa55a8baefb87ec02826d178fb1e3aff1223dee4d
# Tue, 11 Mar 2025 16:16:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_VERSION=3.5.2
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_SHA256=f2f3c3c1a3bdaca69dd1d4e1cd8aed075242fc72ae41463ddb82e367b388f6ad
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.2
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.2.jar
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.2.jar
# Tue, 11 Mar 2025 16:16:28 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Mar 2025 16:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 16:16:28 GMT
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
	-	`sha256:a764e64196b52daf7bbc53db90ab9c51e680df7eaf1799b3396fa43ea917d1bc`  
		Last Modified: Thu, 06 Mar 2025 19:07:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7f2e569f5134efb72d3d959997bb1de5d3938650d6637eb55558ac0a84d5a7`  
		Last Modified: Thu, 06 Mar 2025 19:15:30 GMT  
		Size: 13.5 MB (13478721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f398f7259bb0d5c638bbb37ade3f6c25439a41fe9f5c12bf7c59170206dade4`  
		Last Modified: Thu, 06 Mar 2025 19:15:30 GMT  
		Size: 15.2 MB (15202225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b492ae51a91a919ae162f71196e48534ac3de52e186bbcb005894d959eface4a`  
		Last Modified: Thu, 06 Mar 2025 20:12:55 GMT  
		Size: 188.9 MB (188874996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849bd2e17dfd7483db40a33bcc994e7e0c6db811d43d81981c9bb517d5587bac`  
		Last Modified: Tue, 11 Mar 2025 17:45:39 GMT  
		Size: 316.8 MB (316789906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af3c0260a8fcc31566abc85edceb8cd7d3eecc4f431a938d9ed97fe8861100`  
		Last Modified: Tue, 11 Mar 2025 17:47:13 GMT  
		Size: 688.7 KB (688724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25e22775ecf7750b97b14355ea7511092f6eddc9b509a88235ab33d0e91814d`  
		Last Modified: Tue, 11 Mar 2025 17:47:13 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3df5c04a31c9c52ed6c10850124768cffef8c3f4a6801c2ae766897fa07b883`  
		Last Modified: Tue, 11 Mar 2025 17:47:13 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ce5c73046ae2d07ab0cff319d5e06677f6e1b08df02e5bb3d325f5fd3526a9`  
		Last Modified: Tue, 11 Mar 2025 17:47:13 GMT  
		Size: 6.6 KB (6625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218ef6654253860a79bf1d73b1c1ae0017bc7dd04ce8f713c3838169499df784`  
		Last Modified: Tue, 11 Mar 2025 17:47:14 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:9ee059eacde008de950e6d03004cd8431d3bffdf81029f6856b55686da06025a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8799635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b12f6564302a0b2f5af6790974b7dc3f9719976cac4eaaf792cb318d16a92cd`

```dockerfile
```

-	Layers:
	-	`sha256:c57c9519ee8711e067efeccf0a3f13af39a150fd95f175075c2afdb581425d70`  
		Last Modified: Tue, 11 Mar 2025 17:47:13 GMT  
		Size: 8.8 MB (8758976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21d98865b660fa3933cf98fb36d0ef7bd740db68882c69d91e0ec270a0c8652`  
		Last Modified: Tue, 11 Mar 2025 17:47:13 GMT  
		Size: 40.7 KB (40659 bytes)  
		MIME: application/vnd.in-toto+json
