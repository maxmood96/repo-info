## `tomcat:9-jre8-temurin`

```console
$ docker pull tomcat@sha256:deff3fbcf1e04f441550f5d0aa5688b518f7c7473d04c2670c17e769ae4c6c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:9-jre8-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:7dc1be56d03d97af2426d11be068d2fe4cf7882cb7dd0c9685c20b55caa0ae0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98071665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1957cfda2f2b0101917a47601c91167412dec24a58dac73ea6cc90ca70e274c0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Apr 2024 10:12:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 16 Apr 2024 10:12:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 10:12:45 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 16 Apr 2024 10:12:45 GMT
WORKDIR /usr/local/tomcat
# Tue, 16 Apr 2024 10:12:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 16 Apr 2024 10:12:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 16 Apr 2024 10:12:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 16 Apr 2024 10:12:45 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Apr 2024 00:46:42 GMT
ENV TOMCAT_VERSION=9.0.88
# Wed, 17 Apr 2024 00:46:42 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Wed, 17 Apr 2024 00:46:42 GMT
COPY dir:c63e8c91b45d73465cb0e368e15f31bdd74a73588bb5416f2bb819d312bf2f5c in /usr/local/tomcat 
# Wed, 17 Apr 2024 00:46:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Apr 2024 00:46:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 17 Apr 2024 00:46:49 GMT
EXPOSE 8080
# Wed, 17 Apr 2024 00:46:49 GMT
ENTRYPOINT []
# Wed, 17 Apr 2024 00:46:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dddff65ed2408fb8512cf4a5e475bc56396102dc76b9968c1f68a06414767b`  
		Last Modified: Tue, 16 Apr 2024 04:03:41 GMT  
		Size: 12.9 MB (12905145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c7e4ccbe979d8e79e63d863452c2bc94f95fd31b8cf46ae307470f61a03f80`  
		Last Modified: Tue, 16 Apr 2024 04:04:17 GMT  
		Size: 41.8 MB (41846616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59af882453355c312e1afd4d49bc179f05565d48e626b679bd634738a1739e8f`  
		Last Modified: Tue, 16 Apr 2024 04:04:12 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8ac3bcbe147b6a36609f38f62b6f16e47f2726880baf7eec6483da2bc3d8a0`  
		Last Modified: Tue, 16 Apr 2024 04:04:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3842e734b13e246fa5de00ffff351722b062ade4565e24ec1c64b91b573c1fa7`  
		Last Modified: Tue, 16 Apr 2024 10:23:04 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2880aff0ff884fc811952b4a5fd968d78ea34821ad604856a8919faed5b17fad`  
		Last Modified: Wed, 17 Apr 2024 00:56:41 GMT  
		Size: 12.4 MB (12422659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94c74048a525e8b5ebc4c79b59c60cbb1ca546d7f4c3f9ccb51c6b17be44df7`  
		Last Modified: Wed, 17 Apr 2024 00:56:40 GMT  
		Size: 456.3 KB (456270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af55e90af1daf3aaf13024fd468b0eaa2570b00d19d8f8a0914d9e5da1dd9be`  
		Last Modified: Wed, 17 Apr 2024 00:56:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:aebb4716649f5eebe5018f6b3362bee43d628b8d270ec14f30ef8ede28ce12b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92376660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd5e770f38ff2d89f209714d3c8bf801f6bb9326b46993c8b646215af82e304`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Apr 2024 19:09:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Apr 2024 19:09:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:09:25 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Apr 2024 19:09:25 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Apr 2024 19:09:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Apr 2024 19:09:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Apr 2024 19:09:25 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 24 Apr 2024 19:09:25 GMT
ENV TOMCAT_MAJOR=9
# Wed, 24 Apr 2024 19:09:25 GMT
ENV TOMCAT_VERSION=9.0.88
# Wed, 24 Apr 2024 19:09:26 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Wed, 24 Apr 2024 19:09:26 GMT
COPY dir:c7e155b87a6f672c7f87a50c2425d4a978f9b5fa3c5bf566217903a2ff4fc5eb in /usr/local/tomcat 
# Wed, 24 Apr 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 19:09:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Apr 2024 19:09:33 GMT
EXPOSE 8080
# Wed, 24 Apr 2024 19:09:33 GMT
ENTRYPOINT []
# Wed, 24 Apr 2024 19:09:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8e34fc49fc731bf85ce0a83deec49456ee2c584bf1a5c472db447d8a9b9a06cb`  
		Last Modified: Fri, 12 Apr 2024 01:35:18 GMT  
		Size: 27.5 MB (27533083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fcdb6b302d1f197eacdca37c53a51b762670c261ce3f687c83be6f26ee6ab6`  
		Last Modified: Tue, 16 Apr 2024 01:53:36 GMT  
		Size: 12.5 MB (12492494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838446cb9a99549d07302cc1b184f07fe5ca1cb1e95a8582a7f072f0b97a0891`  
		Last Modified: Wed, 24 Apr 2024 18:13:27 GMT  
		Size: 39.6 MB (39563144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635699c660d041e378251b4a2d6b58568dbe7c024808ae6610fe37b6ea9a2d5b`  
		Last Modified: Wed, 24 Apr 2024 18:13:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a728b81c3e238153e6a2826a7d4a8c70a6cb5d008bc7ecb7e2c2b2d8fc53bb81`  
		Last Modified: Wed, 24 Apr 2024 18:13:22 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863d78495771d58ee2e21ea6bf8a177860d11923b288873220a5439137e56181`  
		Last Modified: Wed, 24 Apr 2024 19:16:30 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95d6baa5ad034534c9debddb882714f2cdedcf9e088ef45121412f9f1df4a3a`  
		Last Modified: Wed, 24 Apr 2024 19:16:31 GMT  
		Size: 12.4 MB (12357218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34a40a1a41a16df48abfd438aca844cd2698a000b6729e0403a0522e966c76e`  
		Last Modified: Wed, 24 Apr 2024 19:16:30 GMT  
		Size: 429.5 KB (429526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53da42425e52c1c684588d255ed33f6dbae95a4a1082be0abcfcc0309dcf2cc`  
		Last Modified: Wed, 24 Apr 2024 19:16:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:6aa312b0fcc01c7c1eb521ecd674dbe7c2614275e237c9e51f09f3a90b96c421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94983980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6631162ee0f891e2834f93472dcf091265d77d34dd9069caa6b650a57c4ff1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Apr 2024 20:17:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Apr 2024 20:17:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 20:17:09 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Apr 2024 20:17:09 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Apr 2024 20:17:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Apr 2024 20:17:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Apr 2024 20:17:09 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 24 Apr 2024 20:17:09 GMT
ENV TOMCAT_MAJOR=9
# Wed, 24 Apr 2024 20:17:09 GMT
ENV TOMCAT_VERSION=9.0.88
# Wed, 24 Apr 2024 20:17:09 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Wed, 24 Apr 2024 20:17:10 GMT
COPY dir:ab1f5933f8e0571badd9c5f85aea7e29005842b39ed010a8eccfcb979cefda3d in /usr/local/tomcat 
# Wed, 24 Apr 2024 20:17:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 20:17:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Apr 2024 20:17:15 GMT
EXPOSE 8080
# Wed, 24 Apr 2024 20:17:15 GMT
ENTRYPOINT []
# Wed, 24 Apr 2024 20:17:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84929ccc85f98585c5a55bfaab61c181e21f64829da65349954899cbc817f826`  
		Last Modified: Wed, 24 Apr 2024 17:55:10 GMT  
		Size: 40.9 MB (40850732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd26556457856fa4ef6b357415e157af19510bd101171f9668d8357a1015d87`  
		Last Modified: Wed, 24 Apr 2024 17:55:06 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cf19aa92390bd600a9a8a0eebd62e904f2d0f3b1342cb8f0a0ad06936f0761`  
		Last Modified: Wed, 24 Apr 2024 17:55:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868f8f83393f5b0cf26776cb42bf71cd6c89923958978d4e031ae355fd011089`  
		Last Modified: Wed, 24 Apr 2024 20:27:07 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e29f39b54ae0afebbbba7fea828fa9fdb4594ec17c2b7df2ca442dbf798747e`  
		Last Modified: Wed, 24 Apr 2024 20:27:08 GMT  
		Size: 12.4 MB (12428963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3cf3d750f6319848885240975ccf4455a23b5469be8cb750a58d457bdb0947`  
		Last Modified: Wed, 24 Apr 2024 20:27:07 GMT  
		Size: 455.7 KB (455692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a67712179826099845b88b35647643a54d4e61108e2df140589a733018b37`  
		Last Modified: Wed, 24 Apr 2024 20:27:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:9527963e17df421902c4540b7b7c3b4bd2151b5bb28eea741392f0776c029037
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103536359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b2b6518dfdd6dd1a785885b1730c7100fb6d1d7df0e94c0fcd55dc5b513da8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Apr 2024 19:25:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Apr 2024 19:26:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:26:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Apr 2024 19:26:02 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Apr 2024 19:26:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Apr 2024 19:26:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Apr 2024 19:26:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 24 Apr 2024 19:26:05 GMT
ENV TOMCAT_MAJOR=9
# Wed, 24 Apr 2024 19:26:06 GMT
ENV TOMCAT_VERSION=9.0.88
# Wed, 24 Apr 2024 19:26:06 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Wed, 24 Apr 2024 19:26:07 GMT
COPY dir:82fe6ad15605f862f0227c4856d75282ba6148803d35c21ee3b4575d57c52bb7 in /usr/local/tomcat 
# Wed, 24 Apr 2024 19:26:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 19:26:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Apr 2024 19:26:19 GMT
EXPOSE 8080
# Wed, 24 Apr 2024 19:26:20 GMT
ENTRYPOINT []
# Wed, 24 Apr 2024 19:26:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27059a37dad5b2569dc7e52921098941cfcaf0d5cde7c56e3a893ad1e2f636f`  
		Last Modified: Tue, 16 Apr 2024 02:49:35 GMT  
		Size: 13.8 MB (13767192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc3b674c9d8931b9e2b9ded6a0e4a9429115f4fbf77b12659a05dd4a993cb3`  
		Last Modified: Wed, 24 Apr 2024 17:43:05 GMT  
		Size: 41.2 MB (41242486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7536b63fb36ffd54193d39746541be162744d35817f961b6a7802f067fce1943`  
		Last Modified: Wed, 24 Apr 2024 17:42:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac275397cec88123e32b7f07481f8c1261b5656a7ebadd395b6866fcc10a2cb`  
		Last Modified: Wed, 24 Apr 2024 17:42:59 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de00dcb679fba5a90f2ba80f542e904a2a389f5a0ef309597023bc2545e8584`  
		Last Modified: Wed, 24 Apr 2024 19:39:13 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3544449cdebd7264ce464f9966e8318a1bde3a27d85751b5965be357a7351d29`  
		Last Modified: Wed, 24 Apr 2024 19:39:15 GMT  
		Size: 12.5 MB (12450585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb5edc7f6e82babcd589f171ddeeb4c24305d847c830bca6302baa8694fbe89`  
		Last Modified: Wed, 24 Apr 2024 19:39:14 GMT  
		Size: 487.6 KB (487650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341054094fc97a7714c201c3baa9a34a117bcad57613047c51ca19c46627c9fb`  
		Last Modified: Wed, 24 Apr 2024 19:39:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
