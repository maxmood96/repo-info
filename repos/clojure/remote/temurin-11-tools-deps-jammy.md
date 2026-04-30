## `clojure:temurin-11-tools-deps-jammy`

```console
$ docker pull clojure@sha256:c6f73620394755e7669ec930164b48ace67c0bdb0757e6113aeaf42733f3ea33
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

### `clojure:temurin-11-tools-deps-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:bf6ca3cdc6ff8941c40316658634f94637d579e0e4d45839d41937a590421659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242708356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e72813355bc3f4fc37927b7d620544a15ab39c4db68431f5513156454baafc1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:20 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:45:27 GMT
CMD ["jshell"]
# Wed, 29 Apr 2026 23:15:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:10 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 29 Apr 2026 23:15:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6756caac2204f2dcfe0e28fe3d343b925a9e18714e38758e51cbb7035ab4f0`  
		Last Modified: Wed, 29 Apr 2026 22:45:43 GMT  
		Size: 16.2 MB (16150932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba97a1e216602501a222608cca17fe98230eb56fb2f62609db1164208efbbd9`  
		Last Modified: Wed, 29 Apr 2026 22:45:46 GMT  
		Size: 145.9 MB (145894861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbe72533979ecbdbf8386663ba083fbd0d77956a10b565315261a201419cd63`  
		Last Modified: Wed, 29 Apr 2026 22:45:42 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5543a57dc9c2ec9d559b6207e7946c482aa21412666bd3cdfd398e6d14db37ec`  
		Last Modified: Wed, 29 Apr 2026 22:45:42 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70901393c3fa75f57a98f5e657941c10b0085fe412141d460be9969304a40de`  
		Last Modified: Wed, 29 Apr 2026 23:15:41 GMT  
		Size: 50.9 MB (50922975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2895d6663e8de2a05bd1e0278262571bd5b19b78f7833eba465232181fde35d8`  
		Last Modified: Wed, 29 Apr 2026 23:15:40 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:7256001e24a039b6bda090ae7f3920d5a35ab885132ef16be86877b2a8da3097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d049d1722fb4bd6611eef0a297f4af861abfce2fc25e3b895a2ac2e1d81f125b`

```dockerfile
```

-	Layers:
	-	`sha256:6ef95ab3afccf602ffaaa05ec86549eb0db13f7dbc43abd8030ceabc5b395b39`  
		Last Modified: Wed, 29 Apr 2026 23:15:40 GMT  
		Size: 6.3 MB (6323619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af301df2c0dc83a10c5f6a500bd0dc52d2b49fb5a58f4239f07087fe58478fa6`  
		Last Modified: Wed, 29 Apr 2026 23:15:40 GMT  
		Size: 13.5 KB (13508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:11ab475860ec830bcd041b2c0221cd3037f67554fbae729b24dea5c2c72f4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237173276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3d60dae86c28697438888484838ae1f227c7670a6318aa23dae7dc9ba05f8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:06 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:45:15 GMT
CMD ["jshell"]
# Wed, 29 Apr 2026 23:14:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:14:44 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 29 Apr 2026 23:15:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea38cd2682a0e9f5bd923a93115f44d3da2af925a9692421df6e32e020b120d`  
		Last Modified: Wed, 29 Apr 2026 22:45:32 GMT  
		Size: 16.1 MB (16075115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ac5b3fc588803fce69d83176dff89b894f0c5a1b5b14d1a8bc707e6495f3b9`  
		Last Modified: Wed, 29 Apr 2026 22:45:35 GMT  
		Size: 142.6 MB (142588531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a9aed5c5bbca31310b529a69deacd1f167494859e62ef80c48bbd4e90785bb`  
		Last Modified: Wed, 29 Apr 2026 22:45:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0189d752e5a5bd064120c7e8125bcd01b66bf130136867f538dbc9c22ad7bb99`  
		Last Modified: Wed, 29 Apr 2026 22:45:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2571a8c90eb88c4c21fda0776ca9427033ed374cc7fcb487027677b504519ffc`  
		Last Modified: Wed, 29 Apr 2026 23:15:18 GMT  
		Size: 50.9 MB (50899997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddd9a7f109b84c422f0ec858a0a5627dc66171d181e28b685da28fab76e6293`  
		Last Modified: Wed, 29 Apr 2026 23:15:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:c188475a19b72425fcc5d5e0509a16b42d1de80bd46f9e76150a23841ce5aff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6343603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9277387fc00f7a6761e5d7cd1b5ac90563a7a51d9251aee9531e834a6f18212e`

```dockerfile
```

-	Layers:
	-	`sha256:f7c8e68e20d98fe0cacf9284ee55a794e124d920bf9885fdc0d9e424233eec4c`  
		Last Modified: Wed, 29 Apr 2026 23:15:17 GMT  
		Size: 6.3 MB (6330003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c59aeffc11bb2e7a37fd8b8abb9a1514a1b60a7f9ada6bd9c24142b06df0797`  
		Last Modified: Wed, 29 Apr 2026 23:15:16 GMT  
		Size: 13.6 KB (13600 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:6bfb350ea849329d4062347bb08f201b881453e22df5230be692036f2cce016d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240146195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9c8395965b74e44e5fd80106f3088c5d22925fc93e0b8ecaee051fe98292e1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 21:15:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:15:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:15:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:15:42 GMT
CMD ["jshell"]
# Thu, 16 Apr 2026 02:40:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:40:58 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:46:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 16 Apr 2026 02:46:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:46:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daff7109f55b8cc0b7e69fe198543694d719051240d4561b9270b80defba029`  
		Last Modified: Wed, 15 Apr 2026 21:16:19 GMT  
		Size: 133.0 MB (133004428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7379797a06ce2def1e4a142f71b7d8c76bde4197f3015c5c070c364bc8390da7`  
		Last Modified: Wed, 15 Apr 2026 21:16:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2525a18bdf4f76303a1a69b609a60f60bb4bb849a141b500f0fef54d7f121a74`  
		Last Modified: Wed, 15 Apr 2026 21:16:16 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38c3f9d9306c624494dd366759facbea287affa7634b9971840c0eebccf09f1`  
		Last Modified: Thu, 16 Apr 2026 02:46:51 GMT  
		Size: 54.9 MB (54866741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5715badff8842dae70916812623cb4f6a4f2b8a79f9e0b1ae482352348d5a12b`  
		Last Modified: Thu, 16 Apr 2026 02:46:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:26015e18198785ef9f8d3744923e6bd7acca049622944b014f303453e5348069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6341770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a484c16662446f7579c8cb13cc75708b2a83f44086d75b3c344ec13a196d14`

```dockerfile
```

-	Layers:
	-	`sha256:991eb970b02b0ff8d8b28fb13440abeb278f725f9d78d61b556c9510d1b926ab`  
		Last Modified: Thu, 16 Apr 2026 02:46:49 GMT  
		Size: 6.3 MB (6328225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9c19959deb85b08f8dbcececdf23619c97fadcdc39392985ca93ca324599a99`  
		Last Modified: Thu, 16 Apr 2026 02:46:49 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-jammy` - linux; s390x

```console
$ docker pull clojure@sha256:db2a6a238ababf03d6a9039df422da234bd0cae6ad2c2b2eb4970fa7cd941c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221932063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff09595327b033b31744a370cbf625a88cc1477ff991caa7d9b1742a5079e32`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:42:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='3e0ff500a650a552adb2478895ba5de2b133da9b4b816fa76095969b4eec61ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:42:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:42:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:42:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:42:53 GMT
CMD ["jshell"]
# Wed, 29 Apr 2026 23:14:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:14:57 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 29 Apr 2026 23:15:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c51485dd5e5833ab7674e1e5cc519567d9a32213b24543b0a774e065e75e26`  
		Last Modified: Wed, 29 Apr 2026 22:43:21 GMT  
		Size: 126.7 MB (126662254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004cf295eda68a69b582d75d1739a93d10f62fb50290bddd738dd1ceb978b50`  
		Last Modified: Wed, 29 Apr 2026 22:43:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee783b5eb1a8d1bdcb04c45973a7dd441b9c9bdbe392197ec4f1c57f9d15717`  
		Last Modified: Wed, 29 Apr 2026 22:43:18 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8649a10f544e8a8a872db60f82306a509cc805c7c0df89708e3d3806aebd7bfe`  
		Last Modified: Wed, 29 Apr 2026 23:15:30 GMT  
		Size: 50.9 MB (50913912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf38a6948d4a98a737ff177ba27e98fded12264291df46caa05ed38330559c`  
		Last Modified: Wed, 29 Apr 2026 23:15:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:f281dcabe43a7f3f9cfcd2d6ff441104cee008528819cfaa8bf5c815fd2c414f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6333054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5092c84b5a81956aa763c82e707faa6a836341e493f0f48089f5d03679f4006c`

```dockerfile
```

-	Layers:
	-	`sha256:10243cc9c0a8f791e458656d745139d2bd6a59fb9e368cc45b63a5d15a512f13`  
		Last Modified: Wed, 29 Apr 2026 23:15:30 GMT  
		Size: 6.3 MB (6319546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e2e8dff47caa403f8ada510cd3a2279db7f54263778ab19b981c1234fd849d`  
		Last Modified: Wed, 29 Apr 2026 23:15:29 GMT  
		Size: 13.5 KB (13508 bytes)  
		MIME: application/vnd.in-toto+json
