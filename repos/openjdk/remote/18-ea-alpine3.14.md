## `openjdk:18-ea-alpine3.14`

```console
$ docker pull openjdk@sha256:2f63859ec38bc66be7d338a6dcc21984ece02d4e0d45dac35e67363cdef7bb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-alpine3.14` - linux; amd64

```console
$ docker pull openjdk@sha256:032dd42277d85dff42b6189ca6aba090917b2df77a2733bf8f914f9c5a63427a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192442519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107eee9e44806f32017c011ceef1a6fe258392fab6f215b0e2452c4918d968fb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 17:32:24 GMT
RUN apk add --no-cache java-cacerts
# Fri, 27 Aug 2021 17:32:24 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Fri, 27 Aug 2021 17:32:24 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 17:32:25 GMT
ENV JAVA_VERSION=18-ea+11
# Fri, 27 Aug 2021 17:32:36 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 27 Aug 2021 17:32:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79fb3f4ca2289d42dd52c21c56c23417196696f2696abbcdedada7306f552ca`  
		Last Modified: Fri, 27 Aug 2021 17:42:52 GMT  
		Size: 928.4 KB (928417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d1a4c2ebf908279e849340d10f4eb1cb7fdd9fc8468e6ab2f77544ec171985`  
		Last Modified: Fri, 27 Aug 2021 17:43:11 GMT  
		Size: 188.7 MB (188699656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
