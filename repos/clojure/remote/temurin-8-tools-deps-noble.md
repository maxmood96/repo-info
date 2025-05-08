## `clojure:temurin-8-tools-deps-noble`

```console
$ docker pull clojure@sha256:a1e0db0670a512c9d615beb879acb63c2b2394a30964bca8b40a1292953a4283
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-noble` - linux; amd64

```console
$ docker pull clojure@sha256:ab071a3d2403dfafc68c775c6c50f66354d797f4eb3d29e9d7bfd8693b6a3d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156372534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59550a2e93a6b8760ef3e6a22c74185ac42c9c9c8ee15cec47404a7dea705970`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
ARG RELEASE
# Sun, 27 Apr 2025 20:21:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 27 Apr 2025 20:21:59 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb5d2e77b3ed75952e2bded6d2509fc3b0f0958c0a5385913bf231e9b6d6e64`  
		Last Modified: Thu, 08 May 2025 17:05:01 GMT  
		Size: 17.0 MB (16967841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c2d7a8381af026cd9491e9d666414bd50c606f6b58f620736a1ecda35b133`  
		Last Modified: Thu, 08 May 2025 17:05:03 GMT  
		Size: 54.7 MB (54721274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd55451101e874abbc40476fe1ee16036d7f3e1a6411d5d4afba0018342ce52b`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb3baa036a920247f651a9ae6f80f550b94abf4fa90cea1de56f90496840bcf`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6995c8787435557f495753225541c3c0494887106e9a2021cc322d1b036e36b4`  
		Last Modified: Mon, 05 May 2025 17:06:58 GMT  
		Size: 55.0 MB (54962807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615053d958698a70eedcdc329f59d17066ef40836afeaa87cf643cda3a02d99`  
		Last Modified: Mon, 05 May 2025 17:06:58 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:166dae87410272e070831b7dbfabe51b777b929e8581bb6e1f0f58dd4e325e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5651937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcf780b66944ce9e0bb17bc1fc3f6a3432c75b633a00f13553f6a7cfac4e0b2`

```dockerfile
```

-	Layers:
	-	`sha256:bc13459aa9b3497d5374c97c69d8eb3a2ca240c70d94675f45b4f73f14cec41b`  
		Last Modified: Mon, 05 May 2025 17:06:58 GMT  
		Size: 5.6 MB (5638402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3965a0ae7055261c533c19b1ed0135a44539450758b69f884b52118c51d2973`  
		Last Modified: Mon, 05 May 2025 17:06:57 GMT  
		Size: 13.5 KB (13535 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2a33d18908cf65ccb985406dc2299b0a0c30befde566a2474399783bad2480d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154588455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98979945c20c0e40087509957a6d5c66085f4fbe1a2b41192db4132d44bed0fd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
ARG RELEASE
# Sun, 27 Apr 2025 20:21:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 27 Apr 2025 20:21:59 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44030c5633c35d5105714bc1403c988244c1f643b1d66f623b7e1beade4140a0`  
		Last Modified: Thu, 08 May 2025 17:05:03 GMT  
		Size: 17.0 MB (16987252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dff70b78d4d1f4b7dc66cc237a357770b23872a7b924568ec5672e27da03928`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 53.8 MB (53833597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf9b6410e706984f5d3a6e937f69555762bd1b66b6268b5854e25988482791`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3424dcd404288880438075ce3c6b639fa897573913857c32aeca0c35fe9ba4f1`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d93e096f5209f0ba9593bac93694f92fbb8a5eb9536c8ea83327d2840e7d0e`  
		Last Modified: Tue, 06 May 2025 00:22:20 GMT  
		Size: 54.9 MB (54917644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867ac33a39cf42081ccc9ada16822a0d2c1a2132e8fae1562285fd9dc6e55b05`  
		Last Modified: Tue, 06 May 2025 00:22:18 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:ef05ba0eb770d0f3b9b7ba5d6d77210b57eaf66fb502c5e9d420518ae9011872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5659291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bcae3291e9e67204a62b5a4858898e989dba21922d90684bcf7fd76b4d2b62`

```dockerfile
```

-	Layers:
	-	`sha256:38f05ec4af3994b390dcc5fe3edde642baa5dbcd23ba597326a3962580addf59`  
		Last Modified: Tue, 06 May 2025 00:22:18 GMT  
		Size: 5.6 MB (5645664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb92a1e1ef4886b1fac8c392cbeccf3b6a08f4996869ae4c07be1f6b95a172f`  
		Last Modified: Tue, 06 May 2025 00:22:18 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json
