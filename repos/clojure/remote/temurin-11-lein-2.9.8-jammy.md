## `clojure:temurin-11-lein-2.9.8-jammy`

```console
$ docker pull clojure@sha256:e52eb3fb752ab0744d7e047fced353783e53eb218bbc5c41da5febfb4c1812da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.9.8-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:8dbeedd13300a20f3d8e89f9e4eee7476f3e8b5e6d2c9deb049480867fa53422
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256333582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8aad2d141eeac940c8999b0250540089e6ad11cea0662dce448320ef23deb6f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 19:20:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:20:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:20:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 19:20:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 19:22:41 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 11 Aug 2022 19:22:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 19:22:53 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:22:53 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:07:29 GMT
ENV LEIN_VERSION=2.9.8
# Thu, 11 Aug 2022 20:07:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:07:29 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:07:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Aug 2022 20:07:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:07:38 GMT
ENV LEIN_ROOT=1
# Thu, 11 Aug 2022 20:07:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Aug 2022 20:07:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc15e118841a9f177bca811667e37fe099192eb26678de7c0b49e003dac8576`  
		Last Modified: Thu, 11 Aug 2022 19:30:35 GMT  
		Size: 11.3 MB (11343716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae545d0e244624cad6836109afd6b4fd72d2ea80d41de580f4743574100dc5b`  
		Last Modified: Thu, 11 Aug 2022 19:33:24 GMT  
		Size: 198.1 MB (198127110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e721c03588353305d9e6be4975a7e9a0ae2f1d8e660abcdfaf50905ba46244`  
		Last Modified: Thu, 11 Aug 2022 19:33:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b330a8a867c9de165dc90b63e30c0dcd88ad4e4ca3de34b643fcc4a5c87e8de`  
		Last Modified: Thu, 11 Aug 2022 20:20:16 GMT  
		Size: 12.0 MB (12044553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9717da3b99f76035bb5dacc672d2d95516cb2791ee7f5d9c543c9e22fe64f654`  
		Last Modified: Thu, 11 Aug 2022 20:20:16 GMT  
		Size: 4.4 MB (4391895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.9.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9069c1cbd2fdc632edfc932d38367af7c1d00326a88959fb389d41314779d675
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250761601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ebd9f0b5ebc7d6dd8cda722f6f912cbfa38d15b97e9b4980a2551abad37ea9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:40:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:40:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:40:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 18:40:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 18:43:19 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 11 Aug 2022 18:43:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 18:43:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 18:43:30 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 19:53:39 GMT
ENV LEIN_VERSION=2.9.8
# Thu, 11 Aug 2022 19:53:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 19:53:41 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 19:53:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Aug 2022 19:53:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 19:53:56 GMT
ENV LEIN_ROOT=1
# Thu, 11 Aug 2022 19:54:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Aug 2022 19:54:00 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b941860b1b56dff93374f7988debb6b45635d744ea5fe506bdc3aff09ba84e11`  
		Last Modified: Thu, 11 Aug 2022 18:52:53 GMT  
		Size: 11.3 MB (11311183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06051de7538c100c4092baa889d014909f43621fa81c3bdc7c23b0a5cfbd2798`  
		Last Modified: Thu, 11 Aug 2022 18:55:14 GMT  
		Size: 194.9 MB (194871143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ccc1a6712100b1e7edd29f3a2bcf08585a6cff7265676804c385ae60a8d07b`  
		Last Modified: Thu, 11 Aug 2022 18:54:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62eab7e54423d7208d2c6a5f02cefd0cc9e0d7e75677b5da0ad0e0b988325d0`  
		Last Modified: Thu, 11 Aug 2022 20:08:03 GMT  
		Size: 11.8 MB (11806142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ba5ed739d0dd44c632fd81462b3528367dfe7f51b37bb3ed46a3408388b467`  
		Last Modified: Thu, 11 Aug 2022 20:08:02 GMT  
		Size: 4.4 MB (4391820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
