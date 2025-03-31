## `xwiki:stable`

```console
$ docker pull xwiki@sha256:6bbf39623653b335b9cec00af7401fb2f3f30ced12aa8acef2d05af229f6850e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:8f18d5d9a9b1c61e1b393a199cf63337decdeb60aa660d786b89b46c8ef5116b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 MB (640028011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e296bf7bd95d40e69cd7b8809b3047292ecac635b94c73e3826ec764c8071508`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 07 Mar 2025 21:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 07 Mar 2025 21:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Mar 2025 21:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 07 Mar 2025 21:03:19 GMT
WORKDIR /usr/local/tomcat
# Fri, 07 Mar 2025 21:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 07 Mar 2025 21:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 07 Mar 2025 21:03:19 GMT
ENV TOMCAT_MAJOR=10
# Fri, 07 Mar 2025 21:03:19 GMT
ENV TOMCAT_VERSION=10.1.39
# Fri, 07 Mar 2025 21:03:19 GMT
ENV TOMCAT_SHA512=55998c7e906a37340f4b56ca66d4a1ef7c0f7a061a9b868e7ed90cce8188f469495ee590d9971eb8d9870dc34ed89b63d6b870a281cb7e84de14a7555fc100e1
# Fri, 07 Mar 2025 21:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 07 Mar 2025 21:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 21:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 07 Mar 2025 21:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 07 Mar 2025 21:03:19 GMT
ENTRYPOINT []
# Fri, 07 Mar 2025 21:03:19 GMT
CMD ["catalina.sh" "run"]
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 31 Mar 2025 16:08:40 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_VERSION=17.2.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.2.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=8c35dae775bbc834e5d747c8b0613016beea6168e96034dd11e29ed88fe6e26e
# Mon, 31 Mar 2025 16:08:40 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Mon, 31 Mar 2025 16:08:40 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
VOLUME [/usr/local/xwiki]
# Mon, 31 Mar 2025 16:08:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 16:08:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21fde7f674e1262f9a291fb3b148dce3986b16a6afe2b1077240af4411e8d`  
		Last Modified: Tue, 04 Feb 2025 04:40:13 GMT  
		Size: 17.0 MB (16962453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e1027cc04acbd0bbe96f77c4b07270e74687784095964c3f8e1145ed4062a0`  
		Last Modified: Tue, 04 Feb 2025 04:40:14 GMT  
		Size: 52.9 MB (52876121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb109d1b0266a0c777373e83c16fd3b583414425ea70ad73adbf43bf4b8a569e`  
		Last Modified: Tue, 04 Feb 2025 04:40:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f09a34126553bccc37644f98b45096297b0127f040e8492684976c77ec2b14a`  
		Last Modified: Tue, 04 Feb 2025 04:40:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d920e1ad43ba60b7e9166dae4c2e0cf4b86e4452193514637b0f106cf8a750`  
		Last Modified: Mon, 10 Mar 2025 22:11:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf57f078e9a35638443bab460c6ac7f1a1f8564b77f5007db180a0e4361ff9f8`  
		Last Modified: Mon, 10 Mar 2025 22:11:15 GMT  
		Size: 13.8 MB (13837934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83078856c2b945e4393f34e46703c6dd3e66c207b0bef041b14d0dacd3a5d80`  
		Last Modified: Mon, 10 Mar 2025 22:11:15 GMT  
		Size: 15.6 MB (15641688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2351cb4bd82cd124f749b7b432c7acdfcd01d4e647b22b7f8bb3dee8527b136f`  
		Last Modified: Mon, 31 Mar 2025 17:31:59 GMT  
		Size: 191.2 MB (191197092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c840d91998609da418483007d1ccb9ddb0ef4ae8861fe541b6e1628793ae5c39`  
		Last Modified: Mon, 31 Mar 2025 17:32:01 GMT  
		Size: 317.3 MB (317308788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f2e7911c1202fdec0d923b07dc86f8d842d718402133ce5b3b59e071a259fb`  
		Last Modified: Mon, 31 Mar 2025 17:31:56 GMT  
		Size: 2.4 MB (2434177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ad18d9f2f6253a799171e90cf13de796b07bb07ec2f681261b0f38c842169c`  
		Last Modified: Mon, 31 Mar 2025 17:31:56 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5021bb16e1bcf09c22a2f30a265cf10f06f26bdbd0003b5fc904c5017671b3`  
		Last Modified: Mon, 31 Mar 2025 17:31:57 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfd8b9e823fd5369980ab002caaff1131d7c0e6538c38ded7e3763fd5530036`  
		Last Modified: Mon, 31 Mar 2025 17:31:57 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7564ac8e85850a1cde0ccf72060547d6a4c411511dcc35964dfd20e6512ad70c`  
		Last Modified: Mon, 31 Mar 2025 17:31:58 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable` - unknown; unknown

```console
$ docker pull xwiki@sha256:77cae59ebb3efbc8be9cf47549098ff77d54c856a20404043497fb57a91e509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8812017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dbc2acca91c1be1e385844aee93fe77edcb6537d73d587205542fb546d604d`

```dockerfile
```

-	Layers:
	-	`sha256:09b5257787b7b269a5b9f7a8adaaa0ae9835e356b5704c6a86073794cde0dffe`  
		Last Modified: Mon, 31 Mar 2025 17:31:56 GMT  
		Size: 8.8 MB (8769861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68360d83083134c7758c5c53427c91bc0570fe1c838ac1555420b2704dcd4eda`  
		Last Modified: Mon, 31 Mar 2025 17:31:56 GMT  
		Size: 42.2 KB (42156 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b2659ef121188577966f43c5d8c0e0ebfe7a1edaa01cd4b5e25ab149b329cde8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.6 MB (635608430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2034d68f223a22121e3662e7e2bd0524cd9f4abb698a2d3cd4e3924c77a3d616`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 07 Mar 2025 21:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 07 Mar 2025 21:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Mar 2025 21:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 07 Mar 2025 21:03:19 GMT
WORKDIR /usr/local/tomcat
# Fri, 07 Mar 2025 21:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 07 Mar 2025 21:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 07 Mar 2025 21:03:19 GMT
ENV TOMCAT_MAJOR=10
# Fri, 07 Mar 2025 21:03:19 GMT
ENV TOMCAT_VERSION=10.1.39
# Fri, 07 Mar 2025 21:03:19 GMT
ENV TOMCAT_SHA512=55998c7e906a37340f4b56ca66d4a1ef7c0f7a061a9b868e7ed90cce8188f469495ee590d9971eb8d9870dc34ed89b63d6b870a281cb7e84de14a7555fc100e1
# Fri, 07 Mar 2025 21:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 07 Mar 2025 21:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 21:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 07 Mar 2025 21:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 07 Mar 2025 21:03:19 GMT
ENTRYPOINT []
# Fri, 07 Mar 2025 21:03:19 GMT
CMD ["catalina.sh" "run"]
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 31 Mar 2025 16:08:40 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 31 Mar 2025 16:08:40 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_VERSION=17.2.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.2.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=8c35dae775bbc834e5d747c8b0613016beea6168e96034dd11e29ed88fe6e26e
# Mon, 31 Mar 2025 16:08:40 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Mon, 31 Mar 2025 16:08:40 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Mon, 31 Mar 2025 16:08:40 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 31 Mar 2025 16:08:40 GMT
VOLUME [/usr/local/xwiki]
# Mon, 31 Mar 2025 16:08:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 16:08:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cbfadccc4ef79b758e18dd8d1708943e6c36b0c9c7e7b94a5d7ff99d3d28af`  
		Last Modified: Tue, 04 Feb 2025 09:25:48 GMT  
		Size: 52.1 MB (52058738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426c44160873d09bb23bdec752f80f9f6f3a7b054d0cd8a334eeb2c92fa0ed9`  
		Last Modified: Tue, 04 Feb 2025 09:25:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3daf2a897e045b94b8cf1d4c94f9dc6f09163273fbbf52afcd8dc60a445788`  
		Last Modified: Tue, 04 Feb 2025 09:25:47 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a764e64196b52daf7bbc53db90ab9c51e680df7eaf1799b3396fa43ea917d1bc`  
		Last Modified: Thu, 06 Mar 2025 19:07:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545aecc6d55dfdd9f0694bdba12ce8b8348d2b7af0439b9382d98ecda2388c8f`  
		Last Modified: Mon, 10 Mar 2025 22:17:08 GMT  
		Size: 13.8 MB (13842724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8513396dc4cad00e35346aacef17991a4feb6cc61ea60e176ac97829203f32a6`  
		Last Modified: Mon, 10 Mar 2025 22:17:08 GMT  
		Size: 15.2 MB (15202210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e30d0f33354547781723bbfd046776fb767ff857425c5f21c0f05f4ed63aa5b`  
		Last Modified: Mon, 31 Mar 2025 18:06:29 GMT  
		Size: 188.9 MB (188875326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb55f7c7771440eb5a7fca1215cd5d3ab608c5c587c0fbb4513fd482caa01e6f`  
		Last Modified: Mon, 31 Mar 2025 18:06:32 GMT  
		Size: 317.3 MB (317308805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba8dd19204d8570f0ba27e54aaaa22af59159decb09931e19058b26514a4f56`  
		Last Modified: Mon, 31 Mar 2025 18:06:25 GMT  
		Size: 2.4 MB (2434166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9fd508f09f4b13d972fdeaa0873119aff2c7427b0697de0e5369f531320fa7`  
		Last Modified: Mon, 31 Mar 2025 18:06:24 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d9f1831a3bd30ad107c4a1386d2503d4452172062b861a1e4060a1549f0881`  
		Last Modified: Mon, 31 Mar 2025 18:06:25 GMT  
		Size: 2.4 KB (2365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433fc810a08b85bee4028dcd78d2cad27a8e46d6b7eb2d631fac02452998d95e`  
		Last Modified: Mon, 31 Mar 2025 18:06:26 GMT  
		Size: 6.6 KB (6603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739b4246cc7ff5d8e66bb196cdce8fe60667408fe244a150c763da8a67783f01`  
		Last Modified: Mon, 31 Mar 2025 18:06:27 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable` - unknown; unknown

```console
$ docker pull xwiki@sha256:6d8cbbd82bc8ec910e3e1785a47c98aa2e067cb960e377917b142996b4a36eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8813063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97f747ad9e74be5157fcaa5132d28ad69efc58708efe5bb35ad1eeffde80c7`

```dockerfile
```

-	Layers:
	-	`sha256:0fd2bd97a716a708d4492c99f60aa4584727107af930578737882c627cf43d5a`  
		Last Modified: Mon, 31 Mar 2025 18:06:25 GMT  
		Size: 8.8 MB (8770674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8693c754587a19d165040510e23f9a804631f7449edaf5d6800259e14608467`  
		Last Modified: Mon, 31 Mar 2025 18:06:24 GMT  
		Size: 42.4 KB (42389 bytes)  
		MIME: application/vnd.in-toto+json
