## `eclipse-temurin:24-jre-noble`

```console
$ docker pull eclipse-temurin@sha256:dc420ecfb5590a21ebddfc4ea264cc56affc19fc3d6e48b758db544563b7dbc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:24-jre-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:92d92a4d5c2e9343a1e7a15b4811e1a745f85441dc200a9322a557c7d8062281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105907674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d5c0d29a659af05f3eb6415263499d115801675740b56d13de15b91d4546cb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bee902852ae8b6698e04eb1599dc94af844ae45b72b3b8ec854350b9aba41335';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        arm64)          ESUM='6b06ed1d91930ef86afc7d2159948aa9b3054b154cd8afda35d1fddd158fc11d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64el)          ESUM='de9ec7034fb369ec9b5d12bba9d51984d14d859006e89ef2b86bbae9bc4c7ae4';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        riscv64)          ESUM='4a1177077bc5937ec93cfaaff60fd212a8591af241827869c73f87949a1268e9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='b25ab757f131f965195fd2cb63853299ed6bef268c845283a5a9fff562840fe2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45257b9cd352042e744f22d0f60171c28333a9a9bc982b9ee0a4b113ac11500`  
		Last Modified: Tue, 12 Aug 2025 17:24:50 GMT  
		Size: 15.3 MB (15339492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837b55b79228a4445b27f1ed852a3f312987181ce50ffb5c921199a2011dc202`  
		Last Modified: Tue, 12 Aug 2025 17:24:56 GMT  
		Size: 60.8 MB (60842653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaa4b02646e1ffae2621dbe230c24c2270c0dcfb8005e3f27ac4d9e9818b746`  
		Last Modified: Tue, 12 Aug 2025 17:24:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5a29d659eb602ddb2347cc8dc37b8bb8e4b63fce3f0be67691a87b992ca078c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74aa809c46155b46daba81b18c8e2cda722febba0c49eef5726f58ed6c6ba83`

```dockerfile
```

-	Layers:
	-	`sha256:caa25f3c7016473a1f6bb869c30a28bdd6161c25316cf1957536f176d03ba3f9`  
		Last Modified: Tue, 12 Aug 2025 18:18:21 GMT  
		Size: 3.2 MB (3228595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f232674ca0b576f11a648916b718bed41059c99e26519901f2bee08ca7001e`  
		Last Modified: Tue, 12 Aug 2025 18:18:23 GMT  
		Size: 22.9 KB (22941 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e44ade1a7b83dbf669eb22526aebddaa89a9f8fe253a59e316e747ec3a486101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104080418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d410e27dbf923ea0048e807b5706dcf5519387b1ba684446d3dc855eae7624b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bee902852ae8b6698e04eb1599dc94af844ae45b72b3b8ec854350b9aba41335';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        arm64)          ESUM='6b06ed1d91930ef86afc7d2159948aa9b3054b154cd8afda35d1fddd158fc11d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64el)          ESUM='de9ec7034fb369ec9b5d12bba9d51984d14d859006e89ef2b86bbae9bc4c7ae4';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        riscv64)          ESUM='4a1177077bc5937ec93cfaaff60fd212a8591af241827869c73f87949a1268e9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='b25ab757f131f965195fd2cb63853299ed6bef268c845283a5a9fff562840fe2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5fd5a803e5d0283a8d34ab1172b71cbe06dfbeb5c83252ea70762784967c67`  
		Last Modified: Tue, 12 Aug 2025 18:40:58 GMT  
		Size: 15.3 MB (15332275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a225be7fb47759f2370cc3e9f8163448daaf810806c9d28de09a5bc6f567bc4`  
		Last Modified: Tue, 12 Aug 2025 18:41:09 GMT  
		Size: 59.9 MB (59885451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e554ac2b9884bb827eaedde2d42e4a2e7ac1b8bcf99e9f77295ef57c3e1b704`  
		Last Modified: Tue, 12 Aug 2025 18:40:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6a97069f40689ca1010995ee6e964256eb8de12d3191a99d8ea753a9ff20ddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9142173ac2f40d2e5289a6399abbe9dad68b2b523a68111a016f095f82c36f42`

```dockerfile
```

-	Layers:
	-	`sha256:90c670f03ca71ad7920a18d5d61e85639e3e74fad458530399413f85146b8cfa`  
		Last Modified: Tue, 12 Aug 2025 21:18:15 GMT  
		Size: 3.2 MB (3229053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe9eafc20bf88269a287666d6671091a533697adf60872c493b7602db910867`  
		Last Modified: Tue, 12 Aug 2025 21:18:15 GMT  
		Size: 23.1 KB (23074 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4bc91a5fcea4e5ef1bd8cf4921d1535ee5794206b9c717cbdfd1ef1d6d815cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111765482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224df6b24cf89ba5d4145c427e7a136ee5f06d339e0c1159e0ff306f3da65324`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bee902852ae8b6698e04eb1599dc94af844ae45b72b3b8ec854350b9aba41335';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        arm64)          ESUM='6b06ed1d91930ef86afc7d2159948aa9b3054b154cd8afda35d1fddd158fc11d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64el)          ESUM='de9ec7034fb369ec9b5d12bba9d51984d14d859006e89ef2b86bbae9bc4c7ae4';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        riscv64)          ESUM='4a1177077bc5937ec93cfaaff60fd212a8591af241827869c73f87949a1268e9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='b25ab757f131f965195fd2cb63853299ed6bef268c845283a5a9fff562840fe2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b08a225a0aacf70339a16116ba4f24948e13ebfb9ba345e7b29d37a2db978`  
		Last Modified: Tue, 12 Aug 2025 17:49:09 GMT  
		Size: 16.8 MB (16768157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d15c2140f71bd97161221e4d6c34b08d47da84288080c296553f78e30cae1b0`  
		Last Modified: Tue, 12 Aug 2025 17:49:16 GMT  
		Size: 60.7 MB (60665362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9137d05bd61365c675a64e6949175d8fc86912d5d1d2f21ac79648e538d4b041`  
		Last Modified: Tue, 12 Aug 2025 17:49:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8586f4d7c068f5212d49460e71f3baca9b6bc5c3a32e068b29794adde801d67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3254944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b9743b869439b5f60420739eed8916af3c876ec053b0e8c89a0712f7c9f8eb`

```dockerfile
```

-	Layers:
	-	`sha256:029a15af9435148d25fa981e62e36c8dee520770e5721874c30e42622c519123`  
		Last Modified: Tue, 12 Aug 2025 18:18:33 GMT  
		Size: 3.2 MB (3231956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:066415ff6963c983a2da0632de4ba5fbc16ce8bd991c6b1ea8c29df4b2936dc7`  
		Last Modified: Tue, 12 Aug 2025 18:18:34 GMT  
		Size: 23.0 KB (22988 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:e37a6aaa4bf4103f845a40cab74fae2e20b2e6f8bc696e9fc39df62f651c1c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105603860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6abc8aeda1e4462270bdea555ad770deb1b1a5f051278bdf84fffb7dda45f16`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 07:17:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:17:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:17:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:17:52 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:18:34 GMT
ADD file:07f3c32dd2b7f6af0f399701257442794654b72aa96759b98cb033a715461739 in / 
# Wed, 30 Jul 2025 07:18:38 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bee902852ae8b6698e04eb1599dc94af844ae45b72b3b8ec854350b9aba41335';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        arm64)          ESUM='6b06ed1d91930ef86afc7d2159948aa9b3054b154cd8afda35d1fddd158fc11d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64el)          ESUM='de9ec7034fb369ec9b5d12bba9d51984d14d859006e89ef2b86bbae9bc4c7ae4';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        riscv64)          ESUM='4a1177077bc5937ec93cfaaff60fd212a8591af241827869c73f87949a1268e9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='b25ab757f131f965195fd2cb63853299ed6bef268c845283a5a9fff562840fe2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:b12e9b07091787c99b29dd2be63680c86c47e8be60a46566329007fb82cee41d`  
		Last Modified: Tue, 12 Aug 2025 17:05:53 GMT  
		Size: 31.0 MB (30951577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4a8e441380dc70e1721820397a9620eb691d549f5130646641acb15f7fbcfe`  
		Last Modified: Tue, 12 Aug 2025 18:05:45 GMT  
		Size: 16.1 MB (16109946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff06df8b524ba5273e08e349c552d651dbafceb17f5873a3f0d565a11fe653c1`  
		Last Modified: Tue, 12 Aug 2025 18:05:47 GMT  
		Size: 58.5 MB (58540022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cf8986e7ea6ce642c1ee321330c91415f04adfadf258e3f35526bf864acc9b`  
		Last Modified: Tue, 12 Aug 2025 18:05:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c4c43cab06c25d2af00ca5243a3a702d102bbdd276a107712352722153ca4f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3243609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e44ad081ef603ff4a5b59b4d3c523769a7e9e4ea189a31e5cb6c25ba2ebc4`

```dockerfile
```

-	Layers:
	-	`sha256:3bbe3e45d4dc7640644bc8d7a82936d174742731e89962c74e3a8d1bcf17df7b`  
		Last Modified: Tue, 12 Aug 2025 18:18:39 GMT  
		Size: 3.2 MB (3220620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:146d1546cd709a3fde8be975f91f92724f6fccc2023fbcd6886835af0446f270`  
		Last Modified: Tue, 12 Aug 2025 18:18:40 GMT  
		Size: 23.0 KB (22989 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:69d2b0232429267f36725fa23a7a919deefbc0ac02192ac8dba45d578967e093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103416934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7fe535a859d2ecb8e26e6d8c3de0cb516f4c5036e44be14fb5a8ac0835c3ea`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 06:55:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:55:12 GMT
ADD file:f751959e6b8dae58a35017dc82c7271708f085c111710b59527373699b0784b5 in / 
# Wed, 30 Jul 2025 06:55:12 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='bee902852ae8b6698e04eb1599dc94af844ae45b72b3b8ec854350b9aba41335';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        arm64)          ESUM='6b06ed1d91930ef86afc7d2159948aa9b3054b154cd8afda35d1fddd158fc11d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64el)          ESUM='de9ec7034fb369ec9b5d12bba9d51984d14d859006e89ef2b86bbae9bc4c7ae4';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        riscv64)          ESUM='4a1177077bc5937ec93cfaaff60fd212a8591af241827869c73f87949a1268e9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='b25ab757f131f965195fd2cb63853299ed6bef268c845283a5a9fff562840fe2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1c5d0b18c745fadd2e177b54d4df793f25b01437577bc09c72ae52a0f3f9aeb3`  
		Last Modified: Wed, 30 Jul 2025 11:30:49 GMT  
		Size: 29.9 MB (29932680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfdf93d33f722aadd1ebf516c0f09de8f930b72a2391227592aab06df8fd092`  
		Last Modified: Tue, 12 Aug 2025 17:37:37 GMT  
		Size: 15.9 MB (15874961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3a145ce445b13ded89d2f2adae4c5d712d96f70bfc1c506c8dce4abac15e49`  
		Last Modified: Tue, 12 Aug 2025 17:37:40 GMT  
		Size: 57.6 MB (57606978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20fde4c02c8417d968fc6d2e385f3a65cbc18c4573efdeb67b22e2e54e9e240`  
		Last Modified: Tue, 12 Aug 2025 17:37:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e9cb4f150b46a2612929990f10327246926eb9c2efe7f810e2c6e3fa3e943b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea65e4e1c2910e361b75c5d352ce71323c43b511f35e5afe46d8701ce687277`

```dockerfile
```

-	Layers:
	-	`sha256:eaec91e6ba7bfc3867b8372df7c0208f4d6332a6d8e3c096918bf267ca64cdb1`  
		Last Modified: Tue, 12 Aug 2025 18:18:44 GMT  
		Size: 3.2 MB (3230184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898d5ca2ea13ac2da3c5d73f9aa51b1de638d96f61ceffadb61683a07fc7f097`  
		Last Modified: Tue, 12 Aug 2025 18:18:45 GMT  
		Size: 22.9 KB (22940 bytes)  
		MIME: application/vnd.in-toto+json
