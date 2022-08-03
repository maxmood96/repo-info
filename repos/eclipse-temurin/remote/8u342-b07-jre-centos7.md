## `eclipse-temurin:8u342-b07-jre-centos7`

```console
$ docker pull eclipse-temurin@sha256:97da5e36ae3ab99f622539f6ddfda93a9380bc39f3bf7648c6637f39ffe62a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u342-b07-jre-centos7` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2d007fa01d7cfae075842bbcfe01f1bb78186626ad1378e2c7d540ca3d0aafa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130610031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a068c8981b25f9f735235017fc87acbe9f506317002ca162fd8ea924c4ec1a21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:51:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 18:51:48 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Tue, 02 Aug 2022 19:06:34 GMT
ENV JAVA_VERSION=jdk8u342-b07
# Tue, 02 Aug 2022 19:07:08 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7e6cb9ee2bbbc1b960e5e443fe7e6145a46e06678b6d0b0683fd4996d40c8fcf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u342b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='d27ef577eaa68aaea944bfc6c8d695b2b0c770a26116b9977d54025265f1756b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u342b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8362dc39dd92faff221c7ca314ed2ff289c17e1447cd2ed01f3b8541c9f1e9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_linux_hotspot_8u342b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 19:07:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 19:07:09 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df6893209e3a4a16d453c0b998ba34f62067ad6099b971afc4f30040eb1467d`  
		Last Modified: Wed, 15 Sep 2021 18:54:13 GMT  
		Size: 12.7 MB (12706445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711ff4f19b55583c6b9ead32a8acbc3f9002eba3c7210a23be935d39f9baa7f1`  
		Last Modified: Tue, 02 Aug 2022 19:15:09 GMT  
		Size: 41.8 MB (41806269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f4d68108d1cc81c8e1ff7d7294f74a9cb25df5ced172026b2fa7591a88eb9f`  
		Last Modified: Tue, 02 Aug 2022 19:15:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u342-b07-jre-centos7` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ad25eecfd7dc3734572c3288892b72c56a210f233d70b62f1a751220f94f34fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162232807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b572ed5ffc15ccf9caadeea25a7ded7d6170ed1ea07ded3e62c8a4ad8e147255`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 14 Feb 2022 19:59:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Feb 2022 19:59:30 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Tue, 02 Aug 2022 17:52:01 GMT
ENV JAVA_VERSION=jdk8u342-b07
# Tue, 02 Aug 2022 17:52:42 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7e6cb9ee2bbbc1b960e5e443fe7e6145a46e06678b6d0b0683fd4996d40c8fcf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u342b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='d27ef577eaa68aaea944bfc6c8d695b2b0c770a26116b9977d54025265f1756b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u342b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8362dc39dd92faff221c7ca314ed2ff289c17e1447cd2ed01f3b8541c9f1e9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_linux_hotspot_8u342b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 17:52:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 17:52:44 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130170151f9f3710dd5b3e651dfb953b4ced0d33d1b4c77d70c35bd91d07e040`  
		Last Modified: Mon, 14 Feb 2022 20:04:32 GMT  
		Size: 13.1 MB (13059526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ed3f484fe0c5406f1b2b75adec74749790875cc4d2478c884dacaafe83992d`  
		Last Modified: Tue, 02 Aug 2022 18:01:29 GMT  
		Size: 40.8 MB (40798208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61345af38d52a31d1331251dad06be4b18643f98ca67de1113f23712f8cfe70c`  
		Last Modified: Tue, 02 Aug 2022 18:01:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u342-b07-jre-centos7` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e4cfe4fd3f71fab7cd4d0564188ee606fe05db7c6dbffccc442eebdae53ed160
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135241367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec7365b7e3238a128f65a5a6cc7ff08cf1b453fa1d1f6dc78d59c971c8bb9de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:29:27 GMT
ADD file:7f21ae7d20a8e347d8b678bcf26be83abb1ee27d3b567c9cddd993e45ce8ac34 in / 
# Wed, 15 Sep 2021 18:29:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:29:40 GMT
CMD ["/bin/bash"]
# Wed, 27 Jul 2022 00:36:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Jul 2022 00:37:19 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Wed, 03 Aug 2022 03:22:18 GMT
ENV JAVA_VERSION=jdk8u342-b07
# Wed, 03 Aug 2022 03:23:23 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7e6cb9ee2bbbc1b960e5e443fe7e6145a46e06678b6d0b0683fd4996d40c8fcf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u342b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='d27ef577eaa68aaea944bfc6c8d695b2b0c770a26116b9977d54025265f1756b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u342b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8362dc39dd92faff221c7ca314ed2ff289c17e1447cd2ed01f3b8541c9f1e9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_linux_hotspot_8u342b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 03 Aug 2022 03:23:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 03:23:26 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3fe478aaff9b8f3ba958253e7339e9016ec07c075b805ebfc8cd372ddd01ee64`  
		Last Modified: Tue, 17 Nov 2020 04:06:20 GMT  
		Size: 80.5 MB (80516460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d09697c3a630c35e8d45ccb0233578c9ad68f0448605800b3e2f3c500fa3a5`  
		Last Modified: Wed, 27 Jul 2022 00:51:05 GMT  
		Size: 13.5 MB (13509908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bb72c2021e009ad464cd806d0962afac78e00c2c605d323414dbd42ff06732`  
		Last Modified: Wed, 03 Aug 2022 03:35:53 GMT  
		Size: 41.2 MB (41214838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f5916e22ed2d2d9d73a815fcd62c76109cf87bf0669722647a880db59357fe`  
		Last Modified: Wed, 03 Aug 2022 03:35:45 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
