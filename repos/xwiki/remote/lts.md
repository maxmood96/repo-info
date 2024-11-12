## `xwiki:lts`

```console
$ docker pull xwiki@sha256:72f97f1e0015a74e14c573bf3888a80a432b9e3468c1773c83a391a65db24cd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:0b73ccde2955abf4dd0ec0a8e52e11b4dee8fad69e2e84717bd50b4abc3ddb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.0 MB (608974269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328d24e76c541df862a8d3dc8fc538c2a4d92b7d6d92bee028fde4a0eae01510`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Mon, 21 Oct 2024 15:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 21 Oct 2024 15:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2024 15:59:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 21 Oct 2024 15:59:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 21 Oct 2024 15:59:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2024 15:59:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 21 Oct 2024 15:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 21 Oct 2024 15:59:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_MAJOR=9
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_VERSION=9.0.97
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_SHA512=537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9
# Mon, 21 Oct 2024 15:59:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT []
# Mon, 21 Oct 2024 15:59:18 GMT
CMD ["catalina.sh" "run"]
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 21 Oct 2024 15:59:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_VERSION=15.10.13
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.13
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=bb84c62fbe5d6e1ab4b4f3fae25665f98d0e36186f626222a578c608c9401f70
# Mon, 21 Oct 2024 15:59:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_VERSION=8.4.0
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_SHA256=d77962877d010777cff997015da90ee689f0f4bb76848340e1488f2b83332af5
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.4.0
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.4.0.jar
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.4.0.jar
# Mon, 21 Oct 2024 15:59:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
VOLUME [/usr/local/xwiki]
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Oct 2024 15:59:18 GMT
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
	-	`sha256:c3432b713e60c07405dd99c350f49dbec2153937fa02b34cdfd31acb7f9db5b4`  
		Last Modified: Mon, 11 Nov 2024 20:49:14 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae45b2ffab2f2bf7f1d3cd898642855b88c5f4e6378f8f5066c7dc30175bf47`  
		Last Modified: Mon, 11 Nov 2024 20:49:15 GMT  
		Size: 13.4 MB (13407598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593646ad6b26739771ad7986741e4550b155513b1e21a40c35026906d8ca9d9e`  
		Last Modified: Mon, 11 Nov 2024 20:49:15 GMT  
		Size: 223.0 KB (223045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30be480297d00a72af31e63671673ef66e5e3ab73b361afc40ba93e7ea63b8`  
		Last Modified: Mon, 11 Nov 2024 21:51:08 GMT  
		Size: 192.3 MB (192263510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4118e86d74a24f0e064e8c08d96342f27b116872dea7c7263238e0a17ecb54fd`  
		Last Modified: Mon, 11 Nov 2024 21:51:09 GMT  
		Size: 307.0 MB (307013205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41d550d7400b9855c17f5663d5a5b8a3a9338003ca2a8586479a5c77d833d8`  
		Last Modified: Mon, 11 Nov 2024 21:51:06 GMT  
		Size: 2.4 MB (2393579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e896e64e34524f11f6d1623b7f36c5a22a7abd8e5a2023f362ffd7836a48a1`  
		Last Modified: Mon, 11 Nov 2024 21:51:06 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45633e2a34f6ace663a0372884516d6acf1885eea23e4be0e7618f8eb66c7738`  
		Last Modified: Mon, 11 Nov 2024 21:51:06 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975195741cd07dd2936c8e2e204f00e88a18b64f0e1afbdc577091b5295009a`  
		Last Modified: Mon, 11 Nov 2024 21:51:06 GMT  
		Size: 6.5 KB (6466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b72ac63b32255e777b54d0981fcfaa12189d91ad7040aa1715ec2830fda501`  
		Last Modified: Mon, 11 Nov 2024 21:51:07 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:22f1ff0b4edc28f6aaffaa10f013bfa95ccb94cc31dde0b0344ee4285e31d003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8826765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d3f646cc029bb8bdddff9df785586499be617ddd9ae90b42a509093a38d008`

```dockerfile
```

-	Layers:
	-	`sha256:85753c829778088f244bb9a7a951644312c7f299d7d3e1d9934576be64de56b6`  
		Last Modified: Mon, 11 Nov 2024 21:51:06 GMT  
		Size: 8.8 MB (8784688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e7e2de7054c50db502a530942873d44581dc12212eea4c72f34a4e5a6d2f10`  
		Last Modified: Mon, 11 Nov 2024 21:51:05 GMT  
		Size: 42.1 KB (42077 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0948f5e24d2502fe49597e25289e7cb7a408b9f5089079aa043dc70233c50461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.2 MB (605216303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f686350fd8a16d7c65036fd4f356c7674ccddf149f82d6c1023a679d3d54d8cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Mon, 21 Oct 2024 15:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 21 Oct 2024 15:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2024 15:59:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 21 Oct 2024 15:59:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 21 Oct 2024 15:59:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2024 15:59:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 21 Oct 2024 15:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 21 Oct 2024 15:59:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_MAJOR=9
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_VERSION=9.0.97
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_SHA512=537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9
# Mon, 21 Oct 2024 15:59:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT []
# Mon, 21 Oct 2024 15:59:18 GMT
CMD ["catalina.sh" "run"]
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 21 Oct 2024 15:59:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_VERSION=15.10.13
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.13
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=bb84c62fbe5d6e1ab4b4f3fae25665f98d0e36186f626222a578c608c9401f70
# Mon, 21 Oct 2024 15:59:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_VERSION=8.4.0
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_SHA256=d77962877d010777cff997015da90ee689f0f4bb76848340e1488f2b83332af5
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.4.0
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.4.0.jar
# Mon, 21 Oct 2024 15:59:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.4.0.jar
# Mon, 21 Oct 2024 15:59:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
VOLUME [/usr/local/xwiki]
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Oct 2024 15:59:18 GMT
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
	-	`sha256:42643b42f9d46a521c93ae6aa98bfcf7df2af6a425a5cb714f605b13cd53ba3d`  
		Last Modified: Mon, 11 Nov 2024 20:51:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71c39ae33b2d1f4582470747b07dd46b1fc92eca04e57256e622d58219b2919`  
		Last Modified: Mon, 11 Nov 2024 20:56:07 GMT  
		Size: 13.4 MB (13418519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f16806359a1ac39a8ee91d0bf466fb185529dc367a485db3a4c4c0afee537d`  
		Last Modified: Mon, 11 Nov 2024 20:56:07 GMT  
		Size: 223.5 KB (223540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15b8efe9d0a3ce934f42eb98692be8aed7f6255e768788e96bf09cad4336f85`  
		Last Modified: Mon, 11 Nov 2024 21:53:16 GMT  
		Size: 189.9 MB (189854825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed77d0a89aa0eb0e1bc8d1d64c96593751b0901da45e4d66e6e2cfcbc5502b15`  
		Last Modified: Mon, 11 Nov 2024 22:02:31 GMT  
		Size: 307.0 MB (307013335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c1a88780110fa63bced805851b1d848d5cd0358347983e7a452d294cdf2b9f`  
		Last Modified: Mon, 11 Nov 2024 22:02:20 GMT  
		Size: 2.4 MB (2393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495ec0dcdea1f63f27004082cee144ed910c59310e4ebd163c01c47196b661c9`  
		Last Modified: Mon, 11 Nov 2024 22:02:19 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8059dffb761dd47e715d01663ceab9e13d92d9f61d4c002f0dee3cdae36e73da`  
		Last Modified: Mon, 11 Nov 2024 22:02:19 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cc67b36695f9e0b4fdf9562224b1c18a344f7278f7f2eabb84a67428ce2a3a`  
		Last Modified: Mon, 11 Nov 2024 22:02:20 GMT  
		Size: 6.5 KB (6464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0130f1f4788fa95439afab8b34368d667aa092ada3eae4a1d3867068ff6114e3`  
		Last Modified: Mon, 11 Nov 2024 22:02:20 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:989732c38383dd10754fdc9ce77e0fa317ae6d45ed626dbac96b80d15a23da65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cff0235e7ed94349f313cbae708a75eb0c8b2f983606e63865e6c3059445fa`

```dockerfile
```

-	Layers:
	-	`sha256:58d8b5c6edb9780b810806f3b4e625123dd3b3afd6ea684977bbf59edf901344`  
		Last Modified: Mon, 11 Nov 2024 22:02:20 GMT  
		Size: 8.8 MB (8785476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09a0055fcb4be29901c6bf46dcc4f02973c6500a68e83b87a76dfc54744f9dea`  
		Last Modified: Mon, 11 Nov 2024 22:02:19 GMT  
		Size: 42.3 KB (42286 bytes)  
		MIME: application/vnd.in-toto+json
