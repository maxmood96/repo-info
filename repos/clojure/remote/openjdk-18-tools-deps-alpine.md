## `clojure:openjdk-18-tools-deps-alpine`

```console
$ docker pull clojure@sha256:2cd54fb086ce9048d4305278eb89a19d95038cc6a48d660761cbff53a399b53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-18-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:875d0b344b0cdc41cbf7da7e4c1f98e4d220ed8fe4e995388958ba69919253ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218407317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22c435cba2b49ddf47acc5cf70c8fd863932f97b9c8295af7d2a1c54b30ba17`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:32:26 GMT
RUN apk add --no-cache java-cacerts
# Sat, 13 Nov 2021 07:32:27 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Sat, 13 Nov 2021 07:32:27 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 07:32:27 GMT
ENV JAVA_VERSION=18-ea+11
# Sat, 13 Nov 2021 07:32:40 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 13 Nov 2021 07:32:40 GMT
CMD ["jshell"]
# Sat, 13 Nov 2021 11:57:10 GMT
ENV CLOJURE_VERSION=1.10.3.1020
# Sat, 13 Nov 2021 11:57:10 GMT
WORKDIR /tmp
# Sat, 13 Nov 2021 11:57:17 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "afc87e2c8cfbf87e43553439c69a4c8e36bc2094405d08f39ca542b4cca0920a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Sat, 13 Nov 2021 11:57:17 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad0d0169427449f303a2c6baf5a00c969d2b2b85c2edd07aaa19ce580773a4a`  
		Last Modified: Sat, 13 Nov 2021 07:40:09 GMT  
		Size: 928.2 KB (928186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c40c2a9a506010fe514760d27418dde11f26d48c0ceb564f3e4f2bf468074ba`  
		Last Modified: Sat, 13 Nov 2021 07:40:24 GMT  
		Size: 188.7 MB (188699691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9a0625d8cc8e3b0c73a27d4320c4b8f965bd4f611f381ced7eedcff0ac88f8`  
		Last Modified: Sat, 13 Nov 2021 12:06:06 GMT  
		Size: 26.0 MB (25956459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
