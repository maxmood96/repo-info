## `clojure:temurin-8-tools-deps-1.11.1.1149-alpine`

```console
$ docker pull clojure@sha256:7111f472a5f22db98196ea33e4a23e9b76758ee0006c47662b871f75c0fbe814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-tools-deps-1.11.1.1149-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:14e817bf9cd923072a8db34648baf94ad2974a6c6619474b46f3a22d79ef8a78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146156757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab995ae7e528c04dfcffa9b7f8bbe5782a78ea12069259a429cd52642755383`
-	Default Command: `["clj"]`

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
# Thu, 11 Aug 2022 19:19:40 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Thu, 11 Aug 2022 19:19:49 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e5dcb8f947b687597f92fa80c008a2a17ce86f739dd6dce7ca741921621acb21';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 11 Aug 2022 19:19:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 11 Aug 2022 20:03:53 GMT
ENV CLOJURE_VERSION=1.11.1.1149
# Thu, 11 Aug 2022 20:03:54 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:03:59 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "9aadc1a1840a458517a6efb111eba72be93c17bbdc874c833ef781e77aacc55e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 11 Aug 2022 20:03:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Aug 2022 20:03:59 GMT
CMD ["clj"]
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
	-	`sha256:0785c5e3ab89a9dfa7638fd78c1fc211af4fab5cc276025f6f0bd09e13f0581c`  
		Last Modified: Thu, 11 Aug 2022 19:29:59 GMT  
		Size: 101.4 MB (101436564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758050903e3eb20e7b6f221721deaa4ec312c37440aec34aa44fdf73788659b0`  
		Last Modified: Thu, 11 Aug 2022 19:29:50 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7ac062c3ded32736f547b74327914462a8401769d639861ea35eccfe5de71`  
		Last Modified: Thu, 11 Aug 2022 20:18:55 GMT  
		Size: 29.9 MB (29863285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab979a69537a07d82bcdc054e78898f422782b4d377ae0860b4151586639229f`  
		Last Modified: Thu, 11 Aug 2022 20:18:52 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
