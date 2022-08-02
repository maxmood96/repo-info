## `eclipse-temurin:18-jre`

```console
$ docker pull eclipse-temurin@sha256:5d4c4378839a22028c35f802acf17d03b38d52d5100e83cee7492917a62c6e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:18-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e9d7ec03909aed9733f9066e2975c508eb8a438d585ae588741e7725b2cc8da0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93741142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795ec7e02047a70fb159af700e6a829862bf5bf10894c701427ebe357c3ba8da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:16:52 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 07 Jun 2022 00:17:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cacb261967585ccd3eefe9a44f277b23aaa0b60772589ac220f03941c2bcdad1';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='24ec0eb692e30c7055cc863e4f47aa9cec2c069849f09b227adb14c87a70e8e7';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b43c2a662a88054886c7a89696248c0c99927fe97750c5e7690eddba4fb9645';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c9fb7c6fb110ad2e6ffaae9a8c3b8ea51098f98c60eaa1a0fcb0019c980227ab';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='67c2cea6040b12c125bb1bea74b3eeb42c94072713b152b720e50c897b946ffa';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:17:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:17:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160c99d3182b28de91f5c2c165e40fe309db075058fa23129c7dc2b4e2852b0e`  
		Last Modified: Tue, 07 Jun 2022 00:22:32 GMT  
		Size: 16.7 MB (16660695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358e5808f8143fe8bfe55618a647b0e32fe0f4b548ebc4fae8a186b91a87a5de`  
		Last Modified: Tue, 07 Jun 2022 00:24:50 GMT  
		Size: 46.7 MB (46656572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3925efda31eb84b767043ca2c9a07dba2ff36292466bd38486ad81d1d333153`  
		Last Modified: Tue, 07 Jun 2022 00:24:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:1aed3ed461234b133220dc13aedb39037f2bb6142a160831b353562ea0671700
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88147248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b43dda8f08a1a257a4aab40e7012bf73d8ed4e2f846e7caf757e60769d9ad1f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:51:35 GMT
ADD file:26c86cfcbc153addbca421974e648a7af07234cb3f741bfb030aa0db90b6a7c6 in / 
# Tue, 07 Jun 2022 05:51:36 GMT
CMD ["bash"]
# Sat, 30 Jul 2022 02:49:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Jul 2022 02:52:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jul 2022 02:53:59 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Sat, 30 Jul 2022 02:54:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cacb261967585ccd3eefe9a44f277b23aaa0b60772589ac220f03941c2bcdad1';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='24ec0eb692e30c7055cc863e4f47aa9cec2c069849f09b227adb14c87a70e8e7';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b43c2a662a88054886c7a89696248c0c99927fe97750c5e7690eddba4fb9645';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c9fb7c6fb110ad2e6ffaae9a8c3b8ea51098f98c60eaa1a0fcb0019c980227ab';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='67c2cea6040b12c125bb1bea74b3eeb42c94072713b152b720e50c897b946ffa';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jul 2022 02:54:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jul 2022 02:54:31 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5aeb313108e16ff98084efb2ae2830cbe915ea38b3e2fd1e32688dd9d8c11320`  
		Last Modified: Tue, 07 Jun 2022 05:56:03 GMT  
		Size: 27.0 MB (27017432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f87cf011b7201a432fd3e5af81c6bc43a001749514828e3740e9c6019d8e6b`  
		Last Modified: Sat, 30 Jul 2022 03:00:24 GMT  
		Size: 16.8 MB (16819353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd99430a9deb2bc59e380042069ca09fa96c201d948c21ea594dbef34c8305e1`  
		Last Modified: Sat, 30 Jul 2022 03:03:00 GMT  
		Size: 44.3 MB (44310303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de0f220f604b012e2c18a30319d98fc0fed8ec310c5fb0fd3309b908f8407b8`  
		Last Modified: Sat, 30 Jul 2022 03:02:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2b957337ef78423c340c93482640bcab5c5a081a78b88c1a4c31a57a5017c72b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92643556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc24ddb98b7c41ba832923033eda6b939e16d776ed61763e341b8fedc133d36f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:51:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Aug 2022 17:54:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:56:01 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 17:56:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b95934d11105c5a99a8bf087fdfc28a8a644b4265b6cf7518d70404a4dc82da2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        armhf|arm)          ESUM='bec2d075e81e4732835f71b7ea5c91b4a42e7b7d38b99ab845f76b421cc0b00e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_arm_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b084a373f3d4a8735f10a68cf2e73ff5c454162c62dd1bd268265b22ae1d8818';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67de23a526b4feda63d87dc57b6755beb997e3231017ab1cd70ef9193637979a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_s390x_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='efcfe9206ce467a0a197463283e74621f4ba037994d29606c572766945a01a91';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 17:56:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 17:56:58 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8576b6657b6f443770d5698f03730a1bd775828185316d3d49be89ae29eb2b`  
		Last Modified: Tue, 02 Aug 2022 18:03:57 GMT  
		Size: 18.1 MB (18093178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845cc3328f2bd5922d30627e5491348333ba59b5b195a842e7c8ab19302242a5`  
		Last Modified: Tue, 02 Aug 2022 18:07:09 GMT  
		Size: 46.2 MB (46169095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3e31e4505e683dc0856efd5b16726ee0fbe526c33780b7191152378b523cc6`  
		Last Modified: Tue, 02 Aug 2022 18:07:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:63be5190b685bf41d29407d57bdebd4a6f09e217e873b3057649e00232443476
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100068277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721542bee086286543f421489044ae8b8d54ed487d8f44064e8df894dafe1b94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:46:49 GMT
ADD file:62ec907c651e833838867bd541cf824f5f609ea4e2b19c4b26cec74a57b60470 in / 
# Tue, 07 Jun 2022 05:46:54 GMT
CMD ["bash"]
# Wed, 27 Jul 2022 00:35:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Jul 2022 00:42:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jul 2022 00:45:48 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 27 Jul 2022 00:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cacb261967585ccd3eefe9a44f277b23aaa0b60772589ac220f03941c2bcdad1';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='24ec0eb692e30c7055cc863e4f47aa9cec2c069849f09b227adb14c87a70e8e7';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b43c2a662a88054886c7a89696248c0c99927fe97750c5e7690eddba4fb9645';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c9fb7c6fb110ad2e6ffaae9a8c3b8ea51098f98c60eaa1a0fcb0019c980227ab';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='67c2cea6040b12c125bb1bea74b3eeb42c94072713b152b720e50c897b946ffa';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 27 Jul 2022 00:47:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:47:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b851cfa9fcbcb74629241502e21ebbae255fe40a2f26949573f278672b65c308`  
		Last Modified: Tue, 07 Jun 2022 05:49:53 GMT  
		Size: 35.7 MB (35717509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271d3996199a8c9ad9db4f7588a0b27613eb16f8a0ebaef74b5c3f327011070a`  
		Last Modified: Wed, 27 Jul 2022 00:56:12 GMT  
		Size: 17.9 MB (17867147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096118bdcfcf8a4344569f2cec218b9e61d1d7bd362d227069b9910ab97012ca`  
		Last Modified: Wed, 27 Jul 2022 01:01:18 GMT  
		Size: 46.5 MB (46483461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee06d1409afb87ddbe861e021a33a054f184781b862fd4398e7d344a5a95bc7`  
		Last Modified: Wed, 27 Jul 2022 01:01:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:2f003fcf7e13c1f6e11b3f000cf3a11032f57d8b91869ed0fb6ded9249beaeb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88521598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b1d110c3e71b3a858f4f16bc6ed8715fcaa7260895e792da2c0b66871fca90`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:03:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Aug 2022 13:05:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:06:45 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 02 Aug 2022 13:07:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cacb261967585ccd3eefe9a44f277b23aaa0b60772589ac220f03941c2bcdad1';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='24ec0eb692e30c7055cc863e4f47aa9cec2c069849f09b227adb14c87a70e8e7';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b43c2a662a88054886c7a89696248c0c99927fe97750c5e7690eddba4fb9645';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c9fb7c6fb110ad2e6ffaae9a8c3b8ea51098f98c60eaa1a0fcb0019c980227ab';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='67c2cea6040b12c125bb1bea74b3eeb42c94072713b152b720e50c897b946ffa';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jre_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 13:07:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 13:07:25 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4328fc07834dd0e146d74c56047ec3f1357f57d71002b6517534dce3f350cd7`  
		Last Modified: Tue, 02 Aug 2022 13:10:34 GMT  
		Size: 16.4 MB (16429583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4272695014cce2cb146b229f4f6880969429c5ba9120c69d29fbe44a4fc12dd`  
		Last Modified: Tue, 02 Aug 2022 13:12:20 GMT  
		Size: 43.4 MB (43449068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b389946462363af709e7651cedc6480295ea09b4b136505a63daa70d917cdb0`  
		Last Modified: Tue, 02 Aug 2022 13:12:14 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:4963636b46111cee32f693db1b19b206f987c1b29b004049bc3465259d96a178
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2375392154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cb76dc337fd62013a4eda8b99b2136ac0fc022bbb435312547803346ef0594`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Aug 2022 18:26:50 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 18:32:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_x64_windows_hotspot_18.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_x64_windows_hotspot_18.0.2_9.msi ;     Write-Host ('Verifying sha256 (5a29dbdbdfff80c24a02aa6ee239f36a1891efc4c07e80ebb238d2f9b6cdb0a8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5a29dbdbdfff80c24a02aa6ee239f36a1891efc4c07e80ebb238d2f9b6cdb0a8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 02 Aug 2022 18:33:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc14bd69273eb440f31c9bab8b8c19bdde6f079401e43e46ed1bce8dd0b6700b`  
		Last Modified: Tue, 02 Aug 2022 18:44:13 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9d664fe0f3fddedf27027c3966bc6f5f0ca4481e8ef8a9767f6f2a1ff66f05`  
		Last Modified: Tue, 02 Aug 2022 18:46:21 GMT  
		Size: 74.6 MB (74586526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab93292dbe7ad97048d503cb463cb95210ae8bbdd0297387f37fbe0b468b092c`  
		Last Modified: Tue, 02 Aug 2022 18:46:11 GMT  
		Size: 571.2 KB (571194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:bd16ccc8724e0ee7563b8ba1058b7f1b0c120422d0f41b4199b5b41c1ad93db5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2749584041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7660fadd67e923e229fc3d82a2487b097d6caa6a196c558d9cdf0eda153acb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Aug 2022 18:28:32 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 18:34:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_x64_windows_hotspot_18.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jre_x64_windows_hotspot_18.0.2_9.msi ;     Write-Host ('Verifying sha256 (5a29dbdbdfff80c24a02aa6ee239f36a1891efc4c07e80ebb238d2f9b6cdb0a8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5a29dbdbdfff80c24a02aa6ee239f36a1891efc4c07e80ebb238d2f9b6cdb0a8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 02 Aug 2022 18:35:30 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f4de99d54b8fbebc1ba4c25840e27b3a1810a5cdb487374ce99f80bca2e4ab`  
		Last Modified: Tue, 02 Aug 2022 18:45:00 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b47e27dbbfaccbd46afefd0c77d1f5f2ccb43b3e340f21b0d11476da80f81df`  
		Last Modified: Tue, 02 Aug 2022 18:46:41 GMT  
		Size: 74.3 MB (74335215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921dd0ff0a23caa6ce1dfcbb1ff8a5f88a87792e5f7d661b58d1512791748c48`  
		Last Modified: Tue, 02 Aug 2022 18:46:32 GMT  
		Size: 3.2 MB (3202244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
