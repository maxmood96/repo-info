## `clojure:temurin-21-alpine`

```console
$ docker pull clojure@sha256:7508101818874e1c0742f7eb4b8ebc2d07641dd62d7ab19c8b2b1aa5b72210d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:323a46124d71c77a5519d1aff553885d65034fea6b20a3f5653c6648e193941a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208668426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdad2b36f60b975da8991b58b6b0f9fbf51b6afa301411da7652154e3390ef0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:52 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:02 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:04:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:47 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:15 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 15 Apr 2026 22:05:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ef2c34364d42e41eb14af65c85cfcd9ba8407f18b51bde4f6428bff92388a2`  
		Last Modified: Wed, 15 Apr 2026 20:34:17 GMT  
		Size: 21.3 MB (21315853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136a888652a1277373c20061d1c0d79e332ba8eece5ba04c0c24fce61ce8940d`  
		Last Modified: Wed, 15 Apr 2026 20:34:20 GMT  
		Size: 158.1 MB (158118925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b440bedad35bcaf95f5c16474e5bcdc67677eca1377bc3b6bd9a64aa13552d0`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c1bb0b54884876ce179c9ad3683a68d7689b97597df8b1b2dfeeaaf5e7b60e`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7434fa0f34ee64153984a987269460cfa18630aec6ae996254d24926a5a4b53`  
		Last Modified: Wed, 15 Apr 2026 22:05:23 GMT  
		Size: 25.4 MB (25366000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fce256c628131c6edf3cba3dc19c0bbc6324a31b5e83c026fc93ef61ef55e`  
		Last Modified: Wed, 15 Apr 2026 22:05:22 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec87b64890734ccd18af24b2fdb2c0142c402cb9b369472a1eccf6b405ff8f4`  
		Last Modified: Wed, 15 Apr 2026 22:05:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:9d9fbc0251d6b43716ea324c9906358ab468fc7f9068807ebcf03b3bd9fc1839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a879e559df1b5814e51f35d217d8674cec42f9f13d579b18e1317bc80b0b42ff`

```dockerfile
```

-	Layers:
	-	`sha256:e7d42c356e70f1d5affaf227688aa84b27d9b8d2b37cfc5606fc24cb87a2d7fd`  
		Last Modified: Wed, 15 Apr 2026 22:05:22 GMT  
		Size: 1.3 MB (1309950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:567dfc2a05928342d7668b09d748cc8bd2484bdf169abcf2fc1f932f10b78c45`  
		Last Modified: Wed, 15 Apr 2026 22:05:22 GMT  
		Size: 15.4 KB (15431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c28a8f9f341e4c26df21ec4446a1597ee411b4dfe87a79cba1611e0cbd781892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207159932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e92de2fbfd1d08c8b754458080c07af9ad7c14104ebed1d6593af873c31cc2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:18:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:18:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:18:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:18:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:18:10 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:18:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:18:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:18:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:18:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:18:18 GMT
CMD ["jshell"]
# Mon, 09 Mar 2026 20:35:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:28 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:33 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 09 Mar 2026 20:35:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5089fa766c3c57eb5cdb3a5598c7f03110834ceee51d81992317c110371aff`  
		Last Modified: Thu, 05 Feb 2026 22:18:35 GMT  
		Size: 21.3 MB (21312383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17a1043f9baa0dcfa204d652bd299bd7e2ea6bf633efb9cd52c3f9f54976b7c`  
		Last Modified: Thu, 05 Feb 2026 22:18:38 GMT  
		Size: 156.1 MB (156130023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b7508607faa8f1e571f0bf716125a563c17b8e3883efba109aff61801ae738`  
		Last Modified: Thu, 05 Feb 2026 22:18:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f522a964bdc39f18b044b5e8f2817027173df17e2d19e26e356d7ef7c4afa85c`  
		Last Modified: Thu, 05 Feb 2026 22:18:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b23baa818b89509e6830f107cf3b9cba0e6296450c59338166284023ea0bc32`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 25.5 MB (25516968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc18cec856d13147e6014577865eacec678ded439bf177266ff934f0bfa48ed`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641a8d14188bfe5ec6e2d7083c398851b8d05eb2236538db71dac0585b410579`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:ea1e48ee535df2f9bfbec038557d96d68235adff56fb60de89d619a906f6db52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1476780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72860bc70ecb294d85b95b0c17755919494ce331ae7e444581a08794f553c6b0`

```dockerfile
```

-	Layers:
	-	`sha256:e0bad222ad9f52cde32b7706b469fa46e9128de7ed408671ff54770cc5fc9b9a`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 1.5 MB (1461257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:385a6bb1cfd165efb2ca75ec3d48444b49bb2e34057cbe57c9179614015dc2b1`  
		Last Modified: Mon, 09 Mar 2026 20:35:42 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json
