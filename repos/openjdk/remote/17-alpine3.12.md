## `openjdk:17-alpine3.12`

```console
$ docker pull openjdk@sha256:8844e3a6cb91649f2863aa2052dba68fd202ebc236ba3618a4936ca3af958704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-alpine3.12` - linux; amd64

```console
$ docker pull openjdk@sha256:0660c201a6927cef285c2701a51a8b6e6dd33d0b34b36ba938b53a22491e9da7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190616630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fc75fab4b712966f3952e947e156b8e270a8a5c1fde190a31aad628a616ffc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Tue, 09 Mar 2021 20:58:21 GMT
RUN apk add --no-cache java-cacerts
# Tue, 09 Mar 2021 20:58:21 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Tue, 09 Mar 2021 20:58:21 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 20:58:22 GMT
ENV JAVA_VERSION=17-ea+10
# Tue, 09 Mar 2021 20:58:32 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/10/binaries/openjdk-17-ea+10_linux-x64-musl_bin.tar.gz'; 			downloadSha256='fc3ea4225030a5df6191b6027051e705e6c34b72115dfdb36d170d735cb409d5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 09 Mar 2021 20:58:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea7707410946c5cf4f9f2af0296e45ce8735e11d901f7e133ece9efdafeb02`  
		Last Modified: Tue, 09 Mar 2021 21:12:29 GMT  
		Size: 927.4 KB (927410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe2dbf6877f8039535c6e94f8177fcb903c4572bf7858c621a9e9529c4833c1`  
		Last Modified: Tue, 09 Mar 2021 21:12:44 GMT  
		Size: 186.9 MB (186889727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
