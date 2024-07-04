## `openjdk:24-ea-4-oraclelinux8`

```console
$ docker pull openjdk@sha256:4cbf1cc4b9e9c850942315279181fe5fa5b21bbb888c27d75a7ea608d30ba617
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-4-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:da4fd84fb0fa6d3e52529132c25337dd126bbd790b872a7d5b1f2af4ac561451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278039094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ad3c910c7261bf34ee8f333bb4ca1072757237634d079f746db57f80c7c43`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:52:17 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 29 Jun 2024 00:52:17 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_VERSION=24-ea+4
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='64aa493b28493a2d223626bdad774640cb148b0d52f392b081b2776532a980a0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d0b65f191528ab241b4e238568e52fa7199975b4f4b7badcf58a279b1fac426'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bae6bc93086a65f0e3dcda99cdead4b4b085c053ae616a754f7171da5234105`  
		Last Modified: Wed, 03 Jul 2024 23:56:50 GMT  
		Size: 15.0 MB (15036279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a71ed5db32a83f02ca3ee0cfda64a9e3c15c8c868870683a6bfc2d0d3fee0b`  
		Last Modified: Wed, 03 Jul 2024 23:56:52 GMT  
		Size: 211.8 MB (211783191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-4-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:648312e57669b950b622c5d0e0dbc7391aba5b0d5011420f3ea492c76836156a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a048993c2ba22d6f17939436f5046ae3e6e9d3a16e4c85cd050aa9b7bba78da7`

```dockerfile
```

-	Layers:
	-	`sha256:7b5d6aa924a1cad1ad05fd4ff9a973fd88894b30f0792d088376049ca0d10313`  
		Last Modified: Wed, 03 Jul 2024 23:56:50 GMT  
		Size: 2.3 MB (2267569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cac2642615d988a9bd3c6274b33334bf632a3fea47cbaeb80e378f31ed713d3`  
		Last Modified: Wed, 03 Jul 2024 23:56:50 GMT  
		Size: 15.8 KB (15803 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-4-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cc934add472ffc542a1c1340053067b6e8b515308ff1531198dc1ef6edc56df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275253823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012143295402962a944217fa1aab199bc2faeea4bc272838dc84824480e63cb2`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:52:17 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 29 Jun 2024 00:52:17 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_VERSION=24-ea+4
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='64aa493b28493a2d223626bdad774640cb148b0d52f392b081b2776532a980a0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d0b65f191528ab241b4e238568e52fa7199975b4f4b7badcf58a279b1fac426'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6708363575e82894d4714b00358e6cfc904f5e8213ff218080d18d8c0a3aea8`  
		Last Modified: Wed, 03 Jul 2024 22:41:29 GMT  
		Size: 49.9 MB (49925030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53325ebdf5962703e657719964570a5baf1824ea843ea45441c78f115b80fb18`  
		Last Modified: Wed, 03 Jul 2024 23:56:52 GMT  
		Size: 15.7 MB (15686023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f932b7d1981ceff77cc1d2933e6af8078e4deeddf9306c162c526b143fc1613`  
		Last Modified: Wed, 03 Jul 2024 23:56:57 GMT  
		Size: 209.6 MB (209642770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-4-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b27ac79ba23f0e785df5c6057ecc1dd12fe2c3a3e9c5ab0d5ff951325f2c8d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c9edf76762fba501a76314ed8441ad2783f94e43b728fc13fc805ed94e88f7`

```dockerfile
```

-	Layers:
	-	`sha256:ac17395c7f429d4580a894353317c1c5a2f01c61d92c7fe51ad46a4a3c4d2262`  
		Last Modified: Wed, 03 Jul 2024 23:56:51 GMT  
		Size: 2.3 MB (2267038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a61d9f7aac79482abfa8da510ed52c753b1531a8987c9a3f46087012ef08b507`  
		Last Modified: Wed, 03 Jul 2024 23:56:51 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json
