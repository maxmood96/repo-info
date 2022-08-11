## `clojure:temurin-17-tools-deps-1.11.1.1149-alpine`

```console
$ docker pull clojure@sha256:77531cfb81a0ec709b046505315937f16298220293520ae1adeee6589610082a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-tools-deps-1.11.1.1149-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:a85d37794fd8eed8337734d8286a87cd494596bc9d101ab7bab45dae1e3bae94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236170533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80f0f8941e47ad85b11af781bca8c3df7997a63a9c6248f21eebac4ab880c96`
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
# Thu, 11 Aug 2022 19:23:40 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 11 Aug 2022 19:24:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b356512c955f2d1a66b714ab3acaad942d04f80603af7dcd56e1fe5baeaeeda';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 11 Aug 2022 19:24:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:24:07 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:10:54 GMT
ENV CLOJURE_VERSION=1.11.1.1149
# Thu, 11 Aug 2022 20:10:54 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:11:00 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "9aadc1a1840a458517a6efb111eba72be93c17bbdc874c833ef781e77aacc55e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 11 Aug 2022 20:11:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Aug 2022 20:11:00 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:11:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:11:00 GMT
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
	-	`sha256:cdeb5c36e3987cc21fc57eda9f965b006f42903399b536e06aef37ff462fb27e`  
		Last Modified: Thu, 11 Aug 2022 19:35:23 GMT  
		Size: 191.4 MB (191449939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32867cbcebbe8d6d561e769be3ba911e76008280e8de56032b16a7b21538e5ba`  
		Last Modified: Thu, 11 Aug 2022 19:35:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612b0e8218472e279d28e8d47f87a0cf9342468679336508bae196445bee1f6c`  
		Last Modified: Thu, 11 Aug 2022 20:22:43 GMT  
		Size: 29.9 MB (29863262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b07111f19110ea97e0bba1f9f60aa00ad0a447fc2352e1aa8b1497962e8a47`  
		Last Modified: Thu, 11 Aug 2022 20:22:41 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3840d5a54fddce6c928479849f1789bfce846e62497ebcd2ac8d41af3b7d9149`  
		Last Modified: Thu, 11 Aug 2022 20:22:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
