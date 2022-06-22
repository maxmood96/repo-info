## `clojure:temurin-17-boot-alpine`

```console
$ docker pull clojure@sha256:98607f386dd6d2fd048aa2c6dc4c2307e410e9ad0cc49146cd24077863f6c903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:6dbb49e7ed374356806e587d68364aec28451aaa7a3e9306b675e7566d52465d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254757204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88814d997fe6239db6eab5924bae284ab7a026c2afbf8e23f23f5766ab250bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Tue, 21 Jun 2022 20:45:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Jun 2022 20:45:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Jun 2022 20:45:58 GMT
WORKDIR /tmp
# Tue, 21 Jun 2022 20:46:00 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Tue, 21 Jun 2022 20:46:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Jun 2022 20:46:00 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Jun 2022 20:46:25 GMT
RUN boot
# Tue, 21 Jun 2022 20:46:25 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Jun 2022 20:46:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Jun 2022 20:46:25 GMT
CMD ["repl"]
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
	-	`sha256:e6792ecb99e858a080a618a330553ef34dd810d90507d4d249d438b1ac0f3b9e`  
		Last Modified: Tue, 21 Jun 2022 20:49:49 GMT  
		Size: 850.3 KB (850300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7246587a92a9ef404358609a46b3dc5fed2ede8702b5cc073bc5703db18778`  
		Last Modified: Tue, 21 Jun 2022 20:49:53 GMT  
		Size: 58.8 MB (58820503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c47915347f4440a062a42d1a1925501cd135383498fe7b53a43a1e88f7693f`  
		Last Modified: Tue, 21 Jun 2022 20:49:49 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
