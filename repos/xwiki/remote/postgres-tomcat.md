## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:fe28da0c9d1359bf8b0a31bcf5f6d1ae3fe17d00cca03f2f99eae16968b66327
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ce0170d0640792260efd534e553fb515ebe7458bb9d071ddaa497aac4b1eb80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.1 MB (616056273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c847cb57a0b94d574e579101fd459c26530094566312b18a83d1325010d637`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Dec 2024 15:07:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 09 Dec 2024 15:07:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 15:07:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 09 Dec 2024 15:07:33 GMT
WORKDIR /usr/local/tomcat
# Mon, 09 Dec 2024 15:07:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 09 Dec 2024 15:07:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 09 Dec 2024 15:07:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 09 Dec 2024 15:07:33 GMT
ENV TOMCAT_MAJOR=9
# Mon, 09 Dec 2024 15:07:33 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 09 Dec 2024 15:07:33 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 09 Dec 2024 15:07:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 09 Dec 2024 15:07:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 15:07:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 09 Dec 2024 15:07:33 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Dec 2024 15:07:33 GMT
ENTRYPOINT []
# Mon, 09 Dec 2024 15:07:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 10 Dec 2024 13:44:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
ENV XWIKI_VERSION=16.10.1
# Tue, 10 Dec 2024 13:44:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.1
# Tue, 10 Dec 2024 13:44:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=f9f365da951626711ec44aebd0276517d8fe1522b1c209c0d3af9c302071ee6e
# Tue, 10 Dec 2024 13:44:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Tue, 10 Dec 2024 13:44:08 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
VOLUME [/usr/local/xwiki]
# Tue, 10 Dec 2024 13:44:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 13:44:08 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8102a0b8aebb9e83cf9b49babb681033fba25f145e468519031ad5707f50183`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 17.0 MB (16966381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e948b4564476a47332ef63d2b656fcb32b4f8aabfde1e9783e2991a957f2f314`  
		Last Modified: Tue, 03 Dec 2024 02:30:20 GMT  
		Size: 46.9 MB (46941841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584d1027889dd7e727c0c5421e5f0e2bcdf156cc2f260f28fe85c1d48018ed81`  
		Last Modified: Tue, 03 Dec 2024 02:30:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac37ec29a9a744ee416c3d313bafb8a47e50e62524ca8773b9515782f326873`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3231c3821950c0b05b6106372497bb01492e45b8060ebe83020c5c87824d7e9`  
		Last Modified: Tue, 10 Dec 2024 02:09:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a565ea0a4cafbddc68b958a13ddc706b7fe78907bfe3418f36d32193c53c8d88`  
		Last Modified: Tue, 10 Dec 2024 02:09:26 GMT  
		Size: 13.4 MB (13418214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c711d8fb95f4043fb7c872a90cbd14a285652e27bc37a5646c838e3094693014`  
		Last Modified: Tue, 10 Dec 2024 02:09:26 GMT  
		Size: 223.4 KB (223408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f252d90fb0412a34ebc9b9eab84390958b0153dfd287ead64441d17c9b6b4a18`  
		Last Modified: Tue, 10 Dec 2024 18:33:53 GMT  
		Size: 191.2 MB (191150010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac3cec3b1f6cc14ed9d4ee312ccea4a01826be586975771133a332850515ab5`  
		Last Modified: Tue, 10 Dec 2024 18:33:54 GMT  
		Size: 316.6 MB (316575348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d73845f7278ba60e0eab390816c15082e5f7f908d7bfb7281c1c1d8f484ac`  
		Last Modified: Tue, 10 Dec 2024 18:33:49 GMT  
		Size: 1.0 MB (1013642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd1bce81e7d156190808910a5f73521f05c09a8558984e231b2a64784876548`  
		Last Modified: Tue, 10 Dec 2024 18:33:49 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b911fb7f195d4d06bc082abc633a602cb1c6858e3185b915756545ba970b6ce1`  
		Last Modified: Tue, 10 Dec 2024 18:33:50 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bebbafdc70236d607b5cab85ba417a590169ecbd35dea8ffe65d72781d5d6ad`  
		Last Modified: Tue, 10 Dec 2024 18:33:50 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f48b8234fa27daa7b1bb30a1fe87ced19eaf38568270039026a3a5fbed70d56`  
		Last Modified: Tue, 10 Dec 2024 18:33:51 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:8860eea9bf5d5f610745b136d481d09415ce4de60c3f3fae0d47a8eebb9fb02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8836276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9362dc17e9a9dd6e676b2543284a7a9d23c362c10a806d077db5c54b8a76639`

```dockerfile
```

-	Layers:
	-	`sha256:fd25d8ad9fc0bc6856df04a200309bd63ab4d16b433ee473a1de6c98e7d376b6`  
		Last Modified: Tue, 10 Dec 2024 18:33:49 GMT  
		Size: 8.8 MB (8794953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b1be66ef8bcebfdd2d0f6cc0365fff0bab85bb7cfa0ba91485614e540fb9f0c`  
		Last Modified: Tue, 10 Dec 2024 18:33:49 GMT  
		Size: 41.3 KB (41323 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:fef84e3a0e817bc0cbbcdf6e14f2eff545e28ba2a2e7215b1263574b6c1c6091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612386716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad59dfc001875ee47237e9c1df43055def9eec1c41b2c6c7ad0938ed9c7f8f21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Dec 2024 15:07:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 09 Dec 2024 15:07:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 15:07:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 09 Dec 2024 15:07:33 GMT
WORKDIR /usr/local/tomcat
# Mon, 09 Dec 2024 15:07:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 09 Dec 2024 15:07:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 09 Dec 2024 15:07:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 09 Dec 2024 15:07:33 GMT
ENV TOMCAT_MAJOR=9
# Mon, 09 Dec 2024 15:07:33 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 09 Dec 2024 15:07:33 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 09 Dec 2024 15:07:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 09 Dec 2024 15:07:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 15:07:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 09 Dec 2024 15:07:33 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Dec 2024 15:07:33 GMT
ENTRYPOINT []
# Mon, 09 Dec 2024 15:07:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 10 Dec 2024 13:44:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 10 Dec 2024 13:44:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
ENV XWIKI_VERSION=16.10.1
# Tue, 10 Dec 2024 13:44:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.1
# Tue, 10 Dec 2024 13:44:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=f9f365da951626711ec44aebd0276517d8fe1522b1c209c0d3af9c302071ee6e
# Tue, 10 Dec 2024 13:44:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Tue, 10 Dec 2024 13:44:08 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Tue, 10 Dec 2024 13:44:08 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 10 Dec 2024 13:44:08 GMT
VOLUME [/usr/local/xwiki]
# Tue, 10 Dec 2024 13:44:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 13:44:08 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636d6d39497cde5edbefcc48f9d73d53c8b5408b69b8cc70ceb265af74eba9e2`  
		Last Modified: Tue, 03 Dec 2024 05:48:36 GMT  
		Size: 17.0 MB (16981577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c00ca83c9141f23bb773168f443dd5ebfe15eb9251d848d166d8fff3158e24e`  
		Last Modified: Tue, 03 Dec 2024 05:51:23 GMT  
		Size: 46.4 MB (46430917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5c0bfb583c70e3d3b37ce5b84ddaf77609232633842ecaf5813b86ce4d4af2`  
		Last Modified: Tue, 03 Dec 2024 05:51:21 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7573b7342583b03280fa66f7b674dec2151c223902f20c24aa397d98d85f88f`  
		Last Modified: Tue, 03 Dec 2024 05:51:21 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca22a4ddc288ae35e07a6cf53adeec6bdad414d4aab28fcee63dd9f4860cd3`  
		Last Modified: Tue, 03 Dec 2024 17:35:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bca028e31a392b6603b7929851a3bac241bd09916d10fa88f606ec036f3cc7b`  
		Last Modified: Tue, 10 Dec 2024 02:47:56 GMT  
		Size: 13.4 MB (13428400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b740db3c43f49f9288e60e87632fa4aa0ddf340b6905cb1d99db0d1ecdff65`  
		Last Modified: Tue, 10 Dec 2024 02:47:56 GMT  
		Size: 223.9 KB (223946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f5870bee79cb7010d55ccb81b32ee776774fedfcb59842e438effda918ebda`  
		Last Modified: Tue, 10 Dec 2024 05:14:01 GMT  
		Size: 188.8 MB (188824761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ecc45da93017188fdb06549bf6d830a1a997dbb743ba1b8a5218214d811c25`  
		Last Modified: Tue, 10 Dec 2024 18:32:16 GMT  
		Size: 316.6 MB (316575340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b0c92704c1f336e4fd2013b39b3a32d92b8fc11ec280ce0745b5474fafc7de`  
		Last Modified: Tue, 10 Dec 2024 18:32:06 GMT  
		Size: 1.0 MB (1013639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7f275bd7925bd4b998b4ad3ee9f92356b1af17ba8a605b6bf2b6a58eee1b7d`  
		Last Modified: Tue, 10 Dec 2024 18:32:06 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612d5a97b84bd07d3fc4dc91fc7bd0f33ab0919f5a7659152fe4399a3aef3a12`  
		Last Modified: Tue, 10 Dec 2024 18:32:06 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d451776453cd4ca2d273d34beb8eb5011b42fa22b462926f302cce50b6390c8d`  
		Last Modified: Tue, 10 Dec 2024 18:32:07 GMT  
		Size: 6.6 KB (6599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10a2f7c33409d141740ded05b6b9fa3516d3c26a491f9c05ac379ca736dc09`  
		Last Modified: Tue, 10 Dec 2024 18:32:07 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:7566fd457c4e721f9549dcb247efe5b393805ce0373b9a6a5695c77f3cfb5c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8837201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cca9b23861e1755e62ac0b2345f2b4b1b6876976612a22e7c1c2d2c3c3cfd74`

```dockerfile
```

-	Layers:
	-	`sha256:f5cef13c927358002d8e8124913107d2cf01e76cd92bcac00555e0fda32778df`  
		Last Modified: Tue, 10 Dec 2024 18:32:06 GMT  
		Size: 8.8 MB (8795705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419fdf21c458d7e156cc4c6e5415c78f92ed4d7a6296bb93236ba0e468b05208`  
		Last Modified: Tue, 10 Dec 2024 18:32:06 GMT  
		Size: 41.5 KB (41496 bytes)  
		MIME: application/vnd.in-toto+json
