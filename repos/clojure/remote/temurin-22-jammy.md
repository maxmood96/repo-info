## `clojure:temurin-22-jammy`

```console
$ docker pull clojure@sha256:e0ea5a697ee5eaa3d8865d8bffee87e9945d2730a9d1f07feefa71f823d625d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:a42dd9717d23e7920c61e18d2850678f938bbe542cf4119ed65fe4cff5b3f0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255824796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01133c2e64736d7e8221e50f0873c4f0e633f8fa35b6feb2fa68ac2b4e96fd0a`
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
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
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
	-	`sha256:caf80bf1683b33de1672b7f1e53363d0982fcdeef5b510c2d526bbd0445c6f2b`  
		Last Modified: Sat, 17 Aug 2024 01:15:03 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4919750562d99afb8084468d7203fe0ea27f42ef8073829cfeea5e32c82715bf`  
		Last Modified: Sat, 17 Aug 2024 02:04:35 GMT  
		Size: 52.6 MB (52581024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddff43e0a10605ed4ef2be009b89e9e6f1fccd45d5fd04130aa3036abf7f294c`  
		Last Modified: Sat, 17 Aug 2024 02:04:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c2342c6b755149544ebe849a768251cc09f0c5db2d96833b916f838d5eb5fe`  
		Last Modified: Sat, 17 Aug 2024 02:04:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:f26cf81d37758f20340980c9075d1db69fccdede519100a354ac204341b75aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc1ee38d9cbb2bd5ecc025e7381341e4a005210b42cefffe96ca12669e69e01`

```dockerfile
```

-	Layers:
	-	`sha256:592e612d3590354df2c7a8a5e7921cf3bc66de3296527bc195998a4610e51978`  
		Last Modified: Sat, 17 Aug 2024 02:04:33 GMT  
		Size: 5.9 MB (5930830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bee016b491500f960e3ff500875543d839cda4fbf86d84de8f7520cba9c3b317`  
		Last Modified: Sat, 17 Aug 2024 02:04:32 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:109c4e8a9f46b43b0b57d4ae8e289af4fd45531e572b2813b11f7cde7cf4e13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253182942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd428e52ffe8961bb59d0a678af9a097c179a1577b248eb3dffd6726b2e8f56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac50ae6767d4a91ada9d54209c76b3645963c6e1b649e0894bcfbc75cf1e0877`  
		Last Modified: Tue, 02 Jul 2024 04:36:41 GMT  
		Size: 17.7 MB (17721806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccb33b6e6156bf3bae7feb6806afcc4d2c0fe9235dfbb29068ff2855c4cb5ae`  
		Last Modified: Wed, 24 Jul 2024 00:53:07 GMT  
		Size: 154.5 MB (154500947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16094ccf4532f9f5a492b45dba12cf96fef5f6df808bd1fb8116edb76befaf85`  
		Last Modified: Wed, 24 Jul 2024 00:52:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d600663c90612c96e00442ef9a3ef10a0f567ff4b02a4b0e6de9f0619a20e6`  
		Last Modified: Thu, 25 Jul 2024 17:48:20 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a83133824d082f1c3aba657c1829deb3adafa0304fed247de480f7a977e4a7`  
		Last Modified: Wed, 07 Aug 2024 20:20:23 GMT  
		Size: 52.6 MB (52556002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e018e5bcb3f835fa7ce097d7a81c61b97324d5de237660ef3abf3359578ff0`  
		Last Modified: Wed, 07 Aug 2024 20:20:21 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae6970cb4420d6bac5f49241a586a65f95bfed450a7193e2da09712b9561ca`  
		Last Modified: Wed, 07 Aug 2024 20:20:21 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:8e5f499e907f46c7342b33bc42ced271af466376a9c08a8013c848582d77befa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6048972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82b3f2b36fe8beb0f44795b9d1c2fe761a9c72230f39d6539da5a733a8cea4d`

```dockerfile
```

-	Layers:
	-	`sha256:7b9fd55ca78a116dc4ad9a1cf96ea2fa5737acbc1609e7b588a9bb4a1c11d020`  
		Last Modified: Wed, 07 Aug 2024 20:20:22 GMT  
		Size: 6.0 MB (6033139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9a2242b26cef3b4877970a0f971db56145a2f6c8154a2efc3b70a3ebf62d067`  
		Last Modified: Wed, 07 Aug 2024 20:20:21 GMT  
		Size: 15.8 KB (15833 bytes)  
		MIME: application/vnd.in-toto+json
