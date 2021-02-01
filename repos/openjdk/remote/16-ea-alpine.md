## `openjdk:16-ea-alpine`

```console
$ docker pull openjdk@sha256:49d822f4fa4deb5f9d0201ffeec9f4d113bcb4e7e49bd6bc063d3ba93aacbcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:16-ea-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:f9be8e89a2bbf973dcd6c286f85bb0f68a8f9d5fa7c6241eb59f07add4a24789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189697937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa8569968b8d76c8e121516f183b8abc2b639158973a5812a2a6c474a80c63a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Mon, 01 Feb 2021 19:46:23 GMT
RUN apk add --no-cache java-cacerts
# Mon, 01 Feb 2021 19:49:51 GMT
ENV JAVA_HOME=/opt/openjdk-16
# Mon, 01 Feb 2021 19:49:51 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:49:52 GMT
ENV JAVA_VERSION=16-ea+32
# Mon, 01 Feb 2021 19:50:18 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/32/binaries/openjdk-16-ea+32_linux-x64-musl_bin.tar.gz'; 			downloadSha256='f9ec3071fdea08ca5be7b149d6c2f2689814e3ee86ee15b7981f5eed76280985'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:50:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1834e342ac63f74ab268f59b78219089f04f37c6c39e469afc0292192b9c2d`  
		Last Modified: Mon, 01 Feb 2021 20:02:23 GMT  
		Size: 928.2 KB (928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f4563ac5cfaa5b85c77a78809e4a4d118e39ea769eff648554e6b66d21ad3f`  
		Last Modified: Mon, 01 Feb 2021 20:05:18 GMT  
		Size: 186.0 MB (185958372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
