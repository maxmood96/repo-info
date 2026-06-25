## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:1f6412172a4f8b9faf2ff36cba4904bad55d72ffa0c34103a7416e5ab66ae680
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:68326904b12be264ca3cb3b60951c236a0f746748c076399ac313c6938907108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.4 MB (641383120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b25345858f9634a03d92a6f9cbf54d7af025bcb0529fe43928d273275fb6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:14:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 02:13:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jun 2026 02:13:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 02:13:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 25 Jun 2026 02:13:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:13:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_MAJOR=10
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_VERSION=10.1.56
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_SHA512=8fae99273615eb9d7fbe7ed80abda0ca27647a80f6fcfda98459c5b412d5ef555740b4c4d4af5afae2eb150f1f5bede21ab007ab8cc1f407f508d8908a81b7cc
# Thu, 25 Jun 2026 02:13:22 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 25 Jun 2026 02:13:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 02:13:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 25 Jun 2026 02:13:26 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 25 Jun 2026 02:13:26 GMT
ENTRYPOINT []
# Thu, 25 Jun 2026 02:13:26 GMT
CMD ["catalina.sh" "run"]
# Thu, 25 Jun 2026 04:12:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 25 Jun 2026 04:12:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:12:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:12:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 25 Jun 2026 04:12:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 25 Jun 2026 04:12:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 25 Jun 2026 04:12:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 04:12:26 GMT
ENV XWIKI_VERSION=17.10.9
# Thu, 25 Jun 2026 04:12:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.9
# Thu, 25 Jun 2026 04:12:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=b786a85a043cc673e26d887fd0ef34d2fda2f4a9ef4a362360814868ccf41e1f
# Thu, 25 Jun 2026 04:12:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 25 Jun 2026 04:12:49 GMT
ENV POSTGRES_JDBC_VERSION=42.7.11
# Thu, 25 Jun 2026 04:12:49 GMT
ENV POSTGRES_JDBC_SHA256=1981b31d3993c58702783c1cddf10a34e48c1f413d70ff1cb6def0a143484647
# Thu, 25 Jun 2026 04:12:49 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.11
# Thu, 25 Jun 2026 04:12:49 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.11.jar
# Thu, 25 Jun 2026 04:12:49 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.11.jar
# Thu, 25 Jun 2026 04:12:49 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 25 Jun 2026 04:12:49 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 25 Jun 2026 04:12:49 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 25 Jun 2026 04:12:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 25 Jun 2026 04:12:49 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 04:12:49 GMT
VOLUME [/usr/local/xwiki]
# Thu, 25 Jun 2026 04:12:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 04:12:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9e436cd644d0619bdfd1c8d1dce9e824e836e6102bf4a4c26919785ffe2a7c`  
		Last Modified: Tue, 02 Jun 2026 08:14:35 GMT  
		Size: 17.0 MB (16984112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87482ed64d79af651c4c12177abc09ecb3e56b9d8d0f50a562d2f590d06f86d4`  
		Last Modified: Tue, 02 Jun 2026 08:15:02 GMT  
		Size: 53.1 MB (53123212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc789882cf0d5dbeb8bc4705a9265f34e7a07d131d29a28ab214e03c5848204d`  
		Last Modified: Tue, 02 Jun 2026 08:15:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61623c08676d47596865bd7b800628bf28592b0b9ffaedb68600f7ce6243b27`  
		Last Modified: Tue, 02 Jun 2026 08:15:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0511e9999bcd27a02849550499c434bf5a04b85d448b6edea21a693ec20faffc`  
		Last Modified: Thu, 25 Jun 2026 02:13:35 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aff57e488da9dbb54d8c18a5b7a7c3afd121063fb34d981a71843516dfee90`  
		Last Modified: Thu, 25 Jun 2026 02:13:35 GMT  
		Size: 14.3 MB (14349294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50ded7df386c999094d43699b85d64540a1b6a56d8dfefc2192ae52a7b99192`  
		Last Modified: Thu, 25 Jun 2026 02:13:35 GMT  
		Size: 3.0 MB (3030334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc370f219e0066f02084d6afdafd6405fdd24e17418a09c41ca8f50cb12e5f8`  
		Last Modified: Thu, 25 Jun 2026 04:13:34 GMT  
		Size: 191.2 MB (191223082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7a6fa594bec9238dcffa0e0d2c6eb1aff099860e9af928f738bcf8be4e2837`  
		Last Modified: Thu, 25 Jun 2026 04:13:38 GMT  
		Size: 331.9 MB (331853481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0f114add82cd921e841d3d028df6b6da10d1118c73bd8146c5d91e3f4875cc`  
		Last Modified: Thu, 25 Jun 2026 04:13:26 GMT  
		Size: 1.1 MB (1067144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e100dc3f2e6ba253c421d008cbe11155f6f7e7fb9664fb7bb669b70c39fa39`  
		Last Modified: Thu, 25 Jun 2026 04:13:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab7490e2bb972859de1a40b5cb1960ee9fafd691398e97e5e0ccd2168ef5b06`  
		Last Modified: Thu, 25 Jun 2026 04:13:27 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadf5c1e873ac6bad4f2ff5c19b74cb170f2d1e031d48304c3d5271186ba6b9a`  
		Last Modified: Thu, 25 Jun 2026 04:13:27 GMT  
		Size: 10.8 KB (10763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a95742f40b78ae8e61c56a629c7fe6f8f00994695acab2587034d4c1cfeb311`  
		Last Modified: Thu, 25 Jun 2026 04:13:28 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:e91351e88937550f5d6a5c1329c47b65342639d817a6fd4a0ca766edf15dd4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1f29fcca76076ecbe8201cc2f453468ead58c5580469d457cc9aa746cf2976`

```dockerfile
```

-	Layers:
	-	`sha256:8615d7b7a58a2fbd1dd6af988c974c251b7fe576c199eca8ab6079a08f8550db`  
		Last Modified: Thu, 25 Jun 2026 04:13:26 GMT  
		Size: 9.2 MB (9183164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d893a32f5459dbf6028d97686abcd9b40ca4fa0f97ef7615afb6ee6fb1a1503`  
		Last Modified: Thu, 25 Jun 2026 04:13:25 GMT  
		Size: 40.4 KB (40448 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:3526805200155a2056b571c3651c95e1c9f6c532c60a085e1d001012ad882aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.2 MB (637187878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0876a2ce8434069633e289a8f9607728856df0173d2b0144d23769c645b0b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:15 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:16:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 02:12:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jun 2026 02:12:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 02:12:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 25 Jun 2026 02:12:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:12:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_MAJOR=10
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_VERSION=10.1.56
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_SHA512=8fae99273615eb9d7fbe7ed80abda0ca27647a80f6fcfda98459c5b412d5ef555740b4c4d4af5afae2eb150f1f5bede21ab007ab8cc1f407f508d8908a81b7cc
# Thu, 25 Jun 2026 02:12:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 25 Jun 2026 02:12:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 02:12:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 25 Jun 2026 02:12:54 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 25 Jun 2026 02:12:54 GMT
ENTRYPOINT []
# Thu, 25 Jun 2026 02:12:54 GMT
CMD ["catalina.sh" "run"]
# Thu, 25 Jun 2026 04:11:48 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 25 Jun 2026 04:11:48 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:11:48 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:11:48 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 25 Jun 2026 04:11:48 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 25 Jun 2026 04:11:48 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 25 Jun 2026 04:11:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 04:11:48 GMT
ENV XWIKI_VERSION=17.10.9
# Thu, 25 Jun 2026 04:11:48 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.9
# Thu, 25 Jun 2026 04:11:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=b786a85a043cc673e26d887fd0ef34d2fda2f4a9ef4a362360814868ccf41e1f
# Thu, 25 Jun 2026 04:12:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 25 Jun 2026 04:12:13 GMT
ENV POSTGRES_JDBC_VERSION=42.7.11
# Thu, 25 Jun 2026 04:12:13 GMT
ENV POSTGRES_JDBC_SHA256=1981b31d3993c58702783c1cddf10a34e48c1f413d70ff1cb6def0a143484647
# Thu, 25 Jun 2026 04:12:13 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.11
# Thu, 25 Jun 2026 04:12:13 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.11.jar
# Thu, 25 Jun 2026 04:12:13 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.11.jar
# Thu, 25 Jun 2026 04:12:13 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 25 Jun 2026 04:12:13 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 25 Jun 2026 04:12:13 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 25 Jun 2026 04:12:13 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 25 Jun 2026 04:12:13 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 04:12:13 GMT
VOLUME [/usr/local/xwiki]
# Thu, 25 Jun 2026 04:12:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 04:12:13 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c56d3b03f3eed5e9e98720fc008e29f5ad7edffbb3d0095a9751486b593905e`  
		Last Modified: Tue, 02 Jun 2026 08:16:32 GMT  
		Size: 17.0 MB (16997505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87a7c029e17f2ca0e18faf162ffda9b94bff8a6c53017932eea8e9d7c8d257`  
		Last Modified: Tue, 02 Jun 2026 08:16:33 GMT  
		Size: 52.3 MB (52314907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a42fa743e77cd7a6e3837c86c2a0c4d959a29959bad6ce7730b2a3c45b1c838`  
		Last Modified: Tue, 02 Jun 2026 08:16:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229c6fba250cd9ec9dea9d2580e679f6a3e697d45386c7d8e63d493bf8134fa`  
		Last Modified: Tue, 02 Jun 2026 08:16:31 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384e21c77bf8435eca6b03f134c29c283a4cc58758713f928a217ee1029073e0`  
		Last Modified: Thu, 25 Jun 2026 02:13:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17306b9dbf994913c9c2774b349038212546a1558f34aaf094bc26b9f2b59037`  
		Last Modified: Thu, 25 Jun 2026 02:13:03 GMT  
		Size: 14.4 MB (14352031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461465510cdd039be85c0c637eae3a3d19183c82d849f758283f1b15090458cc`  
		Last Modified: Thu, 25 Jun 2026 02:13:02 GMT  
		Size: 2.8 MB (2829997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dba58c355f6ac88e5eeb9ecffe0d1885cc3ff87a363548cbdc837101c7ce0`  
		Last Modified: Thu, 25 Jun 2026 04:12:53 GMT  
		Size: 188.9 MB (188876786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d021f36b20ac40135efec66b66f359fabcfb5e60bfdc35c3ddf379bdcceebf15`  
		Last Modified: Thu, 25 Jun 2026 04:12:55 GMT  
		Size: 331.9 MB (331853455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089e528099a2893a28c4359fb9cf876934c55e0a14f0c56a574c1fd8b670118d`  
		Last Modified: Thu, 25 Jun 2026 04:12:46 GMT  
		Size: 1.1 MB (1067144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392bb89ecabc111557bf33e45adfb0005742e0683e3b88715d25269be8c3a90f`  
		Last Modified: Thu, 25 Jun 2026 04:12:46 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3a307c1d83b65a8d49da3b69f1e5384157c2e7616dd2a4181061cc299416cf`  
		Last Modified: Thu, 25 Jun 2026 04:12:47 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3134bda9d061a07b9277b57f2289b40188b4e18f2c4b69b4069acba919d3471`  
		Last Modified: Thu, 25 Jun 2026 04:12:47 GMT  
		Size: 10.8 KB (10760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21188c0f3e2ed13211c2098c0626e6877738597c8919bea7b57f2b4781d767ef`  
		Last Modified: Thu, 25 Jun 2026 04:12:49 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:4bff8edd89551894fb180611af5031c27efb3f8ba999b7c6a6eff79aed9a716c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9224515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6cbee1269c96cde58a7c537e1335e2d4452032d427c50363ad7674783bffbe`

```dockerfile
```

-	Layers:
	-	`sha256:2cf227acf6c586af885cdf5f24b842e903be2df158d0622043fb274b4a4e71ac`  
		Last Modified: Thu, 25 Jun 2026 04:12:46 GMT  
		Size: 9.2 MB (9183905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f5745a1d1de0870446f39f647e2bb22ee136dc20327eb86ae6623b227a6782`  
		Last Modified: Thu, 25 Jun 2026 04:12:46 GMT  
		Size: 40.6 KB (40610 bytes)  
		MIME: application/vnd.in-toto+json
