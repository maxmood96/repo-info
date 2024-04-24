## `maven:3-eclipse-temurin-11-focal`

```console
$ docker pull maven@sha256:23fa84eb16e49c1c106047a4479df6c3d889e76325a164011a8aff269787c11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-eclipse-temurin-11-focal` - linux; amd64

```console
$ docker pull maven@sha256:6de5c5ba959d3d0d60334147084cd97ab1695036eaf2d1178104e07e099e60bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228636634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958cff48e8a89343498f5aadf336cd25d4205ef641c0ec7be5f883df2fef534`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf168757422d85fc784edd9f8eab4082cd0da552a3faa4294d478d5faf0594d`  
		Last Modified: Tue, 16 Apr 2024 04:03:22 GMT  
		Size: 16.9 MB (16920620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2188129ff30b4265f5b264e6dd755578df2f8a9604a5a7784e867a43a2ad72`  
		Last Modified: Wed, 24 Apr 2024 19:10:21 GMT  
		Size: 145.5 MB (145507634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9c4849de3ade9e4dabc060b78b95bd709e43375d8cbf1ffb0cda63739df0e1`  
		Last Modified: Wed, 24 Apr 2024 19:10:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e082f9e9fc92c1020dfb472e6186aed4764a0a15131f21c215689f6a3c341c`  
		Last Modified: Wed, 24 Apr 2024 19:10:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecaab9caca8d8ec1725652a9abfd83f9a98e6fa9a10dfc4e0916d64951344ff`  
		Last Modified: Wed, 24 Apr 2024 22:04:12 GMT  
		Size: 28.1 MB (28141649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b9a1189739efafb176cca26c8b254ef3a549019efd7797a4ec95a65c6da9be`  
		Last Modified: Wed, 24 Apr 2024 22:04:08 GMT  
		Size: 9.5 MB (9479945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a8fe7d79f1316955fd6b7498a7dd93246b2f4dd6a8d23c0dc91130dbc72555`  
		Last Modified: Wed, 24 Apr 2024 22:04:07 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e286ace524d6f02362cd3143912206e1b23881bfc614d5b9146e6327a554d5`  
		Last Modified: Wed, 24 Apr 2024 22:04:07 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5159e8dfaacf8e003e98bfa1d66adc2cb72ebe714dae363d1f178936d553219f`  
		Last Modified: Wed, 24 Apr 2024 22:04:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11-focal` - linux; arm variant v7

```console
$ docker pull maven@sha256:a81921777666d148705c70601ffc6cb1daddcf3e570debdfede4a7deab0ab2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212576300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f91bc26c2a214a782986f2f9f5df59ae94c3879cde444661702740245c7668`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d12b682cbcc5b59bbe1432d30883570b4dd781fd2260db8ec9fc50b11db15d2`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 15.7 MB (15664712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49790c1f0e7e7802115c00f4d9ffc31865449c887a140eb6b9c3a5d73e8c4980`  
		Last Modified: Wed, 24 Apr 2024 18:13:51 GMT  
		Size: 138.0 MB (138005747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e843ccabf9623cf1c02cd0f2723e455ce1778d22724df834d16bfdd9b53e87f`  
		Last Modified: Wed, 24 Apr 2024 18:13:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c49cf56f4c79acaa8b195a12b07ec063ff25bfab73c57e5e1f151238a448d`  
		Last Modified: Wed, 24 Apr 2024 18:13:36 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba46348cdf1e2f208700d385afdefe9e866c0ba77496fa96f9a00e986493d7b`  
		Last Modified: Wed, 24 Apr 2024 18:42:31 GMT  
		Size: 24.8 MB (24820998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1500fa6a693d4f9c641db34ef7c185ee4f2f04c14146fb894e8facaa3dd51b`  
		Last Modified: Wed, 24 Apr 2024 18:42:28 GMT  
		Size: 9.5 MB (9479937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5752541883e618d10f173bc0f1ea62eae81484ef8febc223525982f98757c3c2`  
		Last Modified: Wed, 24 Apr 2024 18:42:27 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1159f3835d3dc15ed2a92d9a7ed27df4dcb3b4033623bcda5c173608faca24`  
		Last Modified: Wed, 24 Apr 2024 18:42:27 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e22720afc16d2a8d5946a6e921e11ce097c1bd7c643c7c4227f3d416057df4`  
		Last Modified: Wed, 24 Apr 2024 18:42:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11-focal` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d144a8734aa2fb23b680d0b94ffefdbef572ae3f30894a02b42fb1092c374ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (223964881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4322f190963ac6727486aab052a7bd26fabe2b7d97e2245c155eb11ee1828fe7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2f0d048c4dc921b108e92215dcba18b91b316fdaad6521463665d94fdab64c`  
		Last Modified: Tue, 16 Apr 2024 02:55:17 GMT  
		Size: 16.8 MB (16777181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601d897de74ebfb58425587a54a3f97e66b6ea8f34ce6e45656f8191b0290926`  
		Last Modified: Wed, 24 Apr 2024 17:55:51 GMT  
		Size: 142.3 MB (142314441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1e9a5e7a96647a1f8061a63dcdd4feae1a09cd6a84f0c3c4ecb3f03773b9f0`  
		Last Modified: Wed, 24 Apr 2024 17:55:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad23767a4d80722952294cb8053d79f23534c297194c813ddf2541b9b23a1d2`  
		Last Modified: Wed, 24 Apr 2024 17:55:42 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00248b15e000027ad73d651fa2b72bb817ff81503feab92fb1d05bd4ab2f9ea0`  
		Last Modified: Wed, 24 Apr 2024 18:55:37 GMT  
		Size: 28.2 MB (28186047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfaf52b4b9638cf197f2cdca5b595cb3dd89518b94930c1b0d5a365f66589d9`  
		Last Modified: Wed, 24 Apr 2024 18:55:35 GMT  
		Size: 9.5 MB (9479950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5b63c8b2199232a60d5ae54ad5183a2ba602af8c8fe44f83a0a69b8b1b7334`  
		Last Modified: Wed, 24 Apr 2024 18:55:34 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a1c40c7d860bb9582c1b05a904289bd874e87f5dfe6c58e0efd30ae3283b9e`  
		Last Modified: Wed, 24 Apr 2024 18:55:34 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267c6f748b5cf308d34f254fcec77d593d02b9aae7140c282fd08dcdb61301a2`  
		Last Modified: Wed, 24 Apr 2024 18:55:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11-focal` - linux; ppc64le

```console
$ docker pull maven@sha256:c5d7a83cbc3840efc877ab9d3ec5699f4d4bc6be51c7669bb346b395304e38e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228234417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47587cd32cca9167859a869a24bee4d46e5c7c539f626c7701bb33df9a11fe61`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 19:04:56 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:04:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:04:59 GMT
ADD file:8efe37e124c3eb7c9e2b3ba1f33a019526490b9a49cbe8997abf72caf6bb7ece in / 
# Wed, 10 Apr 2024 19:04:59 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0c372adcddc32347cef56486050a9e3f15243cd4c6b2ef3b7de6d5d6f7bf9ef1`  
		Last Modified: Tue, 16 Apr 2024 02:49:17 GMT  
		Size: 33.3 MB (33315676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf2659681487961e24fc1b8f8f4a0ce1842d1f26fd5bcb1498c53ad86d1d942`  
		Last Modified: Tue, 16 Apr 2024 02:49:16 GMT  
		Size: 18.2 MB (18222412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5114d255d40b7d36826e85578ee08fc18aa455c1a9ef50cbbe3c6cb681698bfe`  
		Last Modified: Wed, 24 Apr 2024 17:44:00 GMT  
		Size: 132.7 MB (132720700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8797e46b2ec0d22d35dcf38023fabbc23dfc0b42f3b9621315ac823694dee834`  
		Last Modified: Wed, 24 Apr 2024 17:43:45 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3a3f188bed7ef4bd5e84b08d0ee8a87a08e34a20ba904a37e960141c9095f9`  
		Last Modified: Wed, 24 Apr 2024 17:43:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dbb670485310bf9425624e26ce5ac0e1e48763b11c1d7c8535f2bd3ab2facd`  
		Last Modified: Wed, 24 Apr 2024 18:42:50 GMT  
		Size: 34.5 MB (34493406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32eef0cc1948bf713b1217cfc8546d33ed324c7bee9e97d9451021e09e56236`  
		Last Modified: Wed, 24 Apr 2024 18:42:43 GMT  
		Size: 9.5 MB (9479941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475b78f9aaf0c67537afd284a24b2f77b51b3b01b8845133169d91ce0a682b81`  
		Last Modified: Wed, 24 Apr 2024 18:42:42 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de049ea367f72116eb71178d0e7be154d41c48da4d5897717f0090e12eeb28f2`  
		Last Modified: Wed, 24 Apr 2024 18:42:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ca363327b5dcb5489de07ed9a92cc31f64814d04a8b6218db03d2d7a32071`  
		Last Modified: Wed, 24 Apr 2024 18:42:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11-focal` - linux; s390x

```console
$ docker pull maven@sha256:232ee86be38eac528eafb011ff395cbec88fdc08f0914875a290dc8e84b1ecc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206462625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d9a5de9123f2dcad73c009bef4c1fae2d3c3715e51d52d46be4f1fc9cfef48`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 18:51:34 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:51:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:51:38 GMT
ADD file:c91b061ad49bce1f6e2860bfe87ed2e94cc280b915289f041d2dd5ce3ef385ad in / 
# Wed, 10 Apr 2024 18:51:38 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d94fd945c36b3b9c768528b528e1b8e7d49b0c692243295ec499726809202c4e`  
		Last Modified: Tue, 16 Apr 2024 01:36:12 GMT  
		Size: 27.0 MB (27013490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91663146dd1c9c0ef53a6a37dab31f5b428cfdfaf89084e3c721274d612d5d13`  
		Last Modified: Tue, 16 Apr 2024 01:50:27 GMT  
		Size: 16.6 MB (16645247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b449109c446438796bfa12ad04b426fdc81ecd8e47bc5f80c4a90b939aa4877`  
		Last Modified: Wed, 24 Apr 2024 19:48:51 GMT  
		Size: 125.5 MB (125502152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c5433843f79cda6b15bf657b74beb1d4a95e1091ac64b9446a44b16f9f95df`  
		Last Modified: Wed, 24 Apr 2024 19:48:42 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026abb37793873e4951a1ed519af4d523f8346c0bcc5be99389c2ec8a7ccaf5b`  
		Last Modified: Wed, 24 Apr 2024 19:48:42 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faad130b4d944fc090bca9d651243b067ed6d5fb0c6f382d54a30c3b96103d6`  
		Last Modified: Wed, 24 Apr 2024 22:09:55 GMT  
		Size: 27.8 MB (27819523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf4449068b6da926278e55da7310c3a2114c694f5cbc163582030287ec5b766`  
		Last Modified: Wed, 24 Apr 2024 22:09:51 GMT  
		Size: 9.5 MB (9479937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06683f33dbbf67632720b0661e167c04f38d9c150f81059f66df12ea0d1c8405`  
		Last Modified: Wed, 24 Apr 2024 22:09:51 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba0236f52693cff29353fd00095a72a1178ae021fbc4ce8174b52f626a95533`  
		Last Modified: Wed, 24 Apr 2024 22:09:51 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fbbbf7a5d5c5a61fe15b294c61f03ab7d93a928e95dcde071c82468d8ff04a`  
		Last Modified: Wed, 24 Apr 2024 22:09:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
