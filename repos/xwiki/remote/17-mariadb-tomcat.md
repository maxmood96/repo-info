## `xwiki:17-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:24a86cc1a74cb32ed467a076967445ddf03b311b9c3e0b7198936b02dde6eeb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:385f2890d0c33a2fafb18bed0d3f4bd78c5c763dcb817b77e0d21b1635de95e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 MB (638074681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd80821073c206b3687fd239a3e78c4963286bf98f66dc598255fe4aae5d3e50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:33 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:38:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:38:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:38:01 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:38:01 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:38:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:38:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:38:01 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:38:01 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:38:01 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:38:01 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:38:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:38:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:38:06 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:38:06 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:38:06 GMT
CMD ["catalina.sh" "run"]
# Wed, 13 May 2026 00:14:47 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 May 2026 00:14:47 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:47 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:47 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 May 2026 00:14:47 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 May 2026 00:14:47 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 May 2026 00:14:47 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 00:14:47 GMT
ENV XWIKI_VERSION=17.10.8
# Wed, 13 May 2026 00:14:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.8
# Wed, 13 May 2026 00:14:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=f5dfab908fddb6319e64897bb2fc41661dd5b5d8aafa455db72c8a794eaa5287
# Wed, 13 May 2026 00:15:10 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 13 May 2026 00:15:10 GMT
ENV MARIADB_JDBC_VERSION=3.5.8
# Wed, 13 May 2026 00:15:10 GMT
ENV MARIADB_JDBC_SHA256=6127dc7858047b3d4482899139640b0e2ab2b8abdeb708cfb8c011117771cddf
# Wed, 13 May 2026 00:15:10 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.8
# Wed, 13 May 2026 00:15:10 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.8.jar
# Wed, 13 May 2026 00:15:10 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.8.jar
# Wed, 13 May 2026 00:15:10 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 13 May 2026 00:15:10 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 13 May 2026 00:15:10 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 13 May 2026 00:15:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 13 May 2026 00:15:11 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 13 May 2026 00:15:11 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 May 2026 00:15:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 00:15:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddba20b57055d40e461149d994ec0cb413acb11933063fb067bef26d04f19e5`  
		Last Modified: Fri, 08 May 2026 00:00:50 GMT  
		Size: 17.0 MB (16984109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86efa879232eb8f00c346e19b20f3574da2aae8c03b7832a9790ff45be526d2d`  
		Last Modified: Fri, 08 May 2026 00:00:51 GMT  
		Size: 53.1 MB (53123205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a6536d8fe0f97af211732b2a2398d9c3fa5f0cceaaaec494787b95b8e710ce`  
		Last Modified: Fri, 08 May 2026 00:00:49 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b19a677a848917cae6512f190c51a8df85b683b2d4e390d33f8d71f637bb734`  
		Last Modified: Fri, 08 May 2026 00:00:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a298a176ea43fc8b3f9a3ff8e5995270b38de11b4bbfa28e14d2bbce0815285`  
		Last Modified: Tue, 12 May 2026 23:38:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a19875ad1cc202378242948ab997dd2d8f720e8de8445955ecdb6551a244410`  
		Last Modified: Tue, 12 May 2026 23:38:14 GMT  
		Size: 14.3 MB (14311217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20fb52c4c87467e26e3b535e06d71dbd3957ae03200794c46ed3c1ea49fe954`  
		Last Modified: Tue, 12 May 2026 23:38:14 GMT  
		Size: 224.7 KB (224738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5970ae6b75fcb4160706ee15dc8d59fe61f80c366821010fcd1e5ba7176fc903`  
		Last Modified: Wed, 13 May 2026 00:15:55 GMT  
		Size: 191.2 MB (191244998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c6a9ed491167bf3f4697e4561095b8c3b144c33ffab118b1bd1e9594a55797`  
		Last Modified: Wed, 13 May 2026 00:15:56 GMT  
		Size: 331.7 MB (331721521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d460e7883684ca3a8e94d68e1dff7468f26ef1fcc7c2d85a949bbdeba8911d`  
		Last Modified: Wed, 13 May 2026 00:15:46 GMT  
		Size: 712.4 KB (712448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025eb6a67961c8c23c3c93fb07d1e60f16514d9500a53a580bf81ca51fc3c513`  
		Last Modified: Wed, 13 May 2026 00:15:46 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906e52345de0ca4e21830aa29c14fb44f0ee4fd5105aebf1b9ecf584f7a40ed4`  
		Last Modified: Wed, 13 May 2026 00:15:48 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2496ad42a1f6538833f4df645b9c63191436d8c01894dbfce68e2ba028e9a2b4`  
		Last Modified: Wed, 13 May 2026 00:15:48 GMT  
		Size: 10.7 KB (10675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffba4e84eae536d4aa17d92182d9485e8d1f3a8560db8bf64d34171afa89909`  
		Last Modified: Wed, 13 May 2026 00:15:49 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:620ea7e255bfe00e7767b28e1e52465acdf1116b7ff5b34083791042fc24ff91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541c82247245f43da91794818220b290e80bcf1cfbad30c2031ad592245556c9`

```dockerfile
```

-	Layers:
	-	`sha256:adb96ce14844ad747ded1f6f91b0455facc508ccb2c154451ea35d5fe0591b00`  
		Last Modified: Wed, 13 May 2026 00:15:47 GMT  
		Size: 9.2 MB (9181824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c105b0bb9459f972f63a982a726823fb03e53b704b815f217cf25ce7d01892d`  
		Last Modified: Wed, 13 May 2026 00:15:46 GMT  
		Size: 40.5 KB (40453 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bb8005260b7e53a6feb0ed663aa4f5abb3bc11a40d3a7a5c9d9e9a687e999ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.1 MB (634097954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bd5a67115c50204ed6db8285b4167eb1b91314ecf5716f2758d4d2f523ef6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:37:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:37:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:37:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:37:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:37:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:37:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:37:33 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:37:33 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:37:33 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:37:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:37:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:37:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:37:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:37:43 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:37:43 GMT
CMD ["catalina.sh" "run"]
# Wed, 13 May 2026 00:14:57 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 May 2026 00:14:57 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:57 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:57 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 May 2026 00:14:57 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 May 2026 00:14:57 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 May 2026 00:14:57 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 00:14:57 GMT
ENV XWIKI_VERSION=17.10.8
# Wed, 13 May 2026 00:14:57 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.8
# Wed, 13 May 2026 00:14:57 GMT
ENV XWIKI_DOWNLOAD_SHA256=f5dfab908fddb6319e64897bb2fc41661dd5b5d8aafa455db72c8a794eaa5287
# Wed, 13 May 2026 00:15:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 13 May 2026 00:15:20 GMT
ENV MARIADB_JDBC_VERSION=3.5.8
# Wed, 13 May 2026 00:15:20 GMT
ENV MARIADB_JDBC_SHA256=6127dc7858047b3d4482899139640b0e2ab2b8abdeb708cfb8c011117771cddf
# Wed, 13 May 2026 00:15:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.8
# Wed, 13 May 2026 00:15:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.8.jar
# Wed, 13 May 2026 00:15:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.8.jar
# Wed, 13 May 2026 00:15:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 13 May 2026 00:15:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 13 May 2026 00:15:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 13 May 2026 00:15:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 13 May 2026 00:15:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 13 May 2026 00:15:21 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 May 2026 00:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 00:15:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38815cba44dccf952747a068e6817ab567111a1c108b6dcd5c0b012d0f109b97`  
		Last Modified: Fri, 08 May 2026 00:00:24 GMT  
		Size: 17.0 MB (16997471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deedef5af075591feecaed06bc515c816989687a293e4bb0831646d46420af2`  
		Last Modified: Fri, 08 May 2026 00:00:25 GMT  
		Size: 52.3 MB (52314893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62335cfc5fbef6fb489815953e6ae3eca5ab0be8a983b3a23657e220be53e087`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0308dfed5f9175f77174db7f0b8419872cd497212c4a39110d8d4c35707627d2`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2294bfa5ed9e69b6ed7e3a2ddb7dda944403b5c5706104d873f9df7da349da5`  
		Last Modified: Tue, 12 May 2026 23:37:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ad49dc75be6c83ae7cb60f8ab63fcda1c6b32a2e54a839a7823f6852531baa`  
		Last Modified: Tue, 12 May 2026 23:37:52 GMT  
		Size: 14.3 MB (14314819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb72bbc785bb1cca21fea474a6e61c9f1b0c098c46032d554c8f8dbf6d03b265`  
		Last Modified: Tue, 12 May 2026 23:37:52 GMT  
		Size: 225.3 KB (225256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd7c83b32cfaf47445384aa353fcdc0a0de77451717b39b97dcd3144911ebb`  
		Last Modified: Wed, 13 May 2026 00:16:02 GMT  
		Size: 188.9 MB (188916192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7264266a8ce982b9a7acba8b739bd1784eb9cca281d79dd74c0f83ca9a0c3e`  
		Last Modified: Wed, 13 May 2026 00:16:05 GMT  
		Size: 331.7 MB (331721623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84321c6272216b0bd2a5ef3ad5179610adeca30e56e108a9b365ee52eb280221`  
		Last Modified: Wed, 13 May 2026 00:15:54 GMT  
		Size: 712.4 KB (712447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec445cec6860fe7517573879d6e85f957ebcf70a8338e3cd17e16779f56b2a3f`  
		Last Modified: Wed, 13 May 2026 00:15:54 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365ffa669bbb6c32cf82e439651149d25530df10f14bbe94d0af11d1e733c2f2`  
		Last Modified: Wed, 13 May 2026 00:15:56 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d2b7555438aaab86f01bb39a2f0e0fea5f1e241311ccccf934cc5b4656dc94`  
		Last Modified: Wed, 13 May 2026 00:15:56 GMT  
		Size: 10.7 KB (10673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fd51f7cd6f0864a987dc09c9edbb51d1f5e209f4408b4fe1a25266fd8ed98f`  
		Last Modified: Wed, 13 May 2026 00:15:57 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:c167e89e674ce47240f55b202612a2139d37923fede6902d897eca846aa1968b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe9c75f0f5c885cc3ce5501db68fa456b0772755beb8dacf15845866e5ac7ad`

```dockerfile
```

-	Layers:
	-	`sha256:eb8399a600ba22fdf6f045c7189c9db2acd8e7d05faa0a00d090b2aad3e53a64`  
		Last Modified: Wed, 13 May 2026 00:15:55 GMT  
		Size: 9.2 MB (9182565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56a560392cdad93e0e40d19e5d88ab7709e694b8956ffae73c7150c31db05e61`  
		Last Modified: Wed, 13 May 2026 00:15:54 GMT  
		Size: 40.6 KB (40615 bytes)  
		MIME: application/vnd.in-toto+json
