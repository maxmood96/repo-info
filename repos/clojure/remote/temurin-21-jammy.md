## `clojure:temurin-21-jammy`

```console
$ docker pull clojure@sha256:b447adee2ad895dcbc3029aea575b18b1131ffa6bf6a2e610f0bc446d70a1b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:31e747a5ac87bb9099fa3e3afe3cbed4358fb7ab66f65511589987f245464b52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258081400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9b49608a4bd867651aff7fad852f1a11f5a363046ef195e19b33a6b4372f16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
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
# Wed, 24 Apr 2024 21:32:47 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:32:47 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:33:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Wed, 24 Apr 2024 21:33:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:33:02 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:33:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:33:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3320e4e2ae41973a279c466eba6f7af49750691a7d55baabde5b47c635660f`  
		Last Modified: Tue, 16 Apr 2024 04:06:12 GMT  
		Size: 17.5 MB (17456328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b6c8970fafbd67b6e2704d6584bdfc6e2275755afdc04802a4a93a33682ae5`  
		Last Modified: Wed, 24 Apr 2024 19:16:37 GMT  
		Size: 158.5 MB (158511994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95d7ac9605410015e4da369ce7b01bcee8f2ec9786143fb078632e1d47a3ead`  
		Last Modified: Wed, 24 Apr 2024 19:16:25 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7721b0553ddeb086a53f4c6198ae14407ecc6c369e1005cbfe5c69700e6600`  
		Last Modified: Wed, 24 Apr 2024 19:16:25 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6321ef2e23b0f374b92691e8b12de86745db2596de352e2253aaa1f9aa2507c5`  
		Last Modified: Wed, 24 Apr 2024 21:55:17 GMT  
		Size: 51.7 MB (51671364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20fffb41cf35858027c0b022b08dfa798834b9cac857eca394648de77e7d91e`  
		Last Modified: Wed, 24 Apr 2024 21:55:11 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1834f8011190771b892a631d69ecc0dc633ee8bc01117bd0c4adada29247b4d`  
		Last Modified: Wed, 24 Apr 2024 21:55:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66680d76f662afdbfd8e24b72669a1a8172cc2f50b2df2e78f307a5be33442cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255588995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168d471bdb1d5e4d8d324eca9621c4ac250b4244d0911e931b4088372f3bbddb`
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
# Wed, 24 Apr 2024 19:15:39 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:15:39 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:15:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Wed, 24 Apr 2024 19:15:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:15:53 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:15:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:15:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ca446d1269832583bab37518ceccaf1672995d944d4df514e3d74c11ebc63d`  
		Last Modified: Tue, 16 Apr 2024 02:57:47 GMT  
		Size: 18.9 MB (18858954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576dc41aec19f734359803b0a7553a59b420ac7697fe6fd8e902f6581da3cfa2`  
		Last Modified: Wed, 24 Apr 2024 18:00:52 GMT  
		Size: 156.7 MB (156672762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b463925a66dd796a95fdc0eb9b29d34816fa72ab8eeb4bc916d54694c00b3c97`  
		Last Modified: Wed, 24 Apr 2024 18:00:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ade5645c4cb05ec8a9f51b2c6d60996a044cdbfda593360feedb169cc75311f`  
		Last Modified: Wed, 24 Apr 2024 18:00:42 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b395e8a6f450ae29b4cb8d3f6ee1738b96ee3342e8092baa7aa807d873f9eae`  
		Last Modified: Wed, 24 Apr 2024 19:34:45 GMT  
		Size: 51.7 MB (51655051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4bb485bd2f35b65c6f72e8b1250eafde46c6b7863ac15ac6be3fec2f24ec36`  
		Last Modified: Wed, 24 Apr 2024 19:34:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afa57655cd3f857c0978ec1796184a33ce7e3143501a68f3b6b081c9df36ab6`  
		Last Modified: Wed, 24 Apr 2024 19:34:39 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
