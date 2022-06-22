## `clojure:temurin-17-alpine`

```console
$ docker pull clojure@sha256:ea885e30c6fa223e5073c65e6b9a4413a62a809cd65597daf5a9a6635659d401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:227957540ae716b63e2aff8fbfaccde01f62d52a89be06a3f460adc990f45b1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225328022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9b5d5a89affc9815c8e4cc34c04d44b10ac6e61e9f04f647b0efd5219a6e48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Tue, 21 Jun 2022 20:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jun 2022 20:21:36 GMT
RUN apk add --no-cache libretls musl-locales musl-locales-lang tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 21 Jun 2022 20:22:54 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 21 Jun 2022 20:23:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5cbaece6aec44f6d3911cfa3c5a8659889e85042aff214c944c5fa1b5938a5fc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 21 Jun 2022 20:23:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jun 2022 20:23:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 21 Jun 2022 20:23:19 GMT
CMD ["jshell"]
# Tue, 21 Jun 2022 23:25:46 GMT
ENV CLOJURE_VERSION=1.11.1.1139
# Tue, 21 Jun 2022 23:25:46 GMT
WORKDIR /tmp
# Tue, 21 Jun 2022 23:25:51 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2ba0de34f122f26580e3e6337bd04c8e3f9f648299367b17da85f00d930e191c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Tue, 21 Jun 2022 23:25:51 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 21 Jun 2022 23:25:51 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 21 Jun 2022 23:25:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Jun 2022 23:25:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4177d2591259bff2bae6f43f12721dbe4ed5aac24fb0991377a3d27cdd534e`  
		Last Modified: Tue, 21 Jun 2022 20:26:07 GMT  
		Size: 477.8 KB (477755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192e69d5289dec2e5bbf3ed1456166acafdc67b3e657981604fa21df9ae64084`  
		Last Modified: Tue, 21 Jun 2022 20:27:54 GMT  
		Size: 191.8 MB (191809195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbdc495bee83415cd6c7ddec5b7a12d388962b684278496d8d5798a5a13cd90`  
		Last Modified: Tue, 21 Jun 2022 20:27:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89071dfeb7c0e5aa5d68d89f975a8bfabe6486e94180e353008026d844840980`  
		Last Modified: Tue, 21 Jun 2022 23:31:31 GMT  
		Size: 30.2 MB (30241000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54164048453820f1390880424e97874436491fad325f5a9a892897f9534c8b57`  
		Last Modified: Tue, 21 Jun 2022 23:31:29 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eebe28787ba47079e159337561f9a52b5b09baa141e5fe7bef5ed84ec1a16ec`  
		Last Modified: Tue, 21 Jun 2022 23:31:29 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
