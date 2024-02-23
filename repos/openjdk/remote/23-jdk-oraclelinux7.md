## `openjdk:23-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:6b77bc24429bf1b5246ca257189e8bb35c6303b8197946d4894dad36c3d0602a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:f2672ba8d014c1b5edee43b65d2e2387c92a9f267cd1016c1aed8e2f6e0e906e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267725366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54e216ad2772d1b2feea7e3f7bf71d973c18edc6c89ee8e6be5696187e2203`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:52 GMT
ADD file:6c43f1bc1b598f7b1a5fc6f5c7951e8525eee01704f8f5e5caec8a944a4ecb4d in / 
# Wed, 14 Feb 2024 01:47:52 GMT
CMD ["/bin/bash"]
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ff90099b5a4df32952d1822d472a72c931c53a68c05a3ba7431ea0f85d54135`  
		Last Modified: Wed, 14 Feb 2024 01:50:04 GMT  
		Size: 50.4 MB (50389833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2de0362562e4398264384df79f32fd24b13483430ff8d5daee965d0016630`  
		Last Modified: Fri, 23 Feb 2024 18:51:09 GMT  
		Size: 14.2 MB (14231540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c25f4cd66287e162e5064c220e728add36c8655ab16073a243dd45a55c917b2`  
		Last Modified: Fri, 23 Feb 2024 18:51:13 GMT  
		Size: 203.1 MB (203103993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:16bd464d8e8e13114c9e80be882f1f408c69db496cea2fb34da70dcec8542890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdb835d08c8ca04d2f42520cf29fe05dc8dbb23480ab3a7a54fb6b4fdff64fe`

```dockerfile
```

-	Layers:
	-	`sha256:2bc3688240155b72312604634dc39c49dba2e1045d1706a400bd65e7617c98de`  
		Last Modified: Fri, 23 Feb 2024 18:51:09 GMT  
		Size: 4.4 MB (4429923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb0997f43145b2a8a8ef2533d67ce4aee20355687afd868dcb3c765a12a376c`  
		Last Modified: Fri, 23 Feb 2024 18:51:09 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0c1259e039dc56d8baad5b876a6ba2c9e079fd1ae57217631a65939a8db6a504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267243824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdeeebb457bd9090cf21ee3857c19ea440caca7af76fa7c051def2241dbfdfb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:45:11 GMT
ADD file:8a1de5e2eb0c974503a07ee47335076f6fd201d377d647cbc5454453b71f05dc in / 
# Wed, 14 Feb 2024 01:45:12 GMT
CMD ["/bin/bash"]
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f12fd75c9aeabed692ef7b5d8a691db1e8f77911ac84bdaba43458300ab36fb9`  
		Last Modified: Wed, 14 Feb 2024 01:47:06 GMT  
		Size: 51.0 MB (50996218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f5782b608cb55c41f80fe5c4e8c6606f42add68733d4172117af3cbf2d90aa`  
		Last Modified: Wed, 14 Feb 2024 11:17:14 GMT  
		Size: 15.2 MB (15244449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a79172380130f250511b2158cd312404dd55305d0f4668c4c42bcd25238ea7c`  
		Last Modified: Fri, 23 Feb 2024 19:02:49 GMT  
		Size: 201.0 MB (201003157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:8955cea176373f922f06dde259f00432f79aff557c5f023f28a60114d37eb453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4441830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70821db8694d6d5f72267824b9868a20d954c6e91f1202139e30fe6a2252423b`

```dockerfile
```

-	Layers:
	-	`sha256:17186a6abc60ba3b5733837e2d3f9ba3977f7395d7c2d290ef1172c0ee14781b`  
		Last Modified: Fri, 23 Feb 2024 19:02:44 GMT  
		Size: 4.4 MB (4425580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b79e99fb67854b72324a6e061acb4c05121cd9e3c5872cd78a38168113e515`  
		Last Modified: Fri, 23 Feb 2024 19:02:43 GMT  
		Size: 16.2 KB (16250 bytes)  
		MIME: application/vnd.in-toto+json
