## `openjdk:17-ea-14-alpine3.14`

```console
$ docker pull openjdk@sha256:4b6abae565492dbe9e7a894137c966a7485154238902f2f25e9dbd9784383d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:17-ea-14-alpine3.14` - linux; amd64

```console
$ docker pull openjdk@sha256:a996cdcc040704ec6badaf5fecf1e144c096e00231a29188596c784bcf858d05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190538213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264c9bdce361556ba6e685e401662648358980c01151c3d977f0fdf77f7c26ab`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 21:40:57 GMT
RUN apk add --no-cache java-cacerts
# Tue, 22 Jun 2021 21:40:57 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Tue, 22 Jun 2021 21:40:57 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Jun 2021 21:40:58 GMT
ENV JAVA_VERSION=17-ea+14
# Tue, 22 Jun 2021 21:41:09 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/14/binaries/openjdk-17-ea+14_linux-x64-musl_bin.tar.gz'; 			downloadSha256='f07a1ac921333dafac1cd886ad49600ce143be7efebd32e1a02599a8a0829dd4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Jun 2021 21:41:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c9466125e464fed5626bde7b7a0f91aab09905f0a07e9ad4e930ae72e0fc63`  
		Last Modified: Tue, 22 Jun 2021 21:51:51 GMT  
		Size: 928.4 KB (928436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d715783b80cab158f5bf9726bcada5265c1624b64ca2bb46f42f94998d4662`  
		Last Modified: Tue, 22 Jun 2021 21:52:05 GMT  
		Size: 186.8 MB (186798299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
