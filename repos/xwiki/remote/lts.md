## `xwiki:lts`

```console
$ docker pull xwiki@sha256:0aab4045eee4a793aedf27c695b474cbd069fa6cc413da1be53843f8637c876b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:87b8e14da329d359fc6b647293721387afd3935136bc5d50be78c23f8ed13ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 MB (639804200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7e15d5e136cf7b1e3dce56a895e38d4d0e64855f3f2a2bca101bb5b76c054d`
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
# Wed, 13 May 2026 00:14:40 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 May 2026 00:14:40 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:40 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:40 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 May 2026 00:14:40 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 May 2026 00:14:40 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 May 2026 00:14:40 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 00:14:40 GMT
ENV XWIKI_VERSION=17.10.8
# Wed, 13 May 2026 00:14:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.8
# Wed, 13 May 2026 00:14:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=f5dfab908fddb6319e64897bb2fc41661dd5b5d8aafa455db72c8a794eaa5287
# Wed, 13 May 2026 00:15:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Wed, 13 May 2026 00:15:01 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 13 May 2026 00:15:01 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 13 May 2026 00:15:01 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 13 May 2026 00:15:01 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 13 May 2026 00:15:01 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 13 May 2026 00:15:01 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 May 2026 00:15:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 00:15:01 GMT
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
	-	`sha256:e17a3361be7bdce64e0ab4bb4dddcd31105dfd5a30259e8975f2edc7848a435e`  
		Last Modified: Wed, 13 May 2026 00:15:45 GMT  
		Size: 191.2 MB (191245066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91941a4a0b49c2f9cae12a7669b0d4a6e931547d12a91de01f2223c14c450a54`  
		Last Modified: Wed, 13 May 2026 00:15:50 GMT  
		Size: 331.7 MB (331721646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4465fb8430bc2e555e7afb841c74c2703dc1fd51bd2c62615f3437def7f39793`  
		Last Modified: Wed, 13 May 2026 00:15:37 GMT  
		Size: 2.4 MB (2441669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ad8ad89cfc0f7ae977e066bae43fe01396914b010a828ccbe9291ff62ce9e0`  
		Last Modified: Wed, 13 May 2026 00:15:37 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae8f88b4ee23607f7566c5350d672575f4d5fe212810d6f8f5cc3354a0816f1`  
		Last Modified: Wed, 13 May 2026 00:15:39 GMT  
		Size: 2.4 KB (2375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d48a94912a9a7828c7cc72c331513688181e594230f256433247f44228b01e3`  
		Last Modified: Wed, 13 May 2026 00:15:39 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e6fe7c849cf0077eb3ed6a6965d310f183b5928101984b318606b64012bb41`  
		Last Modified: Wed, 13 May 2026 00:15:41 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:c36ce6359193df6e1af60cc52d986d27c82bcb1f8b70708d82a7571945fc8886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9224542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd46c76557bb12153eb97365c34a13f59fb51de888e76a140c3265322ec609`

```dockerfile
```

-	Layers:
	-	`sha256:8913b3a035d35a4dfc3788bbe07987d3233caafad8597f65beec9de604b1be6e`  
		Last Modified: Wed, 13 May 2026 00:15:38 GMT  
		Size: 9.2 MB (9183045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96abd1596875b0a157416e7d475742f42032facd795129aa8b03816313ec4998`  
		Last Modified: Wed, 13 May 2026 00:15:37 GMT  
		Size: 41.5 KB (41497 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2dc030f5fc89e2f344ebcaf43d4b717fd0728769e3facc0f932ce01f2a22474c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.8 MB (635827399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4da401e397e862472cbdb6da81adde6aacf13cff78b53498f8b7eb3923dd02`
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
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 May 2026 00:14:39 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 00:14:39 GMT
ENV XWIKI_VERSION=17.10.8
# Wed, 13 May 2026 00:14:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.8
# Wed, 13 May 2026 00:14:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=f5dfab908fddb6319e64897bb2fc41661dd5b5d8aafa455db72c8a794eaa5287
# Wed, 13 May 2026 00:15:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Wed, 13 May 2026 00:15:01 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Wed, 13 May 2026 00:15:01 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 13 May 2026 00:15:01 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 13 May 2026 00:15:01 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 13 May 2026 00:15:01 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 13 May 2026 00:15:01 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 13 May 2026 00:15:01 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 May 2026 00:15:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 00:15:01 GMT
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
	-	`sha256:e47608155899ed9ce51f07c247a8cd2f0f74122338087b52a43cd3a13bcbe452`  
		Last Modified: Wed, 13 May 2026 00:15:40 GMT  
		Size: 188.9 MB (188916275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db47b26d5d419e3a7e2253736a7087912be282728dd037a7f62c9d4c99d08f`  
		Last Modified: Wed, 13 May 2026 00:15:43 GMT  
		Size: 331.7 MB (331721664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b8c28c27ecf2a3895091017f4ae8d7b0006badb060a0b53cdf3580377b0c84`  
		Last Modified: Wed, 13 May 2026 00:15:34 GMT  
		Size: 2.4 MB (2441669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ca3d99f86c0e4c65bd5152afed19fb9e3e219bb1709bc68055bfa80aec3584`  
		Last Modified: Wed, 13 May 2026 00:15:34 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6a2dcd2f40a9a4e1d8a3384730897605b2f33809d525c6c0771f1d9a2cf175`  
		Last Modified: Wed, 13 May 2026 00:15:35 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b66a334321666267b0cde3819903de9ed696c4d178e786192b422eac892847c`  
		Last Modified: Wed, 13 May 2026 00:15:35 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f15d8649984a36b8e17417b8f17a2c2aeb913338eea3efda3d0046491b956fa`  
		Last Modified: Wed, 13 May 2026 00:15:37 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:2bf349e8061e43fbdf2691db76db1ad858b05ecdfc5c0197e1de4fe258425bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9225542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9973aac008011824637a8a665af3ebb838422fdd73e88d5698309f9e71bbabe`

```dockerfile
```

-	Layers:
	-	`sha256:c6959647a45473a5c11c610ecf99f00f773838929d81eed15ddc2ca8f3a1c7df`  
		Last Modified: Wed, 13 May 2026 00:15:34 GMT  
		Size: 9.2 MB (9183834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d44a401bb0c290b3a9078d924f98d7635a1845d1003241d7ce9565688f1442`  
		Last Modified: Wed, 13 May 2026 00:15:33 GMT  
		Size: 41.7 KB (41708 bytes)  
		MIME: application/vnd.in-toto+json
