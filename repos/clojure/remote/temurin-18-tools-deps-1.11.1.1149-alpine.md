## `clojure:temurin-18-tools-deps-1.11.1.1149-alpine`

```console
$ docker pull clojure@sha256:35f81c5ef6a2eafa6794897d0fdf38c0234d306d6e8a16c2566ae4260c1201ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-tools-deps-1.11.1.1149-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:029fe4cafff2cf12373cd78dbb6c5af186029aed372446163b4ce1354facf914
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237618114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f4029852905cf3d485fadc1007aeb80a677ad3200d09799ee2f658fe3bcd55`
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
# Thu, 11 Aug 2022 19:26:26 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Thu, 11 Aug 2022 19:26:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='045670342a036fff98b2ee90279ed923dc8c92bebe6227a2a60f64ca84f4f7c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 11 Aug 2022 19:26:48 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:26:48 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:14:35 GMT
ENV CLOJURE_VERSION=1.11.1.1149
# Thu, 11 Aug 2022 20:14:35 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:14:40 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "9aadc1a1840a458517a6efb111eba72be93c17bbdc874c833ef781e77aacc55e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 11 Aug 2022 20:14:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Aug 2022 20:14:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:14:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:14:40 GMT
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
	-	`sha256:e679a78d83de61b5d0ed95e8ee0bdd2eaa0d7f7c320f381f9c5f66b63a3715f5`  
		Last Modified: Thu, 11 Aug 2022 19:38:17 GMT  
		Size: 192.9 MB (192897589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e0855aa0b135a5077a832ca2d50c73d5ea07687225d09966878018473d37aa`  
		Last Modified: Thu, 11 Aug 2022 19:38:03 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012b0f67bc477fdba18f310a895d724d5070485710626c0f091c130ab458bcc`  
		Last Modified: Thu, 11 Aug 2022 20:24:28 GMT  
		Size: 29.9 MB (29863195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07af4fe988a288bd27f74689cd902a2792fe8668ab21c64b645beab037d5d1b4`  
		Last Modified: Thu, 11 Aug 2022 20:24:26 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566c7f8be46aa9ae120d618c3eb8347bd0444b2171372bc18986123e3c8d038c`  
		Last Modified: Thu, 11 Aug 2022 20:24:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
