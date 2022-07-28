## `clojure:temurin-17-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:6a8a59d62fed2850fcb566e1ec7bd1f48a087ede2551874e050407c78737b327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:0d64af2c2b7f3ebf038d4a2fad7cce34a2df2806def2b6643b34f031f36ee06c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265979033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54111fa92e9c74a5f579d0baa7639a38e055a5455fe4ce0f81aaeccdd8b7b22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 28 Jul 2022 16:20:06 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 28 Jul 2022 16:21:48 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:22:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b356512c955f2d1a66b714ab3acaad942d04f80603af7dcd56e1fe5baeaeeda';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:22:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:22:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:03 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 16:53:49 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Jul 2022 16:53:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Jul 2022 16:53:49 GMT
WORKDIR /tmp
# Thu, 28 Jul 2022 16:53:50 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 28 Jul 2022 16:53:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Jul 2022 16:53:50 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Jul 2022 16:54:09 GMT
RUN boot
# Thu, 28 Jul 2022 16:54:09 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Jul 2022 16:54:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Jul 2022 16:54:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2b3b9d0d1a1f972083dde62c850175d26be845971e3c96ff06c8145fbe2fd0`  
		Last Modified: Thu, 28 Jul 2022 16:25:19 GMT  
		Size: 12.1 MB (12050034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2397a8b45ddb9c256e8fa59ff97584ab50a52eea32e237524684a89d415988`  
		Last Modified: Thu, 28 Jul 2022 16:28:24 GMT  
		Size: 191.4 MB (191449900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c65d315368a0cef1d8a17608679846de0f266f1e373c0a519b2924983587380`  
		Last Modified: Thu, 28 Jul 2022 16:28:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9001cefba7f1cf5e8dce13b6aa36da60a1b6d01bf707b41e6997d870e93afbc7`  
		Last Modified: Thu, 28 Jul 2022 17:01:05 GMT  
		Size: 859.3 KB (859318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79d1b5531b68d738526de3af7568281392885694ed694c04c63c11a114c7d28`  
		Last Modified: Thu, 28 Jul 2022 17:01:08 GMT  
		Size: 58.8 MB (58820412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81777230e04c4a4a4f407676449a0a4bed78e36bd66aae8d6fa0ef68871ddbe`  
		Last Modified: Thu, 28 Jul 2022 17:01:05 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
