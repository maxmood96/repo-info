## `clojure:temurin-21-tools-deps-noble`

```console
$ docker pull clojure@sha256:3313ebd74004688749a8252657e162ffad803364ca43a89487b9a3dbe67e6e35
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

### `clojure:temurin-21-tools-deps-noble` - linux; amd64

```console
$ docker pull clojure@sha256:8bee4eb104dc59d56886e35d27345f7d11fd361ea9cfaea15ed90d05d00d86e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 MB (265726588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd4606a4fe1bff7515142d6eae4a545c47ac7e5efda6ea4af0967ef881d5d6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:19 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 01:23:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:23:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 01:23:26 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 03:00:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:00:03 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 03:00:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:00:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:00:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:00:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9e66015a4106ba6a33506aa8681e1e826f3acd628c6ef01dcc42970432c062`  
		Last Modified: Tue, 17 Mar 2026 01:23:44 GMT  
		Size: 23.0 MB (22963852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25811b013510224fb88be99e66652561dfb1e6878aced0885c7da14e1245164`  
		Last Modified: Tue, 17 Mar 2026 01:23:47 GMT  
		Size: 157.9 MB (157867645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1a2f3bb5f3b740bf5ee456c4430e1f1cd3944bb8dfd30eddb42c39222cc651`  
		Last Modified: Tue, 17 Mar 2026 01:23:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e1054453cc8ad0c2fc8f173ab87276807c498c0f9856f5ed9c62761776bf51`  
		Last Modified: Tue, 17 Mar 2026 01:23:43 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1f6c5ffe075662151471f20c486c69a83b0f08778d538aee94c0fb1069939`  
		Last Modified: Tue, 17 Mar 2026 03:00:41 GMT  
		Size: 55.2 MB (55159617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f8f828480249bffea5fb13b2beb9427a1a95dda962b36322e12e77941c1ef9`  
		Last Modified: Tue, 17 Mar 2026 03:00:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4faf427d7f827a8465b932b7c15fb91612a621172f3ee7ebed4bc696249420c8`  
		Last Modified: Tue, 17 Mar 2026 03:00:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:5657cac6cf111856790fb6583aede2b303e6a072b8fe12c178926db7a591d24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5924435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b85ca1738f68087a4c524d1733423ff7bc06d4d452ae0909d45fd0849df57`

```dockerfile
```

-	Layers:
	-	`sha256:555400c34f40c291c5d8797ac21050cd2a5468583a03e815789fa7ef0e78a7d2`  
		Last Modified: Tue, 17 Mar 2026 03:00:40 GMT  
		Size: 5.9 MB (5908891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce867bea51f0b8bb6e9d596bc059c30b0d8b1221cdf32128908081cbf5cc6911`  
		Last Modified: Tue, 17 Mar 2026 03:00:42 GMT  
		Size: 15.5 KB (15544 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5acac9062453eab2700a4c1565b12dcadf0a1f431550fdc2c45536ad60233e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264288652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d419f4e9d5d7e3a079f6021ee73847c09403fdbe26b52b6ead2aa1db9c089f1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:24:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:24:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:24:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:24:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:24:50 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 01:24:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 01:24:59 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 03:04:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:04:41 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 03:05:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:05:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9037bd81beb0e70bff52640592f63e192661f73a6a3a8b49648bd8aafbd778f8`  
		Last Modified: Tue, 17 Mar 2026 01:25:17 GMT  
		Size: 24.2 MB (24170398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1c743c5b7ba0fb25e36c3d6f0903b9bef565f53db6ced6873f24d95f0e48c1`  
		Last Modified: Tue, 17 Mar 2026 01:25:20 GMT  
		Size: 156.1 MB (156139422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90ef8e3c48d2c74984b340f12aca394cd704085e3fd8bf2739d6e3a019d9b0f`  
		Last Modified: Tue, 17 Mar 2026 01:25:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f42adf5c10b40811d2213dd9231d004c92cab7d8049b84a72af374cc967163`  
		Last Modified: Tue, 17 Mar 2026 01:24:46 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780b4266e98cac5623fecd5bf9e2184c4505a49b9ea493c404666cb53e63e5d2`  
		Last Modified: Tue, 17 Mar 2026 03:05:20 GMT  
		Size: 55.1 MB (55105637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31581d1a974149a378b1cc3b9cca8f6381a2da255cb20c94da0de58f3192a1f1`  
		Last Modified: Tue, 17 Mar 2026 03:05:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363da2c70fe24a8f7c0afd35726809e23156b3f091e6980cbec8360f794c9e5a`  
		Last Modified: Tue, 17 Mar 2026 03:05:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:5e9c4d77c2832ae5e92bffcb507ebc470cb303ae9c8730d2544acf99b4003085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6062141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4939b3e8be6a2f14ce4dd6f7daaf67071315397402e7edad70d1ee60495cfbc8`

```dockerfile
```

-	Layers:
	-	`sha256:b89ddbfc79bed7a616dccfbec59e3e4a50a55a4b172e3ecdd820a48996af5325`  
		Last Modified: Tue, 17 Mar 2026 03:05:18 GMT  
		Size: 6.0 MB (6046505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927dab31c0842fcfa58789a969cfb2c11f4dd3392e25a7ca82c49f83e28ba73b`  
		Last Modified: Tue, 17 Mar 2026 03:05:18 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:19c194418f616d34bc52347ae1e88e0b5241eaf8c4669e0ab784fac133c575ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276177156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cc619f3e3914519d9fc01f69501df0a6018710af6fc4d80096f674210f1f8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:33:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:33:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:33:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:33:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:33:24 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 08:35:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:35:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:35:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:35:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 08:35:46 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 18:36:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:36:29 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:41:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 18:41:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:41:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:41:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:41:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f48d84a1379a99480c284bdcb27cb684031729c428960f8f7eef01bbcb15422`  
		Last Modified: Tue, 17 Mar 2026 08:34:21 GMT  
		Size: 24.1 MB (24092342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70c6494b9e947653d4c1c9e222d74542e15c7d205d1abea8aa0c6602d8672b8`  
		Last Modified: Tue, 17 Mar 2026 08:36:30 GMT  
		Size: 158.0 MB (157985081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd84675472f5240e583f93b8c76369b5657b404d3706c649fae203c8120b2b6`  
		Last Modified: Tue, 17 Mar 2026 08:36:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fed2851ec3e68a4f019fd7ce3b9d4df751acca66ddc2149119891b791f61891`  
		Last Modified: Tue, 17 Mar 2026 08:36:26 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd5b05625744da58d36b70bb0292f5e59fb4bd4455f80a9e9a04bcb04850f43`  
		Last Modified: Tue, 17 Mar 2026 18:42:18 GMT  
		Size: 59.8 MB (59786195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6b70acd1e112e1edd359512a337d6925ee10c266723a467dde1d2111eec386`  
		Last Modified: Tue, 17 Mar 2026 18:42:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa7901fc25942ad31d64c7fc98e2f78d0b4b904d2ad8a738d74649244bd453d`  
		Last Modified: Tue, 17 Mar 2026 18:42:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:b6ca72aa880db9e067e9da6c002b9e9d19fda4cfc64fb431f1223e0db5d78c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5fa041073cdac3304bc0363de4efbb53e9a30dbf9e286367def1a86ccd1d5a`

```dockerfile
```

-	Layers:
	-	`sha256:70b47b4abb5f60c5282d02fca5f45955449c420df43b660db8d80a2bb84bc8cd`  
		Last Modified: Tue, 17 Mar 2026 18:42:15 GMT  
		Size: 6.0 MB (5959749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343d0565fd5fff54630e0ac7817bcde9eddaaedaf529112a19e502288e645511`  
		Last Modified: Tue, 17 Mar 2026 18:42:14 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-noble` - linux; riscv64

```console
$ docker pull clojure@sha256:2524e6ce8952d118d5a50ec727a7535ea29bea03e717291a33732a2677414fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271839239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3f1a5f66402d23a07a8717a24fc843da0a369242c6d230cb9c0e70932d3981`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:42:34 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:43:25 GMT
ADD file:1243b7db425cac690d91f87ad37c1beec0d95da6b3942dc8084039fe1cc2baf4 in / 
# Mon, 23 Feb 2026 17:43:30 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 04:18:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 21 Mar 2026 04:18:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Mar 2026 04:18:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 21 Mar 2026 04:18:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Mar 2026 04:18:24 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Sat, 21 Mar 2026 04:30:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 21 Mar 2026 04:30:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 21 Mar 2026 04:30:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 21 Mar 2026 04:30:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 21 Mar 2026 04:30:28 GMT
CMD ["jshell"]
# Sun, 22 Mar 2026 18:44:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 18:44:30 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:04:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sun, 22 Mar 2026 19:04:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 19:04:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:04:23 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:04:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866473980fd7aa6ac5a8a995315a35248ab945008a1938bd15f65082df53b2d3`  
		Last Modified: Mon, 23 Feb 2026 17:51:46 GMT  
		Size: 31.0 MB (30960145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea89a3ea977fd63adb61a466e753cd0923dd91e05938e9b091167d52191765`  
		Last Modified: Sat, 21 Mar 2026 04:23:25 GMT  
		Size: 20.2 MB (20152089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee2f392cf730699f57d1e2d6a62ae7087c2f456e187f209ef1b84a71d51a5cb`  
		Last Modified: Sat, 21 Mar 2026 04:34:50 GMT  
		Size: 157.2 MB (157223326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5fbcd7f77867ae69302e66ca92374245e971dda280d8047f0bd4eb7559c193`  
		Last Modified: Sat, 21 Mar 2026 04:34:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17683dec12cf962906abb5962b9b61e610b217c08fade81ba0d0b33efc2177`  
		Last Modified: Sat, 21 Mar 2026 04:34:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078935a5e4888153a0f3df6780ac66dfa9a54e70c759169cbc176e9d924ccd30`  
		Last Modified: Sun, 22 Mar 2026 19:08:25 GMT  
		Size: 63.5 MB (63500184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d727b1b7449a7245c3fdbbb8fb86fb24204d423ec8b7fc8d3c3aea9155ed5048`  
		Last Modified: Sun, 22 Mar 2026 19:08:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b4b877fd7100021a46e9d5cece9d8f6b729fbe84d78d9ff0b5cfe2d4b22ce8`  
		Last Modified: Sun, 22 Mar 2026 19:08:14 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:51524e7d7f93aa983e469028ddfd72c85f6629ab62579fa138913b81c34d7964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6028198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f64c2dd5619abf017de156aeaa37e0af2cf84038da5e7f97effeb22a4b7c425`

```dockerfile
```

-	Layers:
	-	`sha256:00da4b740c3941339548aff8e44f098c45d117dd987f89f4c8a0f628566fd8c6`  
		Last Modified: Sun, 22 Mar 2026 19:08:16 GMT  
		Size: 6.0 MB (6012616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48ac7939b124090b0b1298e146efd261c25959eef162fd235e694583a070296`  
		Last Modified: Sun, 22 Mar 2026 19:08:14 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-noble` - linux; s390x

```console
$ docker pull clojure@sha256:bac31d2fce26ccb8e86d41c0fc8fd2f60deb034b27c50b1d034b9816255f81f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255672795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c5d4677e16e13d7753aa000794f90108eb149df5fdeaf52724c47d83fe761c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:22:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:22:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:22:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 02:22:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:22:46 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 02:22:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 02:22:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 02:22:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:22:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:22:54 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 11:41:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:41:33 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:42:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 11:42:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:42:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:42:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:42:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352a520f98da0ffcd43cf05ec54371270c23fa95d34702e96f4b9da9cc94834b`  
		Last Modified: Tue, 17 Mar 2026 02:23:20 GMT  
		Size: 22.1 MB (22123462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e9c5c47393cd5467dce3002a83355ec401a73958076cd4d7970322a2074eb5`  
		Last Modified: Tue, 17 Mar 2026 02:23:22 GMT  
		Size: 147.1 MB (147113703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ec4c7ba0ad6b0f45d33fb33b4e49fbed8aea475cbb45f7c92a0e425a8c3f6`  
		Last Modified: Tue, 17 Mar 2026 02:23:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cea839abc61d7f4f82a41a8b2b767ec360be280f4e2660b24e86c755c3f5303`  
		Last Modified: Tue, 17 Mar 2026 02:23:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d57665595926048bf5510bde6e96f762094b8a5a51b862bd8602d304ddb9c5d`  
		Last Modified: Tue, 17 Mar 2026 11:42:36 GMT  
		Size: 56.5 MB (56521757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f53fdd8237697105296f39ed80e6debc53d315d0b8f1cce4077dd9c62c60c`  
		Last Modified: Tue, 17 Mar 2026 11:42:35 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8cd5d366c7121900592aae2fb44eaf206a6edd05c022991398beaf658fce53`  
		Last Modified: Tue, 17 Mar 2026 11:42:35 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:8d254d21f7f5310d36d34789083ea0c847eeff0cd4e7ee602c7709ec4892aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be18d0f12483ecc21249c18a2a99754705e0d35c236713d4758e4933e77763bb`

```dockerfile
```

-	Layers:
	-	`sha256:906a242bc12d62f5949e70b6e5b44a664312516378fb456314ac389b34c10e88`  
		Last Modified: Tue, 17 Mar 2026 11:42:35 GMT  
		Size: 5.9 MB (5854240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cfa156c97e5dd957cd883287ac1dbf83a418c626700b5649e6bacffe7d458cf`  
		Last Modified: Tue, 17 Mar 2026 11:42:34 GMT  
		Size: 15.5 KB (15543 bytes)  
		MIME: application/vnd.in-toto+json
