## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:f33bacf02b5e14b4bf4bd6a91ee141440066196a8d452070551f743d4f01907f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ccd105e8c1ae8a0a259f5360bc14f4bc21a8d6461c333b8c3a19071df2d50e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.6 MB (607594652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db453611a4949b476871e83671a0509609a9777b32dcb2e3016bb05531f915c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Mon, 21 Oct 2024 15:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 21 Oct 2024 15:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2024 15:59:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 21 Oct 2024 15:59:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 21 Oct 2024 15:59:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2024 15:59:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 21 Oct 2024 15:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 21 Oct 2024 15:59:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_MAJOR=9
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_VERSION=9.0.97
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_SHA512=537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9
# Mon, 21 Oct 2024 15:59:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT []
# Mon, 21 Oct 2024 15:59:18 GMT
CMD ["catalina.sh" "run"]
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 21 Oct 2024 15:59:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_VERSION=15.10.13
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.13
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=bb84c62fbe5d6e1ab4b4f3fae25665f98d0e36186f626222a578c608c9401f70
# Mon, 21 Oct 2024 15:59:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 21 Oct 2024 15:59:18 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
VOLUME [/usr/local/xwiki]
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Oct 2024 15:59:18 GMT
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
	-	`sha256:c3432b713e60c07405dd99c350f49dbec2153937fa02b34cdfd31acb7f9db5b4`  
		Last Modified: Mon, 11 Nov 2024 20:49:14 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae45b2ffab2f2bf7f1d3cd898642855b88c5f4e6378f8f5066c7dc30175bf47`  
		Last Modified: Mon, 11 Nov 2024 20:49:15 GMT  
		Size: 13.4 MB (13407598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593646ad6b26739771ad7986741e4550b155513b1e21a40c35026906d8ca9d9e`  
		Last Modified: Mon, 11 Nov 2024 20:49:15 GMT  
		Size: 223.0 KB (223045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7724663f894728fcf0994ab9a4289344d5fa7b73e1b39f698c881e2fe8b9c`  
		Last Modified: Mon, 11 Nov 2024 21:51:08 GMT  
		Size: 192.3 MB (192263746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d120f593bc0c5482534f56d4ea2eabd43ca52d4bd7d61e46b1f1b8cd7e3bfe`  
		Last Modified: Mon, 11 Nov 2024 21:51:09 GMT  
		Size: 307.0 MB (307013294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2ea0c43e004ae87dca7a26ae4db51725d390392a969933968225d5edda607`  
		Last Modified: Mon, 11 Nov 2024 21:51:05 GMT  
		Size: 1.0 MB (1013641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82ba6839f77cbd488bc788693c97613a525b1b60be39cf0fc13b1a80248705d`  
		Last Modified: Mon, 11 Nov 2024 21:51:05 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3cfca7eb55c8a1fcbb537e0049c11151eca8cb32ab2fb171d07891ce7eb21e`  
		Last Modified: Mon, 11 Nov 2024 21:51:06 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e43c46aadbc3a1eecda8e11baa41c29d744fb2467a5b4b2de2910a03e3207a`  
		Last Modified: Mon, 11 Nov 2024 21:51:06 GMT  
		Size: 6.5 KB (6465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff34d02eda51f39b499aaa52b80fb7336fcda92fa8f44244f0a0ece4f7ea358a`  
		Last Modified: Mon, 11 Nov 2024 21:51:07 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:82f57c0ee04ee136a54c1cb070e2685c6f77cf965ffdac20c0eb06b85e26d5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8824494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daf3b5a43e6cad2c74d90190fb349611991211d1b6884da7f8ba869370a3a6a`

```dockerfile
```

-	Layers:
	-	`sha256:647834593ba3a419d9697a9507f35616ac9e12905d740e5a3845d729bc7b0721`  
		Last Modified: Mon, 11 Nov 2024 21:51:05 GMT  
		Size: 8.8 MB (8783490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aca89abaf04567cfb4c73fa9812ef822e0b13fbec9ae0bb7e4d0913857903567`  
		Last Modified: Mon, 11 Nov 2024 21:51:05 GMT  
		Size: 41.0 KB (41004 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c4d1fa0268a256bce5bfbe7c3b47026ff5e1acebcab48a366fec0b837b96beb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.8 MB (603836365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e03ad780fcd9a57375a1464da36445ec303a8b72dfed4c898a176ac24de83ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Mon, 21 Oct 2024 15:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 21 Oct 2024 15:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2024 15:59:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 21 Oct 2024 15:59:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 21 Oct 2024 15:59:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Oct 2024 15:59:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
WORKDIR /usr/local/tomcat
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 21 Oct 2024 15:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 21 Oct 2024 15:59:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_MAJOR=9
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_VERSION=9.0.97
# Mon, 21 Oct 2024 15:59:18 GMT
ENV TOMCAT_SHA512=537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9
# Mon, 21 Oct 2024 15:59:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT []
# Mon, 21 Oct 2024 15:59:18 GMT
CMD ["catalina.sh" "run"]
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 21 Oct 2024 15:59:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 21 Oct 2024 15:59:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_VERSION=15.10.13
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.13
# Mon, 21 Oct 2024 15:59:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=bb84c62fbe5d6e1ab4b4f3fae25665f98d0e36186f626222a578c608c9401f70
# Mon, 21 Oct 2024 15:59:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 21 Oct 2024 15:59:18 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 21 Oct 2024 15:59:18 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 21 Oct 2024 15:59:18 GMT
VOLUME [/usr/local/xwiki]
# Mon, 21 Oct 2024 15:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Oct 2024 15:59:18 GMT
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
	-	`sha256:42643b42f9d46a521c93ae6aa98bfcf7df2af6a425a5cb714f605b13cd53ba3d`  
		Last Modified: Mon, 11 Nov 2024 20:51:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71c39ae33b2d1f4582470747b07dd46b1fc92eca04e57256e622d58219b2919`  
		Last Modified: Mon, 11 Nov 2024 20:56:07 GMT  
		Size: 13.4 MB (13418519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f16806359a1ac39a8ee91d0bf466fb185529dc367a485db3a4c4c0afee537d`  
		Last Modified: Mon, 11 Nov 2024 20:56:07 GMT  
		Size: 223.5 KB (223540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15b8efe9d0a3ce934f42eb98692be8aed7f6255e768788e96bf09cad4336f85`  
		Last Modified: Mon, 11 Nov 2024 21:53:16 GMT  
		Size: 189.9 MB (189854825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed77d0a89aa0eb0e1bc8d1d64c96593751b0901da45e4d66e6e2cfcbc5502b15`  
		Last Modified: Mon, 11 Nov 2024 22:02:31 GMT  
		Size: 307.0 MB (307013335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a2ec90adbc83963c1ed159d7b7cf4963d12f7f8bc63290f80dc99085c860c2`  
		Last Modified: Mon, 11 Nov 2024 22:05:08 GMT  
		Size: 1.0 MB (1013639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2277ebb0e075b1191c681def9f3deeefb76a6180ed0b4e80b7ab6682be394`  
		Last Modified: Mon, 11 Nov 2024 22:05:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372b08c83b85a03624ab7133352b1f831aead1bb8de6afc90902c9fceab1a40b`  
		Last Modified: Mon, 11 Nov 2024 22:05:08 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bf699504babaaebaea82950075dfa223a8be7985993852c3e9550dc6b0d67b`  
		Last Modified: Mon, 11 Nov 2024 22:05:08 GMT  
		Size: 6.5 KB (6464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a59d438e96a83b0cedb00d1deff107065b712c87b9bfe1c8e22e698ff1e9e5`  
		Last Modified: Mon, 11 Nov 2024 22:05:09 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b643815c21720eb7b0d170941c4da704c3a1a120aa5c95710a6d5b45e4944ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8825396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d9c866e37505808b17b1a40eb2ddaa26e53602cd5125795d86c0dc040c425d`

```dockerfile
```

-	Layers:
	-	`sha256:51cd60eef029080381c7352edf6cb4e0136b6d2e7eaf5f230fbcb604deceda3f`  
		Last Modified: Mon, 11 Nov 2024 22:05:08 GMT  
		Size: 8.8 MB (8784230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d6f8c9c535c306694568da84727cacf6a31125d83e4d1d1adaba137bab78c0`  
		Last Modified: Mon, 11 Nov 2024 22:05:08 GMT  
		Size: 41.2 KB (41166 bytes)  
		MIME: application/vnd.in-toto+json
