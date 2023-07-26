## `clojure:boot-focal`

```console
$ docker pull clojure@sha256:9b228a78a7b0841ab2e6e1493316aea29d6e6be5b78435fedc972d2d025f3133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:boot-focal` - linux; amd64

```console
$ docker pull clojure@sha256:04357b8affcf5811fb3efdf9e9f1aeb3e5edf63708685c5a0a534e2152d85a14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300484827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d7b20ba4494459eb6a3f189f44362e25311cdc3f9edcb7d044d8e0c9b3030e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:36:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:36:02 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Tue, 04 Jul 2023 20:36:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 04 Jul 2023 20:36:13 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 04 Jul 2023 20:36:13 GMT
CMD ["jshell"]
# Wed, 05 Jul 2023 11:24:59 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Jul 2023 11:24:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 11:24:59 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:25:04 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Jul 2023 11:25:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 11:25:04 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Jul 2023 11:25:20 GMT
RUN boot
# Wed, 05 Jul 2023 11:25:20 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 11:25:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 11:25:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a37d78e5ccaa1cc0aa197422c7c3994926b644d9f3ec6acf1f9a4f7001b0cb`  
		Last Modified: Tue, 04 Jul 2023 20:41:15 GMT  
		Size: 20.2 MB (20155566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075eb9ef0246b53768bb79c4fdad4d29a0f1e1887fd7c4bf14f6df30e804ffce`  
		Last Modified: Tue, 04 Jul 2023 20:41:26 GMT  
		Size: 192.6 MB (192587874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5fa2a2bc21e1a4f338bce8b335436a31b4d9b7255a7dbd0373b421ffe7c5fc`  
		Last Modified: Tue, 04 Jul 2023 20:41:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7875b65cd6d2012255bcc93f20620faf157ca5434389709434b8b8b25a3f445`  
		Last Modified: Wed, 05 Jul 2023 11:36:11 GMT  
		Size: 340.5 KB (340477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223692cd9dec5a622f156045875ca6ea024e51710febabd7cfb85ed9562e7267`  
		Last Modified: Wed, 05 Jul 2023 11:36:14 GMT  
		Size: 58.8 MB (58820322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8655b74875ea4f27d4c8dfb49900d535bdf056890670794a2d34e8aafaac6e50`  
		Last Modified: Wed, 05 Jul 2023 11:36:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:boot-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:db18e8dfb1ce64a7170f8be7e8a8adb271bf0caac577256b5a68fe1b6a985f89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250783903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f86ce1f1b7b0d9ffb27021e1be4e8ae93f9b28492f5c4fbd36631b6b5ed2a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:34:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:26:03 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:26:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:26:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:26:15 GMT
CMD ["jshell"]
# Tue, 25 Jul 2023 22:59:12 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 25 Jul 2023 22:59:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 25 Jul 2023 22:59:13 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 22:59:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 25 Jul 2023 22:59:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Jul 2023 22:59:30 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 25 Jul 2023 22:59:47 GMT
RUN boot
# Tue, 25 Jul 2023 22:59:47 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 22:59:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 22:59:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1684b62594f0c379e1487e5985d72ce7fa30b5c0f4697d3813e6cea825d0487`  
		Last Modified: Tue, 04 Jul 2023 15:38:48 GMT  
		Size: 20.9 MB (20872213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb65bf10eb4ae5266c5f96553a53ff92faf1eba777905e9f30c9e9d44845763d`  
		Last Modified: Tue, 25 Jul 2023 22:28:59 GMT  
		Size: 143.6 MB (143551716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c29d83ef77e4815b2c09f644fd6855dfdc6069d16fc25af32489733a99848b`  
		Last Modified: Tue, 25 Jul 2023 22:28:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c97ec25f3b2d6dbdc6f0bc3d638d618dbcb25bd3d73b11801f402a2149833c7`  
		Last Modified: Tue, 25 Jul 2023 23:05:22 GMT  
		Size: 340.8 KB (340770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ceb56eb8d2631fb63148d13488a37946081049176a70e007a6f1107c95d3f16`  
		Last Modified: Tue, 25 Jul 2023 23:05:25 GMT  
		Size: 58.8 MB (58820303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c88ac834bc6b5fbe36779704d2a6f4f237ce2804b5e42fce6b547799db4d1a2`  
		Last Modified: Tue, 25 Jul 2023 23:05:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
