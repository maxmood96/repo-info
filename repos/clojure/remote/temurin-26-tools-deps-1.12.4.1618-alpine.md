## `clojure:temurin-26-tools-deps-1.12.4.1618-alpine`

```console
$ docker pull clojure@sha256:bbe525104c714fe4b2c43f00587e9e025084f171874e7590a65c5b38c00272e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-1.12.4.1618-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:c8711250dce2108517aff63ff16a9dd15af58163d68affc14d3f88af86cc9f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138296287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1aa8370b3248a43e0e469abf5662c4dc9bb55765811914ff27b95beeaef51f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:31 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:35:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='049027647a2d1cf3b1e3c1e7dad746aa6436928932bbed9130b87a25f585908a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='c105e581fdccb4e7120d889235d1ad8d5b2bed0af4972bc881e0a8ba687c94a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:35:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:35:21 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:07:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:07:41 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:44 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 15 Apr 2026 22:07:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:07:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bff7045b4dedcda28d3e173f14d1ba10aa99e2d37aca0e2fc2121c2c26408`  
		Last Modified: Wed, 15 Apr 2026 20:35:38 GMT  
		Size: 14.3 MB (14307228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391edefba2e6ae3493026f4fb7364e2b3cfdb3d6f20c95c057a840c7e2a70de4`  
		Last Modified: Wed, 15 Apr 2026 20:35:37 GMT  
		Size: 93.7 MB (93716220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195635ff26dc4127f92b360891f7063894021e91e54110ef34da2c8959f43c67`  
		Last Modified: Wed, 15 Apr 2026 20:35:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3caeef0ce8088f690976509ec2e96ce94d7badc8e863f438892920077dceff`  
		Last Modified: Wed, 15 Apr 2026 20:35:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cb898a64f3cf7104c26d4d496fecb69dd4bb2c15eec8069d59336fc3776e91`  
		Last Modified: Wed, 15 Apr 2026 22:07:54 GMT  
		Size: 26.4 MB (26405194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bc2c8bcf7501eaf8114b4db8a61bbd4122e7519897fa08bada1235e2bdefea`  
		Last Modified: Wed, 15 Apr 2026 22:07:53 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3175bea005216ddd0591a96a628ae6604f7cb2200e5697941cffc2ae6bf7e26b`  
		Last Modified: Wed, 15 Apr 2026 22:07:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:6dc34946debe633ada8426386557c7654421caea54e90f19b9c85a146b53d7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1221650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068d0f029a3d10571c9891b47f19e4a217b03aa7fe2e7073e9d213c21ef73fdd`

```dockerfile
```

-	Layers:
	-	`sha256:2afd6b58dacfe73a3bd5801a6ef35155e8d79f0f2eea373a9095a939a32698d4`  
		Last Modified: Wed, 15 Apr 2026 22:07:53 GMT  
		Size: 1.2 MB (1206228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03356bdd675d5cb35d7f67463972cdbcfbe46da48d82cc1c7d3b8cd05f3d178d`  
		Last Modified: Wed, 15 Apr 2026 22:07:53 GMT  
		Size: 15.4 KB (15422 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d085f711e5b6d9bc84bb773b802cc1b7ca32df4aaeb01d9959d2334857a166cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137745137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a81bc12bc970920b7a1cb6ce8ef8a99c275034ae800039a60630376fe6b312`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:49 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:49 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:34:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='049027647a2d1cf3b1e3c1e7dad746aa6436928932bbed9130b87a25f585908a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='c105e581fdccb4e7120d889235d1ad8d5b2bed0af4972bc881e0a8ba687c94a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:35:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:35:00 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:18:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:18:52 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:19:20 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 15 Apr 2026 22:19:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:19:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:19:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:19:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b8c9f714bd537100e4118563ae7a953d248cf9031f3f9563aec762a9abce04`  
		Last Modified: Wed, 15 Apr 2026 20:35:16 GMT  
		Size: 14.4 MB (14365600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d118d41a2fa844b8c088c1ff89c9b0c2813f936d1f5be8258ff9b6f16390758`  
		Last Modified: Wed, 15 Apr 2026 20:35:18 GMT  
		Size: 92.6 MB (92608698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd56b354af4d3369e57e9e8e23b3c98b944e529ac302b27349c701e656b15fc9`  
		Last Modified: Wed, 15 Apr 2026 20:35:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc27638916d2e266082323745d2dd8fa8a569aef22680acc5e3998a045c25a`  
		Last Modified: Wed, 15 Apr 2026 20:35:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1beaaff1802f52086330853400e370312bc41ab35325299c75f95c700130d6`  
		Last Modified: Wed, 15 Apr 2026 22:19:29 GMT  
		Size: 26.6 MB (26567512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aa439470389376ca86165b90a02e4028c17ef9afc62aec0f06a88dbad67f23`  
		Last Modified: Wed, 15 Apr 2026 22:19:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de6b90acb79ae9ee29752855f90fcfc3416c89ae064c0576fa4d052a92fd809`  
		Last Modified: Wed, 15 Apr 2026 22:19:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:c380d9c641c8fb622c8f27e795d8b90c94a7d488fa53ec278709fffc38839467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1371091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65502302c719cd19feef7cd017168318ea1ffdbf6bf1d596dad0acb63a1bbcb4`

```dockerfile
```

-	Layers:
	-	`sha256:38187fc462a696d29061645742d9e016ac4dfd95e3b2a4e98ce972f0f07a17c0`  
		Last Modified: Wed, 15 Apr 2026 22:19:28 GMT  
		Size: 1.4 MB (1355577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83afddb454fa886c60b6735c53e0c2f8255f4d0ae6e436b5e873047c852aa8c7`  
		Last Modified: Wed, 15 Apr 2026 22:19:29 GMT  
		Size: 15.5 KB (15514 bytes)  
		MIME: application/vnd.in-toto+json
