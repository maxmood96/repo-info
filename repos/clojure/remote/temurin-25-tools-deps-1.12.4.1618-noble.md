## `clojure:temurin-25-tools-deps-1.12.4.1618-noble`

```console
$ docker pull clojure@sha256:70aef7519c7b90f01d7069b41883a7af84834c92e8a21f45fdbba78d44b36d3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - linux; amd64

```console
$ docker pull clojure@sha256:96a58358e1b96ce48bb37bfeea1262c6fafac721fe87bbf96d027e7823179b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (198002344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11e5c2f2f484dfd5131292cf393e6324fd2ecc685bab79bd8fb0cb6d83338f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:33 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 01:23:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:23:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 01:23:52 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 03:01:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 03:01:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:01:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:01:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:01:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9be28b95192c91c53b88e11c9949a475df4ba95e71ca9a2ec1dad33873891c`  
		Last Modified: Tue, 17 Mar 2026 01:24:08 GMT  
		Size: 17.5 MB (17462244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c318c44e952a3391b86e5db6a972878c9a4f3f9b51cfbf6d22dcb6d19db6084f`  
		Last Modified: Tue, 17 Mar 2026 01:24:10 GMT  
		Size: 92.4 MB (92388668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1e0a39126833701e554d624057517d5d5863a8905ba55396be02741c872e51`  
		Last Modified: Tue, 17 Mar 2026 01:24:07 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f672acba440539e7d4ed4d65ceec6d719bd27e09fe703b53710c156d0695a2`  
		Last Modified: Tue, 17 Mar 2026 03:01:55 GMT  
		Size: 58.4 MB (58416074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aea8c817d3230e5fc8c82ea45afe591513edd2a07a3180ff1f76fb262735b28`  
		Last Modified: Tue, 17 Mar 2026 03:01:53 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948103cfe714b3d015bd661d8cdb45e688c9abdc8fcb4b9ad535823159838cff`  
		Last Modified: Tue, 17 Mar 2026 03:01:54 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:3878fb73dda178e7131c2fe6971976df885e1bf666e332a76c0f45bee5f97cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5809062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b37ac09dc40bfdc172cf596056e27cf767a704d1de029bbc5887615972fe39`

```dockerfile
```

-	Layers:
	-	`sha256:e102b4af6f7d2a547999634750fa06b49cfa7b638a5f167a14cb94cae8a9efc8`  
		Last Modified: Tue, 17 Mar 2026 03:01:54 GMT  
		Size: 5.8 MB (5793528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a38616b08590f6641df6d0139de5bcb834c6b7cb9da6ef4b195eebf621200bc`  
		Last Modified: Tue, 17 Mar 2026 03:01:53 GMT  
		Size: 15.5 KB (15534 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d1ca045b98138cae397cf720424e7bd4a9e31f81dfc0fb18d748c20ad7e2259c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197370773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb63e9dfcc80e08ed900df2a6e1d04e84f32b6fa049cfe218c9fbe92e07585b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:24:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:24:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:24:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:24:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:24:56 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 01:25:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:25:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:25:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:25:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 01:25:20 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 03:05:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:05:57 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:06:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 03:06:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:06:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:06:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:06:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3d70b58e831f52fbc6dce33d3ff1038690642b16b38b6f7db8f98ac5492973`  
		Last Modified: Tue, 17 Mar 2026 01:25:36 GMT  
		Size: 18.7 MB (18654274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94752467d7f7e9b696ae83bfed06b478285d7bde18613ae8de5a2f8bb50fe418`  
		Last Modified: Tue, 17 Mar 2026 01:25:41 GMT  
		Size: 91.4 MB (91424581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4349cc07e9d498e29dc68dab8a1e3ad74d586b4b48867318c2d5fadf02c343`  
		Last Modified: Tue, 17 Mar 2026 01:25:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1144ecbfb90afc900337179ac63a3489c91cd9e68e5032cf3544496af7c5f3d`  
		Last Modified: Tue, 17 Mar 2026 03:06:34 GMT  
		Size: 58.4 MB (58418848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df97ad7f8eab9dc9514dedac0dd3db6694889292fc9f3418a74c7801159ef351`  
		Last Modified: Tue, 17 Mar 2026 03:06:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0d3ccd69fcdb1af743afeac427456fbd5c23656411d12419fbd89549827cae`  
		Last Modified: Tue, 17 Mar 2026 03:06:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:d07689fdcce98cd3bd509b7995fa0cf7428e6eefcd634a90dbb9228a851138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5580937bf83d61db26284ac9b51b18e8b3174da392395752a152f209470114b`

```dockerfile
```

-	Layers:
	-	`sha256:2fe5c127ae95325c09f447d515abe412f25b1e937dcdb1dec15c56d560ddfbd7`  
		Last Modified: Tue, 17 Mar 2026 03:06:32 GMT  
		Size: 5.9 MB (5931145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41cfcf87c89e5c5f1741b91851e4c176c1127cc0073e00122d60e691ef9849a1`  
		Last Modified: Tue, 17 Mar 2026 03:06:32 GMT  
		Size: 15.6 KB (15626 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:b9e83cb06d9bbd7ffd7c63f2c8dd5501fe71428d60fd4544dcfe662eb12b6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207134961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fcc35375a14d97334cd258c40c10cb5e19f087419c19112108afc5a8e85790`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:38:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:38:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:38:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:38:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:38:03 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 08:38:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:38:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:38:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:38:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 08:38:53 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 18:45:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:45:00 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:49:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 18:49:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:49:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:49:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:49:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719799e3fd3fced1bf5442d22aed7fb7582f8aef125453efff5308862d936136`  
		Last Modified: Tue, 17 Mar 2026 08:39:28 GMT  
		Size: 17.3 MB (17328483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fd462ea1b064dfa4c0f2866d0b9c265dbb70fc5dc940ba5349e7e89dca9544`  
		Last Modified: Tue, 17 Mar 2026 08:39:30 GMT  
		Size: 91.8 MB (91756951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f07a919432b86262243e8578a37d80592647d53ec1896888579931c683559`  
		Last Modified: Tue, 17 Mar 2026 08:39:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb5f79922ca2ac44d975dfe49900261337d9457f4db904f9480b339e6b5fe35`  
		Last Modified: Tue, 17 Mar 2026 18:50:10 GMT  
		Size: 63.7 MB (63736114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfa32175f35bde41a13010283ece2ca02f9ff534aa66b22bbe0e539745836d2`  
		Last Modified: Tue, 17 Mar 2026 18:50:08 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85777650028d9b55b098c7ace273fec8517dc2557aee61b9babe86efeacfb6e5`  
		Last Modified: Tue, 17 Mar 2026 18:50:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:f513c9a3d49b480712562aa59c2c8de90f601a82a05dc97a0acb9c2796afb4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5843300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5132c356f2ad949988ce71cf941bef12cfabf1fa945d2ae4a636d964c898b80`

```dockerfile
```

-	Layers:
	-	`sha256:c7583629dc969b8130b11d3648d10c3d435e22c54956fda0614ef958f17e41c7`  
		Last Modified: Tue, 17 Mar 2026 18:50:08 GMT  
		Size: 5.8 MB (5827728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef0f96fccfbc5a05054f14ef44bc95d8af6ee5db51cc88ca6a8afc80b4dfb25`  
		Last Modified: Tue, 17 Mar 2026 18:50:08 GMT  
		Size: 15.6 KB (15572 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - linux; riscv64

```console
$ docker pull clojure@sha256:4e2a4d4f12d3818169baebd3d007c91eb3026e549ef81452660427f6bea8c541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202634034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e6927f3e96eb80ee2d7029fae618ea261ca23699b92f9bd6c367d8b4cd3645`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:42:34 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:43:25 GMT
ADD file:1243b7db425cac690d91f87ad37c1beec0d95da6b3942dc8084039fe1cc2baf4 in / 
# Mon, 23 Feb 2026 17:43:30 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 04:40:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 21 Mar 2026 04:40:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Mar 2026 04:40:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 21 Mar 2026 04:40:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Mar 2026 04:40:25 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Sat, 21 Mar 2026 04:42:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 21 Mar 2026 04:43:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 21 Mar 2026 04:43:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 21 Mar 2026 04:43:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 21 Mar 2026 04:43:08 GMT
CMD ["jshell"]
# Sun, 22 Mar 2026 19:23:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 19:23:44 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:41:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sun, 22 Mar 2026 19:41:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 19:41:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:41:59 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:41:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866473980fd7aa6ac5a8a995315a35248ab945008a1938bd15f65082df53b2d3`  
		Last Modified: Mon, 23 Feb 2026 17:51:46 GMT  
		Size: 31.0 MB (30960145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a39ea40737df0869a665cb1cd59261c3e337da5cacd4b5bf17fab5765e174b`  
		Last Modified: Sat, 21 Mar 2026 04:46:34 GMT  
		Size: 13.8 MB (13849902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61a4c41ee7ac84fc9d708e3b438f588cbe9de5cbf14f708499a9366509dbf6`  
		Last Modified: Sat, 21 Mar 2026 04:46:45 GMT  
		Size: 90.9 MB (90910647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595de38fa3ddd618163afb8e9f42eb19f6a4c7a8ce9d4f89f4b6109fbd005c85`  
		Last Modified: Sat, 21 Mar 2026 04:46:30 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04b4153bc81219d630402174d367871ea9c6422dc5ae5bc4ea86831caa2daab`  
		Last Modified: Sun, 22 Mar 2026 19:45:42 GMT  
		Size: 66.9 MB (66909971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fced5a6d090076db04ad105fc46ce3ba94f3e35635466390679db9acf981376`  
		Last Modified: Sun, 22 Mar 2026 19:45:31 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c15c31259e72d908147e8f94cf7bd70866cda09472a6045125fd382de1ce8d8`  
		Last Modified: Sun, 22 Mar 2026 19:45:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:53f132ac2677f2129a96c26a9517cd17e0d0b2cb68249bd15faa582f5ccc7996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5894842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91aa34821c3b13305ee1f1f69de4799e1aa60bbf8b7c89b2196372b62ad3f170`

```dockerfile
```

-	Layers:
	-	`sha256:29b545fdeb4b4d5dac5cc25d8fb9d6135dffdfe90521d8e361cefa271d7c76e3`  
		Last Modified: Sun, 22 Mar 2026 19:45:32 GMT  
		Size: 5.9 MB (5879270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21836c20c26b1d71f2b24f95f787a01483852cf6c99a263b8f3f847119650881`  
		Last Modified: Sun, 22 Mar 2026 19:45:31 GMT  
		Size: 15.6 KB (15572 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - linux; s390x

```console
$ docker pull clojure@sha256:1c9987372e33526f1759ac0365c1187eb90b8270fecb65e17dd7890dda547cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194532374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee19f689abde44655c970fba0665fc3b2de8242c8ae677ca6cb1ee3148ca8650`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:23:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:23:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:23:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 02:23:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:29 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 02:23:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 02:23:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 02:23:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:23:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:23:44 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 11:43:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:43:40 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:46:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 17 Mar 2026 11:46:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:46:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:46:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:46:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7da6924ab3f673899f7ce0847af6c076eaed73a1d60be6eb8dfd22b82ac4f46`  
		Last Modified: Tue, 17 Mar 2026 02:24:13 GMT  
		Size: 16.3 MB (16302767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e241bbcafac16fde4452eb2a412b6220d6022bf3e598be141cf6a4c6d0c477`  
		Last Modified: Tue, 17 Mar 2026 02:24:15 GMT  
		Size: 88.4 MB (88369717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28937ebe9ebf2504be1eda6eec4bdcec5350eb93cb8a373c0a0783aaa02329c1`  
		Last Modified: Tue, 17 Mar 2026 02:24:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278ee95fb669c3effb2cfacee43b1aa5fbc1f7fbf7b40afd8749cc88efc804e2`  
		Last Modified: Tue, 17 Mar 2026 11:47:01 GMT  
		Size: 59.9 MB (59946146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df608ced00076edd68b3b4400a039ef63a78818bf89730e2e6047f943f945b0`  
		Last Modified: Tue, 17 Mar 2026 11:46:59 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc4378740b6f66eba98039a2717e2cd71c2eb03fe0113f36321bbdd703736e8`  
		Last Modified: Tue, 17 Mar 2026 11:46:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:cee09bf59130f05becf29fb94defe058ce0c60c5a469a59490de9f55ed5c8018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129844852e2c8ac180d2e490f2706ae62503284584436b2265217742b14183f`

```dockerfile
```

-	Layers:
	-	`sha256:717452284848f0c191a6a3566de02f72d63301324ee90ea4342bad2b923dcc32`  
		Last Modified: Tue, 17 Mar 2026 11:46:59 GMT  
		Size: 5.7 MB (5723433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d95e187b649fd53046b434f48ae46ca2b7b8318c808ba044aa3deab36c1cd4a5`  
		Last Modified: Tue, 17 Mar 2026 11:46:58 GMT  
		Size: 15.5 KB (15533 bytes)  
		MIME: application/vnd.in-toto+json
