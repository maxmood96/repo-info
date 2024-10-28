## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:ba53625415ce3d6593c2d86bd58b896b44f02170ada5606a1a2c98d30b51f4c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:7454110b207951b65e3122e60362ff4fa198c9d91e21faa35b611122ee0d601d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612200196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7453d0e7acaf0724f3d41d3e632684540d9acf4d1a30726f94c92ab46feec424`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Oct 2024 15:53:54 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_VERSION=16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a66ce45c49863c0e8cbdae0fb5e5dfab317a1c0c3a45e7c33fb61b09b39fe23
# Mon, 28 Oct 2024 15:53:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_VERSION=3.4.1
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_SHA256=f60e4b282f1f4bdb74f0a26436ba7078a5e480b6f6702f6a7b45d9ba5e604a24
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.1
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.1.jar
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.1.jar
# Mon, 28 Oct 2024 15:53:54 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Oct 2024 15:53:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 15:53:54 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4db91116a643f1af6f310b6dfdd6bb6fa9f5a4e5579bc5cdf2ae45c06a7650`  
		Last Modified: Thu, 24 Oct 2024 00:57:09 GMT  
		Size: 17.0 MB (16965851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b16bdaa6a5730f4ec6136b774473dd0b2b687cce3c95f8bc354146474452c`  
		Last Modified: Thu, 24 Oct 2024 00:57:10 GMT  
		Size: 46.9 MB (46941786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3455e586bc9e48010a24a531cb0e35c3363f3605b0ead2e41dff0ca83ace0`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8021e383cc85d1eb186a772b8cbcb0e8278d701580b9eaa081bfd9064af3e64`  
		Last Modified: Thu, 24 Oct 2024 00:57:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee55d0bb1c8869afe9b9d97e530cbcaff3b222149eda66faf123396737a7d53`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b748649db8eb18ca6f22b4e6f45e2418cf840e7b312ec6cee8b81966160d6b`  
		Last Modified: Thu, 24 Oct 2024 02:54:24 GMT  
		Size: 13.4 MB (13374098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9801e0bd5e0f6c538c825c4a336de90e1eaa721823d4854bd300d486fb217afe`  
		Last Modified: Thu, 24 Oct 2024 02:54:23 GMT  
		Size: 223.1 KB (223070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4049fbdf4db46778813338344d9cc37107597c2f40d48e76c7e3479ec81b7fe7`  
		Last Modified: Mon, 28 Oct 2024 18:00:28 GMT  
		Size: 192.3 MB (192263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08790dfe1742dfda9aa6f71fd23fc642475ed1d172e89e5b63dc81148ea662de`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 312.0 MB (312017832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dca83ab60ea66dc72d5c19a7ac7d2ef773a8bff1ad8fa947941efb7f285b133`  
		Last Modified: Mon, 28 Oct 2024 18:00:26 GMT  
		Size: 648.5 KB (648526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c0d2890aaaf469a128de4dd42b20f701b16d0460978472ac382bdc8133e819`  
		Last Modified: Mon, 28 Oct 2024 18:00:26 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c2bc1e883febfe8ba3f29694977c9f7d47a4921c71c4f989687481a23ecaf6`  
		Last Modified: Mon, 28 Oct 2024 18:00:27 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fe44d8aced820c5b9da8a6aac3956ddff7175076d34e97e6d7fd41d7b7a4de`  
		Last Modified: Mon, 28 Oct 2024 18:00:27 GMT  
		Size: 6.6 KB (6589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440bbe963d90c7331d9d0e385820f8809683fd9a0a86cc48c076cb6d37543fe0`  
		Last Modified: Mon, 28 Oct 2024 18:00:27 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:e33efbdec64213ab8681c27f015d30fa7e4eecb9c16d7206bcbc8314f1f30b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03224780ad4ce5edaa6108cf833dbb394c53c2c524e77910a7869189126690a6`

```dockerfile
```

-	Layers:
	-	`sha256:7264ff29429fa7dcd3eefa569aa4afab9c91b43ff09198b0ef822e768ccb3c77`  
		Last Modified: Mon, 28 Oct 2024 18:00:26 GMT  
		Size: 8.8 MB (8788284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1af71242cbaf780193a0a6909f47e2595465cc30e58a25d2b3d877bb7c5ef6`  
		Last Modified: Mon, 28 Oct 2024 18:00:26 GMT  
		Size: 41.3 KB (41336 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:541454f4f67fbe1c68cf7bfa4b36caa9dc308b5a6b38f07d8f38f5d4c1e4412e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.4 MB (608444089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0f899022d58e63d663ce71d285afb81e02ec9f30de4a646b92cd18303e37d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Oct 2024 15:53:54 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_VERSION=16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a66ce45c49863c0e8cbdae0fb5e5dfab317a1c0c3a45e7c33fb61b09b39fe23
# Mon, 28 Oct 2024 15:53:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_VERSION=3.4.1
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_SHA256=f60e4b282f1f4bdb74f0a26436ba7078a5e480b6f6702f6a7b45d9ba5e604a24
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.1
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.1.jar
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.1.jar
# Mon, 28 Oct 2024 15:53:54 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Oct 2024 15:53:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 15:53:54 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e2f7d4d887134d9aff4c6177e18f66336c5f3549bb3d16b0c27622e2b8b22c`  
		Last Modified: Thu, 24 Oct 2024 00:59:40 GMT  
		Size: 17.0 MB (16980397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4547cef613196c0e0f0eddc0c27bfdebd8ba87747901b9fc1fba83828f192b`  
		Last Modified: Thu, 24 Oct 2024 01:13:00 GMT  
		Size: 46.4 MB (46430942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f238f5bd3f6d19b6557a168cdf2216e1c7345f3d9f47f07beb086bf56b80642`  
		Last Modified: Thu, 24 Oct 2024 01:12:58 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc825c390428c52f01639df85bf823ec19660a17b84dff8b0e3a5a25f510ece0`  
		Last Modified: Thu, 24 Oct 2024 01:12:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2163de3883d1b73af731c56b7ccd6ea979d721db6527705908bb06b05bbf6a7`  
		Last Modified: Thu, 24 Oct 2024 12:35:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6f3c5a8eec1b034ff73efefd0a115cdab18cf8e9c1f53bb8c8610151874ed1`  
		Last Modified: Thu, 24 Oct 2024 12:40:57 GMT  
		Size: 13.4 MB (13386564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef23abe225803bcf3217349c97b5019b337a56c684c7a9fb66869d42d45c8b0`  
		Last Modified: Thu, 24 Oct 2024 12:40:57 GMT  
		Size: 223.6 KB (223588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944602abdd9c0e104517f03d57c9fcecf731db0c989d3d90e883a709c7a86634`  
		Last Modified: Thu, 24 Oct 2024 14:36:48 GMT  
		Size: 189.9 MB (189854981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5403e82d0268a09ecebfd40a83d5a1df69f21fecb634a7ee375db4eac7bc5d9`  
		Last Modified: Mon, 28 Oct 2024 18:04:06 GMT  
		Size: 312.0 MB (312017883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef14e998e0748a1615ffd0e7e6ab6cac1b42a128893631f0eebe9f472a69547`  
		Last Modified: Mon, 28 Oct 2024 18:09:47 GMT  
		Size: 648.5 KB (648527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b3d2bad302489fe0aa2969a0644f3fd168ce2e0813e8cdef51fd8d1efabfd6`  
		Last Modified: Mon, 28 Oct 2024 18:09:47 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46e8e0f06fd59bf27a916838baff734b4ef181315b771b63cdbde890c84c079`  
		Last Modified: Mon, 28 Oct 2024 18:09:47 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7b449a7b17c80c32a3f3577055a5019b904bc78646953386bec94be0150651`  
		Last Modified: Mon, 28 Oct 2024 18:09:47 GMT  
		Size: 6.6 KB (6594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d39a7a35c7eae97a6949b2a237942a0d85e909ff2854a612e3eab9d0493eca7`  
		Last Modified: Mon, 28 Oct 2024 18:09:48 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:bd4546df353538c6aa9589a59b6665765686172c2cf12a00d5f0841858130de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf40ac0a8a19461e13f6cf6d9f8b712bec77db26543367af44d44e1faded9a3b`

```dockerfile
```

-	Layers:
	-	`sha256:dd2e54053d11ba15ebe4de33363d83284793264987c7d8a00ebd5ce06c7ee097`  
		Last Modified: Mon, 28 Oct 2024 18:09:47 GMT  
		Size: 8.8 MB (8789036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b58abda15681122333d8b215dace40e981aaa4f6010a34afefc1b918d8465d2`  
		Last Modified: Mon, 28 Oct 2024 18:09:47 GMT  
		Size: 41.5 KB (41509 bytes)  
		MIME: application/vnd.in-toto+json
