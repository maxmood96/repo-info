## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:25f79edfbbd72a5de4dc103ecbf4fbd2fc5b1260e466e816fdf7340710b5d9bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2115f02296e9dcbd5c527123620a0ba37c9959eb410af2b46ca17f2e10485ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.9 MB (607884130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75293539a086c9655a78298a18f79b16567a73a2d065577874292488d6039fb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 21 Oct 2024 15:59:18 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:0429070d206bee5f6b4940b1d1ab86432dca0e2eb92925498f089c8b7df99430`  
		Last Modified: Mon, 21 Oct 2024 18:00:54 GMT  
		Size: 195.5 MB (195456914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a89d9d9d8d70eb3c5f4be6021b49fe1e25e68783e929196d8f1b7dcd00c95d`  
		Last Modified: Mon, 21 Oct 2024 18:00:56 GMT  
		Size: 307.0 MB (307013203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2a210a924b1a47a5c844e546c9a0c3aade8c1cdd49b5c6bc1b9b82fe833656`  
		Last Modified: Mon, 21 Oct 2024 18:00:51 GMT  
		Size: 1.0 MB (1013644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cbeea6a9b9f53150f229e822dafa93068a60033caf59ace658ec6a84f2c396`  
		Last Modified: Mon, 21 Oct 2024 18:00:51 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9f992cbf7b22b85ee9197e8738208f768cb7d66e518446e018b40bacc10c05`  
		Last Modified: Mon, 21 Oct 2024 18:00:52 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c77bbd9c7f02ae341053aaecb4ab94e2cf1e794c8da5408ab55c14ca22ff0`  
		Last Modified: Mon, 21 Oct 2024 18:00:52 GMT  
		Size: 6.5 KB (6465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbce8876bc548984c74ea1b48f9d8db6088307e9b58196f59174c1b5be103958`  
		Last Modified: Mon, 21 Oct 2024 18:00:53 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:efe9ce350a32dcd87363d446be1c8a53eb7838b95e828e25081d5b70d54429a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40634ac0d4a57eec5c9051422266771dc4beb8aa7f127436e05df96edda96ed1`

```dockerfile
```

-	Layers:
	-	`sha256:782ece5973d7e83cba7d959001b7cc0bbe8cebba00041d66fd4e03e60667371b`  
		Last Modified: Mon, 21 Oct 2024 18:00:51 GMT  
		Size: 8.8 MB (8782854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109a6d91437eaaf0543df49bc3502e20ba983a41eb19526dcb70855d14efb564`  
		Last Modified: Mon, 21 Oct 2024 18:00:51 GMT  
		Size: 41.0 KB (41001 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:1675b363efe9859964a609fb89deefe27e0635fee8b9790b1920fb1223910674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.1 MB (604109631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072b8c3aabea3d1348b4d31bd74389129c1c5894c90a994030425766027671b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ARG RELEASE
# Thu, 22 Aug 2024 07:58:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Aug 2024 07:58:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 21 Oct 2024 15:59:18 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:53f4eec6f561250a0d70c55e6bd99d1331023a580a505800e59b70664894053d`  
		Last Modified: Sat, 19 Oct 2024 05:28:16 GMT  
		Size: 13.8 MB (13796069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7674efec743090acabe31a9c87cfc4af0d9e1ebd36b4fcafeff406b927fe5`  
		Last Modified: Sat, 19 Oct 2024 05:39:06 GMT  
		Size: 46.7 MB (46746664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02d0d56a5e588bce0c774599715e9c788b829d3dbe9dc908a858637b545eefc`  
		Last Modified: Sat, 19 Oct 2024 05:39:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9a3e3f11d9a562c5a7cea26bf5fa4a8a858b8fe126aa6ddac4da450cdbfeb`  
		Last Modified: Sat, 19 Oct 2024 05:39:04 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fe37b1877fda729a20a215aa09f8a7fe542bffaae5da1b871ad735bf1465f8`  
		Last Modified: Sat, 19 Oct 2024 21:03:26 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df7be5e56cbc2a715f4cb72c0a0c76aec85d1264adf868a8033937cda68e137`  
		Last Modified: Sat, 19 Oct 2024 21:07:41 GMT  
		Size: 13.4 MB (13386526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95050c8688d73aee237ff31dcf808d439ebdf835e8d2a08a99b191755353b706`  
		Last Modified: Sat, 19 Oct 2024 21:07:40 GMT  
		Size: 212.7 KB (212684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fb0dece9ffb75be9942602ffdd5ef2278db05dba8fb6e68a262c9d5d24e8de`  
		Last Modified: Sat, 19 Oct 2024 23:06:17 GMT  
		Size: 193.0 MB (193039803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acb0e432bbea4cc7ffc6800830dd83d7d2d632fa23e06be3ec0ca12da46a4dc`  
		Last Modified: Mon, 21 Oct 2024 18:55:22 GMT  
		Size: 307.0 MB (307013243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9fe9c6ff5005fe7e3805b698b16766d1073be3d5b3ed96a7f508b3e8deff92`  
		Last Modified: Mon, 21 Oct 2024 18:58:00 GMT  
		Size: 1.0 MB (1013639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54ede4cf0930644de1c2e58e0e1eb126e0493c08cb3e322237a5488a43abb2d`  
		Last Modified: Mon, 21 Oct 2024 18:58:00 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff16dbc92c04c602b54f3667c2acb76ae21dbc8fd80c89bca312e95a9307554b`  
		Last Modified: Mon, 21 Oct 2024 18:58:00 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3a3d0c6921c0dfe5aef9abc4137c0b9da1e5538493cab1d215d31602b375ae`  
		Last Modified: Mon, 21 Oct 2024 18:58:00 GMT  
		Size: 6.5 KB (6465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad4c9e5d7adb5947a06b92407e95c62736dfb5243f33a7d6fae0dc79efd0c43`  
		Last Modified: Mon, 21 Oct 2024 18:58:01 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:07132feec26d7ea89915de6e5ee205df1185c88dc814bcc4cb447a734a537c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8824756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0621fbfa067e694c84f854e88d0d4eeff62a6b409846eef1d34e7bb7746985d5`

```dockerfile
```

-	Layers:
	-	`sha256:0a4a68c45a5e6e81e0b7d11050b51621af82b969e7e86519a0e16afb91cdf797`  
		Last Modified: Mon, 21 Oct 2024 18:58:00 GMT  
		Size: 8.8 MB (8783594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f826bc24a6c86b15789d161b4b91892a5fd27bf51230d4d9f8d231fd2a1fe50`  
		Last Modified: Mon, 21 Oct 2024 18:58:00 GMT  
		Size: 41.2 KB (41162 bytes)  
		MIME: application/vnd.in-toto+json
