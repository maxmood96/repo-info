## `xwiki:15-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:6b07080d27147592266c296522bdd0cc94f23b7fd4b714fb8b843cc0749171be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b9b02a5fc7f0afcee6c3ed7871c052d88cce91a1821a90a7243a32049b4e7503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.3 MB (606292984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f33b3ff023ac51a0de2e43b325c20bd8f78a997d8d0d7e0fc2b4e7e4d5862`
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
# Thu, 05 Dec 2024 10:34:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Dec 2024 10:34:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 10:34:55 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Dec 2024 10:34:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Dec 2024 10:34:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Dec 2024 10:34:55 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Dec 2024 10:34:55 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Dec 2024 10:34:55 GMT
ENV TOMCAT_VERSION=9.0.98
# Thu, 05 Dec 2024 10:34:55 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Thu, 05 Dec 2024 10:34:55 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Dec 2024 10:34:55 GMT
ENTRYPOINT []
# Thu, 05 Dec 2024 10:34:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 05 Dec 2024 10:34:55 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
ENV XWIKI_VERSION=15.10.15
# Thu, 05 Dec 2024 10:34:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.15
# Thu, 05 Dec 2024 10:34:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=93b63b968287f94751285517653083eb2a6da63d7e9af57b5bd7c398d9548033
# Thu, 05 Dec 2024 10:34:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Thu, 05 Dec 2024 10:34:55 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 05 Dec 2024 10:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 10:34:55 GMT
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
	-	`sha256:688f7b98eaa3562c55736637aec927d835eb39a838f24d80c58b6c1d96e5e960`  
		Size: 191.2 MB (191150207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f3352154bf5d29fc9d150d303d0f800c0c7d0a4a84aa370fb3bd8590636b2a`  
		Last Modified: Tue, 10 Dec 2024 05:13:06 GMT  
		Size: 307.1 MB (307144473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84c11be1b0f133eee2b739515b12cc79c2184e9ea9f08009177203c348125f8`  
		Last Modified: Tue, 10 Dec 2024 05:12:58 GMT  
		Size: 681.3 KB (681257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a519bb1301df015d5152ff400475f4424a33d09d16261d1a6fc1fa43a3a4a02`  
		Last Modified: Tue, 10 Dec 2024 05:12:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6558fdda6186d13618e8c1ca582a564a2d7cc3cefdcb5577126dd283d7952b`  
		Last Modified: Tue, 10 Dec 2024 05:12:58 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341fa69f42e5f42368222882c8fbbaccb655ad47cea8e3bf21984359550c56b5`  
		Last Modified: Tue, 10 Dec 2024 05:12:59 GMT  
		Size: 6.5 KB (6464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4f32e9531f263f0b61733fb915926acc82a0058ed648d3387c25adb1320644`  
		Last Modified: Tue, 10 Dec 2024 05:12:59 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:5b4365132ed87d5fe7bd4633339683e95447cf26a57130ffbb0803689c45e4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8824591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bba3007231526eeb0b210421ad363a193a47768e6831d60fb8f767e70a06b33`

```dockerfile
```

-	Layers:
	-	`sha256:f3e917c39235d2a998e04d884706bbf26c8750d72e2a3747ebed0206fa4eadba`  
		Last Modified: Tue, 10 Dec 2024 05:12:57 GMT  
		Size: 8.8 MB (8783561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0f1377de79b823daefe294626388bca2ebca77a5d3337cbccf5b58c29183a4`  
		Last Modified: Tue, 10 Dec 2024 05:12:57 GMT  
		Size: 41.0 KB (41030 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:738a28fc178a824973feed1311b3d976f54e92f8c95545d1145000f260f4e107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.6 MB (602623237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e902a465ccb4214dac43f8bbdca0e95153bf66eb2e0c349b7eb0fdbc96e71c`
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
# Thu, 05 Dec 2024 10:34:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Dec 2024 10:34:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 10:34:55 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Dec 2024 10:34:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Dec 2024 10:34:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Dec 2024 10:34:55 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Dec 2024 10:34:55 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Dec 2024 10:34:55 GMT
ENV TOMCAT_VERSION=9.0.98
# Thu, 05 Dec 2024 10:34:55 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Thu, 05 Dec 2024 10:34:55 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Dec 2024 10:34:55 GMT
ENTRYPOINT []
# Thu, 05 Dec 2024 10:34:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 05 Dec 2024 10:34:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 05 Dec 2024 10:34:55 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
ENV XWIKI_VERSION=15.10.15
# Thu, 05 Dec 2024 10:34:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.15
# Thu, 05 Dec 2024 10:34:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=93b63b968287f94751285517653083eb2a6da63d7e9af57b5bd7c398d9548033
# Thu, 05 Dec 2024 10:34:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Thu, 05 Dec 2024 10:34:55 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Thu, 05 Dec 2024 10:34:55 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Dec 2024 10:34:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 05 Dec 2024 10:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Dec 2024 10:34:55 GMT
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
	-	`sha256:e032e1ab06f86e32c9349c7242400e414926eb0ef02ec8cd99b3e696ce0927f6`  
		Last Modified: Tue, 10 Dec 2024 05:22:22 GMT  
		Size: 307.1 MB (307144484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015f8adc6e799d9f8e7a05d823998df6a83fbbd1fbb31a97ea4661c1b7855ece`  
		Last Modified: Tue, 10 Dec 2024 05:27:06 GMT  
		Size: 681.3 KB (681258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260ce96fd601f2fa73cc887b9c8eb5bb839e6a406b640f88636a5d4f2b804c37`  
		Last Modified: Tue, 10 Dec 2024 05:27:06 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7f755e3b08f3fc82651af6ec2527bf865980f91c7647bd39307b91d3353531`  
		Last Modified: Tue, 10 Dec 2024 05:27:05 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfd8deca0ee3289cee4368fe25c201a0eacb8ab5f0f748f9870554224ce534f`  
		Last Modified: Tue, 10 Dec 2024 05:27:06 GMT  
		Size: 6.5 KB (6466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1422bada4ff32238983b686ad92db3718ea1d85ccb709f6de5f35554ddacdb48`  
		Last Modified: Tue, 10 Dec 2024 05:27:06 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:afe686c96cf288b59dbaf0c70ac1d80517917eea4a8a7f8cac56b928ef951b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8825492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3a1bab0d81a0af6e9f78874edf249bc44fbffdd635c16bb64190709bdcba6d`

```dockerfile
```

-	Layers:
	-	`sha256:731b13e096e3d0642b619f4283f31cc51b793d4dab3289c4747db82cd62c4471`  
		Last Modified: Tue, 10 Dec 2024 05:27:06 GMT  
		Size: 8.8 MB (8784301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49dd87a15482666b5627861a974ca3363e7eac7373ef1eb88b091d5deadaeebb`  
		Last Modified: Tue, 10 Dec 2024 05:27:05 GMT  
		Size: 41.2 KB (41191 bytes)  
		MIME: application/vnd.in-toto+json
