## `eclipse-temurin:16-jdk-focal`

```console
$ docker pull eclipse-temurin@sha256:6f1e9727dbc18fb74597c641b9662295cc4fd90b13bc1fba58eee4c394a5c1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:16-jdk-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f39280eaaac8c5d82b5c3fd9e9d3e1e7c713d3eb032d8cc80a1b150da220672d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254805641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddec6b7d676fa6bf7b3e9e77c6598f30c1f7a342a83d89d7d754d1b523084542`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 24 Aug 2021 18:20:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Aug 2021 18:20:33 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Tue, 24 Aug 2021 18:20:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb77d9d126f97898dfdc8b5fb694d1e0e5d93d13a0a6cb2aeda76f8635384340';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.2_7.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36ebe6c72f2fc19b8b17371f731390e15fa3aab08c28b55b9a8b71d0a578adc9';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.2_7.tar.gz';          ;;        s390x)          ESUM='fa3ab64ae26727196323105714ac50589ed2782a4c92a29730f7aa886c15807e';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.2_7.tar.gz';          ;;        amd64|x86_64)          ESUM='323d6d7474a359a28eff7ddd0df8e65bd61554a8ed12ef42fd9365349e573c2c';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 24 Aug 2021 18:20:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Aug 2021 18:20:44 GMT
RUN echo Verifying install ...     && echo   javac --version && javac --version     && echo   java --version && java --version     && echo Complete.
# Tue, 24 Aug 2021 18:20:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3daa047319b6a85eed1d68142297370fa6c7b3765c475fb36d539d0041afe0`  
		Last Modified: Tue, 24 Aug 2021 18:21:36 GMT  
		Size: 19.8 MB (19775101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea4a0fa432f99cf964fa1e7e733294be074594e2afc3c8e9d7785a83c4034b9`  
		Last Modified: Tue, 24 Aug 2021 18:21:49 GMT  
		Size: 206.5 MB (206462435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5536d555224b1156b6c5b3e5ad4e52a34fd1a689bbedf5da77a534a43eee0739`  
		Last Modified: Tue, 24 Aug 2021 18:21:33 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:16-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8147d6292380931fb60e782261c844e3b308db71583bef33290de848e089c327
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251793335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8531710986ae04a38334fc87b0d219a1deeca96a775a6bd7a0b62a44baad481e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 24 Aug 2021 18:40:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Aug 2021 18:40:19 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Tue, 24 Aug 2021 18:40:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb77d9d126f97898dfdc8b5fb694d1e0e5d93d13a0a6cb2aeda76f8635384340';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.2_7.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36ebe6c72f2fc19b8b17371f731390e15fa3aab08c28b55b9a8b71d0a578adc9';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.2_7.tar.gz';          ;;        s390x)          ESUM='fa3ab64ae26727196323105714ac50589ed2782a4c92a29730f7aa886c15807e';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.2_7.tar.gz';          ;;        amd64|x86_64)          ESUM='323d6d7474a359a28eff7ddd0df8e65bd61554a8ed12ef42fd9365349e573c2c';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 24 Aug 2021 18:40:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Aug 2021 18:40:30 GMT
RUN echo Verifying install ...     && echo   javac --version && javac --version     && echo   java --version && java --version     && echo Complete.
# Tue, 24 Aug 2021 18:40:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cd5c71bfeeb06b1cacd1c7f4538fae9e20c5a7ffab905c3e7232f9aa0f8f44`  
		Last Modified: Tue, 24 Aug 2021 18:41:52 GMT  
		Size: 20.5 MB (20498836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cba5976cdf6807063d51c29d134ed29d6d48a4ade99daf3072a2b068525052`  
		Last Modified: Tue, 24 Aug 2021 18:42:08 GMT  
		Size: 204.1 MB (204124083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203171dd7db349c8a4a4161336ce5049232615096c18547c271659fa7c9bcd29`  
		Last Modified: Tue, 24 Aug 2021 18:41:48 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:16-jdk-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:bbec99a870a61e0fb77da374d33189bab62086484f4de25cd19195952a58356d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241925041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67832e90f1ad5421b70243bff0316e5e907d687f6ba834fc5740f6a08b0fddd4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:29:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 24 Aug 2021 18:19:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Aug 2021 18:20:04 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Tue, 24 Aug 2021 18:20:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb77d9d126f97898dfdc8b5fb694d1e0e5d93d13a0a6cb2aeda76f8635384340';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.2_7.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36ebe6c72f2fc19b8b17371f731390e15fa3aab08c28b55b9a8b71d0a578adc9';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.2_7.tar.gz';          ;;        s390x)          ESUM='fa3ab64ae26727196323105714ac50589ed2782a4c92a29730f7aa886c15807e';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.2_7.tar.gz';          ;;        amd64|x86_64)          ESUM='323d6d7474a359a28eff7ddd0df8e65bd61554a8ed12ef42fd9365349e573c2c';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 24 Aug 2021 18:20:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Aug 2021 18:20:48 GMT
RUN echo Verifying install ...     && echo   javac --version && javac --version     && echo   java --version && java --version     && echo Complete.
# Tue, 24 Aug 2021 18:20:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ef4df798b4c2b8982b7324e2b58a400cbac6d67fcc0325b60b63e8dc6638f0`  
		Last Modified: Tue, 24 Aug 2021 18:22:26 GMT  
		Size: 21.7 MB (21686255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e5ec72bb34bed2b4c27aca8c44962929a9f8f2616496438b978877085f8c39`  
		Last Modified: Tue, 24 Aug 2021 18:22:42 GMT  
		Size: 186.9 MB (186948199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ea965746b8367d71f11a1639554f868a7b11f1d61a743466d7f62e680c40c7`  
		Last Modified: Tue, 24 Aug 2021 18:22:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:16-jdk-focal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:54a5141e65918e3e47cdc6cde31ea3dbe59ef56981fddfdf9dfe892d93bd6f87
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226228411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa5ccca09f08a77cf102d67fb3c3c8b1011cf2be53df89a4c3514be3284513e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:12 GMT
ADD file:b8731edfdacfade2ec96757342f216962f3971b24077a9144da3f80003e6893e in / 
# Mon, 26 Jul 2021 20:55:14 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 21:19:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 24 Aug 2021 18:42:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Aug 2021 18:42:31 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Tue, 24 Aug 2021 18:43:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb77d9d126f97898dfdc8b5fb694d1e0e5d93d13a0a6cb2aeda76f8635384340';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.2_7.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36ebe6c72f2fc19b8b17371f731390e15fa3aab08c28b55b9a8b71d0a578adc9';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.2_7.tar.gz';          ;;        s390x)          ESUM='fa3ab64ae26727196323105714ac50589ed2782a4c92a29730f7aa886c15807e';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.2_7.tar.gz';          ;;        amd64|x86_64)          ESUM='323d6d7474a359a28eff7ddd0df8e65bd61554a8ed12ef42fd9365349e573c2c';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 24 Aug 2021 18:43:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Aug 2021 18:43:16 GMT
RUN echo Verifying install ...     && echo   javac --version && javac --version     && echo   java --version && java --version     && echo Complete.
# Tue, 24 Aug 2021 18:43:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:38800a0044dea146ca3c3a08bc2c9c956396ad3241a3c343010775650298c379`  
		Last Modified: Mon, 26 Jul 2021 20:57:03 GMT  
		Size: 27.1 MB (27149898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a6005406e4c382a54e411e8741f87860e0b7c77ce234b981ca75b873de584`  
		Last Modified: Tue, 24 Aug 2021 18:44:08 GMT  
		Size: 19.2 MB (19241237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f84cd17411ee41f6fbca0b35aab2d16177bd4e96184c618e374b0586125e17`  
		Last Modified: Tue, 24 Aug 2021 18:44:18 GMT  
		Size: 179.8 MB (179837116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97100c2b5f5b64533e47b14abfe81b21efc245d7cbe0ab00e39e91c5ffdf655f`  
		Last Modified: Tue, 24 Aug 2021 18:44:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
