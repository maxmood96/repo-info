## `clojure:openjdk-18-alpine`

```console
$ docker pull clojure@sha256:231a10f5f69cfb33aedab06a9fb8c93e93cd7e982d4993c4cbc17859316cef7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-18-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:cfc7cd24a1a8242776b34577b85db591568cb2573b0ecce8fe8f2067a077ac57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218623734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddedd34086d7ff38907c04d96ab0c9ad67e340230f69e2ae081c07f56993484`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:45:32 GMT
RUN apk add --no-cache java-cacerts
# Tue, 30 Nov 2021 04:45:32 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Tue, 30 Nov 2021 04:45:32 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 04:45:32 GMT
ENV JAVA_VERSION=18-ea+11
# Tue, 30 Nov 2021 04:45:45 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 30 Nov 2021 04:45:46 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 13:15:05 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Fri, 03 Dec 2021 13:15:05 GMT
WORKDIR /tmp
# Fri, 03 Dec 2021 13:15:11 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Fri, 03 Dec 2021 13:15:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 03 Dec 2021 13:15:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 03 Dec 2021 13:15:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Dec 2021 13:15:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ae5de21b2241a24b653013bdda639de16f984789b28bbcb7108523b460d1e4`  
		Last Modified: Tue, 30 Nov 2021 04:55:25 GMT  
		Size: 932.2 KB (932205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3048de22201addf91c8f64e5382a33c2791d3c21a0906eefce3c4cb08d875839`  
		Last Modified: Tue, 30 Nov 2021 04:55:48 GMT  
		Size: 188.7 MB (188699653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35632dc308f2d94a0fbfe48d57b85836c1466e97918bed83e64706f5f6c3092`  
		Last Modified: Fri, 03 Dec 2021 13:32:04 GMT  
		Size: 26.2 MB (26172437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f212645ac6132208b1ed2ed9092eca53fb2042950856d5ec1336b0108aea60`  
		Last Modified: Fri, 03 Dec 2021 13:32:02 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914def7c587a1b1020d0e0708248e9d50404ad0a601b13bc61ccf24248ba2ea4`  
		Last Modified: Fri, 03 Dec 2021 13:32:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
