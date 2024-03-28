## `clojure:temurin-8-boot-2.8.3-jammy`

```console
$ docker pull clojure@sha256:6a3002c1ad1f9c85b8cacb712fa133db69352a16e99a5a384fc6024935089b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:dd9e837ad0bfd94558dbec39b2c7b863525305d2c198e71cc5ac9491136686f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206117293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d6e9b8733595774f993bab553f1bc3607043c9e4d9e0ce1863f79106606e51`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["boot","repl"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 28 Mar 2024 02:54:57 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:54:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:54:57 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:55:03 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:55:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:55:03 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:55:21 GMT
RUN boot
# Thu, 28 Mar 2024 02:55:21 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf356fa6e6902e661a53c29cf3b351f284090cb2c0de2ad6c5c238a6fdb9a8`  
		Last Modified: Thu, 28 Mar 2024 02:03:28 GMT  
		Size: 12.9 MB (12904693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf62b0dd6e4e68ab72316aeb589f5593b8c17e9c1c7713578bf3fcda29bd50fd`  
		Last Modified: Thu, 28 Mar 2024 02:03:33 GMT  
		Size: 103.6 MB (103601321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbcbf92947e43bf222292a1e0d251f46ddfeb5e0924a6638653e972e1660d35`  
		Last Modified: Thu, 28 Mar 2024 02:03:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401c25db2ebafaaede733d2b3e5cd7dc70e004edd4e8b8fbe8768a80106825ec`  
		Last Modified: Thu, 28 Mar 2024 02:03:25 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e5b2843cee6167db017753726cae15fb2b5188e9ca04b65a8ff626df9d0133`  
		Last Modified: Thu, 28 Mar 2024 03:17:12 GMT  
		Size: 338.6 KB (338557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709f8d8fc486d927d77da6dd8064be15d68c8d7408f6a39dde045037caa363d`  
		Last Modified: Thu, 28 Mar 2024 03:17:15 GMT  
		Size: 58.8 MB (58820527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e5fdc38128b28e1f3892667f5ba467a87e64957d1e12d4ff168d6785ba28eff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203112762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f86591e9d158c8f654dead740d82671987fa9039aa5e8e0d03f36e2fb21776`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["boot","repl"]`

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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 28 Mar 2024 02:29:54 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:29:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:29:54 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:30:02 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:30:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:30:02 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:30:18 GMT
RUN boot
# Thu, 28 Mar 2024 02:30:18 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2168560270786452bc1288278f5b8a7831c90a490efa55dc798deec8e871311a`  
		Last Modified: Thu, 28 Mar 2024 00:48:42 GMT  
		Size: 12.8 MB (12846303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13444997d0a536bafe4b843c5d7d607a1f71bd3cc414162b2afd4b60175d20f5`  
		Last Modified: Thu, 28 Mar 2024 00:48:46 GMT  
		Size: 102.7 MB (102705878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333e8df10d7700ececd835993dafc90964410eb0fdd266ce7de75b61ba37c689`  
		Last Modified: Thu, 28 Mar 2024 00:48:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6328c808abc1335b4efa10cdd4cb1d0c9b06b944f4aca3b409376141a42768b`  
		Last Modified: Thu, 28 Mar 2024 00:48:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1162484e4bbfed456c82ca578b2ba6dbd325b64259cef32d3e4b6059a4a861`  
		Last Modified: Thu, 28 Mar 2024 02:48:00 GMT  
		Size: 338.8 KB (338837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf744a92311175c1aa6fa70c85b9976b74d2e57c7f5c7c3014b0c67e61aea101`  
		Last Modified: Thu, 28 Mar 2024 02:48:02 GMT  
		Size: 58.8 MB (58820213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
