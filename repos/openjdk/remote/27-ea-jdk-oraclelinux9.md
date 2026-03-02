## `openjdk:27-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:a48cc36abee2a9ec61055ce458bffe7fc6cbfaf87ab00c580926e10cebbb2ece
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:6ad8f5ba98de3152a877030ac1e4868588ef2d76e893c5483ca590f76a5d27a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314021608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4c2a1c0b3755921db24168d90ed5b4b94b6904783de664d8908fd4d99d218f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 21:24:41 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 02 Mar 2026 21:24:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 02 Mar 2026 21:24:53 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:24:53 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:24:53 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:24:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:24:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b378f89d3b59dd1d2eadb50cf14516db8b51b7dab151586f2653e0c104fe11b7`  
		Last Modified: Mon, 02 Mar 2026 21:25:15 GMT  
		Size: 38.3 MB (38298090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fff2388df8d8696b6cd91a57a90a65878a99c47b7fb50a5a6e2afe2f12a48e`  
		Last Modified: Mon, 02 Mar 2026 21:25:19 GMT  
		Size: 228.4 MB (228414647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:aa9ebeb0d7dee793ede02cbe658c31a01acb00f87c6849295515736195c4dc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da9058b790de1d9c59dc66d62c14adfb041fa6d3fcf635ba6df1cbfc3a62856`

```dockerfile
```

-	Layers:
	-	`sha256:1d4c854ab448b678ce6af4ff009e65600fc3b0b5d720babebcc97ff84ec178b4`  
		Last Modified: Mon, 02 Mar 2026 21:25:13 GMT  
		Size: 3.7 MB (3655435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57996459cec9ed1926d136874dd11e49d447cc1b0644ea8bf713dcf31da24680`  
		Last Modified: Mon, 02 Mar 2026 21:25:13 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:effbf31705c8cbb117fb14b8575eef118ec7a352f3ed5cec394bb0dddd8b8ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310960194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7d3c576848f1f34bf6ae8993492e4a944bfb8af4cf9360dfc6f970bf48e575`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 21:23:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 02 Mar 2026 21:24:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 02 Mar 2026 21:24:06 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:24:06 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:24:06 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:24:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:24:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693a35fbad5e339ce57961bc78978d895c6cdf1e4ac0630de341d4ffb92f2c99`  
		Last Modified: Mon, 02 Mar 2026 21:24:29 GMT  
		Size: 38.7 MB (38693718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deb53670e5a776130fe4b9931c060550e0a0ded14903f7956657142f17c1c5a`  
		Last Modified: Mon, 02 Mar 2026 21:24:32 GMT  
		Size: 226.4 MB (226364496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f184d2a0a9cb56dc40a5705635c04cce1102fc3462140217e10c574ec1421ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0876ecafb5e974cee29a73da82a8cf5f85e5b56a82d708ba824da184fc6638e`

```dockerfile
```

-	Layers:
	-	`sha256:e1bfa79593bfe114beab7784c059036b8b63adcc5c0cf2fb0a9b0615b591a2f1`  
		Last Modified: Mon, 02 Mar 2026 21:24:28 GMT  
		Size: 3.7 MB (3653125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58afdbd10330b0b15ced6039052bb11168096a406a25cf4f4963d010e0986c95`  
		Last Modified: Mon, 02 Mar 2026 21:24:27 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
