## `tomcat:jre25-temurin-noble`

```console
$ docker pull tomcat@sha256:6cdd8a3cbbc3dc63ed9746d0ea926e7e9cd9d03e2fb023d8a2434237909b7b77
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

### `tomcat:jre25-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:5b7667ce908776ac58b61cbf6a17113994fcb993f280b2c1201ddded31d20d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119894046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfc14d914dd6648ba7ce141665725ad8b366e2ff3b60a7719b312fbae1fa2d6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:33 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 01:23:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:23:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 21:00:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 21:00:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 21:00:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 21:00:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 21:00:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:00:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:00:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 20 Mar 2026 21:00:48 GMT
ENV TOMCAT_VERSION=11.0.20
# Fri, 20 Mar 2026 21:00:48 GMT
ENV TOMCAT_SHA512=8edf12ae9ffb837d1fa1542beae9a80b40419c341963eabed074f2f11d8168e0a82307d5fdc010102db5ee2b983b404816b13435f8c6810b7684fe7b3c19191d
# Fri, 20 Mar 2026 21:00:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 21:00:56 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:00:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 21:00:57 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 21:00:57 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 21:00:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e210113259fe04e17a86e74121503992a3e239e1ef81dd38e1e9e83b792202ab`  
		Last Modified: Tue, 17 Mar 2026 01:24:06 GMT  
		Size: 11.5 MB (11478856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fe1bc7be93af9e8b8efe19761ab8d4c2c5288089a9c1971ac3eb4f1bf91ca`  
		Last Modified: Tue, 17 Mar 2026 01:24:07 GMT  
		Size: 62.7 MB (62739519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4beb2895c684784cd3d998919c3e324aa19a17016f005449cecfd56eb34bd`  
		Last Modified: Tue, 17 Mar 2026 01:24:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac91cdcbb38181c01ab9d94f522727adfc4d4d40c1dc68306f58a6ffd55f10c0`  
		Last Modified: Fri, 20 Mar 2026 21:01:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86769c8ea7661319f9c8873c33f038eafe36ac2a9effe6c537cccae47aa72c3d`  
		Last Modified: Fri, 20 Mar 2026 21:01:06 GMT  
		Size: 14.3 MB (14319368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c013e8f26bc256c1d58d4d54ec321a2db38cde5f8e0a9f797acb53c958d532f`  
		Last Modified: Fri, 20 Mar 2026 21:01:06 GMT  
		Size: 1.6 MB (1621792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:da4b3f1576bce32f53f9b055b61932f019f0b20a94d1bf99a3d4ec15155a8873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c66eed4b3ed1bd35eb00b61093bd8548c579dd90a2b6d3d60d142e77913e9d`

```dockerfile
```

-	Layers:
	-	`sha256:4d3c68fc1e2eb323b7b138a0a3f9496aec6fc58b78fa233c0c95e5e8f57a93b4`  
		Last Modified: Fri, 20 Mar 2026 21:01:06 GMT  
		Size: 3.1 MB (3128624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d4977dccc4331dd81502e3266b3bd6460583d52343b99c0fafe52bdf5e4d88`  
		Last Modified: Fri, 20 Mar 2026 21:01:06 GMT  
		Size: 24.0 KB (24034 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2bd980efbdcc39369c60ee583fde23521210f7bb92adb7dfa0ad1ade044ba099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118073697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dceceaa789f6434a8ec76864c5ba4527c43952ff4cbf23edae5588693771d16`
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
# Fri, 20 Mar 2026 21:06:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 21:06:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 21:06:13 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 21:06:13 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 21:06:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:06:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:06:13 GMT
ENV TOMCAT_MAJOR=11
# Fri, 20 Mar 2026 21:06:13 GMT
ENV TOMCAT_VERSION=11.0.20
# Fri, 20 Mar 2026 21:06:13 GMT
ENV TOMCAT_SHA512=8edf12ae9ffb837d1fa1542beae9a80b40419c341963eabed074f2f11d8168e0a82307d5fdc010102db5ee2b983b404816b13435f8c6810b7684fe7b3c19191d
# Fri, 20 Mar 2026 21:06:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 21:06:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:06:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 21:06:24 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 21:06:24 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 21:06:24 GMT
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
	-	`sha256:b7c28a0f88b8086823d989b55f6bdec8c79179ca45c2578957797617d4f96949`  
		Last Modified: Fri, 20 Mar 2026 21:06:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c6494725597a33efa99682263bdad894200a7f8df4be83b620395554ef97f`  
		Last Modified: Fri, 20 Mar 2026 21:06:33 GMT  
		Size: 14.3 MB (14322515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ac1847f12a435f453e8756538d63db79ea442e308e70a59a9ccff3ebe4bb8d`  
		Last Modified: Fri, 20 Mar 2026 21:06:33 GMT  
		Size: 1.7 MB (1701769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:1d9f3fb89205952ccf4b1dd72d7be244c5a4496c687bd1403ebcf41e0eb8940e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a51ac0884bd894b81e78260b9b989021905946dd7f9e5d8d1ec935cd39c8d0f`

```dockerfile
```

-	Layers:
	-	`sha256:291d53a110f170666683ca111780f323e39665df2f8d1d32a352d094b5e34788`  
		Last Modified: Fri, 20 Mar 2026 21:06:32 GMT  
		Size: 3.1 MB (3129170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6fc2e258a70fb3a182ffb5a59504b03bedadda34c701122ac9b7d16339e2ef6`  
		Last Modified: Fri, 20 Mar 2026 21:06:32 GMT  
		Size: 24.3 KB (24291 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:3a49c465959027c8cd367ba1dc18d2030d090d89c4b4fe9fa34461027116dec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124815777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec69201a66ef557d56a3cecb621603b6fb4ac78bd2cbf0eddcbb791ea8af3b1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:40:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:40:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:40:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:40:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:40:15 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 08:40:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:40:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:40:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:40:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 20:59:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 20:59:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 20:59:38 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 20:59:39 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 20:59:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_MAJOR=11
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_VERSION=11.0.20
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_SHA512=8edf12ae9ffb837d1fa1542beae9a80b40419c341963eabed074f2f11d8168e0a82307d5fdc010102db5ee2b983b404816b13435f8c6810b7684fe7b3c19191d
# Fri, 20 Mar 2026 20:59:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 21:00:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:00:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 21:00:05 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 21:00:05 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 21:00:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194463f9419a1bf2205df9e7d5df2892cdbfd6b97558fcadbea80ff7d91f116d`  
		Last Modified: Tue, 17 Mar 2026 08:41:20 GMT  
		Size: 12.0 MB (12045612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8767a2ae368196d31808b3af0f6397980fa2821a14172e25a6987edd81289f24`  
		Last Modified: Tue, 17 Mar 2026 08:41:21 GMT  
		Size: 62.2 MB (62160255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5514a7166c5e3d0d8e756a2c26045b15ea865b76fb8e07e357250db3a21d5c`  
		Last Modified: Tue, 17 Mar 2026 08:41:19 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ea828d41a73557f2d00360e49d6a3e27962e4eec91a3db00d7f176a3da0a0`  
		Last Modified: Fri, 20 Mar 2026 21:00:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc3603b23d566ccaa591efd704e15481e96e48b371107d063767bda053d8e31`  
		Last Modified: Fri, 20 Mar 2026 21:00:28 GMT  
		Size: 14.3 MB (14337059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2906ce8fb7d3124c3fdcfbbd347cdd76669be917dfb4ea91e855979686df02`  
		Last Modified: Fri, 20 Mar 2026 21:00:28 GMT  
		Size: 2.0 MB (1960286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:ee9fda17495561c2cc28fbb26308cb1da816bcc4ba3af0abdc119ba2fd779619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3102942a0a84ca1ac3da3c4f8304255a10e737ac2e41e9ff2e8fe05792707d`

```dockerfile
```

-	Layers:
	-	`sha256:24be82b2483cf804fcf7b3df259536a14505b6c1d487941f1797aebdf65d3064`  
		Last Modified: Fri, 20 Mar 2026 21:00:28 GMT  
		Size: 3.1 MB (3131969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0767c3053f30d3f0833b3b18bc1d9ec99e960cf87efacc514ce885289f8827a`  
		Last Modified: Fri, 20 Mar 2026 21:00:27 GMT  
		Size: 24.1 KB (24141 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:dff497a82fd0771934a91eb3d09b178df16bbd7e6e9770621c8db70119d3445f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121862171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ea182c8399c0a60c19558027962d0ba7782462230b5508fa377df94462cc54`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:42:34 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:43:25 GMT
ADD file:1243b7db425cac690d91f87ad37c1beec0d95da6b3942dc8084039fe1cc2baf4 in / 
# Mon, 23 Feb 2026 17:43:30 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 04:48:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 21 Mar 2026 04:48:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Mar 2026 04:48:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 21 Mar 2026 04:48:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Mar 2026 04:48:43 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Sat, 21 Mar 2026 04:50:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 21 Mar 2026 04:50:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 21 Mar 2026 04:50:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 21 Mar 2026 04:50:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Mar 2026 20:37:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 22 Mar 2026 20:37:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 20:37:55 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sun, 22 Mar 2026 20:37:55 GMT
WORKDIR /usr/local/tomcat
# Sun, 22 Mar 2026 20:37:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 22 Mar 2026 20:37:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 22 Mar 2026 20:37:55 GMT
ENV TOMCAT_MAJOR=11
# Sun, 22 Mar 2026 20:37:55 GMT
ENV TOMCAT_VERSION=11.0.20
# Sun, 22 Mar 2026 20:37:55 GMT
ENV TOMCAT_SHA512=8edf12ae9ffb837d1fa1542beae9a80b40419c341963eabed074f2f11d8168e0a82307d5fdc010102db5ee2b983b404816b13435f8c6810b7684fe7b3c19191d
# Sun, 22 Mar 2026 20:37:58 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sun, 22 Mar 2026 20:38:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Mar 2026 20:38:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sun, 22 Mar 2026 20:38:56 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 22 Mar 2026 20:38:56 GMT
ENTRYPOINT []
# Sun, 22 Mar 2026 20:38:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:866473980fd7aa6ac5a8a995315a35248ab945008a1938bd15f65082df53b2d3`  
		Last Modified: Mon, 23 Feb 2026 17:51:46 GMT  
		Size: 31.0 MB (30960145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f474b2e5cecdff9db4622d779d2676b53a8be46e836dcd3e27e499364ed32139`  
		Last Modified: Sat, 21 Mar 2026 04:53:32 GMT  
		Size: 11.6 MB (11571286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dc35300c04dc5f2fec7cc36aff01f20990d2a79fef31cc558f8c258a69bb04`  
		Last Modified: Sat, 21 Mar 2026 04:53:39 GMT  
		Size: 61.4 MB (61447420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8451caf5f8be0a8de837e0d0bc138af49b47a0cd3a7195f2b2773addef83a200`  
		Last Modified: Sat, 21 Mar 2026 04:53:28 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8fbbf881941970fb59679f80941d7da3c5638443a2c67cafc7629366401b1`  
		Last Modified: Sun, 22 Mar 2026 20:40:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4187172c629fb0e4bc98ef2fbac72e45b0431d90080c57c28c7e40b63434be8`  
		Last Modified: Sun, 22 Mar 2026 20:40:42 GMT  
		Size: 14.5 MB (14506375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b86d0db17cf38bbf1d5054ff46273366b561093b8e97d887a696b62f0ae986`  
		Last Modified: Sun, 22 Mar 2026 20:40:41 GMT  
		Size: 3.4 MB (3374428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:05c45368c89303ed960ef4774b4b20d94456c83cb91b3bbbd7a29acd05396107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65800ea5bdbc64b3dd6c139c76baf6a966a600a2db3c11e9f768d2eb4cd7306a`

```dockerfile
```

-	Layers:
	-	`sha256:febfb245f1333edb9c74dd35ee6b4ca94952c89a7e1a532d6cc2f499f175a638`  
		Last Modified: Sun, 22 Mar 2026 20:40:40 GMT  
		Size: 3.1 MB (3120665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac28df8a10ff58301f63d4d8eb2847bfa98d3c7473caa1635643541603732d0d`  
		Last Modified: Sun, 22 Mar 2026 20:40:40 GMT  
		Size: 24.1 KB (24140 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:2c6ff98190ce01a0413fcb5224e6d0eb9e41e451f8b7749461c5e76541f0b479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117987701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f15859a36f3d8afd604378d8e0ef1cb55bb1c1eb02a731cfb0718cc23d835fb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 02:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:50 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 02:24:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 02:24:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 02:24:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:24:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 21:09:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 21:09:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 21:09:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 21:09:02 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 21:09:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:09:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:09:02 GMT
ENV TOMCAT_MAJOR=11
# Fri, 20 Mar 2026 21:09:02 GMT
ENV TOMCAT_VERSION=11.0.20
# Fri, 20 Mar 2026 21:09:02 GMT
ENV TOMCAT_SHA512=8edf12ae9ffb837d1fa1542beae9a80b40419c341963eabed074f2f11d8168e0a82307d5fdc010102db5ee2b983b404816b13435f8c6810b7684fe7b3c19191d
# Fri, 20 Mar 2026 21:09:02 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 21:09:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:09:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 21:09:07 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 21:09:07 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 21:09:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30166fea89a383a0d9545d5677ccbf686314b4c3a87a74ee27ff60ca9e33be84`  
		Last Modified: Tue, 17 Mar 2026 02:24:26 GMT  
		Size: 11.8 MB (11757226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fbf074b2b1c333204e968253748a06509ab16faff8526baf4ffdec2c9bbc15`  
		Last Modified: Tue, 17 Mar 2026 02:24:28 GMT  
		Size: 60.4 MB (60354197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5516e50ae684951ea25c93200391e1003f440ba8e30af7cdefbe76477b829ade`  
		Last Modified: Tue, 17 Mar 2026 02:24:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c722a4e54892b7dcae1f9925179e51359205036e202667bd22f414130f1383f`  
		Last Modified: Fri, 20 Mar 2026 21:09:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a670887b5976d8c665ae0fa0bcd2fbdabd399cbf14d804e27657b6b78268e31b`  
		Last Modified: Fri, 20 Mar 2026 21:09:21 GMT  
		Size: 14.3 MB (14327866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93e00626bd20764f0c5f7faf18c4d758af9f4ca0c97ea8b506a2deb990eb7ff`  
		Last Modified: Fri, 20 Mar 2026 21:09:21 GMT  
		Size: 1.6 MB (1635516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:c1da21b667eb00784fc322b0ced762bb76c7fd04d047872bba777efa945db3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf20acfa9dedd7bf075a9f1fd394a852cf0ff48e8932fb48da2ee1accc9f2617`

```dockerfile
```

-	Layers:
	-	`sha256:38ee241ee54d81324ed77f97787b588a5105a3aeba03a535957ae4dd39175f05`  
		Last Modified: Fri, 20 Mar 2026 21:09:21 GMT  
		Size: 3.1 MB (3130221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1d0b0070cd2b648603973ca1255c1a35354caefedc7b4ee28775f8865fab5b`  
		Last Modified: Fri, 20 Mar 2026 21:09:21 GMT  
		Size: 24.0 KB (24033 bytes)  
		MIME: application/vnd.in-toto+json
