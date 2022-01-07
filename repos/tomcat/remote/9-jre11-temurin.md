## `tomcat:9-jre11-temurin`

```console
$ docker pull tomcat@sha256:ac336ed1a42b0678ac433aeb5603e34720b4e31768afaf894ab523094ce88c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre11-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:5209d99cfa3670192e9984fbb69d7ae305c9fa9cea30eab951e03d0275385269
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111195744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f2df40ffa90aad980d6cb5db9e61685aa0d2105c8d1dfcb9dee54f0bc29d97`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 20:21:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:22:21 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 20:22:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 20:22:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 20:22:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 30 Nov 2021 01:28:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 30 Nov 2021 01:28:23 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 01:28:23 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 30 Nov 2021 01:28:24 GMT
WORKDIR /usr/local/tomcat
# Tue, 30 Nov 2021 01:28:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:28:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 30 Nov 2021 01:35:48 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 30 Nov 2021 01:35:49 GMT
ENV TOMCAT_MAJOR=9
# Wed, 08 Dec 2021 21:11:58 GMT
ENV TOMCAT_VERSION=9.0.56
# Wed, 08 Dec 2021 21:11:58 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Wed, 08 Dec 2021 21:11:59 GMT
COPY dir:e3d3f180789d9f9be066514d39cc2337a27508089009e55c29e4b42627e7b15b in /usr/local/tomcat 
# Wed, 08 Dec 2021 21:12:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 08 Dec 2021 21:12:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 08 Dec 2021 21:12:06 GMT
EXPOSE 8080
# Wed, 08 Dec 2021 21:12:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c122ee837fa892e5fdd4f7c857600f80a7b8fa855d2475bb325372d55eaff04`  
		Last Modified: Mon, 29 Nov 2021 20:25:31 GMT  
		Size: 24.8 MB (24814948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f1998a9aba4fee813599796e2502aac2844a51a791fdccdf274824664cb50`  
		Last Modified: Mon, 29 Nov 2021 20:26:41 GMT  
		Size: 43.2 MB (43201085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d68b8b292ea2456da9c58fc765ee49e44c5b1e640c6ec5ec01f7db864df5606`  
		Last Modified: Mon, 29 Nov 2021 20:26:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f23bd1ba1ced272aad944abcbfc0bb8af97d29463eae53e8a253d991c09453f`  
		Last Modified: Tue, 30 Nov 2021 01:53:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f2607b61a549df3696127c264a857801e00ad1599ca3460c8b10ce449f6e9b`  
		Last Modified: Wed, 08 Dec 2021 21:50:18 GMT  
		Size: 12.3 MB (12251940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e53f14fe6c45a0a50c6436eec976e07b9e9ede06a2d43cec6a3396961847983`  
		Last Modified: Wed, 08 Dec 2021 21:50:17 GMT  
		Size: 2.4 MB (2360208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779fe985b08c319fad3dfcf95641a7c3285f20de41104a955852f5006a6b68fd`  
		Last Modified: Wed, 08 Dec 2021 21:50:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:e8d17482d77117056277f383c78fdf47e28cdd090c6dd770dc2ffda9bc75c8a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103126400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3882aec3af9498b976c1215fc66897e443581978642a009ea9278368f667b016`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 16 Oct 2021 01:12:00 GMT
ADD file:625e3906181f4bd86e59a0e9748f67fcb1391a2e65e36c729e71353381a49757 in / 
# Sat, 16 Oct 2021 01:12:00 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:38:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 19:58:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 19:59:57 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 20:00:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 20:00:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 20:00:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 22:05:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Nov 2021 22:05:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 22:05:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 29 Nov 2021 22:05:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Nov 2021 22:05:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 22:05:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 22:17:52 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 29 Nov 2021 22:17:52 GMT
ENV TOMCAT_MAJOR=9
# Wed, 08 Dec 2021 21:16:42 GMT
ENV TOMCAT_VERSION=9.0.56
# Wed, 08 Dec 2021 21:16:43 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Wed, 08 Dec 2021 21:16:45 GMT
COPY dir:3ae1d3cdfbd6c700c995b82f5271e63a887af70a8d37d6b2da35463b9395a29a in /usr/local/tomcat 
# Wed, 08 Dec 2021 21:16:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 08 Dec 2021 21:17:01 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 08 Dec 2021 21:17:01 GMT
EXPOSE 8080
# Wed, 08 Dec 2021 21:17:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8795d4da4abd6abcafe7285749aa85d3a164999e84720a3845f764e56e306771`  
		Last Modified: Sat, 16 Oct 2021 01:15:01 GMT  
		Size: 24.1 MB (24064451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f49a73fe087725ab5b9956d86afb7a1ca7735fe7eb993e92d61d1d780acba64`  
		Last Modified: Mon, 29 Nov 2021 20:05:51 GMT  
		Size: 23.1 MB (23068723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebc737d2b5103dbc4a72b621b5299b2d7ebcd1f47bb90c5b2ee006cf4da3a93`  
		Last Modified: Mon, 29 Nov 2021 20:08:58 GMT  
		Size: 41.8 MB (41815184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80530a9d33f73ee9ddebbebb5e081e02740350c2831411c5cd79c46761461b0c`  
		Last Modified: Mon, 29 Nov 2021 20:08:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8567ff9705408bd2e6787431270378b613f024b5f29d8d843d492780acfb2aa`  
		Last Modified: Mon, 29 Nov 2021 22:39:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e686f1767866d207b933ee1072d447f456de067c70f1400a8f6c593d09176b`  
		Last Modified: Wed, 08 Dec 2021 21:38:56 GMT  
		Size: 12.2 MB (12200714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffcc2a4ab31515dc5e885f539ba8b03f8f4748c2d020fcce029dc0d38bd454`  
		Last Modified: Wed, 08 Dec 2021 21:38:52 GMT  
		Size: 2.0 MB (1976866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9b137c8f5677c1d4e1d81c0f9c816ce2cc29e5033963bede86d096e651f7d6`  
		Last Modified: Wed, 08 Dec 2021 21:38:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:1aa8fe94039381c3f584c9cd038ce96cfd5385a8ac0e1c6913ebb7cd9f1e58ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107942875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64db8a9087654987a19b72dde8a2ea30f4fa6f907ead3a94464a5a475e6ffd1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:25:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 19:40:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 19:40:43 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 19:41:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 19:41:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 19:41:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 21:18:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Nov 2021 21:18:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 21:18:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 29 Nov 2021 21:18:23 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Nov 2021 21:18:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 21:18:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 21:29:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 29 Nov 2021 21:29:01 GMT
ENV TOMCAT_MAJOR=9
# Wed, 08 Dec 2021 21:26:39 GMT
ENV TOMCAT_VERSION=9.0.56
# Wed, 08 Dec 2021 21:26:40 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Wed, 08 Dec 2021 21:26:42 GMT
COPY dir:99e5778c9e895a1781f7ad3b363bb8b1a2dd39ce6ffd56861cadc2fe16db92b2 in /usr/local/tomcat 
# Wed, 08 Dec 2021 21:26:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 08 Dec 2021 21:26:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 08 Dec 2021 21:26:52 GMT
EXPOSE 8080
# Wed, 08 Dec 2021 21:26:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa42563dc02061b51ce62bff7340de9cea06ea720e8658d2a7693902aa8f700`  
		Last Modified: Mon, 29 Nov 2021 19:44:11 GMT  
		Size: 24.8 MB (24763049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101fa15230f89da61eea58b54b9d024d06737226966fe8f8c5171944f7fb4979`  
		Last Modified: Mon, 29 Nov 2021 19:45:35 GMT  
		Size: 41.5 MB (41518776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d32a871c058540a54a618d3b3727d761f8693bb09d004cd9b726a47b559c9e7`  
		Last Modified: Mon, 29 Nov 2021 19:45:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3812a70afbea32c5090ccc796433aef26b680f3f9ceeede633b9c82ec87c1346`  
		Last Modified: Mon, 29 Nov 2021 21:56:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9883e2a7330415ca84b9a491d054c13fb188318f12790765d8d81c5b6d2a81`  
		Last Modified: Wed, 08 Dec 2021 22:18:20 GMT  
		Size: 12.3 MB (12267292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d91756e22fafb2cfd4b9380a482a02c076e5fd8048c280390254f2a72390da`  
		Last Modified: Wed, 08 Dec 2021 22:18:19 GMT  
		Size: 2.2 MB (2222591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:36fb27b42c07e8be6019bbea20f1c88e9a7044228a57bd81dc87cfea8db4ee42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113393805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a445622c18f10f067792fa1e4db288b9de7a4da269142436240dcde83f09f7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:54:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 20:18:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:19:43 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Mon, 29 Nov 2021 20:20:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 20:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 20:20:42 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 22:04:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Nov 2021 22:04:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 22:04:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 29 Nov 2021 22:04:57 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Nov 2021 22:04:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 22:05:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Nov 2021 22:28:56 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 29 Nov 2021 22:29:01 GMT
ENV TOMCAT_MAJOR=9
# Wed, 08 Dec 2021 21:32:21 GMT
ENV TOMCAT_VERSION=9.0.56
# Wed, 08 Dec 2021 21:32:24 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Wed, 08 Dec 2021 21:32:26 GMT
COPY dir:65fc489a0d4a4e471da5222abb22dec1401947926058b4bd0f06903a775d2def in /usr/local/tomcat 
# Wed, 08 Dec 2021 21:32:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 08 Dec 2021 21:32:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 08 Dec 2021 21:33:02 GMT
EXPOSE 8080
# Wed, 08 Dec 2021 21:33:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce46da97c533978caacb28d5a66ed1f0b6374622ee6806ebe49cc2fa004597f`  
		Last Modified: Mon, 29 Nov 2021 20:25:42 GMT  
		Size: 26.6 MB (26647174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8269e16c15316b550660b9994c851cab79f9fdebdf42c79b8529f0aee69143`  
		Last Modified: Mon, 29 Nov 2021 20:27:10 GMT  
		Size: 38.6 MB (38610182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c82f11e0647d3ee00a96acb9ec278aac47c4b5b8fde3cec519fad7146843088`  
		Last Modified: Mon, 29 Nov 2021 20:27:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae10a965d616944f516bb943a64df545e97be856cabdf631a3a83c7a2975b98`  
		Last Modified: Mon, 29 Nov 2021 22:54:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb6802cda3f68064061d0494b1215a06fdf2946e1bc340b19418a4967f9b680`  
		Last Modified: Wed, 08 Dec 2021 21:49:33 GMT  
		Size: 12.3 MB (12293603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ac0def540e79ebe5ac4b45f66ea3d5dc6f24a558637a0bbcf3b112dbfb9146`  
		Last Modified: Wed, 08 Dec 2021 21:49:32 GMT  
		Size: 2.6 MB (2555144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63fb18cc1f8cce8d73fab5b8ca17a1a7b43f8840ecaa9f3b424aa0d45f8b92c`  
		Last Modified: Wed, 08 Dec 2021 21:49:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:028111bd4aaf22a0029f8253a8ab242ffaeb354060987e12e5308a215ed3607e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101585882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3979acac475dddb0f3ea58291e960731b7132a159b161b09939e98f8da03506`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:15:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 02:15:38 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:15:39 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Fri, 07 Jan 2022 02:16:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        armhf|arm)          ESUM='aee2f20d005b58e79c3c6c02271f797cb387d33a135b762886990b9bf7cb262e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='b4a5af4ffcc98f6b7cdd2232f79aa12f20efa769b5255277fa4974e2e19d4409';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 02:16:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 02:16:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Fri, 07 Jan 2022 03:38:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 07 Jan 2022 03:38:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 03:38:10 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 07 Jan 2022 03:38:10 GMT
WORKDIR /usr/local/tomcat
# Fri, 07 Jan 2022 03:38:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 03:38:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 03:43:02 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 07 Jan 2022 03:43:02 GMT
ENV TOMCAT_MAJOR=9
# Fri, 07 Jan 2022 03:43:03 GMT
ENV TOMCAT_VERSION=9.0.56
# Fri, 07 Jan 2022 03:43:03 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Fri, 07 Jan 2022 03:43:03 GMT
COPY dir:6d4996b162ffd871c5431ede34c1607da4781d35a8cc3680f9589bdf8f6235f0 in /usr/local/tomcat 
# Fri, 07 Jan 2022 03:43:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:43:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 03:43:10 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 03:43:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f72e3f9d5b463f73df3140cbe7e59d12fed8b7531031e702de787ea477fb99`  
		Last Modified: Fri, 07 Jan 2022 02:18:29 GMT  
		Size: 24.4 MB (24446369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8679d0dbf8a4efe252ca844c4d339706419ab6a2237dece25592a751fb5203`  
		Last Modified: Fri, 07 Jan 2022 02:18:52 GMT  
		Size: 37.3 MB (37299559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de505b973cbd8e432df4a36f6b5b76cf72e12402097d370d82863bb89092af47`  
		Last Modified: Fri, 07 Jan 2022 02:18:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910b9a91db898e62b20a5f876a33263b9830fae915ddc3b38c7e2d7c15061ab4`  
		Last Modified: Fri, 07 Jan 2022 03:51:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83458a94826a25bad27d37ace1a0b2fc6a57fbdd10732f5376c8c1bedc6b205e`  
		Last Modified: Fri, 07 Jan 2022 03:54:17 GMT  
		Size: 12.3 MB (12264719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3105c73e57034b0bd9c4454eb9362282faa613411b69f7296b34c65dc735b423`  
		Last Modified: Fri, 07 Jan 2022 03:54:16 GMT  
		Size: 453.8 KB (453772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f538d9201bdfc1603057533343df7182af165da4a4a99f2b76704a74183fb3`  
		Last Modified: Fri, 07 Jan 2022 03:54:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
