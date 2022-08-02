## `eclipse-temurin:18-centos7`

```console
$ docker pull eclipse-temurin@sha256:812f2c37115c21f87645207005fb7a9b7da0eef5ec3f34af50c8c3a24b91b86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:18-centos7` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f40f7d3f8e7b9fddf9bce69bf0bc025e76bce8349a4949140fb8dc1bef89693d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282347035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6b52e8d7af3284921cd9011910c56edaa21174f1a9e628163797eee25d737`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:51:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 18:53:12 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar binutils     && yum clean all
# Wed, 04 May 2022 18:22:11 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 04 May 2022 18:22:20 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='37ceaf232a85cce46bcccfd71839854e8b14bf3160e7ef72a676b9cae45ee8af';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7c3376b4eb14a58d27816776e965f1b214c17c4c2e918dc9e996a0f30e76550e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='16b1d9d75f22c157af04a1fd9c664324c7f4b5163c022b382a2f2e8897c1b0a2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 04 May 2022 18:22:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 May 2022 18:22:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 04 May 2022 18:22:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eafaeccaf7b18df74301fade3ec58483f58947f3a10bbc458aa7fe6e063d060`  
		Last Modified: Wed, 15 Sep 2021 18:55:36 GMT  
		Size: 12.7 MB (12704282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c49ae550ad023748a33008178e3e436db9cb98fc02e08fb6095bdbf13b607a`  
		Last Modified: Wed, 04 May 2022 18:25:25 GMT  
		Size: 193.5 MB (193545436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dc268afe1638c6f33b740285a46afdd40fc76c10cc035764851e058dfc063c`  
		Last Modified: Wed, 04 May 2022 18:25:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-centos7` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:51a0d20a79a680d80d6c48e7b2c91cf690e605121a3bf5311023d7e5e55f2b6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318849968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b0bdb3b9ff166fffad330046cd2d0458e75f8ea4579cc086d5bf6534d3787c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 14 Feb 2022 19:59:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Feb 2022 20:01:29 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar binutils     && yum clean all
# Tue, 02 Aug 2022 17:56:19 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 17:56:34 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='f4aca720bfcea4df7f02b59de1f68648632070c492f210b9e41e69170ee5e48f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4262677f8b6054d26f1c0042ac47dfbaab6a18d7dc73fa807b15ee03cdcbdece';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5e5dbf6f1308829528778e00631ec83e252d90fc444503091e71a66465e88941';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 17:56:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 17:56:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 02 Aug 2022 17:56:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fd0ac8e8fe7aee16a10c67c8c9c7b02a8102e7dd0f11573c3265a4f6803004`  
		Last Modified: Mon, 14 Feb 2022 20:06:08 GMT  
		Size: 18.0 MB (18047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4390f131c34734642bdedf4120bc90bae9b4456aa53d594e0310f970a7072e06`  
		Last Modified: Tue, 02 Aug 2022 18:06:28 GMT  
		Size: 192.4 MB (192427307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60e5c1adc1697cb67e9dbdc1844ca387a66486641ff0a71ce4fe7bfd6b40fc8`  
		Last Modified: Tue, 02 Aug 2022 18:06:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-centos7` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d6c42f2253614174d72680ae7c7a1f52cada28d9820000a1e6f82e0e5f7463bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292009789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5265f4d7f2c5763716c5cb769c017f04f1dd60612694a95fcb74c883b19ea9e2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Sep 2021 18:29:27 GMT
ADD file:7f21ae7d20a8e347d8b678bcf26be83abb1ee27d3b567c9cddd993e45ce8ac34 in / 
# Wed, 15 Sep 2021 18:29:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:29:40 GMT
CMD ["/bin/bash"]
# Wed, 27 Jul 2022 00:36:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Jul 2022 00:43:42 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar binutils     && yum clean all
# Wed, 27 Jul 2022 00:46:19 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 27 Jul 2022 00:46:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='37ceaf232a85cce46bcccfd71839854e8b14bf3160e7ef72a676b9cae45ee8af';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7c3376b4eb14a58d27816776e965f1b214c17c4c2e918dc9e996a0f30e76550e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='16b1d9d75f22c157af04a1fd9c664324c7f4b5163c022b382a2f2e8897c1b0a2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 27 Jul 2022 00:46:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:46:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Jul 2022 00:46:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3fe478aaff9b8f3ba958253e7339e9016ec07c075b805ebfc8cd372ddd01ee64`  
		Last Modified: Tue, 17 Nov 2020 04:06:20 GMT  
		Size: 80.5 MB (80516460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5339c61bbfec28187bc4e02f22d1dad7466fb40ff7376ff68c37fc72c000efac`  
		Last Modified: Wed, 27 Jul 2022 00:56:53 GMT  
		Size: 18.6 MB (18586903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646da3acb140478717207b8f38c0a0a984bae6ebb5f995466c56d6d103860e33`  
		Last Modified: Wed, 27 Jul 2022 01:00:27 GMT  
		Size: 192.9 MB (192906266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ecb37e78976e19822345b9b12daa83a6d5b9a210228d4d52ec293553e8e215`  
		Last Modified: Wed, 27 Jul 2022 01:00:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
