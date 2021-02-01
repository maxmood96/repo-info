## `clojure:openjdk-16-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:d832f20fbc646a58c3a200c6be7e47a13a236d186f3637c33eb1f6d710fcc8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:254234158353e554e3f9a65cb17634c1c686f08effd5b660b516a0dcb83320cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249346191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d3345767627ec6795506c3593bd7d373337684b81f00e351897a8d34f5b16`
-	Default Command: `["boot","repl"]`

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
# Mon, 01 Feb 2021 20:48:30 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 01 Feb 2021 20:48:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 01 Feb 2021 20:48:30 GMT
WORKDIR /tmp
# Mon, 01 Feb 2021 20:48:32 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Mon, 01 Feb 2021 20:48:32 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 01 Feb 2021 20:48:32 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 01 Feb 2021 20:48:52 GMT
RUN boot
# Mon, 01 Feb 2021 20:48:52 GMT
CMD ["boot" "repl"]
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
	-	`sha256:72c4843a9cd321370b6b8e8dacd3b6f95cff45c87830d2193ed264e8768323d4`  
		Last Modified: Mon, 01 Feb 2021 20:54:37 GMT  
		Size: 828.4 KB (828409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8755375efb7c439a7bb05c4858793f2bfed09356d92521c589056b96e8c242`  
		Last Modified: Mon, 01 Feb 2021 20:54:41 GMT  
		Size: 58.8 MB (58819845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
