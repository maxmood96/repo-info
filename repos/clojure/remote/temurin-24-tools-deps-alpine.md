## `clojure:temurin-24-tools-deps-alpine`

```console
$ docker pull clojure@sha256:804b7fbf4f34ab46f0bdef46bcc8e4e3e9157567a78e172319994785f9d5659e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:8f36f6139e40049c270f8ba323abb632e6c21c3c2da353873fdd36d9871e1c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140130920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f09fb61e562f00b18e00f7f40169c42995087580fa404c9d771e17dcff48bcb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5ef2386be4a27ea92a01ef0263a3104d9355ac7f4fb22aa55e2a91eeee344e`  
		Last Modified: Mon, 04 Aug 2025 20:12:09 GMT  
		Size: 21.1 MB (21104348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eae701b9ed8b56a4df38c4ec9b72d1f048c6055ba56cff62e61db3768256810`  
		Last Modified: Mon, 04 Aug 2025 20:12:16 GMT  
		Size: 90.1 MB (90132918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939aba76ded566210b691bda00b92ffc2029071fc4984207e3c7d6dce00328d6`  
		Last Modified: Mon, 04 Aug 2025 19:25:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907d1c29ddd75894bbcf074eab7ed68afbe4634ea810f2cf54368a7eec0eb6bc`  
		Last Modified: Mon, 04 Aug 2025 19:25:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c3adca4fcd45ec56e49e477d5f6a7502970ac196af844c5bdf4f6532982751`  
		Last Modified: Tue, 26 Aug 2025 17:28:04 GMT  
		Size: 25.1 MB (25090504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee2f7ec87f2008f49194798d89a2f7d22e237daa700f1e325cfea0488d890c`  
		Last Modified: Tue, 26 Aug 2025 17:27:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fa10fc85c41979b4a9066cf2c47e84175e2cea3ba6d09f4735572f95856949`  
		Last Modified: Tue, 26 Aug 2025 17:27:51 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:3b266e0edd9403db0af349eddb83bdd2e9a8a59a669b90163843634e926d788b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1261360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceabbacd1a9d756354cafd9e894c1f15ea82001c811312a004ad7acc41407105`

```dockerfile
```

-	Layers:
	-	`sha256:5e7e9897ce9b9a7a4cedb2527d8b79f61f03173fefce04bb75a4161837b08e4e`  
		Last Modified: Tue, 26 Aug 2025 18:41:43 GMT  
		Size: 1.2 MB (1245891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee334a774cb41f2e985e605e1f1572b14518836e05b95d9f198a7f68ab84fe70`  
		Last Modified: Tue, 26 Aug 2025 18:41:43 GMT  
		Size: 15.5 KB (15469 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04c42bdd6757548085f334b838b240411862d82943258005ee3d641a45c2178c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139611316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f613af91dbea8ddb8f2b98160b9b8da2a18fdc351be1ef086f6cdeeeee65a6d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a495748323e0cdac275f94a75856b53137d10e7dd79d59568fe601407fb00e`  
		Last Modified: Mon, 04 Aug 2025 19:31:51 GMT  
		Size: 21.1 MB (21148725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f503b83c17e606e525a15bdf8c088d8b510866bd192730491923c7e09021b161`  
		Last Modified: Mon, 04 Aug 2025 19:39:38 GMT  
		Size: 89.1 MB (89116820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e121434e3e7ced93721c74730970c4545f0d07a1ab8a3cb707d8d97621657a`  
		Last Modified: Mon, 04 Aug 2025 19:39:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94585305800850d7db8da0cf8b919141fa5eb89e43d0bf4133469159f0960634`  
		Last Modified: Mon, 04 Aug 2025 19:39:33 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae543504bb02d981164fe9368ca1928f6b2b069dae18d22bbce57f9246b39b0`  
		Last Modified: Tue, 26 Aug 2025 17:53:53 GMT  
		Size: 25.2 MB (25211562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2778c7b44f69bd0b11839471e8e7486c9716c8fccf6678176ac27cd1cfa4d900`  
		Last Modified: Tue, 26 Aug 2025 17:53:48 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3df59705415349d14a313f394b1b7f8e3437b980f2f5b133fdd492445e16ad8`  
		Last Modified: Tue, 26 Aug 2025 17:53:48 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:eb284487ba7c99dca0da1ee289d3424af061893ee6a4fd92964eb8ab73738f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1411451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be674057fde856c20dc0eba664ed06f7f413737b05d77dab21a19d6a13ae0314`

```dockerfile
```

-	Layers:
	-	`sha256:2850f36563a2b2c0abbd7588ec01b4f1162b88ba601af9d3906949958b1b59f1`  
		Last Modified: Tue, 26 Aug 2025 18:41:48 GMT  
		Size: 1.4 MB (1395890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff7b14931b86786ce444bce1c522f33856dab19f8ea8e0f2a26d2c7a3cac336`  
		Last Modified: Tue, 26 Aug 2025 18:41:49 GMT  
		Size: 15.6 KB (15561 bytes)  
		MIME: application/vnd.in-toto+json
