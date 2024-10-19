## `xwiki:14-postgres-tomcat`

```console
$ docker pull xwiki@sha256:fcde0e75a29f56bed05cda2f2c06f67a7a52bc2f9e50a7e102b3e668371d0d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:14-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:58573ac1ed53397ae7d05df650e43e6d418137fe9e236f6f08d410c8f548d005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.4 MB (608378601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5e9062d1689cb33f0876969a29bb0def72d5d8ff39c9779e4c787815fec634`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 13 Feb 2024 09:10:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20749b397c3a6bc19ec9ddf36b367cb00bf54de9bec9e01e79d8e7fa2fb32e7d`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 13.8 MB (13767623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0940445ae18372caa52e403c6c8ff97e436110f8061efd3290531a2e34e36b`  
		Last Modified: Sat, 19 Oct 2024 02:06:54 GMT  
		Size: 47.3 MB (47280422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309fceffb97efd41db69e8a254578c4f9ec003685a627105686cae69aa3d83c8`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d982170b03634ac8927b7220b277153cd02acf95debbbae86c02cbb606d5a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d717ac50c6bc6f99fddb0341c93950dda8de80e21588b7776644e2019ec3e`  
		Last Modified: Sat, 19 Oct 2024 04:06:09 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a55ed203e629c8935fe446405e280c324cce48c6409d3b625452f2e8e4c1324`  
		Last Modified: Sat, 19 Oct 2024 04:06:10 GMT  
		Size: 13.4 MB (13373906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4920a2e05dd0c7147ab8fcc0a416b5974a4c1671e20c3278e543c27138f91cdb`  
		Last Modified: Sat, 19 Oct 2024 04:06:10 GMT  
		Size: 212.9 KB (212910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9e82c6b8e6e4f62fa35778c681cff344cc81d22f55d5d5d9433852ce1dfef3`  
		Last Modified: Sat, 19 Oct 2024 04:56:45 GMT  
		Size: 196.5 MB (196450622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd3290fe96d40b11cf8af457518cfde6cf11933003a67f31562e02701366b77`  
		Last Modified: Sat, 19 Oct 2024 04:56:48 GMT  
		Size: 306.5 MB (306538940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39cfea3e87aaf5d07af66da4eb22032d44e8272b1a20f7748b1f2b5bc1df95e`  
		Last Modified: Sat, 19 Oct 2024 04:56:41 GMT  
		Size: 989.0 KB (988987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e8be03c0126d486c39d857537b27b750118a6ec231feda7560fea5f913f549`  
		Last Modified: Sat, 19 Oct 2024 04:56:41 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2a3e56b5674c5889e858133835e31acf8f1105927a1caf957e6d71a0f89b41`  
		Last Modified: Sat, 19 Oct 2024 04:56:42 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad152f6e2b22864cfdcb2b3ca0150c0642fc07bd2f067b7ce84c8e56226e6f6`  
		Last Modified: Sat, 19 Oct 2024 04:56:42 GMT  
		Size: 6.1 KB (6134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c64ea65be59bc2446e69e3935bc7edf5d16544e8d439ee3c33d7268f6fc31b4`  
		Last Modified: Sat, 19 Oct 2024 04:56:43 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:4c4a59861d8eeb7e9aa2bad79f3f72c907c1230c981789a463ee332687deb66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8815359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d098acc1a5d00eb8298e02efd0141dbf185c4efa6e1abe69c8762f54b6e8a0`

```dockerfile
```

-	Layers:
	-	`sha256:f4be7955b566bfd9b94956605fccee40e9569653375f67ed756125f06cf6afc7`  
		Last Modified: Sat, 19 Oct 2024 04:56:41 GMT  
		Size: 8.8 MB (8776569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b779b5a670e78080af3cd3042b909913129bdf7d5f7c002f07af800ff6e7d567`  
		Last Modified: Sat, 19 Oct 2024 04:56:40 GMT  
		Size: 38.8 KB (38790 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:14-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:5b74c39ef55542d71ab977da341c203e626fa8890fa8feda84395499cb168a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.7 MB (605676222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57aa695ff3cb54a1046428f6747e809be2d43666955d434924c88681c253196a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 13 Feb 2024 09:10:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185af607866372c42b75ce6a89acba6d7e5d2cb54d2fb846f7d86da63371897e`  
		Last Modified: Wed, 16 Oct 2024 01:15:52 GMT  
		Size: 13.8 MB (13798568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abe1f00c4a59efc8b8b98a4c72f2a24678aa2ac24213badb68e8c730c7d11fa`  
		Last Modified: Wed, 16 Oct 2024 01:18:34 GMT  
		Size: 46.7 MB (46746395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa4d4c8336cbb9757f56d63c4952e4b1066c14093ab74c11112de2c61da7e9`  
		Last Modified: Wed, 16 Oct 2024 01:18:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e548190d29ede72fe071dd39371bfe2e204f8f8a3dd19c6d316055be7a5ad60`  
		Last Modified: Wed, 16 Oct 2024 01:18:29 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1703032e55e677467db9ab6e29804c68e6150e8b0d2fd82163425e9fe3d7a9c`  
		Last Modified: Wed, 16 Oct 2024 07:40:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa98ec0e64b170664f1a3f83cb6dd3d061f5c36e0b4ab973fc194dc1bd2d0c9`  
		Last Modified: Wed, 16 Oct 2024 07:41:37 GMT  
		Size: 13.4 MB (13386530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b57f6c3a10b03b6911ba82735d1ede0077bcdb895eab33f7a413484c399916d`  
		Last Modified: Wed, 16 Oct 2024 07:41:37 GMT  
		Size: 212.7 KB (212662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d1e2a16ccb72d73d7fe275ca21f97ed5d2b9da697645b1b1cfc845388250a`  
		Last Modified: Wed, 16 Oct 2024 08:05:01 GMT  
		Size: 194.0 MB (194036733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01341ca492f8182e50d0e8dc1a8328e0e2864b23c53cae8de802bfd51ae09d97`  
		Last Modified: Wed, 16 Oct 2024 08:05:02 GMT  
		Size: 306.5 MB (306538706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8668b9944fbb86d340bd517dfa583920b91e4b7827693d0668972cb39c65f5c`  
		Last Modified: Wed, 16 Oct 2024 08:04:56 GMT  
		Size: 989.0 KB (988990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0ab90520f6d26ecdf5f4d1480809ad5a5c25bccde0944617a1325ff7a09d2a`  
		Last Modified: Wed, 16 Oct 2024 08:04:56 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f945ebcf0827065ce1221a9df6b006087d5b618c4f501e1305d2e32bedf2a361`  
		Last Modified: Wed, 16 Oct 2024 08:04:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c23eb5a4ff10efb8ec6f25bfe7a85eae91f73117806d019419b3d667e8af164`  
		Last Modified: Wed, 16 Oct 2024 08:04:57 GMT  
		Size: 6.1 KB (6136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96515a43511570680359a49dbabdd108edc689055c363288634c17ca35deaebe`  
		Last Modified: Wed, 16 Oct 2024 08:04:57 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:f3e053f8cea576e9b395be109e7a578d78f7fd2b63157e130ae1b65f17b0cbbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8698489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e461c06d1e000658e18838cf6dd79139506003acc2e9abc245920c476c56b5`

```dockerfile
```

-	Layers:
	-	`sha256:f8c735873a3326895e23c9291364a2676b0eeb0e1cc43f7c08d8400ce2521ca4`  
		Last Modified: Wed, 16 Oct 2024 08:04:56 GMT  
		Size: 8.7 MB (8659320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab178e5ac68e19185f1e58090c0828511285fdaaf34f5a7db5568d9154482e7`  
		Last Modified: Wed, 16 Oct 2024 08:04:55 GMT  
		Size: 39.2 KB (39169 bytes)  
		MIME: application/vnd.in-toto+json
