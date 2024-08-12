## `openjdk:24-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:fba27da1c8f4d0dae654a99793112d75286d0106af12531f30cd3b2789a020b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:bb1de1f01254d61ab1c619038ded91a905c977da0ff61edbed564417d54583e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278474134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6be8971739d6ffd71cbe4a77eff09b24669ebda1a1255c89b349284a19a368f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 23:20:38 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Wed, 03 Jul 2024 23:20:38 GMT
CMD ["/bin/bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c4a0071ee69bc91680473e2340f553ba8037ab4408531726458f499a7f856f`  
		Last Modified: Mon, 12 Aug 2024 17:59:29 GMT  
		Size: 15.0 MB (15036191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2cadb14f74a60264452eb9cdeb966bd91dacdaa3d464dbc3a5468865cc07dc`  
		Last Modified: Mon, 12 Aug 2024 17:59:31 GMT  
		Size: 212.2 MB (212218319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2d09283e033fcd54d36e0beff6f14d7df6a065846411a326393544b0f06ec17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35f1ea6fc6d96cfddca0e091e0c414f3674ddcfa36061a5e4e9026a536c64f7`

```dockerfile
```

-	Layers:
	-	`sha256:a8dd5edc5549687e08fbfeda7f224c48cb6e6589816a2bf59dda8ebda4e79308`  
		Last Modified: Mon, 12 Aug 2024 17:59:28 GMT  
		Size: 2.3 MB (2287825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:159d4994f10d7754712dec0f46d29134269e1aa64af2ea4dfdcfb8fa87c3dc8e`  
		Last Modified: Mon, 12 Aug 2024 17:59:28 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:233ee7da2235af2be7f43fccc1f171136b2da12db622dd600c7d3529947b757e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275669835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9061f19b455e7151a4eb749326291b112ddc47e2107b086434a9af3fe588ea`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 22:40:38 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Wed, 03 Jul 2024 22:40:39 GMT
CMD ["/bin/bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6708363575e82894d4714b00358e6cfc904f5e8213ff218080d18d8c0a3aea8`  
		Last Modified: Wed, 03 Jul 2024 22:41:29 GMT  
		Size: 49.9 MB (49925030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca345db69d5fd49f13cb0fd444dd21dc5576cd6587605dd8acb1793f7ebac2b`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 15.7 MB (15686119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e230df25a26c7218ad92274642db654e949a7785d6f4e50d19a90fae8654af`  
		Last Modified: Mon, 12 Aug 2024 18:29:57 GMT  
		Size: 210.1 MB (210058686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d955f45428e30dcf8e83676e089ea0f6bd48188d680f1effafcaf0d63813a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39db82c1a5f1e67552af7f1a4f8fa321d38205f4556281d563defbb1302a7bdd`

```dockerfile
```

-	Layers:
	-	`sha256:603a6a80a8497dff73d9c72aeceec1f8dde0980139c679aacd157fca1940bcdc`  
		Last Modified: Mon, 12 Aug 2024 18:29:52 GMT  
		Size: 2.3 MB (2287294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddd8e3c798960247c3d2475bf24aacee26b111fc80fcb4e49887912ce67a4a8`  
		Last Modified: Mon, 12 Aug 2024 18:29:51 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
