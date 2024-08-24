## `clojure:temurin-22-tools-deps-1.11.4.1474-noble`

```console
$ docker pull clojure@sha256:d51f3c39daab94cbb30d51cb6a51d4fd9f6f4418fa3bad47573da9da4e4610f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.4.1474-noble` - linux; amd64

```console
$ docker pull clojure@sha256:a4403dd648a5fe2528fc9a07026ef18f0ec8deb2913fe4bab512cf9c75d194ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262686757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5e0a955b80559a1ef21d9af06deef0bf56ddd7b047d719990261a2579f00b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        riscv64)          ESUM='830a0d006c2dae95c0855aa70e193dba637831b491ccd67333322dea31bcf389';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_riscv64_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a476ddaf8f2380122935e7fa2924236f31f3ecd947aac602c3f934f04c2c3f68`  
		Last Modified: Sat, 17 Aug 2024 01:15:27 GMT  
		Size: 17.8 MB (17831031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7668611b52c084e8cac4c64a8ed4664f98b67a79a8c70111453be10b0951336`  
		Last Modified: Fri, 23 Aug 2024 19:30:05 GMT  
		Size: 156.5 MB (156487285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749a9b747a4e64836b5ce0849fc24d13c1c49eb8d710ab4bc307fcb81911eba0`  
		Last Modified: Fri, 23 Aug 2024 19:29:53 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6059789c2a0f78562153e0ef1319a7528230093e0debbb9a81c1dd8e92aeae08`  
		Last Modified: Fri, 23 Aug 2024 19:29:53 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe8962d07a85adcd5ca6276f694f10aa1b12b0dfb4eb2a33f223c3e3de824c5`  
		Last Modified: Fri, 23 Aug 2024 20:05:43 GMT  
		Size: 57.8 MB (57797836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd6e3e36e73cdb23c30f9cffc6e40b38891283efaf1cb48acd152d5297f3cf3`  
		Last Modified: Fri, 23 Aug 2024 20:05:41 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c64eb144ba07cce6d7232f7f63f77d8ce49c2be65727de24e1b7ab229624ae4`  
		Last Modified: Fri, 23 Aug 2024 20:05:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.4.1474-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:f47817d9ea78120aac32b8db97a7b017213e438576117a15bd419f5c8680ec90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5442733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd49c533444fb5e657a34b589bcd27b2eb6d30bcac6dc706999e6f8bbdd08c2`

```dockerfile
```

-	Layers:
	-	`sha256:688a918c3e64af0f05357a4fbbeeb48aa9d48b7e5db304255caceea1aa78a129`  
		Last Modified: Fri, 23 Aug 2024 20:05:41 GMT  
		Size: 5.4 MB (5427203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1717ed9f4c8c5d72bc94df9e61afcc7c4fbabd23fee33e0268d4619f0d78bb0`  
		Last Modified: Fri, 23 Aug 2024 20:05:41 GMT  
		Size: 15.5 KB (15530 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.4.1474-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7f809edb24927bdf651807ea647e361c2ba17b7f0cd381dc956c17851b074a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261218136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ff32aa37b62d7fb4debd86f6fbe86db76090793995a5556f9c1f043ae8bebe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        riscv64)          ESUM='830a0d006c2dae95c0855aa70e193dba637831b491ccd67333322dea31bcf389';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_riscv64_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b141587f26721272defe7a8441c82c6c025cf68abf11c95e7a03e721dc40110`  
		Last Modified: Sat, 17 Aug 2024 01:38:00 GMT  
		Size: 19.0 MB (19004619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a374b5775895dc65797da72facef41db14d5f3979612dfbd5da693a0d479c9`  
		Last Modified: Fri, 23 Aug 2024 19:47:22 GMT  
		Size: 154.5 MB (154501072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db2a5830202fd55fd0da6d5cfe5c2d16d0835d17cccd1ab5c4f431ee094fed4`  
		Last Modified: Fri, 23 Aug 2024 19:47:12 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529f9deb08c05f614fdb41320b00241cefb7299bb2d29d9f5b1f3015c3d253d5`  
		Last Modified: Fri, 23 Aug 2024 19:47:12 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a596511390ba8f23bc81882679fea52d765d82fcd4b71a2b7664779e555760e7`  
		Last Modified: Fri, 23 Aug 2024 22:06:27 GMT  
		Size: 57.8 MB (57799119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac815cb87ae936b4d74e269e36b43bc5d007eea230202502b3797715929a2d`  
		Last Modified: Fri, 23 Aug 2024 22:06:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089e7645512e31bfec15afea1b8ef6924cfae082a67b785544a0671eeeb0a104`  
		Last Modified: Fri, 23 Aug 2024 22:06:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.4.1474-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:a1e38f9e0f73428e86096bf015a68f92dad5de7e8f38c0b96e3ddfcc6fc9ffe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5581444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f57a80121987eca20a26926489f273ae20a2141209273f5b18247122ce6faa`

```dockerfile
```

-	Layers:
	-	`sha256:75614c92414de729856d0e6c8fe73e96e0bbec389c95ba339447e5727ee20d95`  
		Last Modified: Fri, 23 Aug 2024 22:06:26 GMT  
		Size: 5.6 MB (5565609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55555bcffb42ac770b36bc84b2c0cad431460f22a77ad22371745f8084820f1e`  
		Last Modified: Fri, 23 Aug 2024 22:06:25 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
