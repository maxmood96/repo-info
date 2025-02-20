## `clojure:temurin-23-noble`

```console
$ docker pull clojure@sha256:e20478fd21ddccdda6ef72f81980cc0000ff5eebe679612cb7d316d06b611fec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-noble` - linux; amd64

```console
$ docker pull clojure@sha256:3118afe9d347dee91b464e366075fa71044b44b73be4c037b6fbc4cd74c7c8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275421074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14faf560b63e8df53ba99b738e20894d4d4ef44c6ae21c7f866804f97dbf7df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='1e102e1e6653f8810ef6c275b0d38ea7036abd4a8709f0f916b339f65e76bb56';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1504bee8985780f3a868793411f26933d71ee828bc50880d128017596324321`  
		Last Modified: Tue, 04 Feb 2025 07:59:07 GMT  
		Size: 21.3 MB (21318286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5a3507f742036dd166ee8b5a8ceeb35d451eacd472188cb43fdf7844a9e06b`  
		Last Modified: Tue, 04 Feb 2025 07:39:24 GMT  
		Size: 165.3 MB (165317796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea28f6f7f0aa0864f252fa90ca3f85687428d91dd6f829f2ba81dc8719e2e3be`  
		Last Modified: Tue, 04 Feb 2025 07:15:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f710610a5590898a3f0cf7b538bbc25d7c04c96ea891b3051d65d130b5cf464`  
		Last Modified: Thu, 20 Feb 2025 08:42:10 GMT  
		Size: 59.0 MB (59027347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9875c97026b6fceb4f12d18c79b1bea145d636ed9f03e98b549c93f860832166`  
		Last Modified: Thu, 20 Feb 2025 08:42:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1707e0426627089c57460559b18159cd7b2b3d17e1cf30139c684d0e01221e2c`  
		Last Modified: Thu, 20 Feb 2025 08:42:06 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:906b6e6ac64bcf4bdfce0a0e3c3309563614c2b189f2800155dfba65614b947e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3b6ccb0a433e6c6803d70fb7d249ba108bc51374683ea8e6fa368efb40b903`

```dockerfile
```

-	Layers:
	-	`sha256:41b5eae9e233045d1f1f0d33302453da694705936591ff2d2f39847c75513d10`  
		Last Modified: Thu, 20 Feb 2025 04:38:17 GMT  
		Size: 5.7 MB (5676967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39927ee43bcdfd27f3cafbe4a2516a77a36e56294721adb5ee66f7d04537e09`  
		Last Modified: Thu, 20 Feb 2025 04:38:18 GMT  
		Size: 15.6 KB (15581 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:871608a041af25f752eca8614f7ea83eefbffd1eb6b6bcb82efaa5b7f82042c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273701816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e566cead196d20cd2673f45d89b7ebcf6dfcbe0560230f735da25ac342fe87a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='1e102e1e6653f8810ef6c275b0d38ea7036abd4a8709f0f916b339f65e76bb56';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2245538400d4103f4db24ab5d1b42b9ea469aa61330be59963921f029696d`  
		Last Modified: Tue, 04 Feb 2025 21:41:10 GMT  
		Size: 22.5 MB (22496103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953931721e17dba0346c2346b62471cfe151b7afcc3c70b868f521bea1f60f02`  
		Last Modified: Tue, 04 Feb 2025 14:23:15 GMT  
		Size: 163.3 MB (163346325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00aa35d7029404f46e849dbd52e030cf92d6c4f560d92511f5223c10cea8a644`  
		Last Modified: Tue, 04 Feb 2025 20:08:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8affe9d69ea72481397ad14037b465871edecbf9c3b836c0653fa9e9b35f49`  
		Last Modified: Thu, 20 Feb 2025 04:05:26 GMT  
		Size: 59.0 MB (58962431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16152307e0399e085b6092ffa08ccf039f320e54d96be88cf1ae191e0164d989`  
		Last Modified: Thu, 20 Feb 2025 04:05:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3e8fe2276790fd68f0bb818512ff3b0ec950ae26e522f727af9c8b05d0b45b`  
		Last Modified: Thu, 20 Feb 2025 04:05:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:c68e2d1d9379372917d1dfa2e8b2608276c4b97c44a3058c313238717fc37854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5829632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292212efda313169c7e6d439f3fd4362db8fe71782735dc2f3d9f50b78d5e2cf`

```dockerfile
```

-	Layers:
	-	`sha256:65e259d89ed6fc6a01938548691986f0fe6750fccbb44b2b689a503ac3a5b702`  
		Last Modified: Thu, 20 Feb 2025 04:38:21 GMT  
		Size: 5.8 MB (5813959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb832ce98a98116f900c7cd60a73eab7c069737924ecce37ce8c0d766dc3012`  
		Last Modified: Thu, 20 Feb 2025 04:38:22 GMT  
		Size: 15.7 KB (15673 bytes)  
		MIME: application/vnd.in-toto+json
