## `xwiki:latest`

```console
$ docker pull xwiki@sha256:a3e129db2e5b54a2350851f8bc21b8e3f794682c2671778e4d4c57057c35418e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:27451a27adede79e283df4629599552b9cb809e7f4da397cd4c18d63859163f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.6 MB (655553430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa17f567a96ee25898384e0f3fc96d9f53ea38697561556edfff8911dffe783`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:14:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 02:13:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jun 2026 02:13:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 02:13:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 25 Jun 2026 02:13:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:13:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_MAJOR=10
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_VERSION=10.1.56
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_SHA512=8fae99273615eb9d7fbe7ed80abda0ca27647a80f6fcfda98459c5b412d5ef555740b4c4d4af5afae2eb150f1f5bede21ab007ab8cc1f407f508d8908a81b7cc
# Thu, 25 Jun 2026 02:13:22 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 25 Jun 2026 02:13:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 02:13:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 25 Jun 2026 02:13:26 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 25 Jun 2026 02:13:26 GMT
ENTRYPOINT []
# Thu, 25 Jun 2026 02:13:26 GMT
CMD ["catalina.sh" "run"]
# Thu, 25 Jun 2026 04:11:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 25 Jun 2026 04:11:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:11:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:11:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 25 Jun 2026 04:11:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 25 Jun 2026 04:11:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 25 Jun 2026 04:11:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 04:11:19 GMT
ENV XWIKI_VERSION=18.4.1
# Thu, 25 Jun 2026 04:11:19 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.4.1
# Thu, 25 Jun 2026 04:11:19 GMT
ENV XWIKI_DOWNLOAD_SHA256=568d3aa4708a5c75d141a978491d800a90d8485afd06e1eb203d003a5a6f8ede
# Thu, 25 Jun 2026 04:11:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 25 Jun 2026 04:11:41 GMT
ENV MYSQL_JDBC_VERSION=9.7.0
# Thu, 25 Jun 2026 04:11:41 GMT
ENV MYSQL_JDBC_SHA256=0353648eaa1c91e0f4020c959abf756bc866ffd583df22ae6b6f6e0cbd43eb44
# Thu, 25 Jun 2026 04:11:41 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.7.0
# Thu, 25 Jun 2026 04:11:41 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.7.0.jar
# Thu, 25 Jun 2026 04:11:41 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.7.0.jar
# Thu, 25 Jun 2026 04:11:41 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 25 Jun 2026 04:11:41 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 25 Jun 2026 04:11:41 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 25 Jun 2026 04:11:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 25 Jun 2026 04:11:41 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 04:11:41 GMT
VOLUME [/usr/local/xwiki]
# Thu, 25 Jun 2026 04:11:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 04:11:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9e436cd644d0619bdfd1c8d1dce9e824e836e6102bf4a4c26919785ffe2a7c`  
		Last Modified: Tue, 02 Jun 2026 08:14:35 GMT  
		Size: 17.0 MB (16984112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87482ed64d79af651c4c12177abc09ecb3e56b9d8d0f50a562d2f590d06f86d4`  
		Last Modified: Tue, 02 Jun 2026 08:15:02 GMT  
		Size: 53.1 MB (53123212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc789882cf0d5dbeb8bc4705a9265f34e7a07d131d29a28ab214e03c5848204d`  
		Last Modified: Tue, 02 Jun 2026 08:15:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61623c08676d47596865bd7b800628bf28592b0b9ffaedb68600f7ce6243b27`  
		Last Modified: Tue, 02 Jun 2026 08:15:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0511e9999bcd27a02849550499c434bf5a04b85d448b6edea21a693ec20faffc`  
		Last Modified: Thu, 25 Jun 2026 02:13:35 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aff57e488da9dbb54d8c18a5b7a7c3afd121063fb34d981a71843516dfee90`  
		Last Modified: Thu, 25 Jun 2026 02:13:35 GMT  
		Size: 14.3 MB (14349294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50ded7df386c999094d43699b85d64540a1b6a56d8dfefc2192ae52a7b99192`  
		Last Modified: Thu, 25 Jun 2026 02:13:35 GMT  
		Size: 3.0 MB (3030334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688ece32bc1c42576c33b68c32f6e3107aa27bccc54484a0b4ce1ed817056119`  
		Last Modified: Thu, 25 Jun 2026 04:12:25 GMT  
		Size: 191.2 MB (191223134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00295102b189e7edc62e9fd83122a30a1bd32c23aa1d41a75403f5fbba1a58d`  
		Last Modified: Thu, 25 Jun 2026 04:12:27 GMT  
		Size: 344.6 MB (344644635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57732bd7bff4b9f7438cd3e3bc55d50bca17fc97b5a52c2a1dce5ab25993ffe2`  
		Last Modified: Thu, 25 Jun 2026 04:12:18 GMT  
		Size: 2.4 MB (2446028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d6c3b67948bbbe07b794fec3ec7d3c558217debc3dbeca952932ca9ae2d392`  
		Last Modified: Thu, 25 Jun 2026 04:12:18 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36adfa81782b497307171a23859c13160544fd52eb68c2788969866b680688e7`  
		Last Modified: Thu, 25 Jun 2026 04:12:19 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d1e615586bfcfbfa529ebc1e70bcc070ff7177e8a40e15140438a0e496f8f`  
		Last Modified: Thu, 25 Jun 2026 04:12:20 GMT  
		Size: 11.0 KB (10986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc7fe5e34d66dd0377906995d24e98039cd75b4c4fdc0a2139089d0b5040476`  
		Last Modified: Thu, 25 Jun 2026 04:12:21 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:eb16e83f074081913c678fb5aa5ed9d6cc34f536c9d9b26a05ba3587c0d0b0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9242561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de6e7243e94a09762bf78c98eeb545dc4946c03880a94e681c59459c0dba548`

```dockerfile
```

-	Layers:
	-	`sha256:7a17da80157d00a353d365995f068964d360fd8dd4318fc01eaff8ae8b78e410`  
		Last Modified: Thu, 25 Jun 2026 04:12:19 GMT  
		Size: 9.2 MB (9200446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e691b4ceaed9044ed926e81390e65f91e5c54ed36726a3f6af3d5bd60735c9`  
		Last Modified: Thu, 25 Jun 2026 04:12:18 GMT  
		Size: 42.1 KB (42115 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:latest` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:98ad5c3a0fdb53da15018f415c7c4eb9d333bad4b3c83a1b16fa064a8990bb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.4 MB (651357887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124225f5c526fe9e0156fb490130e58f5a35c7c9024ab9d007c3b6bb09c299c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:15 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:16:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 02:12:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jun 2026 02:12:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 02:12:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 25 Jun 2026 02:12:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:12:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_MAJOR=10
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_VERSION=10.1.56
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_SHA512=8fae99273615eb9d7fbe7ed80abda0ca27647a80f6fcfda98459c5b412d5ef555740b4c4d4af5afae2eb150f1f5bede21ab007ab8cc1f407f508d8908a81b7cc
# Thu, 25 Jun 2026 02:12:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 25 Jun 2026 02:12:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 02:12:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 25 Jun 2026 02:12:54 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 25 Jun 2026 02:12:54 GMT
ENTRYPOINT []
# Thu, 25 Jun 2026 02:12:54 GMT
CMD ["catalina.sh" "run"]
# Thu, 25 Jun 2026 04:11:01 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 25 Jun 2026 04:11:01 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:11:01 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:11:01 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 25 Jun 2026 04:11:01 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 25 Jun 2026 04:11:01 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 25 Jun 2026 04:11:01 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 04:11:01 GMT
ENV XWIKI_VERSION=18.4.1
# Thu, 25 Jun 2026 04:11:01 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.4.1
# Thu, 25 Jun 2026 04:11:01 GMT
ENV XWIKI_DOWNLOAD_SHA256=568d3aa4708a5c75d141a978491d800a90d8485afd06e1eb203d003a5a6f8ede
# Thu, 25 Jun 2026 04:11:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 25 Jun 2026 04:11:24 GMT
ENV MYSQL_JDBC_VERSION=9.7.0
# Thu, 25 Jun 2026 04:11:24 GMT
ENV MYSQL_JDBC_SHA256=0353648eaa1c91e0f4020c959abf756bc866ffd583df22ae6b6f6e0cbd43eb44
# Thu, 25 Jun 2026 04:11:24 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.7.0
# Thu, 25 Jun 2026 04:11:24 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.7.0.jar
# Thu, 25 Jun 2026 04:11:24 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.7.0.jar
# Thu, 25 Jun 2026 04:11:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 25 Jun 2026 04:11:24 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 25 Jun 2026 04:11:24 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 25 Jun 2026 04:11:24 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 25 Jun 2026 04:11:24 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 04:11:24 GMT
VOLUME [/usr/local/xwiki]
# Thu, 25 Jun 2026 04:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 04:11:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c56d3b03f3eed5e9e98720fc008e29f5ad7edffbb3d0095a9751486b593905e`  
		Last Modified: Tue, 02 Jun 2026 08:16:32 GMT  
		Size: 17.0 MB (16997505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87a7c029e17f2ca0e18faf162ffda9b94bff8a6c53017932eea8e9d7c8d257`  
		Last Modified: Tue, 02 Jun 2026 08:16:33 GMT  
		Size: 52.3 MB (52314907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a42fa743e77cd7a6e3837c86c2a0c4d959a29959bad6ce7730b2a3c45b1c838`  
		Last Modified: Tue, 02 Jun 2026 08:16:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229c6fba250cd9ec9dea9d2580e679f6a3e697d45386c7d8e63d493bf8134fa`  
		Last Modified: Tue, 02 Jun 2026 08:16:31 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384e21c77bf8435eca6b03f134c29c283a4cc58758713f928a217ee1029073e0`  
		Last Modified: Thu, 25 Jun 2026 02:13:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17306b9dbf994913c9c2774b349038212546a1558f34aaf094bc26b9f2b59037`  
		Last Modified: Thu, 25 Jun 2026 02:13:03 GMT  
		Size: 14.4 MB (14352031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461465510cdd039be85c0c637eae3a3d19183c82d849f758283f1b15090458cc`  
		Last Modified: Thu, 25 Jun 2026 02:13:02 GMT  
		Size: 2.8 MB (2829997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2cd6a977ac94e443b40452439d6fb483a82e3bba0f51f48144b66a4ebc1e9`  
		Last Modified: Thu, 25 Jun 2026 04:12:05 GMT  
		Size: 188.9 MB (188876464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967ea4a18c7abb488875666c1597498321b7f93e0782baa30ff47fc44e02503`  
		Last Modified: Thu, 25 Jun 2026 04:12:07 GMT  
		Size: 344.6 MB (344644680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fabcef73816f66f246b5274337da88410a5b89a8c753338f4dc6cb05c9f9f07`  
		Last Modified: Thu, 25 Jun 2026 04:11:58 GMT  
		Size: 2.4 MB (2446032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14564ed0ac823b8504442ca718d8db07df6718c201134cd2868d23be5a412dd`  
		Last Modified: Thu, 25 Jun 2026 04:11:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd772ea1642f14fd25e5951a076f08f6ce91f38ee7ad1a5da4599094aa8f7e4a`  
		Last Modified: Thu, 25 Jun 2026 04:11:59 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3453b687f253cdfab29cc06cd1d812e502d475ad480bf7a528500de0dd13cc`  
		Last Modified: Thu, 25 Jun 2026 04:11:59 GMT  
		Size: 11.0 KB (10983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced536db9dddcf91636d88eeff1207b173e214387e19bc8ef139b706c7ffcc9b`  
		Last Modified: Thu, 25 Jun 2026 04:12:01 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:7bee11ab8e1d9f85d841a6c7f0d0e8d93add480cd2888b4fa1068329703ec808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9243607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4bf1129a3a2430d6a1b48e97f15ab538877a478bb086347c70ff786c334c00`

```dockerfile
```

-	Layers:
	-	`sha256:b673a0e4f195894455c2e1690b6b40cf7b11aa1f6351de24e6407c27fad1f060`  
		Last Modified: Thu, 25 Jun 2026 04:11:58 GMT  
		Size: 9.2 MB (9201259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21e11be745e5a866dcc0ff62d39cc8659b1a83458b5981ef9925711e8e41f745`  
		Last Modified: Thu, 25 Jun 2026 04:11:58 GMT  
		Size: 42.3 KB (42348 bytes)  
		MIME: application/vnd.in-toto+json
