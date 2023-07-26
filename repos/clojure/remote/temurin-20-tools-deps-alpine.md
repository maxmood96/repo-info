## `clojure:temurin-20-tools-deps-alpine`

```console
$ docker pull clojure@sha256:0e85c7c6a552ee7df3fa3a6006018942fac862507667f25a12b1618535370c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-20-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:27c9be6808eef859def5296c589bbeae7d3fbd54c823660ca60dc6621604a96e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192017311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4a89acd93e492039d0b3621f25386ad2f2d276e6c11c3e2564f45bdb59f397`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jun 2023 05:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:11:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jun 2023 05:11:54 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 26 Jul 2023 00:55:11 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 26 Jul 2023 00:55:22 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b03aced4b7a1c49bc00297e35e45480fd03818862b93e17e1551a3b721e89306';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_alpine-linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 26 Jul 2023 00:55:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:55:24 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 02:47:12 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 26 Jul 2023 02:47:12 GMT
WORKDIR /tmp
# Wed, 26 Jul 2023 02:47:17 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Wed, 26 Jul 2023 02:47:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Jul 2023 02:47:17 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 26 Jul 2023 02:47:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Jul 2023 02:47:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aadc9aaa732ac5b0edd00545607971071fa1868047a65249e483ba2443982e6`  
		Last Modified: Thu, 15 Jun 2023 05:15:34 GMT  
		Size: 7.6 MB (7648372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b7e63bdaf06570d0b464338c3b8fc5b5fb410322a7bdbd3b3d39e4c7a6ef54`  
		Last Modified: Wed, 26 Jul 2023 01:00:51 GMT  
		Size: 152.9 MB (152930840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d6fd526a8eea2699c6cb34679b49ea094771b660204d9dbc657b9b417765e4`  
		Last Modified: Wed, 26 Jul 2023 01:00:39 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf67672326c39bb002bb6438c89e2d3aeb3bf000cec0f4d70acbd330659eed0`  
		Last Modified: Wed, 26 Jul 2023 02:52:54 GMT  
		Size: 28.0 MB (28039014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a0089ba4e5a0c92ce0d7fff10ca64b839fa6b53987504ef00d1c03e6c5b735`  
		Last Modified: Wed, 26 Jul 2023 02:52:52 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f219e809938760068620b3c45b08ce5df6e7cfdaacc84683fe37d8f5765fba2a`  
		Last Modified: Wed, 26 Jul 2023 02:52:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
