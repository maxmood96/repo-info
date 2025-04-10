## `xwiki:stable`

```console
$ docker pull xwiki@sha256:b0ec50e6c33f61749ee940571cfc06d6774b386c969ad1d8a49574ead65881d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:2edd65c6477ba31f0aeac545bbb01c12b43d9e670b00979c3a6c47ce131d0d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624536332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b4546ef023455ab1794ac0cc83e65cfb5d5ad1562d436373930d32d19825e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
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
# Mon, 31 Mar 2025 16:08:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 31 Mar 2025 16:08:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 16:08:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 31 Mar 2025 16:08:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 31 Mar 2025 16:08:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 31 Mar 2025 16:08:40 GMT
ENV TOMCAT_MAJOR=10
# Mon, 31 Mar 2025 16:08:40 GMT
ENV TOMCAT_VERSION=10.1.40
# Mon, 31 Mar 2025 16:08:40 GMT
ENV TOMCAT_SHA512=2bde772acf2e6f300f0f8341eb4de7da5d59af6a95f607bcdb92e4c22e0a253d437ea9a423d7d3e334af1c608f33489f32d32d346fbef5b0abef1dee666895ea
# Mon, 31 Mar 2025 16:08:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 31 Mar 2025 16:08:40 GMT
ENTRYPOINT []
# Mon, 31 Mar 2025 16:08:40 GMT
CMD ["catalina.sh" "run"]
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 31 Mar 2025 16:08:40 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_VERSION=17.2.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.2.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=8c35dae775bbc834e5d747c8b0613016beea6168e96034dd11e29ed88fe6e26e
# Mon, 31 Mar 2025 16:08:40 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Mon, 31 Mar 2025 16:08:40 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
VOLUME [/usr/local/xwiki]
# Mon, 31 Mar 2025 16:08:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 16:08:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f077abe239c4b7c52baccfdc40cf1d11599c65c059129059886ba1ce35baf7`  
		Last Modified: Wed, 09 Apr 2025 01:16:40 GMT  
		Size: 17.0 MB (16967596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32015a69421bcce8c43294589f07eede587c47a2a4da89558659befdc27a754`  
		Last Modified: Wed, 09 Apr 2025 01:16:41 GMT  
		Size: 52.9 MB (52876141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b689d8529676c7666da8709db4efbb9cd10fe9e60851b44920556f0057025b23`  
		Last Modified: Wed, 09 Apr 2025 01:16:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b596fb477614cbefc72ad1979a8307c4a41d346ee9db9835a85e6ca807ccb9`  
		Last Modified: Wed, 09 Apr 2025 01:16:39 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d7aa9422b09dba2e0f062dd20ec4a3dc69feafc069a9c37bb903689f117b65`  
		Last Modified: Wed, 09 Apr 2025 03:11:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113211f9a6aac869da5f42af6576d21295758d65a6fcef6d05df1dd40ba3be71`  
		Last Modified: Wed, 09 Apr 2025 03:11:20 GMT  
		Size: 13.8 MB (13829786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68ee9fe8c965f64d6810d8d7c97714c7a3c7d8a200be104b971022ce254e921`  
		Last Modified: Wed, 09 Apr 2025 03:11:19 GMT  
		Size: 224.5 KB (224476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9604adaec429f83c63dc55879ac13f7beea9113ac09883cd4cf596ba1bfdcb`  
		Last Modified: Wed, 09 Apr 2025 04:11:36 GMT  
		Size: 191.2 MB (191162324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b1054a64dcd37d568d2c4f1030b8253cabdda4295eaa39208ad6f829fb860`  
		Last Modified: Wed, 09 Apr 2025 04:11:45 GMT  
		Size: 317.3 MB (317308713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2a3b90ba724213aa35d4d31bf09235f0347bce011d7995655101358f4824c9`  
		Last Modified: Wed, 09 Apr 2025 04:11:30 GMT  
		Size: 2.4 MB (2434169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef4dd1c7d93aac2d84190e566a5cd9f3ae9051020d47efe36d26311aab52cd0`  
		Last Modified: Wed, 09 Apr 2025 04:11:30 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7d93f17e8caa5f6dee45928ffd6022d8eb0120554557b6ed430b66f77bb9b9`  
		Last Modified: Wed, 09 Apr 2025 04:11:31 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e1d0606937a16b39a35f2ba0288925dd88a3c68c3838c8422482e248c91e9a`  
		Last Modified: Wed, 09 Apr 2025 04:11:31 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a3a45a6d4ef999675ac8a95f486aadaf1e835e32decee889f59ee8642ef26`  
		Last Modified: Wed, 09 Apr 2025 04:11:32 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable` - unknown; unknown

```console
$ docker pull xwiki@sha256:b523fe2ef83e47b8cfaacb9516dbf47380833ac16a2936419cdfb9384c81fc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8812917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cefa67fa0b4f2d0e93e9ef52cb59caa076526f59833d0c3c0fdd93be27965be`

```dockerfile
```

-	Layers:
	-	`sha256:8ad2963be480904e9d487c93e5987802fc4b83eee24162ce51f5abe297150cc2`  
		Last Modified: Wed, 09 Apr 2025 04:11:30 GMT  
		Size: 8.8 MB (8770781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d9f56c8c86980d0ad37ecb15daac74fb447d359a763a3983c570a4aece8adba`  
		Last Modified: Wed, 09 Apr 2025 04:11:30 GMT  
		Size: 42.1 KB (42136 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:65a3ca7cc6190da0aa1cd52cdce0e6a31b895a761bba4b7d024d88acef08dd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.5 MB (620544717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dc9fbfab673fe01ae265fe7f1f0dd685d47e2249112d5541cb493626ec02e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Thu, 30 Jan 2025 14:32:57 GMT
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
# Mon, 31 Mar 2025 16:08:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 31 Mar 2025 16:08:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 16:08:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 31 Mar 2025 16:08:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 31 Mar 2025 16:08:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 31 Mar 2025 16:08:40 GMT
ENV TOMCAT_MAJOR=10
# Mon, 31 Mar 2025 16:08:40 GMT
ENV TOMCAT_VERSION=10.1.40
# Mon, 31 Mar 2025 16:08:40 GMT
ENV TOMCAT_SHA512=2bde772acf2e6f300f0f8341eb4de7da5d59af6a95f607bcdb92e4c22e0a253d437ea9a423d7d3e334af1c608f33489f32d32d346fbef5b0abef1dee666895ea
# Mon, 31 Mar 2025 16:08:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 31 Mar 2025 16:08:40 GMT
ENTRYPOINT []
# Mon, 31 Mar 2025 16:08:40 GMT
CMD ["catalina.sh" "run"]
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 31 Mar 2025 16:08:40 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_VERSION=17.2.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.2.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=8c35dae775bbc834e5d747c8b0613016beea6168e96034dd11e29ed88fe6e26e
# Mon, 31 Mar 2025 16:08:40 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Mon, 31 Mar 2025 16:08:40 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
VOLUME [/usr/local/xwiki]
# Mon, 31 Mar 2025 16:08:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 16:08:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787aea36c8936222fd96cbbd68c43aadaafb0e67fe9615a7545f05fd317f522d`  
		Last Modified: Wed, 09 Apr 2025 06:58:50 GMT  
		Size: 17.0 MB (16987241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16692c778676906d73d822ec619e2970ded47b269622846a4c7933b754b87b`  
		Last Modified: Wed, 09 Apr 2025 07:08:54 GMT  
		Size: 52.1 MB (52058673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8f51bd58eed49767ea3bf421cf280e982985b1a5bb7a1eba0db547371b75af`  
		Last Modified: Wed, 09 Apr 2025 07:08:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffc1b509e96871f44ef99b101d7e6f3b14a1a9894545bc33e960517fef95012`  
		Last Modified: Wed, 09 Apr 2025 07:08:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d2b057f1bfe56ba11c3dd3c937c9fbc1dc3d5bb20e58429fede0aef76ea3d5`  
		Last Modified: Wed, 09 Apr 2025 19:58:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0182870468cecabacf784077b3bcd5e1ae569ded8633d974d8abe253235258ad`  
		Last Modified: Wed, 09 Apr 2025 19:58:26 GMT  
		Size: 13.8 MB (13832502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d1ad11d2c5eafc4e836202b600fde88fc7adbff2643f2c9ab40845638f36d`  
		Last Modified: Wed, 09 Apr 2025 19:58:25 GMT  
		Size: 225.0 KB (224974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e8763975c56b2f000f6d42d70c46191c413c068027ff235e896f31d1cdb12a`  
		Last Modified: Wed, 09 Apr 2025 23:50:12 GMT  
		Size: 188.8 MB (188835939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79200482c1cca444b5c7b7ac955106bb63276b75e3379fe207e10b028f8c6c3`  
		Last Modified: Wed, 09 Apr 2025 23:50:15 GMT  
		Size: 317.3 MB (317308788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500ce06131f5de713311404a59871d43d12a89d5985437c2cf99ac9168c572c1`  
		Last Modified: Wed, 09 Apr 2025 23:50:08 GMT  
		Size: 2.4 MB (2434179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbbb2a4f815219682a5a30f119840c58fc8965ad20de9aec00363ff14ed8960`  
		Last Modified: Wed, 09 Apr 2025 23:50:08 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e481254d2f41f5dddef59c3ae550fd4933e0a0821eaa1401c142792f7a57766b`  
		Last Modified: Wed, 09 Apr 2025 23:50:09 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba6d962635fd045065648beea06bb1995c8f052974a310bb00373218df998e`  
		Last Modified: Wed, 09 Apr 2025 23:50:09 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8d11cfcb1dd57699265d457140a4984487e5d64cfa26501a15a4d796c0e370`  
		Last Modified: Wed, 09 Apr 2025 23:50:10 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable` - unknown; unknown

```console
$ docker pull xwiki@sha256:e23d347ba9161f738b4dc9007e2fedafcff00cb2d958d6851da96735497ef6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8813967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9830b78314cfa39577f38966251fb7157cf0f479576b8ce543e987d726a94c`

```dockerfile
```

-	Layers:
	-	`sha256:9dec17125417deab10218496c5f2bd9459e04b1af155953433c0387a35be3513`  
		Last Modified: Wed, 09 Apr 2025 23:50:08 GMT  
		Size: 8.8 MB (8771594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a65a13027ab02481346bf2b6cd8028d9c29e1a5f9e8847a67196b48043663c0`  
		Last Modified: Wed, 09 Apr 2025 23:50:08 GMT  
		Size: 42.4 KB (42373 bytes)  
		MIME: application/vnd.in-toto+json
