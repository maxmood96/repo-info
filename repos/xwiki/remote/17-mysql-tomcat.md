## `xwiki:17-mysql-tomcat`

```console
$ docker pull xwiki@sha256:3cd747985634a0720b460abc1556a73e7dab6ba8e9586fa88c16c954f5123903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:c548db8c28a1345634c10316f0fe8315d12fee21c928973be3101219fef14a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 MB (636233638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f803271ca735636042cf2989289e738f6f8cede7ef552bc9f2b2f044428877f4`
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
# Tue, 28 Jan 2025 17:13:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 17:13:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:13:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 17:13:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2025 17:13:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:13:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 17:13:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_MAJOR=10
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_VERSION=10.1.35
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_SHA512=814500908e139fd984bbacf10ccf8ad400d129ce23a7ba47b771f0ca308b148e23a58c83eb924653f62ca2a0696c87fc6128c7a81def18b04c2f0c01f08009b9
# Tue, 28 Jan 2025 17:13:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT []
# Tue, 28 Jan 2025 17:13:32 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jan 2025 17:13:32 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_VERSION=17.0.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.0.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd4d25b42c5645d87f7ed242967161ccb2648688948de93649a5ca11a1845c34
# Tue, 28 Jan 2025 17:13:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 17:13:32 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 17:13:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21fde7f674e1262f9a291fb3b148dce3986b16a6afe2b1077240af4411e8d`  
		Last Modified: Tue, 04 Feb 2025 07:16:41 GMT  
		Size: 17.0 MB (16962453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e1027cc04acbd0bbe96f77c4b07270e74687784095964c3f8e1145ed4062a0`  
		Last Modified: Tue, 04 Feb 2025 07:28:42 GMT  
		Size: 52.9 MB (52876121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb109d1b0266a0c777373e83c16fd3b583414425ea70ad73adbf43bf4b8a569e`  
		Last Modified: Tue, 04 Feb 2025 07:20:28 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f09a34126553bccc37644f98b45096297b0127f040e8492684976c77ec2b14a`  
		Last Modified: Tue, 04 Feb 2025 07:24:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8eb193441d50e58a6bfecfde06924ddce7695116b316d7b36f55d8ce0e7930b`  
		Last Modified: Tue, 11 Feb 2025 04:20:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a9912a296475b5fb1b484823166adb6a72a6466c4e86ec1f04ac5cc4790ea7`  
		Last Modified: Tue, 11 Feb 2025 04:20:06 GMT  
		Size: 13.8 MB (13825646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99ff0fa96ba41035bd78f2fab2c0e1b8fc42c581033dd1d8f54cae9680a2629`  
		Last Modified: Tue, 11 Feb 2025 04:09:29 GMT  
		Size: 12.8 MB (12832469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d64e886b51c9be6c69e1e83c3c8ae79fc8a6baa77d307e9b4819b3b2e1f8dd`  
		Last Modified: Tue, 11 Feb 2025 04:22:30 GMT  
		Size: 191.2 MB (191196422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b710e97e128e01ffc35ffd308ffce02be4f03c61f14b02f3d9e69f1b0c817475`  
		Last Modified: Tue, 11 Feb 2025 04:22:25 GMT  
		Size: 316.3 MB (316336616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0344fbbb951948f2c8643a061700b36b7c995e3b657b3f6c45429b622a11abb`  
		Last Modified: Tue, 11 Feb 2025 04:22:09 GMT  
		Size: 2.4 MB (2434174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d057190dd7966f4e8a6fd241efb720d3dfe12e3b4d5e54bd2a3c1dfd34595c`  
		Last Modified: Tue, 11 Feb 2025 04:22:11 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b66a4af7e2720b3cbb831d3922f8015e4658cf932f9956fcec8b26fd91eec01`  
		Last Modified: Tue, 11 Feb 2025 05:12:20 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79facaf3585ad42447e88a989795e8782c398864786528fa3e0f18a81384222`  
		Last Modified: Tue, 11 Feb 2025 04:22:15 GMT  
		Size: 6.6 KB (6582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c188dbe7b5fa48d9fa61a312c41179cd8a34ec6bcfaa99767040b88154856497`  
		Last Modified: Tue, 11 Feb 2025 04:22:16 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:7eb2c8881c8e6f9a97f42736d122d2b867053e1accd1ae36ea2b7c89c0c98953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8809194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3346ac5fec40f32e9b5b91df01718c3fcd8619d285859d68e68bd2375ebd10`

```dockerfile
```

-	Layers:
	-	`sha256:455d3a3a99da3d957c20ab82e814a388b297ca557ad744c11683c501fb5913cf`  
		Last Modified: Mon, 17 Feb 2025 02:16:10 GMT  
		Size: 8.8 MB (8767038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3241e70effb39199f80ff87d925ce149f9d7e2d05ff38a61597ce9494c505ff7`  
		Last Modified: Mon, 17 Feb 2025 02:16:09 GMT  
		Size: 42.2 KB (42156 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b7097fcf61889e4d6baad4246b531166c8ec6479522ae117a3ab16ea0f950820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.0 MB (632013432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5e85269b127c39b042d68c26d9b255c4e14a4162848866059bd570cf310e48`
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
# Tue, 28 Jan 2025 17:13:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 17:13:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:13:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 17:13:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2025 17:13:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:13:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 17:13:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_MAJOR=10
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_VERSION=10.1.35
# Tue, 28 Jan 2025 17:13:32 GMT
ENV TOMCAT_SHA512=814500908e139fd984bbacf10ccf8ad400d129ce23a7ba47b771f0ca308b148e23a58c83eb924653f62ca2a0696c87fc6128c7a81def18b04c2f0c01f08009b9
# Tue, 28 Jan 2025 17:13:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT []
# Tue, 28 Jan 2025 17:13:32 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jan 2025 17:13:32 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jan 2025 17:13:32 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_VERSION=17.0.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.0.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd4d25b42c5645d87f7ed242967161ccb2648688948de93649a5ca11a1845c34
# Tue, 28 Jan 2025 17:13:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 17:13:32 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 17:13:32 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Jan 2025 17:13:32 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Jan 2025 17:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 17:13:32 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 10:15:57 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cbfadccc4ef79b758e18dd8d1708943e6c36b0c9c7e7b94a5d7ff99d3d28af`  
		Last Modified: Tue, 04 Feb 2025 14:22:53 GMT  
		Size: 52.1 MB (52058738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426c44160873d09bb23bdec752f80f9f6f3a7b054d0cd8a334eeb2c92fa0ed9`  
		Last Modified: Tue, 04 Feb 2025 10:53:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3daf2a897e045b94b8cf1d4c94f9dc6f09163273fbbf52afcd8dc60a445788`  
		Last Modified: Tue, 04 Feb 2025 13:37:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ee034a146c65a6d1fdfbfcc76a4dea8b9a3fc21563811d2cd9443e32f75a3`  
		Last Modified: Wed, 05 Feb 2025 06:42:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7936391fabda047f45aa865401f449a834d8661f5eb44b5cb66235178a07398`  
		Last Modified: Tue, 11 Feb 2025 04:40:36 GMT  
		Size: 13.8 MB (13828040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28d997418bf21d3f396d7b1f546c77d8695c3f4b47d9a082503e448bb6f69c`  
		Last Modified: Tue, 11 Feb 2025 04:40:37 GMT  
		Size: 12.6 MB (12601442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6844170bbc4940788ec69b2c2d202a1f940e2599c2b87ac0573c7db8030f8`  
		Last Modified: Tue, 11 Feb 2025 09:01:43 GMT  
		Size: 188.9 MB (188867888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2060cfa272957c4b9817020e1293bffb4d2919f4b5c23f6e7c2751c26666b3e8`  
		Last Modified: Tue, 11 Feb 2025 09:01:55 GMT  
		Size: 316.3 MB (316336713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817ced4d115637fc15a0d85800ef7e0d26de0b28eae0fd8799fd539dd8376625`  
		Last Modified: Tue, 11 Feb 2025 07:27:00 GMT  
		Size: 2.4 MB (2434174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b012f1d249128868e174a5903e2796916aefd4b79a477a0ba9c029f4946d`  
		Last Modified: Tue, 11 Feb 2025 07:27:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a25d550b597334cc16778fa1f8bc6ce29ba31cd4d7f846175faadd855fadd99`  
		Last Modified: Tue, 11 Feb 2025 07:27:07 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d7373673d420052b85b81e1c189838c668d3d5fa14f1d1e8c089cd6c3274a4`  
		Last Modified: Tue, 11 Feb 2025 07:27:14 GMT  
		Size: 6.6 KB (6580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9abbe4d8b60853f8a3b0e4cfc77adb1ef945f28840ced288514ce44f9d36fe`  
		Last Modified: Tue, 11 Feb 2025 09:02:21 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:9464e4862ddc9b8562e46ddb203cc70f601061d53347d469f9009dd4eb4b26b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf0b01e8ac997a8bd09531fc0e0b7c06734e9bdd4088655ee82a8765271a4ed`

```dockerfile
```

-	Layers:
	-	`sha256:b7cc4270a66231326ad7f29d920fe5b725cb0840589bfcaa1317b8a0004f92e9`  
		Last Modified: Fri, 14 Feb 2025 10:30:07 GMT  
		Size: 8.8 MB (8767851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf5332264da08a26fb6e0235ee87c4ab9e943cb53017926660b5ab359c2c284`  
		Last Modified: Fri, 14 Feb 2025 10:30:09 GMT  
		Size: 42.4 KB (42389 bytes)  
		MIME: application/vnd.in-toto+json
