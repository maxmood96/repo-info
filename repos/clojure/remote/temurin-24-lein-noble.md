## `clojure:temurin-24-lein-noble`

```console
$ docker pull clojure@sha256:bd081ddb2a4f88fd30bfb304746fb05e4656b05470a5e1a71e49fde230025664
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-noble` - linux; amd64

```console
$ docker pull clojure@sha256:9aea82af388d56f8b530a7aa52bbd22b0ce89e5415783d8adcdb2fe530b4ea64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184564442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b7ab30b416bb26c738fdf904cd941f4f7ecc73bbb64370588bd877d6488da6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='a1d993ab0b4b80101ec2e2452bdd37735572b734c255576a47c5130eab55f09a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e424a5f4017c616dd70e460381d8638ca74da30bce4cc759914e06c782aa2b8`  
		Last Modified: Wed, 09 Apr 2025 01:16:38 GMT  
		Size: 21.3 MB (21326882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ff1ff9a059dfbbea99287fc827dcbaab5bbb5f34f047e9e13fd5435637e80f`  
		Last Modified: Wed, 09 Apr 2025 01:16:40 GMT  
		Size: 90.0 MB (89956637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21c27cceb184256ee474b28fbafebf0ea555626b31cdfc372746ab7e12839f0`  
		Last Modified: Wed, 09 Apr 2025 01:16:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac5273a3f27a429a7c105f24a5c0955578c613bfde30317b4c420cd0f2c502c`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 39.0 MB (39046418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87184a483cfc014a2effab0162e8519659cac08df0349ab207dd8fef39978222`  
		Last Modified: Wed, 09 Apr 2025 02:19:14 GMT  
		Size: 4.5 MB (4514108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce127b1284f15f1acb7b40121c7473dbba82202916fc5dea0c40b3d3726c6b37`  
		Last Modified: Wed, 09 Apr 2025 02:19:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:e2ee5adc517b16c07b333d4f6f48e3e13abc62836446ccca5ed91649d8536e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4950233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5f62665acbc723b99e74a929712bc7db28165be0c445afdceb1c7169195f8c`

```dockerfile
```

-	Layers:
	-	`sha256:c9eae63bfb5c5f16f43158ee43ab871f1dadbbe6707705a1377f6e560422d086`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 4.9 MB (4931824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d19a556809908d6ad442ee06d673986594e65ba5e777b616ad77d820f79617e`  
		Last Modified: Wed, 09 Apr 2025 02:19:14 GMT  
		Size: 18.4 KB (18409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:56f8a48e833b8a606d38f0248105afcf62ab0e3ea59235e05a67512cea9e8f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184122832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec7187414cef01319f8ec66cc2da78926f2e92f29dba86b300aca90f7e0b319`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='a1d993ab0b4b80101ec2e2452bdd37735572b734c255576a47c5130eab55f09a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1f88b0048087a927aaa11ebe30b554ae89bcf45d82f54e062e83cfbd360155`  
		Last Modified: Wed, 09 Apr 2025 07:09:46 GMT  
		Size: 22.5 MB (22505411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03d5053eb7b361f72cc13c49b6196523cf837d820bcfb38c5a6e1e38ef865fd`  
		Last Modified: Wed, 09 Apr 2025 07:09:48 GMT  
		Size: 89.1 MB (89093483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e180717685609933b5eb7bfea3b99fef248102e202ac6d46474033ae8bef8089`  
		Last Modified: Wed, 09 Apr 2025 07:09:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff4d8bde3bce41d60aed317cccfd71e4c943b79a0e443c505f7fee9db1399a5`  
		Last Modified: Wed, 09 Apr 2025 17:51:17 GMT  
		Size: 39.2 MB (39160087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce95c182dfaf9dbe1acaf13d4d42d45fe339ada47b2b48624501de62466d4ba`  
		Last Modified: Wed, 09 Apr 2025 17:51:16 GMT  
		Size: 4.5 MB (4514146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f06651d10704b3b169f32a80083015b7fe95203526abe29bc8945e7628fe3a`  
		Last Modified: Wed, 09 Apr 2025 17:51:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:1b331c531bc11a19b03548e395f9b517fa0051c95c72fce895d624a0c1382543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6499cfc682b71d5d05a059ff0b914414986d5ff51dfaadb93b741df56d6262`

```dockerfile
```

-	Layers:
	-	`sha256:1e619f1f9ed08041a1cf3764f26199d1d004bdce4ae2957a65aa20723c22c10a`  
		Last Modified: Wed, 09 Apr 2025 17:51:16 GMT  
		Size: 5.1 MB (5069370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3dbb03aff740051274f4a802cbca1bbe8772aa5058ff8c5781aec27f535877`  
		Last Modified: Wed, 09 Apr 2025 17:51:16 GMT  
		Size: 18.5 KB (18504 bytes)  
		MIME: application/vnd.in-toto+json
