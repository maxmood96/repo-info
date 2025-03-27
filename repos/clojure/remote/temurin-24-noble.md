## `clojure:temurin-24-noble`

```console
$ docker pull clojure@sha256:746010bc29f1d30676f317cac219cfe04e0aba9dd164c3f538950dde0b719a2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-noble` - linux; amd64

```console
$ docker pull clojure@sha256:d43f8a8c60353bc1b4b5dc0404929f599a603cef11fca4ca772509e3d04e9dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208552614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4316b4a1759323ade00c6c3ef235544dd28d7b1402aa23fb3e73044af6de0e96`
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
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='a1d993ab0b4b80101ec2e2452bdd37735572b734c255576a47c5130eab55f09a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d64a00472960835509d7aca644e6f1aa288b1da5b66276bdaaa89cfb795508`  
		Last Modified: Tue, 25 Mar 2025 21:57:57 GMT  
		Size: 29.8 MB (29810691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cca89372c16627655655d29d212f2f05234515758cd5b9221a628de390a9d6`  
		Last Modified: Tue, 25 Mar 2025 21:57:58 GMT  
		Size: 90.0 MB (89956636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e10385d296e036f10239d1b2aa58020cdf5982d5dd6249b22b681df84efe17`  
		Last Modified: Tue, 25 Mar 2025 21:57:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fb79f4cc1c22e0783384f8ae0f095a4e937c2997ea299f39ee41a924799710`  
		Last Modified: Thu, 27 Mar 2025 17:53:30 GMT  
		Size: 59.0 MB (59027640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48ce1c8a2bfa457e6f9b9441260cbc0ddf928612095cfc0b3f85054e46760fa`  
		Last Modified: Thu, 27 Mar 2025 17:53:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c155fb742cdd8c9daf158cecffc5807349b7002f9d6ec96dd8afac0822f9`  
		Last Modified: Thu, 27 Mar 2025 17:53:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:04142411b9729c1cb19af538781795bb09e926f196b10497ce165efadb0da663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5635012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a24c90f34894dfd6f3da68dd8a0d302d42d823621b374789cf9bca4aab97926`

```dockerfile
```

-	Layers:
	-	`sha256:7dec81e2d03a64949cce351e41c955db83ebf1f7d5ba971ac63f901e7d668783`  
		Last Modified: Thu, 27 Mar 2025 17:53:30 GMT  
		Size: 5.6 MB (5619439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb5453a802980d6ab86775b0a889422044ad499e05bac1d6968ef98bb02ed869`  
		Last Modified: Thu, 27 Mar 2025 17:53:29 GMT  
		Size: 15.6 KB (15573 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2e0035a553236b1947a8196356e844c3a746d11805814396ee94e94d1c9df82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207524048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8710619f663708cb9286304528e21e0c64cca5e2dc1f5f4b0b318560a124ef82`
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
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='a1d993ab0b4b80101ec2e2452bdd37735572b734c255576a47c5130eab55f09a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe6ed91129b7d4def6fa771bdde6970a7982e7fad16ae145192b4e16dccf4f9`  
		Last Modified: Tue, 25 Mar 2025 22:03:57 GMT  
		Size: 30.6 MB (30575227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b245a41dc050bf013c4e251e6f42adc662b63845f553dd0f36408eca39fb9`  
		Last Modified: Tue, 25 Mar 2025 22:03:59 GMT  
		Size: 89.1 MB (89093535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64135d99b56097d1ea171c9795be20eb16a29b08259b176721818b12d58a88bc`  
		Last Modified: Tue, 25 Mar 2025 22:03:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc47e35313355fa85ab2a594a246624fa8cbb61868b75e03409a704cf497d1aa`  
		Last Modified: Thu, 27 Mar 2025 18:02:02 GMT  
		Size: 59.0 MB (58958331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568a91705b4e31d797632daefb30dfe35a95e972d6c1a5fb4b3854bc085cd9b8`  
		Last Modified: Thu, 27 Mar 2025 18:01:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76772312aa5029d74b8c317042a26031fc9b738c1b6947449f689fd1f96e53f`  
		Last Modified: Thu, 27 Mar 2025 18:01:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:76548c5b938a8726ab610c5b6d694cced1ded339fcefcd998c6d8b58cd9844e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c99e30cf6f87763c832ffc04e1154fc97c6152df8b97eb8f96a56886a79ce4`

```dockerfile
```

-	Layers:
	-	`sha256:eabbfc0ccbd0d22c2bc28e4935546b14b0fd6c9f41bde95899f1d2e5b567da86`  
		Last Modified: Thu, 27 Mar 2025 18:01:59 GMT  
		Size: 5.8 MB (5757049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf7d88dac0b05b13b07f6c562068e7f6a0048c21723956339fdc73ec6110698`  
		Last Modified: Thu, 27 Mar 2025 18:01:59 GMT  
		Size: 15.7 KB (15665 bytes)  
		MIME: application/vnd.in-toto+json
