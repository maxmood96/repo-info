## `clojure:temurin-22-noble`

```console
$ docker pull clojure@sha256:f6126076742927fd878903aa41ce37a83f7a1614fef676795017f21c5d750134
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-noble` - linux; amd64

```console
$ docker pull clojure@sha256:7bf3c8035c79b82297c4f62844d1ed0d8b2a86f94e8526645165889fd1d34842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262686279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acaf61eaf6f7c056171da8bcdef93d2e23b4cf47113e7f881c7a902cc3644c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
CMD ["jshell"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a476ddaf8f2380122935e7fa2924236f31f3ecd947aac602c3f934f04c2c3f68`  
		Last Modified: Sat, 17 Aug 2024 01:15:27 GMT  
		Size: 17.8 MB (17831031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff749a8ed96d1c97779149221d24843dd54b0909ad54baa41392f5b20d96eda`  
		Last Modified: Sat, 17 Aug 2024 01:15:37 GMT  
		Size: 156.5 MB (156487288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578dad01d9c015abf8ecf1bb1cb395d8ec15cdfbcf75bbb01ecf95db65195fea`  
		Last Modified: Sat, 17 Aug 2024 01:15:25 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabd2051722b74d9fd44361c50e72a2173dd15eb3c69a73005fe95d120effd0e`  
		Last Modified: Sat, 17 Aug 2024 01:15:25 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9728cc626f8cfb1b8aca6bf138f8cc507fbbb7de1521374104d31cad6fb89430`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 57.8 MB (57797598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d4b7e2e5d55c3816f8b5b15492b616e74610ec4017fcca7b87cdc8da2d3a4`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff613f39aaba7bf087fe4984950a53add1082bd6600b28cc436e9c88f0cc34ff`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:6c86d30ebd7e23e5495eb1777f57141f62b8316e29dea931f1581021662d1c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5442716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956383ddf8d1cb096f25a00395b6a9158a01587c7de0adab8da374ce2127f5eb`

```dockerfile
```

-	Layers:
	-	`sha256:d512d54d7f7dd75e1b13cb4a5f91f66d1875731715b89b03f0096426d2a888f2`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 5.4 MB (5427187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d776dc025fafedd68db55b2a639e594a1a8e93464d924597d5c5df55c85f24cc`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:43cc7f45abb27cbc546951892cd706f9929477715879d07ad87d790d279065c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261211650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb6a15edb2f5d810a74de5140887e33dddeeab3882fbe0933e421cdf6c268fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
CMD ["jshell"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28befbd61f65e6d4a7600a1f972a34ae124464ea3d7cc74d246731c78428af9c`  
		Last Modified: Wed, 24 Jul 2024 00:53:19 GMT  
		Size: 19.0 MB (19004558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dde306a13d0338916b20c00ca274708e1b46c4e845def7dc40cd19870b0e45`  
		Last Modified: Wed, 24 Jul 2024 00:53:27 GMT  
		Size: 154.5 MB (154501089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ab4612f3b874bcb0bbc7ffe36db11705d68e4456158147aa34eeff8d1f4e5a`  
		Last Modified: Wed, 24 Jul 2024 00:53:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff8792953874cde357fe8576e9ceff93696b846c8851fc1ef69cf6d53255421`  
		Last Modified: Thu, 25 Jul 2024 17:48:28 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8ecbb7e5e5c1ef6d6e8309ad3ee9f4d07d55c8ebed878724dd2abf320462b5`  
		Last Modified: Wed, 07 Aug 2024 20:21:24 GMT  
		Size: 57.8 MB (57794971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca04a9c506d3c1794b3813d2b98010bd5ae71850b13bcc97094db6009f937c0`  
		Last Modified: Wed, 07 Aug 2024 20:21:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6dfeb44e981f492d8f8da0eed1852f31f4cfeffe8b3cf191f19d027e09e113`  
		Last Modified: Wed, 07 Aug 2024 20:21:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:fe9ea32d648865872221e951ad39fb410be652d99bfd22b4556c1d3e43be4009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5581404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00a395b992ff4b08878a732354d90c19cd12940b0d3967c14b1189cd6b4b197`

```dockerfile
```

-	Layers:
	-	`sha256:94e3b967808f836ab8f839c977acf0bed2d07760ecc4acf89ced0741c81e9073`  
		Last Modified: Wed, 07 Aug 2024 20:21:22 GMT  
		Size: 5.6 MB (5565569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209019b1bb3e61d705bdb201e68f9ef123b648efd6f86f0659cef2a0e407f240`  
		Last Modified: Wed, 07 Aug 2024 20:21:22 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
