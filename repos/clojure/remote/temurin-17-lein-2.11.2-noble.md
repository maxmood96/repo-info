## `clojure:temurin-17-lein-2.11.2-noble`

```console
$ docker pull clojure@sha256:bd79923992e68e9dc53168fca40efd2f9337881430f07ef2b6ac42ba67852bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.11.2-noble` - linux; amd64

```console
$ docker pull clojure@sha256:0274d5d3dae07d738ab086e4405129548fd2ae72ac2becb640978963f950f815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239725447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a61aade8399cf88ebe63041fe5f8b5f2e749a3059a64c35365c23501134376`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ARG RELEASE
# Thu, 03 Oct 2024 17:49:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 03 Oct 2024 17:49:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 03 Oct 2024 17:49:34 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8682892fc02965930b9022c066fa164dd6f458ef4a5dc262016aa28333b30f49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='0c17fa4f14c0d2cc9e9334f996fccdddc5da4459d768f3105c7ff0283c47bf62';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='e69d43be937e05dbccae4cc98f732ed86aa11993234bf5ad6e81c30475a78ce7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='d4e553c6fa7afdfe2577420c6e77a558db8113a3cef84e755384148f5610834e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='e7c82833a7381a05cae2be0e947c08e971bbae4f2e4142c6ec87bbd7530a5646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='1f824d7369dfd570dc561e2a56035fdcd2970c97cbd355f6deb6ed0e7c6bcb79';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["jshell"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c83835a594a8b0613ec21fa579a8e40cfe71b50991cfb84b8ad0901afeac2`  
		Last Modified: Wed, 08 Jan 2025 04:42:46 GMT  
		Size: 22.9 MB (22948557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735344c4030102dd4f803056f564831c3c572c0f49f8412c61c2d0c6e2833072`  
		Last Modified: Wed, 08 Jan 2025 05:04:39 GMT  
		Size: 144.5 MB (144542438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb6bbb9e7eae15223a1b9bec4f44d764a5f61608c199f1207dc11a052b3b7d8`  
		Last Modified: Tue, 03 Dec 2024 02:30:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9d1e181a2a2b6ed242e21c8a4d40d33cf851fd5522737a9aaa8a708d215f94`  
		Last Modified: Tue, 03 Dec 2024 02:30:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8149de16253c2fafaedeb6f96cb1c26f586b5545b794b6de776c6458e007651`  
		Last Modified: Tue, 03 Dec 2024 03:19:46 GMT  
		Size: 38.0 MB (37965456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d129b8fc664f58d2dd9935a6acc7f6fa82ee2daa932baa645ce572f587538014`  
		Last Modified: Tue, 03 Dec 2024 03:19:45 GMT  
		Size: 4.5 MB (4514154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d5adcf1b147090e711b0397306e6980d2ef77c4f2066fcaabd92a2c1afaed4`  
		Last Modified: Tue, 03 Dec 2024 03:19:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:d4ef3f75fffe2f651f4438f44f97f0fe283dd80978be83ea35a8e56fb159e924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5009347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdcc9dc6c85262dc287cf48cc4ee745189e9835b0204272bf65f6939ffa7d05`

```dockerfile
```

-	Layers:
	-	`sha256:d2680f5967a9d6268436f3eed615d5c7454d8f976270f53b382135a0f6b8f943`  
		Last Modified: Tue, 03 Dec 2024 03:19:45 GMT  
		Size: 5.0 MB (4990918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a77ec98e67d6bff4d5f6de7d8c7e5b1b4418d4271b53fb19a71bd2e6592e11`  
		Last Modified: Tue, 03 Dec 2024 03:19:45 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f9c117a491718f583d6cfd455c1e3ea3f39ddef8b41afe8af9751a264ac151c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238991125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8215a7f922f526988c1f31d664a833467202279ff1d67378b30e2dd19496f1fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ARG RELEASE
# Thu, 03 Oct 2024 17:49:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 03 Oct 2024 17:49:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 03 Oct 2024 17:49:34 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8682892fc02965930b9022c066fa164dd6f458ef4a5dc262016aa28333b30f49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='0c17fa4f14c0d2cc9e9334f996fccdddc5da4459d768f3105c7ff0283c47bf62';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='e69d43be937e05dbccae4cc98f732ed86aa11993234bf5ad6e81c30475a78ce7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='d4e553c6fa7afdfe2577420c6e77a558db8113a3cef84e755384148f5610834e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='e7c82833a7381a05cae2be0e947c08e971bbae4f2e4142c6ec87bbd7530a5646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='1f824d7369dfd570dc561e2a56035fdcd2970c97cbd355f6deb6ed0e7c6bcb79';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["jshell"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4710d3748e6eecf27ed172c1655ce54d98b0ba8e89dbcfe941361161b2a0618c`  
		Last Modified: Tue, 03 Dec 2024 05:50:57 GMT  
		Size: 24.2 MB (24159369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541c9eefc8a3c1cb3f8f2bb6e1fd1bcc202032a6c2d25405a46289388e7ffa3b`  
		Last Modified: Tue, 03 Dec 2024 05:50:59 GMT  
		Size: 143.4 MB (143368186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f75a3586fbf1ee58ff56c3fe189c7fe5a1ae073fcca833d607508b8c098967b`  
		Last Modified: Tue, 03 Dec 2024 05:50:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae76379d9fa81ce9f3f8eaf6297921926bd624e57d53568aff0ff97ed801ed73`  
		Last Modified: Tue, 03 Dec 2024 05:50:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad1bd89119977db03dc7f66bdd40b86716e7f238d6cc64993c4585da00b277`  
		Last Modified: Tue, 03 Dec 2024 15:20:12 GMT  
		Size: 38.1 MB (38053899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34114b3b505f5d470dfa713e2f1b122f4c600fa74222431acd133ace7e5a1ceb`  
		Last Modified: Tue, 03 Dec 2024 15:20:10 GMT  
		Size: 4.5 MB (4514129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670b693235851f4df7e5a7401aeaa7d3b641173c1e066a885763498f5b6a593f`  
		Last Modified: Tue, 03 Dec 2024 15:20:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:b541f75e64e54b91c018be53cc0e9bd8d66955cf34d37ae45c7917cbaec36f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febd95df66fc7b006534e844a530ae65600a130cba6c2379ee07fd8f31ae63d9`

```dockerfile
```

-	Layers:
	-	`sha256:8375ae799e715545551edf970c867609b05c92c9de002af9ff56bfd109df013e`  
		Last Modified: Tue, 03 Dec 2024 15:20:10 GMT  
		Size: 5.1 MB (5128636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58273b1943ca1181ceedca77c1f638e250ecad8c1c3ed02a6da7cc6a20f8e82b`  
		Last Modified: Tue, 03 Dec 2024 15:20:10 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.in-toto+json
