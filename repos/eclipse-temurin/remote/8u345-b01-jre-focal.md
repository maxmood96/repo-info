## `eclipse-temurin:8u345-b01-jre-focal`

```console
$ docker pull eclipse-temurin@sha256:818c2e67d7c83b30aa1ca5683adc41823287a34a27b41be594e7720246d84f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u345-b01-jre-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e4965985a370d89aa118c36d6e53301cf5ae084d1b0d1b272179fee7104d5c20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86752047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4b30ba8416d52a1a7383b52508c843275d97ff3e8d6bf2875f9f482f996147`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 19:19:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:19:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:20:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:20:21 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:21:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:21:38 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc2312f5e68afa6ded43a60d337b515cef59842d8cf965c44d959c3fbcc1648`  
		Last Modified: Fri, 12 Aug 2022 17:28:10 GMT  
		Size: 16.4 MB (16370849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d77544238d4a99d811ce649d3356c4b5a267ef841c66b12177776a559cfff15`  
		Last Modified: Fri, 12 Aug 2022 17:29:17 GMT  
		Size: 41.8 MB (41808442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff36f18d9f2504c55366be1350eaa96ca7132ba52c480bfd8339d2d0d04f1894`  
		Last Modified: Fri, 12 Aug 2022 17:29:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u345-b01-jre-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:268920394a97903ecdce4433c69408f05725c3d8710b7d76727968b3f1d827f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79326650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cda20778cd72c3a7e9c1c5813b9b79ebaf3d2adf11eb13d03cceaad298c027`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:57:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:57:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:57:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 16:57:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 16:57:55 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 16:59:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 16:59:06 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fac9c53b2f58de4f435c8c3bf1b4f37d34bc505b27a9b855c3de5523784c3a`  
		Last Modified: Fri, 12 Aug 2022 17:06:05 GMT  
		Size: 15.2 MB (15197069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8547d0a1f0a449ec8367201eb5523ad704961a15f543fe3ca5f2b89c87af0ce`  
		Last Modified: Fri, 12 Aug 2022 17:06:59 GMT  
		Size: 39.5 MB (39540148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c6968629ddba8781ed4c69e3c4aab7fff4477fb6268780111c252e08d8573`  
		Last Modified: Fri, 12 Aug 2022 17:06:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u345-b01-jre-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ce7ce8391247ef1a19123c32bb31e9a5739ed686593e3702b2402b2ca0315f0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84230435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d9062d1a28c58a0ef05d3b4aabb17e8026f14ae93f596e25e44aab6ef6ce7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:40:12 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 12 Aug 2022 17:41:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 12 Aug 2022 17:41:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5306171288e9c45d43fbb0a459aefe6b98dfa4755c0799ca2eade2326d39d45`  
		Last Modified: Fri, 12 Aug 2022 17:51:06 GMT  
		Size: 16.2 MB (16234664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3500e78c5eaeb95acc671408bfe18944946e5015a4a0cfb5b9bc91ef0db6a03`  
		Last Modified: Fri, 12 Aug 2022 17:52:21 GMT  
		Size: 40.8 MB (40803839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7dc4c61eb8ae3204b54587cb0bf87dd1773639be52dc637a2ee46557bba1d`  
		Last Modified: Fri, 12 Aug 2022 17:52:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u345-b01-jre-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d5d32a8cd1188a8a81d4b34affdbd6f2167579cc4c14741dea918d728a0029fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92082122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b8a10214e02d0a8ac7144f06568dc71ab6ce189041b70eb530b846a6e1072c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:54 GMT
ADD file:eb82827919ea73f9595d7b0b70fe9aa5ff23e16ea6a87f7f9ef4e1905857b789 in / 
# Thu, 01 Sep 2022 23:49:56 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:00:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:00:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:00:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:01:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:01:23 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Fri, 02 Sep 2022 04:02:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Sep 2022 04:02:48 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:891f6400ce611ee5975f04ad6d2c68305c76a8628b846df1b1f9ac7c45b1311c`  
		Last Modified: Thu, 01 Sep 2022 23:52:11 GMT  
		Size: 33.3 MB (33295624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1ac4dd8cb9b2b85d5f08f192b8d22024b1e070f6a40bb2e3220d3911ba9d39`  
		Last Modified: Fri, 02 Sep 2022 04:12:41 GMT  
		Size: 17.6 MB (17591088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe7e836dd4dbd4606b163cafa9d05d98a4ca6cbf314f40ca251424606d88871`  
		Last Modified: Fri, 02 Sep 2022 04:13:41 GMT  
		Size: 41.2 MB (41195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65a23c54dbeab253496fe4334fdab22eda0e617f259214222b23a7cab058652`  
		Last Modified: Fri, 02 Sep 2022 04:13:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
