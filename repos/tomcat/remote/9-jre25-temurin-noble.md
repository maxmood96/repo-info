## `tomcat:9-jre25-temurin-noble`

```console
$ docker pull tomcat@sha256:999168b5f698e85aa0df9c531d8305a9062ec3fb4ba87dc5c044d1bc4b21d51f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:9-jre25-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:753574e1a589b6333f06733c9ee9912f4946c2188db134ec5461b5027ac20f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117928715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb2ab0b1059567eac662b8a4212b034f9665e48d9571f83e0aa881c2b806c9f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:20:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:20:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:20:27 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Feb 2026 20:20:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:56:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:56:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:56:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:56:49 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:56:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:49 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 21:56:49 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 21:56:49 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 21:56:49 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:56:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:56:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:56:57 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:56:57 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:56:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c455c0f698f7e1cd2c305f426f9306ffd199fdf279d571220d153da681406c51`  
		Last Modified: Tue, 17 Feb 2026 20:20:59 GMT  
		Size: 11.5 MB (11478448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778806e8a80c3539a1b703b2b5d01890828c8c7de74eb541afb571192642807`  
		Last Modified: Tue, 17 Feb 2026 20:21:01 GMT  
		Size: 62.7 MB (62739588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbc60fb7edbd02ff22bc83c9018ed57979fa894f84276db97e2f09ddfb1ab8a`  
		Last Modified: Tue, 17 Feb 2026 20:20:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1d6cb0fa2ccfda035bba461c14eefd1edda1cb7d846e2a0c28e15b8931b8e8`  
		Last Modified: Tue, 17 Feb 2026 21:57:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20070f60e1754ceb29ea92d50e806fddc1eaaf608668705f6b8eb27f4ad70a4b`  
		Last Modified: Tue, 17 Feb 2026 21:57:07 GMT  
		Size: 13.8 MB (13772861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7933c3cda262ad44a6411e038af0ae2ee5659208aa437029b5bd0998cb3ce86b`  
		Last Modified: Tue, 17 Feb 2026 21:57:06 GMT  
		Size: 207.7 KB (207689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:850c43a2f0f937dd0c542085ecbc5e3b3bb3bd5a89361b72bbb050bcf96dc666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001d809ff7f155d58d819c6fcbd64ebcc4461a1e1cf1e24c0717f4624da2c340`

```dockerfile
```

-	Layers:
	-	`sha256:d27d758f909ef8fa0faf295e2f9e9c28b224f7c29195641991edf11d5d98a8d7`  
		Last Modified: Tue, 17 Feb 2026 21:57:06 GMT  
		Size: 3.1 MB (3124990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4bd0090d09dc2baeb2dc5542692cecdb1d70a440e7201c198bb70a75facdef`  
		Last Modified: Tue, 17 Feb 2026 21:57:06 GMT  
		Size: 23.1 KB (23085 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:dbfd806ce2416a1b61027dd8a853d15d151295ead231a43d401dcef2442bb4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117535330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03d81f72de4701183833fa21b7bab97665cb9700f54824bda08baab4631f216`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:25:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:25:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:25:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:25:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:25:08 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 01:25:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:25:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:25:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:25:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 03:30:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Mar 2026 03:30:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:30:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Mar 2026 03:30:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Mar 2026 03:30:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:30:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:30:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Mar 2026 03:30:03 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Mar 2026 03:30:03 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Mar 2026 03:30:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Mar 2026 03:30:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:30:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Mar 2026 03:30:14 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Mar 2026 03:30:14 GMT
ENTRYPOINT []
# Tue, 17 Mar 2026 03:30:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b12c6640853e67ef0d9a7a4d247818668c2edf45a9334c716bdd25d19d4cbd7`  
		Last Modified: Tue, 17 Mar 2026 01:25:44 GMT  
		Size: 11.5 MB (11474104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1744d0bb12d98f6d6a2f9273c5c27f3bbaf85750ec288690fd03450eb825c99`  
		Last Modified: Tue, 17 Mar 2026 01:25:45 GMT  
		Size: 61.7 MB (61703083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67820c22223e552e861de5238ee4bce7a26990c6e01f12bbcc141ab8a6a99f19`  
		Last Modified: Tue, 17 Mar 2026 01:25:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200fa2c1412fb07e942134ef69c24a39fbdd3394f352be5db5948b674f4b20c0`  
		Last Modified: Tue, 17 Mar 2026 03:30:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafbecc15b4071005822264a80cb6d097f0942a9df21affe81b248de2c9e0ff4`  
		Last Modified: Tue, 17 Mar 2026 03:30:23 GMT  
		Size: 13.8 MB (13784185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6966d858787a685ea1daab57d83484e2702f838a3ed24f9d237d580e7a8b67e`  
		Last Modified: Tue, 17 Mar 2026 03:30:23 GMT  
		Size: 1.7 MB (1701732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:e733b0649cf4ebfc03b0ad63f6cc9c4b32a60944016960cce355f92dc13c4827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3751c2c09391c46418e05e2ff4a100884708be3a37d4badd17761eb80aabba33`

```dockerfile
```

-	Layers:
	-	`sha256:25d04bc4f1d8325563878e685a635b0a41626272f6654e05a3cfae3d6de46458`  
		Last Modified: Tue, 17 Mar 2026 03:30:23 GMT  
		Size: 3.1 MB (3125528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:547d47c51c84bae90e2d02eba295ef2aa4751082388ddb9845202aaef1ef078c`  
		Last Modified: Tue, 17 Mar 2026 03:30:22 GMT  
		Size: 23.3 KB (23307 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:0549f3a69fd737892313e6143bae3cb690840259411e9c858b5ecef551f47a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122567950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a063c55158f80970037b878db0fc1055a266496e6a2972488b5c0c17f4a6963b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:25:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:25:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:25:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:25:14 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Feb 2026 20:25:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:25:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:25:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:25:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 01:02:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 18 Feb 2026 01:02:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 01:02:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 18 Feb 2026 01:02:02 GMT
WORKDIR /usr/local/tomcat
# Wed, 18 Feb 2026 01:02:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:02:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:02:02 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 Feb 2026 01:02:02 GMT
ENV TOMCAT_VERSION=9.0.115
# Wed, 18 Feb 2026 01:02:02 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Wed, 18 Feb 2026 01:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 18 Feb 2026 01:11:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 01:11:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 18 Feb 2026 01:11:24 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 18 Feb 2026 01:11:24 GMT
ENTRYPOINT []
# Wed, 18 Feb 2026 01:11:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ac8130911d29552005e8dc1adc8d4c0c77a134e745283a38f5cae953119387`  
		Last Modified: Tue, 17 Feb 2026 20:26:23 GMT  
		Size: 12.0 MB (12049938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a70277297fa4e7bcde81697a95d520c7f21512faebf0954fc8e3c64af78c73`  
		Last Modified: Tue, 17 Feb 2026 20:26:24 GMT  
		Size: 62.2 MB (62160546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120e2f662b07e2a925eb202b36cb6128e839518ec207ded27522998aaf4c06c1`  
		Last Modified: Tue, 17 Feb 2026 20:26:22 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba2ce10dffcba095afeb5f52853f5826f44776b47a7a657f9408854e61cbf04`  
		Last Modified: Wed, 18 Feb 2026 01:02:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83da9cb706c7527c8eb150a97c75c0d0511c423353f78584ea6e9faac44d1021`  
		Last Modified: Wed, 18 Feb 2026 01:11:49 GMT  
		Size: 13.8 MB (13809177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c6ca26df897706d8e3ea489b0cef1dbae4960b6a2d9fb63586f067726d92fb`  
		Last Modified: Wed, 18 Feb 2026 01:11:49 GMT  
		Size: 238.9 KB (238866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:92f9c9cf28726b97f4f3d3fdeb329889242fdea23fdd6918ed30202bc04a2c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656d01f2f2d203ead7ac982f1a65546cd97d39c6c2588191d3e0a1da380f0763`

```dockerfile
```

-	Layers:
	-	`sha256:cbb85ef7000931645924bd3dd5af9bba7fdecbcd222e723224bccb6dd74fb619`  
		Last Modified: Wed, 18 Feb 2026 01:11:49 GMT  
		Size: 3.1 MB (3128317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ebf2b19759ff94f1893380536e9a39801031b057067049d060729064f5956a`  
		Last Modified: Wed, 18 Feb 2026 01:11:49 GMT  
		Size: 23.2 KB (23173 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:98e070c88609115ef06dbe317e27c27d257dfb120e0f06c3746c7c167a8dc9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118473850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6397dd220a569070b90e1f36581812da2d453eb36d98d5a30b515803661fafe1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 17:33:09 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:33:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 17:33:55 GMT
ADD file:b4821892707dbb5cc8e8eb3b4e757edc2d124db81fcdedfc3b244dcb5c1fa6c0 in / 
# Tue, 10 Feb 2026 17:34:00 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 00:29:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 00:29:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 00:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 00:29:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 00:29:12 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 18 Feb 2026 00:31:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Feb 2026 00:31:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 00:31:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 00:31:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 12:42:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 18 Feb 2026 12:42:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 12:42:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 18 Feb 2026 12:42:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 18 Feb 2026 12:42:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 12:42:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 12:42:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 Feb 2026 12:42:45 GMT
ENV TOMCAT_VERSION=9.0.115
# Wed, 18 Feb 2026 12:42:45 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Wed, 18 Feb 2026 13:01:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 18 Feb 2026 13:02:02 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 13:02:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 18 Feb 2026 13:02:10 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 18 Feb 2026 13:02:10 GMT
ENTRYPOINT []
# Wed, 18 Feb 2026 13:02:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f2683d5e2cbe038b4f1178e139d507e705e0a3a566f8b9c89bf3484f426119af`  
		Last Modified: Tue, 10 Feb 2026 17:42:05 GMT  
		Size: 31.0 MB (30954431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831de0243bc9488f71b3b66349d205a1d996f7b01d436abc07a6b50156e53075`  
		Last Modified: Wed, 18 Feb 2026 00:34:05 GMT  
		Size: 11.6 MB (11570590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd6ac6c036f44fa37a8137dbec73ed0f64cc75f098f6904bbecb16b777ed088`  
		Last Modified: Wed, 18 Feb 2026 00:34:13 GMT  
		Size: 61.4 MB (61447006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12257dd5655bcabd3b34a807f625883ca5a5d196d0fceae3fbcbfdf3ad3c06`  
		Last Modified: Wed, 18 Feb 2026 00:34:02 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659700a256920ffb615e14afd1753c39b11e975be80d45169d90b969657c0ea7`  
		Last Modified: Wed, 18 Feb 2026 12:45:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebc65e9438c6ecad6b6c5abc531611406067df023401bf0a0e2e97ab01653d0`  
		Last Modified: Wed, 18 Feb 2026 13:03:55 GMT  
		Size: 14.3 MB (14289442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fde52fef5db7e47a99b781192cf9e8ea83879383e3b1fd5dcd722b05a282b68`  
		Last Modified: Wed, 18 Feb 2026 13:03:52 GMT  
		Size: 209.9 KB (209864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:4dc37299622e56d346de6f8af4ac2cb329641c595dc1d622b40883a0db4eae9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee07a39ff74185e539bc60360a393ef65369c66cf7aff30c3bcb9502a8a24f4`

```dockerfile
```

-	Layers:
	-	`sha256:a051d3c122765634d993087c14a61ddeeb0ffc6dd1fd2ac52c9f36fecb7e3f40`  
		Last Modified: Wed, 18 Feb 2026 13:03:53 GMT  
		Size: 3.1 MB (3117013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34864d8f535b4981feebcc09014c646aaf02e51ae159b341ee37deb10d690778`  
		Last Modified: Wed, 18 Feb 2026 13:03:52 GMT  
		Size: 23.2 KB (23173 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre25-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:4ac1fe2efd4f5261a7e6597700fe0692ff5adcc99433e71f3ab89f93ea8aca91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116036401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1af1007395c3530d3a18ea400b0d7892a49da747a6c4f89b4d6bb041b90fc8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:16:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:16:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:16:02 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Feb 2026 20:16:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:16:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:16:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:16:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 22:46:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 22:46:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:46:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 22:46:08 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 22:46:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:46:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:46:08 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 22:46:08 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 22:46:08 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 22:46:08 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 22:46:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:46:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 22:46:14 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 22:46:14 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 22:46:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616bbe1030ddb84f1469d98d7314f3325675d775c27f7da2ba229294acb3afc3`  
		Last Modified: Tue, 17 Feb 2026 20:17:00 GMT  
		Size: 11.8 MB (11768526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae760efd38f3a43c7ef95223d19bf2cbc55d9cc670c37eecb547e12c1d324e5e`  
		Last Modified: Tue, 17 Feb 2026 20:17:01 GMT  
		Size: 60.4 MB (60354428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e64028b16e2074c26eb1055cd858f83774643d4c0d54f71a228afa34e53555`  
		Last Modified: Tue, 17 Feb 2026 20:16:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ed5b94dd350041298ce9d77c00a5081478bde2e4c093c667297a980c136d2f`  
		Last Modified: Tue, 17 Feb 2026 22:46:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a8bb03adc0a6a01b28b5c6dd9d17b55a9c45ce0edce4a6b5d44b2816df4c55`  
		Last Modified: Tue, 17 Feb 2026 22:46:43 GMT  
		Size: 13.8 MB (13785847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c986990242fc14f184ef70f1854f56992d192efc88a46b21f3e86951079a2`  
		Last Modified: Tue, 17 Feb 2026 22:46:43 GMT  
		Size: 215.3 KB (215299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:8e22016f89d96d3f8d8a80d00d3fb909e74ede05001a5a556d9f7234068032e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c02f869e07ea6e634ace2a40d5e3911e05155d4ac41933d9554e1f37a06a2df`

```dockerfile
```

-	Layers:
	-	`sha256:35b41e01c1336db0820f169c81cec9ee96ad0177da24f97885bf54d0546f02c6`  
		Last Modified: Tue, 17 Feb 2026 22:46:43 GMT  
		Size: 3.1 MB (3126587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c473e8a85329f22a8d88969a0709a8f6a497b4e8dceeb4c66b19551aec54173`  
		Last Modified: Tue, 17 Feb 2026 22:46:43 GMT  
		Size: 23.1 KB (23085 bytes)  
		MIME: application/vnd.in-toto+json
