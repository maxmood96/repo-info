## `openjdk:26-ea-33-oracle`

```console
$ docker pull openjdk@sha256:f7ae7aa0250445a1a130a198bf110768f43391ebd41e66b599342587e2e375a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-33-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:bf20711987231781005d4aaa4031485386d5e85b125235fe0ebf63fcaf63706b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313476164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c841da86b75aed2ad8473c66fb85186fd04187f4719b25ef7c3d39a0cbea65`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:09:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 05 Feb 2026 22:09:04 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:09:04 GMT
ENV LANG=C.UTF-8
# Thu, 05 Feb 2026 22:09:04 GMT
ENV JAVA_VERSION=26-ea+33
# Thu, 05 Feb 2026 22:09:04 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 05 Feb 2026 22:09:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde458ea0ff4b78b30f5d919c75eb9e773aceb8420df617f9565a55227465343`  
		Last Modified: Thu, 05 Feb 2026 22:09:26 GMT  
		Size: 38.3 MB (38300090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0630f27946e6452686f52fc9079cfb715f84bf941fa0d696165caa28626e815b`  
		Last Modified: Thu, 05 Feb 2026 22:09:30 GMT  
		Size: 227.9 MB (227868532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:598f356c001356067f25f9796e2c8b9966ba12ddfabb4af1ce65aa0a4976246f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fa6599ce81b022d0af011bea8bd1a6742925dae76d0937458737695d5ff65b`

```dockerfile
```

-	Layers:
	-	`sha256:38e5e2b0bf08f14e9526c835a81e71067b9fd1dd3b06dd8393300ddb05b3b727`  
		Last Modified: Thu, 05 Feb 2026 22:09:25 GMT  
		Size: 3.7 MB (3655419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b3605fcc630f4679510d240de3c34a4c05243a6810a110ca963fe06c78af36b`  
		Last Modified: Thu, 05 Feb 2026 22:09:25 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-33-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3c2fc88e436a1e42d80de996ea125bc37955a2be6b294d11178245f580ea55ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310385230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894d82ea5b990797572458e6927da99f575e73aa48cd9f8e0104c174b2d3a1dc`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:11:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:11:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 05 Feb 2026 22:11:20 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:11:20 GMT
ENV LANG=C.UTF-8
# Thu, 05 Feb 2026 22:11:20 GMT
ENV JAVA_VERSION=26-ea+33
# Thu, 05 Feb 2026 22:11:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 05 Feb 2026 22:11:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0a21c1ba79d16f56f48e154d176a3ebfd98240e948e1b4a553ff00b9873305`  
		Last Modified: Thu, 05 Feb 2026 22:11:43 GMT  
		Size: 38.7 MB (38697324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdd596edae2a808c97aa0a549aa6a01f846421c5977a5d3ec7fdaa82ef65b4d`  
		Last Modified: Thu, 05 Feb 2026 22:11:46 GMT  
		Size: 225.8 MB (225784496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:4caef164a5d45923173b3fca2ab8ac094cb0baaae28bbe04586776bf035cb38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30248390245a408226a033e85977f62ce98573c36d667402d0e769daef87f96f`

```dockerfile
```

-	Layers:
	-	`sha256:e9eeed2b4c353629e990341c9aa6ee463dbb4b236c7e9764f07547243abaecd4`  
		Last Modified: Thu, 05 Feb 2026 22:11:41 GMT  
		Size: 3.7 MB (3653109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4bb650366195a9e08f7fd885cc5a8fb659e4c8c5742eaf0b49c19d470310ce5`  
		Last Modified: Thu, 05 Feb 2026 22:11:41 GMT  
		Size: 18.1 KB (18053 bytes)  
		MIME: application/vnd.in-toto+json
