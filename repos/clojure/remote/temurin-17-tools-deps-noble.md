## `clojure:temurin-17-tools-deps-noble`

```console
$ docker pull clojure@sha256:2f5248ae87f5ae17a7f3955cb61b1937fc5dc5a9bc02876c3c97bbc4389f9d74
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

### `clojure:temurin-17-tools-deps-noble` - linux; amd64

```console
$ docker pull clojure@sha256:3d97848a8ba920d88decbb9813a6f28de2c488b448ec192220bb15232d25efb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254031098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632184115f8bb0a57ce5713b871e1e9bb6df4e075db5d7d7118a2498a4e922b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:19:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:19:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:19:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:19:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:19:39 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:19:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:19:46 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:46:50 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:50 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:47:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:06 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f3ac7b458bcc0853b8cddf5bb91d305f64732b5e46f7897402e9104a2b6c7`  
		Last Modified: Tue, 17 Feb 2026 20:20:03 GMT  
		Size: 23.0 MB (22962446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbcf5688c1943d868111317459775672c2eb59c07b04633f4653e36deaac799`  
		Last Modified: Tue, 17 Feb 2026 20:20:05 GMT  
		Size: 145.6 MB (145633930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78395afbc5ebce60b7dff0200af60f0f3df93dd724ebb8f148212ed7d9b243e7`  
		Last Modified: Tue, 17 Feb 2026 20:20:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88562ce968f9f2742decb2b41610942b1696ea2c5e3d23e5a6d4d60c881435`  
		Last Modified: Tue, 17 Feb 2026 20:20:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab545b83e36bc827ee3fc19bd8193a313d38355143ce43252a7a7651d8e0016`  
		Last Modified: Mon, 02 Mar 2026 19:47:22 GMT  
		Size: 55.7 MB (55703625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e560594d46129de967622788612a76e93ba21f66498cd79ed0a5c42eefbd9f66`  
		Last Modified: Mon, 02 Mar 2026 19:47:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d10805e8e6e8a69768b4d6ecf88f7f6b3024d547fcdeb1a5252b6a757fec3a`  
		Last Modified: Mon, 02 Mar 2026 19:47:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:a67e281d0a0d748067244debf15aa5affe015268fc248df3bd8b8c9ed42e8a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86247aa99cedc9290e1fe9e4a096db7861489d876fde65cdb0bf7c8dfb554027`

```dockerfile
```

-	Layers:
	-	`sha256:c6a93e25445edaca781f611f4a7c27b068fe5c8266f94f13578fa9d7acdaa0ac`  
		Last Modified: Mon, 02 Mar 2026 19:47:21 GMT  
		Size: 5.9 MB (5907695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86de2b09a0ac09756b55c12aa28968f3f5fd7b0a686f094aa94482f17eaf0f25`  
		Last Modified: Mon, 02 Mar 2026 19:47:20 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c5949820905f6afda53680bfe55bb352de1b78b01a5db933efcc1228a396c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253125527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a8d2e295e7872d4fe66b9c86617752ef8025281ec319985bdd421a605b5b5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:19:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:19:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:19:10 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:19:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:19:18 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:46:39 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:39 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:46:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:56 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eac264d5df3e5eb1611554c669ffd726b07509669fe4411c456ad62c8b7c56`  
		Last Modified: Tue, 17 Feb 2026 20:19:36 GMT  
		Size: 24.2 MB (24167692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55071af2ac506944e21770c81b651f5847488178ff0b8c1a20af67215fa4af2f`  
		Last Modified: Tue, 17 Feb 2026 20:19:38 GMT  
		Size: 144.4 MB (144444038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1777e35d8796120890d06a7d8a9a53285fb384b677055548643f669b12f7a58`  
		Last Modified: Tue, 17 Feb 2026 20:19:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9731669689e82e918ab1cb1cbda39d05b6eb9bc7544f6f9d0ea3e41a4955015`  
		Last Modified: Tue, 17 Feb 2026 20:19:35 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6cfcee92daf04d78cc9494778e99ba934e8a16b60d637cb89a6792568cb2a7`  
		Last Modified: Mon, 02 Mar 2026 19:47:12 GMT  
		Size: 55.6 MB (55645186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c31a8b85da871fa6965bcb12e0893d9326afbdd3e1348c0cd36182c6f2519b9`  
		Last Modified: Mon, 02 Mar 2026 19:47:11 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e9a7d7104599ac1e05de47c1d59f74aac64e28f2d61b54f318a661a8a69ea`  
		Last Modified: Mon, 02 Mar 2026 19:47:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:0346a4e4929d6c0ee3c58f209c24973b0c2502d40ef877be3fcae6d9a8d66615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6061677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64f3db68e330411974606f131d05a2d7bc19119e17d35250d67304a47aa6b11`

```dockerfile
```

-	Layers:
	-	`sha256:20cd8a13c3677131feb29a983718ef74118a9438b640d1bf570a84244719e6a0`  
		Last Modified: Mon, 02 Mar 2026 19:47:11 GMT  
		Size: 6.0 MB (6045333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada62dcd6327b97885b2648a981e5193fc8d570ceeca1415431f20f8c80fb390`  
		Last Modified: Mon, 02 Mar 2026 19:47:11 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:044bd8dc7cd1f272e41e5223638bda65cb99824552f55a58ae04d47c4a13c55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264324059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfc52825df0b703d65bb7eef7ab3ac1308b98db7fd8c602774508ce1618d1f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:26 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:18:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:18:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:18:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:18:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:18:42 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:58:02 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:58:02 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:58:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:58:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:58:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:58:41 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:58:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6703b8ece0ce217ed67aed2176638b1c0350e7c03037dcb896534a4ce5717701`  
		Last Modified: Tue, 17 Feb 2026 20:19:22 GMT  
		Size: 24.1 MB (24105013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b51b4d285c18057ca2953badeb4295cedd2dbb9de0040649b364e75308c449`  
		Last Modified: Tue, 17 Feb 2026 20:19:25 GMT  
		Size: 145.4 MB (145442153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56e0d963cecc750cd56528c0fdc8dca07e42a8c364451325464e5634c550806`  
		Last Modified: Tue, 17 Feb 2026 20:19:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373d81525a1ef425261ca57b59de8a8b189e892f1e63410a0f33e22a80829e8`  
		Last Modified: Tue, 17 Feb 2026 20:19:21 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175201fab4e2b07a7217c14a9d4383f85bb8e81e67592ec973207aeb2961e12c`  
		Last Modified: Mon, 02 Mar 2026 19:59:23 GMT  
		Size: 60.5 MB (60466502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1a10031d289d590bb645e1dad623c2f9433cca50d8e2fcff2394f9b322f728`  
		Last Modified: Mon, 02 Mar 2026 19:59:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce0315902cddbd041c37b817353c5bbf473108d8126ab2f747c164b8369ec93`  
		Last Modified: Mon, 02 Mar 2026 19:59:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:83a3e4b3d4d44254daf19faef630882ab2d709e62a52d5d6c3450db348e991c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5974843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345f13b7e620b6124ef281d18ca8a6fd95e8c2991dec866df2251ec7b611ba8e`

```dockerfile
```

-	Layers:
	-	`sha256:6dab24cea54125b25c1e4cbe0fcbed15846f300ed366cde73873f9bacb7b4807`  
		Last Modified: Mon, 02 Mar 2026 19:59:22 GMT  
		Size: 6.0 MB (5958565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e39a6a12270ab0741c65c5f89b1b7055f1ce60296d73ad3a41655272c02c55`  
		Last Modified: Mon, 02 Mar 2026 19:59:21 GMT  
		Size: 16.3 KB (16278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-noble` - linux; riscv64

```console
$ docker pull clojure@sha256:86e2936f0c2a6957735fc7bef6fa6c5fb2e32d273dcdd7d7705becf7c66d5a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257261813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad963f4399fd17424be94e4ae0abf3284b7a7f5bb0d76e49e035b067da29d3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 10 Feb 2026 17:33:09 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:33:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 17:33:55 GMT
ADD file:b4821892707dbb5cc8e8eb3b4e757edc2d124db81fcdedfc3b244dcb5c1fa6c0 in / 
# Tue, 10 Feb 2026 17:34:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 23:55:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:55:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:55:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 23:55:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 23:55:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 23:56:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 23:57:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 23:57:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 23:57:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 23:57:10 GMT
CMD ["jshell"]
# Wed, 18 Feb 2026 10:15:32 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 18 Feb 2026 10:15:32 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 10:35:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 18 Feb 2026 10:35:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 18 Feb 2026 10:35:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 10:35:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 10:35:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2683d5e2cbe038b4f1178e139d507e705e0a3a566f8b9c89bf3484f426119af`  
		Last Modified: Tue, 10 Feb 2026 17:42:05 GMT  
		Size: 31.0 MB (30954431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614295373cf4c3ef1337c5a5d4db707ed77d979783528ade7ef2348217817a9f`  
		Last Modified: Wed, 18 Feb 2026 00:01:21 GMT  
		Size: 20.1 MB (20149150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701f885e07aa43d93c4a16212cf99d9295dfb6fb82dd649910db461caab430fc`  
		Last Modified: Wed, 18 Feb 2026 00:01:39 GMT  
		Size: 142.7 MB (142673620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69891d9ddc34168c5dc5ea12e24b536ea05f9e35edcb8a7cda4a5de2343947ea`  
		Last Modified: Wed, 18 Feb 2026 00:01:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e07c306dd6c3a49cc23abaf5d962ae796801e8ea8309fc7af13936210fc2a6`  
		Last Modified: Wed, 18 Feb 2026 00:01:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87bc3f610895739cc73cbfe2d016d4f1c2d70f087378c497e40efd3ab1d0179`  
		Last Modified: Wed, 18 Feb 2026 10:38:48 GMT  
		Size: 63.5 MB (63481124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbbca9b9500b46506e094bb28e66863cb5dcc05e4da8c7a8f714ea644b1b61a`  
		Last Modified: Wed, 18 Feb 2026 10:38:37 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203cc5d39f86fc78c84e945091937d09920b929770e4dca5efad633cfd1e40bd`  
		Last Modified: Wed, 18 Feb 2026 10:38:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:893bc3718d8c49bd91fd56927d6faf48e4b368d38520d0cde7a5112209096e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6024264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49b4914c41a138031a4e49bd95be40e803c5a92fc10e6cdad6a5d77126d6cc0`

```dockerfile
```

-	Layers:
	-	`sha256:3a62e6d044adbc72819d6cb822e15a733dec42aa11e1b47634fe7d0c3d5c0c47`  
		Last Modified: Wed, 18 Feb 2026 10:38:39 GMT  
		Size: 6.0 MB (6007986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff03cd1351a7fc084725218e5f48348a315f54aa331c101c2cb84297225bd30d`  
		Last Modified: Wed, 18 Feb 2026 10:38:37 GMT  
		Size: 16.3 KB (16278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-noble` - linux; s390x

```console
$ docker pull clojure@sha256:85cd0544b1ad5167aa04f360bfb0c9f9a1e0a89fce1d8d3ac6da6da4f65df1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244758748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58378316db4eb3e2a0371f804fcc353b5a8a1cf8de264787c6b073029471658c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:13:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:13:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:13:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:13:16 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:13:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:13:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:13:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:13:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:13:23 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:46:15 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:15 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:46:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:26 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c61c0dceff600fa73a9e5c4c1e6b5bd67c056a803cadf4663f05f037f3b413`  
		Last Modified: Tue, 17 Feb 2026 20:13:59 GMT  
		Size: 22.1 MB (22132300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a2b165a5fba8af9a2e977c81f301b9d7c5419451e10e73cac02e889467deae`  
		Last Modified: Tue, 17 Feb 2026 20:14:01 GMT  
		Size: 135.6 MB (135631870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd81daff4e2f95b8488e3f8a8b906c21526856272c6e595a95f9e11f7e2b324`  
		Last Modified: Tue, 17 Feb 2026 20:13:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c3dd95c98dc1182338a43a3c388dcf56e1e4ab3a398575d60aa93eaf9fe7e`  
		Last Modified: Tue, 17 Feb 2026 20:13:58 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68a388149a66b9e09e827c92e17b50c2d1147bf19d416e95e0dc826cc9c4893`  
		Last Modified: Mon, 02 Mar 2026 19:46:52 GMT  
		Size: 57.1 MB (57081309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1493cac11941d0c746e3a0173129c53d71123ffe0447397e7bb1eeb4b822ee3`  
		Last Modified: Mon, 02 Mar 2026 19:46:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b79b6db3e03fd0d5d4bd366e7faa7db2f68a1bad3b16db07bb146d06fd76f6`  
		Last Modified: Mon, 02 Mar 2026 19:46:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:084b07709c09de22aff1b16c70c1934f993005927352f0d4308301feea3a86a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b027d88b8a566ce01f1470a0d261fcc6b047dc47d5114fa73382674e36eed5`

```dockerfile
```

-	Layers:
	-	`sha256:2319b0b3d5748ea5d8cc2b35de96a96cfe5e4564894c56fb35770fff2eb8b3a9`  
		Last Modified: Mon, 02 Mar 2026 19:46:51 GMT  
		Size: 5.9 MB (5853044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57a117431c38372e3e416c21c562163ba0414bd8b770d15fdcfe714545f855b2`  
		Last Modified: Mon, 02 Mar 2026 19:46:50 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json
