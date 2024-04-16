## `clojure:temurin-22-tools-deps-1.11.1.1435-jammy`

```console
$ docker pull clojure@sha256:51bf0a1cd64135c7f96eb2d006b956588c483a367df5315d2723d7980a8621bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-1.11.1.1435-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:6fcb9cb554f1ed0b64597a9f6d2a140239e973c7f3244701df135b7e7ae6d259
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257537521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7876de60216f4c0e5d82de32ea8b220db1a4ba85f4091eb697a8b255b3c83981`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4b52670caea44848cee893e35c804380817b6eff166cf64ee70ca2bfaac3d1c7';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc3d99e816d0c373f424cd7aa2b6d3e8081a7189fe55c1561616922200ec8e47';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c062e934d95c639f97b4e51b968eed694a6653248727c3db8bc5e0e55cfd7f4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
CMD ["jshell"]
# Wed, 10 Apr 2024 20:38:15 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 20:38:15 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 20:38:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Wed, 10 Apr 2024 20:38:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 20:38:33 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 20:38:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 20:38:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e531083e1b0a15cdfac26d85cd8a10953cf6e70ef3798ed13a8457344f2c87f`  
		Last Modified: Thu, 28 Mar 2024 02:13:42 GMT  
		Size: 16.3 MB (16337175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34e2093c50752190bab37a96ab0af869b84a8714e622349658adf61bddee95a`  
		Last Modified: Thu, 28 Mar 2024 02:13:52 GMT  
		Size: 157.9 MB (157881913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b36755bec6f1cea87895a91d5c638c7e0f2aa7b78f0f866b30ff5c50886159`  
		Last Modified: Thu, 28 Mar 2024 02:13:40 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d7b39df2027f8c1ade8a458cf1f2d5926a841b79715789ce75737f160b950a`  
		Last Modified: Thu, 28 Mar 2024 02:13:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0be61c797cbbf04624348e3605f133d80ac7ba85ac488723d3e7722f0e0cdd`  
		Last Modified: Wed, 10 Apr 2024 20:53:33 GMT  
		Size: 52.9 MB (52865228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f6e1431a63f0639b26188a64358e0ad505f1f8bd71eae45929c4dd8562f4dc`  
		Last Modified: Wed, 10 Apr 2024 20:53:25 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb40dfcfdbba22ea00d79cf556b9e7b0f14b2f19272d79bf3251f3de37953375`  
		Last Modified: Wed, 10 Apr 2024 20:53:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-1.11.1.1435-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c49f7959cf62b6ba993750c6bd6594ba75a25784f4381940de55dba186acd5d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254869445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1a2ed5c9ea0e92d63785a59426d3ba73046da9ae1c7e383e40c7f95e330326`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4b52670caea44848cee893e35c804380817b6eff166cf64ee70ca2bfaac3d1c7';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc3d99e816d0c373f424cd7aa2b6d3e8081a7189fe55c1561616922200ec8e47';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c062e934d95c639f97b4e51b968eed694a6653248727c3db8bc5e0e55cfd7f4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
CMD ["jshell"]
# Tue, 16 Apr 2024 06:48:10 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 16 Apr 2024 06:48:10 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:48:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 16 Apr 2024 06:48:32 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 16 Apr 2024 06:48:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:48:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:48:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ed6356befcb3f3e3f2dbe4ed0457e6f2e017191ad3f4f999da71660803fb42`  
		Last Modified: Tue, 16 Apr 2024 02:59:21 GMT  
		Size: 17.8 MB (17753415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d67b61cf32e2270130b73c2a006e1b0750e3a77ea9613844583a8400ff9f6`  
		Last Modified: Tue, 16 Apr 2024 02:59:29 GMT  
		Size: 155.9 MB (155868249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65dc80542294dec55abc165ea565444bb81164a7332ef94ed22b1857b7da32e8`  
		Last Modified: Tue, 16 Apr 2024 02:59:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa6cf93078a2fbfea07d632c3cc6b201cc6ee1113991699f63538522b562ebf`  
		Last Modified: Tue, 16 Apr 2024 02:59:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bfce86bff83f103a232605fbd725d7f7274599f7e45471c166f5a89ef264d5`  
		Last Modified: Tue, 16 Apr 2024 07:02:03 GMT  
		Size: 52.8 MB (52845586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d535579fc04d957dcb6e901ed3c368164937575d3d7b2c10d4f1a530a0cdc3`  
		Last Modified: Tue, 16 Apr 2024 07:01:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec720e9a41814e3952e373e3a38fb585ae1de996ad4275cf8872bd5cb6ae838`  
		Last Modified: Tue, 16 Apr 2024 07:01:58 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
