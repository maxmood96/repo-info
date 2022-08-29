## `clojure:temurin-18-tools-deps-1.11.1.1155-alpine`

```console
$ docker pull clojure@sha256:d54c094ad4b738c90750edfed4eff92b8957de92a4bdca160f2995b5ff895027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-tools-deps-1.11.1.1155-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:3cca5e234f56d0f2e5959273e941c806cdae489327156e965a22886183968410
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237854194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cf9aa733b43f19c77a29de7c64e66f5f15f68b10bbf727837fdb109437d0c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 19:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 19:19:40 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 29 Aug 2022 18:27:26 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Mon, 29 Aug 2022 18:27:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='478c8f56dec7378ed8c687e8d7d0fbf729973c62c497cfc8cf58bd621849d764';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 29 Aug 2022 18:27:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Aug 2022 18:27:45 GMT
CMD ["jshell"]
# Mon, 29 Aug 2022 18:55:33 GMT
ENV CLOJURE_VERSION=1.11.1.1155
# Mon, 29 Aug 2022 18:55:34 GMT
WORKDIR /tmp
# Mon, 29 Aug 2022 18:55:39 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7eb9aa2ecc6c0abfdb1578d4b99ca7c2055111aafa38524a12a6fb76fe01f30b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Mon, 29 Aug 2022 18:55:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 29 Aug 2022 18:55:39 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 29 Aug 2022 18:55:39 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 29 Aug 2022 18:55:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107abfa4a9656cc98051eebaf02de090526191f4d53ab3733605b34f84513224`  
		Last Modified: Thu, 11 Aug 2022 19:29:52 GMT  
		Size: 12.1 MB (12050073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740e3cdadfebcaafba907a9fba5363e7b2da3e4636a0340e58c190daa0667e08`  
		Last Modified: Mon, 29 Aug 2022 18:31:41 GMT  
		Size: 192.9 MB (192911706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71f0ae6ae71d4a6dd24382195739038e7f96208259eb6100971cd8eed81943a`  
		Last Modified: Mon, 29 Aug 2022 18:31:26 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f1f0e31ba155766203d394f0049c05292c35db89e5d403e44c64e45704e54d`  
		Last Modified: Mon, 29 Aug 2022 19:00:57 GMT  
		Size: 30.1 MB (30085151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e3bf61560e3c9535f55a94c4700056666cd29904c064939f6ae75bf31948d0`  
		Last Modified: Mon, 29 Aug 2022 19:00:55 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b3c72f06056366f5da481e301a6a32b3412eb1dbffd0af9b13d9268b30e3a7`  
		Last Modified: Mon, 29 Aug 2022 19:00:55 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
