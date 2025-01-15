## `xwiki:stable-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:35a9ee31a784f0da4d808c2d5220fca79c1df5bef6e72dbc9e1e61be23c0d496
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:da7128fda4f5c17884aab91e95bb660e6e1a42628d4ac9d23ea77d1ab6fdecc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.4 MB (616434798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997f0578d0f953ea50a066731565874867e26f0891917752b21872d400ad198a`
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
# Thu, 26 Dec 2024 14:50:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 26 Dec 2024 14:50:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2024 14:50:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
WORKDIR /usr/local/tomcat
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 26 Dec 2024 14:50:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_MAJOR=9
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_VERSION=9.0.98
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Thu, 26 Dec 2024 14:50:58 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT []
# Thu, 26 Dec 2024 14:50:58 GMT
CMD ["catalina.sh" "run"]
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 26 Dec 2024 14:50:58 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_VERSION=16.10.2
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.2
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_DOWNLOAD_SHA256=1a6287416db4243e3d40939e19509ca4ebe9e4f46f8fcf7204f223bcfff8b6e2
# Thu, 26 Dec 2024 14:50:58 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Thu, 26 Dec 2024 14:50:58 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
VOLUME [/usr/local/xwiki]
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2024 14:50:58 GMT
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
		Last Modified: Fri, 13 Dec 2024 15:52:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac37ec29a9a744ee416c3d313bafb8a47e50e62524ca8773b9515782f326873`  
		Last Modified: Fri, 13 Dec 2024 15:21:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fa6d05f80a2196e166688bbecf02378b409a935b995dca5fc900fdf4802b31`  
		Last Modified: Tue, 14 Jan 2025 02:41:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f574b0618e30098ea39fc0190d74fde8640ddb397f16a507b0aac18f7a36653f`  
		Last Modified: Tue, 14 Jan 2025 20:40:31 GMT  
		Size: 13.4 MB (13440285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5c2edf69f5d13f2305291af2caec384b18a2b265ec58917f4e0f9196eee466`  
		Last Modified: Tue, 14 Jan 2025 20:40:30 GMT  
		Size: 223.4 KB (223435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca5b6c0793918b6a42bf1189887ec6734a8e8875e375f69858c858ded5361f2`  
		Last Modified: Tue, 14 Jan 2025 03:26:15 GMT  
		Size: 191.7 MB (191716637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704e9193f98c61d0cb7f3f50d50816b04ca5d5458efec1ce2d4fc2536bfae501`  
		Last Modified: Wed, 15 Jan 2025 01:00:42 GMT  
		Size: 316.7 MB (316697628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c699297ba15141a8a0360a35d7cbe2474e9f5865fd8e38549d037c14b6114b`  
		Last Modified: Tue, 14 Jan 2025 03:26:10 GMT  
		Size: 681.3 KB (681255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9570294e1caf51e516ec339b69726ffcfd0291c56275dafea5c6f622a6212c51`  
		Last Modified: Tue, 14 Jan 2025 03:26:10 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1239fe1ec3d068c181320f7036f0c069398e4ea9c3b0539d6e4a48dd42fc387`  
		Last Modified: Tue, 14 Jan 2025 03:26:11 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f599d23831d91ef777eb38425166d043c5c8d72611c59a0dd7495b5dc8c54a`  
		Last Modified: Wed, 15 Jan 2025 02:00:17 GMT  
		Size: 6.6 KB (6597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0840a91e0615af71e9ae14ca996278ccfea4295272ed95ab05149d67f0805`  
		Last Modified: Tue, 14 Jan 2025 21:07:54 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:4bae98160f5592549e4c6f6621b0047e5566a617fa25aea81838d84d108eb6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c3aa4774fe499ca7e6303692cd5450fa87fbe4cfed97c8ede2f089bc49e3a3`

```dockerfile
```

-	Layers:
	-	`sha256:33eca7ca004e83c5968e276de6d81a5ab2838623ea8d2e74d70a86fec6951a93`  
		Last Modified: Tue, 14 Jan 2025 03:26:10 GMT  
		Size: 8.8 MB (8753594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef4cbc3ad86ebb32ed83ce5b812cbbc9e4af5410fc0b9b315e301d98b82365e`  
		Last Modified: Tue, 14 Jan 2025 03:26:09 GMT  
		Size: 41.4 KB (41435 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:1b6fc51e56637a23c9910d9b88410f4605ac9b67e35433cbea4c7c7eed13b844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.7 MB (612728938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1892eab3be734fa867aaaad81daf94ebc718e87e8ba6d7b953ffee2796fa460d`
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
# Thu, 26 Dec 2024 14:50:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 26 Dec 2024 14:50:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Dec 2024 14:50:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
WORKDIR /usr/local/tomcat
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 26 Dec 2024 14:50:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_MAJOR=9
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_VERSION=9.0.98
# Thu, 26 Dec 2024 14:50:58 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Thu, 26 Dec 2024 14:50:58 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT []
# Thu, 26 Dec 2024 14:50:58 GMT
CMD ["catalina.sh" "run"]
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 26 Dec 2024 14:50:58 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 26 Dec 2024 14:50:58 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_VERSION=16.10.2
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.2
# Thu, 26 Dec 2024 14:50:58 GMT
ENV XWIKI_DOWNLOAD_SHA256=1a6287416db4243e3d40939e19509ca4ebe9e4f46f8fcf7204f223bcfff8b6e2
# Thu, 26 Dec 2024 14:50:58 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_VERSION=3.5.1
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Thu, 26 Dec 2024 14:50:58 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Thu, 26 Dec 2024 14:50:58 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Dec 2024 14:50:58 GMT
VOLUME [/usr/local/xwiki]
# Thu, 26 Dec 2024 14:50:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2024 14:50:58 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Fri, 13 Dec 2024 13:09:54 GMT  
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
		Last Modified: Fri, 13 Dec 2024 17:02:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7573b7342583b03280fa66f7b674dec2151c223902f20c24aa397d98d85f88f`  
		Last Modified: Fri, 13 Dec 2024 20:17:04 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7262991182989bcbde11009a69b17999af5df3cd07d4d8b95114ad70dfccd8`  
		Last Modified: Tue, 14 Jan 2025 11:56:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16ffe8fdbf7ab23da3b356cb66e1d5117fbf163fe1e9805854d52ebb95d7b7c`  
		Last Modified: Wed, 15 Jan 2025 04:01:21 GMT  
		Size: 13.5 MB (13450954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14679ef59efb92a67a72ae685e193fe16627744fa280e33b7ad6e6d57a68787`  
		Last Modified: Tue, 14 Jan 2025 23:06:32 GMT  
		Size: 223.9 KB (223950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9c7e2d2ab4557840b2b4e664d5279b244123fec74d622662a68247c29b0ee3`  
		Last Modified: Wed, 15 Jan 2025 00:14:43 GMT  
		Size: 189.4 MB (189354726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a702bd4d9175d8d8e0bd272b97724341507780f45d2f42873420492a62a16907`  
		Last Modified: Tue, 14 Jan 2025 16:01:15 GMT  
		Size: 316.7 MB (316697530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac443ae79bafc508cdb661f5e2794817984464d0f2bf1edddafb25c1942ac2`  
		Last Modified: Wed, 15 Jan 2025 01:01:56 GMT  
		Size: 681.3 KB (681258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0760516ba59220350427f6a62a9a3613bdba6ef0d45921e0811db75ebe5e4f28`  
		Last Modified: Wed, 15 Jan 2025 01:01:57 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df29732da1918dd8e2c27859b04ecc4561f88cad68f152cc0760e5d4e6151f5`  
		Last Modified: Tue, 14 Jan 2025 16:02:34 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931307fc06d6b54e964b2367b56723270467162749400a7ebc372012f80f8de`  
		Last Modified: Wed, 15 Jan 2025 04:11:42 GMT  
		Size: 6.6 KB (6599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce19cae3643f0dd02134bfe890994f5c7debc22440400c2d7a48f543a5906a2d`  
		Last Modified: Tue, 14 Jan 2025 16:02:35 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:33b51fb0d00098a14c3b7fedd20e93f51233d843ae87e88e1e3923df54370194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8796004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84551d9995f4e526162b6559cee1f705291bfa8b55d3ce224160740dd894abb`

```dockerfile
```

-	Layers:
	-	`sha256:591284937d9fda90294a97434d5c742ff2440d561e3271e217c001890dca176e`  
		Last Modified: Tue, 14 Jan 2025 16:02:34 GMT  
		Size: 8.8 MB (8754371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1696e948a09d124421d871b1353ebc0f8191939e193a3d4cd98f86e7ba5ab09f`  
		Last Modified: Wed, 15 Jan 2025 07:34:42 GMT  
		Size: 41.6 KB (41633 bytes)  
		MIME: application/vnd.in-toto+json
