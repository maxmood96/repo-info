## `clojure:temurin-23-alpine`

```console
$ docker pull clojure@sha256:e5bdd3922e62a3275ff78bc2f2a6d9ec66413afcd7042f8da3d8312ee10bd44d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-23-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:d014e6f2cab6b0d9996aca17fcbc663b83845c14d13c74ee21f38c0b4d50debf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214427026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83f10c3488665f7fb1c6b9e39ef8d8496c2e64bd2a17ff473e63a1f49109f4b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225cb0f2398c82803e0a664bca2838b6952c8625269bacb10309a51d08b246a7`  
		Last Modified: Wed, 08 Jan 2025 04:32:08 GMT  
		Size: 20.6 MB (20646818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372a9834e30bc1a4ac9cf9ed49635b1495df06f03aec898ef29d50dabefc1db`  
		Last Modified: Tue, 07 Jan 2025 03:31:58 GMT  
		Size: 165.5 MB (165513260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9c3a812f9de067e26e45678b86e96db89e7f0dae9089fbdc3c188e4238f4f1`  
		Last Modified: Tue, 07 Jan 2025 03:31:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec9ff0efbdd4303d78867776fe04d39637d68c10fe145cb24df20fc8b1f2478`  
		Last Modified: Tue, 07 Jan 2025 03:31:55 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5e1cc9a17a35ac29c6131c91d94aca45aaec636f4683efff22a23ee458838c`  
		Last Modified: Tue, 07 Jan 2025 04:23:14 GMT  
		Size: 24.6 MB (24649494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4067a0c606df111dcbf6a95f36ab61aa129890ad3a6b1f45392e0942e7cb53c`  
		Last Modified: Tue, 07 Jan 2025 04:23:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38492f4277e7b626509110f1e9e946d010ce3378e68545704a68b6ad44fce8b7`  
		Last Modified: Tue, 07 Jan 2025 04:23:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:7260e1df5d24f4c6ba5912ad0c06563aa0484011da6e5c1f784a39b75cf8df2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1232154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719970fd9733a361fd9aa42bce35cf22a2d9b22fcecf280a816d53580e4a21b5`

```dockerfile
```

-	Layers:
	-	`sha256:14dcaca7c8febf5c4e7923fb3afd869a2044763eef4f4d0473798dfc4998afa2`  
		Last Modified: Tue, 07 Jan 2025 04:23:13 GMT  
		Size: 1.2 MB (1216695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25ed7f2e3e284527634b77f0c1749c048a1446d35f41b3d38161457d153dafb`  
		Last Modified: Tue, 07 Jan 2025 04:23:13 GMT  
		Size: 15.5 KB (15459 bytes)  
		MIME: application/vnd.in-toto+json
