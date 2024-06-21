## `tomcat:9-jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:293d3440466c74562efc851b79c821d4a43bf0d96fefecd05467884505e9f258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:aae6599302e90707fe8232c3e5c3e324516378446be4266c96f26f1089d2e606
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109711971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82417ff8dab67337c92ef1b814d2cf752b014035327e61fb67aeccfd067dfab2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 08:06:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jun 2024 08:06:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 08:06:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jun 2024 08:06:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jun 2024 08:06:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 08:06:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 08:09:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jun 2024 08:09:54 GMT
ENV TOMCAT_MAJOR=9
# Wed, 05 Jun 2024 08:09:54 GMT
ENV TOMCAT_VERSION=9.0.89
# Wed, 05 Jun 2024 08:09:54 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Wed, 05 Jun 2024 08:09:54 GMT
COPY dir:240389a8e5f840a2587eaf13a3a466c5151188ccb775ef01d5f0342d6a81d542 in /usr/local/tomcat 
# Wed, 05 Jun 2024 08:09:59 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 08:10:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 05 Jun 2024 08:10:01 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 08:10:01 GMT
ENTRYPOINT []
# Wed, 05 Jun 2024 08:10:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d859b28d5306bac2883873dfd359a793fe2086ce99608de5dd6137ab2445a8d1`  
		Last Modified: Wed, 05 Jun 2024 05:02:04 GMT  
		Size: 53.5 MB (53472211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c5c06d3c33e2779e44f13e323ac953809d196d828c1376242cb73f239ab0a8`  
		Last Modified: Wed, 05 Jun 2024 05:01:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fb58717a078f857d9a88d9e05ebe0c9a92bbb905490889ee02778ace8b73b2`  
		Last Modified: Wed, 05 Jun 2024 05:01:56 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed5ee96d276b6260913c7a72fa2c73ad1de20dd959a6489bea880c855f15bab`  
		Last Modified: Wed, 05 Jun 2024 08:21:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2f3245586b8c5497ace68d50a247413e3e9a9e78aa0fa224baa64996a61fc6`  
		Last Modified: Wed, 05 Jun 2024 08:25:44 GMT  
		Size: 12.4 MB (12438176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdbeecbeb1ae134dad602ff7ddcc4a235e584254fbaafdd31443b3fedac9c5a`  
		Last Modified: Wed, 05 Jun 2024 08:25:43 GMT  
		Size: 456.3 KB (456323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedd43354f33cadb2fed070c895ddf55e9b96e6033933e9a10b930c438916615`  
		Last Modified: Wed, 05 Jun 2024 08:25:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:dd289a5fbd401bd954302976f7735359f384d7eb58371523f553b2b6a93113ee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106753451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a935bba1310c99b8d1505ad9c56fc16036534228ca60e4b073ce747c6d52411b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 07:19:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jun 2024 07:19:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 07:19:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jun 2024 07:19:08 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jun 2024 07:19:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 07:19:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 07:21:58 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jun 2024 07:21:58 GMT
ENV TOMCAT_MAJOR=9
# Wed, 05 Jun 2024 07:21:58 GMT
ENV TOMCAT_VERSION=9.0.89
# Wed, 05 Jun 2024 07:21:58 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Wed, 05 Jun 2024 07:21:59 GMT
COPY dir:9e8fee4f1735e14de6d1bf0e48c3696cd3112448c5a372034dfd076714be77e9 in /usr/local/tomcat 
# Wed, 05 Jun 2024 07:22:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 07:22:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 05 Jun 2024 07:22:05 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 07:22:05 GMT
ENTRYPOINT []
# Wed, 05 Jun 2024 07:22:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dd329103023d18ce41eb44652e30ca689a1d755661726432a511d48d5b8890`  
		Last Modified: Wed, 05 Jun 2024 04:58:24 GMT  
		Size: 52.6 MB (52600169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7503519ffa3903a117a59b2eb3a0f023ffc97a0090a85df1b75cc000d939844a`  
		Last Modified: Wed, 05 Jun 2024 04:58:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f3b62f3663e6c9ca03fe5533e86a7b8d60753f4fb61c55d859e48259774de9`  
		Last Modified: Wed, 05 Jun 2024 04:58:18 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7e24c54ab7453a6cabb878c4b168a3f56324f6c819234271c701fbb1947b1`  
		Last Modified: Wed, 05 Jun 2024 07:32:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b62a0b1b610d1655edefbe90ad83abd87530a760ddc6ea7a2faab59d915cdc2`  
		Last Modified: Wed, 05 Jun 2024 07:36:16 GMT  
		Size: 12.4 MB (12445132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759ab119f864bd8b56e8faa0c0cfc114091977d480083deadb2a98b162828f28`  
		Last Modified: Wed, 05 Jun 2024 07:36:15 GMT  
		Size: 456.8 KB (456845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e45fd713076e5335af5903c6c461020e02995863b1edbe45f51b42839e1605`  
		Last Modified: Wed, 05 Jun 2024 07:36:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:00e9d3912e3dc0b47ae31091f00421f188d9f3b44dbad93228ee7ca3d0d21813
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115859416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ff7501fa53cee028f73bc0a5b0eaec8b166d18c39a26659f72a9c6284eb19f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 07:38:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jun 2024 07:38:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 07:38:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jun 2024 07:38:53 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jun 2024 07:38:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 07:38:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 07:45:32 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jun 2024 07:45:33 GMT
ENV TOMCAT_MAJOR=9
# Fri, 21 Jun 2024 00:39:31 GMT
ENV TOMCAT_VERSION=9.0.90
# Fri, 21 Jun 2024 00:39:31 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Fri, 21 Jun 2024 00:39:32 GMT
COPY dir:91a85f2c4557a81b150f0a255e26933541d7875578b50affb5308ddabe6fe23a in /usr/local/tomcat 
# Fri, 21 Jun 2024 00:39:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Jun 2024 00:39:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 21 Jun 2024 00:39:42 GMT
EXPOSE 8080
# Fri, 21 Jun 2024 00:39:43 GMT
ENTRYPOINT []
# Fri, 21 Jun 2024 00:39:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82f84268a93862af92928dd1cc1dc31937bbffd50302e61f899397e5223399d`  
		Last Modified: Wed, 05 Jun 2024 04:00:20 GMT  
		Size: 13.8 MB (13766991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5d177e0f88b208921a397171ed73385b75d7f432016500791420c409f00ec9`  
		Last Modified: Wed, 05 Jun 2024 04:04:18 GMT  
		Size: 53.5 MB (53538097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d410407483ede35959a0b6045706e85e41c88124bb8ecd62847b5b2f61fc82bb`  
		Last Modified: Wed, 05 Jun 2024 04:04:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed363f50e5e6714fd4c28aa4be93d0aac96e086f7e2a3aa187353c0af702b20`  
		Last Modified: Wed, 05 Jun 2024 04:00:55 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a4254d4f52ed527bf3056d00504ee9f5a3fe28a78e49e6d4dab9641ed0d92c`  
		Last Modified: Wed, 05 Jun 2024 07:56:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5d92f21a181e603771c895b5236faf392a223ccb231a2ea250bc1a274147b7`  
		Last Modified: Fri, 21 Jun 2024 00:54:05 GMT  
		Size: 12.5 MB (12477320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094bd8b49ae9a042286f68362bd606f303f2cbabcd726fa7948e3e7a028cb13f`  
		Last Modified: Fri, 21 Jun 2024 00:54:03 GMT  
		Size: 487.5 KB (487515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e68e5e3854ab8cd07d9ffddff1cc11c246ce6ac41a7984c540025f0e6181e22`  
		Last Modified: Fri, 21 Jun 2024 00:54:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:14a0cd6ccbd4d9638a4271e8ed1a13438c749115ff254829247c83f17aa51629
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104146927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d814705ef94778e1150133877456c4928c671967fa7de66af8d9d6d1ce663`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 04:14:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jun 2024 04:14:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 04:14:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jun 2024 04:14:36 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jun 2024 04:14:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 04:14:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 04:19:25 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jun 2024 04:19:25 GMT
ENV TOMCAT_MAJOR=9
# Wed, 05 Jun 2024 04:19:25 GMT
ENV TOMCAT_VERSION=9.0.89
# Wed, 05 Jun 2024 04:19:25 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Wed, 05 Jun 2024 04:19:26 GMT
COPY dir:43e41b0cfa1d81d67dda380c3888f10fdffc88bbf8ffe6c045376dd5eaed172b in /usr/local/tomcat 
# Wed, 05 Jun 2024 04:19:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:19:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 05 Jun 2024 04:19:32 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 04:19:32 GMT
ENTRYPOINT []
# Wed, 05 Jun 2024 04:19:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87504bacc983be102c1f56d585bd6aeb2fba4f402fc20a73671274561ac7e98b`  
		Last Modified: Wed, 05 Jun 2024 03:12:32 GMT  
		Size: 13.0 MB (12986422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc08fdaddc92cd1582e03995fdc813d8c09e5fd70040c98d0d35e53bbe8db81`  
		Last Modified: Wed, 05 Jun 2024 03:14:49 GMT  
		Size: 49.6 MB (49630210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756e0fceb49e23b0fc2a9fb98b4f3503b94285f7e530e743701da1f857102345`  
		Last Modified: Wed, 05 Jun 2024 03:14:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eca96f435e3adf1f8b160398ae3c0d9764e9c447022ffb531abd9e279601d00`  
		Last Modified: Wed, 05 Jun 2024 03:14:42 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197c111438ccfb4164b4349621815f87c92ed2c759ac0b93b37464cc9488a6c7`  
		Last Modified: Wed, 05 Jun 2024 04:26:02 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2bbaac76b6dd8fce3de840d37b1ceef717d73faf703dd67673d53f4a795ef5`  
		Last Modified: Wed, 05 Jun 2024 04:29:29 GMT  
		Size: 12.4 MB (12433906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a925440820abb2e06e8c843ad2365ee85551630e3424ab9896102fbc6bd30c43`  
		Last Modified: Wed, 05 Jun 2024 04:29:28 GMT  
		Size: 457.8 KB (457829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476fb5b1ff6b97ee13964e726ede6b87a969c741b93e8b41cd6b769b13092418`  
		Last Modified: Wed, 05 Jun 2024 04:29:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
