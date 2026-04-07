## `xwiki:17-mysql-tomcat`

```console
$ docker pull xwiki@sha256:5f0092a9babc8aa3ddd155ed36f627d5c4599a9f31a5f9fbd05001f86bc2c382
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b012e883c8e200d2b2890344b3764305a1c146f1bb07c56ae2f3fc8d5c6582cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639185929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b57106dd7d3c4b5beef08a37c7ad3ac775a13bb143532530c4b1b668269a94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:36 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 07 Apr 2026 01:52:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:52:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:52:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:52:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:30:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 03:30:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:30:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 03:30:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 03:30:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_MAJOR=10
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_VERSION=10.1.54
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Tue, 07 Apr 2026 03:30:30 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 03:30:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 03:30:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 03:30:37 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 03:30:37 GMT
CMD ["catalina.sh" "run"]
# Tue, 07 Apr 2026 05:04:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 07 Apr 2026 05:04:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:04:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:04:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 07 Apr 2026 05:04:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 07 Apr 2026 05:04:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 07 Apr 2026 05:04:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:04:10 GMT
ENV XWIKI_VERSION=17.10.5
# Tue, 07 Apr 2026 05:04:10 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.5
# Tue, 07 Apr 2026 05:04:10 GMT
ENV XWIKI_DOWNLOAD_SHA256=686d7d548e801b061add84e58be1f015a1949f0899cfb230435e0f3dbdf8aaa2
# Tue, 07 Apr 2026 05:04:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 07 Apr 2026 05:04:31 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Tue, 07 Apr 2026 05:04:31 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Tue, 07 Apr 2026 05:04:31 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Tue, 07 Apr 2026 05:04:31 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Tue, 07 Apr 2026 05:04:31 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Tue, 07 Apr 2026 05:04:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 07 Apr 2026 05:04:31 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 07 Apr 2026 05:04:31 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 07 Apr 2026 05:04:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 07 Apr 2026 05:04:31 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:04:31 GMT
VOLUME [/usr/local/xwiki]
# Tue, 07 Apr 2026 05:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:04:31 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b68b8ef47fdb988fb4023edbb2a8d6a19ba659a4921fc9f25c496fe28ae1ef1`  
		Last Modified: Tue, 07 Apr 2026 01:51:50 GMT  
		Size: 17.0 MB (16983568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9370ed7c35a22ef566a4d1ee7eb152dc6f37abe64e4fc7df70647fa0499dc`  
		Last Modified: Tue, 07 Apr 2026 01:52:20 GMT  
		Size: 53.0 MB (52985505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef302449c04c900de9660d789c58e12374e181f0204d02016bf10d05a2ea02`  
		Last Modified: Tue, 07 Apr 2026 01:52:19 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9425bf26e9ee5e1bdec0dd158e59f754d3f4b3866a00a320bf3dafdf1a133d42`  
		Last Modified: Tue, 07 Apr 2026 01:52:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c9795ba8e7d43886e47c9f28f417b2ad6594c5ba4081bd0f3079a1a17c92b3`  
		Last Modified: Tue, 07 Apr 2026 03:30:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415216d03967c36779ab9218ed04e2d48721c138ee3007af7305157c05d21243`  
		Last Modified: Tue, 07 Apr 2026 03:30:45 GMT  
		Size: 14.3 MB (14301303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298a021259cbe800fc2783c266cf2edbfe485bf898fa08ccf32f52653362586a`  
		Last Modified: Tue, 07 Apr 2026 03:30:45 GMT  
		Size: 224.9 KB (224915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce2b307e711e3bdfefdadde0b2e20f0e793dafe7aff7eb31a531f3866e00a2`  
		Last Modified: Tue, 07 Apr 2026 05:05:09 GMT  
		Size: 191.2 MB (191191171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4bb3195dedc1b972c25e0a637a25446d2e8fc0b78845a7720179d7ac280fda`  
		Last Modified: Tue, 07 Apr 2026 05:05:17 GMT  
		Size: 331.3 MB (331304799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640cc1a195766540607c362073fe30ceb0da6ad1e76e705bfc4f83b211ed1681`  
		Last Modified: Tue, 07 Apr 2026 05:05:03 GMT  
		Size: 2.4 MB (2441658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4190d822c8f6ad0e1c71a1821a85199b602f3e351d86311ab6e39801d6e37c1`  
		Last Modified: Tue, 07 Apr 2026 05:05:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f6efe394b90445ea86cd82508db0ae396a8c72e1fb06ef4f8a73f37aa91b70`  
		Last Modified: Tue, 07 Apr 2026 05:05:05 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39e9e701937608431b51937dfa8884e10e1eb5157d6b2d78d906a54cdb00389`  
		Last Modified: Tue, 07 Apr 2026 05:05:05 GMT  
		Size: 10.7 KB (10673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77519bc247f8500dcff4baffb54522456a35e9334f2de6ced85b5773ba8fc395`  
		Last Modified: Tue, 07 Apr 2026 05:05:06 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:f55b258de813d808d0d9de47a1a0fef24b71bd090099f96c15c7dbdecdff5004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc09e5ac9c37a0bbcd4705b58def86612ee37873e6b2a812b91963bcbf39a8d`

```dockerfile
```

-	Layers:
	-	`sha256:c2aad6d6331f0dbf682e34cf18ec3e0c98c85399fceb9b7fd92b32bb961f6bed`  
		Last Modified: Tue, 07 Apr 2026 05:05:04 GMT  
		Size: 9.2 MB (9180967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0cf6b38296723c6b929856ba7c34abbc13f7d60307b755433cf57a9bc68c14e`  
		Last Modified: Tue, 07 Apr 2026 05:05:03 GMT  
		Size: 41.5 KB (41495 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8b5b6a4a17df601378df416903ce44f90b1205bf354cc63b6baa6a7a22355737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 MB (635172837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf5da3296df99abffb9a70067c86f78a7b83c519443a15da81c8489d640e2f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 07 Apr 2026 01:55:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 05:10:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 05:10:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:10:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 05:10:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 05:10:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_MAJOR=10
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_VERSION=10.1.54
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Tue, 07 Apr 2026 05:10:01 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 05:10:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:10:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 05:10:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 05:10:09 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 05:10:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 07 Apr 2026 05:24:48 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 07 Apr 2026 05:24:48 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:24:48 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:24:48 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 07 Apr 2026 05:24:48 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 07 Apr 2026 05:24:48 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 07 Apr 2026 05:24:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:24:48 GMT
ENV XWIKI_VERSION=17.10.5
# Tue, 07 Apr 2026 05:24:48 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.5
# Tue, 07 Apr 2026 05:24:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=686d7d548e801b061add84e58be1f015a1949f0899cfb230435e0f3dbdf8aaa2
# Tue, 07 Apr 2026 05:25:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 07 Apr 2026 05:25:09 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Tue, 07 Apr 2026 05:25:09 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Tue, 07 Apr 2026 05:25:09 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Tue, 07 Apr 2026 05:25:09 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Tue, 07 Apr 2026 05:25:09 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Tue, 07 Apr 2026 05:25:09 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 07 Apr 2026 05:25:09 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 07 Apr 2026 05:25:09 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 07 Apr 2026 05:25:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 07 Apr 2026 05:25:09 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:25:09 GMT
VOLUME [/usr/local/xwiki]
# Tue, 07 Apr 2026 05:25:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:25:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc1fe49c2f79e04d9e562ce4ee017e874bf7e23feea81b6df6f351ab993d9b5`  
		Last Modified: Tue, 07 Apr 2026 01:55:07 GMT  
		Size: 17.0 MB (16996238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538e758f95d8493adbf608ecfa760b05bb49d3ceee0f1e637ca69598f3434ea6`  
		Last Modified: Tue, 07 Apr 2026 01:55:40 GMT  
		Size: 52.2 MB (52155642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0252f321812c22ad7139fe93995a4ab816f331d23ab15579dedbc1027f1ca`  
		Last Modified: Tue, 07 Apr 2026 01:55:39 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f199c35f5162fea3c8f07eef1e388cab02e2e3f619c9b2842b8bcd77a768e1e`  
		Last Modified: Tue, 07 Apr 2026 01:55:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac5f94c5bcca79f12bddc6c46eb7fa6c04e4e0e9ed03895d1a50ef57c72bb4b`  
		Last Modified: Tue, 07 Apr 2026 05:10:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908a696e504aba798cd3c2d7427bb96e96f3b09202e8c8142034cb000c030d62`  
		Last Modified: Tue, 07 Apr 2026 05:10:18 GMT  
		Size: 14.3 MB (14303384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f112508064b8beb36c4dfc19b3697a983e5ded489ff63aef3a3905f0f61481`  
		Last Modified: Tue, 07 Apr 2026 05:10:18 GMT  
		Size: 225.3 KB (225282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f664ed7c5e43d65b7ed03c3308aea830907b4b9268745db0ac0a28e00b4ca0a`  
		Last Modified: Tue, 07 Apr 2026 05:25:47 GMT  
		Size: 188.9 MB (188852172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7f4bfc0a1a3815c2eaf52bf19f4c049cbba5d543509fd23cc0dad0b5c82d55`  
		Last Modified: Tue, 07 Apr 2026 05:25:50 GMT  
		Size: 331.3 MB (331304823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf55f33cd8e81bde54be23e6cff3f1c280f7bedcb6802746177b30b19f1837a`  
		Last Modified: Tue, 07 Apr 2026 05:25:42 GMT  
		Size: 2.4 MB (2441661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f448c8ce0df0001334ec22a4bf5a5ba52bdb7adf029c0d559dc33949d3a20c17`  
		Last Modified: Tue, 07 Apr 2026 05:25:42 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b8050c3f749efde70c1d4f49f839ecc0d49b66940fd73521525d72530d6db4`  
		Last Modified: Tue, 07 Apr 2026 05:25:43 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9052cdbb4102b42b670388dcc12837697342c7a46f15d4c65cd1d0a8de207ef`  
		Last Modified: Tue, 07 Apr 2026 05:25:43 GMT  
		Size: 10.7 KB (10672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3b98c506c1754d2a5571a965147f302fb8a44beef6049e82052bf9bb28579`  
		Last Modified: Tue, 07 Apr 2026 05:25:44 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:69cf2a5abdeff07384bbd4d3cb2e47e55500e01a359a46500f421093a894adcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e736776dadec9a4aa8286e1bfa34858d9b19a5a6aa8069323ad2bbf8f99dfd9`

```dockerfile
```

-	Layers:
	-	`sha256:19b33c2135ffcb24347f06d8cdb8ba8668f366faa2aede85fcd06610c8c8f301`  
		Last Modified: Tue, 07 Apr 2026 05:25:42 GMT  
		Size: 9.2 MB (9181756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d796d22cc46c04a02100e9d89ee4cf4a9c88201bebf2d7a21945f39e00a37921`  
		Last Modified: Tue, 07 Apr 2026 05:25:41 GMT  
		Size: 41.7 KB (41704 bytes)  
		MIME: application/vnd.in-toto+json
