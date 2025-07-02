## `openjdk:25-ea-29-jdk-oracle`

```console
$ docker pull openjdk@sha256:e99a0bdcc12290c5a2f7f1a25faf694a676face03559445fc877ccb88007873a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-29-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:c6fdc3a01586ae69b29b70202a9f345a73000749d69105cdc0c02d555fed8c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310617266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e017c148ccda6772da7c191fcbd1999034a1fe06c8f65041b6544be219c1f27`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 Jun 2025 00:48:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
CMD ["/bin/bash"]
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 28 Jun 2025 00:48:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_VERSION=25-ea+29
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='4fcf990db7180589d31e39c0985acb5d19a6992d77c94892636b4035b004dd3f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='565ce268822423c068fb97a832ad2c4add94427561e8e3ce29057fb8ccfbb72e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7add0131e3ae98d29441ef83ff7a097f3b2c2a09eb8902d5b0cf9b7fb7f1c83b`  
		Last Modified: Tue, 01 Jul 2025 21:36:02 GMT  
		Size: 38.1 MB (38092097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f19ff74f550c502e8d71056786593ff02ea2e2e2baf2668fe190592237c0a98`  
		Last Modified: Wed, 02 Jul 2025 01:02:34 GMT  
		Size: 223.0 MB (223024621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-29-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d7671fbc963056089199fa9e7a581ce46b106f2db3f543425cd4f6d2df3ebd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8fba6fd502379fb120a87ebc3b5fcd5c7977ed218d60e93a48a4925fa81c89`

```dockerfile
```

-	Layers:
	-	`sha256:c2ac769158933a12b2efc5a3eba3e4a4381262acfc5c545f23dfff3b39f01b10`  
		Last Modified: Wed, 02 Jul 2025 00:23:21 GMT  
		Size: 3.6 MB (3641308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aa6f8dd8edfe46e9f749e2071c86113bf11f584a58dff918ad2dfa39f71232c`  
		Last Modified: Wed, 02 Jul 2025 00:23:22 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-29-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1b502e0489bb924a5f1fd44c3ee82cd639f5711e91901fe4190d1b905a709d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307398757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0469fa14c8f66fe9a8bcdc7b92479ef35e6300e0ec5e9c5cea8370c06bde09`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 25 Jun 2025 23:22:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 25 Jun 2025 23:22:52 GMT
CMD ["/bin/bash"]
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 28 Jun 2025 00:48:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_VERSION=25-ea+29
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='4fcf990db7180589d31e39c0985acb5d19a6992d77c94892636b4035b004dd3f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='565ce268822423c068fb97a832ad2c4add94427561e8e3ce29057fb8ccfbb72e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8651adb19772f22f50f38bb61855702b5099b0a0045fea8c9db8dcc1cadfea34`  
		Last Modified: Thu, 26 Jun 2025 05:13:18 GMT  
		Size: 48.1 MB (48087180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf0ee1c604fdbae17917604a097f1f42ae8abcc22cd62c1260386266d1d6ac8`  
		Last Modified: Thu, 26 Jun 2025 04:43:33 GMT  
		Size: 38.5 MB (38495135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df56d3cb3b0aea333de9cd05c77d0fc6eca11d8d820a0ab086b78f3659db74`  
		Last Modified: Mon, 30 Jun 2025 19:06:15 GMT  
		Size: 220.8 MB (220816442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-29-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:bb224ad21a8fbc56ffeb17e973499af14ee79160c84edceb5348f1b3b1aaa230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1916378b11cf56f0213d580debefe040e33dd8bda5932d663f62e6fad87932b3`

```dockerfile
```

-	Layers:
	-	`sha256:223e63fb980c57498c0943a1e898fc4d8bbea5aebdbb90d7829086e5981296b6`  
		Last Modified: Mon, 30 Jun 2025 18:23:33 GMT  
		Size: 3.6 MB (3639070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28830cb0e0432843582ed83545212ff568792f043a6f4eaa4a03b190d40c6674`  
		Last Modified: Mon, 30 Jun 2025 18:23:33 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
