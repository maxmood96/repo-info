## `clojure:temurin-17-tools-deps-alpine`

```console
$ docker pull clojure@sha256:60431b031046dbcee4d42cb18b455e416dc05516ebe7ef19c92bac3895b4eb07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:beecd018864582fc225be7fc5a40e3c41858b98650785172d84f40ffdafa8a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195311848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb843df6f6c812711189287f1711db82c8de0909b6ebf5dcae859dfe6022e291`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:20 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:28 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3246fb1834d21c22ed717db9f8ba3f07e0f562bbeeebdc44a7499d5eb6df47bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:33:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:29 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:03:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:03:52 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:56 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 15 Apr 2026 22:03:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:03:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:03:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e18feb881252411e8481c736f2ef1a8f450f8e9fa28a7834b4cd096ffcc796`  
		Last Modified: Wed, 15 Apr 2026 20:33:44 GMT  
		Size: 21.3 MB (21315838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642fade5205f4033b5c781cc2d6a0fcf038d2f82370ae6789690d81c2cd9b8d`  
		Last Modified: Wed, 15 Apr 2026 20:33:46 GMT  
		Size: 144.8 MB (144762385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec5268d796984af3be20bf1cbadc4a60b0a45eff14ccfda5cb11252b8154707`  
		Last Modified: Wed, 15 Apr 2026 20:33:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b25f7d051ea8167c6952fccc5be5ccf7e6b821446064bb49ec9e2c3e1c80b5`  
		Last Modified: Wed, 15 Apr 2026 20:33:43 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f8ec56d7dd909cebbb51117b1f5d1cd06762e574e21078024cc585b5bac998`  
		Last Modified: Wed, 15 Apr 2026 22:04:07 GMT  
		Size: 25.4 MB (25365981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1f3f4ef05c2cacef2e74f1ed5be210b6b9c5f924c180660dc68d18e94bca4`  
		Last Modified: Wed, 15 Apr 2026 22:04:06 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1620b9a1fb14dea922efb4d61f11de3b8b1a3199170748fbb2435e847ef8c6b`  
		Last Modified: Wed, 15 Apr 2026 22:04:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:1de669fbad05cdee9e22a22da7da102789f5746ca558d39eaba139523454a9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5f5059a96052ad170ac3f7da5b2112f94c0439e0cabb1914497ed9931833fd`

```dockerfile
```

-	Layers:
	-	`sha256:01a4d67699d2cef383696a55f48e0f01ad6ada1827fbe5f32efd119ccdc86859`  
		Last Modified: Wed, 15 Apr 2026 22:04:06 GMT  
		Size: 1.3 MB (1308098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c6b129d3aec860b1296db1e23fc838449bf0401178de09fb2318698a75c7b3`  
		Last Modified: Wed, 15 Apr 2026 22:04:06 GMT  
		Size: 15.4 KB (15431 bytes)  
		MIME: application/vnd.in-toto+json
