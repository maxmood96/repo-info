## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:5833c25ea94c9feab5ff48bd81d2ea8eff9c351fd4d6767ac51947b6890a7313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:995e045411d6d607fd30ade506b6a890a65a87059b8483a2dc0e2fe7cd1d5809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612388707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7979c7ddf1cb05143b5a31d7f03b79ad00f24eefca4e700c946ca9ec76aff6d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 01 Oct 2024 13:05:18 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:05:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:05:18 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Tue, 01 Oct 2024 13:05:18 GMT
CMD ["/bin/bash"]
# Tue, 01 Oct 2024 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Oct 2024 13:05:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:05:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:05:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 01 Oct 2024 13:05:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:05:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 01 Oct 2024 13:05:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 01 Oct 2024 13:05:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 01 Oct 2024 13:05:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT []
# Tue, 01 Oct 2024 13:05:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 01 Oct 2024 13:05:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_VERSION=16.8.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.8.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=7eca55bbe56a45f34b81e9884bb4f190af24306db3da9032c27126d3cf11f4f1
# Tue, 01 Oct 2024 13:05:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Tue, 01 Oct 2024 13:05:18 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 13:05:18 GMT
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
	-	`sha256:07fb95567b88fc7a1c11dc880a4d27cd2ed13e49d8559e56f49f27f41f35ea82`  
		Last Modified: Thu, 24 Oct 2024 03:53:39 GMT  
		Size: 192.3 MB (192263682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269e5438ff11645e17f59c768a46f8442f098269111b130ead406e788fff5710`  
		Last Modified: Thu, 24 Oct 2024 03:53:40 GMT  
		Size: 311.8 MB (311840791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455c2e0fc3b9d3e3fad5008c475195d6f12d30ddf8c678e67e44460d2c0878ed`  
		Last Modified: Thu, 24 Oct 2024 03:53:36 GMT  
		Size: 1.0 MB (1013642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ca5658583390503927f9519f8afe67f88905aa3d4d28a9da8254fc1fbd85eb`  
		Last Modified: Thu, 24 Oct 2024 03:53:35 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd18559097c988fb9bc4dceb447366fcfdfe130bbf1e5d2f21c77bdf7d866dd`  
		Last Modified: Thu, 24 Oct 2024 03:53:35 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373f19275d720349d3fd172ee86101c942d1529661c43fdf44db5408378bf4fc`  
		Last Modified: Thu, 24 Oct 2024 03:53:37 GMT  
		Size: 6.6 KB (6564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f864404aeb958681153de158cf3b9b415de77994ad25b8bb8cb76461bc1cc3b0`  
		Last Modified: Thu, 24 Oct 2024 03:53:37 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b103a040e5fa69f8f35e85fe5b1e7ab9f8bd4c2b8f31ba697603c28261eb6f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3e064233f3f1375f85c705cd15fa8857ba495007a3cc19ffdcffa6c5a748ae`

```dockerfile
```

-	Layers:
	-	`sha256:c4a2e05c6735b01ef0da9859ef5734334baf0b28b4f2173c22df8e6ebdda1a07`  
		Last Modified: Thu, 24 Oct 2024 03:53:36 GMT  
		Size: 8.8 MB (8788247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28076f15571879d3c033e363c16435300d121a3535b45bbae4ffe0a8e931a95b`  
		Last Modified: Thu, 24 Oct 2024 03:53:36 GMT  
		Size: 41.3 KB (41313 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:1f9e8974bcaf6fdfb906465b4ac715313f5417a6f9a7e6ee89fb053e5632fe25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.6 MB (608632112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5700a0f41c6330bafbcc8def34eb5c6604d7fd12fd03cf23a18913f217d7fc6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 01 Oct 2024 13:05:18 GMT
ARG RELEASE
# Tue, 01 Oct 2024 13:05:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Oct 2024 13:05:18 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Tue, 01 Oct 2024 13:05:18 GMT
CMD ["/bin/bash"]
# Tue, 01 Oct 2024 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Oct 2024 13:05:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:05:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 01 Oct 2024 13:05:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 01 Oct 2024 13:05:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 13:05:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 01 Oct 2024 13:05:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 01 Oct 2024 13:05:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 01 Oct 2024 13:05:18 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 01 Oct 2024 13:05:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT []
# Tue, 01 Oct 2024 13:05:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 01 Oct 2024 13:05:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 01 Oct 2024 13:05:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_VERSION=16.8.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.8.0
# Tue, 01 Oct 2024 13:05:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=7eca55bbe56a45f34b81e9884bb4f190af24306db3da9032c27126d3cf11f4f1
# Tue, 01 Oct 2024 13:05:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Tue, 01 Oct 2024 13:05:18 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Tue, 01 Oct 2024 13:05:18 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 01 Oct 2024 13:05:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 01 Oct 2024 13:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 13:05:18 GMT
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
	-	`sha256:71ba3c8e4eb98e1433300b83b352594fce4c9ec4cc6647cf317cc5072068b4e8`  
		Last Modified: Thu, 24 Oct 2024 14:36:50 GMT  
		Size: 311.8 MB (311840731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e61abd58d38fa041e857cd3e1bb7cde1ff103dacd495c537bd1a20297607d22`  
		Last Modified: Thu, 24 Oct 2024 14:39:40 GMT  
		Size: 1.0 MB (1013644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e84b78b1d81bd5fbf7e2dba0dd70d717cd30ad5c71835ed40db44f51ba14af`  
		Last Modified: Thu, 24 Oct 2024 14:39:40 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c680a922035bf258e5490d5ac94f35f3cc7b63a3e9633a1e897206e2334a9727`  
		Last Modified: Thu, 24 Oct 2024 14:39:40 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fbc5dc04328f351a2bc150b7aa8a65ee79eda18f4892dbd6e3bd8814464771`  
		Last Modified: Thu, 24 Oct 2024 14:39:40 GMT  
		Size: 6.6 KB (6563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013e4f394a3dae01d1c9dd328fc52706ef25b768388a131df0fedf28b5097ccf`  
		Last Modified: Thu, 24 Oct 2024 14:39:41 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:fd9dcc9b92a59d0278bcf5e9debd3478877026cb50d5cb566e27bda3502bd20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ff32bf9ede8d888fbc3837730f9284e2664884c14b6bd6f8ef05760973e885`

```dockerfile
```

-	Layers:
	-	`sha256:17c41f2b81dfa2a630ec6a0a3c50e6178e906ea108cbd0be5e5f818625055085`  
		Last Modified: Thu, 24 Oct 2024 14:39:40 GMT  
		Size: 8.8 MB (8788999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2293835ae4dbe4e7f4cd2c41c4052b0adb1cb319e60399c7a781b1a0d233adb`  
		Last Modified: Thu, 24 Oct 2024 14:39:40 GMT  
		Size: 41.5 KB (41486 bytes)  
		MIME: application/vnd.in-toto+json
