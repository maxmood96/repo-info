## `openjdk:24-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:8f6f67814886bccca8f2d921dc5ec2e39b9c2c4e6ffe75781034686d3b926e60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:fc67137384521429a95422a1c5668df2b803f00ad8759c1174f4c7cbad8b06d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278633462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce1aff5feae938a72ea71b35b9da2a79ff8bdc3cbb387aed377e59ed4b445d1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 06 Sep 2024 18:48:13 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7d760ad2fe664c6995a4d9508e389d78b6bdf1b1f154b4a216d0fd3ad9a46bc`  
		Last Modified: Tue, 10 Sep 2024 01:03:41 GMT  
		Size: 51.3 MB (51293960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c23a68b10483f3bf89822c62cbe47c7a900c8b6f26b83d147575c3dc0c2049`  
		Last Modified: Tue, 10 Sep 2024 01:55:13 GMT  
		Size: 15.0 MB (15040857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f25332a8bbb9604ca8e1888fb808c4b69eb603726d635671fcdcbfaf3bc5ac`  
		Last Modified: Tue, 10 Sep 2024 01:55:15 GMT  
		Size: 212.3 MB (212298645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f05f38be5e331fc8657b6acc50505ad33b5a75c3baf30150eb6945834315b97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69b5d2a505a96c8a22ef19fe405211b822e4f287deb67da47ab151fd36b9292`

```dockerfile
```

-	Layers:
	-	`sha256:5f3f51d04ecb0bc86a854e4ef302de3429a969523222213d7cb596c9647940c4`  
		Last Modified: Tue, 10 Sep 2024 01:55:13 GMT  
		Size: 2.3 MB (2287869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5454c73e73cbac42eb9add66f217b9b89ccbe29bc05f52d6d665693ba64795`  
		Last Modified: Tue, 10 Sep 2024 01:55:13 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:df08456e348c453e43285cf2505b2c1b8420f355ee46f08406ec7e691016cd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275858201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ef53388b577f4f337d864fad5ad6282326b42a83404ca15e3bbee5a45eec05`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Aug 2024 00:40:52 GMT
ADD file:6b13879bf605622e279dbcac5c590af19f2ada3a9a83051585288eac41ef5a5b in / 
# Fri, 23 Aug 2024 00:40:53 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee4bb281b07b90a8d48b631141dbbfe6ee3f5d88680eac4b43c59de36db45ca5`  
		Last Modified: Fri, 23 Aug 2024 00:42:25 GMT  
		Size: 50.0 MB (50007867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c165483eb500b45b6fd4a0a0a8a6f46fbfdc62a2aba4faac778e22aac9005d`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 15.7 MB (15702976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc51607f9b4594225e6b8a2a9948627b64463c1b438c5794e6995a581e46104`  
		Last Modified: Fri, 06 Sep 2024 22:26:55 GMT  
		Size: 210.1 MB (210147358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:84acfe26091493528edcc742ee589577bb1f05cc3cd116c055f42d9382a6e13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb71228d92f092f69c8219979e37cdfee1e4d21e9626a30e7972b553571feef`

```dockerfile
```

-	Layers:
	-	`sha256:745656cf95658b5d9d8fa839b032f2f77cb4b1c9730d0eb19663e5ef00853603`  
		Last Modified: Fri, 06 Sep 2024 22:26:50 GMT  
		Size: 2.3 MB (2287338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62d254168bec24c25935d9f486212ca018aeb289184fced688135e4463fe9e5`  
		Last Modified: Fri, 06 Sep 2024 22:26:50 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
