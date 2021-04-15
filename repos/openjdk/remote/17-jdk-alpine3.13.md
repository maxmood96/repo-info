## `openjdk:17-jdk-alpine3.13`

```console
$ docker pull openjdk@sha256:7ee07585addded886cfea377f2ff6d03c707509ef2426b70bd6e1d4e8a3fc7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-jdk-alpine3.13` - linux; amd64

```console
$ docker pull openjdk@sha256:57c2bd64588e39a7d00581b094136e4b13d2056b5a4f5a0fc39f23f17f1b6965
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190538697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9b6ac51f12c210d8e4bd4e7268d4c6e913338dfc6c0963381a065083c55026`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:36:27 GMT
RUN apk add --no-cache java-cacerts
# Wed, 14 Apr 2021 23:36:27 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Wed, 14 Apr 2021 23:36:27 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 23:36:28 GMT
ENV JAVA_VERSION=17-ea+14
# Wed, 14 Apr 2021 23:36:39 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/14/binaries/openjdk-17-ea+14_linux-x64-musl_bin.tar.gz'; 			downloadSha256='f07a1ac921333dafac1cd886ad49600ce143be7efebd32e1a02599a8a0829dd4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 14 Apr 2021 23:36:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59807c90332abccc99cec67ac7e54a6f2030704f47653b41ca8d4d82301dcbd`  
		Last Modified: Wed, 14 Apr 2021 23:42:06 GMT  
		Size: 928.4 KB (928421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f4673b4883008024de99185a0fa8b4c418c4208a54a723b50b7244eeaec203`  
		Last Modified: Wed, 14 Apr 2021 23:42:21 GMT  
		Size: 186.8 MB (186798307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
