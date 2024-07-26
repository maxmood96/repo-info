## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:f9ad4db1543f5330fb4bc6ae633b07f514eab5da0f3629b88b2dcb2a013272fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:cc0694f616e51d30b2c61c553bb4141b7f335edf9c3b1d1fe2bb1989be418358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.1 MB (591072026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa9415ca8f3e1aeaa7d1eb8dd0a470d750d4e67b47b2f82245b403bc5948885`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 27 Jun 2024 13:08:28 GMT
ARG RELEASE
# Thu, 27 Jun 2024 13:08:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 13:08:28 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_MAJOR=9
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 27 Jun 2024 13:08:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT []
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 27 Jun 2024 13:08:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_VERSION=8.4.0
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_SHA256=d77962877d010777cff997015da90ee689f0f4bb76848340e1488f2b83332af5
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.4.0
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.4.0.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.4.0.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
VOLUME [/usr/local/xwiki]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f05e0c470fe19918a4af17eda4c3c834422ca9ed93b2de24950e8aad0a0fff`  
		Last Modified: Thu, 25 Jul 2024 20:08:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdb07bfe42a20f2cd030c81fa9ad17c22dd69661de1b765db64b564c9d0953c`  
		Last Modified: Thu, 25 Jul 2024 20:08:45 GMT  
		Size: 12.4 MB (12442381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f193b178fdc20c06503220f2d211fc9970df5681afb5f3eaa7538f61e0811e6`  
		Last Modified: Thu, 25 Jul 2024 20:08:45 GMT  
		Size: 217.8 KB (217846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8820f7185121ff9d829d1ad9feae5b861696fda9fb4365195649b318ac87e8`  
		Last Modified: Thu, 25 Jul 2024 21:03:31 GMT  
		Size: 178.4 MB (178444115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4be8d516731fc8053f19afe19a38182355c0b1120ba4d76f3abcf5e2dc67e8`  
		Last Modified: Thu, 25 Jul 2024 21:03:33 GMT  
		Size: 307.0 MB (306968169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862985bf53acf3c19b54d2afc9f01720b1eb560baae594b52cf8bb39755c5427`  
		Last Modified: Thu, 25 Jul 2024 21:03:27 GMT  
		Size: 2.4 MB (2393572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77ec14242a1d6bde5ac50a08a0bd355ad5a9d1d44d4d0270a14d81bb3f0c973`  
		Last Modified: Thu, 25 Jul 2024 21:03:26 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457f0a4c15feddfc7bd99a29d1a6a8de28b79279b2077b16425f78fc698d0b63`  
		Last Modified: Thu, 25 Jul 2024 21:03:28 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcd908473020cd738151052fb9c15c956825f0ecb09af4fe93c70b31cfb6c77`  
		Last Modified: Thu, 25 Jul 2024 21:03:28 GMT  
		Size: 6.4 KB (6431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36e7628182518f0d95c51d1fd926c1193fc62f39ba564baa292fd032f2b03d3`  
		Last Modified: Thu, 25 Jul 2024 21:03:29 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:02d8e69c2519c8b7ff6c8d652dddcfbc03b7847c21cd3317ccf90af83f50a41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9109213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a27932da75d9581079aee048679102bfb53a96824dde55afdf38e2cac04df0`

```dockerfile
```

-	Layers:
	-	`sha256:cd3a36298fb9ba2726d4069aca11a7f0ddc3ac6558909e18a5c764ad497a22e6`  
		Last Modified: Thu, 25 Jul 2024 21:03:27 GMT  
		Size: 9.1 MB (9067174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e75261c06de0c166ee4cb878db9d487988cf2f298abb209e1075e9ec1bfeaa`  
		Last Modified: Thu, 25 Jul 2024 21:03:26 GMT  
		Size: 42.0 KB (42039 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8077e9d11a4464d4bf554dcbfeeab4fcdd78216915703fa2447ebfb9dbf14d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583480438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7df71d1f10d09135a0ff34d0ae9c0a8fdfe3becbeee4e7d049a7e834af190b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 27 Jun 2024 13:08:28 GMT
ARG RELEASE
# Thu, 27 Jun 2024 13:08:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 13:08:28 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_MAJOR=9
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 27 Jun 2024 13:08:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT []
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 27 Jun 2024 13:08:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_VERSION=8.4.0
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_SHA256=d77962877d010777cff997015da90ee689f0f4bb76848340e1488f2b83332af5
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.4.0
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.4.0.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.4.0.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
VOLUME [/usr/local/xwiki]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3111de98c20040058bea11c27a5e778456de5a7ddfd95d12181ae4e957d00f`  
		Last Modified: Fri, 26 Jul 2024 02:21:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e06e0924efe8009d39115128b6ae083770ee28f8e31da8ca1414a54e65fa20`  
		Last Modified: Fri, 26 Jul 2024 02:22:27 GMT  
		Size: 12.4 MB (12448777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c670c389695106d88747dd0c5a114b40d724869dff39c8f3b76b6116e258a2`  
		Last Modified: Fri, 26 Jul 2024 02:22:26 GMT  
		Size: 216.8 KB (216777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c3101dbce77e8ae0799c890839e887b4f0d5f3eb029648034e35144160ce31`  
		Last Modified: Fri, 26 Jul 2024 03:13:04 GMT  
		Size: 173.5 MB (173477887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ec32e0d27da3c743cb44bcbab31353ce22607a44d8bc7a66ab7b063fa85565`  
		Last Modified: Fri, 26 Jul 2024 03:17:04 GMT  
		Size: 307.0 MB (306968122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba4ee10c364e40ac7b5b96899ae7e719ea09d717f8a5e3a7cc5ea31dc3fbe4`  
		Last Modified: Fri, 26 Jul 2024 03:16:56 GMT  
		Size: 2.4 MB (2393576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b28b704c0668aebc4f7f41fd1ae8671a9f24c384ceed59dd81c8fdfd08fece6`  
		Last Modified: Fri, 26 Jul 2024 03:16:55 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5dc1688ae986cf68022ec1a58cc8b5682b5cfbdaf978fff3913ff58abc4c26`  
		Last Modified: Fri, 26 Jul 2024 03:16:55 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5351b5bfa77ad90fe207ca39f6d1c17afd836fdf9248b90517569b6b7f3d1a`  
		Last Modified: Fri, 26 Jul 2024 03:16:56 GMT  
		Size: 6.4 KB (6430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746494fab455e3a3cae9e4c21dffbb05aa511b37465d40397c63870a8d7eb338`  
		Last Modified: Fri, 26 Jul 2024 03:16:56 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:6d180872ea47ad53f28949c0c9091629adf8e213f1e6082394060310a50403a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9110508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb92dc8febf1ec15cecb8da5dff760ebae6fd055bcafcad902c419e9e236396`

```dockerfile
```

-	Layers:
	-	`sha256:eef54b31a55eca4fd7a7779789d079aefdee3d0b2a8f896c10550ac9dbad8cc4`  
		Last Modified: Fri, 26 Jul 2024 03:16:55 GMT  
		Size: 9.1 MB (9067784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f111d1e9917eb5fb43541c220af536df844454a223e31a2221d460e4a8468109`  
		Last Modified: Fri, 26 Jul 2024 03:16:54 GMT  
		Size: 42.7 KB (42724 bytes)  
		MIME: application/vnd.in-toto+json
