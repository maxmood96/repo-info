## `clojure:openjdk-16-boot-alpine`

```console
$ docker pull clojure@sha256:427a9beab20a4aebad8bd6dd9b0733c7026a7da791035beaf5ad41650232824a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:44aedb35c7c99e078c95a67ebeefb332b11600b9080a9e5506e9ccd37ce7fe9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261005093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1237afe5dbf5fbe6d4701f093ffebc8b6f812b13fda5e0cd83e1e3aea8d8a85f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:36:52 GMT
RUN apk add --no-cache java-cacerts
# Thu, 22 Oct 2020 02:36:52 GMT
ENV JAVA_HOME=/opt/openjdk-16
# Thu, 22 Oct 2020 02:36:52 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 02:36:52 GMT
ENV JAVA_VERSION=16-ea+14
# Thu, 22 Oct 2020 02:37:35 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64) 			downloadUrl=https://download.java.net/java/early_access/alpine/14/binaries/openjdk-16-ea+14_linux-x64-musl_bin.tar.gz; 			downloadSha256=6d6943f9c350ca20fd2892e024c363e538ab4a2c1aeaceeab4450a47cbaca54c; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 22 Oct 2020 02:37:36 GMT
CMD ["jshell"]
# Thu, 22 Oct 2020 08:34:00 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 22 Oct 2020 08:34:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 22 Oct 2020 08:34:01 GMT
WORKDIR /tmp
# Thu, 22 Oct 2020 08:34:02 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 22 Oct 2020 08:34:02 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Oct 2020 08:34:02 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 22 Oct 2020 08:34:22 GMT
RUN boot
# Thu, 22 Oct 2020 08:34:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90d4961e1b84bb83aca8e1aadcad45ff59be8b1b7e2040c1004a1a4e4dd330b`  
		Last Modified: Thu, 22 Oct 2020 02:46:10 GMT  
		Size: 926.4 KB (926394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746e2d2217623d0a52653391881289717c3b58886a6dd0e0c2c74933de18c3c9`  
		Last Modified: Thu, 22 Oct 2020 02:46:35 GMT  
		Size: 197.7 MB (197669288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecb2852acb083966200361ed6ae77f4a1ab3af53326922a9b9ca8dedd986f1f`  
		Last Modified: Thu, 22 Oct 2020 08:36:11 GMT  
		Size: 792.3 KB (792315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3761f2b4b0d910b627034effc5fb66523c4b5a013d91e6e2ab217facd83fa9`  
		Last Modified: Thu, 22 Oct 2020 08:36:14 GMT  
		Size: 58.8 MB (58820236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
