## `clojure:temurin-11-tools-deps-jammy`

```console
$ docker pull clojure@sha256:908c7bcae119947fd7a0c2f6339d23074fe268fefaae62734e5fc59c6ceb974b
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
$ docker pull clojure@sha256:1358bc49121a05db616d8426877c2168cb67975186fc080f441e44431d863d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242632526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576b098f773d91c592f4112790c719568496b17b8dbe299e5593fcf50d876b21`
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
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:33:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:20 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:02:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:02:52 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 15 Apr 2026 22:03:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9e4b9c046d36a50de4010f387b9dd9d78efd89cbaee7cdc00caec0228f10b0`  
		Last Modified: Wed, 15 Apr 2026 20:33:39 GMT  
		Size: 145.8 MB (145819383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b52b8edbca62a689304401b2ed73eeb1b7490cd870bb64711b7e8e81a7598c3`  
		Last Modified: Wed, 15 Apr 2026 20:33:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21fe64a09a45b54d9a097439865ccefeb3330c77dfac688f15bd22214bd6ecc`  
		Last Modified: Wed, 15 Apr 2026 20:33:35 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5581968ede19acfb55b3fef0be3da269d20e49f0218992b2e7cbb621d0fa9b`  
		Last Modified: Wed, 15 Apr 2026 22:03:24 GMT  
		Size: 50.9 MB (50922699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3eb030a2aa388f06bf169d25450a26f48ed67c0fd7713b894492799f945cb`  
		Last Modified: Wed, 15 Apr 2026 22:03:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:6a6110ef4778e8bb9efd58b19d977a34ebb312908aab96a32f0ba6f0205612ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b504127f41b5aa5f8dfdca197fae92acbb7364558836b0894023e9bb9e7350f0`

```dockerfile
```

-	Layers:
	-	`sha256:bdd48ecbfb2579641fbf712babdc145bd2b93c821b378a83adada9f118222ba6`  
		Last Modified: Wed, 15 Apr 2026 22:03:22 GMT  
		Size: 6.3 MB (6323617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eee7e674868d7e665a8c5397087a03e420b0601fdcd5b7951a1ad955d29b7c1`  
		Last Modified: Wed, 15 Apr 2026 22:03:22 GMT  
		Size: 13.5 KB (13507 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c3906e7d518cbb2930e5b504d86fd4cf0446bc534edfadc3ece85c357459c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 MB (237099967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbdc352a84ae03749b83daa1363461063d037d61c5e279e0d8e712eb778a9ff`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:33:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:15 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:14:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:14:18 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:14:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 15 Apr 2026 22:14:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:14:37 GMT
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
	-	`sha256:a8b12ebabfa0ce9e749f98a960c3297536b5a591782009946a5351d2ee39f14a`  
		Last Modified: Wed, 15 Apr 2026 20:33:35 GMT  
		Size: 142.5 MB (142514615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bfd1d7a1329265c728ccb5154e2dd1ecddfbfb0f5e76b9d51986ea6b32050c`  
		Last Modified: Wed, 15 Apr 2026 20:33:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed7de9465cc40026f718ee347f51526a7765907c54916e572420999aae304b7`  
		Last Modified: Wed, 15 Apr 2026 20:33:31 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c480edbe59ed1eb03dc9eec72076d596dd7c456e69c8aeefae8cb17be34a45`  
		Last Modified: Wed, 15 Apr 2026 22:14:54 GMT  
		Size: 50.9 MB (50900519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b6bf000f126d7fc9db9a8839d481b8a900141602f1fe0b115a63910a95584a`  
		Last Modified: Wed, 15 Apr 2026 22:14:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:b305706b1e924168132e1eb5ba6e3975aeb3a493d829b1146f5368ecb3860361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6343600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31735dd154070039a0f6e6b1a422d97eb24da8c7c1c684e9fda9e3ea0ecc5ac`

```dockerfile
```

-	Layers:
	-	`sha256:6f79a5d799645a4bb3184f6bd9e3cdfdfb9105417dc5af291c988b5cfc272559`  
		Last Modified: Wed, 15 Apr 2026 22:14:53 GMT  
		Size: 6.3 MB (6330001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1307870a816485fb63ba58acc4bcbfa3031ee22503fe71429b86d86b276b88ee`  
		Last Modified: Wed, 15 Apr 2026 22:14:52 GMT  
		Size: 13.6 KB (13599 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:79d48a58a5ef3f2851221459ab684809af83143908f877001c4d290bed6fc76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240147653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b311a861a47d240cf4cfa71b9b6d547c66671d047c7779059caf91c37c7e76af`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 01 Apr 2026 20:21:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:21:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:21:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:21:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:21:56 GMT
CMD ["jshell"]
# Wed, 01 Apr 2026 21:40:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 01 Apr 2026 21:40:40 GMT
WORKDIR /tmp
# Wed, 01 Apr 2026 21:42:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 01 Apr 2026 21:42:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 01 Apr 2026 21:42:13 GMT
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
	-	`sha256:99494b52cd5050a3cd5fc880ddaa6aeaa606f6a3534dbf988980dff9469cc12e`  
		Last Modified: Wed, 01 Apr 2026 20:22:33 GMT  
		Size: 133.0 MB (133005478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eea0535e8dcd1ee79fc36dfe9f79691c79ead285390852fa9c365615e1fbcb0`  
		Last Modified: Wed, 01 Apr 2026 20:22:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16d5ad51c54b0d101a47ef8913a0040560602537b4ee1e39a65d21c4c124f81`  
		Last Modified: Wed, 01 Apr 2026 20:22:29 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980c58247cd2cd164828eb71060ad136550f5c5840a2c30e65c0a81b6f09efd3`  
		Last Modified: Wed, 01 Apr 2026 21:42:43 GMT  
		Size: 54.9 MB (54866904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfbb996b8e99a1d0af7aeb45a692b1f6fc43b68806946aab8a1a142dc69fda6`  
		Last Modified: Wed, 01 Apr 2026 21:42:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:15cb6b3c1356cf8531951dee0aaa7f573dd7681cb9ac00e567cf0066ddd54d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6341770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de4cc23840c765f9fdc7b5639838586e7a6b2d583fc0c0175a0ac0aaf381fd`

```dockerfile
```

-	Layers:
	-	`sha256:3fbaa5959772155e09c35ea0cb1316233033f73259985c65a91c9445e8c225f8`  
		Last Modified: Wed, 01 Apr 2026 21:42:41 GMT  
		Size: 6.3 MB (6328225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb1cb373943a796958427b68b7221f25e7fcf51ffcfac218942da082f940e41`  
		Last Modified: Wed, 01 Apr 2026 21:42:41 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-jammy` - linux; s390x

```console
$ docker pull clojure@sha256:bdec8d1ef4f8c8917aa8e6eb57d8afbc5a3d05e4983bdedcf3049bcd395193ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221834461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f57d1a0b44893a8f19dc5d6c04dfef2967fc186fb9e116d318a1a24f877d86`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:14:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:14:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:14:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:25 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 01 Apr 2026 20:14:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:43 GMT
CMD ["jshell"]
# Wed, 01 Apr 2026 22:28:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 01 Apr 2026 22:28:49 GMT
WORKDIR /tmp
# Wed, 01 Apr 2026 22:32:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 01 Apr 2026 22:32:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 01 Apr 2026 22:32:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a59ee336d717802579088b4cee85f4403cd37fb7a0310cd7a69cd001882256`  
		Last Modified: Wed, 01 Apr 2026 20:15:10 GMT  
		Size: 16.1 MB (16149562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83525277d815061f402c6691f30e0c8eb340adf1e2eb614f0f59a98a285460f`  
		Last Modified: Wed, 01 Apr 2026 20:15:13 GMT  
		Size: 126.6 MB (126565505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5967a9db81478ca08971cacb8cdc172b0361bcd8e2f306800c238bedecc5396`  
		Last Modified: Wed, 01 Apr 2026 20:15:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b2119a4f24b03f8c94f7dc79d3e92ac1aad2bf299a2cd875c13ceb37b83864`  
		Last Modified: Wed, 01 Apr 2026 20:15:08 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6105efd042276553446e7e7831b028f58db7ffff23eae5bc17ca64647803081`  
		Last Modified: Wed, 01 Apr 2026 22:34:00 GMT  
		Size: 50.9 MB (50913577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721d5551d25c5f60e662d3ac5f5daf5ba9cb16ad3a1f99caeb7d1bf004df3797`  
		Last Modified: Wed, 01 Apr 2026 22:33:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:5425ed0123f68c714859ccfacd9d720e8aa768e7b113fc4cee05972c48021bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6333050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149973249c2ee83258fcd8dc9758c181e6568ddb4d9c62a635279872a9915b5d`

```dockerfile
```

-	Layers:
	-	`sha256:60a5279b5348aaf3c0c21f353a90c6987777acb6fba9a16bb78c3ffdf7f9645f`  
		Last Modified: Wed, 01 Apr 2026 22:33:55 GMT  
		Size: 6.3 MB (6319544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:831067ba01ca306450bb1118351d89c1980b96028a3cf4e5673eec725db8b79c`  
		Last Modified: Wed, 01 Apr 2026 22:33:48 GMT  
		Size: 13.5 KB (13506 bytes)  
		MIME: application/vnd.in-toto+json
