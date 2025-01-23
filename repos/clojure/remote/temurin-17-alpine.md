## `clojure:temurin-17-alpine`

```console
$ docker pull clojure@sha256:697605cf0dc9a3ec73c3ade9c25d1afd3bbd1aacd393d33c414b34dadbce2bf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:0630cdaf2a238570c96416bc4ad97d52bcd865d6caf9f50b8d76b7583f198bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193019436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5116cb10234ac7c9939db6aca196f4227990285599f2e32a61303217af7ef7e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='67632ee4563e9827b56f62ab6da95bce200d9e82092b211988c0d2113abc4071';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["jshell"]
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8ac0524037a4eda23f7295f488c7798e164d787fdcd8357dcca0b4fc2137ee`  
		Last Modified: Wed, 22 Jan 2025 18:27:48 GMT  
		Size: 20.9 MB (20908664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa1b94f6a742fb709df97843970ae7c293892e396cbd5d0e74544dd5243e194`  
		Last Modified: Wed, 22 Jan 2025 18:27:50 GMT  
		Size: 143.7 MB (143688888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec922bc2dc31ed98aa0bf71cf9059f1f676b6d2e0af56ff5a0841825cdd8d3cf`  
		Last Modified: Wed, 22 Jan 2025 18:27:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9085af3d24e4ee3869258681600497e04f0d55f37be9c305dc9970cc976e5174`  
		Last Modified: Wed, 22 Jan 2025 18:27:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b87496bdfc1a33174de112cf8f328a7422cc5d911784f5a47490ea99fe172b`  
		Last Modified: Wed, 22 Jan 2025 19:42:06 GMT  
		Size: 24.8 MB (24776703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8580df57dc8bb3231b6bfa2baf62830ea1fa2ac070b0ccb13d1a125876e50408`  
		Last Modified: Wed, 22 Jan 2025 19:42:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3705738c2e72bcdaec5063b4913be483ec7fd6e73d39ce149a1e5efd22e43f31`  
		Last Modified: Wed, 22 Jan 2025 19:42:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f93f7c5b9d2fa82fb44dc7f3c050b5e12d941a166313244f447ce6feb315b95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1264967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c345358b583dcbf423bcac390e7d1f4537f79ac4a570e3e8f0a40da85017ae2`

```dockerfile
```

-	Layers:
	-	`sha256:02d58eaf6ddaa05ac0a91f206d6afe7a58659f40d9b41cd704e8d53f22da7458`  
		Last Modified: Wed, 22 Jan 2025 19:42:05 GMT  
		Size: 1.2 MB (1249507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818bc9645e704089fb37eeff6f5ce058edc364383f5568115d6d8e294b4ec6cc`  
		Last Modified: Wed, 22 Jan 2025 19:42:05 GMT  
		Size: 15.5 KB (15460 bytes)  
		MIME: application/vnd.in-toto+json
