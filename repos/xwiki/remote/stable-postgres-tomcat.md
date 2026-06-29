## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:14ee9eeabab5fe13083aef91e751473e2b4c7c43960df3667f72fdc0f917e8a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0736fabd6991fabb7e0ce57f62a8753e5ed4738c685633dd6320b7e491a22a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.4 MB (654445889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c267f6361e259bbfe96e87498c80fb38cf5660b88534f6d363d65b8889c9a6`
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
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jun 2026 19:12:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
ENV XWIKI_VERSION=18.5.0
# Mon, 29 Jun 2026 19:12:19 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.5.0
# Mon, 29 Jun 2026 19:12:19 GMT
ENV XWIKI_DOWNLOAD_SHA256=649a5c53bc7ca02d80b3a3dcd1c03a7534ff868b6fe4f6eafa198602bc31c6df
# Mon, 29 Jun 2026 19:12:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jun 2026 19:12:41 GMT
ENV POSTGRES_JDBC_VERSION=42.7.11
# Mon, 29 Jun 2026 19:12:41 GMT
ENV POSTGRES_JDBC_SHA256=1981b31d3993c58702783c1cddf10a34e48c1f413d70ff1cb6def0a143484647
# Mon, 29 Jun 2026 19:12:41 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.11
# Mon, 29 Jun 2026 19:12:41 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.11.jar
# Mon, 29 Jun 2026 19:12:41 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.11.jar
# Mon, 29 Jun 2026 19:12:41 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 29 Jun 2026 19:12:41 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jun 2026 19:12:41 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jun 2026 19:12:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jun 2026 19:12:41 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jun 2026 19:12:41 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jun 2026 19:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:41 GMT
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
	-	`sha256:933aa48d778ce753407704113674bd6147537e3fc4637a0c4b2ec4aa58192266`  
		Last Modified: Mon, 29 Jun 2026 19:13:19 GMT  
		Size: 191.2 MB (191222652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30b2700bce35a9c88618c899c26986249fbf47fe2cda7e81bafc9d8f299b63d`  
		Last Modified: Mon, 29 Jun 2026 19:13:22 GMT  
		Size: 344.9 MB (344916459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46f1508fef57b344de72ae91c37ea98fc9aa5090e01297a80e40405099e6f8e`  
		Last Modified: Mon, 29 Jun 2026 19:13:14 GMT  
		Size: 1.1 MB (1067141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7754e06980ac156af53edd1a2fa722731a21e63612fdf9c373ac763558a37b96`  
		Last Modified: Mon, 29 Jun 2026 19:13:14 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9f593acd5f290cc3838bd49e988dba8761546e63edf17413e31350843c10dc`  
		Last Modified: Mon, 29 Jun 2026 19:13:15 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8c8c53659df5b6276c2c3af037c6685a0849469654b42c28e126ae039fb5a`  
		Last Modified: Mon, 29 Jun 2026 19:13:15 GMT  
		Size: 11.0 KB (10980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4315b6ca739ce40417e6e7da92646e9a6d519c570d16e3ae18150695c471af33`  
		Last Modified: Mon, 29 Jun 2026 19:13:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:c958923bcb81a28b9133a366104963785710f8e7332f229171c5b19e76e9437e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9241089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23552b3b3029ce3cceab9a03f1e466812cb68fd4eefec1aaf9249a76d10bffe9`

```dockerfile
```

-	Layers:
	-	`sha256:70ad5c1507bc6dd0ba2e95abd81c1fecb2c35350281a09c68e074723a457196a`  
		Last Modified: Mon, 29 Jun 2026 19:13:14 GMT  
		Size: 9.2 MB (9200328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a948b4e66308b9c84952a6b9d4582768ea5236cd792af879f89d024b592826`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 40.8 KB (40761 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:69e089ece88917aa8686b744a655fb28d82d64c3d04594759ac5db783ea373ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.3 MB (650251305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c916df7ed105c4f74caa33ab3003ae4b5bba797ecc0bc75c92fcf9a45f041d3a`
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
# Mon, 29 Jun 2026 19:10:52 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jun 2026 19:10:52 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jun 2026 19:10:52 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jun 2026 19:10:52 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jun 2026 19:10:52 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jun 2026 19:10:52 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jun 2026 19:10:52 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jun 2026 19:10:52 GMT
ENV XWIKI_VERSION=18.5.0
# Mon, 29 Jun 2026 19:10:52 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.5.0
# Mon, 29 Jun 2026 19:10:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=649a5c53bc7ca02d80b3a3dcd1c03a7534ff868b6fe4f6eafa198602bc31c6df
# Mon, 29 Jun 2026 19:11:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jun 2026 19:11:13 GMT
ENV POSTGRES_JDBC_VERSION=42.7.11
# Mon, 29 Jun 2026 19:11:13 GMT
ENV POSTGRES_JDBC_SHA256=1981b31d3993c58702783c1cddf10a34e48c1f413d70ff1cb6def0a143484647
# Mon, 29 Jun 2026 19:11:13 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.11
# Mon, 29 Jun 2026 19:11:13 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.11.jar
# Mon, 29 Jun 2026 19:11:13 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.11.jar
# Mon, 29 Jun 2026 19:11:14 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 29 Jun 2026 19:11:14 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jun 2026 19:11:14 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jun 2026 19:11:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jun 2026 19:11:14 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jun 2026 19:11:14 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jun 2026 19:11:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:14 GMT
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
	-	`sha256:f8d94e5345bedbba3e1b49deea6167d3e315fe1df000bfe4060d96f4c622fef6`  
		Last Modified: Mon, 29 Jun 2026 19:11:55 GMT  
		Size: 188.9 MB (188877039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b702fd95f86b3f7daa75101c732c58718682e20d2640c9fdf5cb0f7253c4a20`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 344.9 MB (344916408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3466e750bb863a78a515e526992dcc99ce299139342c8eea60be0b294583bf`  
		Last Modified: Mon, 29 Jun 2026 19:11:48 GMT  
		Size: 1.1 MB (1067140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0376a8a488960c88fd716b632e2dc242334f5aadff7901c83a569f767dd3b48e`  
		Last Modified: Mon, 29 Jun 2026 19:11:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bf6c83e9c51b86fe78127ccca36a53f1d65f0cb406471dacad8968451aa6ca`  
		Last Modified: Mon, 29 Jun 2026 19:11:49 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4e7f35f64c1e97d19208fd98d6dd1532ccf90822f616bb0211f667710e078`  
		Last Modified: Mon, 29 Jun 2026 19:11:49 GMT  
		Size: 11.0 KB (10982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293433410d06c402770e132acc332dd232e4d2ddf025c5adb7c48bcc6654520f`  
		Last Modified: Mon, 29 Jun 2026 19:11:50 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:835f1ebd14ea7d12ca49dcd74205dbf87dc8cb84e24d5926988f2a7af7658796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9242015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0745a79adbaf6690b3bc065c28b3876ce2352b254e778860b9a49d8a03b554f`

```dockerfile
```

-	Layers:
	-	`sha256:4455daff59a8b1f3ed3449004c428d6058111460c6a154dfcda0940b8a46d415`  
		Last Modified: Mon, 29 Jun 2026 19:11:48 GMT  
		Size: 9.2 MB (9201081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3bee89f298d64382e745454f163af6eaca91d39a5121aec856d8c3a734ed97`  
		Last Modified: Mon, 29 Jun 2026 19:11:48 GMT  
		Size: 40.9 KB (40934 bytes)  
		MIME: application/vnd.in-toto+json
