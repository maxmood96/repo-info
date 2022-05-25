## `openjdk:19-ea-jdk-alpine`

```console
$ docker pull openjdk@sha256:f59fa1224f4af28299e484fd72c13549408b69b20ba4ad3b590a854df22dfd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-jdk-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:5bf18c827959c2d7b56b27328547faeefba886f23be35c0fe2093a5353135d99
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194310946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca34f2407938c2d19fb198df608c843f79f3f9d94d39c77a40a28d35d89f352c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 19:39:36 GMT
RUN apk add --no-cache java-cacerts
# Wed, 25 May 2022 19:39:36 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Wed, 25 May 2022 19:39:37 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 May 2022 19:39:37 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 25 May 2022 19:40:00 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 25 May 2022 19:40:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7539cd38faad629c8ff238def9f20f1fc46a9ffcf39b6d18ec1de588346a69`  
		Last Modified: Wed, 25 May 2022 19:45:16 GMT  
		Size: 919.4 KB (919428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b7305bbd037f158fc336e8bbd92d50181ba5dd151233c90af909ef97523bed`  
		Last Modified: Wed, 25 May 2022 19:45:30 GMT  
		Size: 190.6 MB (190592629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
