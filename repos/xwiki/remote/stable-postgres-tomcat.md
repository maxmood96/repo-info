## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:27f68babe75e124d7931b3c2307955c61fd513356fd5224c72092342ee2a55b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:629afc9f947708e8504cdb0c7db0095ad49197b707e1284cb08a261ed7851758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.6 MB (612565529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e121374b5f324105790f1b9ad1f92c9cf7f022484515ced04d6807c7139b6737`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Oct 2024 15:53:54 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_VERSION=16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a66ce45c49863c0e8cbdae0fb5e5dfab317a1c0c3a45e7c33fb61b09b39fe23
# Mon, 28 Oct 2024 15:53:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 28 Oct 2024 15:53:54 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Oct 2024 15:53:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 15:53:54 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4db91116a643f1af6f310b6dfdd6bb6fa9f5a4e5579bc5cdf2ae45c06a7650`  
		Last Modified: Thu, 24 Oct 2024 00:57:09 GMT  
		Size: 17.0 MB (16965851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b16bdaa6a5730f4ec6136b774473dd0b2b687cce3c95f8bc354146474452c`  
		Last Modified: Thu, 24 Oct 2024 00:57:10 GMT  
		Size: 46.9 MB (46941786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3455e586bc9e48010a24a531cb0e35c3363f3605b0ead2e41dff0ca83ace0`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8021e383cc85d1eb186a772b8cbcb0e8278d701580b9eaa081bfd9064af3e64`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee55d0bb1c8869afe9b9d97e530cbcaff3b222149eda66faf123396737a7d53`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b748649db8eb18ca6f22b4e6f45e2418cf840e7b312ec6cee8b81966160d6b`  
		Last Modified: Thu, 24 Oct 2024 02:54:24 GMT  
		Size: 13.4 MB (13374098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9801e0bd5e0f6c538c825c4a336de90e1eaa721823d4854bd300d486fb217afe`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 223.1 KB (223070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316515a8aabb0534c505b6fee6c10bd562d3bd87a5c5aab11892149741350e61`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 192.3 MB (192263388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac623f5efab4df747367f64b1857c8dd26f3b9c4afd2424f9418d51e09ec69cc`  
		Last Modified: Mon, 28 Oct 2024 18:00:33 GMT  
		Size: 312.0 MB (312017882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c650b9188f598f3ecd5de151bbb49943ca2c79bca1e55d15163e6bfa4ad55d51`  
		Last Modified: Mon, 28 Oct 2024 18:00:28 GMT  
		Size: 1.0 MB (1013643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1797fc659e1a9d64fadc1281bf078ec5603813dd63dc963c34eb089766806a2`  
		Last Modified: Mon, 28 Oct 2024 18:00:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5848b1b19bac7456498b122e4ff0962344619848dc83a1837814976de96b87c`  
		Last Modified: Mon, 28 Oct 2024 18:00:29 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0355c728825afd462ea5b54a3deb4d95028d6c1f6d172777ee21f1464d20b49e`  
		Last Modified: Mon, 28 Oct 2024 18:00:29 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a6ee4d5047c4edabec5ff44f86ad7003891f077b81120a25e906906658f0d1`  
		Last Modified: Mon, 28 Oct 2024 18:00:30 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:63ce2f0d60ecd24530dea1feed4d631fec9749b47a44a150707ab247953c9e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96f2ca840b0419c7d7defc1331979786edb8916ef68ea29d42ae176088a5049`

```dockerfile
```

-	Layers:
	-	`sha256:74ef9a3b03a60c6150f9fb6de07f736dcb5a5755f940696ec00c45b11a8ec4ae`  
		Last Modified: Mon, 28 Oct 2024 18:00:28 GMT  
		Size: 8.8 MB (8788268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f41061a6dcdaa573a98697abb83c12955930837735f66fd38d8615d6bb4e3f9`  
		Last Modified: Mon, 28 Oct 2024 18:00:28 GMT  
		Size: 41.3 KB (41313 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cefd3c1e34e7114d0ea055b55d53b773a75e0e3a8f1e65c085636af4ddddbe0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.8 MB (608809284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e17037d06f73e5edf15fb4a9a5617ec5276b86aeef57d121d7edea1f881e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Oct 2024 15:53:54 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_VERSION=16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a66ce45c49863c0e8cbdae0fb5e5dfab317a1c0c3a45e7c33fb61b09b39fe23
# Mon, 28 Oct 2024 15:53:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 28 Oct 2024 15:53:54 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 28 Oct 2024 15:53:54 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Oct 2024 15:53:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 15:53:54 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e2f7d4d887134d9aff4c6177e18f66336c5f3549bb3d16b0c27622e2b8b22c`  
		Last Modified: Thu, 24 Oct 2024 00:59:40 GMT  
		Size: 17.0 MB (16980397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4547cef613196c0e0f0eddc0c27bfdebd8ba87747901b9fc1fba83828f192b`  
		Last Modified: Thu, 24 Oct 2024 01:13:00 GMT  
		Size: 46.4 MB (46430942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f238f5bd3f6d19b6557a168cdf2216e1c7345f3d9f47f07beb086bf56b80642`  
		Last Modified: Thu, 24 Oct 2024 01:12:58 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc825c390428c52f01639df85bf823ec19660a17b84dff8b0e3a5a25f510ece0`  
		Last Modified: Thu, 24 Oct 2024 01:12:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2163de3883d1b73af731c56b7ccd6ea979d721db6527705908bb06b05bbf6a7`  
		Last Modified: Thu, 24 Oct 2024 12:35:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6f3c5a8eec1b034ff73efefd0a115cdab18cf8e9c1f53bb8c8610151874ed1`  
		Last Modified: Thu, 24 Oct 2024 12:40:57 GMT  
		Size: 13.4 MB (13386564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef23abe225803bcf3217349c97b5019b337a56c684c7a9fb66869d42d45c8b0`  
		Last Modified: Thu, 24 Oct 2024 12:40:57 GMT  
		Size: 223.6 KB (223588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944602abdd9c0e104517f03d57c9fcecf731db0c989d3d90e883a709c7a86634`  
		Last Modified: Thu, 24 Oct 2024 14:36:48 GMT  
		Size: 189.9 MB (189854981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5403e82d0268a09ecebfd40a83d5a1df69f21fecb634a7ee375db4eac7bc5d9`  
		Last Modified: Mon, 28 Oct 2024 18:04:06 GMT  
		Size: 312.0 MB (312017883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae29fd6c4038a6e2231a8572ad210c5385ce1c3df7326e00fa2e48741205f44`  
		Last Modified: Mon, 28 Oct 2024 18:06:57 GMT  
		Size: 1.0 MB (1013638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84569ffebce0e6bcd4fb80ff39df133ec8411fbcb5fe1934b0daedd732519060`  
		Last Modified: Mon, 28 Oct 2024 18:06:57 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42e6c59c65db56cd9652dad15393460a3951d5ab608174525256c798c913292`  
		Last Modified: Mon, 28 Oct 2024 18:06:57 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e178187b0de15302ce4bf65cb5f58caa64cfe8173a380ffbee7cbdd18f48fb`  
		Last Modified: Mon, 28 Oct 2024 18:06:57 GMT  
		Size: 6.6 KB (6592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd588bf39d52700ae641c93db745748531ab320c4b674882925418aba9402ab4`  
		Last Modified: Mon, 28 Oct 2024 18:06:58 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:6d09ae896d7e0ff576602dcbe3aa3a86e7f8a2c39197f7514376cdaa525e0d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3389ce289e2fcad2930a46971ca00c05fa28feb81ba55d5abf0a4599cf07fcaa`

```dockerfile
```

-	Layers:
	-	`sha256:d9cfe2fefdba0f0e7960d5d99bdaae4d782b10bc42cf8d7bf0baef39f8113632`  
		Last Modified: Mon, 28 Oct 2024 18:06:57 GMT  
		Size: 8.8 MB (8789020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581157f87d2dcf4a99408f276a6417586991331d51856f6d74b98bdfbedb947d`  
		Last Modified: Mon, 28 Oct 2024 18:06:57 GMT  
		Size: 41.5 KB (41486 bytes)  
		MIME: application/vnd.in-toto+json
