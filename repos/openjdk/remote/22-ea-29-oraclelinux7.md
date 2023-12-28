## `openjdk:22-ea-29-oraclelinux7`

```console
$ docker pull openjdk@sha256:aa3a7a70643b66bec8a59119f2c25d39649da58aae596bbe5a6b442d055375d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-29-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:d86804bab8ac515ec74a271ee9c888e06740cd2388590ce26f7da65cb31d55f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267478130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f12b922fb8a82326f5d4f64abe61e8728af98b93708274aa8a38d54429ad4b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 14 Dec 2023 23:21:44 GMT
ADD file:74b33794f8e61e810f09c38da020f9becc9f6987d22fa6f42af6b4226505e6ca in / 
# Thu, 14 Dec 2023 23:21:45 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20e4dcae4c693910efbf28a556e2fa88ef717e15364f63da7e0a4a130b9b714e`  
		Last Modified: Thu, 14 Dec 2023 23:23:14 GMT  
		Size: 50.5 MB (50499235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747225cf6655783afcb4155eeb88a6c665129f0c973cbcd2d2156f23f0d66bbb`  
		Last Modified: Wed, 27 Dec 2023 21:53:55 GMT  
		Size: 14.2 MB (14232177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182af54ff61bb66b578ed3a131da6a5ca2570dcf34617ef8a0cfc06ae38eac99`  
		Last Modified: Wed, 27 Dec 2023 21:54:00 GMT  
		Size: 202.7 MB (202746718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-29-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:f4b31c24db70d9e3647dcaa05c778d8a7517865752608bc673abed738fba7234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6419e8c3d2b51f4dd1353206bc4991eb1cd06975fc37182b5815cc2f00c157a`

```dockerfile
```

-	Layers:
	-	`sha256:bf067937da55db71714c36261f14377c66f4a17d23977c3ca91accd35d7e5736`  
		Last Modified: Wed, 27 Dec 2023 21:53:55 GMT  
		Size: 3.8 MB (3768690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5cc18a81fee6ac5f1df05d5ab1aee8789e220be97bf8d42e9922ccfd9fd489`  
		Last Modified: Wed, 27 Dec 2023 21:53:55 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-29-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2e39c03f5d671ff62da7df14c1086319290cb33ea0ea76bb6ae596344cb19bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267143259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3f8030dcbce0a784a7f8767ad07eeeb2eee7c05f01948808c3f85e6ba98fa9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Dec 2023 00:02:56 GMT
ADD file:7f9b20722f4f2c781b7814e113711ee10ee458be84fe343e7d61658ede9c4711 in / 
# Fri, 15 Dec 2023 00:02:57 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01eab324a7fc4cacc34c78d38ce9548750df098b20899d269b500307b6765a1d`  
		Last Modified: Fri, 15 Dec 2023 00:04:16 GMT  
		Size: 51.1 MB (51110815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96633a794a03133d53bf43854186ba59a38c777f78fe1e7226aff149ef8d228`  
		Last Modified: Fri, 15 Dec 2023 23:21:22 GMT  
		Size: 15.2 MB (15241860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b370819db365b3a1cab945b6a072e476a5a1e6daff4c2c70b8f748f2b7dee9`  
		Last Modified: Thu, 28 Dec 2023 05:05:53 GMT  
		Size: 200.8 MB (200790584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-29-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:eccdfd272321903489404e94d9757815671705107c40436420a130185436e4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eae2d841996eca4f40b5fd592e23499844f9b2455239a50d25914cfed0d75a`

```dockerfile
```

-	Layers:
	-	`sha256:80f545099186cafc6927a1a60bdbce6e1eb4bdac32126c29fb4b635ae990116e`  
		Last Modified: Thu, 28 Dec 2023 05:05:47 GMT  
		Size: 3.8 MB (3764557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f310981dda673ad21c86361c5b68005487426dba3ab0c44680018ba6a480af`  
		Last Modified: Thu, 28 Dec 2023 05:05:47 GMT  
		Size: 16.2 KB (16250 bytes)  
		MIME: application/vnd.in-toto+json
