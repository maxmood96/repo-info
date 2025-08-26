## `clojure:temurin-11-tools-deps`

```console
$ docker pull clojure@sha256:d4e7765eb065f68ee8b3455f43a627fbf060e10916b7b4feeb4567e7848cd867
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:493ae06a4b1b2742921138ee639ea862c01da4866a37dce9e6844f464835a085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247497582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3769f8628d7e133616cc9d9bc098018c9e96f7a9c1dfafef27ae443a2cab2b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebddd0f241035b3ac279bacb85896c78bc53f995e51ea210d037e262e39b01a`  
		Last Modified: Tue, 12 Aug 2025 17:24:41 GMT  
		Size: 17.0 MB (16971712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488732cd9995947c08132df4d04851ff13a96dce2af8d560dfdd81c85051d296`  
		Last Modified: Tue, 12 Aug 2025 17:53:19 GMT  
		Size: 145.7 MB (145669216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae6624228d7d81e9d7fb906d6393b41ccf4f215e26a0c3e24136d4385a6f9bd`  
		Last Modified: Tue, 12 Aug 2025 17:24:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9456c27737eb949b81db43a51b05c1096d5637db00cc473b7e13018b17b9a92`  
		Last Modified: Tue, 12 Aug 2025 17:24:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0478c097629a5872b921848750447497ebbd3ec2616e8695c3787bee5ee6bef`  
		Last Modified: Tue, 26 Aug 2025 17:28:11 GMT  
		Size: 55.1 MB (55130350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7565eb49bd1aea44a9f9c80f68ab40786b18bcbbefc6174ce1941de2cbabef1`  
		Last Modified: Tue, 26 Aug 2025 17:28:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:210d185e5df164818a39104bf29b7d395c8cd0d1036f72266c3180543d29548e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5786902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c73fd57c2fd296c95862dcf10b64a87fe4b0815f104ca759c83fdcb4184cede`

```dockerfile
```

-	Layers:
	-	`sha256:8686db4e46976f0474469f26a9497c5d6cbd97a6ec1295bab30f2b8b85b6281c`  
		Last Modified: Tue, 26 Aug 2025 18:36:05 GMT  
		Size: 5.8 MB (5772668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660659ff8e78091b887a43645044f8cc24c2caa1d5e74cbd0d0b0e5c0b2fe390`  
		Last Modified: Tue, 26 Aug 2025 18:36:06 GMT  
		Size: 14.2 KB (14234 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad5e11e8e3e05318f6982bf8c44c133dc0cdd671da1f82488a8f7f8e6e0b9060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243387676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694c75902232c574e3c6b13bf582e11a91a8b7a4183ca28db154f20b058d0c1c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3eefddfbcab06ca4f10ce56a232d4ec2d822b72ac91b8958abc9acd3c4223c`  
		Last Modified: Tue, 12 Aug 2025 18:31:54 GMT  
		Size: 17.0 MB (16988833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5604d256c331353ad0b7d919fff68b4e5451d6ccf77e9544d5a2386a51097606`  
		Last Modified: Tue, 12 Aug 2025 21:18:44 GMT  
		Size: 142.5 MB (142465489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77b4329086092251cbc41af0e8446b11c7e2012cd29c7f59905b4d2f143dabb`  
		Last Modified: Tue, 12 Aug 2025 18:33:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc383dcd537d2af9789da6a706eda5766cf726a8f2f0c0054c08fee68bb505e`  
		Last Modified: Tue, 12 Aug 2025 18:33:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f190b3db9583dfa65c5bd6dbfd4dffada90c7de0374a3f87ff211fff9b30338f`  
		Last Modified: Tue, 26 Aug 2025 17:38:53 GMT  
		Size: 55.1 MB (55069889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f195507d110ee248db3639986b4ad16a36b317457c548b3c944d342be77d7d`  
		Last Modified: Tue, 26 Aug 2025 17:38:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:4d36ca8d855ef06166ab59d478487dbdf71e65159e34fb4f902622b21f9d99f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7786cb842685d355024c761e22f7e9273fac405b4d7451c24546db7f444517ec`

```dockerfile
```

-	Layers:
	-	`sha256:317b7f4227e82f40e91e10dd1a1bb72147e9d3c507d7082440b98a235de981d1`  
		Last Modified: Tue, 26 Aug 2025 18:36:11 GMT  
		Size: 5.8 MB (5779874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3a69d076f36ae792f4e9bf681dc474f46252673f50087404bd09357889d928f`  
		Last Modified: Tue, 26 Aug 2025 18:36:12 GMT  
		Size: 14.3 KB (14349 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:6f9c52da61c31e4baca1c753be36b8edfea084c1b1eaa7af30a17759af0471ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245759998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f596090c3df2b4e2ded748e1fe93bdb037406d9967a083cf47f51f259e1b4b0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096eab1deeb8fde16ff57db7eaa184cd4e8ab0d206018acdb9ab5ac1843566c9`  
		Last Modified: Tue, 12 Aug 2025 17:31:12 GMT  
		Size: 18.8 MB (18814780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263b0bd45afde24f479bcff4236faba3efa1587afa88b49ecc4ae5358fc7cca1`  
		Last Modified: Tue, 12 Aug 2025 20:36:09 GMT  
		Size: 132.9 MB (132863065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2995d9ff14f3b1510b31fd7cb09d3841396fd3805799e3729a380d9c1d2330`  
		Last Modified: Tue, 12 Aug 2025 17:34:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6093df0a500fbf3ba171218d2efe470b7703e18ba6551abb1b5fe7b36228671e`  
		Last Modified: Tue, 12 Aug 2025 17:35:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb8a8408f2bd18fb6cfd6d6eb3a623e9c22e9fa076e14ce28aaf6bccf9a8b1e`  
		Last Modified: Tue, 26 Aug 2025 17:47:22 GMT  
		Size: 59.7 MB (59749413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a179a0f14fc195c898eed12e15373fb7f1bdfef8f558773a0565ed61858265a`  
		Last Modified: Tue, 26 Aug 2025 17:47:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:d7e542496c971722a73329bf575ee3f8882009e86e7558db20092ffea5542172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185e63ccbe6366d3578cc3192e2f45e265dd11c703f8d47074b07f73f641bfcf`

```dockerfile
```

-	Layers:
	-	`sha256:5355aa4bddf423289523b24948c9fa97c40f15fe7ffd5ffcdcd48c04b6cfe6dd`  
		Last Modified: Tue, 26 Aug 2025 18:36:17 GMT  
		Size: 5.8 MB (5777298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afdc1eab7c02e391d8d9ff41f46d32e4f78e9a3352c73b09083ebde133de5ab8`  
		Last Modified: Tue, 26 Aug 2025 18:36:18 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:f1e294178a2351d6b2a43b0c15c6cc0be7d45dc4669cac19805c11fab81fd69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229644386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419c5fc09cd8d5a26e3003b1eaf0404b7517a270e0fbf56cfaea038636ea5899`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 30 Jul 2025 06:55:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:55:12 GMT
ADD file:f751959e6b8dae58a35017dc82c7271708f085c111710b59527373699b0784b5 in / 
# Wed, 30 Jul 2025 06:55:12 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c5d0b18c745fadd2e177b54d4df793f25b01437577bc09c72ae52a0f3f9aeb3`  
		Last Modified: Wed, 30 Jul 2025 11:30:49 GMT  
		Size: 29.9 MB (29932680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be43c90819238ceb0f3b3a9810a063a7e4b16e3faac49694c12e7ffaf1bf1717`  
		Last Modified: Tue, 12 Aug 2025 18:15:47 GMT  
		Size: 17.6 MB (17580544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5242cc1dcfd1cd5b8f803e8b15d72433b439e30805801c357459596386da55`  
		Last Modified: Tue, 12 Aug 2025 18:15:55 GMT  
		Size: 125.6 MB (125635904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562912e9a800eda52fdfb67b6a081b9c5f2dc6fa1238d33f59606297ce1f4724`  
		Last Modified: Tue, 12 Aug 2025 17:57:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faec723017c186c6cd9e4c4034de12ced98a38555bd0476e8a3b8d856ccb54c`  
		Last Modified: Tue, 12 Aug 2025 17:57:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12ef3d9cc93259312537513be15710e6dc52a07005a9269dff7b36b586efdb4`  
		Last Modified: Tue, 26 Aug 2025 17:55:15 GMT  
		Size: 56.5 MB (56492170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3c5bbbbcb85541823da7953d57eed6ff85a5c8ca8788e917782203b5602eb7`  
		Last Modified: Tue, 26 Aug 2025 17:55:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:c164632eb7056d79f74ce47243680c360c5a197a2f265d44cb4fe2eb74c873e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5784242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feeb8d6aace693a2d8a643eddf1d5dd8bdf3cac4c724a2129777281fc176f76a`

```dockerfile
```

-	Layers:
	-	`sha256:1c6bff50bc46976f9048392b5ffbcfdbaba351ac5c131187a90b0ae291720839`  
		Last Modified: Tue, 26 Aug 2025 18:36:23 GMT  
		Size: 5.8 MB (5770008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f14cc28642069f4239397179392a06b2f6c7ae02960548822095c5679b9986db`  
		Last Modified: Tue, 26 Aug 2025 18:36:24 GMT  
		Size: 14.2 KB (14234 bytes)  
		MIME: application/vnd.in-toto+json
