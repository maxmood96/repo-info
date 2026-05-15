## `clojure:temurin-26-alpine`

```console
$ docker pull clojure@sha256:c46ace903ce13720bb21d15b48d55d87458173d731ada82eb57d89e319cf007c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:2c78de217a2850950da6a9263ca88c069a9f3b892938372488c781fe0d3a79f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138326235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938dd8be2d070d3831d068c6e397c7554850c152f38a71c9a7c986a4cbfb99a5`
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
# Thu, 14 May 2026 23:36:36 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:36 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:39 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 14 May 2026 23:36:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:39 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:39 GMT
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
	-	`sha256:d113be40d93a28630de93829b80897849f5701bc0abff66bd4bb485cb51d3acf`  
		Last Modified: Thu, 14 May 2026 23:36:49 GMT  
		Size: 26.4 MB (26435139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d550bdf79c7205bfb01854babc9de1791658d1c233b274ed2673c4f8652ef0f6`  
		Last Modified: Thu, 14 May 2026 23:36:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b36ead3e796364d88d5e02fcfc2b5cf9cf3bc303ed121c6f18a515320a1cbdd`  
		Last Modified: Thu, 14 May 2026 23:36:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:621797eba11c306818e686e6a3dc2a6886e96243cbd2c5ca1369bf8d010e92d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1221648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11acbaee31a7032d36acbe69652640d0cab53b9fdb0c70afa36313463c68a04f`

```dockerfile
```

-	Layers:
	-	`sha256:c11b340075758d4b9693c7f99b34548275a39a87312c53d44ccc8b3cfe060eb3`  
		Last Modified: Thu, 14 May 2026 23:36:48 GMT  
		Size: 1.2 MB (1206226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8242fa7ca66d0378fb5a7823dfc674ebce7a153c1461e1aaec1332d3c81f6299`  
		Last Modified: Thu, 14 May 2026 23:36:48 GMT  
		Size: 15.4 KB (15422 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0f405f5e661b511276ffd68baa86a9b285c9dada5908b335f3eb358ceef39f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137774517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bc0e176452eeb2571d8c9f945543a222591f374b9f624295bea4ff02a7939b`
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
# Thu, 14 May 2026 23:36:38 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:38 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:42 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 14 May 2026 23:36:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:42 GMT
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
	-	`sha256:ed9018fa794f235e4ddbb83ea487f0a4623ff7e531b582a239069c4c399ce2e3`  
		Last Modified: Thu, 14 May 2026 23:36:51 GMT  
		Size: 26.6 MB (26596883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c5c8e0342b516ed512a5ed262e8cc668d2901e27c1f6052771868907ef3dab`  
		Last Modified: Thu, 14 May 2026 23:36:50 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01284d5de2e3024709b4e611e0007f40f6c1032ac845f3d721516b7901fd5b37`  
		Last Modified: Thu, 14 May 2026 23:36:51 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:e5637da25234f6231bf69c57e488cf701f8194ef7d1d7cad738b94b5432d0fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1371089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9868e7b32f7dd6698b5c6a8e54146c4656068910ec4fbafe435b395caeaa88`

```dockerfile
```

-	Layers:
	-	`sha256:d2a1ec198e5e12509d6bcac972ee95162000222d0da5da1c2442159c5bffb526`  
		Last Modified: Thu, 14 May 2026 23:36:51 GMT  
		Size: 1.4 MB (1355575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d39f59154eeba77e78f23bed41141159bc3c172e57a1cd6a67b46a7d2112a4d`  
		Last Modified: Thu, 14 May 2026 23:36:50 GMT  
		Size: 15.5 KB (15514 bytes)  
		MIME: application/vnd.in-toto+json
