## `tomcat:10-jre21-temurin`

```console
$ docker pull tomcat@sha256:1082b7125b71dca26a09b5d6bd7c9c2c66343b23166c62c6a1d8a37fc0aacff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:10-jre21-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:3c1ae4dd3dc3bdc30741fe48eacb0663ccde8fb654ec01160fe12462e8a1900f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110119211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf472fa3ffb6da893db581e8a0ab839c18654378972fdffd9e4db4fda9448bfa`
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
# Wed, 05 Jun 2024 08:07:28 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 05 Jun 2024 08:07:28 GMT
ENV TOMCAT_MAJOR=10
# Wed, 05 Jun 2024 08:07:28 GMT
ENV TOMCAT_VERSION=10.1.24
# Wed, 05 Jun 2024 08:07:28 GMT
ENV TOMCAT_SHA512=793802f5cbbc0c4f722d3c63b52323df7ca37846445c254edcaaa7702fd71cf72aa9506b2b2c59322b9635e25f69913aa1b223098d9b4f1426f5f5447dd78ff3
# Wed, 05 Jun 2024 08:07:28 GMT
COPY dir:ecd88a972e285cc0d22d48532215a37b2d3e7c9938c4280a51c7986c7566e21e in /usr/local/tomcat 
# Wed, 05 Jun 2024 08:07:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 08:07:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 05 Jun 2024 08:07:35 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 08:07:35 GMT
ENTRYPOINT []
# Wed, 05 Jun 2024 08:07:35 GMT
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
	-	`sha256:0de8ca77a41faa79a7d9d74e1f8e010acc85467947dec94e1dc216e08af02946`  
		Last Modified: Wed, 05 Jun 2024 08:22:49 GMT  
		Size: 12.8 MB (12845406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c18d1cc33a761b93067d79f55f949d5ea3865acaaeec0b0072b50dbfe420b74`  
		Last Modified: Wed, 05 Jun 2024 08:22:48 GMT  
		Size: 456.3 KB (456333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c1d6f3dbb806fe3a532aef3c114fd85d22c8179ee058bea8b80acdc2583543`  
		Last Modified: Wed, 05 Jun 2024 08:22:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre21-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:a3560f6fecf058edbbcd5d5cb8625f02a4638f778482f17aa571f7a7cd32c9ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107155165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93bd9fa68ffaeca7107dbf25f0b742e81108191f45da4cb1e58b9d2b32d4a56`
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
# Wed, 05 Jun 2024 07:19:46 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 05 Jun 2024 07:19:46 GMT
ENV TOMCAT_MAJOR=10
# Wed, 05 Jun 2024 07:19:46 GMT
ENV TOMCAT_VERSION=10.1.24
# Wed, 05 Jun 2024 07:19:46 GMT
ENV TOMCAT_SHA512=793802f5cbbc0c4f722d3c63b52323df7ca37846445c254edcaaa7702fd71cf72aa9506b2b2c59322b9635e25f69913aa1b223098d9b4f1426f5f5447dd78ff3
# Wed, 05 Jun 2024 07:19:46 GMT
COPY dir:36e5ca59596256de8b9f27d64090ad97f6d8ce61cdbccf774386b79a9d2e9209 in /usr/local/tomcat 
# Wed, 05 Jun 2024 07:19:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 07:19:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 05 Jun 2024 07:19:51 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 07:19:51 GMT
ENTRYPOINT []
# Wed, 05 Jun 2024 07:19:51 GMT
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
	-	`sha256:e6b1e04643232f58664a48ca7d328b02cd8da8a9708652b7162a3a0c052f1d92`  
		Last Modified: Wed, 05 Jun 2024 07:33:32 GMT  
		Size: 12.8 MB (12846840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53749386bfd12b9496b2b545a22ebeeb5fbda374516498580e86002ecd158d47`  
		Last Modified: Wed, 05 Jun 2024 07:33:31 GMT  
		Size: 456.9 KB (456850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adcce79092e33322677f0f0bf13edca32eecd80dcf4ef86f6001323c07a5a30`  
		Last Modified: Wed, 05 Jun 2024 07:33:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre21-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:c1088373be334344e88db8370c48fdebe86515eb3ce6cc6762a013d8c8a9e593
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116253970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb1810ae30543aba923786d092bfd25098538338b6d9159f3e03e13443144a`
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
# Wed, 05 Jun 2024 07:40:23 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 05 Jun 2024 07:40:23 GMT
ENV TOMCAT_MAJOR=10
# Fri, 21 Jun 2024 00:35:21 GMT
ENV TOMCAT_VERSION=10.1.25
# Fri, 21 Jun 2024 00:35:21 GMT
ENV TOMCAT_SHA512=d7498e23e54425d728ed3481579dccc4fe3d720a4b6d491ce9a04f9d19647b60a398b76dbfec63a32f7ee98195b97231d34b6f850283f38a1acb9908d3015565
# Fri, 21 Jun 2024 00:35:22 GMT
COPY dir:c61101d237ea107f71663f0b40263b87dcce5a38576802d777e2db48c44b0bf4 in /usr/local/tomcat 
# Fri, 21 Jun 2024 00:35:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Jun 2024 00:35:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 21 Jun 2024 00:35:32 GMT
EXPOSE 8080
# Fri, 21 Jun 2024 00:35:32 GMT
ENTRYPOINT []
# Fri, 21 Jun 2024 00:35:33 GMT
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
	-	`sha256:0f321e47ad551d866f6e5b190f23e156ccc71aa8b9ff188e054ee6d1137e36a8`  
		Last Modified: Fri, 21 Jun 2024 00:51:06 GMT  
		Size: 12.9 MB (12871879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67506b13a1f7af7d3f58aab8ec9a2e37f31af4d3d2616eb432820223350be9fe`  
		Last Modified: Fri, 21 Jun 2024 00:51:05 GMT  
		Size: 487.5 KB (487509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c176ad97e176a57a3cba3f73e68f452c8874ae58fdce67b71bb40964cfe371ea`  
		Last Modified: Fri, 21 Jun 2024 00:51:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre21-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:bd1c2de787787381ef843ade6703a8b274a894b35a20eafe4ebfd8a3f092fe7c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104559990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a23637d3ee1bf0b2abec7b4eed1d9270abf3478af66ea2dc639fffa92018f`
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
# Wed, 05 Jun 2024 04:15:50 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 05 Jun 2024 04:15:51 GMT
ENV TOMCAT_MAJOR=10
# Wed, 05 Jun 2024 04:15:51 GMT
ENV TOMCAT_VERSION=10.1.24
# Wed, 05 Jun 2024 04:15:51 GMT
ENV TOMCAT_SHA512=793802f5cbbc0c4f722d3c63b52323df7ca37846445c254edcaaa7702fd71cf72aa9506b2b2c59322b9635e25f69913aa1b223098d9b4f1426f5f5447dd78ff3
# Wed, 05 Jun 2024 04:15:52 GMT
COPY dir:e9ea9676e2e4affc3986bb311c414c51c4961ea01ead817310c88b27342fa6c4 in /usr/local/tomcat 
# Wed, 05 Jun 2024 04:15:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:15:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 05 Jun 2024 04:15:58 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 04:15:58 GMT
ENTRYPOINT []
# Wed, 05 Jun 2024 04:15:59 GMT
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
	-	`sha256:e64d3cf7f5230b7ebbb2dcd8e9b79d791736f60e35de3e1d6bc861a153f6188e`  
		Last Modified: Wed, 05 Jun 2024 04:26:51 GMT  
		Size: 12.8 MB (12846946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e649cce57bdb568d8d5cd4279a369679fc1aabb7a531f4143e52d75b5b6ba`  
		Last Modified: Wed, 05 Jun 2024 04:26:50 GMT  
		Size: 457.9 KB (457851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554a69e48208fcf8bd5801baf0326c08e43c3e57440645d8c63e982855507ce8`  
		Last Modified: Wed, 05 Jun 2024 04:26:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
