## `openjdk:19-ea-5-alpine`

```console
$ docker pull openjdk@sha256:ed44c8062a672fab12c3bab1379ed65d6cd47fbd89f0eaacd067ad03440f85f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-5-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:24e7974abfc4d32531fc34c61115ce7b709ed7d64119913599cc7b8ba0d6a458
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194325864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b13fd32ce444b672edd5b30e74142b1a3a30897dc0a390c4662f3d8a0ae821`
-	Default Command: `["jshell"]`

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
