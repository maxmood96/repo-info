## `clojure:temurin-18-lein-focal`

```console
$ docker pull clojure@sha256:b38804ad45cb658eb660597162cc2bc148e422d87d6051e7063d2c44e8b6005e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-18-lein-focal` - linux; amd64

```console
$ docker pull clojure@sha256:02768e4e94adefc33f3e64c1d7c6ebc4ee96a47fe91c90a0905073c771639c03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254879050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71af992db2bdae824597b2ab913b85ac2702cf2b293399792364508f2e5ad2a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 19:19:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:19:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 19:24:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 19:26:54 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Thu, 11 Aug 2022 19:27:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f4aca720bfcea4df7f02b59de1f68648632070c492f210b9e41e69170ee5e48f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        armhf|arm)          ESUM='52ec0ddee9ff16397de2c9f614ff6b5464220bd5c3d705e8b89d28fd478feb60';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4262677f8b6054d26f1c0042ac47dfbaab6a18d7dc73fa807b15ee03cdcbdece';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d916cfa15552ae2ad2f2c96ebc72aaaea4c844af9842f5ca9724fcbbdc08d25c';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5e5dbf6f1308829528778e00631ec83e252d90fc444503091e71a66465e88941';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 19:27:12 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:27:12 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:14:01 GMT
ENV LEIN_VERSION=2.9.8
# Thu, 11 Aug 2022 20:14:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:14:02 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:14:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Aug 2022 20:14:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:14:13 GMT
ENV LEIN_ROOT=1
# Thu, 11 Aug 2022 20:14:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Aug 2022 20:14:16 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:14:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:14:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dd6b41e17bd3ada96d1c3dafaeca8e6ef810daf9822be394cbebf694c15561`  
		Last Modified: Thu, 11 Aug 2022 19:35:38 GMT  
		Size: 16.3 MB (16299780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1392d2793c8c587e314bc1e4cbecee611fbc3fa66154814efdaed3d86d80e94`  
		Last Modified: Thu, 11 Aug 2022 19:38:45 GMT  
		Size: 193.6 MB (193578827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece9e452506d41e98d84ea560c71f2ab6027362b327878ad56977c943dab1d78`  
		Last Modified: Thu, 11 Aug 2022 19:38:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7349a2e564ce71166626e27172f53baf55f8e945cf657f66fc4579efd655616e`  
		Last Modified: Thu, 11 Aug 2022 20:24:00 GMT  
		Size: 12.0 MB (12035381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9187dd5c1466db14826551a80f3dcfb12b5d635c8ed5cb32ad448e96b3c2a74`  
		Last Modified: Thu, 11 Aug 2022 20:23:59 GMT  
		Size: 4.4 MB (4391893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdb1e665f606636e3d8c8ec53fd5c1f4fb66ce93f9b42a24119f8d7e56ca48b`  
		Last Modified: Thu, 11 Aug 2022 20:23:59 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-18-lein-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ffae2375b746c73114db166131402d7f4a6df87ddae95ee7084791786de5d5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252820577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252dabddc63364892e9abc31fbfa404402a0bec66e664357cd5c14affd2c1bee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 18:44:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 18:47:12 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Thu, 11 Aug 2022 18:47:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f4aca720bfcea4df7f02b59de1f68648632070c492f210b9e41e69170ee5e48f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        armhf|arm)          ESUM='52ec0ddee9ff16397de2c9f614ff6b5464220bd5c3d705e8b89d28fd478feb60';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4262677f8b6054d26f1c0042ac47dfbaab6a18d7dc73fa807b15ee03cdcbdece';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d916cfa15552ae2ad2f2c96ebc72aaaea4c844af9842f5ca9724fcbbdc08d25c';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5e5dbf6f1308829528778e00631ec83e252d90fc444503091e71a66465e88941';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 18:47:28 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 18:47:29 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:00:59 GMT
ENV LEIN_VERSION=2.9.8
# Thu, 11 Aug 2022 20:00:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:01:00 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:01:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Aug 2022 20:01:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:01:15 GMT
ENV LEIN_ROOT=1
# Thu, 11 Aug 2022 20:01:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Aug 2022 20:01:20 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:01:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:01:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb7631a1ffbba0a5b60549c314d974241510989eeceaa9db55cdc489b0e2ae0`  
		Last Modified: Thu, 11 Aug 2022 18:56:54 GMT  
		Size: 17.0 MB (17006184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93463167319e95aad850cde591cc61d4a2407e07b63887eb338372072115d10`  
		Last Modified: Thu, 11 Aug 2022 18:59:45 GMT  
		Size: 192.4 MB (192431721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a63be3658a2d858a10b5e46bb0dc9a623da2f592994ecde47c0f0f1e369b1af`  
		Last Modified: Thu, 11 Aug 2022 18:59:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42062750cb2ba1143831974d2c372f80e682ba5d08f76f741b8f8bda5ed7142f`  
		Last Modified: Thu, 11 Aug 2022 20:10:39 GMT  
		Size: 11.8 MB (11798490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8feddc8ac52f35e3a3ec7cd1addfb335aec69282181ad5a368683df8d608b5aa`  
		Last Modified: Thu, 11 Aug 2022 20:10:38 GMT  
		Size: 4.4 MB (4391818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d57f04330f89c21c159e874fd1f5e6888b0f4809c261c77528a97c35abdd6e5`  
		Last Modified: Thu, 11 Aug 2022 20:10:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
