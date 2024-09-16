## `openjdk:24-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:84c2920a4acb70943366362d94015641c051d279c9f4e6635f33b1333f9016a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oraclelinux8` - linux; amd64

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

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

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

### `openjdk:24-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:876f846ac52ceba6c9c88b6dc22c859ecba6cf9ced81d7a232b430537c650731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275875975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf7df4934d981542ce9a41e6559495065e1e986f3dbe92b2aae744f0c4df921`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:35:51 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:35:51 GMT
CMD ["/bin/bash"]
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 14 Sep 2024 06:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Sep 2024 06:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_VERSION=24-ea+15
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='b41d4867c348d7f1991085d8bcc8797eaf032d9dfaa3419bc9db15eaea75e91e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='165b7c19403e9708ca261cdfe4c385e837df683049203e33ad2bf76228054a25'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:26021d1fe840c0392b944d95d8144754412f70a5f838918b647f05d3328586c0`  
		Last Modified: Tue, 10 Sep 2024 05:36:16 GMT  
		Size: 50.0 MB (50007854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8f1fe5883f1349449977ab234d0a93bca6d93708c0b7fbc87d663587cc3b10`  
		Last Modified: Mon, 16 Sep 2024 19:21:20 GMT  
		Size: 15.7 MB (15702876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7b88ac3417a144ebd170d098de7bace93847e040767e86cd914c4ea755b51`  
		Last Modified: Mon, 16 Sep 2024 19:21:26 GMT  
		Size: 210.2 MB (210165245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:dc50f023297fa7268eb18e3ce462ebb1ec301b8eae6f69326c4aa4105e478244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4a85eac8f3e888407b40fb23c527216f8e626cf69b047ee4f1e347b65cd028`

```dockerfile
```

-	Layers:
	-	`sha256:071d3fe1f948efde876a2247893eb7fcd9273b18a8e80228ae286477e9c7e5e0`  
		Last Modified: Mon, 16 Sep 2024 19:21:20 GMT  
		Size: 2.3 MB (2287338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0168019933040f424631efaf73748c29f1c908b4500c55f43fb4dbf95324c69d`  
		Last Modified: Mon, 16 Sep 2024 19:21:20 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
