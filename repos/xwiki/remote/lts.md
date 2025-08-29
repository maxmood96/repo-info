## `xwiki:lts`

```console
$ docker pull xwiki@sha256:0d4657027cf44b377452fc96dfe38d0c70872f0f5417c000d91b6d92d5b21e1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:04e322c32df5b19bb531c175b7629ec80b2c429b000f9db429118fb4b7725078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624553839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044dd305a51697971f0ddbbdadd898c5456a809e166819b34e1358621efc46a3`
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
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:12:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:12:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_VERSION=9.0.108
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Wed, 06 Aug 2025 20:12:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:12:57 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:12:57 GMT
CMD ["catalina.sh" "run"]
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 28 Aug 2025 16:09:51 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_VERSION=16.10.11
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.11
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_DOWNLOAD_SHA256=9c1d464e35ed8f58f7b47213220db7528cd10732a7428eb9f7ee7c29adc83bbd
# Thu, 28 Aug 2025 16:09:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_VERSION=9.4.0
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_SHA256=49ed93c8b2bea9cb0929b85a8a28837b191d0f8eac6919fdcef16e36e2cd53b3
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.4.0
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.4.0.jar
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.4.0.jar
# Thu, 28 Aug 2025 16:09:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
VOLUME [/usr/local/xwiki]
# Thu, 28 Aug 2025 16:09:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 16:09:51 GMT
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
	-	`sha256:327e42e06b31355de84240f5e956aef546555e24aa5b94daa2584d8b6c1b101f`  
		Last Modified: Thu, 28 Aug 2025 18:08:36 GMT  
		Size: 191.2 MB (191178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4d1234110668afbbda312b8c4c1d74a2d7d86426d58be38cb41d6595dc86f`  
		Last Modified: Thu, 28 Aug 2025 18:09:23 GMT  
		Size: 317.3 MB (317325749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1c3b3291c5f415de1b4d65fda014aa68cd1e51e96f806800238042d25e27fc`  
		Last Modified: Thu, 28 Aug 2025 17:58:42 GMT  
		Size: 2.4 MB (2430452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fc06b0ff9604a14fae2448e075c4cc072c89b9ef99d578365d613435f9986`  
		Last Modified: Thu, 28 Aug 2025 17:58:41 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d372bb04b81602af58eb824490b93e158a0e32fb971ecd5bc9797a552f631ac`  
		Last Modified: Thu, 28 Aug 2025 17:58:41 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2f21db79da5e2fe9ac6c4bd7061673e75852bcdafa2f04dad3f885f2064ea4`  
		Last Modified: Thu, 28 Aug 2025 17:58:41 GMT  
		Size: 6.6 KB (6626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d391b8841f812ed951fff6d8ced73d013c424c2b404a21e136feef931cbc4279`  
		Last Modified: Thu, 28 Aug 2025 17:58:42 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:311c435e871a978d3cff038b4d988a6f9420864ec3097a94f1452067bbeb32eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9152279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd04e373a79daa6e56a5f2dc0a9d6f5c3c21a6d6d6c62e384230fd43944d1921`

```dockerfile
```

-	Layers:
	-	`sha256:34f754ef91b85404d16b8efee0096467e6df095e011089875bc4dc12d9a8d5b0`  
		Last Modified: Thu, 28 Aug 2025 18:07:29 GMT  
		Size: 9.1 MB (9110742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327cfcccadcee966a350269d6ad9f3a0109ee2766c5efff12a8bd560a7156e0a`  
		Last Modified: Thu, 28 Aug 2025 18:07:30 GMT  
		Size: 41.5 KB (41537 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:57a0a14e7ff337f49ec7f50ff46997653f49b50be22672bcd6550e6c0a0ac894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.6 MB (620562522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9d4463f75a32df2b583868669a9e640945d553db7afacd166f15c17153fe1`
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
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:12:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:12:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_VERSION=9.0.108
# Wed, 06 Aug 2025 20:12:57 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Wed, 06 Aug 2025 20:12:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:12:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:12:57 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:12:57 GMT
CMD ["catalina.sh" "run"]
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 28 Aug 2025 16:09:51 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_VERSION=16.10.11
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.11
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_DOWNLOAD_SHA256=9c1d464e35ed8f58f7b47213220db7528cd10732a7428eb9f7ee7c29adc83bbd
# Thu, 28 Aug 2025 16:09:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_VERSION=9.4.0
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_SHA256=49ed93c8b2bea9cb0929b85a8a28837b191d0f8eac6919fdcef16e36e2cd53b3
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.4.0
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.4.0.jar
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.4.0.jar
# Thu, 28 Aug 2025 16:09:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
VOLUME [/usr/local/xwiki]
# Thu, 28 Aug 2025 16:09:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 16:09:51 GMT
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
	-	`sha256:8b204cf7af2ce86d623cb17b6360c675bcaaf8c10989abb0a9fd3943289f819c`  
		Last Modified: Thu, 28 Aug 2025 21:35:22 GMT  
		Size: 188.8 MB (188839175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4c319ab5b0a3f2871a469a972c7057d8ebc5e88e06cf295d9e0f807efc050f`  
		Last Modified: Thu, 28 Aug 2025 21:36:18 GMT  
		Size: 317.3 MB (317325653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79d029870f6a5ff912edbf886523e4677c7604d85f7e37bb2ee2d428adf4e53`  
		Last Modified: Thu, 28 Aug 2025 21:17:46 GMT  
		Size: 2.4 MB (2430454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762e89bf168e404db7920ed1e7a4d69b9be0a84d25ec993e037383c8580d5132`  
		Last Modified: Thu, 28 Aug 2025 21:16:58 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56460911d090065aad9fcf4c86701b69aea61cb8f81a560b9e75f2dce70c3a86`  
		Last Modified: Thu, 28 Aug 2025 21:16:59 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c997161f42f074631135784fe943cdb8759a189eaff6c0591082e5499767028a`  
		Last Modified: Thu, 28 Aug 2025 21:16:59 GMT  
		Size: 6.6 KB (6627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36fe43c0a55965e317907ccc2dad7bac5e691ef43ec8b3511784b5c8a5f18aa`  
		Last Modified: Thu, 28 Aug 2025 21:16:59 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:40a609ea206e0bab2f02a2a9f6b2cf81443a743e3a66c09f097848ed3b777f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9153275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e1ce0fb87567f6b599313c8bb5186757f2354529ee5841695325b4b8c8858`

```dockerfile
```

-	Layers:
	-	`sha256:43b860e23128bf74c2bed874a6a1c804730ccc1c2d5d2e58e2306dc4ce4796e8`  
		Last Modified: Fri, 29 Aug 2025 00:07:31 GMT  
		Size: 9.1 MB (9111531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64460771795b4c5690727e2ba3be2cdef503b5c96f085c29eb1707c576343891`  
		Last Modified: Fri, 29 Aug 2025 00:07:32 GMT  
		Size: 41.7 KB (41744 bytes)  
		MIME: application/vnd.in-toto+json
