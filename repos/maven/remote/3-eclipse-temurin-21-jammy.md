## `maven:3-eclipse-temurin-21-jammy`

```console
$ docker pull maven@sha256:b5496a26f9480872f09d06a23c1d69c278690f5f753edc9cb67b059661b529e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-eclipse-temurin-21-jammy` - linux; amd64

```console
$ docker pull maven@sha256:d55d030e13d560a75c7a75027d615af19b2f5fd757d79e2c2fc6e4ab2945d78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234885974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a9cec4ee7322f79c9e9542190c65a37fb34bf99f782d5a6c9f458ef12308a4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 21 Dec 2023 18:23:51 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 21 Dec 2023 18:23:51 GMT
ARG USER_HOME_DIR=/root
# Thu, 21 Dec 2023 18:23:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 21 Dec 2023 18:23:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 21 Dec 2023 18:23:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55658331de81e7dada3fa1214092b18d21c8d99da07608151a56009208f18799`  
		Last Modified: Thu, 25 Apr 2024 22:15:54 GMT  
		Size: 17.5 MB (17456385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8e686262e697325f0f35df9a25b11a02b8a1583f8fac33e913f4e2de5ed398`  
		Last Modified: Thu, 25 Apr 2024 22:17:01 GMT  
		Size: 158.5 MB (158512018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee9c63e92e8fde0c51fd3698e3c17883a90e9601b20f9508e2491f424858bad`  
		Last Modified: Thu, 25 Apr 2024 22:16:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbcba47533cf8bd48ce84f2866453bba90b2e3552d84f0302f90e1f68303dd`  
		Last Modified: Thu, 25 Apr 2024 22:16:49 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ee85b042a2bd870fdd5408ae8c5add90f715be2763e05c0b14d0e41412e085`  
		Last Modified: Fri, 26 Apr 2024 05:12:50 GMT  
		Size: 19.0 MB (18995625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e62130faccd617ae3688039608507a7c7ab06adbf1b81ca46027897daf098a8`  
		Last Modified: Fri, 26 Apr 2024 05:12:48 GMT  
		Size: 9.5 MB (9479945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9821bdc8d65877fe528e728a83af3bac8575863c426a321665fcfe7545f54e46`  
		Last Modified: Fri, 26 Apr 2024 05:12:47 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944041ac3797f0cfba9b33e669e5d33f7e035ee4393b4370fc2101b86df36113`  
		Last Modified: Fri, 26 Apr 2024 05:12:47 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7199066acb62a67676b1c668ed6cba135187956609bc81d00d27f062ca7df871`  
		Last Modified: Fri, 26 Apr 2024 05:12:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-21-jammy` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d3fd2654822a770c98e86623821289e4a0b64550fb775471927020599b3d3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232419296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6a7ac9dbf69e8f15a0131397aa2d02d3c10dafaceeb09cdf601ae8cc5505be`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 21 Dec 2023 18:23:51 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 21 Dec 2023 18:23:51 GMT
ARG USER_HOME_DIR=/root
# Thu, 21 Dec 2023 18:23:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 21 Dec 2023 18:23:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 21 Dec 2023 18:23:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0291b8882ad816d01ed9fd2230efc5c3ecf6b5ca8ea8ffb34837450d74db68f`  
		Last Modified: Thu, 25 Apr 2024 22:01:34 GMT  
		Size: 18.9 MB (18858662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3019c93f1cb3fe9002b9a8f1e1d38a15797ad2e4b19b775a6acbf0dba09de70`  
		Last Modified: Thu, 25 Apr 2024 22:02:40 GMT  
		Size: 156.7 MB (156672789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7f3c3e9756fb6f5edea609011d0e4f657b80a9880408c7296f4c61d8a43ec7`  
		Last Modified: Thu, 25 Apr 2024 22:02:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a25e90ee0ad6f4838a3869f28210a0a9d84f9e58fee64f3725fdf1299e14fe`  
		Last Modified: Thu, 25 Apr 2024 22:02:29 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bf682022b94f57fdae3f8680291415a54a61aae1e3dc40bff8e9daca293217`  
		Last Modified: Fri, 26 Apr 2024 01:15:36 GMT  
		Size: 19.0 MB (19004610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5c2ff61b886f54e238733958fe2026c32fc74a61a0ed1163764716b7049a15`  
		Last Modified: Fri, 26 Apr 2024 01:15:34 GMT  
		Size: 9.5 MB (9479959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a536dbafbb8264e7aafef345cfda85a4a95a6177f94f0d9c9a9a0020a1dec3d5`  
		Last Modified: Fri, 26 Apr 2024 01:15:33 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d907a34ff212e455d87e0bb889ee548185756c87cf190fb2244f13b0874e6ac`  
		Last Modified: Fri, 26 Apr 2024 01:15:34 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7169ab61c1ac4d49179b29753ca0d0a371d3ff1eb8520dbfad959410e362523`  
		Last Modified: Fri, 26 Apr 2024 01:15:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-21-jammy` - linux; ppc64le

```console
$ docker pull maven@sha256:97a03e5aaca651d54e139f87d305abeadecc7e34763d222f558a357c09eb7edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244629661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c801a45a56650fc45b3965c0c2496bfbfb5911555817028b4fd9232f7d136f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 21 Dec 2023 18:23:51 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 21 Dec 2023 18:23:51 GMT
ARG USER_HOME_DIR=/root
# Thu, 21 Dec 2023 18:23:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 21 Dec 2023 18:23:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 21 Dec 2023 18:23:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34360d55ae028192392c25f1a7ba3e34d2877f439114b2769039b5dfa13b9d`  
		Last Modified: Thu, 02 May 2024 01:54:21 GMT  
		Size: 18.7 MB (18722864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cadc60b2867a893cac0d973bf6c2cc7f91f01e77b8e7febfadc724000b38fb`  
		Last Modified: Thu, 02 May 2024 01:55:34 GMT  
		Size: 158.7 MB (158746526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404dda89117bad0eed86dec0bb4c10fd73e9f1c1ac681bb4f748b46a2d794282`  
		Last Modified: Thu, 02 May 2024 01:55:18 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2115b3de26a6ef13a2ebe010b5dba0ee52016123df044888237ce7d84995a6`  
		Last Modified: Thu, 02 May 2024 01:55:18 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f439a1183c63d59b22b886ce849730f21d0aa745d2011d68f392b83b931a11e8`  
		Last Modified: Thu, 02 May 2024 04:32:44 GMT  
		Size: 22.1 MB (22089535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b055bd1ae71749a445be204094dca2ebf854af19cbfea2dd23874bb6781d43`  
		Last Modified: Thu, 02 May 2024 04:32:34 GMT  
		Size: 9.5 MB (9479939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caa4a69f393e68fd6b3533d834f5db6fcd8e5e37908ccaf9f731328e1261b22`  
		Last Modified: Thu, 02 May 2024 04:32:33 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a049655231dcb2a5603acf8f64d5d1817fe4817554323c189cc9a6c721b3c200`  
		Last Modified: Thu, 02 May 2024 04:32:33 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe6d1bd1c6e7f8ac0dc9c447d29404ee01be0936cb29e017ff666701d72fa11`  
		Last Modified: Thu, 02 May 2024 04:32:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-21-jammy` - linux; s390x

```console
$ docker pull maven@sha256:e5ecb944ea152dd39a4e0b8d42eb752a73bcf263a8acf2c6dbffa525af272393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221585339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032aca72418c47c75d5f86adc207deb82d3770fd4ec19cfb1e346ff0d4058f4f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 27 Apr 2024 13:52:56 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:52:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:52:58 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Sat, 27 Apr 2024 13:52:58 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 21 Dec 2023 18:23:51 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 21 Dec 2023 18:23:51 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 21 Dec 2023 18:23:51 GMT
ARG USER_HOME_DIR=/root
# Thu, 21 Dec 2023 18:23:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 21 Dec 2023 18:23:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 21 Dec 2023 18:23:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ffda8878ec88daab976ebae63a8dc770c7ff669cb06828bf12b1a5acca67f1f8`  
		Last Modified: Thu, 02 May 2024 01:13:50 GMT  
		Size: 28.6 MB (28637522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9390685e0a430de7796df7df6993f29237307d1119a049ee83b14acf2ef63598`  
		Last Modified: Thu, 02 May 2024 01:46:04 GMT  
		Size: 17.3 MB (17259595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27989a70c2265779bd365d730189d760d09c9789fcc26bb5a790e62832787077`  
		Last Modified: Thu, 02 May 2024 01:47:01 GMT  
		Size: 147.0 MB (146982798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d927f73ab60e4c7b3be31ed9377c104ad06b1b443a6150a0cb3d916dbdec91`  
		Last Modified: Thu, 02 May 2024 01:46:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcbf13b8dc3ea41793044de92ff4a7e427b60ffc76a3cf6254b19713ec92c98`  
		Last Modified: Thu, 02 May 2024 01:46:49 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf61838d2465b716ba5b1f307cf7fb6b4977bc79ae29558d8855cfdc7b8f321`  
		Last Modified: Thu, 02 May 2024 01:54:59 GMT  
		Size: 19.2 MB (19223208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ead130e2cc48d5c3525beeebc0447c88448671ec2855f9a0ab54d5037c0bcf`  
		Last Modified: Thu, 02 May 2024 01:54:55 GMT  
		Size: 9.5 MB (9479944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef99a4aadf313b296e2a9b88c18ad69188572cb5a0b792ea1e1c4b9736c10f7`  
		Last Modified: Thu, 02 May 2024 01:54:55 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd95e4b5d987d4b7d9dd7f291e4ed6f09297d7c7c8e973c693d790d2eb6e71f6`  
		Last Modified: Thu, 02 May 2024 01:54:55 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26a37bdd0525aa7b787d9687013516ffeb5bb1f67fc1106ccd61487a1faf6e3`  
		Last Modified: Thu, 02 May 2024 01:54:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
