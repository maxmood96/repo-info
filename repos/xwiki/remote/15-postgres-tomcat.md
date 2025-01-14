## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:a244bcf39e24b9628ad49f49cf035ea528bf9b9f2ccc9d6dcb248bf7677eb726
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8f8fb2701ba5455106fe01cec95e02a0af7225135231516bd8a649c8b999ba41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.2 MB (607214039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8a6a2cfaf13df31a030e9cf1bb637d4fa33aa4f7509ec3965ed181fd7f3039`
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
ENV POSTGRES_JDBC_VERSION=42.7.4
# Thu, 05 Dec 2024 10:34:55 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Thu, 05 Dec 2024 10:34:55 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Thu, 05 Dec 2024 10:34:55 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Thu, 05 Dec 2024 10:34:55 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Thu, 05 Dec 2024 10:34:55 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
		Last Modified: Fri, 13 Dec 2024 13:08:53 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8102a0b8aebb9e83cf9b49babb681033fba25f145e468519031ad5707f50183`  
		Last Modified: Fri, 13 Dec 2024 15:14:23 GMT  
		Size: 17.0 MB (16966381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e948b4564476a47332ef63d2b656fcb32b4f8aabfde1e9783e2991a957f2f314`  
		Last Modified: Fri, 13 Dec 2024 15:10:16 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:41:56 GMT  
		Size: 13.4 MB (13440285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5c2edf69f5d13f2305291af2caec384b18a2b265ec58917f4e0f9196eee466`  
		Last Modified: Tue, 14 Jan 2025 02:41:56 GMT  
		Size: 223.4 KB (223435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e396447fb08fd6cb20dcce17dfc72e18991da6b01b49b187d3e0db3c36eab35`  
		Last Modified: Tue, 14 Jan 2025 03:26:05 GMT  
		Size: 191.7 MB (191716605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2344c09b038949e6d7317d5f39b7d7223521f65a6a49678048ea1a5204e9b6b1`  
		Last Modified: Tue, 14 Jan 2025 03:26:08 GMT  
		Size: 307.1 MB (307144547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6aca56d124cc68506644ac5b8220b1c87118f632b327dde32e5d3dd7779362`  
		Last Modified: Tue, 14 Jan 2025 03:26:02 GMT  
		Size: 1.0 MB (1013641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ee873a2b64f3497afcf7a63d188f737b243f3463bf4e2d902eb353f9448068`  
		Last Modified: Tue, 14 Jan 2025 03:26:02 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4092415fa79bf83ffce6441e461ac334a7f89d3464f266de7114450d9456fec4`  
		Last Modified: Tue, 14 Jan 2025 03:26:03 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dce3df53ecbb2ef47f03a6045178d7cbe8db3bce4115d078014fcf04c505f7d`  
		Last Modified: Tue, 14 Jan 2025 03:26:03 GMT  
		Size: 6.5 KB (6464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6900d036d6e593cee23804fccfa905bb8d886a6431a4fd1e1c71f21a38b01`  
		Last Modified: Tue, 14 Jan 2025 03:26:04 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:35eae4e83e50089eeb5cb8b4545c67cc4806b521acbf389b8c770a04fb61c994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8783732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270c54aa9d29f42f85c183e2c854a510d9f5cbac94aba7377a24923731f5dae3`

```dockerfile
```

-	Layers:
	-	`sha256:3b72fd17cafccff8787ba484b77805ad8ae82c16b19f7de49e7c02a82f441293`  
		Last Modified: Tue, 14 Jan 2025 03:26:02 GMT  
		Size: 8.7 MB (8743894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5ae7d0236773ce662920f5cb04473a7c052ce5407380a3944a263bcb12725c`  
		Last Modified: Tue, 14 Jan 2025 03:26:02 GMT  
		Size: 39.8 KB (39838 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d1b5017dafab0c91feee78d5abc337c074fa866e9e594a3c06eec175b5a8e5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.5 MB (603508242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d125535a53df3ff00326dac91d61396abe41d7fe56a6f8c6c497551b5c611b`
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
ENV POSTGRES_JDBC_VERSION=42.7.4
# Thu, 05 Dec 2024 10:34:55 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Thu, 05 Dec 2024 10:34:55 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Thu, 05 Dec 2024 10:34:55 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Thu, 05 Dec 2024 10:34:55 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Thu, 05 Dec 2024 10:34:55 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
		Last Modified: Fri, 13 Dec 2024 15:49:37 GMT  
		Size: 17.0 MB (16981577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c00ca83c9141f23bb773168f443dd5ebfe15eb9251d848d166d8fff3158e24e`  
		Last Modified: Fri, 13 Dec 2024 16:07:19 GMT  
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
		Last Modified: Tue, 14 Jan 2025 12:00:37 GMT  
		Size: 13.5 MB (13450954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14679ef59efb92a67a72ae685e193fe16627744fa280e33b7ad6e6d57a68787`  
		Last Modified: Tue, 14 Jan 2025 12:00:37 GMT  
		Size: 223.9 KB (223950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9c7e2d2ab4557840b2b4e664d5279b244123fec74d622662a68247c29b0ee3`  
		Last Modified: Tue, 14 Jan 2025 16:01:13 GMT  
		Size: 189.4 MB (189354726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cadc6e220033e82a6dd4757670a63043bba059e596fccd0a9f1982a330b63e7`  
		Last Modified: Tue, 14 Jan 2025 16:03:58 GMT  
		Size: 307.1 MB (307144476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aead3001e8f60787a29dbb49f041c4b219e1852024a1845d03176239d383360`  
		Last Modified: Tue, 14 Jan 2025 16:04:34 GMT  
		Size: 1.0 MB (1013648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c1e535a5c4d1dfb22973008e8e42fd4a29c19e85d5b4df11b8a329650eef14`  
		Last Modified: Tue, 14 Jan 2025 16:04:33 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648321e9f06c71224fdc23f32bcf97aa5aecb84cd5ea80741b61273080f27bdc`  
		Last Modified: Tue, 14 Jan 2025 16:04:33 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0de82e2ece1f36e4eb77db01dba29961723258002ac134a3007d8e57be1478`  
		Last Modified: Tue, 14 Jan 2025 16:04:34 GMT  
		Size: 6.5 KB (6464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0b35e7dbe71da2b7f2998c44f335badddd30ac73e74317ba9726de94b492f`  
		Last Modified: Tue, 14 Jan 2025 16:04:34 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:7603df32aeb9d0a08c43e44dc738f0c05935bc7cb5f00049652bf78ed5a33e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8784587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e569898d3c86d2aa51e70defd87fc4716902227b25a015effde004b25a4776`

```dockerfile
```

-	Layers:
	-	`sha256:69c07f69dc92e54d0f8bde508cbf54f297516417a2d54ddbddff9430531c8b18`  
		Last Modified: Tue, 14 Jan 2025 16:04:34 GMT  
		Size: 8.7 MB (8744611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0879fe211a3ff348951dabb83b4dc5b090d639033b3731a8cadf79b0771313f`  
		Last Modified: Tue, 14 Jan 2025 16:04:33 GMT  
		Size: 40.0 KB (39976 bytes)  
		MIME: application/vnd.in-toto+json
