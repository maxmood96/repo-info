## `openjdk:27-ea-11-oraclelinux8`

```console
$ docker pull openjdk@sha256:f75c4a4b4450e6fba455a8eddf2f0c161bcccc1d4856d3a517f7bd507dc08640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-11-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:fea9f1730e7f81e0984a80c738c9e96ffcb12b76672ca13c762cb5c0c89ec848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295315008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba25d56cb6cf5a101849a90fb527dbacd990fa82d88b282910b211d18e6771a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:12:15 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:12:15 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 21:24:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 02 Mar 2026 21:25:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 02 Mar 2026 21:25:07 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:25:07 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:25:07 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:25:07 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:25:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:910e0c7025a94af1bf4f9980abe31c6c0541dbb5c579f5a09497c1a5d667c578`  
		Last Modified: Tue, 24 Feb 2026 21:12:26 GMT  
		Size: 51.5 MB (51462874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab824a29fe20e321c4fb1cffacb174a98e65106fa5377eff80b6b8293cae882f`  
		Last Modified: Mon, 02 Mar 2026 21:25:27 GMT  
		Size: 15.0 MB (14986783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdc99fddb579377810fd0d99421966c1f12267421c76178fd894a0fb70107e8`  
		Last Modified: Mon, 02 Mar 2026 21:25:33 GMT  
		Size: 228.9 MB (228865351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:0b203ea256330dada8f25970a62c7f81aa0ca450e95522ae56aaba18b2e53250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d055907637b13c841b3643d0f9dcc3f2c54b1dbf7550f77e3d36d6ba8385ef67`

```dockerfile
```

-	Layers:
	-	`sha256:33261f01df99466d7eb0d51b0c14e9541d5e92633808fe0d26e07dfeaf238c1a`  
		Last Modified: Mon, 02 Mar 2026 21:25:26 GMT  
		Size: 2.4 MB (2448696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a2dbb05c40ed0a0c125c28e7c9e4865d2c15f219cc796bd7e8d61759766fe1`  
		Last Modified: Mon, 02 Mar 2026 21:25:26 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-11-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:eacb6595e1038bc409177b0b265296b10edc54e0d4be79a237a916c3e32eff9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292745050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383ac4a0e83596f2b275019a00c44be8f7a4fa3c4ebd84b26bffce7983a0faa7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:25:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:25:54 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 21:25:03 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 02 Mar 2026 21:25:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 02 Mar 2026 21:25:11 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:25:11 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:25:11 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:25:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:25:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:308b2ffa0912bdff2bf3b77a5f2634a00c2761e38a51260adbdfe882bc668185`  
		Last Modified: Tue, 24 Feb 2026 21:26:05 GMT  
		Size: 50.2 MB (50199180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ca85b2af089e539778f59254ba68450c4714388d4aeaad63b447b1a53e6146`  
		Last Modified: Mon, 02 Mar 2026 21:25:33 GMT  
		Size: 15.7 MB (15700112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db84fd413f2dca9b845d8b4f1c8a36488fa57d6016126d7dc325dec2fe88e31`  
		Last Modified: Mon, 02 Mar 2026 21:25:39 GMT  
		Size: 226.8 MB (226845758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:67d126dc2273a1b06aef9e22e4ca7af850f5813dc15e4eb2266c9256e25f155d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9267ce33e8654777a0c78b168045fe456c1e61241ca6062179ed2803a9d2fc`

```dockerfile
```

-	Layers:
	-	`sha256:f85498c71b79b76034a149f4f0dc3794c568acd6551b08d26e95d2ac421cfc9f`  
		Last Modified: Mon, 02 Mar 2026 21:25:33 GMT  
		Size: 2.4 MB (2447506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8ee5bbe7e7254cdf8d0209e75a74963fd6e211b091daf81926b8e12511c210d`  
		Last Modified: Mon, 02 Mar 2026 21:25:32 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
