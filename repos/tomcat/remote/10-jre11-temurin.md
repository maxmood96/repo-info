## `tomcat:10-jre11-temurin`

```console
$ docker pull tomcat@sha256:3e54f9be8be5524e2ae4a85beb367503bc6c17b53f3cabf0deed18178a6891d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:10-jre11-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:c3a659d1c2b05d50c6f57528afdbec810d9946167dc6acc57720bbfca2ac14ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101584189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da0cc02d5298721e878226742dc9c197a1ced44543b4411f8c140cd1b0ec8d1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:13:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:50 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:21:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:21:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 19:07:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 28 Jul 2022 19:07:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 19:07:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 28 Jul 2022 19:07:38 GMT
WORKDIR /usr/local/tomcat
# Thu, 28 Jul 2022 19:07:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 19:07:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 19:07:39 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 28 Jul 2022 19:07:39 GMT
ENV TOMCAT_MAJOR=10
# Thu, 28 Jul 2022 19:10:17 GMT
ENV TOMCAT_VERSION=10.0.23
# Thu, 28 Jul 2022 19:10:17 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Thu, 28 Jul 2022 19:10:17 GMT
COPY dir:78be586a327545f995719a2315f46eef7a63b8ecdc0babf4e4268053fd317316 in /usr/local/tomcat 
# Thu, 28 Jul 2022 19:10:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 19:10:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 28 Jul 2022 19:10:23 GMT
EXPOSE 8080
# Thu, 28 Jul 2022 19:10:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c045aca8dd90fbfb1afd1343ec6ce2e08ab62f20e8943d3e313dd745e22ee37`  
		Last Modified: Tue, 07 Jun 2022 00:19:41 GMT  
		Size: 12.1 MB (12116064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e4e8c31f0810f5cb82c91bf61acf99e7a81bd911fcdb5df0d53ad540574b31`  
		Last Modified: Thu, 28 Jul 2022 16:27:43 GMT  
		Size: 43.5 MB (43516884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5758e94c6e396f94a62bd4a9b0f25729383864b05594308c77c14fba3f661bad`  
		Last Modified: Thu, 28 Jul 2022 16:27:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31da9a0904ac36419d87cd32948624c7d60902dfe92bcf3554667f8248e93ffa`  
		Last Modified: Thu, 28 Jul 2022 19:30:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fb89de7f4ab78c6e9a347fe845b7ec9925ea517d56ee79beec805c958292c1`  
		Last Modified: Thu, 28 Jul 2022 19:33:56 GMT  
		Size: 12.6 MB (12567870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6058052b3aa7e6f464b09dbfba5cab1db4427b89154c3dca831871d099bb89c`  
		Last Modified: Thu, 28 Jul 2022 19:33:55 GMT  
		Size: 3.0 MB (2959193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7c2e860d9b6c7e4ff1a4405b9ee78223e358d9230115f2fa67b147dd6ed125`  
		Last Modified: Thu, 28 Jul 2022 19:33:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:c5263dea987b57009f723b8b43b5bdb6f20109f561423cc57f9cd76e32bfe329
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95773636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc2d7ce26be0da4c3471ba526d15e9a98447464f2ebd952af645ad361be534d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 07 Jun 2022 05:51:35 GMT
ADD file:26c86cfcbc153addbca421974e648a7af07234cb3f741bfb030aa0db90b6a7c6 in / 
# Tue, 07 Jun 2022 05:51:36 GMT
CMD ["bash"]
# Sat, 30 Jul 2022 02:49:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Jul 2022 02:50:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jul 2022 02:51:21 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Sat, 30 Jul 2022 02:51:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jul 2022 02:51:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jul 2022 02:51:52 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Sat, 30 Jul 2022 12:53:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 30 Jul 2022 12:53:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jul 2022 12:53:54 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 30 Jul 2022 12:53:54 GMT
WORKDIR /usr/local/tomcat
# Sat, 30 Jul 2022 12:53:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 30 Jul 2022 12:53:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 30 Jul 2022 12:53:54 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 30 Jul 2022 12:53:54 GMT
ENV TOMCAT_MAJOR=10
# Sat, 30 Jul 2022 12:57:25 GMT
ENV TOMCAT_VERSION=10.0.23
# Sat, 30 Jul 2022 12:57:25 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Sat, 30 Jul 2022 12:57:26 GMT
COPY dir:9a3395da2ff4df0824e84f1ddf8f6ee79079d23d8f7c0c7252748f036b362bd6 in /usr/local/tomcat 
# Sat, 30 Jul 2022 12:57:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 30 Jul 2022 12:57:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 30 Jul 2022 12:57:35 GMT
EXPOSE 8080
# Sat, 30 Jul 2022 12:57:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5aeb313108e16ff98084efb2ae2830cbe915ea38b3e2fd1e32688dd9d8c11320`  
		Last Modified: Tue, 07 Jun 2022 05:56:03 GMT  
		Size: 27.0 MB (27017432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19fdce069a7dff1a637320e689a92f499bee9dae5c6492ede30168a6194ccd3`  
		Last Modified: Sat, 30 Jul 2022 02:57:14 GMT  
		Size: 11.7 MB (11712882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fd826a0f40510bfbcc2511892f7c717060a1741eb81dbd81f693c7adaf047a`  
		Last Modified: Sat, 30 Jul 2022 02:59:34 GMT  
		Size: 42.1 MB (42097252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4608a760fde635bb54503e31cf7c4f210defaac718c3afc3218108ecc372933`  
		Last Modified: Sat, 30 Jul 2022 02:59:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd6a0dcf8fdb93b5e2c93ea4f5406a00884e905a0c98537eece6b68c41b3feb`  
		Last Modified: Sat, 30 Jul 2022 13:27:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad7c490c5505500df0c30c8f9814d7f589e2329197bad8277487b88a68b261`  
		Last Modified: Sat, 30 Jul 2022 13:31:22 GMT  
		Size: 12.5 MB (12503840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c772beddf759f811b4706f03b67ffa5d6357b1143f89890776e1afdee79205c0`  
		Last Modified: Sat, 30 Jul 2022 13:31:21 GMT  
		Size: 2.4 MB (2441769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232ccfde06ebfc997ef3b8c5ee09ddfdb6bd9cf422d8920ea8c58671fb7aeec1`  
		Last Modified: Sat, 30 Jul 2022 13:31:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b9bcfcbd874e1a33499be5c2bc820bd3126071704a6a347c106339dd4e78b9c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97673372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd08b9bc5c57b680495462731f6e559accfec864bb3f6308a8705215b9e57ef`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:32 GMT
ADD file:20805b983efd5443e34ebdfb7795010e5684eb1ca1ffea30a3e61e0089c0eee8 in / 
# Tue, 07 Jun 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:34:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 06:34:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:41:00 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 15:42:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:42:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 17:25:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 28 Jul 2022 17:25:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 17:25:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 28 Jul 2022 17:25:56 GMT
WORKDIR /usr/local/tomcat
# Thu, 28 Jul 2022 17:25:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 17:25:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 17:25:59 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 28 Jul 2022 17:26:00 GMT
ENV TOMCAT_MAJOR=10
# Thu, 28 Jul 2022 17:30:11 GMT
ENV TOMCAT_VERSION=10.0.23
# Thu, 28 Jul 2022 17:30:12 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Thu, 28 Jul 2022 17:30:14 GMT
COPY dir:5202aeca3c7843279ca4440baae24472702385f5f5662f3b10d5bc21d145566d in /usr/local/tomcat 
# Thu, 28 Jul 2022 17:30:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 17:30:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 28 Jul 2022 17:30:24 GMT
EXPOSE 8080
# Thu, 28 Jul 2022 17:30:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ed02c6ade914c2962413c1ad2ccc86ed8d1512098f2c87fe7bafa8e1b5293185`  
		Last Modified: Thu, 02 Jun 2022 08:38:25 GMT  
		Size: 28.4 MB (28378212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05aeb470f3c462a081767db5b92aa49a956ba558fd0474c8aa38f2197af012ab`  
		Last Modified: Tue, 07 Jun 2022 06:42:05 GMT  
		Size: 12.1 MB (12078242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccd2584ced00304e4d655915cc98d9922b1e7562c8a7d3b206c760c97f4f70e`  
		Last Modified: Thu, 28 Jul 2022 15:49:09 GMT  
		Size: 41.8 MB (41846574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230a803e773b2c421b9d747fa87005a446a1939339294f506a48206570cc92f0`  
		Last Modified: Thu, 28 Jul 2022 15:49:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd22583316ee5235aeaccdff753d38ef1ca35beebc5cfdbed87e8656994a1338`  
		Last Modified: Thu, 28 Jul 2022 18:07:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afc409adcae022df9adf151869e3047634ef734e8610cd21220322734ec7347`  
		Last Modified: Thu, 28 Jul 2022 18:11:53 GMT  
		Size: 12.6 MB (12575125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b35858d2f4b215f4238a314de931da7628915c4f21aa428c6ff8184652b5767`  
		Last Modified: Thu, 28 Jul 2022 18:11:52 GMT  
		Size: 2.8 MB (2794953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:2216d427c579154562b1e4df4cebae25de5f3cedf7bdb89382b9cfb3ffb6be0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103477292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0aa2a8cff1b2627dab70338be3aa8fc80bc2a459e25c4bdf3747c2ba6e659c9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 07 Jun 2022 05:46:49 GMT
ADD file:62ec907c651e833838867bd541cf824f5f609ea4e2b19c4b26cec74a57b60470 in / 
# Tue, 07 Jun 2022 05:46:54 GMT
CMD ["bash"]
# Wed, 27 Jul 2022 00:35:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Jul 2022 00:35:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:17:54 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:19:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:19:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 17:23:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 28 Jul 2022 17:23:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 17:23:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 28 Jul 2022 17:23:01 GMT
WORKDIR /usr/local/tomcat
# Thu, 28 Jul 2022 17:23:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 17:23:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 17:23:02 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 28 Jul 2022 17:23:02 GMT
ENV TOMCAT_MAJOR=10
# Thu, 28 Jul 2022 17:27:45 GMT
ENV TOMCAT_VERSION=10.0.23
# Thu, 28 Jul 2022 17:27:46 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Thu, 28 Jul 2022 17:27:47 GMT
COPY dir:37e0e45eb2f761625f23e2213c3e59ae5bca5006097a7b36f8231fe63044f47a in /usr/local/tomcat 
# Thu, 28 Jul 2022 17:27:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 17:27:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 28 Jul 2022 17:27:58 GMT
EXPOSE 8080
# Thu, 28 Jul 2022 17:27:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b851cfa9fcbcb74629241502e21ebbae255fe40a2f26949573f278672b65c308`  
		Last Modified: Tue, 07 Jun 2022 05:49:53 GMT  
		Size: 35.7 MB (35717509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cafa1747753931a54cd680bfab88daa275922d652dd97af00c278ecbddb7a1`  
		Last Modified: Wed, 27 Jul 2022 00:50:36 GMT  
		Size: 12.9 MB (12861467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1921b191487a9f8fb1f0ea66d84ea176c27885e8b546f9f8c914408247dfeebb`  
		Last Modified: Thu, 28 Jul 2022 16:27:38 GMT  
		Size: 39.0 MB (38955451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acda316018a427209ff3c0f1166ff80b70eab4e135799a4a1001ecf5faf50e70`  
		Last Modified: Thu, 28 Jul 2022 16:27:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdf3f2696845b416af049e1447249e1d0dd06e615ebafff78145c011fadcab8`  
		Last Modified: Thu, 28 Jul 2022 17:54:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1925cab2f9bc8e879622f2bbdb6d21724a1275bb81e10d543c7cf1ccbaa55d70`  
		Last Modified: Thu, 28 Jul 2022 17:59:04 GMT  
		Size: 12.6 MB (12595342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c5bf4a2b066b7252142b60130cda29ba8e725026dbac4d5351fdb4cb14e585`  
		Last Modified: Thu, 28 Jul 2022 17:59:03 GMT  
		Size: 3.3 MB (3347061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b39e79b98ea9d60a33b43ae83b3811868b36c266d4e05f398861f213286dc26`  
		Last Modified: Thu, 28 Jul 2022 17:59:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:fe158bbb31b7d1f454ed2827dee1c16b083ef2c393caac5b99da85928bb35100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91262916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c692d919cc3173f9a35db1acf45e91ac368bc2ba810cc8a64efc4ddff44a94`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:03:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Aug 2022 13:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:03:58 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Tue, 02 Aug 2022 13:04:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 13:04:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 13:04:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 03 Aug 2022 01:48:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Aug 2022 01:48:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 01:48:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 03 Aug 2022 01:48:14 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Aug 2022 01:48:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 01:48:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 01:48:14 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 03 Aug 2022 01:48:15 GMT
ENV TOMCAT_MAJOR=10
# Wed, 03 Aug 2022 01:50:45 GMT
ENV TOMCAT_VERSION=10.0.23
# Wed, 03 Aug 2022 01:50:45 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Wed, 03 Aug 2022 01:50:46 GMT
COPY dir:d8e2a94e4a45badef6ac2cb3bd434ffc4747e84c41b3e3d23aaa825d97cd7977 in /usr/local/tomcat 
# Wed, 03 Aug 2022 01:50:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 01:50:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Aug 2022 01:50:50 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 01:50:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46d94d0c843b66928f2a851d94cb062b8cf7bf458d8730859fb3e10b6838317`  
		Last Modified: Tue, 02 Aug 2022 13:09:24 GMT  
		Size: 12.2 MB (12164840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c51c23f784b7af99062b7358f237f1842b79958776d9f432c94c7ed3e46b14b`  
		Last Modified: Tue, 02 Aug 2022 13:10:02 GMT  
		Size: 37.4 MB (37438359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b8af85d3c97f325e7342ee78c8e8e9059f7e5d4d82769d3dc05291dc2edd81`  
		Last Modified: Tue, 02 Aug 2022 13:09:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c707a62fb803689065814e3d9be7b445647b2602bc3a1d00135035fc6124dea`  
		Last Modified: Wed, 03 Aug 2022 02:05:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ea271c95d8e3d3e4d2bab207d2e23196a6d0f415a0a867951cca35877fdfe9`  
		Last Modified: Wed, 03 Aug 2022 02:07:57 GMT  
		Size: 12.6 MB (12564812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4236915d41c468b3b2d4ab27bea1272a9c603c6abac85f3b24f6f1bcde065088`  
		Last Modified: Wed, 03 Aug 2022 02:07:56 GMT  
		Size: 451.7 KB (451657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddee01551691b71a6564b3288c9d50ddb1d2c346a21edc02f0bfd7402c25d951`  
		Last Modified: Wed, 03 Aug 2022 02:07:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
