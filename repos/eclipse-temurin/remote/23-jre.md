## `eclipse-temurin:23-jre`

```console
$ docker pull eclipse-temurin@sha256:e3984f2382a0649aaf322388f8974ebe907ed48b15208c8251eae56c024cd643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:23-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2bbf2b6a5e929c699c09fc4f01cc5cab8707d950441db9aa40e7d445c69d14da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97806156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dc36b25bcf2810fbbdbd0d785166d510073f0380de4e5946bcbd3046460483`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
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
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7733983173882f1481b4c6868b5b01adf3d7c0de7467b266d1faccec4b10303`  
		Last Modified: Tue, 17 Sep 2024 01:13:05 GMT  
		Size: 14.2 MB (14247394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856dd5e9df3f976cd99fd94c8d8da9d65c6e3fe8fc5dc5f551b4a391df075633`  
		Last Modified: Wed, 18 Sep 2024 21:25:46 GMT  
		Size: 52.9 MB (52944977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3509702a2d12bd42ff8361f73e6127801ae6f57ab6766199063e46db0d6464de`  
		Last Modified: Wed, 18 Sep 2024 21:25:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46868948c5b682b4253673bf23eefd44acc1e04dee7e0a004e34beffae2b26c6`  
		Last Modified: Wed, 18 Sep 2024 21:25:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:cfe852cfe3d6768d71147b0b36a3b5e9c7af71fb9010a3d873ae70c9699733b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95973279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b4b31c4ca1ca2575b1db285ebd7fc6a58c9df967dd08027dddcfb2d1bae0db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
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
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6a44bd3a962d8581d46ba26e118a19cb4d4b06188d2b8ab3440e28411f3235`  
		Last Modified: Tue, 17 Sep 2024 01:42:29 GMT  
		Size: 14.1 MB (14052969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c370ed45c298a6681bb202d8b90bd48bac74953ff9ce84ac0af9c8166d51d9`  
		Last Modified: Wed, 18 Sep 2024 21:44:12 GMT  
		Size: 52.0 MB (51964867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba0cf590469b6f82c6811a3f5344b786f567c8d1c1675ef1e4406d903715785`  
		Last Modified: Wed, 18 Sep 2024 21:44:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917e132d40aadc357b2decc469f7ae9b6aa51f10499ff19cba85339599596149`  
		Last Modified: Wed, 18 Sep 2024 21:44:06 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:0f3069c54d648fce491a9674f97e16a3c603baae06600f5e4d27a50a174864d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103452864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81e8388844adafd3f9fd652276e7f4f292adefebe7329fbfbf6ded5b11cd48a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
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
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394082a78f48228823aeb6e88b5f3c54eb90d4d6a362d9dbd546943d2f05d830`  
		Last Modified: Tue, 17 Sep 2024 01:12:17 GMT  
		Size: 15.1 MB (15111829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ba77700fcb68c12d4d3afa03a76197c8ab70715395eb1875c70efe4a0ede88`  
		Last Modified: Wed, 18 Sep 2024 21:22:14 GMT  
		Size: 52.8 MB (52820617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f777746bb0c14c75c3384b2f4b3c4154f0c68e7b78ed11c5090d377b868017`  
		Last Modified: Wed, 18 Sep 2024 21:22:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8543c08c9ebec0717b6581a8872299835b24d1af83042d0160f546f95bf9447a`  
		Last Modified: Wed, 18 Sep 2024 21:22:05 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f5eb5db6253d928599c74e51488512f3f2134756cbaa00d65d840d98ec617ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94355060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54519e7dc80175f5c1df7aed2d81f30415bba1dc1ab50394feabdead4b0713e0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
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
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c820efbcad1839fd235de65a7456aaba01330c07cdb1391d67a1c6229c24b28d`  
		Last Modified: Tue, 17 Sep 2024 01:42:36 GMT  
		Size: 14.2 MB (14248048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cd28e4fe79a5e8d5fa5a6c0ae0f014fdf1096755b28237887c829d07d2d92d`  
		Last Modified: Wed, 18 Sep 2024 21:48:21 GMT  
		Size: 49.4 MB (49439383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebd936bdea76cf2c9c36f220591517512e3df841ff1f6b9bc43809b14bb4c56`  
		Last Modified: Wed, 18 Sep 2024 21:48:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdb17fad59effee5cc56bc3cef54cadc8a4b03235ba9f73af0b196ae1f3f736`  
		Last Modified: Wed, 18 Sep 2024 21:48:15 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:67d2522b0da885b286e7e4509ca1fffb2b60d3dcbb821f7fe71ec3a577d83321
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1546623427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ceac92bcf3e7bb752c6144c1d53e85ebae491ba50565b8321c96f7dcd473e16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:35:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Sep 2024 21:17:40 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 21:22:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 18 Sep 2024 21:22:38 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0ff9a79ca5aec0b3e3be0c49c873a237847a9d74342acad1818e3f10647107`  
		Last Modified: Wed, 11 Sep 2024 01:13:29 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e7842774e6f3b7aa5d5da5f10556d5ee58d2ed3bcbaf492d583620158d1f45`  
		Last Modified: Wed, 18 Sep 2024 21:27:11 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd4000708c52382caea0488cc0083bd49cd714e3b94aaedef06cef6c3c1f59d`  
		Last Modified: Wed, 18 Sep 2024 21:28:40 GMT  
		Size: 84.1 MB (84149353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b826d21b0c8c196c18cee6b8e93ec8589bb2d8081c467832cca025b1e44a8b2`  
		Last Modified: Wed, 18 Sep 2024 21:28:30 GMT  
		Size: 278.9 KB (278853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:fb65962b38d03a252fc1bb65bee558477de7a1725c82e42d4aa9b74f02100adc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1808264300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2ac033887abd56626bbae5020c8ce118819c8d21337be8e139b7dd7fb15ba5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Sep 2024 21:19:38 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 21:23:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 18 Sep 2024 21:23:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b681a22e2ab818abdc55dff7075266cbdad9e0c1d79f16a962cabde9559b4bc1`  
		Last Modified: Wed, 11 Sep 2024 01:17:09 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192c9af22a70bd2ee1407e227c80f7c4934714b6d6214e1008bb26b348abea39`  
		Last Modified: Wed, 18 Sep 2024 21:27:50 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee82905aaa1094f1eb535b100b92e463b3af0cd4c3e41322799e86c24b1cc7d`  
		Last Modified: Wed, 18 Sep 2024 21:29:00 GMT  
		Size: 84.2 MB (84177038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088e7e826ce6bf938d80ecb1802d1e7f6828d5e297baf7bdac127ff39d36206b`  
		Last Modified: Wed, 18 Sep 2024 21:28:50 GMT  
		Size: 3.8 MB (3816085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
