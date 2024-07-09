## `openjdk:24-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:bd04ee991b4e1a35aa018e4f61483c85826d3f434219107af59c35149c5a7e6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:62ddf43edad1587d2d318a8b38c6590f08216c626837c644b4397f370fb9eb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298242463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aed08e90d8e7f35d02d4976d3b59a1281c5572f902a9a7fe906605de379d03e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f320f4609c78d43ef6d8e1a2359d2a4040505b830301d5c98599f895a0288ce`  
		Last Modified: Mon, 08 Jul 2024 20:56:58 GMT  
		Size: 37.9 MB (37862625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f53be992d36102e38a13e156f9ab4331c37a5ee8ae29fd2bea84ae5a6135f7a`  
		Last Modified: Mon, 08 Jul 2024 20:57:00 GMT  
		Size: 211.4 MB (211386185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a6a49e50e9a687cd8c845fe36898508025d299471ea377979072b05aacf9269a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecab36f0d2cea1ed5f967b73b64b3c09395728b700d443948d6cf65d7f1b7132`

```dockerfile
```

-	Layers:
	-	`sha256:5356f07e20e5a0743b6c55d16e73b78939b76400a4d8b276ee5f2e5c9219674f`  
		Last Modified: Mon, 08 Jul 2024 20:56:57 GMT  
		Size: 3.3 MB (3333228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e68b5a7d1dedc201cdd893c203b9953ea5c64926d62fa66f871bb9b21f37de7`  
		Last Modified: Mon, 08 Jul 2024 20:56:57 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b327aef9274c67d0a50ae3537b41b89d1a45d21f016a4e66e90070c47f6be277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295173420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7fc350b67e950e4a70dbbcd19f334b082bcd33c039eb69e5f1cbf1af40cb22`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090038af1dc654e39101a0e5c1948e4487961717162abcaa289f614004326864`  
		Last Modified: Mon, 08 Jul 2024 20:57:10 GMT  
		Size: 38.3 MB (38256393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227419e67fdf132c6283bb10917ff62a6e7daf642373b953eb1f91311365ab78`  
		Last Modified: Mon, 08 Jul 2024 20:57:13 GMT  
		Size: 209.3 MB (209264261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6ba86c69f38cc658a5e85981b238d7dadb55610a87047c534f0d5042899b397d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc7695dd9476a674beb30971dc97cadb05b6ba55805def63a318b5409c1b3e7`

```dockerfile
```

-	Layers:
	-	`sha256:5aea8a20fb388713125d52040f8cd7e3e9562ac3e46b1a398947ed5a480ff541`  
		Last Modified: Mon, 08 Jul 2024 20:57:09 GMT  
		Size: 3.3 MB (3331611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbe4e76573a75ba292e38b294c0b3acd0d994e21a572953cc5a3b0f4ca5275a`  
		Last Modified: Mon, 08 Jul 2024 20:57:08 GMT  
		Size: 20.0 KB (19978 bytes)  
		MIME: application/vnd.in-toto+json
