## `clojure:temurin-11-noble`

```console
$ docker pull clojure@sha256:87e210be57ac21f71d4d8ed4bef0b2a0c73e5a38baa7f581532285c32b97d400
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-noble` - linux; amd64

```console
$ docker pull clojure@sha256:cf449c49c25c2572c9ab71651dd7a18cb39e0bbb2f6452b5ddcb56c54ee3e0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249702560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f3fe4a004a31208a211d0fa0fffab263b66a44b6da98112bab69038bca610e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
CMD ["jshell"]
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3821a13f2b31421584f6d74839f18b0fb1989084be5d424eadbffb78d173abf7`  
		Last Modified: Wed, 22 Jan 2025 18:27:54 GMT  
		Size: 17.0 MB (16966728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83cad2e0a1624b2f5d9115bbd6760c79b9bd1d7076d776fdf434ff42da8e7b`  
		Last Modified: Wed, 22 Jan 2025 18:27:56 GMT  
		Size: 145.6 MB (145608992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838d869a877530e00422b76b4d652da4f151143772e7a938b693caf44198405a`  
		Last Modified: Wed, 22 Jan 2025 18:27:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f9cf0f943b65414cb0e3376ce0edc15fb285a135b6523b5f695e51ece38a6`  
		Last Modified: Wed, 22 Jan 2025 18:27:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68550e55da9521c674d7697115a05c7e31c0e2a53eb14a29b4e1f2d11c5b0e4b`  
		Last Modified: Wed, 29 Jan 2025 20:27:34 GMT  
		Size: 57.4 MB (57371785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0fd69074e1167a2424b701324cbe4f5b986e0b8fb8feb8479b5cabf719bb4d`  
		Last Modified: Wed, 29 Jan 2025 20:27:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:cfd02a764fb9fd465307bc233fbd24e728be2bd591ca4d8baa581e3f570d9f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5549458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95f2a91d6769f7caef7c4322c9e997bde17b8b2ded5153b857c654afa1238b6`

```dockerfile
```

-	Layers:
	-	`sha256:8dca2d54795d4e3a7e40a6be81e1f9f1790440626850413f4eb15205c73d3778`  
		Last Modified: Wed, 29 Jan 2025 20:27:33 GMT  
		Size: 5.5 MB (5535908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3090a038ffc3ed3c0d4df45830c3be3151d25bb3d95f15606fe2c858057a516`  
		Last Modified: Wed, 29 Jan 2025 20:27:33 GMT  
		Size: 13.6 KB (13550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bacb72fce94480caf7e76dd35275b35e77dcab4d550788e133d4ac1b3e56be9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245560897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e774cdf549459fa13fe6a8a950646c632f57f0b3115c9b6dc33551474d3eb783`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
CMD ["jshell"]
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c530cc6ab046b19072365b8fb7487e6403ab28eafc4b1af8a84c7f66621b0e33`  
		Last Modified: Wed, 22 Jan 2025 20:58:17 GMT  
		Size: 142.4 MB (142387296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071da2e36cd1c43af95f429b3fb3695cbcf1f18fbaff07102104308cb330460`  
		Last Modified: Wed, 22 Jan 2025 20:58:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fbfab1f1c0c83577e4bf53eab3ddc2a97a14bfcd47729e3749066c2f987494`  
		Last Modified: Wed, 22 Jan 2025 20:58:14 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bef9f7bf55b31f6235b6f1e70af3bce5b2911415b4c01ddfcfbcf12f7ffbfb`  
		Last Modified: Wed, 29 Jan 2025 20:47:25 GMT  
		Size: 57.3 MB (57294986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e131478bbd023bd47b4a259c3f6591d0586303e8456191b61f234c6770cc4b2b`  
		Last Modified: Wed, 29 Jan 2025 20:47:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:8a84d28b6709654e9a8ede48be9415f0530e221b88001cdd31eaa9efcca33ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cceb969413e864bedd799c2bf47b370aa28065e877b2f4146d4595422a5ee6`

```dockerfile
```

-	Layers:
	-	`sha256:aa403e05770d7f4a4b7d464dcf9623cc08964c36e3bcca05f855cbaa963aa693`  
		Last Modified: Wed, 29 Jan 2025 20:47:23 GMT  
		Size: 5.5 MB (5543090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:705962746fb0147ed31c8451695a3749c1b8d1e6c40c83e4dfeb14c4a6e24496`  
		Last Modified: Wed, 29 Jan 2025 20:47:22 GMT  
		Size: 13.6 KB (13642 bytes)  
		MIME: application/vnd.in-toto+json
