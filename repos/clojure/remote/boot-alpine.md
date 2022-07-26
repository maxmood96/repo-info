## `clojure:boot-alpine`

```console
$ docker pull clojure@sha256:7a8a24d7da7e4ff6b25d9fa38b49e2883138aebf3e3826d01afaf4b48a395806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:63bc175767a6c30ccff0b9f0dee4380200593d11064dd93114aa2f83a34d298f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254757629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be762dbf2394483fd603cc551ce390751b6f09b66d42bc96f1aea75b224f705`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 18 Jul 2022 22:20:08 GMT
RUN apk add --no-cache libretls musl-locales musl-locales-lang tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 18 Jul 2022 22:21:30 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Mon, 18 Jul 2022 22:21:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5cbaece6aec44f6d3911cfa3c5a8659889e85042aff214c944c5fa1b5938a5fc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 18 Jul 2022 22:21:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 22:21:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 18 Jul 2022 22:21:48 GMT
CMD ["jshell"]
# Tue, 19 Jul 2022 03:28:36 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Jul 2022 03:28:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Jul 2022 03:28:36 GMT
WORKDIR /tmp
# Tue, 19 Jul 2022 03:28:38 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Tue, 19 Jul 2022 03:28:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Jul 2022 03:28:38 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Jul 2022 03:29:12 GMT
RUN boot
# Tue, 19 Jul 2022 03:29:12 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Jul 2022 03:29:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Jul 2022 03:29:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d31e16dc1b50d804a50e80381050a90d4dc55a110eae65cd1cef937d3dc18d3`  
		Last Modified: Mon, 18 Jul 2022 22:24:55 GMT  
		Size: 477.8 KB (477762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ea1633255a1557ec5be0901310988f2a60b65a3ee873350ac747fb18021645`  
		Last Modified: Mon, 18 Jul 2022 22:26:46 GMT  
		Size: 191.8 MB (191809263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976b645f054d012cff86ab7d955417b543a4db89fdb6c0f85d606fc7a22ed7f5`  
		Last Modified: Mon, 18 Jul 2022 22:26:30 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3d0946f3d051f2bdd6207b105ca45c2e4d007ea572e64e2d0c192d28e690`  
		Last Modified: Tue, 19 Jul 2022 03:32:40 GMT  
		Size: 850.3 KB (850310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193b9db0430bc168348db780c5d884aa3cd00b07d5153926a2c8fdcba6e686e5`  
		Last Modified: Tue, 19 Jul 2022 03:32:43 GMT  
		Size: 58.8 MB (58820926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f4397514a462b4a6091860fbf02c6e85ba7bf1f2b2931c761cc16d51b9df54`  
		Last Modified: Tue, 19 Jul 2022 03:32:40 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
