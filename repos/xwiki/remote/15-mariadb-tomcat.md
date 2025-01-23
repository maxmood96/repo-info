## `xwiki:15-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:8ff78b23ec10875568f9f872527b5e41cd9b9e376db54143e9eff7d8d46a96bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:3e4fae17b98fe761eeae623a03ed326b857a3fd4d06d7f6f75f4ddec459474a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.4 MB (606417511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a88cf0d021638ad77c339a80204ff748a35c09d873ea93285a2d8d11e0377f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
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
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 16 Jan 2025 09:27:38 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
ENV XWIKI_VERSION=15.10.16
# Thu, 16 Jan 2025 09:27:38 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.16
# Thu, 16 Jan 2025 09:27:38 GMT
ENV XWIKI_DOWNLOAD_SHA256=c3a7bca6a05cf185ecfbea6df886c5764c6e0fcfdfce988498909911ebe98dda
# Thu, 16 Jan 2025 09:27:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Thu, 16 Jan 2025 09:27:38 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
VOLUME [/usr/local/xwiki]
# Thu, 16 Jan 2025 09:27:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 09:27:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2cb0ec536fae9a1d80cad8b56b3c05119e2b57a0d04af676008312af681aea`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 17.0 MB (16966698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587b49ab5385c6f5be0e6991c10019ab858a1af9825c21ccdda057797d644f80`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 46.9 MB (46941810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca0dfb15aaaf344fb918a4b317840752b2893048212ad3919135d3f8a3f5a04`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a2aa0ee1f1005a034027e32ac2cf1fb52534ead7ab4409e049bf1126c86c96`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22be8538e3a373858cde50e718fd497c582c5cc85de1d00774ce89d01b6ebf5c`  
		Last Modified: Wed, 22 Jan 2025 20:32:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a39ef8c389b6656116f6eff521b3d0c90c53ba7c99ab660765a3fc7e7a8833`  
		Last Modified: Wed, 22 Jan 2025 20:32:42 GMT  
		Size: 13.4 MB (13440286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c094a7a953cad2eb4fb1f2b210ec9511cc05f733f80bab36616173de25a6eda0`  
		Last Modified: Wed, 22 Jan 2025 20:32:41 GMT  
		Size: 223.4 KB (223384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d98e629a5864573e39066aaf3b46e97806c645ad50c45f28f7012e27602ed1`  
		Last Modified: Wed, 22 Jan 2025 21:11:39 GMT  
		Size: 191.2 MB (191150486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533cd4fb1a7234c57517bfd66019ab550c2b1dfe0c852d3f57692fb8328cf347`  
		Last Modified: Wed, 22 Jan 2025 21:11:41 GMT  
		Size: 307.2 MB (307246384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa552454cd30c1a878812039e12c961b3efac896c1773f9f3496d1804a27fbbc`  
		Last Modified: Wed, 22 Jan 2025 21:11:36 GMT  
		Size: 681.3 KB (681257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a71465a92a807d4a80368e22e934eab6c5a4ae465f7bb71977532f4a85c658d`  
		Last Modified: Wed, 22 Jan 2025 21:11:36 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd0cf3ba42082e88fd027919cf41b482b06ced0b1056becd8aed7bec5a4437a`  
		Last Modified: Wed, 22 Jan 2025 21:11:37 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae79bb3fcab2089e609616c843606cecff892a7d54fedaa55dd8bbe3703bad9f`  
		Last Modified: Wed, 22 Jan 2025 21:11:37 GMT  
		Size: 6.5 KB (6463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d226d91c25a00b83fa7f78f3a9c040110fb9498737cb576e4d3df87b13e9301`  
		Last Modified: Wed, 22 Jan 2025 21:11:38 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:956754d8c356d3bfe60dd1660b644ed9f6df609d22e6b2c4a6a4146d5c64d636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8785152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea502949e91651fa1535b6c7ae55a936245fa1e0a7d5b3c0cd27e07afce9a0aa`

```dockerfile
```

-	Layers:
	-	`sha256:b8eb34f270cf02f1c629e97927529af01b223653131ddae2266cb8f1b22b0ca9`  
		Last Modified: Wed, 22 Jan 2025 21:11:36 GMT  
		Size: 8.7 MB (8745284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a1fc638cb3eeb8db4e5a19d51eefd92ba3d91efbeba4768c447e4edc573701`  
		Last Modified: Wed, 22 Jan 2025 21:11:35 GMT  
		Size: 39.9 KB (39868 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:5d3e02abe96510c6b50c7fd4c9ae00c75baef447e262608fe6b63e9f93e81d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.2 MB (604228723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088b474fa106c052ce49f5de0e5d7df968171ff87a561213d844da74b332d5d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
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
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 16 Jan 2025 09:27:38 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 16 Jan 2025 09:27:38 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
ENV XWIKI_VERSION=15.10.16
# Thu, 16 Jan 2025 09:27:38 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.16
# Thu, 16 Jan 2025 09:27:38 GMT
ENV XWIKI_DOWNLOAD_SHA256=c3a7bca6a05cf185ecfbea6df886c5764c6e0fcfdfce988498909911ebe98dda
# Thu, 16 Jan 2025 09:27:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Thu, 16 Jan 2025 09:27:38 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Thu, 16 Jan 2025 09:27:38 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 16 Jan 2025 09:27:38 GMT
VOLUME [/usr/local/xwiki]
# Thu, 16 Jan 2025 09:27:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 09:27:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdecf092a77e3bcc60bf2a2f0d9bb37477afb75ca7c9781f98a76d3722450717`  
		Last Modified: Wed, 22 Jan 2025 21:06:49 GMT  
		Size: 46.4 MB (46430926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46396c1812fff3f42c7bce2cfc29c910045b7fd281e96d27491bddc27a25f4a5`  
		Last Modified: Wed, 22 Jan 2025 21:06:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1d9c149d4e66dbbc5d2f77d496f834696346b93887893c1a1b4cd3dbc46ff9`  
		Last Modified: Wed, 22 Jan 2025 21:06:48 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97be03f8c1ceae9246d08d9cad75d685289df723a3277870c2dfec2f67ff8b`  
		Last Modified: Thu, 23 Jan 2025 03:46:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c972788f94ae2ef95aac9270d0d354a6bfc6ef8a362fada80d182525b094aa`  
		Last Modified: Thu, 23 Jan 2025 03:50:46 GMT  
		Size: 13.5 MB (13450951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997c07d109b8193850dba25ad47cb23b7a65987d049595756721eda0e132646a`  
		Last Modified: Thu, 23 Jan 2025 03:50:46 GMT  
		Size: 1.7 MB (1721637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd1006b4347ffe00c828718072676317818810ed8591f616b3d37efbdf98f94`  
		Last Modified: Thu, 23 Jan 2025 04:50:49 GMT  
		Size: 188.8 MB (188806889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c1f96f792f62804d714e509c2089bcd0e809173e0463a11c5634dae22a7b2d`  
		Last Modified: Thu, 23 Jan 2025 04:53:38 GMT  
		Size: 307.2 MB (307246313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ce1a2726668768d71cd52d02769dd62cf8d65d8d7f4cae351e67d209296ba6`  
		Last Modified: Thu, 23 Jan 2025 04:54:20 GMT  
		Size: 681.3 KB (681256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b498dae86c1c2d238263ec963df75e6ff4fe97f9e1f6e6aee13af2b41de7926`  
		Last Modified: Thu, 23 Jan 2025 04:54:20 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021572a481495a8458c2260eb067c6fef23aec6044bc55e5db207656b90c4ef9`  
		Last Modified: Thu, 23 Jan 2025 04:54:20 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0665f08db114ea6145ab480b5a622c945e70ac6c0671b7f7912aebad9839b3`  
		Last Modified: Thu, 23 Jan 2025 04:54:21 GMT  
		Size: 6.5 KB (6459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ca155aea1cf22bd67c7c1e7a99abb5f0bf11f2b0cefffaae12e286f7959c22`  
		Last Modified: Thu, 23 Jan 2025 04:54:21 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b042762519e13d5ae95fb8a4277611205926b5aee43b28ced025bfc10d5d94e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8786014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abbb5aef19429383b1a44c9c59d75e15e7b39116c560ee5fe4bf2a4e8cfc7c8`

```dockerfile
```

-	Layers:
	-	`sha256:f3fb58777d1ea136e13ec37f6e236ba7032f11f509ec704146410d89072f2ba1`  
		Last Modified: Thu, 23 Jan 2025 04:54:20 GMT  
		Size: 8.7 MB (8746001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d81545244d4b2947527569bdeebda6f34d83f9f58cfde1ca690e88595ca1f04a`  
		Last Modified: Thu, 23 Jan 2025 04:54:19 GMT  
		Size: 40.0 KB (40013 bytes)  
		MIME: application/vnd.in-toto+json
