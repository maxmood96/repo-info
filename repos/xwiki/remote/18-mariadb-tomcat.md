## `xwiki:18-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:96e3938a5f16aabf5585e12591c3e482bb7b814cd66cc776d9ad74fe0c6d1d74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:18-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4569e89896b9f8109889ad06427a5c22cbb5b971527fdbe17cbd617b2ee25e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.8 MB (645806195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edccfefce0b742d906d44ab31385edb699771e95e2fc57d10f298ccfabee0669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:22:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:22:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:22:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:22:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:22:45 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 01:23:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:23:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:10:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:10:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:10:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:10:41 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:10:41 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:10:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:10:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:10:50 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:10:50 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:10:50 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Apr 2026 19:11:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Apr 2026 19:11:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Apr 2026 19:11:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Apr 2026 19:11:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Apr 2026 19:11:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Apr 2026 19:11:24 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Apr 2026 19:11:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 19:11:24 GMT
ENV XWIKI_VERSION=18.2.0
# Fri, 03 Apr 2026 19:11:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.0
# Fri, 03 Apr 2026 19:11:24 GMT
ENV XWIKI_DOWNLOAD_SHA256=1dbbf05fcb593f738a3f922c0d12bd4524c789a9f404e0e035bd6b2da2d1d26f
# Fri, 03 Apr 2026 19:11:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 03 Apr 2026 19:11:45 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Fri, 03 Apr 2026 19:11:45 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Fri, 03 Apr 2026 19:11:45 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Fri, 03 Apr 2026 19:11:45 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Fri, 03 Apr 2026 19:11:45 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Fri, 03 Apr 2026 19:11:45 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 03 Apr 2026 19:11:45 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 03 Apr 2026 19:11:45 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 03 Apr 2026 19:11:46 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 03 Apr 2026 19:11:46 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 19:11:46 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Apr 2026 19:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 19:11:46 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6502333748a9e5b5a7e8aaabb484e42b3cc861ca1dcf4d70331259c318eb596d`  
		Last Modified: Tue, 17 Mar 2026 01:23:01 GMT  
		Size: 17.0 MB (16983392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b331859550d0b667a6ab32159d398031b1c5ed2e351a645be1e3dcd633f6ab`  
		Last Modified: Tue, 17 Mar 2026 01:23:21 GMT  
		Size: 53.0 MB (52985455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded334408097f08dde9507428976abc2f844eae59856aecc45671fb699f88f74`  
		Last Modified: Tue, 17 Mar 2026 01:23:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6ab2a4ddd47ce46630077d0e137301e2294ad28cbbd10ed888d2782bc027be`  
		Last Modified: Tue, 17 Mar 2026 01:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131d49d157d95cbd54bf28befca298a2b188d01cd7353f56b361a011ef2a959b`  
		Last Modified: Fri, 03 Apr 2026 18:11:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e9af362e01e7131442569686c288308fb221bc78f5a6658847ed4b744ee4c`  
		Last Modified: Fri, 03 Apr 2026 18:11:00 GMT  
		Size: 14.3 MB (14301288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c083d14ca258a3f5b4d89ecab64719562974385bd7d8a810e5248d77e09cc3`  
		Last Modified: Fri, 03 Apr 2026 18:11:00 GMT  
		Size: 1.6 MB (1639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b109856f2e6e34a2482ae359db9eeb828c151f5c9d68d43fcdcf02403da4ff`  
		Last Modified: Fri, 03 Apr 2026 19:12:27 GMT  
		Size: 191.2 MB (191193213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0e5eb9063f866b73de06b65476da8015009d0ac49c9f17a66c14f2c3cf3fa3`  
		Last Modified: Fri, 03 Apr 2026 19:12:30 GMT  
		Size: 338.2 MB (338242792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfd0ed7e1936d5b49b5b66e3a4d34cbf079ee3683297a84de978ff3584be5e2`  
		Last Modified: Fri, 03 Apr 2026 19:12:19 GMT  
		Size: 708.5 KB (708549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73135e80c28b83eb69a5dea5fa2ddff6211334d58545a85aa015b981e04aa0e3`  
		Last Modified: Fri, 03 Apr 2026 19:12:19 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54922ce1a9a50a3ed876c91d856aa3cd957182639e45e8442ddef2afb7e5b5e`  
		Last Modified: Fri, 03 Apr 2026 19:12:21 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac90ab284faac0e409b9f18373f8731d46e75c15688d2c91ff6adb390129f88a`  
		Last Modified: Fri, 03 Apr 2026 19:12:21 GMT  
		Size: 11.0 KB (10956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d72e9251803d9fb1ed5a3166503afd3e5c9354bc60151dde51935fe8eed96c2`  
		Last Modified: Fri, 03 Apr 2026 19:12:22 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:16dac87242c1d7a83d698f99c45bd133d0a2b95e9e7fa19b413a0d71f0f45476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9233527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bce3d759df8deb77e230b36a17340388a430983f27575c2872aef6b7763decf`

```dockerfile
```

-	Layers:
	-	`sha256:0b712cd6ec4e282ef054fb947f5eda0c970cb616fc412d86f922e68daaede0ed`  
		Last Modified: Fri, 03 Apr 2026 19:12:20 GMT  
		Size: 9.2 MB (9192755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58fb3310450fab3df73e82bbafd2366da740cfb7c03a1dc24bea3b6c03a1de51`  
		Last Modified: Fri, 03 Apr 2026 19:12:19 GMT  
		Size: 40.8 KB (40772 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:18-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:6c23f213709a8f8c48501c9cb616efe5dab22a85379eba7d1bcb246e491cdec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.9 MB (641868323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e86f78178dffbc533972d42b6e66e6b56754beede1b83595dcdd9c5e4f74d9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:54 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 01:24:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:10:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:10:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:10:38 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:10:38 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:10:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:38 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:10:38 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:10:38 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:10:38 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:10:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:10:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:10:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:10:49 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:10:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Apr 2026 19:11:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Apr 2026 19:11:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Apr 2026 19:11:23 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Apr 2026 19:11:23 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Apr 2026 19:11:23 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Apr 2026 19:11:23 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Apr 2026 19:11:23 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 19:11:23 GMT
ENV XWIKI_VERSION=18.2.0
# Fri, 03 Apr 2026 19:11:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.0
# Fri, 03 Apr 2026 19:11:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=1dbbf05fcb593f738a3f922c0d12bd4524c789a9f404e0e035bd6b2da2d1d26f
# Fri, 03 Apr 2026 19:11:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 03 Apr 2026 19:11:48 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Fri, 03 Apr 2026 19:11:48 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Fri, 03 Apr 2026 19:11:48 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Fri, 03 Apr 2026 19:11:48 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Fri, 03 Apr 2026 19:11:48 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Fri, 03 Apr 2026 19:11:48 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 03 Apr 2026 19:11:48 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 03 Apr 2026 19:11:48 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 03 Apr 2026 19:11:48 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 03 Apr 2026 19:11:48 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 19:11:48 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Apr 2026 19:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 19:11:48 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135b685185570494910edd394b8134172c97bab64cfef4134685bc7a7adf965`  
		Last Modified: Tue, 17 Mar 2026 01:24:08 GMT  
		Size: 17.0 MB (16996055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa618972369eec5997c7c2a43c076f8237d95b3c56ab24e45bbe1196cd969d4f`  
		Last Modified: Tue, 17 Mar 2026 01:24:57 GMT  
		Size: 52.2 MB (52155671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d719861772c215e9e1cdc82ae81b5a5009e75c9adb2502f42cb33948ac1f0168`  
		Last Modified: Tue, 17 Mar 2026 01:24:52 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79f03dbf43ae3059af78550ba432373910eb86b58ffaf54e088f81646486ec`  
		Last Modified: Tue, 17 Mar 2026 01:24:53 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdbb005420d0488ac01418ae996fab349cb6d2d14740e23099bc1c826800a4e`  
		Last Modified: Fri, 03 Apr 2026 18:10:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6981e2ba09a603636306253c42625aaeac324110d92404bab431ff6127f3da5f`  
		Last Modified: Fri, 03 Apr 2026 18:10:58 GMT  
		Size: 14.3 MB (14303386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947eeb35156714dc336354678cfcdd43f54b3cfed9a911a49d09aedfa7fc5335`  
		Last Modified: Fri, 03 Apr 2026 18:10:58 GMT  
		Size: 1.7 MB (1719582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5ddec73e0e860cdef35805f19a03021bbec9a6d5bd03a4668d06f177ff5085`  
		Last Modified: Fri, 03 Apr 2026 19:12:35 GMT  
		Size: 188.9 MB (188852835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aa6d39a418fab34e01b6f78fb645670f5620043852ff0c97f5720b3c9411f7`  
		Last Modified: Fri, 03 Apr 2026 19:12:40 GMT  
		Size: 338.2 MB (338242793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb11024d91c1ae51a792a9f1139220bb9dc910a8785c6f331eaa255b30199da`  
		Last Modified: Fri, 03 Apr 2026 19:12:21 GMT  
		Size: 708.5 KB (708549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9320c91326213bb60bfddf7b8333be310718e15085841caf7b8a109d88321896`  
		Last Modified: Fri, 03 Apr 2026 19:12:21 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc091e9d573ad07be4fcb0e80f674c966cb7279fb6cc3343a88927629c4741`  
		Last Modified: Fri, 03 Apr 2026 19:12:23 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff6e0eae007e2b68f26456d8c7571532d6c3aa52a578f026b56178ebed04d6e`  
		Last Modified: Fri, 03 Apr 2026 19:12:23 GMT  
		Size: 11.0 KB (10953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcec050d96fc43c6d5f195b0736b9363a425c73a9848c091e31d4776b50b03f`  
		Last Modified: Fri, 03 Apr 2026 19:12:25 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:aa28a923710204806cd4a6d9d83fcd0bb402526c28ff2caf01d2a1607af75bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e3883393243a80632ef18641b1cf7ddca9a605497e4c33bbed7c6c733a1246`

```dockerfile
```

-	Layers:
	-	`sha256:017b125bf7cc1955f407bd98e267dfa12961d0285b93e02af65ce98b3cbc1c69`  
		Last Modified: Fri, 03 Apr 2026 19:12:22 GMT  
		Size: 9.2 MB (9193508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9e320c6ef36db3989b9139143a18ea440a605a8c7545232a93b99585768455e`  
		Last Modified: Fri, 03 Apr 2026 19:12:21 GMT  
		Size: 40.9 KB (40945 bytes)  
		MIME: application/vnd.in-toto+json
