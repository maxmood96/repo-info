## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:d36d3633887e50ed00ef72ca3f76620544f8d956405e020f6a71fac4e2ef1aab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:3d608be458c2892ddd978491d28e5517c9d5e4ddcb1a687c8ac60e6a518d61ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.0 MB (641027959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45919c09955765c60555ce417373a9c9654ff223a724e4b59ec6f8fe0cfff5c9`
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
# Thu, 25 Jun 2026 04:12:56 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 25 Jun 2026 04:12:56 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:12:56 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:12:56 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 25 Jun 2026 04:12:56 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 25 Jun 2026 04:12:56 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 25 Jun 2026 04:12:56 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 04:12:56 GMT
ENV XWIKI_VERSION=17.10.9
# Thu, 25 Jun 2026 04:12:56 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.9
# Thu, 25 Jun 2026 04:12:56 GMT
ENV XWIKI_DOWNLOAD_SHA256=b786a85a043cc673e26d887fd0ef34d2fda2f4a9ef4a362360814868ccf41e1f
# Thu, 25 Jun 2026 04:13:17 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 25 Jun 2026 04:13:17 GMT
ENV MARIADB_JDBC_VERSION=3.5.8
# Thu, 25 Jun 2026 04:13:17 GMT
ENV MARIADB_JDBC_SHA256=6127dc7858047b3d4482899139640b0e2ab2b8abdeb708cfb8c011117771cddf
# Thu, 25 Jun 2026 04:13:17 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.8
# Thu, 25 Jun 2026 04:13:17 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.8.jar
# Thu, 25 Jun 2026 04:13:17 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.8.jar
# Thu, 25 Jun 2026 04:13:18 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 25 Jun 2026 04:13:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 25 Jun 2026 04:13:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 25 Jun 2026 04:13:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 25 Jun 2026 04:13:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 04:13:18 GMT
VOLUME [/usr/local/xwiki]
# Thu, 25 Jun 2026 04:13:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 04:13:18 GMT
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
	-	`sha256:71eb5dccb05f0afdd15f07f1b05c5c3c333eed30c8d05f44ec12a68b5d7976ee`  
		Last Modified: Thu, 25 Jun 2026 04:14:02 GMT  
		Size: 191.2 MB (191222777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99e491de8413af75a09e04624df402f07deeb1d868bef3a940483172c9892ca`  
		Last Modified: Thu, 25 Jun 2026 04:14:05 GMT  
		Size: 331.9 MB (331853420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b3bbb9b939285c1939e8c07f9d0b2ee9c88a71b9df8f314c197544700f6ced`  
		Last Modified: Thu, 25 Jun 2026 04:13:54 GMT  
		Size: 712.4 KB (712448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e97a9a1518a5899a254f5afe36cf0aebadcb6893292f350d37357c96bde1b9`  
		Last Modified: Thu, 25 Jun 2026 04:13:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47604eca4cd883c592d4dc25487078f8abf8a1c320163464867101f6483e1f8e`  
		Last Modified: Thu, 25 Jun 2026 04:13:55 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5ba3fe011412dad56ca08c8fbb8ad106c920c41cc0f7db18dcae295e3e7c0d`  
		Last Modified: Thu, 25 Jun 2026 04:13:55 GMT  
		Size: 10.8 KB (10760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25edd37e610f0fc765b2598d488a085612553beb8c5be111f9cbd666aaa3a4`  
		Last Modified: Thu, 25 Jun 2026 04:13:56 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:d253a53885ec13abc1c179a73c11ec77d9c68d5b5a55bf529223b1a4166ec3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc1e995a2ce49c008fd97a4fc4bc5b07612cc6bf4978bdaac127d97a68fae6a`

```dockerfile
```

-	Layers:
	-	`sha256:e859300132b15a60b36a87e22cd0578c031cd3af8e1ddd8300233616e458351b`  
		Last Modified: Thu, 25 Jun 2026 04:13:54 GMT  
		Size: 9.2 MB (9183146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc86ee13bc049f0029e63fc6a7249bf2e5edbde1fca35708fbb14d0ed6e1845`  
		Last Modified: Thu, 25 Jun 2026 04:13:53 GMT  
		Size: 40.5 KB (40462 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ee67995cc6272be330af973752e8ba0277071c56a8b52f4541b325bf5c743500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 MB (636833343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb66cc50f43e9446fcbe804efc5c62fc3b7cf0fbf22c6dc435e8f10c1e6facbb`
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
# Thu, 25 Jun 2026 04:12:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 25 Jun 2026 04:12:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:12:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:12:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 25 Jun 2026 04:12:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 25 Jun 2026 04:12:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 25 Jun 2026 04:12:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 04:12:10 GMT
ENV XWIKI_VERSION=17.10.9
# Thu, 25 Jun 2026 04:12:10 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.9
# Thu, 25 Jun 2026 04:12:10 GMT
ENV XWIKI_DOWNLOAD_SHA256=b786a85a043cc673e26d887fd0ef34d2fda2f4a9ef4a362360814868ccf41e1f
# Thu, 25 Jun 2026 04:12:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 25 Jun 2026 04:12:31 GMT
ENV MARIADB_JDBC_VERSION=3.5.8
# Thu, 25 Jun 2026 04:12:31 GMT
ENV MARIADB_JDBC_SHA256=6127dc7858047b3d4482899139640b0e2ab2b8abdeb708cfb8c011117771cddf
# Thu, 25 Jun 2026 04:12:31 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.8
# Thu, 25 Jun 2026 04:12:31 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.8.jar
# Thu, 25 Jun 2026 04:12:31 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.8.jar
# Thu, 25 Jun 2026 04:12:31 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 25 Jun 2026 04:12:31 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 25 Jun 2026 04:12:31 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 25 Jun 2026 04:12:31 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 25 Jun 2026 04:12:31 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 04:12:31 GMT
VOLUME [/usr/local/xwiki]
# Thu, 25 Jun 2026 04:12:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 04:12:31 GMT
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
	-	`sha256:2bb09b9b17d81ea2b510210272e797074cb65b4b288dc4a8de5e07ca0ff1550e`  
		Last Modified: Thu, 25 Jun 2026 04:13:11 GMT  
		Size: 188.9 MB (188876999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9c931fba06c0e774dbf57c3744a8fad28907766e8acaa2b0049290de2db130`  
		Last Modified: Thu, 25 Jun 2026 04:13:13 GMT  
		Size: 331.9 MB (331853504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82672c483c3f133e98c74c05cd4e322f35be64ba62be08a07e082de992383b7f`  
		Last Modified: Thu, 25 Jun 2026 04:13:04 GMT  
		Size: 712.4 KB (712444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237cfd28000bcdb97277ebed228cc4bc519d5be1bb853b5d52463acc005dcf52`  
		Last Modified: Thu, 25 Jun 2026 04:13:04 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7784c641dc20dd0a507f1c80cc33306ba0ca222b923243315a59ab9ccdc404`  
		Last Modified: Thu, 25 Jun 2026 04:13:05 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c510b71af9cb335f7a8a36b15c52b7a263c7a6dc489b726e2976d28f8e5e30`  
		Last Modified: Thu, 25 Jun 2026 04:13:05 GMT  
		Size: 10.8 KB (10759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5f55dfbf2502b108c73086e016fd41f4c17ba9a7f4465d0c1df15b9434782b`  
		Last Modified: Thu, 25 Jun 2026 04:13:07 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:12bc12cd393881ccb1fd41da6f75fd601ad56c0772a3d41f1361f6939da03910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9224510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6681767214f650efd1a3fcd3d2cfa0b42241e7c9d0c973e4547db15ffbe0c2eb`

```dockerfile
```

-	Layers:
	-	`sha256:e987d82444f94476378662b0c9417a525770947414c13e1d009a8b6bc8232574`  
		Last Modified: Thu, 25 Jun 2026 04:13:04 GMT  
		Size: 9.2 MB (9183887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d862b64843befd1bcbf57376c8267bf0889882ae5eb8f85f2d10458f4ec968bc`  
		Last Modified: Thu, 25 Jun 2026 04:13:04 GMT  
		Size: 40.6 KB (40623 bytes)  
		MIME: application/vnd.in-toto+json
