## `openjdk:23-ea-25-oracle`

```console
$ docker pull openjdk@sha256:039149510255c5142c45db956f1c8f0321d2d37c6115d4e78eb17ff7f9acc593
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-25-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:2330032dbaa5e5a26a27f35cbc873648b5a6b0066a10bbc6aa505a1c8e802a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298032452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5636b90f15d09b8f6750c6c57d046e69258b7d363a74f68c5d1e4d5c4cc00885`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2024 00:48:11 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Fri, 31 May 2024 00:48:11 GMT
CMD ["/bin/bash"]
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 31 May 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+25
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='155a1386301d0ac6cd1ce5769b31f550bb400d652f4211454b9988bf25fa173d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b00cd1591ad9727c48c07e598f57cdec15fa40b605ae712b67f35f221534d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b697b9633f3095e03b7c2f6c799942a12e6f626d3aa8936bb6032548b8e4a8`  
		Last Modified: Mon, 03 Jun 2024 19:01:02 GMT  
		Size: 37.9 MB (37862598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c3a27ca778663f8f208cf61903b61549b0cadb9c3ecff9539b90c2b1f44051`  
		Last Modified: Mon, 03 Jun 2024 19:01:06 GMT  
		Size: 211.2 MB (211174976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-25-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:394c92d1310966915783986e9892192c8f725d2781f3be9d35b3256b9327e79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913ca7f56c39f3dcb50caaf2c29b1f5c7e4fc2f2878f416e5278b11e9595a3a0`

```dockerfile
```

-	Layers:
	-	`sha256:84680f3a7c56fbbaf779233ea28e2a72fa2a141a9d0dd155d335588ab240b918`  
		Last Modified: Mon, 03 Jun 2024 19:01:02 GMT  
		Size: 3.3 MB (3333243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d8568ddd5b12e69880045074e8904730938130ccf0b3819a0a80a8bb8a99ed`  
		Last Modified: Mon, 03 Jun 2024 19:01:02 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.in-toto+json
