## `xwiki:16-mysql-tomcat`

```console
$ docker pull xwiki@sha256:a5806d6afd9d360165dd415c0dc3363a15c15372d1d9e66c4cdcee2aa6b15cb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:27a20486b2bc1405cba5cc7dba3e21dde66d4c77f22a064e44d7430e9a3b5287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.4 MB (624428752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51456ea3713f1fa599f0a71a2b785712358fe9e577f878728c1aecb0d889df6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 08:06:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 08:06:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 08:06:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 08:06:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Jul 2025 08:06:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 08:06:53 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Jul 2025 08:06:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_MAJOR=9
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_VERSION=9.0.108
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Thu, 31 Jul 2025 08:06:53 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT []
# Thu, 31 Jul 2025 08:06:53 GMT
CMD ["catalina.sh" "run"]
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 31 Jul 2025 08:06:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_VERSION=16.10.10
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.10
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=85dee4db22bb98bde66c4f7b379251f2d86f6ac3e6e92449e3b79a921e0192fd
# Thu, 31 Jul 2025 08:06:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_VERSION=9.3.0
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_SHA256=6c8e6692b521376d89bc5618c16cdeaf8c61854329f4fa25677ed08776c5bb76
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.3.0
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.3.0.jar
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.3.0.jar
# Thu, 31 Jul 2025 08:06:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
VOLUME [/usr/local/xwiki]
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Jul 2025 08:06:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1ceb63b80a861ae319235f3b1e3e392279a30c5cc9f0dec5c5582505b55f8`  
		Last Modified: Tue, 12 Aug 2025 17:24:47 GMT  
		Size: 17.0 MB (16971683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b74addfec2b46a83d8e9d131c7c6563aa4399f142b91d977d506f6c137dcb`  
		Last Modified: Tue, 12 Aug 2025 17:25:01 GMT  
		Size: 53.0 MB (52968913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac95b0cea99b9ed5ddc084d329fc5e139c2adde65e599e4f9803bd9aa474ef`  
		Last Modified: Tue, 12 Aug 2025 17:24:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cce32af8d45a5194c78928090c5748f048a001dcd13b737c7a2992892753871`  
		Last Modified: Tue, 12 Aug 2025 17:24:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048acea221768da20725347d2ca1930edd926946b945247a95c036f37ac46d36`  
		Last Modified: Tue, 12 Aug 2025 18:08:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4039141278925b609c33ca139b6e0b13dd6ab0d4b1ac9fe4f6e58436a9eea9a7`  
		Last Modified: Tue, 12 Aug 2025 18:08:58 GMT  
		Size: 13.7 MB (13714791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7118dfe85abe7d4fd72eb30fb7ea3047bae30f860b6f613c14e52e5bb20ba948`  
		Last Modified: Tue, 12 Aug 2025 18:08:56 GMT  
		Size: 224.7 KB (224673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6d4656046fa2d852c0817597d1156a5d1ea185ee44a165d03ee1917224746b`  
		Last Modified: Tue, 12 Aug 2025 21:10:08 GMT  
		Size: 191.2 MB (191179030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdf83c93cb8eca73922a2e0cfd54edfd3df3063bcfe6a8978b895a6febd8493`  
		Last Modified: Tue, 12 Aug 2025 21:10:17 GMT  
		Size: 317.2 MB (317199344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526670cb8ab8871daee574b8b02eff12986d10231d86e69f7f6f398b10d7dc30`  
		Last Modified: Tue, 12 Aug 2025 19:16:34 GMT  
		Size: 2.4 MB (2431602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e289c0b766881bdc2182f667a202a92c7179fd64a7237e1fec78648b696233`  
		Last Modified: Tue, 12 Aug 2025 19:04:04 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12f4ca676b0d3b49ec55a3243875036ac4af1fff0c8d6d2183b1fd31edcfa64`  
		Last Modified: Tue, 12 Aug 2025 19:16:33 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa5a909f8a690bce16abc448c3b6a6a3ebf547c40da330df043557f47907d9f`  
		Last Modified: Tue, 12 Aug 2025 19:16:32 GMT  
		Size: 6.6 KB (6630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc16acff4150f72833b6b2d6a65022c37e1f88c8181106eda04282bad76564d`  
		Last Modified: Tue, 12 Aug 2025 19:16:34 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:375b9560e87087f5d0502bbcb8d61c788f957499985df53ac7f5b2e1d898345c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9147074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b94ce94ef0974c1da980115486f2e0baab40f3ab23f4bc952d6101815139d77`

```dockerfile
```

-	Layers:
	-	`sha256:189cd3ebd15bba663211a8fe8978a07fedd360db08dd24f1f7712185efbb11a0`  
		Last Modified: Tue, 12 Aug 2025 21:07:19 GMT  
		Size: 9.1 MB (9105538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c2ec4851ae79fdcf3dd0654752ef8de89c64aad3ff2b5d3d4243babcaf59a5`  
		Last Modified: Tue, 12 Aug 2025 21:07:20 GMT  
		Size: 41.5 KB (41536 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:6f5fa8e94991dd436cac941835d64e9fa255f9de4d9ff97a4715658e4a33b095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.4 MB (620436160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6f341749b017f64948daaafc8ee42420cfe482ba2b4e7d77605395bce71898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 08:06:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 08:06:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 08:06:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 08:06:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Jul 2025 08:06:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 08:06:53 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Jul 2025 08:06:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_MAJOR=9
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_VERSION=9.0.108
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Thu, 31 Jul 2025 08:06:53 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT []
# Thu, 31 Jul 2025 08:06:53 GMT
CMD ["catalina.sh" "run"]
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 31 Jul 2025 08:06:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_VERSION=16.10.10
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.10
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=85dee4db22bb98bde66c4f7b379251f2d86f6ac3e6e92449e3b79a921e0192fd
# Thu, 31 Jul 2025 08:06:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_VERSION=9.3.0
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_SHA256=6c8e6692b521376d89bc5618c16cdeaf8c61854329f4fa25677ed08776c5bb76
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.3.0
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.3.0.jar
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.3.0.jar
# Thu, 31 Jul 2025 08:06:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
VOLUME [/usr/local/xwiki]
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Jul 2025 08:06:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3eefddfbcab06ca4f10ce56a232d4ec2d822b72ac91b8958abc9acd3c4223c`  
		Last Modified: Tue, 12 Aug 2025 18:31:54 GMT  
		Size: 17.0 MB (16988833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2683f57ecc3239b77668933adbcb066b796b3d8385694028dfa534473428efe9`  
		Last Modified: Tue, 12 Aug 2025 18:39:53 GMT  
		Size: 52.1 MB (52148453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1835951682aea5916d97b15850e70d45156732945ac0dbb2535d8c6306228f`  
		Last Modified: Tue, 12 Aug 2025 18:39:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766ee17d70f62cab7ff1f4f47b0567a37c24335c88c58b652cb5b22e4f7e92e0`  
		Last Modified: Tue, 12 Aug 2025 18:39:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8672b50cb4a092687fe9a28d3978851b924618ac39a15dae4dadfaadaf822e`  
		Last Modified: Wed, 13 Aug 2025 14:31:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745e7b18fef68c2dc0727ebca6a566adfbcf521cd41c00458a712681effe3eb0`  
		Last Modified: Wed, 13 Aug 2025 14:36:03 GMT  
		Size: 13.7 MB (13728952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dadd24cb1a7cf3a62f14194b36c6a42b20a1c57d6cd0680e1c3658f6a65be91`  
		Last Modified: Wed, 13 Aug 2025 14:36:01 GMT  
		Size: 225.1 KB (225136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219819923fb989a7f43488cca289ed02e2602c2f14b3e4a53f2a926ef1761709`  
		Last Modified: Wed, 13 Aug 2025 21:55:08 GMT  
		Size: 188.8 MB (188837856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bb3794cde91907e61b44269b1dcc6e73f715e229912970ea22a65e6fb22c65`  
		Last Modified: Wed, 13 Aug 2025 21:55:38 GMT  
		Size: 317.2 MB (317199458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc00896354fedaa17fc27a8ae0b4c650bb22bcf644f53a91cce3c879f58530f`  
		Last Modified: Wed, 13 Aug 2025 19:11:11 GMT  
		Size: 2.4 MB (2431599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa798721f7ef213748b80b2da334837218d9fdc780c92cba433866594b11f70`  
		Last Modified: Wed, 13 Aug 2025 19:11:11 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9184ec62ce2579ac679ebdcd2826297e31c6e492a28cd772b80f38c718b2ba`  
		Last Modified: Wed, 13 Aug 2025 19:49:02 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b164c4b3b0e26d1c95f1b1e82fce2ba967fc6270905dc4e1b8da777ae5459753`  
		Last Modified: Wed, 13 Aug 2025 19:49:01 GMT  
		Size: 6.6 KB (6629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48fdca70bb552f5e1538ae7346576ff80876891d330d225792a3b4c248aeda3`  
		Last Modified: Wed, 13 Aug 2025 19:49:01 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:5dec8df5dba39fbbd6f9a4621bfa4fefab448533d33b410110c3740375531b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9148073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62035c8cbf0be248232753659fc5f284cde372bbbb34ae7051af99910b5e84d1`

```dockerfile
```

-	Layers:
	-	`sha256:c98f09cad4946694ba504167bb530057eefa0b54c35627e7ff87f6477c95b07e`  
		Last Modified: Wed, 13 Aug 2025 21:07:42 GMT  
		Size: 9.1 MB (9106327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33bdbf1c9c475dd1655ef07737f8f706d3ddf9721e975c701ecb4013ae8514aa`  
		Last Modified: Wed, 13 Aug 2025 21:07:43 GMT  
		Size: 41.7 KB (41746 bytes)  
		MIME: application/vnd.in-toto+json
