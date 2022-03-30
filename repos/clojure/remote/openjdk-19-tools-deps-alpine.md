## `clojure:openjdk-19-tools-deps-alpine`

```console
$ docker pull clojure@sha256:07f62e700ffe566355c42130cd35868d2962addb6b25a06d2db8caa5d194b267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:46a184b8a7a0bc81e6b9ff2f2d7888d507b7f29a91b407e26a3e54a93d9f9aa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223745146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04471d67cda6379abe5f290e293438440877fe5181ccd0f44f701864ec35a6b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 00:53:12 GMT
RUN apk add --no-cache java-cacerts
# Tue, 29 Mar 2022 00:53:12 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 29 Mar 2022 00:53:12 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:53:12 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 29 Mar 2022 00:53:23 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:53:24 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:54:33 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Tue, 29 Mar 2022 23:54:33 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:54:38 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Tue, 29 Mar 2022 23:54:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 29 Mar 2022 23:54:38 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:54:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:54:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc6d90ffa98debe440e17dff9ae93f8fc2b8065f5e2d7bc0d2261f9651ae35b`  
		Last Modified: Tue, 29 Mar 2022 01:06:31 GMT  
		Size: 918.6 KB (918583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1650a84836207ca17554d4eebd9a03ac64a82705d0b490da64d2094be0481e6`  
		Last Modified: Tue, 29 Mar 2022 01:06:45 GMT  
		Size: 190.6 MB (190592769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b97c4f4aabc37aa809a829862abf6c41b811634733fcb81c3f64df7addd82`  
		Last Modified: Wed, 30 Mar 2022 00:14:05 GMT  
		Size: 29.4 MB (29418258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e31b2151eb8674e57c81bb791d3296b805d0aaf7bedeeb9cce34fa8af94797`  
		Last Modified: Wed, 30 Mar 2022 00:14:02 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c585977a5731a98bac59c553a7b243a6ede48c9a356bd5eca40405d8a04afaa`  
		Last Modified: Wed, 30 Mar 2022 00:14:02 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
