## `openjdk:25-ea-18-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:bb1a59a381471ccb1a9accd9bc9dcc5c24ffc88330b5ca1b27eafd3aaac9630f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-18-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:2e9721fb5d1985c8111f47e45ae14b28d68a115fa379f421502147e1bba56a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299063954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0d65f8afc6f94a0d1263f92d9c1b61305ff2ae53f01d6eed662ac5ae8d2e77`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952dda8603befdbc3d079d07cd1236b572f739e9bc63c9d5a50e339d185ef0e4`  
		Last Modified: Mon, 14 Apr 2025 22:59:01 GMT  
		Size: 38.1 MB (38106128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8450d7c78f440bf2c9160e45101dd0cf2d34b913ae96eaeb936768b1c0e7222`  
		Last Modified: Mon, 14 Apr 2025 22:59:06 GMT  
		Size: 211.9 MB (211866616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-18-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:89c419b83aad6cd9cbf8970f5f821b531d8cfa3d0b2b91ffb418a63750eaa06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3644252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a619ce2bda486008a9eb6a1aad98b5dac94c5459d1b1f5c457383bb8ffdb27dc`

```dockerfile
```

-	Layers:
	-	`sha256:b4ad59f75120f2bdf33ff48a35762a8339de1df2049bab388a29e3edbb057bee`  
		Last Modified: Mon, 14 Apr 2025 22:59:01 GMT  
		Size: 3.6 MB (3624506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c81e9fd9c50a3c4142d84fbe1730a7a919b3e15ed99f353164525afedee39bc`  
		Last Modified: Mon, 14 Apr 2025 22:59:00 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-18-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ddf9c7fbbfd1996647150b539eb9505830e5ed337288ffab62eb3f5399f1e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295856463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea5c0e7977c61cc739e403771f5b7704753cfd96b2ec4400373bec4de7e3280`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5750f1793fdd6894b80fd32af7c3dc7fd61fe28a4003df2c3b5206dfd9ecf575`  
		Last Modified: Mon, 14 Apr 2025 22:58:29 GMT  
		Size: 38.5 MB (38500787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e87964cac2832152cfbf4fef61d2efe16f1950dd6241389c2f163dc7f98c46`  
		Last Modified: Mon, 14 Apr 2025 22:58:34 GMT  
		Size: 209.7 MB (209680853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-18-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:d62963ca8d9155d1680767598ca8a181242a9a3ae3c84dfcd68a8d546cf5edbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d4c711fd3b577c37011fe2dc54470c471824f0f6938159367d98c3696a0b75`

```dockerfile
```

-	Layers:
	-	`sha256:1fba32c0264a14cb63fca4ab8cfd7b474b97df2bea376352abfe770789d47191`  
		Last Modified: Mon, 14 Apr 2025 22:58:28 GMT  
		Size: 3.6 MB (3622268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541f59555fad7f6aef78cecd86b1752e8d43eea3687024508190a64deecd102a`  
		Last Modified: Mon, 14 Apr 2025 22:58:28 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
