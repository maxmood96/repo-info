## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:cc33682bf8e641f289add0b44002d76b8799c00a3ae0f626691aa0a357750839
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:1879350e9a4000d31cba771d608f5ae603c07693aee30e4daa1d24e8ea73689f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.5 MB (625532258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b4639124691655a67b00c1eecce5bfa24c7d646f9d44214af409fe69ae8c0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
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
# Fri, 05 Sep 2025 16:01:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Sep 2025 16:01:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_VERSION=9.0.109
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Fri, 05 Sep 2025 16:01:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 05 Sep 2025 16:01:09 GMT
ENTRYPOINT []
# Fri, 05 Sep 2025 16:01:09 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Oct 2025 14:43:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_VERSION=16.10.12
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.12
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_DOWNLOAD_SHA256=2a0a3f6eb12177b87d2b15e6fc8b955d171a36c6b9e6acfb32f8c4b980652846
# Fri, 03 Oct 2025 14:43:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Fri, 03 Oct 2025 14:43:49 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Oct 2025 14:43:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 14:43:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2569d95ac3cad1e081eb0cadd06ec41b066fe85885c6d0c029833d09bdeb785`  
		Last Modified: Thu, 02 Oct 2025 05:02:06 GMT  
		Size: 19.4 MB (19377145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99162d145ed15eaef231c1152439075a98c43e224a7d3378dd3569f8132a5557`  
		Last Modified: Thu, 02 Oct 2025 05:02:25 GMT  
		Size: 53.0 MB (52968889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b650b1a0903a78b1352f908bc1ab1a88148d74932ae66ac697b9c7fcfb1ce17`  
		Last Modified: Thu, 02 Oct 2025 05:02:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0474e363db68b6324a1fcffcfbfac1b9084bb1c4e2bfb0df7557e9c92fc7bc5a`  
		Last Modified: Thu, 02 Oct 2025 05:02:09 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1198c80b04218050e7e680da108953d38cf04eff6d3abc833aee816cf863206`  
		Last Modified: Thu, 02 Oct 2025 12:10:03 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c67a8ad587478cfef39059a0b69af70da3e06593e367938cc1d1ca78909f3f0`  
		Last Modified: Thu, 02 Oct 2025 12:11:19 GMT  
		Size: 13.7 MB (13721807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec84443c6e66c39d8dffdbeb7b6e2fc67f831f10f448a24562ed6739c4e84b7a`  
		Last Modified: Thu, 02 Oct 2025 12:11:18 GMT  
		Size: 224.8 KB (224773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b4481a285e4e3ad2421f3c75f31c80ff7ff66478021d0526c53c3cc1f1549f`  
		Last Modified: Fri, 03 Oct 2025 19:00:44 GMT  
		Size: 191.2 MB (191177475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9c152b1dbe1fa5b3045434b761d1618963625635fe0ac780bf6ee933c453b7`  
		Last Modified: Fri, 03 Oct 2025 18:55:53 GMT  
		Size: 317.6 MB (317618825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751001b2eb45d94c92a0014e41c245952fa718413a57393df76ffdcb2cb24170`  
		Last Modified: Fri, 03 Oct 2025 17:52:29 GMT  
		Size: 705.0 KB (704955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3852259f446916cf27c620d8482ea1e469b82f88fee4a45b2814d37d540af44`  
		Last Modified: Fri, 03 Oct 2025 17:52:28 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce2f0e74bcabdcd24dc7fc45ea46d0ff2a830167ed672c3cb99be26a4f581ac`  
		Last Modified: Fri, 03 Oct 2025 17:52:29 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfc7109b27dfe71bafd7c11926c3f5016cc21d31a0c0a3930e7598dd5688a86`  
		Last Modified: Fri, 03 Oct 2025 17:52:32 GMT  
		Size: 6.6 KB (6620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a5613ebfabb7071d1c8fe83c868aacb83f3abe2f6f04ade484dd8c9f4f5d68`  
		Last Modified: Fri, 03 Oct 2025 17:52:28 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:e95fa2316f1f8aa064acbee337249bac6d313218c0e3289adb69dc3cdff1ee91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38edf00b06226318bf031e76bf1a6b10480d71d8b6e338f6c3c51b23ea843b8`

```dockerfile
```

-	Layers:
	-	`sha256:79e615f2feaa0b6793a416c9c2d214f757fd9a974d3b28433a0285820ddf3e25`  
		Last Modified: Fri, 03 Oct 2025 18:07:34 GMT  
		Size: 9.1 MB (9109535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a285ab0e36b5dbcacbb9ab7baafc0d5e6904e6ff28e854177791ae999327080a`  
		Last Modified: Fri, 03 Oct 2025 18:07:35 GMT  
		Size: 40.5 KB (40490 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d1db0ecb9822635c07472e4e6751e954d7c12b66362c460ef7b3992080464065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.4 MB (621360803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3703a1bae220b28f1b220901ce000d434e05be6c593dc7e28fa75069e7d6bce5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 01 Aug 2025 11:04:34 GMT
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
# Fri, 05 Sep 2025 16:01:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Sep 2025 16:01:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_VERSION=9.0.109
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Fri, 05 Sep 2025 16:01:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 05 Sep 2025 16:01:09 GMT
ENTRYPOINT []
# Fri, 05 Sep 2025 16:01:09 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Oct 2025 14:43:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_VERSION=16.10.12
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.12
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_DOWNLOAD_SHA256=2a0a3f6eb12177b87d2b15e6fc8b955d171a36c6b9e6acfb32f8c4b980652846
# Fri, 03 Oct 2025 14:43:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Fri, 03 Oct 2025 14:43:49 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Oct 2025 14:43:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 14:43:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6e0e7ba59c46747fca6b4371f060d57be2b74f88c20ab65b86093a904721df`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 52.1 MB (52148465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f043a2b7ac7283aed8cbd3c5f15d2ea54efec6b3caaee6c9aa3604381c49e35`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8638ac656cf58a686e913d6ff24b9568968c949eb31951f04bdfa835ef450334`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253c73424a202e3d38e2849219b75acafc7c777bfd268cb04fd47c7ac9e55291`  
		Last Modified: Thu, 02 Oct 2025 03:20:22 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af036e8a488c31cff5eb358296d3f8a48f9fbd0a627b731f866443a1a7de566`  
		Last Modified: Thu, 02 Oct 2025 03:20:24 GMT  
		Size: 13.7 MB (13731842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cba829b10231fddbb2cc336f4a702f5ae0ee526bb633bcd276c6f46a8a150e3`  
		Last Modified: Thu, 02 Oct 2025 03:20:23 GMT  
		Size: 225.3 KB (225253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab868a2a32ba0d51e26d7fb4461fe5632ce468ff9dc47a43d8a620a8e1ab8133`  
		Last Modified: Fri, 03 Oct 2025 16:59:07 GMT  
		Size: 188.8 MB (188848170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d113c5f2c02056f7b89f21f055eefa5b52ad80196a19c45098b992e19d8ad`  
		Last Modified: Fri, 03 Oct 2025 16:59:10 GMT  
		Size: 317.6 MB (317618809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b76d2c04df9a31acc129b7779251a6d18da89d39f085546168b296b017f398`  
		Last Modified: Fri, 03 Oct 2025 16:59:15 GMT  
		Size: 704.9 KB (704946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56094e1ec29ef5d27fc4501565d3be9ac5f4d6c40aa164aec3e8c84343e9732d`  
		Last Modified: Fri, 03 Oct 2025 16:59:15 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed6912407a986a495138433920b1292d20e1863775759f260a3da93d44d8c8`  
		Last Modified: Fri, 03 Oct 2025 16:59:15 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c54a3aacbf7d06aa4a3b18095e7c38ca00c73c5a26e2c009be36af51d2dce7`  
		Last Modified: Fri, 03 Oct 2025 16:59:15 GMT  
		Size: 6.6 KB (6618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607654c9534af3b80ae1ee92ca4768a4c5dc63f1888f691940a347747e81f3cd`  
		Last Modified: Fri, 03 Oct 2025 16:59:15 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:68883b409780cf94a15960d9aba3a6966465b63fbbbffcf0dbf5fdd96a8df9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b9af44dcb5103cad7b080da35b08c0c7135d55f9d81890f141c7cd9f7f3e2d`

```dockerfile
```

-	Layers:
	-	`sha256:f4b534a7dace9d0d0be9fd7514a3ea0b364329b8260c12e6112b5d4806ce43d1`  
		Last Modified: Fri, 03 Oct 2025 18:07:43 GMT  
		Size: 9.1 MB (9110276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5679b49241d42b8edb454ded389268b3fa73e3fbd2b91ae776c6a617a3e47fc`  
		Last Modified: Fri, 03 Oct 2025 18:07:44 GMT  
		Size: 40.6 KB (40650 bytes)  
		MIME: application/vnd.in-toto+json
