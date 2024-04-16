## `clojure:temurin-22-lein-2.11.2-jammy`

```console
$ docker pull clojure@sha256:c7de2c36f917c03b625df0a72bd9fd6392ea35bf1283dbac47baa2f0d42e04ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-lein-2.11.2-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:ee97e3b6a28860bc16bf05e4aa1cc9c59f70d2938f8e1d34289aad2cf2492fc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223528406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f670f4174a9b7da457df9b12e2a7c146841ac3f741ebb61abd407699403e6f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4b52670caea44848cee893e35c804380817b6eff166cf64ee70ca2bfaac3d1c7';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc3d99e816d0c373f424cd7aa2b6d3e8081a7189fe55c1561616922200ec8e47';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c062e934d95c639f97b4e51b968eed694a6653248727c3db8bc5e0e55cfd7f4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
CMD ["jshell"]
# Wed, 10 Apr 2024 20:36:01 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 10 Apr 2024 20:36:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 20:36:01 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 20:36:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 10 Apr 2024 20:36:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 20:36:25 GMT
ENV LEIN_ROOT=1
# Wed, 10 Apr 2024 20:36:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 10 Apr 2024 20:36:28 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 20:36:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 20:36:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e531083e1b0a15cdfac26d85cd8a10953cf6e70ef3798ed13a8457344f2c87f`  
		Last Modified: Thu, 28 Mar 2024 02:13:42 GMT  
		Size: 16.3 MB (16337175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34e2093c50752190bab37a96ab0af869b84a8714e622349658adf61bddee95a`  
		Last Modified: Thu, 28 Mar 2024 02:13:52 GMT  
		Size: 157.9 MB (157881913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b36755bec6f1cea87895a91d5c638c7e0f2aa7b78f0f866b30ff5c50886159`  
		Last Modified: Thu, 28 Mar 2024 02:13:40 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d7b39df2027f8c1ade8a458cf1f2d5926a841b79715789ce75737f160b950a`  
		Last Modified: Thu, 28 Mar 2024 02:13:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c79717a9cf6c2181354caac822d97cb5fdc906e5d118eedaa797aa5da92a1b4`  
		Last Modified: Wed, 10 Apr 2024 20:51:42 GMT  
		Size: 14.5 MB (14457579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a1b542f88409cff1376c673ec175b19fac8e70bfdca5beb6c791502d49a858`  
		Last Modified: Wed, 10 Apr 2024 20:51:42 GMT  
		Size: 4.4 MB (4399155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2abd7fd686cb40b5a9303e628ff0c7589f2b36698766f8d23e824c5c50a4e54`  
		Last Modified: Wed, 10 Apr 2024 20:51:41 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-lein-2.11.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9dffe81f5feb6f5236fbb3bcb01399827829585a7a35c50b2c4a78b008f1fceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220881048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113b5d97abd6dc2260e726c81e50bf4f9feca5542704975f8258e1edd0b77b0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4b52670caea44848cee893e35c804380817b6eff166cf64ee70ca2bfaac3d1c7';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc3d99e816d0c373f424cd7aa2b6d3e8081a7189fe55c1561616922200ec8e47';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c062e934d95c639f97b4e51b968eed694a6653248727c3db8bc5e0e55cfd7f4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
CMD ["jshell"]
# Tue, 16 Apr 2024 06:47:43 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 16 Apr 2024 06:47:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:47:43 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:47:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 16 Apr 2024 06:47:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:47:57 GMT
ENV LEIN_ROOT=1
# Tue, 16 Apr 2024 06:47:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 16 Apr 2024 06:47:59 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:47:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:47:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ed6356befcb3f3e3f2dbe4ed0457e6f2e017191ad3f4f999da71660803fb42`  
		Last Modified: Tue, 16 Apr 2024 02:59:21 GMT  
		Size: 17.8 MB (17753415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d67b61cf32e2270130b73c2a006e1b0750e3a77ea9613844583a8400ff9f6`  
		Last Modified: Tue, 16 Apr 2024 02:59:29 GMT  
		Size: 155.9 MB (155868249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65dc80542294dec55abc165ea565444bb81164a7332ef94ed22b1857b7da32e8`  
		Last Modified: Tue, 16 Apr 2024 02:59:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa6cf93078a2fbfea07d632c3cc6b201cc6ee1113991699f63538522b562ebf`  
		Last Modified: Tue, 16 Apr 2024 02:59:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa575294240413b4e032cfb005fc39ba8c8f05503e4d6e0c04f2e6dd1725521`  
		Last Modified: Tue, 16 Apr 2024 07:01:42 GMT  
		Size: 14.5 MB (14458648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd12e5659ff4fde6fc0524f84b4103be7e16fb3b08fdcf82defa27fedfc12a`  
		Last Modified: Tue, 16 Apr 2024 07:01:42 GMT  
		Size: 4.4 MB (4399160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3af5592697202ebd0a96cbd5bb0cb6fbe771554f96e04225128a7ba1983c330`  
		Last Modified: Tue, 16 Apr 2024 07:01:41 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
