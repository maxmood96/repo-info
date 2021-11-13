## `clojure:openjdk-18-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:9d092db166a4e2ba7c146ee0b79c6d1c446c5143468c922d3b35ec1eb83da9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-18-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:af53c461a1dbce2da47a1a581d9b5630369f3ab8644fc859857fc8ae19862895
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252101058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41ac530b24e544f5183605f8de041dfe3130dda8902bcaaf09f999e0b98ad1c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:32:26 GMT
RUN apk add --no-cache java-cacerts
# Sat, 13 Nov 2021 07:32:27 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Sat, 13 Nov 2021 07:32:27 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 07:32:27 GMT
ENV JAVA_VERSION=18-ea+11
# Sat, 13 Nov 2021 07:32:40 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 13 Nov 2021 07:32:40 GMT
CMD ["jshell"]
# Sat, 13 Nov 2021 11:56:13 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 13 Nov 2021 11:56:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 13 Nov 2021 11:56:13 GMT
WORKDIR /tmp
# Sat, 13 Nov 2021 11:56:15 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Sat, 13 Nov 2021 11:56:15 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 13 Nov 2021 11:56:15 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 13 Nov 2021 11:56:59 GMT
RUN boot
# Sat, 13 Nov 2021 11:57:00 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad0d0169427449f303a2c6baf5a00c969d2b2b85c2edd07aaa19ce580773a4a`  
		Last Modified: Sat, 13 Nov 2021 07:40:09 GMT  
		Size: 928.2 KB (928186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c40c2a9a506010fe514760d27418dde11f26d48c0ceb564f3e4f2bf468074ba`  
		Last Modified: Sat, 13 Nov 2021 07:40:24 GMT  
		Size: 188.7 MB (188699691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e75099e637f182a534369f10677dc67fef732fc7a4790eacccadfec0dee9b0`  
		Last Modified: Sat, 13 Nov 2021 12:05:51 GMT  
		Size: 829.1 KB (829066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2244f901b1d58804fb35193db78d254c2ffeefe9acc474c3ac26b54b71cafbe0`  
		Last Modified: Sat, 13 Nov 2021 12:05:55 GMT  
		Size: 58.8 MB (58821134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
