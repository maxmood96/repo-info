## `openjdk:26-jdk-oracle`

```console
$ docker pull openjdk@sha256:08c989c63625ab6c0d0ba4325bb6d0d60ffe3d91aa88e6e8e99796f231207a17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:8d7c378765a71534f01b7282f8a5e3b34cd0c9214762151f77468ba417026c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313253484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623e9b73c742e68499824e9d0a93e2de15804b3cf7a2cf31a97c4d44aedc9142`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c866b10aa84572d6ccbe9ede1c14e6efb6e2dbe1cdecfdd5070cae2ea27f72`  
		Last Modified: Tue, 21 Oct 2025 20:20:42 GMT  
		Size: 38.1 MB (38087689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0597ba46067f9c883e71e3c80c84ae2224b43600a53b6f1771d77742a04008b`  
		Last Modified: Tue, 21 Oct 2025 21:30:18 GMT  
		Size: 225.7 MB (225669290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:4a5ed51e5f0b75cfa7223f23a55bb679803f9d9cdcd772af5ed0339b28769677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee96783f628f0a03477b012f9829f231a80c0f460edb5900307d4615e6fe1053`

```dockerfile
```

-	Layers:
	-	`sha256:2e85abe5da17d804ae255cbb6412ec25ba6e2292cd27124782bc016ec37888ed`  
		Last Modified: Tue, 21 Oct 2025 21:23:26 GMT  
		Size: 3.6 MB (3639498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e739561f92386c76f77e10b96b5b5c43ebccd49b14b31f997c504abe4546dd4`  
		Last Modified: Tue, 21 Oct 2025 21:23:26 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:80f0e92ed6f4d4d80f4ffd9170ac79a4a35d56298cac5304e9c64db3ac672a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310109383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca318e0c6b372994880cbacf95242d4533226be5a44dc6070af01c09ef2bbe7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7abf9b5ac6e04ae79429ac398f1c36fe0800241f536cfec4212e43951406c4f`  
		Last Modified: Tue, 21 Oct 2025 18:13:51 GMT  
		Size: 38.5 MB (38491195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27c39ec2fc86bde4248d7676af7a1be3e098446bed593adc792141beaec2ce`  
		Last Modified: Tue, 21 Oct 2025 21:37:02 GMT  
		Size: 223.5 MB (223531287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b06072fd086447aff33d4b1f6c8a71d7dbd056a704f61ebbb0ffe264c55b1560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb747b7cf2206f08db68e772b32efccc04a2dee17c68bcd22141c2e131e2e4e6`

```dockerfile
```

-	Layers:
	-	`sha256:4671df4d1762f10bb5f78ef01f1eb575481a26ade2f2725da736e05be92eea9d`  
		Last Modified: Tue, 21 Oct 2025 21:23:31 GMT  
		Size: 3.6 MB (3637260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb4c00d5b889a7d6b210c9cfcf3e20358d77a6b441af78d33880dadf7bf1150`  
		Last Modified: Tue, 21 Oct 2025 21:23:31 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
