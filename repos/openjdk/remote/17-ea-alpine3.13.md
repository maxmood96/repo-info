## `openjdk:17-ea-alpine3.13`

```console
$ docker pull openjdk@sha256:29a512da3618d3bd815f21a3edfc93f8aeb8db3bde18065bc473433e704f91ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-ea-alpine3.13` - linux; amd64

```console
$ docker pull openjdk@sha256:7e1426ff3f1ce54117609db3fb277ba2c8f039aa3de04a014019bd902149f439
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190810903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f0456324daf46775d08ad9118318873a61f3a2dad6536aa2107b04c3c4eb31`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 05:42:40 GMT
RUN apk add --no-cache java-cacerts
# Thu, 18 Feb 2021 05:42:40 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Thu, 18 Feb 2021 05:42:40 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Feb 2021 05:42:40 GMT
ENV JAVA_VERSION=17-ea+5
# Thu, 18 Feb 2021 05:44:02 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-17-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='709daae3577453dba8e4ea03e8b52daeb11370648d2da1d012df527556c0cda2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Feb 2021 05:44:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155cb13c45d5b09951cf0b8e75c365b37550dce6b8ca7c5532d4bd491dd8f3f6`  
		Last Modified: Thu, 18 Feb 2021 05:48:13 GMT  
		Size: 928.2 KB (928245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b734bc2be44a08658a032f99ca24092dcf632770965fcde5a74dd0b728f74dd`  
		Last Modified: Thu, 18 Feb 2021 05:48:30 GMT  
		Size: 187.1 MB (187071001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
