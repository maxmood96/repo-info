## `xwiki:16-postgres-tomcat`

```console
$ docker pull xwiki@sha256:d8d0c4c200675085f3f1af5e4ecafd7bacac1b805876ebff18d7c59009fd91f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ecc08aad484d90d9468293a9c6036aa4ecb256f552841a815f7dd4f48817f87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.0 MB (624039198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7175af1423c8c71766bc3be6c11fcfd10552a30b238a2d786fba2dd90d4a126e`
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
ENV TOMCAT_MAJOR=9
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_VERSION=9.0.117
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Tue, 07 Apr 2026 03:31:01 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 03:31:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:31:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 03:31:08 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 03:31:08 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 03:31:08 GMT
CMD ["catalina.sh" "run"]
# Tue, 07 Apr 2026 05:05:32 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 07 Apr 2026 05:05:32 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:05:32 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:05:32 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 07 Apr 2026 05:05:32 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 07 Apr 2026 05:05:32 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 07 Apr 2026 05:05:32 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:05:32 GMT
ENV XWIKI_VERSION=16.10.17
# Tue, 07 Apr 2026 05:05:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.17
# Tue, 07 Apr 2026 05:05:32 GMT
ENV XWIKI_DOWNLOAD_SHA256=4e43dde6d4f971e789b8d38c06404ce14f40c65e2e541303fbb7d2151c113a85
# Tue, 07 Apr 2026 05:05:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 07 Apr 2026 05:05:51 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Tue, 07 Apr 2026 05:05:51 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Tue, 07 Apr 2026 05:05:51 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Tue, 07 Apr 2026 05:05:51 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Tue, 07 Apr 2026 05:05:51 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Tue, 07 Apr 2026 05:05:51 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 07 Apr 2026 05:05:51 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 07 Apr 2026 05:05:51 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 07 Apr 2026 05:05:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 07 Apr 2026 05:05:51 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:05:51 GMT
VOLUME [/usr/local/xwiki]
# Tue, 07 Apr 2026 05:05:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:05:51 GMT
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
	-	`sha256:bc8d2b8625c5ac6f57034eb2e74998dfe0d8dc28d524c781d64b47d64b3319e9`  
		Last Modified: Tue, 07 Apr 2026 03:31:16 GMT  
		Size: 13.8 MB (13788487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d365640aaf5f14db69e0c619b305bf650da8ca6e5ce7cc11c8215ede865912e`  
		Last Modified: Tue, 07 Apr 2026 03:31:16 GMT  
		Size: 224.9 KB (224915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c887294fc0b5a338a0a019dc54f85c7f5584c8b2ed7a863cadc29befe2517b9`  
		Last Modified: Tue, 07 Apr 2026 05:06:28 GMT  
		Size: 191.2 MB (191192777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dde2eae58a761217bd6b2bf82dd88072efdf6e89a25b0c4184750a83350537`  
		Last Modified: Tue, 07 Apr 2026 05:06:29 GMT  
		Size: 318.1 MB (318059882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a620623496f9fd89fddd535fc65b4ba7f17a5e280b82851a092109ba3dc455`  
		Last Modified: Tue, 07 Apr 2026 05:06:21 GMT  
		Size: 1.1 MB (1055029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0787eed2f1edff5e681ef8790883605a6f355c6e4eb16af9286a341068953d`  
		Last Modified: Tue, 07 Apr 2026 05:06:21 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32a05f89a0f38a9d15b5103c768bdfda7a887a86b04512194bf5c41f617d67c`  
		Last Modified: Tue, 07 Apr 2026 05:06:23 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4030eafc0f3ddf8f218d357e64f7a93d5926abdab290e75cad4c278b65b349`  
		Last Modified: Tue, 07 Apr 2026 05:06:23 GMT  
		Size: 6.7 KB (6718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ebe648d0a813d415fa334312fc5b30afcbf94a085612c50d6e6c71bb311a6b`  
		Last Modified: Tue, 07 Apr 2026 05:06:24 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:71e04080b87de98f85521de40d5fc0d7bd90a9f65dace57b05cddc817e897e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30465c5ab3fd45ea08e219b4006b8c67698034bd35925ff31349ea6de597c021`

```dockerfile
```

-	Layers:
	-	`sha256:9f28eae9cde4f1def7a59b0240a9024ef89d78725ecf7ce3de6d53f97315962f`  
		Last Modified: Tue, 07 Apr 2026 05:06:22 GMT  
		Size: 9.1 MB (9110326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96dc269c1b805f5887d622554d84486d5a9e214a73acbadacb87fa5757df9cd`  
		Last Modified: Tue, 07 Apr 2026 05:06:21 GMT  
		Size: 39.8 KB (39796 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f558be73437bce2fd54321a11a7ec19858b6576e50461b40a1601c42268bcc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (620031638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a765191616464e8bc55ea7cbe77d8c04b34bcf922a90a3b8d237e7154a3595cd`
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
# Tue, 07 Apr 2026 05:10:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 05:10:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:10:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 05:10:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 05:10:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 05:10:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 05:10:28 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 Apr 2026 05:10:28 GMT
ENV TOMCAT_VERSION=9.0.117
# Tue, 07 Apr 2026 05:10:28 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Tue, 07 Apr 2026 05:10:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 05:10:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:10:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 05:10:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 05:10:37 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 05:10:37 GMT
CMD ["catalina.sh" "run"]
# Tue, 07 Apr 2026 05:26:46 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 07 Apr 2026 05:26:46 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:26:46 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:26:46 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 07 Apr 2026 05:26:46 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 07 Apr 2026 05:26:46 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 07 Apr 2026 05:26:46 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:26:46 GMT
ENV XWIKI_VERSION=16.10.17
# Tue, 07 Apr 2026 05:26:46 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.17
# Tue, 07 Apr 2026 05:26:46 GMT
ENV XWIKI_DOWNLOAD_SHA256=4e43dde6d4f971e789b8d38c06404ce14f40c65e2e541303fbb7d2151c113a85
# Tue, 07 Apr 2026 05:27:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 07 Apr 2026 05:27:06 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Tue, 07 Apr 2026 05:27:06 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Tue, 07 Apr 2026 05:27:06 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Tue, 07 Apr 2026 05:27:06 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Tue, 07 Apr 2026 05:27:06 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Tue, 07 Apr 2026 05:27:06 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 07 Apr 2026 05:27:06 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 07 Apr 2026 05:27:06 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 07 Apr 2026 05:27:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 07 Apr 2026 05:27:06 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:27:06 GMT
VOLUME [/usr/local/xwiki]
# Tue, 07 Apr 2026 05:27:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:27:06 GMT
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
	-	`sha256:abbd90b469523c8b118e8df02a5c72a17540f34dd73472f02af45b2e5536bf51`  
		Last Modified: Tue, 07 Apr 2026 05:10:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fc30ef0ac8ea4eee97c67ab75fb3e458e803fad4788ee5b90448076470c958`  
		Last Modified: Tue, 07 Apr 2026 05:10:45 GMT  
		Size: 13.8 MB (13797555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c0435d019f49893e24db90dd7de598006d95b4391c9f55d6cfe04f6775800a`  
		Last Modified: Tue, 07 Apr 2026 05:10:45 GMT  
		Size: 225.3 KB (225264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7fbf24edcca4bcb136bd7708ffbf2ac4872937747edc2c9dab2badfcc6f3cb`  
		Last Modified: Tue, 07 Apr 2026 05:27:45 GMT  
		Size: 188.9 MB (188852443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16294db7105fd2f1cf52c7b050336edc58090df13cc510ddc85ad0482a6631a2`  
		Last Modified: Tue, 07 Apr 2026 05:27:48 GMT  
		Size: 318.1 MB (318059817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51d951e49fe9fdeb13684d0bdfe8bfda49d7cb4e29795d0901c187f64741082`  
		Last Modified: Tue, 07 Apr 2026 05:27:39 GMT  
		Size: 1.1 MB (1055028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3869aec20d222cff679c9845ce5f7bfe0cf73f6542664b8cfc114f386b9ce02`  
		Last Modified: Tue, 07 Apr 2026 05:27:39 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5581a5197e38a0bb4b1ec887f37a4f58efb0f712b297aeed3da99f56ad07357c`  
		Last Modified: Tue, 07 Apr 2026 05:27:40 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff62664bf6e06f24b5e7378d482149a047b38f90dab88c637af44d37818a898`  
		Last Modified: Tue, 07 Apr 2026 05:27:40 GMT  
		Size: 6.7 KB (6719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e6f51e8d092402f7a7f192dd23946c62c48e20008659c67e0fc448ca3012dc`  
		Last Modified: Tue, 07 Apr 2026 05:27:41 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:71cd13ceba74308eb59dc6527dd2ccc6e9d2749333e320ebab9d8b6cfdde31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e829f16a78d4d365b0c138ea5e0b8dbd4f1e529ecddd5bd527e94cef3dac86b`

```dockerfile
```

-	Layers:
	-	`sha256:d63ff03968975e4fe4a673c0f2b94e00fcf2ff7cf16afcf7a8247ff60dcaf6ef`  
		Last Modified: Tue, 07 Apr 2026 05:27:39 GMT  
		Size: 9.1 MB (9111043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e66aa238251920d012577465455b54b8795a33a08fdde677552acf74508de9`  
		Last Modified: Tue, 07 Apr 2026 05:27:39 GMT  
		Size: 39.9 KB (39932 bytes)  
		MIME: application/vnd.in-toto+json
