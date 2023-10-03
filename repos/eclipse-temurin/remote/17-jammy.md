## `eclipse-temurin:17-jammy`

```console
$ docker pull eclipse-temurin@sha256:892d2ba323635bfb5ccdc60bf355612959c3e11fb131ed461d0f6f147ff42c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:831f00e903bf888787b8ffd1bf5252e5903e1b19d5bc17f7e5b9761ffec11785
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192675638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034a1f9b6fb7cb9281a0243eada42f33572c4024f8e1e716e0e4a7d24735ded`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:11:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 05:11:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 05:11:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 05:13:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:13:30 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 05:13:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 05:13:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 05:13:41 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 05:13:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 05:13:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e560b9ae2a605cbabd174647e334b0807409ab4cdb14e3ffa28655f8e033811`  
		Last Modified: Tue, 03 Oct 2023 05:17:36 GMT  
		Size: 17.5 MB (17455429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a200e428b29b17c8b134286a64173f5831f00680858051961b5ca7505306d59`  
		Last Modified: Tue, 03 Oct 2023 05:17:45 GMT  
		Size: 144.8 MB (144778433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc43ecfdc127e5008009135350763c92b0750409668ab2304125d4e657891ef`  
		Last Modified: Tue, 03 Oct 2023 05:17:34 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef680a12b1abdae0115a150b78eb9007d4d676c8bd48ddd8a63b50a1f58df57`  
		Last Modified: Tue, 03 Oct 2023 05:17:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jammy` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:990b43cdb34f4531c78293a1521fb29cc583da031e129c594e1f1d0e67872c57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187167877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0c2ed29835aed21c03d76f0bc855fd375d763b51f512ff930daf689c8aead7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 25 Sep 2023 10:19:15 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:19:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:19:18 GMT
ADD file:0008d56422c09f73afbcd40ace46d311e36ba0d60eef05198ea3665172ba3433 in / 
# Mon, 25 Sep 2023 10:19:18 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:00:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 06:00:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:00:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 06:02:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:02:50 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 06:03:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 06:03:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 06:03:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:03:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 06:03:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7271b2c80df6c73d794550b50f57d78c6fd5b85da7934c6506c76ea706087280`  
		Last Modified: Tue, 26 Sep 2023 02:07:56 GMT  
		Size: 27.5 MB (27515498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a42f949007cfbde4e09ba505ced26b019abd8a7ea5591c2ee0c80fe213191ee`  
		Last Modified: Tue, 03 Oct 2023 06:05:16 GMT  
		Size: 17.6 MB (17587273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8cb2c36aabb6e51e5cb39d9ab060ca54e69d03596ee2fb3f3a2013aa6949b`  
		Last Modified: Tue, 03 Oct 2023 06:05:26 GMT  
		Size: 142.1 MB (142064196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f283f5a680dae88eb915b9ed36820132a65dd6d02068dec9c2217211bf3600a0`  
		Last Modified: Tue, 03 Oct 2023 06:05:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb39d0c5347dc505dfd2a2b89a3972c4c610328559f92df055be0d6d90b5ef`  
		Last Modified: Tue, 03 Oct 2023 06:05:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:767d2f0b7457816b3a15f414e0074afb3d00e4673b1d358eb4f05dc9606f6226
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190806534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0e6ccbbe6c397d955d222398c6a91d26db24f1931051680db5a35bce2adc13`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 06:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:06:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 06:08:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:08:17 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 06:08:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 06:08:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 06:08:29 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:08:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 06:08:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba2aefbab3334adfc4bfa89dd448c89bc452ab89a02053172fb42a8e5288ba3`  
		Last Modified: Tue, 03 Oct 2023 06:11:30 GMT  
		Size: 18.9 MB (18859718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753b98fc35cd82fe89ecc7d11b833688e92102be27567d036bb1ead5eec98ed5`  
		Last Modified: Tue, 03 Oct 2023 06:11:37 GMT  
		Size: 143.6 MB (143553841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e5167f5e56a4dc905a342ae65372a5b2d6d6947e1d47086302582aa91263e`  
		Last Modified: Tue, 03 Oct 2023 06:11:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580f4b189461fdb8b41219e07a2c3ea5531b35d7e2b6e4768a911c12cff95029`  
		Last Modified: Tue, 03 Oct 2023 06:11:27 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f4c01d29d0250f23f15c9ce9dc015ca9aad2fda5135d1bd14c176680f6949f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198932453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa8efdb6ab2cbbe6c58b80714986e24daf520e1ae06d85468527ede07b3d4f9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:03:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 00:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:03:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Sep 2023 00:06:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:06:41 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Sat, 02 Sep 2023 00:06:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Sep 2023 00:07:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 02 Sep 2023 00:07:06 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Sep 2023 00:07:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 00:07:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d4cfc5435802883c4aaa9fa4afcc1b07f40e20bee68f058f0671804ab6bc3a0`  
		Last Modified: Sat, 02 Sep 2023 00:08:58 GMT  
		Size: 35.7 MB (35705651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cf6ea565778c3d8bea7e7e22e09a388b4e63b84893d5323563a7fb240485b0`  
		Last Modified: Sat, 02 Sep 2023 00:10:54 GMT  
		Size: 18.7 MB (18729609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bddb39f1fdebd321ac34b576c330189814a27282229b9a65e6090dcd830d1aa`  
		Last Modified: Sat, 02 Sep 2023 00:11:10 GMT  
		Size: 144.5 MB (144496286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba63aa3b50c517e5c94403858edd5723610014d8e77aa42bf4074dca90472cc`  
		Last Modified: Sat, 02 Sep 2023 00:10:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5ef12154e6821f7d55d5adce4cad445dda959f09ff3ea3ce077a0cd73792e`  
		Last Modified: Sat, 02 Sep 2023 00:10:49 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jammy` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:8e7f581f483098f79906dc7720e4b50b7488a329bc2843f1b70ebfcfc61b0263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180119822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0dae89c0c221a294a050d6a199f705b6693f4e27539b1f1bd4c38b84eacb78`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:26:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Sep 2023 23:26:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Sep 2023 23:26:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Sep 2023 23:27:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:27:38 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 01 Sep 2023 23:27:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 01 Sep 2023 23:27:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Sep 2023 23:27:58 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Sep 2023 23:27:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Sep 2023 23:27:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e19a32372cc8a39496c7cbc80d6c7213997c1b24d50309e770a59738f35c719d`  
		Last Modified: Fri, 01 Sep 2023 23:23:30 GMT  
		Size: 28.6 MB (28645834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351bc6a2ce88dd5072fe74c40fe5a76147b4c44751fb62974f74bd1eaf40aafb`  
		Last Modified: Fri, 01 Sep 2023 23:29:38 GMT  
		Size: 17.3 MB (17255550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2df682594d614eb39c1767c08d3e9078d528d8cb5081c9a171697a348eba5f`  
		Last Modified: Fri, 01 Sep 2023 23:29:46 GMT  
		Size: 134.2 MB (134217531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb71f98547ff743cd9301ebc43f5b154f089311a93e15001e8c271c703d0e9d`  
		Last Modified: Fri, 01 Sep 2023 23:29:36 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad043f6fb7f10bf8558dfa3cadfe771b6b9ba06e096352d274ccb2bcdd9019b`  
		Last Modified: Fri, 01 Sep 2023 23:29:36 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
