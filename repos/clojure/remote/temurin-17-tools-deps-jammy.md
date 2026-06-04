## `clojure:temurin-17-tools-deps-jammy`

```console
$ docker pull clojure@sha256:218e8611772600b1fcc7f58c5c7a30cc7e3abb3a24d5f9b6a34189f917bb1853
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:b088263748dc08281a31220ae9e7b3833adbc40348a67ea36c00f09c78f8e057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244214092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c09c82b3bb65317b6537d3e45543265fcd6f5f1897f9771a75e319d2efaed4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:15:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:15:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:15:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:15:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:15:47 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:15:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:15:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:15:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:15:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:15:55 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:45:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:21 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 04 Jun 2026 17:45:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909fe7dc1afc2b7c2ce46b1d0166713560a7d2f913022d4e991dd6d98701a2b3`  
		Last Modified: Fri, 15 May 2026 21:16:11 GMT  
		Size: 20.7 MB (20696952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937c31685fefe899abb3e773bf9e4fea73fcbd2cc6f2e126fe41ac4a69b28397`  
		Last Modified: Fri, 15 May 2026 21:16:14 GMT  
		Size: 145.9 MB (145912351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ba0d2efe79548df209692310f9d4cc47306c76336e362f4f125b29470ab56f`  
		Last Modified: Fri, 15 May 2026 21:16:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb50d9aa1fdda8a54b2787672840c41a0cc1165e14d3f515c888e3cde82ffb`  
		Last Modified: Fri, 15 May 2026 21:16:09 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d01da41126ba451df6163fa880112e320acd887d127a24e69c22871c708198`  
		Last Modified: Thu, 04 Jun 2026 17:45:52 GMT  
		Size: 47.9 MB (47864619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5630d7e3c27f6417a169f5bb663fff99e9f66346aed936b88837fdf86aaf368`  
		Last Modified: Thu, 04 Jun 2026 17:45:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080f59747056c192369f89f5689bccd8970838c703acf8ba57ce3d98478a6e81`  
		Last Modified: Thu, 04 Jun 2026 17:45:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:311b9bc88446c2433cb24e61c6bcdf29894075a88e59348360e05d2686179ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6476537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c34ad2ef0e7cca7e77c76b56462a1a2925edf3c3299186c50ea55dafb66483`

```dockerfile
```

-	Layers:
	-	`sha256:ca3da895955a21ca954c9599fc5977aed801f767357169ea194882940edc4011`  
		Last Modified: Thu, 04 Jun 2026 17:45:50 GMT  
		Size: 6.5 MB (6460992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f9e7dc6bb6adbe5182e08411b41bdb63d5b3429e8e2494327b2f208537f69a`  
		Last Modified: Thu, 04 Jun 2026 17:45:50 GMT  
		Size: 15.5 KB (15545 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da7eda24bea4ef0fde6da434847d8a69545cdbeeca4223fd6912748b6608bd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242302137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85e1c30b75fda3b5b6909742d1cdaf1c1635b6573a00d0004ee17618fcf41f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:16:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:16:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:16:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:16:20 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:16:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:16:29 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:44:58 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:44:58 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 04 Jun 2026 17:45:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bc8906a7610c5b0a4df49ed0c81a0753ae645c3b3d827930f9e97113bd2c00`  
		Last Modified: Fri, 15 May 2026 21:16:47 GMT  
		Size: 22.1 MB (22110130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44773ebf0b26708d3c1a138319ca2dfc1dea75e131eb674bbea177043ac0460`  
		Last Modified: Fri, 15 May 2026 21:16:50 GMT  
		Size: 144.7 MB (144741869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af9943ce0bcdad9ab8323df7c126e54f6dbd8374052a398c962c880573588b3`  
		Last Modified: Fri, 15 May 2026 21:16:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ae8d3db94381716ad314cd2a45c3486c7c18b7eb32c026331be40f76fb6e8f`  
		Last Modified: Fri, 15 May 2026 21:16:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9506371bc1eba00a93a9d54762c5a81875bf04e0a4e7d0699e06604e39e126ec`  
		Last Modified: Thu, 04 Jun 2026 17:45:27 GMT  
		Size: 47.8 MB (47840028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5944f97eab56bb7c66d65828753fef2483234662af7af29dc31790bde5eded8c`  
		Last Modified: Thu, 04 Jun 2026 17:45:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d154153a8b294c8bcdaa19686119922a722ed025d7e331d51d48ffe4ae371d96`  
		Last Modified: Thu, 04 Jun 2026 17:45:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:ce70310b1f1a22ac2e15fef4161c5f8a6bcb5077b97624922628ef1d41a29bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6578197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad4042fb2c6d9ac10da71c9190944499b46322489bf1b536787feb5644faa55`

```dockerfile
```

-	Layers:
	-	`sha256:7ca164f26956cae8b64b07b79f23f2afb6ae5e01a67c869bb4defe395e896e69`  
		Last Modified: Thu, 04 Jun 2026 17:45:25 GMT  
		Size: 6.6 MB (6562560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae4a7679460b9c1c0c297c4b031a4c8884f96ae7468d726d7acb14c980e3ae1`  
		Last Modified: Thu, 04 Jun 2026 17:45:25 GMT  
		Size: 15.6 KB (15637 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:0ad5f1eb6df3f3a08fb86d31b642080b7328df2bc395625124c13ca228262e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254825981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d04f88f6e2c197f7169631d55e66fec655d377d681a47f018144b60fe3e51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:12:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:12:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:12:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:12:31 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:12:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:12:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:12:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:12:45 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:54:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:54:23 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:54:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 04 Jun 2026 17:54:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:54:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:54:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:54:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ba0627ad64b0a6b1ebf88e18bcc537d7ccaf8ddfb659f50480d115f4660520`  
		Last Modified: Fri, 15 May 2026 21:13:21 GMT  
		Size: 22.6 MB (22589674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccde48847baa039e482b5a40c28108c264b0836efc8273fd6129013727164050`  
		Last Modified: Fri, 15 May 2026 21:13:24 GMT  
		Size: 145.8 MB (145773796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7253369a6abf18b9171f1221e5b46f0c48d97181e284e3df6ef53f33d248de8b`  
		Last Modified: Fri, 15 May 2026 21:13:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c539817e8010f3f18434713ca4911e7a7c6eb473e295887c368508793e0eb`  
		Last Modified: Fri, 15 May 2026 21:12:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba57c9f1a84645a0322e93a9b1f48037e74356d7e7965809bd552bb71840b31`  
		Last Modified: Thu, 04 Jun 2026 17:55:22 GMT  
		Size: 51.8 MB (51812303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525d00c2b4da948ebe90228a146c50cf8323e3c374c19c793fa85092bc8632c`  
		Last Modified: Thu, 04 Jun 2026 17:55:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bcc2b285666d880c46853b1164a46325915a02f491978b9c380b4f2bda17e8`  
		Last Modified: Thu, 04 Jun 2026 17:55:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:42374734ff6c406b49bce8131293325a219bd231b03f154691524f11d951da3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6507188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bad43a4724b51eb856c07e6a593002beb16a7917d94db81eed51f3cc324a7e2`

```dockerfile
```

-	Layers:
	-	`sha256:ca7911d1139960cbd81b09f83ef5c95f8502e670d9302f88fa57fd06a476e5e0`  
		Last Modified: Thu, 04 Jun 2026 17:55:20 GMT  
		Size: 6.5 MB (6491605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c017f69aba0ea016981c9fc750a4a6089ecd8e93d20c7e89e60c74561c9e32`  
		Last Modified: Thu, 04 Jun 2026 17:55:20 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-jammy` - linux; s390x

```console
$ docker pull clojure@sha256:017c8d8ab594381776cd3ac2e71230505e064ee61c5ddcfa0cece34f93592bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232398773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed26431a8cfc5ab3485c2c8eab22d6ecef03b9b98f7ec307f0c85d524d369ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:12:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:12:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:12:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:12:42 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:12:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:12:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:12:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:12:56 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:42:46 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:42:46 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 04 Jun 2026 17:43:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:43:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:43:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae77d3b5f2cc94fd4e05c475655187c63284802cb4d3d3bf62e4de800a5ca60`  
		Last Modified: Fri, 15 May 2026 21:13:33 GMT  
		Size: 20.4 MB (20419503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc78ef64a42cf04e89b70e62492e4ce4e2cb215eadef27e7217f92bfaef439bc`  
		Last Modified: Fri, 15 May 2026 21:13:37 GMT  
		Size: 135.9 MB (135919301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7ea29159b5fa1e507623a8485a25db8fc1decc03e96d20c1f5bedada985127`  
		Last Modified: Fri, 15 May 2026 21:13:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a8ffe1ad79b6ad54f5963ecdc3367f8256404e487fe328ab2d34279fe75997`  
		Last Modified: Fri, 15 May 2026 21:13:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84579aecf13c68348376eddf4c766a3888ca4380197f3c8e8ee045147c6f9e5`  
		Last Modified: Thu, 04 Jun 2026 17:43:27 GMT  
		Size: 47.9 MB (47854177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e459216806fa078a076b96016d3b26cc561fc7a6c693fe0e24a5751019119dac`  
		Last Modified: Thu, 04 Jun 2026 17:43:26 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce8c56a28d910a020bc754183041a3766481fe8b97c31d1cb032c096aeff6f7`  
		Last Modified: Thu, 04 Jun 2026 17:43:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:90b6b2c2092acecc03c0be7ce6ab64ce8a662c9b37d2e863617c4ef657d32b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff2781ef92f154484d7fae7e092ccb5c68a20641e74d046004644d8692becee`

```dockerfile
```

-	Layers:
	-	`sha256:d6207ef9a4f09dd74d6ea492da62a9c3d0df9706647516f1308469f08a5baa38`  
		Last Modified: Thu, 04 Jun 2026 17:43:26 GMT  
		Size: 6.4 MB (6384719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7516b86bf9506e1f2e8eec8eeb0b852003f6bd9ccb3881a318302b6ba021290c`  
		Last Modified: Thu, 04 Jun 2026 17:43:26 GMT  
		Size: 15.5 KB (15545 bytes)  
		MIME: application/vnd.in-toto+json
