## `clojure:temurin-19-boot-2.8.3`

```console
$ docker pull clojure@sha256:be1523db37745dd4d45d8ab0d879a1419c3bd770b7b84d9f70b72ff231b7041e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:831557350bd598674f68cb66165dc1b32cf987d46c0f103ace8ba58f7e7de8e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307424273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7045bda0f1f4d118f5eee28c1e45c23039dd9cc540f5b11f6829c56fda7656c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:22:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:22:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:22:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:24:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Sep 2022 23:21:50 GMT
ENV JAVA_VERSION=jdk-19+36
# Mon, 26 Sep 2022 23:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 26 Sep 2022 23:22:02 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 26 Sep 2022 23:22:02 GMT
CMD ["jshell"]
# Wed, 28 Sep 2022 00:26:37 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 28 Sep 2022 00:26:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 28 Sep 2022 00:26:37 GMT
WORKDIR /tmp
# Wed, 28 Sep 2022 00:26:44 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 28 Sep 2022 00:26:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 28 Sep 2022 00:26:44 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 28 Sep 2022 00:27:03 GMT
RUN boot
# Wed, 28 Sep 2022 00:27:03 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 28 Sep 2022 00:27:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Sep 2022 00:27:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a58ffb4a943ab9205ec8ee456a88a4993ebcd34fca832aa0c3b0162cd79480`  
		Last Modified: Fri, 02 Sep 2022 05:31:23 GMT  
		Size: 17.0 MB (16985308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9288cdbe335dc986486829cc8cbd3db06a7bf652000b02b7772e01a9d73189bd`  
		Last Modified: Mon, 26 Sep 2022 23:26:10 GMT  
		Size: 200.9 MB (200852996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538d26d7dd051dbf793b88903361556aadd8d9cf490e0f7bec91aea8442cb457`  
		Last Modified: Mon, 26 Sep 2022 23:25:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e8243850c6c4714aa4ced5d1d06752a81b8dc7090880fa2add4d9dea06f180`  
		Last Modified: Wed, 28 Sep 2022 00:32:32 GMT  
		Size: 338.1 KB (338142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c86d85b7ee5fb2cc026028d6befefc5b4614ed7de2d9112ddeec93c48b3438e`  
		Last Modified: Wed, 28 Sep 2022 00:32:35 GMT  
		Size: 58.8 MB (58820544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c679ecb77f535acb173dfab44128a1ad2711266f125f71dc8514e89078521c96`  
		Last Modified: Wed, 28 Sep 2022 00:32:31 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5dd372289aeac3b34f233ea3c9d5357fd358b98e7a68ef764099d0be4b25403c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305306749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa3b627a47e36b6b36d8f6bd2eaed6293bb4381cde015e29253d3b1624953a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:51 GMT
ADD file:550e7da19f5f7cef52c6ea160a33daa482f44df086ddecffca8ec9be6385b848 in / 
# Fri, 02 Sep 2022 00:57:52 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:56:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:56:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:56:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:59:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Sep 2022 22:41:42 GMT
ENV JAVA_VERSION=jdk-19+36
# Mon, 26 Sep 2022 22:41:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 26 Sep 2022 22:41:54 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 26 Sep 2022 22:41:54 GMT
CMD ["jshell"]
# Wed, 28 Sep 2022 01:05:42 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 28 Sep 2022 01:05:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 28 Sep 2022 01:05:44 GMT
WORKDIR /tmp
# Wed, 28 Sep 2022 01:05:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 28 Sep 2022 01:05:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 28 Sep 2022 01:05:53 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 28 Sep 2022 01:06:07 GMT
RUN boot
# Wed, 28 Sep 2022 01:06:08 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 28 Sep 2022 01:06:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Sep 2022 01:06:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00f50047d6061c27e70588a5aab89adada756e87d782a6c6bd08b4139eb8ea10`  
		Last Modified: Fri, 02 Sep 2022 00:59:40 GMT  
		Size: 28.4 MB (28381340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948ed504bea9f0b27111de5ca0d2086e160f6df8abc460af1a3b7be67def00da`  
		Last Modified: Fri, 02 Sep 2022 05:07:45 GMT  
		Size: 18.4 MB (18417910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578484c9a43c46eac749c95bb8855e0d01ef3ac008beb00f0fc6ffa051224e5d`  
		Last Modified: Mon, 26 Sep 2022 22:46:33 GMT  
		Size: 199.6 MB (199590012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bdd93173fe621f1969015666efeb6a5fe4575fea1c2ea4d0d04d055921d8a8`  
		Last Modified: Mon, 26 Sep 2022 22:46:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913f2cc8012facfc733f597779d2e3730833a1f8af91d9a4175ebc8b071b8555`  
		Last Modified: Wed, 28 Sep 2022 01:12:26 GMT  
		Size: 101.0 KB (100994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99e2ebbc2a37e45ea6f4f799163ef3c4e3280378f7297d68b9fbaf598496f7f`  
		Last Modified: Wed, 28 Sep 2022 01:12:30 GMT  
		Size: 58.8 MB (58815933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5abd6d3c18781582e992185470148ce755e69eb8918f2600d9b0fe614501bd`  
		Last Modified: Wed, 28 Sep 2022 01:12:26 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
