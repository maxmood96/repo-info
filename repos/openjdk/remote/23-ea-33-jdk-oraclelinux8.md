## `openjdk:23-ea-33-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:52351415eef7dc8eb8b6d2362e6e1202dbc27eaf4f55144c9e3e5ba3fc5312e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-33-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:a90c10127bd21486a0810abd0c3cc7be3e546ca64c970baf0e18e3df2b71c952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278038998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca08f8abf83d23669284ca6e5c20d8f6122f57459bb65d8d0031ace9c1975a38`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 23:20:38 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Wed, 03 Jul 2024 23:20:38 GMT
CMD ["/bin/bash"]
# Sat, 20 Jul 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 20 Jul 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 20 Jul 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+33
# Sat, 20 Jul 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='d44748cfdec1fe164da0725a95fb05f7e4b94070a669f2688f8604154d14df5b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='e25276d4f0cf9fb6f67b3a1be8087fbf0cceadfa33cab8ffc17e99c83e105e74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63f6c25a22370031b05e3cf864e023ae8e9dd55d8219997fc1086194caccce5`  
		Last Modified: Mon, 22 Jul 2024 21:00:22 GMT  
		Size: 15.0 MB (15036197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92923ac64b6c53b74118590aa97370c3852c58019f0a5c5aede057cc8c14336`  
		Last Modified: Mon, 22 Jul 2024 21:00:30 GMT  
		Size: 211.8 MB (211783177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-33-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8b0e2b89549e7fb6ace55c8baa8c8cc3c77471a60562df235e16a5ab3650d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f95e648febe6d536a8cfb68b787df14046ca460e283672a2c62aea72c8d93e`

```dockerfile
```

-	Layers:
	-	`sha256:8cf4b7c9faabac29451831553259d33c97f31c35f35fa535c05cbf9fd6917d49`  
		Last Modified: Mon, 22 Jul 2024 21:00:22 GMT  
		Size: 2.3 MB (2287825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c63af70a1f3dd5dfbbf826652c51cf6e31c46d37afc6e35afe69156e7f96ee`  
		Last Modified: Mon, 22 Jul 2024 21:00:22 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json
