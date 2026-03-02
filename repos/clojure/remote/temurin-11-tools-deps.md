## `clojure:temurin-11-tools-deps`

```console
$ docker pull clojure@sha256:296a498a1f0215aef1a4c5f058365aecbf21dd1808a92cd9c7fcdc2d31da652c
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

### `clojure:temurin-11-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:d90d71c55efe915cd819f2781bc4d5bd88c31ed5951668c1d9122502a6a80b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248230414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebd051b387c8c306b7b6ad9b01227e64c46f2de0e52ea1e7f7979fb10b95753`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
# Tue, 17 Feb 2026 20:18:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:46 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Feb 2026 20:19:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:19:16 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:46:06 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:06 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:46:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1e4d8c9fa230a6a7121fdfb08c183d1a11d03bbca06762023711851fd2ee56`  
		Last Modified: Tue, 17 Feb 2026 20:19:02 GMT  
		Size: 17.0 MB (16980570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709776857b8b715c7bddbd680a8f4fcf5c7fa4c91e48481a3b8d976a0cbaa30d`  
		Last Modified: Tue, 17 Feb 2026 20:19:33 GMT  
		Size: 145.8 MB (145818868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1500b8aad9f8a8bbb3cd32631e6454aa769fe452420bc4b53eb8a84ae872d0`  
		Last Modified: Tue, 17 Feb 2026 20:19:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff47b6a05a0a3cec0fa9c60560ecc33c42bb16a9bd97e2ba3637699b836f0876`  
		Last Modified: Tue, 17 Feb 2026 20:19:30 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efc5adffac9f0292915172e2925ceab7faba9d1017fb8d708f0fb4f06a7a587`  
		Last Modified: Mon, 02 Mar 2026 19:46:37 GMT  
		Size: 55.7 MB (55700276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f565fbfe338de259878ac3d7a95b9d5db1147a745a588a820d6fd7040585b85`  
		Last Modified: Mon, 02 Mar 2026 19:46:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:b1386b0b2d0cf37efd9c3b9657cebc9f98fe3e0adbbfd55ae8264c7d00b72565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c66918e4ad43439e7dab47cd93eb42422c37ab6ba7ede7caca211e4ee6d454`

```dockerfile
```

-	Layers:
	-	`sha256:5a7f6f1edce81a1c29ff4273297944f02a0064984b6be0a2d390f4a9a003295b`  
		Last Modified: Mon, 02 Mar 2026 19:46:36 GMT  
		Size: 5.8 MB (5775485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9e9c31c60e5dd37726418abeb41bad3b8599239f130a481ac55c0fc7079ad8`  
		Last Modified: Mon, 02 Mar 2026 19:46:35 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:56c2c62431e245ba1275ba95f254d2a12a144651078bd1c6181cff346d7f9f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244018702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04d2241af0c528892041be0a585a8f315c673dd432d88d6f295722ff3b4d8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
# Tue, 17 Feb 2026 20:18:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:48 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Feb 2026 20:18:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:18:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:18:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:18:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:18:55 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:45:54 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:54 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:46:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9a0a02907fdd6dd960abed9cafcbf879106f66849dda4f7a233bccb4434ec8`  
		Last Modified: Tue, 17 Feb 2026 20:19:14 GMT  
		Size: 17.0 MB (16994433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0936c532d81e544549abc9fec7b7096b241b85a7acb9e9c58f0cf2b3d643c`  
		Last Modified: Tue, 17 Feb 2026 20:19:16 GMT  
		Size: 142.5 MB (142514757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0835992df6fb5f2b490353ad7dbdad1747643dbfa01c42f1483170b23db75a9e`  
		Last Modified: Tue, 17 Feb 2026 20:19:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadc034fc973dc92a39e24e58c7c85f95d9006bae48364f09534ab9001b5a79f`  
		Last Modified: Tue, 17 Feb 2026 20:19:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef04efe904f5a484be8d4e58c3fc4e205d90f6039c6ccdce67936c7e4d4f2c0`  
		Last Modified: Mon, 02 Mar 2026 19:46:29 GMT  
		Size: 55.6 MB (55641303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb7fbcd40473e26a4bd38f841122979ad3023094184d172423d4aa37f11cfc4`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:73eaf4712f8cad2e1fdb0e8e24c978f6815b78d825752979da010c8569f8f1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d537ea6ff91005a1d80791922eaeaa10c31d685b194854713223de87d6e575f6`

```dockerfile
```

-	Layers:
	-	`sha256:a135059e61cad6a76d5be16bed0ebf6ae7fa9c0be37b7ff753b33bca8157795e`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 5.8 MB (5782691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:430efb7f8b318a955b00339559d92524c4d863c057a59042283505499276d0f6`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:c5b98dfbfc43b6d0a2436f9d5a32be3e27f536d9762764a77b00172ef63eb284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246592726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba9a19b713ce88af8d28f0b07ade6bbbb8ba93de1a6085441389f3186c10e6b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
# Tue, 17 Feb 2026 20:13:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:13:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:13:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:13:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:13:51 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Feb 2026 20:15:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:15:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:15:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:15:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:15:59 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:52:45 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:52:45 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:53:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:53:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:53:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7c72ff62beb3fa7ef85f29d31b133f9c93f5b3be5679ac7a733c7736000812`  
		Last Modified: Tue, 17 Feb 2026 20:14:29 GMT  
		Size: 18.8 MB (18815050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04c6547800d19a188fb623fe8de2a0a27654498abd07c86bdad9d9b4e3be10d`  
		Last Modified: Tue, 17 Feb 2026 20:16:46 GMT  
		Size: 133.0 MB (133005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c46a6d943c8058df826c12da098c7af3c9236ca047becacde9144c097713aba`  
		Last Modified: Tue, 17 Feb 2026 20:16:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e64028b16e2074c26eb1055cd858f83774643d4c0d54f71a228afa34e53555`  
		Last Modified: Tue, 17 Feb 2026 20:16:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed9c346c2fec6457a7e565b62b51a29df505c43f79f8e4e56b95593e5e3d8e`  
		Last Modified: Mon, 02 Mar 2026 19:53:59 GMT  
		Size: 60.5 MB (60462401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6e093c192a3bed7390678ea3f53b12ceecf0c3bb97e626c9ee2f6735a7898b`  
		Last Modified: Mon, 02 Mar 2026 19:53:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:80a15bd92ff1e8afb2b51f7c173e5f92d1f284c5c8782faf969a4236de14d1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf15fb9793f6c217db918c43b4d79407701a3ecdc8559cade0e3dc90aa04d7c`

```dockerfile
```

-	Layers:
	-	`sha256:8111cc4427a723ad2aebfed456c26ec2d555caca22eedc373fd74275213fb866`  
		Last Modified: Mon, 02 Mar 2026 19:53:58 GMT  
		Size: 5.8 MB (5780115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4354448e5b0d10318468cb844e2d7bf0aedf59c49535943e02c051ca009dbb16`  
		Last Modified: Mon, 02 Mar 2026 19:53:57 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:aca6abf4d34a3628cd61917a54ab90c5dbfa3e926322e17d82937baa3a9a5351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231137702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e5a24e2ca007a0c016007ae9e9c2abed84f74a71f9dba3d6afde9069294137`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
# Tue, 17 Feb 2026 20:11:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:11:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:11:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:11:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:11:25 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Feb 2026 20:11:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:11:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:11:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:11:39 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:44:58 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:44:58 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:45:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ca7dd7cf4cafbce3745cdf3295a5a245302b1e1d5370058d4d2007f1947908`  
		Last Modified: Tue, 17 Feb 2026 20:12:10 GMT  
		Size: 17.6 MB (17581365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cd1d5c713e47e9fd8a8e86ff3519ac5ce3501965093e0fd5daf1c36e72b4cb`  
		Last Modified: Tue, 17 Feb 2026 20:12:14 GMT  
		Size: 126.6 MB (126565728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4a75835ef80bef824a3fe42b96cac4b8af8016f8beaff7f359514c485a4575`  
		Last Modified: Tue, 17 Feb 2026 20:12:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e4a8913003be5194d0d17495db7d0de55c8bb161f65ea723e71460b6c4fab6`  
		Last Modified: Tue, 17 Feb 2026 20:12:11 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc44193d4b58bf309aceb309314c6d0232a78c85ee5491970025e6b77a3b3cd`  
		Last Modified: Mon, 02 Mar 2026 19:45:50 GMT  
		Size: 57.1 MB (57077737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e6139af917affde7c5060f1c7a150c0ca54455aa1cec733b227533883019ef`  
		Last Modified: Mon, 02 Mar 2026 19:45:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8272a9943e181654658a430b56f72e83eb7bd277cac48d364dc99a8b3b4e3aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5787016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9482fc4a9fefca17c513d249df1909b0bbecc3e2162f6cbcaa13b9b918ced1`

```dockerfile
```

-	Layers:
	-	`sha256:38c7b739e2d69d05eab03d01230feb28555a49b42ee92435ed1bd25ac2b7751b`  
		Last Modified: Mon, 02 Mar 2026 19:45:47 GMT  
		Size: 5.8 MB (5772825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da138f584e3430e4c53a44190bbd21c099c8670a531f75b979f03a62b592443`  
		Last Modified: Mon, 02 Mar 2026 19:45:47 GMT  
		Size: 14.2 KB (14191 bytes)  
		MIME: application/vnd.in-toto+json
