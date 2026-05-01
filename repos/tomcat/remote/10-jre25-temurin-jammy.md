## `tomcat:10-jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:b179362e5727e48fd8892c735f661d4a9c0b1ba08bc8362383d584c28e2bcc2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:10-jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:95202b35c90060bc4cb803c3ec0929a96f7720085579d31d54052b164a54a69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118684511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d367c27204c2f51f50da167fc692ca61b0c1de5766d289b77c8bc17f9e4a28aa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:32 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 May 2026 00:14:23 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:14:23 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:14:23 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:14:24 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:14:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 May 2026 00:14:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 May 2026 00:14:24 GMT
ENV TOMCAT_MAJOR=10
# Fri, 01 May 2026 00:14:24 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 01 May 2026 00:14:24 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 01 May 2026 00:14:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 01 May 2026 00:14:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:14:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 01 May 2026 00:14:31 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 01 May 2026 00:14:31 GMT
ENTRYPOINT []
# Fri, 01 May 2026 00:14:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2163368e5d72fbd8ff367d4e75341133d7d6f2e0803ae9767457a5b2d3bfd51e`  
		Last Modified: Thu, 30 Apr 2026 23:30:05 GMT  
		Size: 11.4 MB (11406200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bfbb181a4e3f2f4c48687eba9c3def1eddebd4cab5d2206cacffa36bb720cc`  
		Last Modified: Thu, 30 Apr 2026 23:30:06 GMT  
		Size: 63.0 MB (63010594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b3669d69b5182a0d63996ff6b4770086cd3d11e8867474dbd9d4ab6b06c5ab`  
		Last Modified: Thu, 30 Apr 2026 23:30:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f79fa77028344ae46f5f9df2b1be3acbb31d5ecda0632304366ce77f129d45`  
		Last Modified: Fri, 01 May 2026 00:14:39 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9388982b6f3533fd65cb42c707cf209f2f5b1706342efd8924f00cdbdf9020`  
		Last Modified: Fri, 01 May 2026 00:14:40 GMT  
		Size: 14.3 MB (14315229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52199fbca72cfb6428d0b879a5f1b6589782dc0b9122683f67f05ae634832dff`  
		Last Modified: Fri, 01 May 2026 00:14:40 GMT  
		Size: 213.5 KB (213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:372003e4866a9349aca4f2e31ae047bbef91471a4e9ffded1d381eba6db91378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13db461aae7a9e04b0efdc7eabde7915180c1d3aab3e004c45895285233a1c81`

```dockerfile
```

-	Layers:
	-	`sha256:74bbfec1c30efa7ff85240aa4c12e1c664386c5fb9f03b69ccbbf1cb96dd693b`  
		Last Modified: Fri, 01 May 2026 00:14:40 GMT  
		Size: 3.7 MB (3708290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c058866fdaac4c26cf4922fa3497e144cd90e8a4ce3df1f380d876e16075209b`  
		Last Modified: Fri, 01 May 2026 00:14:40 GMT  
		Size: 21.2 KB (21210 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2b005adf60d21d9eecfaf259d1277345391fe6dcee7036c7a649abe8f2b8ccd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115404638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c61cc72b455ebf27b90d50a01443bfe1518cb3e22d1892da829037687baae0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:30:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:30:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:30:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:30:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:30:07 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:30:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:30:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:30:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:30:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 May 2026 00:13:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:13:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:13:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:13:18 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:13:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 May 2026 00:13:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 May 2026 00:13:18 GMT
ENV TOMCAT_MAJOR=10
# Fri, 01 May 2026 00:13:18 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 01 May 2026 00:13:18 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 01 May 2026 00:13:43 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 01 May 2026 00:13:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:13:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 01 May 2026 00:13:51 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 01 May 2026 00:13:51 GMT
ENTRYPOINT []
# Fri, 01 May 2026 00:13:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02b3899d3f6fdf65e2db872c173618ee50fa5f9b0bd944c52e93838eea6dcc9`  
		Last Modified: Thu, 30 Apr 2026 23:30:44 GMT  
		Size: 11.4 MB (11354768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9dbdbb8f943d19f73506d6644410734cbffa8c6646657eb1542fc8e6b10ed1`  
		Last Modified: Thu, 30 Apr 2026 23:30:45 GMT  
		Size: 61.9 MB (61912753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c085cc1723eb9ff96dc6aab8baf1e039501becc056f4e1721c359a2afbbf56a`  
		Last Modified: Thu, 30 Apr 2026 23:30:44 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85ea275b612c239881d8b90930ce309357978a2732da9d642c45ed064619c7e`  
		Last Modified: Fri, 01 May 2026 00:13:34 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55442ea10df0d7395727781ca689d449431bbd90510e51e5f7dddffa9018d133`  
		Last Modified: Fri, 01 May 2026 00:14:00 GMT  
		Size: 14.3 MB (14315580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dcf22cb5539a04fcb6859bfe195bf09ff8359f09a5d8bbb4cb5bc69ffec0a3`  
		Last Modified: Fri, 01 May 2026 00:13:59 GMT  
		Size: 212.5 KB (212476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:128d65053289abd50a98fcc05fff8cf408f569cc2cfe7e98fba8eefa2e5d02d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82f6afd168fb8efa94b64f8f0f935e0bee5f2d145675ac605b0d26c3c603862`

```dockerfile
```

-	Layers:
	-	`sha256:d9f6bd6e7d8dfead7ca264beafc7e0e648fab7e488387a959991c3d825b4ee99`  
		Last Modified: Fri, 01 May 2026 00:13:59 GMT  
		Size: 3.7 MB (3707941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccf7709c415b80cff9e48d60bdf5a64f2930525fbe4660e06391fc1911533c5c`  
		Last Modified: Fri, 01 May 2026 00:13:59 GMT  
		Size: 21.4 KB (21357 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:3d47e0cfc99bd3b93c6a8520da5453ce5aeb761c9aae7e4922e396b9d8ac9f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123526992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb463684422468a9bc283f1303c5ebe86eb0247d6d32e1f248fc56aeeb218ab3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:15 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:30:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:30:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:30:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:30:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 May 2026 00:37:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:37:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:37:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:37:27 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:37:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 May 2026 00:37:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 May 2026 00:37:27 GMT
ENV TOMCAT_MAJOR=10
# Fri, 01 May 2026 00:37:27 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 01 May 2026 00:37:27 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 01 May 2026 00:38:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 01 May 2026 00:38:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:38:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 01 May 2026 00:38:44 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 01 May 2026 00:38:44 GMT
ENTRYPOINT []
# Fri, 01 May 2026 00:38:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09adfae83adada80107491fe4b68740c3c81f0dcd7f5f8a379f33016c2ae35d0`  
		Last Modified: Thu, 30 Apr 2026 23:30:53 GMT  
		Size: 11.9 MB (11894721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa7ef2c458aa59e2cc03df20d01c2230c7cec40ca28809e356d1a404c60ecfc`  
		Last Modified: Thu, 30 Apr 2026 23:30:54 GMT  
		Size: 62.4 MB (62411008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae5c112c97b47fce4c11c5348b61c72ff73d12a0d923784830535efa0a59945`  
		Last Modified: Thu, 30 Apr 2026 23:30:52 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eb0b38f39f1a6540201b239061e9fb53a5b5aa14c9784532f043c5d9631e57`  
		Last Modified: Fri, 01 May 2026 00:38:02 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119d832f65af569672748f4043a3945cc3b1edb42cdf2805a91e208dc13bd622`  
		Last Modified: Fri, 01 May 2026 00:39:08 GMT  
		Size: 14.3 MB (14327159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2049957b2976639f9906eb45279cf4f727169352f38b9bd6ea516c5d60544`  
		Last Modified: Fri, 01 May 2026 00:39:08 GMT  
		Size: 243.2 KB (243188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d47112c67f3ac346d607e34b5d84cb6c7ad2d1d53d3084f9757a3a7051e751e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084e48f7233ed3a75c63b6e38e8d16d8f4c9bd4b786a889852020ed4d6605648`

```dockerfile
```

-	Layers:
	-	`sha256:62f5d3a0910e742e45ff1c9d27c67f6b44b622d233ae6f764bbcbed40e6d3e1d`  
		Last Modified: Fri, 01 May 2026 00:39:08 GMT  
		Size: 3.7 MB (3711630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a10195e13065711bbf8c85ee97091bbd75b77812c8668a4fe0d6d6f664ec60`  
		Last Modified: Fri, 01 May 2026 00:39:08 GMT  
		Size: 21.3 KB (21262 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:1f164c9233f7521dc292c7fd039b40106a1a5bee7afe9f010ba14364d27f8e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114734135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644f52b9c063f61a8b5377976571248de4934b82995a07c19851203c2c9379b7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:26:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:26:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:26:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:26:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:26:14 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:26:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:26:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:26:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:26:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 May 2026 00:13:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 May 2026 00:13:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:13:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 01 May 2026 00:13:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 May 2026 00:13:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 May 2026 00:13:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 May 2026 00:13:51 GMT
ENV TOMCAT_MAJOR=10
# Fri, 01 May 2026 00:13:51 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 01 May 2026 00:13:51 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 01 May 2026 00:13:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 01 May 2026 00:13:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:13:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 01 May 2026 00:13:54 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 01 May 2026 00:13:54 GMT
ENTRYPOINT []
# Fri, 01 May 2026 00:13:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc592beaf1d2de55c24bb557cd1fdaa1b9991cb09f89a8b207ac1c161b01186`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 11.5 MB (11499427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cad66dd9d61f17530c822d80df1d1242c16da3019c260e2ab54defcf554cc7d`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 60.5 MB (60500540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a17d43fe3f5462d687fe571cdf5035bf481a2306154f593df2b329df33e0c6`  
		Last Modified: Thu, 30 Apr 2026 23:26:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09ec4e60fabdea4223fc6492f434522e35389885c5cf9fc0e5431f7f0c75df6`  
		Last Modified: Fri, 01 May 2026 00:14:07 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f407c514d0888296408e7bc3f86c6350892b2946734cc7c5144b75fcca88b9`  
		Last Modified: Fri, 01 May 2026 00:14:08 GMT  
		Size: 14.3 MB (14314691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaea576be6023e4ae70672a08ed915483a51638360a01b8baef497160556fbf`  
		Last Modified: Fri, 01 May 2026 00:14:08 GMT  
		Size: 214.7 KB (214661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ff81c80076cdbe35b2e7143cd2efab3893d48f004f089b6a64d7b7e48333eb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03885d828431c754da1a9b36045814a51f3956e890ec3c3c2f7798157f094c`

```dockerfile
```

-	Layers:
	-	`sha256:f3c18f64a1eaca16a39f99e04ed3e9554275bc6882d9ebbf98e5992d48df2d04`  
		Last Modified: Fri, 01 May 2026 00:14:07 GMT  
		Size: 3.7 MB (3709275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:516581dffd9d8c00bf854447ffa53e28060a746547c8a068e14d81dd75c0a5b4`  
		Last Modified: Fri, 01 May 2026 00:14:07 GMT  
		Size: 21.2 KB (21210 bytes)  
		MIME: application/vnd.in-toto+json
