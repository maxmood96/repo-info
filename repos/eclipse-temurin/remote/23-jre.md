## `eclipse-temurin:23-jre`

```console
$ docker pull eclipse-temurin@sha256:aab42cb3f1891d57885afb9f9c31ec3b93f31ca9cd4b0bffaeb0dcc0b62f39a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:23-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:03644f2a94bcc017c5f5de37f7ceeadcb6c889ef61e2fdeba6aec377a73c8ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95404801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa324d39c53181aff57d6a8f6206cee38fcaafe680b2763a33d1f77a4c1203a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:41:37 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:41:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:41:40 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 10 Oct 2024 07:41:40 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='ca32d942ef5357fb948604cd8aea5c597130cf7fdf6ddee267b4aa99406ee471';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143efbfcaac13674055c10e8665a69072b69f0cc821944cb8cfa950b1173d7e7`  
		Last Modified: Fri, 11 Oct 2024 23:59:09 GMT  
		Size: 11.8 MB (11844349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74687670489b75ea991e55594df259719830804428e858e63a223e0c1fbbf0d2`  
		Last Modified: Fri, 11 Oct 2024 23:59:15 GMT  
		Size: 52.9 MB (52944936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fce1bf4885c14cfa88d9f276152cc573316c1011dbe7d80581e18b48aa189e`  
		Last Modified: Fri, 11 Oct 2024 23:59:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfca803aa9cf908b769884adf58a684cd0e62926e150534903acf4341ef8e0d`  
		Last Modified: Fri, 11 Oct 2024 23:59:07 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:de4e0c38daf6f3b0fd7d5a9d1ebc6059a958ded726b567a5f7c84bd9f43972c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93755785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613e08fe1a16576f10edc71c29daef78046f6612ddd2f7419fc00c1b79fac62b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:44:36 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:44:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:39 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 10 Oct 2024 07:44:40 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='ca32d942ef5357fb948604cd8aea5c597130cf7fdf6ddee267b4aa99406ee471';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73a41b9ec5045d43aca85325c17ff1a8c4989befe3a53815e7de0ad5288d680`  
		Last Modified: Sat, 12 Oct 2024 00:17:24 GMT  
		Size: 11.8 MB (11835081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b23cb26eb236261da6ca52cae580ea8624196bd04919bf90eda4f7e57018f2b`  
		Last Modified: Sat, 12 Oct 2024 00:17:28 GMT  
		Size: 52.0 MB (51964881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda58a29c24f1bcf099d3c58c16b7ea215730ccc2d41d34b4dc89ec72790f06d`  
		Last Modified: Sat, 12 Oct 2024 00:17:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b78f6b652513480abbc8a21e5452aa5ee0c82de61b5b8c0b918bd9b160c8132`  
		Last Modified: Sat, 12 Oct 2024 00:17:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d84db1d4a9b6a764dd393b9adc6a00276eb10d1f5f5b610de1fd692c047e9178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100827557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e752156be3534ba1d7f07e86112efb22cbecc080215eab79eca1da0a0ba2a19`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:56 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:00 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 10 Oct 2024 07:44:00 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='ca32d942ef5357fb948604cd8aea5c597130cf7fdf6ddee267b4aa99406ee471';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:870d99e54f9cdff4b5ba4448d967491786519e8cbf54f10bd271e5dd32285ceb`  
		Last Modified: Fri, 11 Oct 2024 23:47:07 GMT  
		Size: 35.5 MB (35513269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eefa841b4f0b0157132a1ebae65ac01fd0b509625e0ca52ef15acabd835585`  
		Last Modified: Fri, 11 Oct 2024 23:58:27 GMT  
		Size: 12.5 MB (12491447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87df35aa2af02dc26602dcf8ee2ea076fe0b2db216659817ed306c9201ce610`  
		Last Modified: Fri, 11 Oct 2024 23:58:32 GMT  
		Size: 52.8 MB (52820603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ed324e10cabe514c10384bcac0f9310553bfd3b48704caa328fbcac876ac14`  
		Last Modified: Fri, 11 Oct 2024 23:58:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2d5db4c97346d7379120a4ef4c05263c3fa93c9333eb321060d9488333b83b`  
		Last Modified: Fri, 11 Oct 2024 23:58:24 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b8b5c39eaac50852a13a4d92e357c884fd3b56816edc29763fed6c63e6d65f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92262404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72716d47261ab7ba6ae890ad93210b08dc68062d5ac5204b181a0cf315c27620`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:54 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:54 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:43:56 GMT
ADD file:ed84c120e781b2f48856752e1e38d21db0bed5e09a2a64f961f004a4906abcb6 in / 
# Thu, 10 Oct 2024 07:43:56 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9c3c3d42ffb2603b328b7154fc9eb449ef87488b3cbeb24a497d46677c7fd44d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='ec45f4f9a4a98d8a0af24b508ca84a411ea88fac8abb8ad2cfca85cb3902ab5d';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='9120876c35b904ac041c5a021330a6f11d4e6c7537ce28bdbb7170b944673435';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='ca32d942ef5357fb948604cd8aea5c597130cf7fdf6ddee267b4aa99406ee471';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='b42ac56cfb90b313b73622221d8944d32996376d2d953e4ee3942439c5ce91bb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:220da50193dc0598aa4f0418f3c1f89ed396983e85b2032ceeac1e4e044e443a`  
		Last Modified: Sat, 12 Oct 2024 00:18:34 GMT  
		Size: 30.7 MB (30663130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ece7010ec7dd98b5d752684be3bbf2eeaa40efe0e35f9067c93a61aabf51df6`  
		Last Modified: Sat, 12 Oct 2024 00:27:39 GMT  
		Size: 12.2 MB (12157661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e622ff9c76c4ee3d2077e3d2430d9217ee4c9d6811338e2e7c9e5b62319d18cb`  
		Last Modified: Sat, 12 Oct 2024 00:27:44 GMT  
		Size: 49.4 MB (49439376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9824e13e3c1f332d2943a564d5284d813a24fa7f0705dc5f7ed9d02bad6280ff`  
		Last Modified: Sat, 12 Oct 2024 00:27:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67799044538578a3f931271b92b7eb5324aa73da85393ce1daec9ba725a88b`  
		Last Modified: Sat, 12 Oct 2024 00:27:37 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:cd56d3c703f5cb46051c34a80dc7f944fefec6abbc66aefb6294584123178bd7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883920228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9311583e1b279cf23ae929c929643a198358c73af1ddcd8218397eba8207e97d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:33:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Oct 2024 00:04:36 GMT
ENV JAVA_VERSION=jdk-23+37
# Thu, 10 Oct 2024 00:09:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Oct 2024 00:09:34 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd7a167e5d8024c2db3283a385811103c47c1e1349528ae29d41d1aa3117ae`  
		Last Modified: Thu, 10 Oct 2024 00:18:53 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b382d6d68061f3371be6f50b9b98bf213d56f8a3d84748b96d1d8aedb166a5d`  
		Last Modified: Thu, 10 Oct 2024 00:30:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aef43083ee1e4a5939751cf7b3d4adc773d8a823d14d6bb9426335411d02b2d`  
		Last Modified: Thu, 10 Oct 2024 00:32:18 GMT  
		Size: 84.3 MB (84289593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019529abf8d62745b83ef0ff9ad7b93e6f87043df0078e49adfb9fab478c00ee`  
		Last Modified: Thu, 10 Oct 2024 00:32:07 GMT  
		Size: 286.2 KB (286249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:debba9327e33cdef9f40d22ef164d9d5b6a69c15b9790eb2fa4937e1afb68144
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989926183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9960d107abe7f2b8993c125dd190202de5769397723a624a3790a6c5e7fba90b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:35:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Oct 2024 00:06:19 GMT
ENV JAVA_VERSION=jdk-23+37
# Thu, 10 Oct 2024 00:10:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Oct 2024 00:11:29 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71416d65806874920ade48cad9fe9e847b67ca207c59353ff136f87da9c117ce`  
		Last Modified: Thu, 10 Oct 2024 00:19:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ec34a182588fcd8627fb781040f6f0b5dd20245d43f68e2dfd39c36f5222d`  
		Last Modified: Thu, 10 Oct 2024 00:31:26 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e291b2b9ba443f9c3d4019a751a4907b67574009edcb7d6ba5f0785ebe396be`  
		Last Modified: Thu, 10 Oct 2024 00:32:37 GMT  
		Size: 84.3 MB (84301485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e122ae36365b54b24d5837484d177083685776c6d4ff8a6a51cc169d5da7588`  
		Last Modified: Thu, 10 Oct 2024 00:32:27 GMT  
		Size: 3.8 MB (3796618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
