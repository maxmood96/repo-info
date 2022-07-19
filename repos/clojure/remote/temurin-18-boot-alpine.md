## `clojure:temurin-18-boot-alpine`

```console
$ docker pull clojure@sha256:efeed62a87d1b24ffbe06efc7563239a01f8e0ce6f91896ab5fda462652d9649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:ef98b4effb8427b4bd56cca589e80364d979aa8696dc35d25394e453fa8ae150
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255810419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2f1b95f8b256ff2dc8c420ee651289b7a61022be5328d5ec5e8ea5bcd4e9a`
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
# Mon, 18 Jul 2022 22:22:12 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Mon, 18 Jul 2022 22:22:51 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ab72b28e1ce896e6b11e2b362c12c36007ebe9963d8954bc11e637be1f024dfe';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 18 Jul 2022 22:22:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 22:22:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 18 Jul 2022 22:22:53 GMT
CMD ["jshell"]
# Tue, 19 Jul 2022 03:29:44 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Jul 2022 03:29:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Jul 2022 03:29:44 GMT
WORKDIR /tmp
# Tue, 19 Jul 2022 03:29:46 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Tue, 19 Jul 2022 03:29:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Jul 2022 03:29:46 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Jul 2022 03:30:06 GMT
RUN boot
# Tue, 19 Jul 2022 03:30:06 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Jul 2022 03:30:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Jul 2022 03:30:07 GMT
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
	-	`sha256:1692a66f228637064c28c12822caa558cc227d8c55be05dcd9c13f23afe1c3f6`  
		Last Modified: Mon, 18 Jul 2022 22:27:37 GMT  
		Size: 192.9 MB (192862448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae49683e5b028ebf7144f182d99885f81d7393f9ff9fe771a3b2a84e652cc1a4`  
		Last Modified: Mon, 18 Jul 2022 22:27:22 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcee0ffaac86f05262e59a3e706a65e93cdc77f534cbdddeb9ed78e87424680d`  
		Last Modified: Tue, 19 Jul 2022 03:33:33 GMT  
		Size: 850.3 KB (850313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a988d816f16294cc0e796d43b470e044392fee541219dceb4e40e3799a67f3a7`  
		Last Modified: Tue, 19 Jul 2022 03:33:37 GMT  
		Size: 58.8 MB (58820529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2df435e6c22808f19d7f0c5ba52646bb93534acc5e6234bdc80a8844f3f4b`  
		Last Modified: Tue, 19 Jul 2022 03:33:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
