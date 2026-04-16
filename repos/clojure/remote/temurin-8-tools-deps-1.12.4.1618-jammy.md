## `clojure:temurin-8-tools-deps-1.12.4.1618-jammy`

```console
$ docker pull clojure@sha256:f0aa517206cbceada7fa413c3ac0d2e9a9a6a913adb72c2b873c299dac1db7b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:7e74ac05094cdefaa05f003241a3b9c70711ac845481e77397594669da508d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151984285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9618416c8f9b16240fa41f55c53e1e547a64462f475379cd6c460b2422b595f`
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
# Wed, 15 Apr 2026 20:32:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:32:21 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 20:32:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:01:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:01:49 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 15 Apr 2026 22:02:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:02:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b699ac82f8f4bc202667b93bb403fa63a9d1637ce1f8fa60f2e6adceb8bf6be8`  
		Last Modified: Wed, 15 Apr 2026 20:32:38 GMT  
		Size: 16.2 MB (16150818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfae8fec46c3d37535117b69a93963943ff3e3de751e2aa89287f69ec47171a`  
		Last Modified: Wed, 15 Apr 2026 20:32:39 GMT  
		Size: 55.2 MB (55172941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d393a668fd7abdb353104b0fce5968b214d5ac3ff3cbb65251bdfe6116b21b`  
		Last Modified: Wed, 15 Apr 2026 20:32:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2b0e71db5598e689453f02b98ac96955ee8ed91cbe61b6272a4122020be927`  
		Last Modified: Wed, 15 Apr 2026 20:32:37 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc271e45ee24e38f9cd73899a74a25aeae85b95b593730d63aaa14bd58095b28`  
		Last Modified: Wed, 15 Apr 2026 22:02:23 GMT  
		Size: 50.9 MB (50920947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87eff37371df62678e23886ae0247d553f6811d8df15063e3783c1d6e10299a`  
		Last Modified: Wed, 15 Apr 2026 22:02:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:8268e023b01495cd3ba7dc75fcfbecc3aefb71b5e4508a90bbd68802e4076227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6437955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd1936fda97b77979fbc3ab2061baa94f1e52ae0edd0ac2d85b6ad3812abc16`

```dockerfile
```

-	Layers:
	-	`sha256:e994187c2668b8548c4ca6b5c13063bbd2513c8d9533ba2b3fdad40f7f52c753`  
		Last Modified: Wed, 15 Apr 2026 22:02:22 GMT  
		Size: 6.4 MB (6424463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c9bf681ce79a4f60f515aafa05bce93b434906d79477ff91d1ab7745ec729c`  
		Last Modified: Wed, 15 Apr 2026 22:02:21 GMT  
		Size: 13.5 KB (13492 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d45164075f77edfd8f49a80ab403aac41d2c1744b156568d06514a7efc22fac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148845690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d53e21aa807d22b611778ee2ca206e213ead0d9b89002a40a70baf72854150f`
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
# Wed, 15 Apr 2026 20:32:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:32:43 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:12:55 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:12:55 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 15 Apr 2026 22:13:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:13:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a116ac60a9bda7df2aa8d5f8c599e43b76fc505884b313fa5a950252ed9b69`  
		Last Modified: Wed, 15 Apr 2026 20:33:00 GMT  
		Size: 16.1 MB (16075202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53614aca3bb32d1a5095ef396c08b4a7292999ad4a296c5ef9f8a53222ae5e3b`  
		Last Modified: Wed, 15 Apr 2026 20:33:01 GMT  
		Size: 54.3 MB (54261216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88e93f626800c3e743b24f70c0f766f3debe0ba6f4fe4007f364e298391e35b`  
		Last Modified: Wed, 15 Apr 2026 20:32:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f626c4297327dd6abfea8f0acb8ea0be823687a7a4e4f87e1cceb14b277b937e`  
		Last Modified: Wed, 15 Apr 2026 20:32:59 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4a6deff3c584233b84cb7665289437e09ad169f8ec8568b3d3f37c33dc025f`  
		Last Modified: Wed, 15 Apr 2026 22:13:26 GMT  
		Size: 50.9 MB (50899652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e236f60d6b5833ec8465f4cee5830710e0410f2e538b72f000ef057cbcc5c9`  
		Last Modified: Wed, 15 Apr 2026 22:13:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:9c76e1fe51f8c76ab3854e497245f1d58a7bc802cb79e0508998358834e28656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112d0226a3f80025916d90df4d6ef5a94b85abab75ea6d851bf71e5955b6660f`

```dockerfile
```

-	Layers:
	-	`sha256:89d05aae8b4cd2f8467ba22323e6628d46f40304c52c854e85565be607259638`  
		Last Modified: Wed, 15 Apr 2026 22:13:25 GMT  
		Size: 6.4 MB (6430929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2afb55492b528acc569d02318915beb9148fe49543eac344f2171b3f86ded69`  
		Last Modified: Wed, 15 Apr 2026 22:13:24 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:71ffabd88fe50f4c389c9df45cff71d0ab541be9b97b6f4623439e284601a9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159794494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed29ca7a72ed81db5995fca95f30774617c0d22f4ee7684cc42fea823b42ae28`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:20:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:20:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:21:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:21:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:21:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:21:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:39:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 01 Apr 2026 21:39:46 GMT
WORKDIR /tmp
# Wed, 01 Apr 2026 21:40:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 01 Apr 2026 21:40:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 01 Apr 2026 21:40:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e568bb13a59c072b3af8c406e7b451459d28a2bdf653f96393ea9610f7d09959`  
		Last Modified: Wed, 01 Apr 2026 20:21:27 GMT  
		Size: 17.6 MB (17622524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a466cb91d60c12ef2f2ef31a16b61be170026654e23713e63af5dc792239c6f`  
		Last Modified: Wed, 01 Apr 2026 20:21:31 GMT  
		Size: 52.7 MB (52652143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269cef637945ee94a49dcd4126081f85b8c87b30a479e74ae4f41cac1e7d6d2f`  
		Last Modified: Wed, 01 Apr 2026 20:21:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9579f76cd02fb4009f1f98ff5d2fb5a780091ba9a44d68603a54b118fc52524a`  
		Last Modified: Wed, 01 Apr 2026 20:21:29 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb5087645a16310e3244f33507c17165cd5d7582709b606976b1b92bc393b5`  
		Last Modified: Wed, 01 Apr 2026 21:41:17 GMT  
		Size: 54.9 MB (54867088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e111ba9b964de62b1670b559cee8e4b07b9cb9156330814f6feed15c5d524f`  
		Last Modified: Wed, 01 Apr 2026 21:41:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:20897d5ab10ebe2c75211f55a1a4b525c9378a4577fb4002b13857f14e23f3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd26d8847952b0f06fb0d1c75e62c615276e840a2bcf48842cb227756aa517f`

```dockerfile
```

-	Layers:
	-	`sha256:be1975f0d86d1d93c9a00b700ec193df92c073fbd79585f99f703c6b0fd5acab`  
		Last Modified: Wed, 01 Apr 2026 21:41:15 GMT  
		Size: 6.4 MB (6430281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594822a293d1e334594051687136c655dd2de82b7505e58e51de45fd8cc9faa9`  
		Last Modified: Wed, 01 Apr 2026 21:41:15 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json
