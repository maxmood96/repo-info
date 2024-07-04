## `openjdk:23-oraclelinux8`

```console
$ docker pull openjdk@sha256:1f3ee34c8b3168018db4055d45fca765235a99ef297bc5ceac05c0b3a9619409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ef1e9cd7f4aee872772b86ce881d48f20e330b567375e5365676fa7f0931d96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278024456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97f8e19d634a74e69c59bcd6e6b4483689a6d51eb9deaf4a55df8bb6bbec026`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:48:10 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee77a64b0c12cb816b29eacd1593995098ca135ed6078550224c65eaa8096114`  
		Last Modified: Wed, 03 Jul 2024 23:56:57 GMT  
		Size: 15.0 MB (15036221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd961e6533f18b4d0d1d9a2034774515db0f6f6ffa03015ab3a1d54090fc88c5`  
		Last Modified: Wed, 03 Jul 2024 23:57:01 GMT  
		Size: 211.8 MB (211768611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:860313f070e0cd5e1284d311b0940b74d456c3c6a78815ea3db56fa773d9046f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7b95146d1984e5c509a9fc1fb10e56b08bc955d5b96455fb5735a0bc10f626`

```dockerfile
```

-	Layers:
	-	`sha256:92bbb8db189af3350fe83417380017af1b02ee8698bb16ba6a13485a2bdf4117`  
		Last Modified: Wed, 03 Jul 2024 23:56:56 GMT  
		Size: 2.3 MB (2267577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5191f280e55000cd26fecbef512ed952a321fbf3196f4e4e1d17e5f7126f11`  
		Last Modified: Wed, 03 Jul 2024 23:56:55 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e5709b01a1b31e892542d38d72239195b488428de9ff2e075d3cc124b5995070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275238562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ebe0826b447aaed3f5bb226bc1ebfcaa003e347f82ebdb5e483f6d71fb9dc4`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:48:10 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
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
	-	`sha256:7a49a65351eda20e0f4d3c62dfd369f304241eff42c85d38b614d5a3d8c8e271`  
		Last Modified: Wed, 03 Jul 2024 23:57:47 GMT  
		Size: 209.6 MB (209627509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ec7139503068759206fd29fd47543bb25bec2c869875ff4e4c95f7047cc03077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0447be7bcea6c0352080d9817908225ba0b41b673b7e14f35620f8c83be69a44`

```dockerfile
```

-	Layers:
	-	`sha256:997236d424e8fb9a4fc8064d47dbea7057d4eae6f7f995627c8669f5161d94aa`  
		Last Modified: Wed, 03 Jul 2024 23:57:42 GMT  
		Size: 2.3 MB (2267046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1bf9bc7a2c3424b62698bb852758b0c7b2753a12ededc4bebe9077ee474625`  
		Last Modified: Wed, 03 Jul 2024 23:57:41 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
