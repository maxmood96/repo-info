## `clojure:temurin-21-tools-deps-1.12.4.1618-noble`

```console
$ docker pull clojure@sha256:119bee1cef7bd5206a6bac901a0a0783b5341c54532ed254aade08d827e6455d
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

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - linux; amd64

```console
$ docker pull clojure@sha256:cba8bd478d485048e939d6781b778a6397c3f91a7125df97b183a44546b8ffbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 MB (265729220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af343097d05068ff3ff77fbadfaa8dde9c0fa47a8552c68891d4d7b0d316e0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:17 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:05:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:35 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 15 Apr 2026 22:05:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c74f5c2809456d4ea1d8df7e9a8c6ce210cd1a451308fd3ee42cd5613fac2f`  
		Last Modified: Wed, 15 Apr 2026 20:34:34 GMT  
		Size: 23.0 MB (22965503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9a1e97487bbf567fd39c1a971160f21dc69bfea8eeb8bfc923b39fe9c05f8d`  
		Last Modified: Wed, 15 Apr 2026 20:34:37 GMT  
		Size: 157.9 MB (157867624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef33ef1b9930d5fb66257dbd8fbe7e1ccb258d35b87243481902922fdcfae86`  
		Last Modified: Wed, 15 Apr 2026 20:34:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d29f6a4c60335d154318f22c76be42011017740ad6c05fdb6d56ee283f3030`  
		Last Modified: Wed, 15 Apr 2026 20:34:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6260a57105afcdd70ac5f72613018d69c42a5d94fc217a601c81d54acefa20`  
		Last Modified: Wed, 15 Apr 2026 22:06:03 GMT  
		Size: 55.2 MB (55159632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba31d5f9c97ade2b7e18c109312fc3db387e9d13057878dd5803ce852c27557`  
		Last Modified: Wed, 15 Apr 2026 22:06:02 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f810dc681e622f7529c796f3c3132e057d3de2a7fbc7c2a4e2986853e3b6f259`  
		Last Modified: Wed, 15 Apr 2026 22:06:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:f5bf1ce7dd4d2aabf3332daf8817e953c526a122cc792cdf226b5adcddca92d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5924451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a50bd1cc59b12b62175b9610e38b4c3e639403525186f9aeb9d1c5e1f7db2c`

```dockerfile
```

-	Layers:
	-	`sha256:7672301801187d53a62206e72016106d695411691c208f43a10327061bc55206`  
		Last Modified: Wed, 15 Apr 2026 22:06:02 GMT  
		Size: 5.9 MB (5908907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc320c72efb8be3471b524d1fc86db9aee08cc28646e923acead236782ea5a6`  
		Last Modified: Wed, 15 Apr 2026 22:06:02 GMT  
		Size: 15.5 KB (15544 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:234001ac013ff12f33f5af5127f0e5ea0ec5819abcaf322c83d1a7059b34a958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264293904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1c0317d4439d8a497d8e4c58a5863e762dd9c443fa048930101aa1af2a62e0`
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
# Tue, 07 Apr 2026 01:55:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:55:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:55:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:55:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:55:31 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 07 Apr 2026 01:55:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:55:39 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 03:27:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:27:00 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 03:27:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c7d1b1c79c5ecc5fccf686d3358ce1ce67645041767f3b414cf69acfa63f91`  
		Last Modified: Tue, 07 Apr 2026 01:55:59 GMT  
		Size: 24.2 MB (24171161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ff0baa3d4d98b333e10ac5a29849712241a6e7241a71aac16f5e3cbf06d88a`  
		Last Modified: Tue, 07 Apr 2026 01:56:01 GMT  
		Size: 156.1 MB (156139409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270f33f32bad8041e2f3bccef67345ec2c76c01a1d45b76d51a19cb2d52d14b6`  
		Last Modified: Tue, 07 Apr 2026 01:55:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ceb247738b23fbed80439fa7e1cf66042b6767e2c0e0f2057a251f8e1c404`  
		Last Modified: Tue, 07 Apr 2026 01:55:57 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c7dbcef3fe09a82ce998f8393b5507514ef881b4813d45f93b615271e836a4`  
		Last Modified: Tue, 07 Apr 2026 03:27:35 GMT  
		Size: 55.1 MB (55105775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be288d84c26428c02516b39c287aac934c90356965afd2df4e3d84fbcc91875`  
		Last Modified: Tue, 07 Apr 2026 03:27:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aca7655fa503d7b9d5e05282049ac576bb4042b2d876587f65d2a889a5605cf`  
		Last Modified: Tue, 07 Apr 2026 03:27:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:5fc9bee73a12b47fa5938afe2c7acdafd92d8be0bf1382d9644ff52c1daf7c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6062157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9277adaf513032a92033b4761a3ce23983050c71745d006b9b66dd6f8ce66041`

```dockerfile
```

-	Layers:
	-	`sha256:6e5e762ca183d254c72697a06d372fdc27db15dc3fcc9977a4a367c5e3738e6b`  
		Last Modified: Tue, 07 Apr 2026 03:27:33 GMT  
		Size: 6.0 MB (6046521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef46eb9d8d7e080d84f946167d3bd049ec391ac042597e324c2e4ae43ee4ac63`  
		Last Modified: Tue, 07 Apr 2026 03:27:33 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:2a3d0b1666fc649201ce53b11df6c9dafb5312a9d6163444d9c41af6be31c386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276181685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4ef1555300368eb2b6418069b72fe51beebad7853f5040197c3d74f86662d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 04:30:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 04:30:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:30:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 04:30:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:30:08 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 07 Apr 2026 04:31:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 04:31:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 04:31:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:31:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:31:19 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 14:46:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:46:52 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:52:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 14:52:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:52:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:52:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:52:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb69da8bc15c0a11682f0906f2e84b672591fc9ed3e7de40c3263c178cfd38`  
		Last Modified: Tue, 07 Apr 2026 04:31:03 GMT  
		Size: 24.1 MB (24093111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b0a56fc89f03cf04215cf409bf7ba43ba2ce776019b53500503648990a4b4a`  
		Last Modified: Tue, 07 Apr 2026 04:32:08 GMT  
		Size: 158.0 MB (157985050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781baa7571ce5dae318ad0d203ce43d930ec82fc34319f774fb1140409b90352`  
		Last Modified: Tue, 07 Apr 2026 04:32:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3bf01b3d8c84467d940f554268e29aac2dc23f1535cd4ed7101e47fefe16f1`  
		Last Modified: Tue, 07 Apr 2026 04:32:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6ba0098ba0ba1d21bfa7974ec712175c08efc1bb22dd1edc96f75aaf8d0b7`  
		Last Modified: Tue, 07 Apr 2026 14:52:44 GMT  
		Size: 59.8 MB (59786701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739a2bfdeef489893eb0f51902a7f36723a8d2ca9977acca32b4728bb1edaf00`  
		Last Modified: Tue, 07 Apr 2026 14:52:42 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60f6345d35cbb4f1e6cae6cec0697ef5cfb28589cb3d6bd58728e4e685b0ca1`  
		Last Modified: Tue, 07 Apr 2026 14:52:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:22907778464d5f0940b25a869438e38ac7b03401363d919031b4c61fa985ec17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a694fd0426da4211054ac73c221b89710e749be26507586b6057fac8e121b84`

```dockerfile
```

-	Layers:
	-	`sha256:cb703e06e15e9251ccb22f41d752645f663a998f5bfa6da683bd2c071637c097`  
		Last Modified: Tue, 07 Apr 2026 14:52:42 GMT  
		Size: 6.0 MB (5959763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7741a2bd03f1059de0d6dc6001e5a2929dffecf716dd9e27e8a5d251a510ef6`  
		Last Modified: Tue, 07 Apr 2026 14:52:42 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - linux; riscv64

```console
$ docker pull clojure@sha256:4a982a8e0c0a82c544dc683f097103cf25d59108c7b8c5c10ee2f15769982c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273957659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2272f33b977a71c185acd3e547f64962ef3b970a87d59f973f3a826e0dcbb42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:35:32 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:35:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:35:33 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:36:09 GMT
ADD file:59e78909d1b1cd9a524f68d8ff44bb077ea09f4f39da5e046d635b48da9d33bf in / 
# Fri, 03 Apr 2026 15:36:13 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 02:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 02:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 02:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 09 Apr 2026 02:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 02:11:04 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 09 Apr 2026 02:22:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 09 Apr 2026 02:22:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 09 Apr 2026 02:22:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 09 Apr 2026 02:22:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 09 Apr 2026 02:22:54 GMT
CMD ["jshell"]
# Sat, 11 Apr 2026 21:49:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 11 Apr 2026 21:49:23 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 22:09:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sat, 11 Apr 2026 22:09:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 11 Apr 2026 22:09:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 22:09:45 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 22:09:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23ef52cbd4674ce4f8269086177a6a1fc3abbc052567212551b8169743067808`  
		Last Modified: Fri, 03 Apr 2026 15:56:59 GMT  
		Size: 31.0 MB (30963791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd6942c5ca1b5297223819bdcd4483eaaa83528d81c0895b5729ce9bff4d8f0`  
		Last Modified: Thu, 09 Apr 2026 02:16:00 GMT  
		Size: 22.3 MB (22267147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d919a5f892a603e56373e5e7b50a66dc7b8d0571fa0056503599ab6f972b2a79`  
		Last Modified: Thu, 09 Apr 2026 02:27:10 GMT  
		Size: 157.2 MB (157223302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93123224c835a3e9b8ce012c5dd4fbd2556fe165cfe9b0a4dbd2713173b47a13`  
		Last Modified: Thu, 09 Apr 2026 02:26:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93e3171917399825f6d7f5103012c1ef1755a54828c7f7e9f40655fa11e091c`  
		Last Modified: Thu, 09 Apr 2026 02:26:48 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbc1edc24937dd382a8af71d6e950390c1b04d0589377ee93769eca449ab448`  
		Last Modified: Sat, 11 Apr 2026 22:13:45 GMT  
		Size: 63.5 MB (63499925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7cae66841228eff6ac3f4f0de7a148cc0ff11192a5c72cc9ac3ad13c1b344a`  
		Last Modified: Sat, 11 Apr 2026 22:13:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8df839cf3840fcf1b8068143bbc3e0ed42f1ff2186dad50c57d95ad9a908c0`  
		Last Modified: Sat, 11 Apr 2026 22:13:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:088c2bc5c83ec43273ad5c7437cf877e6d2d98df81605e532f568e2d37cd5ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6028198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be72a9240cd5ae0d4904dd609ed82cdaf1b4182c2400cb73b2801ebcec65207`

```dockerfile
```

-	Layers:
	-	`sha256:cc4c21808818afa13ce8c3d2f735b9726c938773dd15bfc5bdb6d07a3ee4be5f`  
		Last Modified: Sat, 11 Apr 2026 22:13:36 GMT  
		Size: 6.0 MB (6012616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0baca9a68ab9f22b325e501623136f414318b35edb76cd129974c47bd5459d47`  
		Last Modified: Sat, 11 Apr 2026 22:13:35 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - linux; s390x

```console
$ docker pull clojure@sha256:621733808445b46d3496190ac87923a50380b2a445c7dd61d6b025e3d3902b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255677613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6600d3dc6766a6c625ea17cfc1fd61156aeb600f64efd25057f2fd1c99ff59`
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
# Tue, 07 Apr 2026 03:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:10:09 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 07 Apr 2026 03:10:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='a57fd486c3c24ed615eb91ef9421ddd38c720e7398df5a161872fb26ad825936';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 03:10:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 03:10:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:10:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:10:16 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:46:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:46:00 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:46:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 05:46:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:46:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:46:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:46:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656a21cdfc92d44b39acf5e5ee1960a1e161e67a37e56cecfcacc1740875daaa`  
		Last Modified: Tue, 07 Apr 2026 03:10:40 GMT  
		Size: 22.1 MB (22127178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149df18c215144bdee84a21e074f4a0f66c26197c8a23478dc02abd2caf490e5`  
		Last Modified: Tue, 07 Apr 2026 03:10:42 GMT  
		Size: 147.1 MB (147113653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fac767a506f2b7fca9762ed23cc63490dd6949f85f5979f2b06c51df29c5786`  
		Last Modified: Tue, 07 Apr 2026 03:10:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923ea226883ad9f14c5eb5ddb5c9e9413c55682e16044d1a6d215a0fec8da304`  
		Last Modified: Tue, 07 Apr 2026 03:10:40 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5461ffc19eb7e99a5694e11bc3ed9bb54f883746d4105821f44490e0eb860829`  
		Last Modified: Tue, 07 Apr 2026 05:46:36 GMT  
		Size: 56.5 MB (56521456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c14e6f86f06b6fc17511751c88fe25a16fb24e09da6ffa5b95869cabf68402`  
		Last Modified: Tue, 07 Apr 2026 05:46:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fe023ae225b636e4644b7b5f193a415f6f037f47145dd088ba9a580729be1f`  
		Last Modified: Tue, 07 Apr 2026 05:46:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:0487cee67d2a8a5a72182ffc16978ebc3cc5d9a0e3f3bb43fde29bd8f2fc74ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39833610840cbcd6866eb3c2beb8329461687135587a76292999dad66688fd08`

```dockerfile
```

-	Layers:
	-	`sha256:4accf5114dfabb79c8359890405542de94a01a47c446a701db605cc104e89faa`  
		Last Modified: Tue, 07 Apr 2026 05:46:35 GMT  
		Size: 5.9 MB (5854254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:545a168e032330ef2c05db5679b603b6bde72f6a3f56b0cadf752517d9e4175d`  
		Last Modified: Tue, 07 Apr 2026 05:46:35 GMT  
		Size: 15.5 KB (15544 bytes)  
		MIME: application/vnd.in-toto+json
