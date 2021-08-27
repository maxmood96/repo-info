## `openjdk:18-ea-alpine3.13`

```console
$ docker pull openjdk@sha256:f02d3ae51771dcc8ee8dd5c9f8bb9229e0bf136370a8795478f8b22afaa48e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-alpine3.13` - linux; amd64

```console
$ docker pull openjdk@sha256:b181906123364a2adc243204211fce90237b41269600687e186f79adaf7c8239
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192439984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0b04940cce22b169fea367d24c0a8d437adfba045f31987debf375e011af37`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:32:42 GMT
RUN apk add --no-cache java-cacerts
# Fri, 27 Aug 2021 17:32:43 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Fri, 27 Aug 2021 17:32:43 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:32:43 GMT
ENV JAVA_VERSION=18-ea+11
# Fri, 27 Aug 2021 17:32:54 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 27 Aug 2021 17:32:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42aaa85cf0a4d68c8c5e8aed66464c941480fd1df06842a281fee75b159ef97c`  
		Last Modified: Fri, 27 Aug 2021 17:43:48 GMT  
		Size: 928.4 KB (928408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8620d06b9abd253dea0bd10f66fc0a75d2da8aaf02f68df2fd3a59c81ea17025`  
		Last Modified: Fri, 27 Aug 2021 17:44:03 GMT  
		Size: 188.7 MB (188699607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
