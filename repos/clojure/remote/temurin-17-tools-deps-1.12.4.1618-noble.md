## `clojure:temurin-17-tools-deps-1.12.4.1618-noble`

```console
$ docker pull clojure@sha256:2b3f51033ee8ed0d6efb388eac2cec84d5b93cacde126e7b9bed8f63f61b08a1
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - linux; amd64

```console
$ docker pull clojure@sha256:e031bab628862118254ecdc3908f6044a412676c6749509683671ae678e75103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253496376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f685fe49d9c3be9c7199dcf8d3f219defeb33728a80c24d887e0a7196502a02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:52:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:52:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:52:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:52:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:52:01 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 01:52:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:52:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:52:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:52:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:52:09 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 03:15:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:15:14 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:15:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 03:15:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:15:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:15:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:15:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e6e1a167f1d8e27a6ca55c32fa609912f9ff5b0fc88c77413259b59e72ac45`  
		Last Modified: Tue, 07 Apr 2026 01:52:26 GMT  
		Size: 23.0 MB (22965663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7428f4f5c1dad835231adfcff057cad6efc5b2dc256a36871e2e72cb75561e4`  
		Last Modified: Tue, 07 Apr 2026 01:52:29 GMT  
		Size: 145.6 MB (145633911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a149c623348dfa371df99c86694ffdf860874791706585045a923ea4e6224b0d`  
		Last Modified: Tue, 07 Apr 2026 01:52:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00bd8c488bba663bd5f60752b0a1ac92bc39a10729a5a8bf7227b10f6096904`  
		Last Modified: Tue, 07 Apr 2026 01:52:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09e08284d843e868cf86de83918f0cbbc24e40028bd4577e1b863198df6266a`  
		Last Modified: Tue, 07 Apr 2026 03:15:45 GMT  
		Size: 55.2 MB (55159859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f54be37dd0340d560f7a8c753c3773232f7c90fc7d957bed999a0cc7a62ad82`  
		Last Modified: Tue, 07 Apr 2026 03:15:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022cf234123eacdb1da2c4a12c0cef9e2c82a0274f14e37aa2929629bb6482c`  
		Last Modified: Tue, 07 Apr 2026 03:15:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:57b56bbff3f7f1a323af67ee7f0be8bdea071c07a1ab24a7ad328d0ffcbab654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823c4f9176d5467e7bde7115c9e23558795206e010638840b09496a5745b99c2`

```dockerfile
```

-	Layers:
	-	`sha256:e081639fc9db7027f77c7b8881b2fe727f8d2a0578c90295973b4f25ce865b6e`  
		Last Modified: Tue, 07 Apr 2026 03:15:44 GMT  
		Size: 5.9 MB (5907739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb84ae0d370422ee1b5a100152ed73badc4c1cce45d46ce56115a3bd84e2047`  
		Last Modified: Tue, 07 Apr 2026 03:15:44 GMT  
		Size: 16.2 KB (16228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6a12d4fd71e2baf4d381ce5d41de8c7eb97d6372384923422530f2af88f3103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252598424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849fda5973866810d1deebce270f7e750ba2ed8789bb1e531bd05a875ede90bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:55:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:55:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:55:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:55:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:55:05 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 01:55:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:55:13 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 03:25:15 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:15 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 03:26:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:26:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e985483d507882b395fa9bb8502182df64b567111ba163105e4e78a8d82c722`  
		Last Modified: Tue, 07 Apr 2026 01:55:30 GMT  
		Size: 24.2 MB (24171221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0cae6e26c9a9b0d927c08ce6052f557fbaa85c2077ab4a22f51846260528f7`  
		Last Modified: Tue, 07 Apr 2026 01:55:32 GMT  
		Size: 144.4 MB (144444005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8606cc4933ad0b03f2864748c68cfe3334622c4272c911a96572d71f63064`  
		Last Modified: Tue, 07 Apr 2026 01:55:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec83fb152f23fdcfc782e44dc3257b4fa3dfa349c36f4b978f9fb2dacfa4abc8`  
		Last Modified: Tue, 07 Apr 2026 01:55:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a450b75a5a3c8a731c23be45d47a61198984857ef08d782af3043cd3df8f4e`  
		Last Modified: Tue, 07 Apr 2026 03:26:25 GMT  
		Size: 55.1 MB (55105636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccae612de2d87a6a98a1bf08e5f65b4a8a3cefeea5f875fa4c690a0dc279f46`  
		Last Modified: Tue, 07 Apr 2026 03:26:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837595c48aefd1a7b0a446881b4121474c5f3de3b600d02b7d4ff3b6240c1bfc`  
		Last Modified: Tue, 07 Apr 2026 03:26:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:25716ed61e1cf22b2012fb46aa5b765573d721906012954b1b4b42b6eecdf748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6061721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ec6af766f075b2304c750a395ebe1bf496b970dd6315cb38af352caafaa3a4`

```dockerfile
```

-	Layers:
	-	`sha256:3fdc5f56a5cc77515654ddb4936ec0d2ceeed624389ebe0a95b789226705e3b2`  
		Last Modified: Tue, 07 Apr 2026 03:26:24 GMT  
		Size: 6.0 MB (6045377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f0df1b30588cbdef9cb2b99f19d1b3be36ccd08e1a9b0847b7293469b19f1b`  
		Last Modified: Tue, 07 Apr 2026 03:26:23 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:ce38444c5140d831ea59800b8944d42b5c5098f7c4a7032d3d507fd867b7bb31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263634809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4f2bd91298e862daa6bec94bc14ab19b25edf23d9ef5149e3987bdd3955937`
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
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Mar 2026 08:33:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:33:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:33:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 08:33:39 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 18:26:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:26:26 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:31:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 18:31:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:31:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:31:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:31:50 GMT
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
	-	`sha256:981735c7aae5cc027968590d9086690a597be7eec9c57a90606381bf824c1db4`  
		Last Modified: Tue, 17 Mar 2026 08:34:23 GMT  
		Size: 145.4 MB (145442395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa7346834b8ed9c07a95fb023462ef1c5015bfff5d8c0036630721e610c595a`  
		Last Modified: Tue, 17 Mar 2026 08:34:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81608779243d1bbd3adc7e7ef1e14a32cb93fb173d4ce2e3758f50652952fce7`  
		Last Modified: Tue, 17 Mar 2026 08:34:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071985e29f29a11e518d720cee7b2e87f7028e5649484f2196890a0ae0df2c3`  
		Last Modified: Tue, 17 Mar 2026 18:32:28 GMT  
		Size: 59.8 MB (59786528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d8752e96ce8afba96e2892d1c3938a687b4ca70038c077233a4143caa84e66`  
		Last Modified: Tue, 17 Mar 2026 18:32:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40659df6e091a169a3815bec2c29feaf7d48ee558cefbcfcbaf905bc38729fd`  
		Last Modified: Tue, 17 Mar 2026 18:32:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:38d9771eb8758fc5e36d38e8459345afc5199a6a7e20d10c74514373a5711c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5974871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e92b5d7770b5e8a2aa1776990acf442c58130ac3226b140f400d0768c3ca5ee`

```dockerfile
```

-	Layers:
	-	`sha256:3c8b245bceeaeb0befe94c659e7f3f23b48b9f59f6e340316b342aa287025095`  
		Last Modified: Tue, 17 Mar 2026 18:32:27 GMT  
		Size: 6.0 MB (5958593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07e4e0553dd95a1983f87238be1fd2feea4e8daac791cc5daa6233abd53d8050`  
		Last Modified: Tue, 17 Mar 2026 18:32:26 GMT  
		Size: 16.3 KB (16278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - linux; riscv64

```console
$ docker pull clojure@sha256:de2e46758c3180a847f394aa5a5cd21a1e43635dbd1ca441e7976105cfb5623b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257289440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab6fdc500275b4a0a6324e8357bc6974066eb9496c35e6dda3abced4bc4b604`
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
ENV JAVA_VERSION=jdk-17.0.18+8
# Sat, 21 Mar 2026 04:19:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 21 Mar 2026 04:19:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 21 Mar 2026 04:19:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 21 Mar 2026 04:19:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 21 Mar 2026 04:19:32 GMT
CMD ["jshell"]
# Sun, 22 Mar 2026 18:17:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 18:17:52 GMT
WORKDIR /tmp
# Mon, 23 Mar 2026 03:30:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 23 Mar 2026 03:30:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 23 Mar 2026 03:30:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 23 Mar 2026 03:30:30 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 23 Mar 2026 03:30:30 GMT
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
	-	`sha256:8fc7236364c2ed9474799b78683b9ef6da53a8bf69d5c4b9e04a277ebae8fc0e`  
		Last Modified: Sat, 21 Mar 2026 04:23:44 GMT  
		Size: 142.7 MB (142673726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c462d769f98214739e547d91b2949cfa77b5fed869a43a6cd9d95e5c947101`  
		Last Modified: Sat, 21 Mar 2026 04:23:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafa4523dc56da682e1f8be9d3bfb7e5bec6110dbd107903bef0c239df5b3080`  
		Last Modified: Sat, 21 Mar 2026 04:23:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc34424adc711f75c846dc7896eaff036437bbb9531ff59bc132f30d5a57c9`  
		Last Modified: Mon, 23 Mar 2026 03:34:19 GMT  
		Size: 63.5 MB (63499989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6cf094e08a413649e0c5e42ace894c94d4858338ccec30b02130ae51ebeb6d`  
		Last Modified: Mon, 23 Mar 2026 03:34:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d478f78a8c361613351e0de682309e0ff461c1d0a45ac1e63ca00035c1e0e0`  
		Last Modified: Mon, 23 Mar 2026 03:34:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:a117fba33c0ccd6dc07f8346788e28582d9229d210ca148f01281236813282d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113857db7a586d59f5f24ab47fc9b4273a933ad01f8eeb75f60c4a21b65783fd`

```dockerfile
```

-	Layers:
	-	`sha256:7af6b304d27798de8ee9e3d9bd7e6ba187b2efb76a7946a7ee181084a7353afb`  
		Last Modified: Mon, 23 Mar 2026 03:34:10 GMT  
		Size: 6.0 MB (6009541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e1b298974c46381a7ce24ff66f7e90ea74d33f80ad5ef7ab065b8d048b0402a`  
		Last Modified: Mon, 23 Mar 2026 03:34:08 GMT  
		Size: 16.3 KB (16278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - linux; s390x

```console
$ docker pull clojure@sha256:83be917c9895fe142688bf51d78fac2d2aa81ae665ab7b4513a596f32530ced6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244195212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34491b13cc8261d43bce7b490e4068bafa9d478f31dadcd0354749ab12ad3d20`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:09:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:09:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:09:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:09:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 07 Apr 2026 03:09:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:38 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:43:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:43:21 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:43:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 05:43:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:43:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:43:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:43:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f58d1092e2c2c340321a8297fc8bee6b44f6de56771a16f20395b432a9bd42f`  
		Last Modified: Tue, 07 Apr 2026 03:10:02 GMT  
		Size: 22.1 MB (22127181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cab1876529a2c46d4c5ff9373dca1be01d5b09a9481d774d4c1678f9939c810`  
		Last Modified: Tue, 07 Apr 2026 03:10:04 GMT  
		Size: 135.6 MB (135631395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26556adc0a7bc4a73104e7711f4587b4972c0d6615a86c57bd254a456c7d02ed`  
		Last Modified: Tue, 07 Apr 2026 03:10:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c2c4f36a6cc4f63b88685ec7c3bc548e5eccbbb502670e37c90b8b3c4336be`  
		Last Modified: Tue, 07 Apr 2026 03:10:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1a1d63f4bdba581b9060d7927bbcc879cb37c659dce8e3dab149329116c468`  
		Last Modified: Tue, 07 Apr 2026 05:44:00 GMT  
		Size: 56.5 MB (56521308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e130ae938d9f94cb3d74bce5206e8987efac1f524019b34063ae46591698ae01`  
		Last Modified: Tue, 07 Apr 2026 05:43:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbf9747a8f0aa7f5bade6fe88a07b33b4d09fd18bd8734b2d21e1519a401faa`  
		Last Modified: Tue, 07 Apr 2026 05:43:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:dd34be99173e4eba3c0119b119cc7050fd88c82596b3686c9a3b1ede14455e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42054b3c449ca95d1056e10eb4861c6542993fc4a011ba7059a3c9caf16ba851`

```dockerfile
```

-	Layers:
	-	`sha256:efd8e1b98bd814fb0302c62bb6746dfcb725d2cdfbdc214a1179353e715a4ab3`  
		Last Modified: Tue, 07 Apr 2026 05:43:59 GMT  
		Size: 5.9 MB (5853086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7a36f3b081f7fc9d03a57cd93526131d0352ed0893eaef1b7480a8001ffffc`  
		Last Modified: Tue, 07 Apr 2026 05:43:59 GMT  
		Size: 16.2 KB (16226 bytes)  
		MIME: application/vnd.in-toto+json
