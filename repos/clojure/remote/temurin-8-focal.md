## `clojure:temurin-8-focal`

```console
$ docker pull clojure@sha256:a328386c81b966f41fc15f70f3929505a853c1194979f523afd1f88aaac59dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-focal` - linux; amd64

```console
$ docker pull clojure@sha256:9c3d9ba2d097036216ad360a3a689d73d65fb8576c3cde0e53bc926c61640a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211468731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed35935e5e54a09ceb48ffb6189e57a737c1d7652dde02dfb43da2b7ebbe4d83`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:27:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 17:27:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 17:27:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 17:27:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:19:59 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:06 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:10:28 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Sat, 05 Nov 2022 01:10:29 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:10:49 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Sat, 05 Nov 2022 01:10:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 05 Nov 2022 01:10:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1869246ce33b7e9d4cfc0f2be772ef684e2425767400664f548b81c2a69eb`  
		Last Modified: Tue, 25 Oct 2022 17:33:48 GMT  
		Size: 16.4 MB (16353656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f80a1a0fab2544d040bfad097e957b495735264717b873ffc8702479c344da`  
		Last Modified: Fri, 04 Nov 2022 23:25:14 GMT  
		Size: 103.5 MB (103530792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474407bf19afc18eb4e902eab43ac082c4e6590966c2de3d6d0cdc74aa8534d6`  
		Last Modified: Fri, 04 Nov 2022 23:25:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b66c0705e2b2db96867c9ea0072daa8a31fd5314e2411621c1e3136f91fe2a`  
		Last Modified: Sat, 05 Nov 2022 01:24:53 GMT  
		Size: 63.0 MB (63005671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb94702d1cbcb76f1fc902b8d65e8f1003dc4bd1f87ccdfbc4ca793e224aca`  
		Last Modified: Sat, 05 Nov 2022 01:24:45 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:11fa5f740fb6ef1e790dba4ee46a975c92abe3a62a29c07cbe380bfb9c5cba68
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209164593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50bd3f3ed867391e016dfd29bcffcf042edf0b26948325806a4f2aca19e8b6a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:07:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 01:07:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 01:07:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Oct 2022 01:08:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:38 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:39:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:39:46 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 04 Nov 2022 23:11:21 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Fri, 04 Nov 2022 23:11:21 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:11:42 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Fri, 04 Nov 2022 23:11:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 04 Nov 2022 23:11:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b9bffe95bbbebdbdfba5c69142aeb65478735d04064fd29982a5b9c980559e`  
		Last Modified: Wed, 26 Oct 2022 01:16:15 GMT  
		Size: 16.2 MB (16216007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d22354a80d2d12ffad6f61953c73519c4d3e501897b672ceaa720a21ca9533`  
		Last Modified: Fri, 04 Nov 2022 22:43:42 GMT  
		Size: 102.6 MB (102630792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd3de5d3cf89d4eb535267ba80576b5c8b40771b2b9213e5a423086faf1b916`  
		Last Modified: Fri, 04 Nov 2022 22:43:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481a3f188ce30f718d3c0c6f721e1d353f2001bf7136ef08e380ae238005545`  
		Last Modified: Fri, 04 Nov 2022 23:22:27 GMT  
		Size: 63.1 MB (63121018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986bbb0c0abb9f9cf26239b94946bd1de1ebe432086e5de93aff6309fb49593f`  
		Last Modified: Fri, 04 Nov 2022 23:22:20 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
