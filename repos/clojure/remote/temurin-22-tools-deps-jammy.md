## `clojure:temurin-22-tools-deps-jammy`

```console
$ docker pull clojure@sha256:bb04407bf7f6b4e5cd89427183761d1253767409525c464e6865e839d8fd69b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:a85d510e683c684259adf9909a27e4ab4f11a526096b17aa1721969f26091421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255825108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bc634675a7a79e766c4409135d928e595796ffbbb9aff2ec089beb53756206`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ARG RELEASE
# Wed, 07 Aug 2024 18:04:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Aug 2024 18:04:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Aug 2024 18:04:12 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["/bin/bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["jshell"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5c2cb1f1de0d5bc5eaed4d185191b13caee359eedb0073a334e6b578b8d43d`  
		Last Modified: Sat, 17 Aug 2024 01:15:06 GMT  
		Size: 16.3 MB (16312792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae8c07f7960329d991c11512cf7955c870c52b0abb9b597aaf273d08ae8b2d`  
		Last Modified: Sat, 17 Aug 2024 01:15:15 GMT  
		Size: 156.5 MB (156487210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3457243757bf1f5c8a106a3e8f6a613b870eaef0f40fed04f204f42d9418a8f`  
		Last Modified: Sat, 17 Aug 2024 01:15:03 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d4a4541e07a46696e57def3d491c78e498e17af338ce4039f70c448e37a782`  
		Last Modified: Fri, 23 Aug 2024 19:29:45 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cec0b9845fb155a304004c8bfd767fdf53c4c8b31a8da7c2d35f93a25d8fd14`  
		Last Modified: Fri, 23 Aug 2024 20:05:27 GMT  
		Size: 52.6 MB (52581094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72c64bf2fc8f4113de2b810f1850d05d865e22545aa24d82133a0cd66064957`  
		Last Modified: Fri, 23 Aug 2024 20:05:26 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe62489282180e89a00c7ab8e776b425f1cfd655cd89ed903e80662e329c2f72`  
		Last Modified: Fri, 23 Aug 2024 20:05:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:d32c05dd939b02b502568c78385da7f76ced61cfc6a3cc2bdf28203661773ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3a84ed52d6c671ff5e1c18b92f5f444b57d28c49d979c97cf4bc4e5ed4d4d9`

```dockerfile
```

-	Layers:
	-	`sha256:bc5c4f61f2881b44834662ba2653126ea1474760d0f2239907ca99547189ae56`  
		Last Modified: Fri, 23 Aug 2024 20:05:26 GMT  
		Size: 5.9 MB (5930846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14199cee89c06286e66dbd4e18888764f9d83225d7bb0d77c4b9ff141b5ef810`  
		Last Modified: Fri, 23 Aug 2024 20:05:26 GMT  
		Size: 15.5 KB (15530 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45fc2691af96368ed2402df8e27ae25682f03bf8dd86bd3c41e2a1f2fc7f81a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253179219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503c428b0ac2cdaaaa653813f30e39e7bef42acb147e5e7596cae9cb80bb7bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ARG RELEASE
# Wed, 07 Aug 2024 18:04:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Aug 2024 18:04:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Aug 2024 18:04:12 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["/bin/bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["jshell"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f8601d4971927f65ddfed0cf5b9958e5d20d67fc7b11da3e4cdced7016186e`  
		Last Modified: Sat, 17 Aug 2024 01:37:41 GMT  
		Size: 17.7 MB (17721990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ae848da0a4fc64b8abab5631eaa6494b54e10851e117345e42984fe341f0af`  
		Last Modified: Sat, 17 Aug 2024 01:37:49 GMT  
		Size: 154.5 MB (154500954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e3e49123955e9f42dd0a91cb2e9e92b23a068b5cea2a2b855485458cc192d6`  
		Last Modified: Sat, 17 Aug 2024 01:37:39 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf39d671670372d1b48b686883752a34be2074f9dd893aa764f47c586778c1b`  
		Last Modified: Fri, 23 Aug 2024 19:47:04 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d5ebdde9a3e00ef53165abb376c52e4ec30fc8d14f34d3bd229a063c8e8f64`  
		Last Modified: Fri, 23 Aug 2024 22:05:40 GMT  
		Size: 52.6 MB (52555867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1ea3447e3cd37065d8c4ae74e0ff3578915300469fed0fe6eaec23625d8e98`  
		Last Modified: Fri, 23 Aug 2024 22:05:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1294b4b39f6179eca6f6a0a72500d116f40ec3db5962da6564f47d341307a405`  
		Last Modified: Fri, 23 Aug 2024 22:05:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:cf565bcb8813619a225b081a8ea4743becfe7e05d2ee5ea505614cfc99d3900f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6048992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427d0b32d4b043ac38a3507e92f2d71aa7779198f8186d000f665427eee60b4d`

```dockerfile
```

-	Layers:
	-	`sha256:8c9c7e23c6e7f4a4bf3aca8f7867f56390ff7cc301bd93417c4007edac7dfde0`  
		Last Modified: Fri, 23 Aug 2024 22:05:39 GMT  
		Size: 6.0 MB (6033159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b853c23a46e1571fd2b19f1a662367678735aad407dfd6ea85159c1e424573`  
		Last Modified: Fri, 23 Aug 2024 22:05:38 GMT  
		Size: 15.8 KB (15833 bytes)  
		MIME: application/vnd.in-toto+json
