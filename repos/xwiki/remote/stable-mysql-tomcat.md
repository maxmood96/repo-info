## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:5e0f4b63f1db9ecb461936d84b1ed43820f798081f7ae3233e165a656ac7abf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:9195b9529b6193433ddbb8dc385993a3b284996294b799604533424212eb6084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.6 MB (617620934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4a1e58016e30f7e20f5bbc82fc5dbba93ca665ae72d704daf98d9b705c3e39`
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
ENV MYSQL_JDBC_VERSION=9.1.0
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Thu, 26 Dec 2024 14:50:58 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:21aca1af90355148d7da10ab19bab1a272a50660b51faf73dc48d4c6e1e007ac`  
		Last Modified: Wed, 22 Jan 2025 21:11:36 GMT  
		Size: 191.1 MB (191149559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9c65498d95e449aa1abb8c6cf7eb77159e0f81e4c248fbcdedc1e04d9840d`  
		Last Modified: Wed, 22 Jan 2025 21:11:38 GMT  
		Size: 316.7 MB (316697587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb84e046acb8a1f28335a0006cee386c4f1ee505702e2b8e8b084de5d52b1b7c`  
		Last Modified: Wed, 22 Jan 2025 21:11:35 GMT  
		Size: 2.4 MB (2434173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0ccc23f49a03b6d02ea738ac382fbe9be7a340ac67fe09e379dfb736b130aa`  
		Last Modified: Wed, 22 Jan 2025 21:11:33 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9096539e97f2cb402935b56e1bbd8eafea3f5802028b96ae81181bbbd32a84`  
		Last Modified: Wed, 22 Jan 2025 21:11:34 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dceaaff0855aa54ce4b6fb6ffb77fb7c949ca4a7af18e9bf2e50c8395749c1`  
		Last Modified: Wed, 22 Jan 2025 21:11:35 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ee99ac1f238bdd16d9ddabf6496c37dc83bd9951a38bb11e2ff593b6dffdec`  
		Last Modified: Wed, 22 Jan 2025 21:11:36 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:be6b2071ca6e0355bb2242a7b6f8e1c2abb4aec85d8816650ef2193b2494e090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8798456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6c0fd968e4a1509747514ef10ae6c7533863294e20cd18363cbbc7531bfc3b`

```dockerfile
```

-	Layers:
	-	`sha256:5c0add8410d97b2667ba11b8be8bbf9a24ba0e08c34c2be4a6ff0b52c25b0783`  
		Last Modified: Wed, 22 Jan 2025 21:11:33 GMT  
		Size: 8.8 MB (8755395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96c5bba21b2bd3addd437f635828d4d5c3cbf4b548ab4847bf3cdaaa8fde3e6e`  
		Last Modified: Wed, 22 Jan 2025 21:11:33 GMT  
		Size: 43.1 KB (43061 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:043af5ffc3e5d575ea20c5437f1cbd08cca9c8c2db10cd1926b1ffb9ec352a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.5 MB (614481956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27772d78357108f62012e91b183f31acf5d6966711033ac87548fae7833414aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
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
ENV MYSQL_JDBC_VERSION=9.1.0
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Thu, 26 Dec 2024 14:50:58 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:636d6d39497cde5edbefcc48f9d73d53c8b5408b69b8cc70ceb265af74eba9e2`  
		Last Modified: Tue, 03 Dec 2024 05:48:36 GMT  
		Size: 17.0 MB (16981577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c00ca83c9141f23bb773168f443dd5ebfe15eb9251d848d166d8fff3158e24e`  
		Last Modified: Tue, 03 Dec 2024 05:51:23 GMT  
		Size: 46.4 MB (46430917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5c0bfb583c70e3d3b37ce5b84ddaf77609232633842ecaf5813b86ce4d4af2`  
		Last Modified: Tue, 03 Dec 2024 05:51:21 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7573b7342583b03280fa66f7b674dec2151c223902f20c24aa397d98d85f88f`  
		Last Modified: Tue, 03 Dec 2024 05:51:21 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7262991182989bcbde11009a69b17999af5df3cd07d4d8b95114ad70dfccd8`  
		Last Modified: Tue, 14 Jan 2025 11:56:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16ffe8fdbf7ab23da3b356cb66e1d5117fbf163fe1e9805854d52ebb95d7b7c`  
		Last Modified: Tue, 14 Jan 2025 12:00:37 GMT  
		Size: 13.5 MB (13450954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14679ef59efb92a67a72ae685e193fe16627744fa280e33b7ad6e6d57a68787`  
		Last Modified: Tue, 14 Jan 2025 12:00:37 GMT  
		Size: 223.9 KB (223950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9c7e2d2ab4557840b2b4e664d5279b244123fec74d622662a68247c29b0ee3`  
		Last Modified: Tue, 14 Jan 2025 16:01:13 GMT  
		Size: 189.4 MB (189354726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a702bd4d9175d8d8e0bd272b97724341507780f45d2f42873420492a62a16907`  
		Last Modified: Tue, 14 Jan 2025 16:01:15 GMT  
		Size: 316.7 MB (316697530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbcedbe6023daa8da461af19d8cdfb4b922b66dce482ca73f9b49ffae46f3c1`  
		Last Modified: Tue, 14 Jan 2025 16:01:09 GMT  
		Size: 2.4 MB (2434170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5d4f0f940a4f902ada9bd9710ddd513497d1b11bf5ae9176088432a3176fc`  
		Last Modified: Tue, 14 Jan 2025 16:01:09 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23240d39170cfda621a7ed959225684f55ccec179e8d33652428475c55f7d17`  
		Last Modified: Tue, 14 Jan 2025 16:01:10 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92936f4c8d219fc474b54c227661bdaf61d708592d8ba1d62b282e4e92039b8e`  
		Last Modified: Tue, 14 Jan 2025 16:01:10 GMT  
		Size: 6.6 KB (6595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f9e41d8a6c7e681bc6584f6479e8372f707012546588bb99cf53f7b63c9767`  
		Last Modified: Tue, 14 Jan 2025 16:01:11 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:428fa3ff39551d08ad14fd5664d93b5764d8f0b0ce73b61723b8a91755492276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8799574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca646c5dca378453cb5810ac2e338a5190a6fe29d85b60640b9bbc132d787c3a`

```dockerfile
```

-	Layers:
	-	`sha256:4371cec18bba54e4fe92e26ec7b33d20897a3089eed75ccbba6f7bc047e51170`  
		Last Modified: Tue, 14 Jan 2025 16:01:09 GMT  
		Size: 8.8 MB (8756244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c2cbbcc7577384b726762e65bb2de24730cda0c2af335eeebf0ebce94cf37f`  
		Last Modified: Tue, 14 Jan 2025 16:01:09 GMT  
		Size: 43.3 KB (43330 bytes)  
		MIME: application/vnd.in-toto+json
