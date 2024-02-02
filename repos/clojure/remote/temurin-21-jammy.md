## `clojure:temurin-21-jammy`

```console
$ docker pull clojure@sha256:43c4255dd34a2b4c30ce9d571eb95d81b7fd44f45faaa34fd7438fb6ce5ee5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:bcd40d38fb30790443eb7e9a01318a0d33df251d24e593da3df92c5202cf6e64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259168485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db8f38b2cf0be08d54f69e51a73f107e5c31c8c3d3012f73e07c9cab8a8b380`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:45:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:45:48 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Fri, 02 Feb 2024 07:45:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce6a2b357e2ef45fd6b53d6587aa05bfec7771e7fb982f2c964f6b771b7526a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='454bebb2c9fe48d981341461ffb6bf1017c7b7c6e15c6b0c29b959194ba3aaa5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='d08de863499d8851811c893e8915828f2cd8eb67ed9e29432a6b4e222d80a12f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0d5676c50821e0d0b951bf3ffd717e7a13be2a89d8848a5c13b4aedc6f982c78';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 07:45:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 07:45:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:45:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 07:45:59 GMT
CMD ["jshell"]
# Fri, 02 Feb 2024 17:26:54 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:26:54 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:27:09 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:27:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:27:09 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:27:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:27:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26611c45681a8966387aee7b2e1494405e20bc5a46dc5da0af9228c45f8e8ec4`  
		Last Modified: Fri, 02 Feb 2024 07:50:10 GMT  
		Size: 17.5 MB (17458288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e5157807e9b9c65d974d61c154ede442ef90216bfc1a6bf15c9056fc25fba9`  
		Last Modified: Fri, 02 Feb 2024 07:51:17 GMT  
		Size: 159.6 MB (159589874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf2af0ceb31387adbe1068001686aba5c034396442aec6756c7d95c0201efa2`  
		Last Modified: Fri, 02 Feb 2024 07:51:04 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9069ee62a4b7a3620745a2d920573721c3543c6c12659b8884fc7e545bd5a705`  
		Last Modified: Fri, 02 Feb 2024 07:51:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a408047d3cd0713db44294a1e8416f03a1e0b937b24f81e81b85e137edb0df4`  
		Last Modified: Fri, 02 Feb 2024 17:41:20 GMT  
		Size: 51.7 MB (51670514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e0ac3e5cf725dc70ef8e846d236dbf0b177394906b7d619689c79810a96d63`  
		Last Modified: Fri, 02 Feb 2024 17:41:14 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1099489eb84a20420ab6bf95ba4f8f2e0d0d561a749af08f15d8edf5a65d74c5`  
		Last Modified: Fri, 02 Feb 2024 17:41:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c4e2e13af821d28d47ba550f89e79741d8a3a7b0785da12db9e026a1bda1972
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256706876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da31c89055e6023790c54ec900a80544fc8608feb2e4385d69a3152ee90bdd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:10:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:10:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:12:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:12:42 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Fri, 02 Feb 2024 02:12:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce6a2b357e2ef45fd6b53d6587aa05bfec7771e7fb982f2c964f6b771b7526a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='454bebb2c9fe48d981341461ffb6bf1017c7b7c6e15c6b0c29b959194ba3aaa5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='d08de863499d8851811c893e8915828f2cd8eb67ed9e29432a6b4e222d80a12f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0d5676c50821e0d0b951bf3ffd717e7a13be2a89d8848a5c13b4aedc6f982c78';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 02:12:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 02:12:54 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:12:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 02:12:54 GMT
CMD ["jshell"]
# Fri, 02 Feb 2024 08:34:22 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:34:22 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:34:35 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:34:35 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:34:35 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:34:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:34:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d031894e4c0411af099ca88f2f4707adffb7144d8d3dc5d40457cededf240b5`  
		Last Modified: Fri, 02 Feb 2024 02:16:39 GMT  
		Size: 18.9 MB (18860666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8147c5140d802de257ae5b5b8b9bea14e1e65e1ac7b1468752795c95fb10e1d8`  
		Last Modified: Fri, 02 Feb 2024 02:17:46 GMT  
		Size: 157.8 MB (157790692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f2ab3d5e230728112ba972dd5f1ec34d3110e9c536173a4c85699422fd7985`  
		Last Modified: Fri, 02 Feb 2024 02:17:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55c7dbfbcf51eb48f161d216fbd46ecacaf8b1e7b953d817e2759029814935a`  
		Last Modified: Fri, 02 Feb 2024 02:17:35 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002cc9550848baa4a03b6c521dee7df212c68912aaa68f42c5b5c64fc95de72`  
		Last Modified: Fri, 02 Feb 2024 08:48:25 GMT  
		Size: 51.7 MB (51653491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77a71cf2ac82a1c3bce1b71e17493d588ace287fa8d183a724cd638b154a160`  
		Last Modified: Fri, 02 Feb 2024 08:48:20 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472c5c268ba7fc8fc2ca92f75e3fa2201966458deb64e251dcbebe243192a3d`  
		Last Modified: Fri, 02 Feb 2024 08:48:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
