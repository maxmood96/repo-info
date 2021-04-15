## `clojure:openjdk-17-boot-alpine`

```console
$ docker pull clojure@sha256:b8b9eee025b7c70c390db5b396e626416667135fd76936f735db94aa42e61eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-17-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:fca2264bf6f088be2d7c9a268de6c0da542bd6fec8ceb55f04ff5c2a8ef0fc70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250187729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e21b7286303cbd3a4b825b2d4e2da6c9bdf6806ae88f6d4d209a1d8ff43b740`
-	Default Command: `["boot","repl"]`

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
# Thu, 15 Apr 2021 10:06:56 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 15 Apr 2021 10:06:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 15 Apr 2021 10:06:56 GMT
WORKDIR /tmp
# Thu, 15 Apr 2021 10:06:58 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 15 Apr 2021 10:06:58 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Apr 2021 10:06:59 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 15 Apr 2021 10:07:27 GMT
RUN boot
# Thu, 15 Apr 2021 10:07:27 GMT
CMD ["boot" "repl"]
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
	-	`sha256:2ce73224fba4e0c669103e9af904a56923446c72a1e644d5e86a300f65e8effe`  
		Last Modified: Thu, 15 Apr 2021 10:10:58 GMT  
		Size: 828.4 KB (828434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ea6b1a9013b5b0596dd6c728db7eb36e71a9569171cecd4217bdcceb618624`  
		Last Modified: Thu, 15 Apr 2021 10:11:02 GMT  
		Size: 58.8 MB (58820598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
