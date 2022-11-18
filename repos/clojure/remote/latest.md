## `clojure:latest`

```console
$ docker pull clojure@sha256:d2f66082258257c3951c4d417af8b61ab97741907e2a0bd0e37324755ba7cfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:4bc2ce7126f4615c303660903101fb2802697d91ee21672273ebb2d3845771c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365772936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a38204dd17a2dbced987db864a83d514199f2a296a68732dd43159d314121b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:45:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 20:21:11 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Mon, 07 Nov 2022 20:21:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c26c0e09f1641a666d6740d802beb81e12180abaea07b47c409d30c7f368109';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        armhf|arm)          ESUM='e7c81596f67b6325036e9182d012f2266ced5663c5d4b0de0540ce62dcc67718';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a426a4e2cbc29f46fa686bea8b26613f7b7a9a772a77fed0d40dfe05295be883';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6fc21601d3cf08584e698d676249a91b6a9e790c8fc7c4d9f294628562e16273';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='482180725ceca472e12a8e6d1a4af23d608d78287a77d963335e2a0156a020af';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 07 Nov 2022 20:21:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 07 Nov 2022 20:21:23 GMT
CMD ["jshell"]
# Mon, 07 Nov 2022 20:44:08 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 07 Nov 2022 20:44:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 07 Nov 2022 20:44:08 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 20:44:17 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 07 Nov 2022 20:44:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 07 Nov 2022 20:44:17 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 07 Nov 2022 20:44:39 GMT
RUN boot
# Mon, 07 Nov 2022 20:44:40 GMT
ENV LEIN_VERSION=2.9.10
# Mon, 07 Nov 2022 20:44:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 07 Nov 2022 20:44:40 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 20:45:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Mon, 07 Nov 2022 20:45:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/:/usr/local/bin/
# Mon, 07 Nov 2022 20:45:14 GMT
ENV LEIN_ROOT=1
# Mon, 07 Nov 2022 20:45:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 18 Nov 2022 22:20:00 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:20:00 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:20:39 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Fri, 18 Nov 2022 22:20:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:20:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:20:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:20:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fa72e018dd1c616d4bdb23d6fbb735820db9a943b470a787973556d4ee24e`  
		Last Modified: Wed, 02 Nov 2022 18:50:22 GMT  
		Size: 17.0 MB (16986189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06768b8afb03c8fcc4ab8c603e517e6dfcf7bae1d192387172bae8f1c67a9ddd`  
		Last Modified: Mon, 07 Nov 2022 20:25:35 GMT  
		Size: 192.4 MB (192440285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c12ca51ab8038afcf4a8a81f280a136af3f8019ff907e66caa14bb42875edff`  
		Last Modified: Mon, 07 Nov 2022 20:25:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4029f8808ada5cd851c6a38ca62af1eba3017aef81d63aa58ecdea6226eee1fd`  
		Last Modified: Mon, 07 Nov 2022 20:56:08 GMT  
		Size: 338.6 KB (338624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b505031aef67f92e149fcff00da27db96ada41435055e079dac0d3247cdc798a`  
		Last Modified: Mon, 07 Nov 2022 20:56:11 GMT  
		Size: 58.8 MB (58820510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f760df016d7964f72e0dae673fde5e4fe0895b5d76f2516d79417a773781ca`  
		Last Modified: Mon, 07 Nov 2022 20:56:06 GMT  
		Size: 12.4 MB (12380600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c136aa58584fb511e0f9ec4fe790451416195aba9815a06016bab432ec6a1c1`  
		Last Modified: Mon, 07 Nov 2022 20:56:06 GMT  
		Size: 4.4 MB (4398840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76edb3633155daa010af9d22d785ba71a4e763fa3862251a46c0e0ee599481bd`  
		Last Modified: Fri, 18 Nov 2022 22:31:44 GMT  
		Size: 50.0 MB (49981088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c890abd4118e4bf75bc4f5741d3fb211acf4739051c07fd0af159c7c4629b`  
		Last Modified: Fri, 18 Nov 2022 22:31:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fba0885931ca70dda18b957782c1c4ffac3c6f414fb796461df45c952801d3b`  
		Last Modified: Fri, 18 Nov 2022 22:31:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b4f24a23da5f07da4076bba0b03ecb131dc096f1e841dd5225272005b69cd5f3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363896302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72f69b9c5085b6b5d9e928c18a72d17373215cd39540c6f97ec635925d0f4d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:45:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 20:40:25 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Mon, 07 Nov 2022 20:40:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c26c0e09f1641a666d6740d802beb81e12180abaea07b47c409d30c7f368109';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        armhf|arm)          ESUM='e7c81596f67b6325036e9182d012f2266ced5663c5d4b0de0540ce62dcc67718';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a426a4e2cbc29f46fa686bea8b26613f7b7a9a772a77fed0d40dfe05295be883';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6fc21601d3cf08584e698d676249a91b6a9e790c8fc7c4d9f294628562e16273';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='482180725ceca472e12a8e6d1a4af23d608d78287a77d963335e2a0156a020af';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 07 Nov 2022 20:40:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 07 Nov 2022 20:40:44 GMT
CMD ["jshell"]
# Mon, 07 Nov 2022 21:01:04 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 07 Nov 2022 21:01:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 07 Nov 2022 21:01:04 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 21:01:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 07 Nov 2022 21:01:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 07 Nov 2022 21:01:18 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 07 Nov 2022 21:01:37 GMT
RUN boot
# Mon, 07 Nov 2022 21:01:37 GMT
ENV LEIN_VERSION=2.9.10
# Mon, 07 Nov 2022 21:01:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 07 Nov 2022 21:01:37 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 21:01:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Mon, 07 Nov 2022 21:01:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/:/usr/local/bin/
# Mon, 07 Nov 2022 21:01:56 GMT
ENV LEIN_ROOT=1
# Mon, 07 Nov 2022 21:01:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 18 Nov 2022 22:39:46 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:39:46 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:40:30 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Fri, 18 Nov 2022 22:40:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:40:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:40:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:40:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8d9c230ad7b20621780183623ce76b7c296e1db90d16a51deeb03f19e2493c`  
		Last Modified: Wed, 02 Nov 2022 19:49:51 GMT  
		Size: 18.4 MB (18416178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dffb0eed171df96cdf9e8acf538509a060d226f8e86ce3b14dfd038e0247743`  
		Last Modified: Mon, 07 Nov 2022 20:43:54 GMT  
		Size: 191.2 MB (191223767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77de63931da811d115434e3cc8d1ffb9ddee625266b56b54e6b987accafb3667`  
		Last Modified: Mon, 07 Nov 2022 20:43:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c13dd1f98bd8e9b4c3f8198a5736af1b5fbf0eeac9437a396193891ad64d8a`  
		Last Modified: Mon, 07 Nov 2022 21:10:43 GMT  
		Size: 338.7 KB (338677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be5742a516c33a090a5ac54023c29176d1150d0ac2b6967af2c40fcae96d9be`  
		Last Modified: Mon, 07 Nov 2022 21:10:46 GMT  
		Size: 58.8 MB (58820376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a590a77051b7be414349cb0f4909d5df6ea031a744ae4ffae74615a55fb6534`  
		Last Modified: Mon, 07 Nov 2022 21:10:42 GMT  
		Size: 12.4 MB (12379091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494a4de69c5385980231c52ab89cee086d831d826e3c7d15143fd8ac1ff76932`  
		Last Modified: Mon, 07 Nov 2022 21:10:41 GMT  
		Size: 4.4 MB (4398836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e07d0a3ea38fc45003333baa76b3dc1e3255391a166fc1435f3bd44c0ae8d71`  
		Last Modified: Fri, 18 Nov 2022 22:49:22 GMT  
		Size: 49.9 MB (49936027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dd28f1e457be109423a0599d3283003c905801be5bdfa4bd196a89c6a9bc5b`  
		Last Modified: Fri, 18 Nov 2022 22:49:17 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2716b5bda55fa6997010bcc583c6cb42bc51f0515f6867579e51fe559dae99d`  
		Last Modified: Fri, 18 Nov 2022 22:49:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
