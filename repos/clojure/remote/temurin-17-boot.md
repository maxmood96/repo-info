## `clojure:temurin-17-boot`

```console
$ docker pull clojure@sha256:76433cddc31dfa6123c46dab66e94a3b1883b66119b7ee5b259ad7aee065b5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot` - linux; amd64

```console
$ docker pull clojure@sha256:63ed967661040cd6506f31d552f2e17e561c02954ae8e1d5bf689feca4a9f04d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251969450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb147fa91f0a61993b5ee06e2a489b7a71c586b8a94e97e4f7f103c9a06dd3b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 11:07:04 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 03:08:45 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 03:08:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:08:45 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:08:50 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 03:08:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:08:50 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:09:07 GMT
RUN boot
# Thu, 28 Mar 2024 03:09:08 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:09:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:09:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0d9a6855e071b36fbc6570e03cad42b0048eb5b1f5614c1753d6380cecfa9`  
		Last Modified: Thu, 28 Mar 2024 02:09:07 GMT  
		Size: 17.5 MB (17455933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7d891635705a3929c1fe0b5cf0e411d6fdff6aada0305d3954968edf973ec`  
		Last Modified: Thu, 28 Mar 2024 02:09:16 GMT  
		Size: 144.9 MB (144899966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71555250e9d75951fa801c00af20690e7a9bcff8db0d671f8d3e8437b8713653`  
		Last Modified: Thu, 28 Mar 2024 02:09:04 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4f3b0af088f0ac99bc27258d0ec957d837be8754ad92943679c318bad4411a`  
		Last Modified: Thu, 28 Mar 2024 02:09:04 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fde622a7f050f89e7dcc37ec667873fac74cd913f0d471a62239f343ff3568`  
		Last Modified: Thu, 28 Mar 2024 03:25:39 GMT  
		Size: 340.7 KB (340697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc4366fe2486745b5845f8262660e20f04f5d65d1eedab5f867f6f1b2bdec72`  
		Last Modified: Thu, 28 Mar 2024 03:25:42 GMT  
		Size: 58.8 MB (58820241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9810de7c46402eeee5c2fb2d0ed5814041cf33bde2c37db27998636324c852a3`  
		Last Modified: Thu, 28 Mar 2024 03:25:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a31d034bd6700256e51da04138f7b0218b43436fd7dcde8a871c6f970bef5f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250145467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0415346484d944687ad12b19f58c1bbd6bf6ef610142b0d291606468776f877`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='9bb8ccb9993f85d07ca3d834354ce426857793262bea8dab861b0aebb152d89c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 11:07:04 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 02:41:18 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:41:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:41:18 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:41:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:41:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:41:22 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:41:37 GMT
RUN boot
# Thu, 28 Mar 2024 02:41:37 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:41:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:41:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5819ee025bb6ae72373320497f73046533f43572fca8bb269097a7bc9560c51c`  
		Last Modified: Thu, 28 Mar 2024 00:52:43 GMT  
		Size: 18.9 MB (18858231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc483c322bc8610f99c561299e34246f3560dfc6e2c1359c538d17c5c1a5c055`  
		Last Modified: Thu, 28 Mar 2024 00:52:50 GMT  
		Size: 143.7 MB (143724118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b16c42c4298557bd72499a0229bb0ebc44eb0389a4a3b450d9f21db7b91159`  
		Last Modified: Thu, 28 Mar 2024 00:52:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c726e3e68e977fd33733b19602bf375a1754d8a0c17285a1381b3092a224d579`  
		Last Modified: Thu, 28 Mar 2024 00:52:40 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf652adcdd3fbb7c611e868db40f77e5838b9b7db7099dfb0159baac5eaecfc`  
		Last Modified: Thu, 28 Mar 2024 02:54:56 GMT  
		Size: 340.9 KB (340889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbde8b1aa1c7ea7cbc4c40c1b26a291a4ca30a52eb2585ef6d513035ea39967f`  
		Last Modified: Thu, 28 Mar 2024 02:54:58 GMT  
		Size: 58.8 MB (58820287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863c3dd58e8250dd089e8f507fe51288b19160e9cbf5e9dffc3204e0b7187ca6`  
		Last Modified: Thu, 28 Mar 2024 02:54:55 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
