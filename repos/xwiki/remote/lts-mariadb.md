## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:edf905548561a0f3515eec0f45c70e12c0ba8a80505183aa9f4395a9894d5b5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:490302447798086671cd086f1dc917829f719b75bd849df20c86ebf0ccf2e50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615867801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6c114a7bf316873e2a945224e93c18378167321513972ab4beb41600243e2a`
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
# Thu, 26 Dec 2024 14:50:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 26 Dec 2024 14:50:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2024 14:50:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 26 Dec 2024 14:50:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 26 Dec 2024 14:50:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2024 14:50:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
WORKDIR /usr/local/tomcat
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 26 Dec 2024 14:50:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_MAJOR=9
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_VERSION=9.0.98
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Thu, 26 Dec 2024 14:50:58 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT []
# Thu, 26 Dec 2024 14:50:58 GMT
CMD ["catalina.sh" "run"]
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 26 Dec 2024 14:50:58 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_VERSION=16.10.2
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.2
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_DOWNLOAD_SHA256=1a6287416db4243e3d40939e19509ca4ebe9e4f46f8fcf7204f223bcfff8b6e2
# Thu, 26 Dec 2024 14:50:58 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Thu, 26 Dec 2024 14:50:58 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
VOLUME [/usr/local/xwiki]
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2024 14:50:58 GMT
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
	-	`sha256:128103dd90cf1f23c6d9eed45501bd0f13e16d6a737b1540f1991d9f651d632d`  
		Last Modified: Wed, 22 Jan 2025 21:11:57 GMT  
		Size: 191.1 MB (191149454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327e4ba1a1bf6633ce267b5a74833af551571f37167ac222a018b9813f2700c8`  
		Last Modified: Wed, 22 Jan 2025 21:12:00 GMT  
		Size: 316.7 MB (316697566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098e558eabdff41c8cbd607959d843a41c53144214569545db09589f8ccc3e4b`  
		Last Modified: Wed, 22 Jan 2025 21:11:53 GMT  
		Size: 681.3 KB (681257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ced6380a268e7b45e8379b9d9cadad941c65d2a07964dc382516b6239b9bc1e`  
		Last Modified: Wed, 22 Jan 2025 21:11:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c4c7c4fb1fa40c6190d6fa0adcfe09a07d48821a36930d53406f29199dfa7d`  
		Last Modified: Wed, 22 Jan 2025 21:11:54 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b68176618e5ed3c035afdd9440c4c7b3f2e3bbed0b8263d215a9939b199d75`  
		Last Modified: Wed, 22 Jan 2025 21:11:54 GMT  
		Size: 6.6 KB (6599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a2eae20caac27cab94fe093aa278923b9576ad4f3e40f24026714d22448d13`  
		Last Modified: Wed, 22 Jan 2025 21:11:55 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:6df5badfe97c121dbf8a5c1a96a13136206bfa70627e2f2a01490948685ef461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54729260dea9cdd5e22c0182aa068c3325b8e22d7217754bdc91b99ed43f20c7`

```dockerfile
```

-	Layers:
	-	`sha256:dac7137fd27b9b5b6b074db99651820dee01fec425b0fa91035717f13a03dbe7`  
		Last Modified: Wed, 22 Jan 2025 21:11:52 GMT  
		Size: 8.8 MB (8753594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:511271cb977f22a08fc4b886e4680abb53450a5fe3a67fc8943fd25124939842`  
		Last Modified: Wed, 22 Jan 2025 21:11:52 GMT  
		Size: 41.4 KB (41436 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d16223d165264ca8f9bf2ad1b56576c17042150311bcf56abfbf07e55cd36fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.7 MB (613680110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3de5233282a89e961040c5c0d05b8ba05510ec09e1c666b8777e1146474cb76`
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
# Thu, 26 Dec 2024 14:50:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 26 Dec 2024 14:50:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2024 14:50:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 26 Dec 2024 14:50:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 26 Dec 2024 14:50:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2024 14:50:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
WORKDIR /usr/local/tomcat
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 26 Dec 2024 14:50:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_MAJOR=9
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_VERSION=9.0.98
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Thu, 26 Dec 2024 14:50:58 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT []
# Thu, 26 Dec 2024 14:50:58 GMT
CMD ["catalina.sh" "run"]
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 26 Dec 2024 14:50:58 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_VERSION=16.10.2
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.2
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_DOWNLOAD_SHA256=1a6287416db4243e3d40939e19509ca4ebe9e4f46f8fcf7204f223bcfff8b6e2
# Thu, 26 Dec 2024 14:50:58 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Thu, 26 Dec 2024 14:50:58 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
VOLUME [/usr/local/xwiki]
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2024 14:50:58 GMT
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
	-	`sha256:cf59fe94091d1133c5271367782e6890dc049bed88c33702a2b10ef33e5078d2`  
		Last Modified: Thu, 23 Jan 2025 04:50:51 GMT  
		Size: 316.7 MB (316697562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d85f485e794ccae52e300163a11bfd62f10805ee52ffc12750c61a7491ea8e8`  
		Last Modified: Thu, 23 Jan 2025 04:52:18 GMT  
		Size: 681.3 KB (681258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4179ab1cc21e4830893533d62ad392fcd2c6a94569053306dc711ca017744e22`  
		Last Modified: Thu, 23 Jan 2025 04:52:18 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2d8c5ff896786ea5c3caed84662291e7f05418738c2fc694edbc29b7b6304`  
		Last Modified: Thu, 23 Jan 2025 04:52:18 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b20d5bb99e6313181227c7d1ca5668034d8c2f0448a15130d43afcb85df625`  
		Last Modified: Thu, 23 Jan 2025 04:52:18 GMT  
		Size: 6.6 KB (6593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20145b94c0948ecf3874608932925bf4bfabab56d0c3327af5f334a48d8077c`  
		Last Modified: Thu, 23 Jan 2025 04:52:19 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:e45114010b668745a0fce300c31ecde51673e0bb5f7739f9a643d87311c41183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8796012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e252efabf8e5be2d423cbdb65f71af50e6e0bf86365372336ef66ce5a11b0d7`

```dockerfile
```

-	Layers:
	-	`sha256:f2287956a2b16b86790cb5b34c376e04d36a06b8d0702bc430d2099f6b1f7364`  
		Last Modified: Thu, 23 Jan 2025 04:52:17 GMT  
		Size: 8.8 MB (8754371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54536e11f8fbca7950ac9f87dcff2b5b548adc62b0987ec9f97c3ee704a22824`  
		Last Modified: Thu, 23 Jan 2025 04:52:17 GMT  
		Size: 41.6 KB (41641 bytes)  
		MIME: application/vnd.in-toto+json
