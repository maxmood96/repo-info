## `openjdk:20-ea-29-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:3ad75a58abe963c9909274ac25943f6d5dc443186d6143e239f35b68d6fba776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-29-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3c168ff239cdf8834c79d53d936f843297b6c2d1b86aed1ed9b83a949b45e87e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254222736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e723fac144316a7af1d7582d34a61beb40bbab89a3ac4f20ca8e51cba88594f2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:27:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:27:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 07 Dec 2022 02:27:04 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:27:04 GMT
ENV LANG=C.UTF-8
# Fri, 23 Dec 2022 01:21:37 GMT
ENV JAVA_VERSION=20-ea+29
# Fri, 23 Dec 2022 01:21:48 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/29/GPL/openjdk-20-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='c8ef212d37d809927edc8f7c4100bc4606a9680ad1646975f365c7fdb2442eba'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/29/GPL/openjdk-20-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='af77c5e0a7ee15fe98e6ed22e007788db669de2637bdd2b6c321144d8a37b260'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Dec 2022 01:21:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3502f40d35be69b4df858d92b5ac60d6b792eec7beabb7cbd78c816329f47b7f`  
		Last Modified: Wed, 07 Dec 2022 02:30:44 GMT  
		Size: 12.2 MB (12248357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03354e6c1e937ec69de0e1f7fb0dddfe0c2f939a0e22b1f38cf36899a9c76ac`  
		Last Modified: Fri, 23 Dec 2022 01:29:58 GMT  
		Size: 198.1 MB (198105641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-29-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8e3428bef7a53df697a215172c15eea5dac70890bb6b86b7f419f024c6945b5c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252443296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4921b7ecca9ef153d1571e92f658e4aa3f67fc2c9e50b2201380bad7c06e07e7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:53:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:53:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 07 Dec 2022 02:53:06 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 23 Dec 2022 00:41:19 GMT
ENV JAVA_VERSION=20-ea+29
# Fri, 23 Dec 2022 00:41:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/29/GPL/openjdk-20-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='c8ef212d37d809927edc8f7c4100bc4606a9680ad1646975f365c7fdb2442eba'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/29/GPL/openjdk-20-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='af77c5e0a7ee15fe98e6ed22e007788db669de2637bdd2b6c321144d8a37b260'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Dec 2022 00:41:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e459b46a4edc515fedc5c9be076b28ba6b0606f3cc90d412ea3d88b15576e`  
		Last Modified: Wed, 07 Dec 2022 02:57:10 GMT  
		Size: 13.1 MB (13058882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14dcc1ed287977c57807fb32e1a1373fbe50fe5bb9dad59e2f3cc88e984ce2f`  
		Last Modified: Fri, 23 Dec 2022 00:49:24 GMT  
		Size: 196.6 MB (196612355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
