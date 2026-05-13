## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:6605baefaa4a67644b9eb7b90ec032ddb289d03eb17cd9f596bfc1ef5d7609da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:954c1ae4420c0f6f35ed7d74b32fc9426913539217d2b24f46f0e878c26a14ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.9 MB (650875729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f567afc16c1174513077c0645afda792b4f65c690e0d1e086fdb8bc7643611ad`
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
# Wed, 13 May 2026 00:14:32 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 May 2026 00:14:32 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:32 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:32 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 May 2026 00:14:32 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 May 2026 00:14:32 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 May 2026 00:14:32 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 00:14:32 GMT
ENV XWIKI_VERSION=18.3.0
# Wed, 13 May 2026 00:14:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.3.0
# Wed, 13 May 2026 00:14:32 GMT
ENV XWIKI_DOWNLOAD_SHA256=3a0594e4260bc832c8a42f9ea1d6f47d9da7c8ffb7bbe65b7c363e7e8308051a
# Wed, 13 May 2026 00:14:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 13 May 2026 00:14:53 GMT
ENV MARIADB_JDBC_VERSION=3.5.8
# Wed, 13 May 2026 00:14:53 GMT
ENV MARIADB_JDBC_SHA256=6127dc7858047b3d4482899139640b0e2ab2b8abdeb708cfb8c011117771cddf
# Wed, 13 May 2026 00:14:53 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.8
# Wed, 13 May 2026 00:14:53 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.8.jar
# Wed, 13 May 2026 00:14:53 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.8.jar
# Wed, 13 May 2026 00:14:53 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 13 May 2026 00:14:53 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 13 May 2026 00:14:53 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 13 May 2026 00:14:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 13 May 2026 00:14:53 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 13 May 2026 00:14:53 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 May 2026 00:14:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 00:14:53 GMT
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
	-	`sha256:f940a442ef83e8cf48e4abf492ba2ed9204827d970061545f2be978ec0827d5b`  
		Last Modified: Wed, 13 May 2026 00:15:37 GMT  
		Size: 191.2 MB (191245002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e63ad8f474950ab52485f6bbe6e2dd905c5f0f9ca7605be1825519b00ed75b`  
		Last Modified: Wed, 13 May 2026 00:15:41 GMT  
		Size: 344.5 MB (344522228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562fc262e5707812f8fb3a393fe8049aff517209751fb017543b975968dc87c`  
		Last Modified: Wed, 13 May 2026 00:15:29 GMT  
		Size: 712.4 KB (712447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d3295374635549636037071139212b37fe8f8f35cf8f1e32bfc02444561b3c`  
		Last Modified: Wed, 13 May 2026 00:15:29 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f517d596ac721b03edd74df591755121c6012f9264cbbf8156560e5654b277e6`  
		Last Modified: Wed, 13 May 2026 00:15:31 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4bfcb07757d37fdc25335f3a99d7e5883f25482c49bf9f7c87c455bbd3d7f3`  
		Last Modified: Wed, 13 May 2026 00:15:31 GMT  
		Size: 11.0 KB (11012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7defcd54b41760a9ec5538ef0ca69dadddd0eb66042694f2dd102386326714`  
		Last Modified: Wed, 13 May 2026 00:15:32 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:80da25c083c8caee01bc41e45d1f5549a725b2d451494ed2c32811e911f237a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9239667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d10cc13fe322c2b7219578071eca1172a2e414f961a42a80d0c96c8a36269c0`

```dockerfile
```

-	Layers:
	-	`sha256:ce24bc1f1b186c7c226b4a963b5f5142218a36283d77769bf25af12f3d920a37`  
		Last Modified: Wed, 13 May 2026 00:15:30 GMT  
		Size: 9.2 MB (9198899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec05cde3c8067953169a50688903151eb9afb1b0428ba6c7a026c9baf032824`  
		Last Modified: Wed, 13 May 2026 00:15:29 GMT  
		Size: 40.8 KB (40768 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2f33551641d0230526b9416afa8500bbcaa1828018c0eb952d54370b1264ee37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.9 MB (646898844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62033afa82392c3c24cbfad9a12b52d5951da8a2a32f8e051ef4297909c84328`
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
# Wed, 13 May 2026 00:14:35 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 May 2026 00:14:35 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:35 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:35 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 May 2026 00:14:35 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 May 2026 00:14:35 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 May 2026 00:14:35 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 00:14:35 GMT
ENV XWIKI_VERSION=18.3.0
# Wed, 13 May 2026 00:14:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.3.0
# Wed, 13 May 2026 00:14:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=3a0594e4260bc832c8a42f9ea1d6f47d9da7c8ffb7bbe65b7c363e7e8308051a
# Wed, 13 May 2026 00:14:57 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 13 May 2026 00:14:57 GMT
ENV MARIADB_JDBC_VERSION=3.5.8
# Wed, 13 May 2026 00:14:57 GMT
ENV MARIADB_JDBC_SHA256=6127dc7858047b3d4482899139640b0e2ab2b8abdeb708cfb8c011117771cddf
# Wed, 13 May 2026 00:14:57 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.8
# Wed, 13 May 2026 00:14:57 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.8.jar
# Wed, 13 May 2026 00:14:57 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.8.jar
# Wed, 13 May 2026 00:14:57 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 13 May 2026 00:14:57 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 13 May 2026 00:14:57 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 13 May 2026 00:14:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 13 May 2026 00:14:58 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 13 May 2026 00:14:58 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 May 2026 00:14:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 00:14:58 GMT
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
	-	`sha256:64d57db04fc6dd4b515f43e8c1603fe6203300ad4d794b665c29368b7c589d0a`  
		Last Modified: Wed, 13 May 2026 00:15:38 GMT  
		Size: 188.9 MB (188916079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0286f5d078e47eaabf651f6eff31da06f1081bf78b3d6a75c222f8f3dd7ec8`  
		Last Modified: Wed, 13 May 2026 00:15:42 GMT  
		Size: 344.5 MB (344522282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a53b45e56bdc880d749b166a204a5527716a56cb86fd7e0d7eac51736f3d7f3`  
		Last Modified: Wed, 13 May 2026 00:15:31 GMT  
		Size: 712.4 KB (712448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3927e20d4b70f15e8d4be413fe891535356776e3da24305c5854eaf940c2645a`  
		Last Modified: Wed, 13 May 2026 00:15:31 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80b377c9e4d5d362c1098b280827a67594ac46f8a6dc2c8cbb87e10e425b7c5`  
		Last Modified: Wed, 13 May 2026 00:15:32 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7a9944cb10ae291ca6895fada38980f3848c71c9422d2abed08fc7335c4b9c`  
		Last Modified: Wed, 13 May 2026 00:15:32 GMT  
		Size: 11.0 KB (11013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb5d4244db458d8d14855f5911e2d7fdc0374db303b9e0da425abe5f945061c`  
		Last Modified: Wed, 13 May 2026 00:15:33 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:fbbbaf73114ddda6221909a9b1971d8a779a3c82881c8ae68f729eb9dd342215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9240593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad52d2a62ccdd0d2d53d972f795abe670510b42de542986da4dbd6ef4e1ef`

```dockerfile
```

-	Layers:
	-	`sha256:e19f127e937255488ef38b8977abe7a39fa62fcfc6d9200c8816c30e71629975`  
		Last Modified: Wed, 13 May 2026 00:15:31 GMT  
		Size: 9.2 MB (9199652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564721e2ec81d12a12b88c203aca45a4aa81a4b0d53372d5bcc0a9242af9c4df`  
		Last Modified: Wed, 13 May 2026 00:15:31 GMT  
		Size: 40.9 KB (40941 bytes)  
		MIME: application/vnd.in-toto+json
