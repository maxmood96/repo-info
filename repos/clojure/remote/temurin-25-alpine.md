## `clojure:temurin-25-alpine`

```console
$ docker pull clojure@sha256:f9ad3e2061c0623cb79428299ede4c7ae4b7362f38e5cce6a8f1fae646c2795e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:d27436c687918534a0285311d7d98b8f6cc9556add281e44bf64f6f23de63d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136071838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a259e5a4e4dee70cc49fae498ac1394fca794d893fe75884844690eeda3dc3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:34:21 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:34:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:23 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:06:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:06:28 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:31 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 15 Apr 2026 22:06:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:06:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d78fbd718571b55d30809c1f3843638bd7b326cdd00fa9b1ad70fa32d1275e`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 14.3 MB (14307228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0758b0503e9474a80d86a6848a74591d1f0224e311fa3e17a5bfa334cd0fd3`  
		Last Modified: Wed, 15 Apr 2026 20:34:45 GMT  
		Size: 91.5 MB (91491756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43844d5cbff66283e09e3dc341de140a185899429dda46c135c2ddbcf13680a7`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8f14395c3629db1f2892a1628820feeeff222bb4aad5de5321d266613dab26`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd7dd5280fdc48084a316c1d798d1dfa328bb60cf4525ce4ee7f67a5038be29`  
		Last Modified: Wed, 15 Apr 2026 22:06:41 GMT  
		Size: 26.4 MB (26405205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150066adfdfd13b41ee1a3716d4487cc9fe1352b182f2096459ee26629a42b1`  
		Last Modified: Wed, 15 Apr 2026 22:06:40 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed20cf9493b78c34febfaad8573ef9b63c800196f84c3f8c7cf19dbdb9c1f414`  
		Last Modified: Wed, 15 Apr 2026 22:06:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:0a3823205b4270804a439e2197459012bf1d5bff1b705f2309b084745c9a3804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1223548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4019bba59d182dc775bb9c3110c318e9129b6696f7af9f20020f4ba3e6f3e7`

```dockerfile
```

-	Layers:
	-	`sha256:9305dc67c335aa6b45609793abec71212e2355b3d50e72b6bedd1f84273afbbe`  
		Last Modified: Wed, 15 Apr 2026 22:06:40 GMT  
		Size: 1.2 MB (1208122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c50b06d6632e5d025247de1c961d8715e9cb56d7e560a3b514d349cfbfef10`  
		Last Modified: Wed, 15 Apr 2026 22:06:40 GMT  
		Size: 15.4 KB (15426 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ec8ac08f54077c626790ac65014e4361fa0222ef24c74663e57b3ee19277c65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135572505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f9e83994845bb1ac955d48ed6ccbcf18e3041719dfd5b9bc3b2989c02ef86b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:42 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:42 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:19:48 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:50 GMT
CMD ["jshell"]
# Mon, 09 Mar 2026 20:36:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:09 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:13 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 09 Mar 2026 20:36:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:13 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc273c5968a27128010b44442da19c1d19512b5d65a3a7fc4734eec44550e27`  
		Last Modified: Thu, 05 Feb 2026 22:20:05 GMT  
		Size: 14.4 MB (14373158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47108ee2f22449f768312319f1c90c0d5a1580374197687fd1944d8e2265225`  
		Last Modified: Thu, 05 Feb 2026 22:20:07 GMT  
		Size: 90.4 MB (90431353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fed661f46011e75ee9460b18305d0584e08525180dd346895a225fab422298`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47f9177a4521d408115970652519968867bb5c776093bf3b8b10b66aaa3caa1`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09cb0c56395f1d4ce73895028273af509e7aeac1527dc1bcc27ff28ec1c0697`  
		Last Modified: Mon, 09 Mar 2026 20:36:22 GMT  
		Size: 26.6 MB (26567441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ba3027c219703fd08fef4db98fdfaa3c7c607288730c844efe4a64f8f3be5`  
		Last Modified: Mon, 09 Mar 2026 20:36:21 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b488e4e60b0c2e292f00d7c0361ee1065228113eb29fa0c806591fb106a19bfc`  
		Last Modified: Mon, 09 Mar 2026 20:36:21 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f8e5d70845a606a40f90bd336f868a68b858fa3595a5a3987224d72238c88389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1374944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081260a867e3cd342ed0a30dd7372db48997030f094ca1f251d080f3aacf1bc4`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ebe245fba5fbbee6ef4da3ff94fc05a67b5f49aba7abdf69c6a205b23bf1d`  
		Last Modified: Mon, 09 Mar 2026 20:36:21 GMT  
		Size: 1.4 MB (1359426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b96073201043656896740ae12fc2c12cba9ee62272e878e30cc41578fa466fd`  
		Last Modified: Mon, 09 Mar 2026 20:36:21 GMT  
		Size: 15.5 KB (15518 bytes)  
		MIME: application/vnd.in-toto+json
