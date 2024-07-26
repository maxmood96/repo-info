## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:2dd0f77765b90daeaf07c34af05c72eb5a335d1c0e7ee1a05e03f5e022c5e8e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5c77c18e4f0e500166c974bf5277649764b26ecc68cd8d0f69cc23ecc6158397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.9 MB (577926167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c128d08eac1d673c468819da6ef2a56f4203fcba1eadb678061b06b34aea560f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 26 Jun 2024 09:06:21 GMT
ARG RELEASE
# Wed, 26 Jun 2024 09:06:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 26 Jun 2024 09:06:21 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Wed, 26 Jun 2024 09:06:21 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 09:06:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jun 2024 09:06:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 09:06:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jun 2024 09:06:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 09:06:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jun 2024 09:06:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jun 2024 09:06:21 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_MAJOR=9
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_VERSION=9.0.91
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Wed, 26 Jun 2024 09:06:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT []
# Wed, 26 Jun 2024 09:06:21 GMT
CMD ["catalina.sh" "run"]
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 26 Jun 2024 09:06:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_VERSION=16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=0997ff4cfe16928996218963fad74d7a564c1aa75c7e8434e7cd25bd471ecd5a
# Wed, 26 Jun 2024 09:06:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
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
	-	`sha256:826e3d26fd33e34010b7b031b61a3587f872b8964d27192f060561a78af4478a`  
		Last Modified: Thu, 25 Jul 2024 21:03:20 GMT  
		Size: 179.4 MB (179382297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4990c0c39f7485bf1f58af351e204857efbd902f805f8e154120545a8588095`  
		Last Modified: Thu, 25 Jul 2024 21:03:26 GMT  
		Size: 294.3 MB (294265577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c1c861e971e692c4cac8cc54572cdc581cc2fe87fa55df8453d80feb977218`  
		Last Modified: Thu, 25 Jul 2024 21:03:17 GMT  
		Size: 1.0 MB (1011979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bbadf1c5282fb18ff388dfea3bfda80a1fca40659ae3fcbcd075d2af31f092`  
		Last Modified: Thu, 25 Jul 2024 21:03:17 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ba0c4c9598ab72acd168d99ff0a9a080e7445ed19e5dfd940e82f52b08f375`  
		Last Modified: Thu, 25 Jul 2024 21:03:18 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b24cbbfb256789395b3d130ed18118784b0936e6f0d0c8df54031a103f1ce`  
		Last Modified: Thu, 25 Jul 2024 21:03:18 GMT  
		Size: 6.5 KB (6526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b8dc0bc5395f9a0e48c77b9f9d18a83f2d18d5e2e1ea164054598e34066002`  
		Last Modified: Thu, 25 Jul 2024 21:03:19 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:1bda8f539c72f1cbeeb1dd7004c6c1a4bcf119aaeea17f05c74e01daf49df759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9106364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fda95cfd7ddca8b15701059895e0fdfa14665a252bb14e091954a5d33c749a`

```dockerfile
```

-	Layers:
	-	`sha256:4ed046466e083d5253a6bbc71fc012c5ed1d9b1a0d48ab07e984de1c52f6f554`  
		Last Modified: Thu, 25 Jul 2024 21:03:17 GMT  
		Size: 9.1 MB (9064981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367799d11baa24154582303e5d6dfd83f5cbdbd12e37a587eadec326762ba4c3`  
		Last Modified: Thu, 25 Jul 2024 21:03:17 GMT  
		Size: 41.4 KB (41383 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:de8500e5f0ccc72bd89d1c982c210cddf02e8abc2907a6aeb99046a15b9b9da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570341481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817bd80f234027c654d623e61ef130b8189e5d1ed99304cf180435bd5b89ef66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 26 Jun 2024 09:06:21 GMT
ARG RELEASE
# Wed, 26 Jun 2024 09:06:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 26 Jun 2024 09:06:21 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Wed, 26 Jun 2024 09:06:21 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 09:06:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jun 2024 09:06:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 09:06:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 26 Jun 2024 09:06:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 09:06:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jun 2024 09:06:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 26 Jun 2024 09:06:21 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_MAJOR=9
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_VERSION=9.0.91
# Wed, 26 Jun 2024 09:06:21 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Wed, 26 Jun 2024 09:06:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT []
# Wed, 26 Jun 2024 09:06:21 GMT
CMD ["catalina.sh" "run"]
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 26 Jun 2024 09:06:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_VERSION=16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=0997ff4cfe16928996218963fad74d7a564c1aa75c7e8434e7cd25bd471ecd5a
# Wed, 26 Jun 2024 09:06:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
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
	-	`sha256:e4bca86f2866267f83c4051ef3d3cd83bbb962af3e1418636881362a42810079`  
		Last Modified: Fri, 26 Jul 2024 03:14:58 GMT  
		Size: 174.4 MB (174422840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f4aca1b5845e6e8e8f86c9a6e6a7f23379c9a8c9ca5a20d7d302a84530c7b`  
		Last Modified: Fri, 26 Jul 2024 03:15:01 GMT  
		Size: 294.3 MB (294265650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8ea8f1314e98b7f5bf29c6737dd5541cae63c48e5982f60aa3ffac032c40f1`  
		Last Modified: Fri, 26 Jul 2024 03:14:54 GMT  
		Size: 1.0 MB (1011980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ea3c07a3284d5da65cdf0e612895a3dead694c14ebbb4f2b00a91d47bfb0a`  
		Last Modified: Fri, 26 Jul 2024 03:14:54 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cc789f9639906a2ee3d89683ab197cf66a6b05d250cee29d3e67f9c17cab16`  
		Last Modified: Fri, 26 Jul 2024 03:14:55 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da8de1a3e313540818ca8b0b9fd192ab8c3fde03c0f61d7a16ef16e56c34f35`  
		Last Modified: Fri, 26 Jul 2024 03:14:55 GMT  
		Size: 6.5 KB (6529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa2ad3d0168ee98bdf5d9303928b4c4caa2da8e78587b8ce523d84b1449a773`  
		Last Modified: Fri, 26 Jul 2024 03:14:56 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:7d08cac57d46f700a8b83cc40cd2ca5b3e8d2f1e320ee3034f0ab5a11e5b403e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9107586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a734e683fa62e42c2377d5209b58018204a1c70a9d65a931f7e9162ae8e6a0`

```dockerfile
```

-	Layers:
	-	`sha256:d837a1de00b3eabac64a03157e8fce5ecee46061bd070040687c9c2dba34b17e`  
		Last Modified: Fri, 26 Jul 2024 03:14:54 GMT  
		Size: 9.1 MB (9065555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d9180fe9c51b0440f7122a6bfac6ab978b2c2bcebef77d86168258978a274e`  
		Last Modified: Fri, 26 Jul 2024 03:14:54 GMT  
		Size: 42.0 KB (42031 bytes)  
		MIME: application/vnd.in-toto+json
