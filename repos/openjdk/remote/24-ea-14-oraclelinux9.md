## `openjdk:24-ea-14-oraclelinux9`

```console
$ docker pull openjdk@sha256:c1fd8d7552d9429fbc3d7ed779e10f63588d2214400d339e7bc362ec13887c3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-14-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:b159ded0cf121c02fd216f9037a1c9175c7c11af45b5552e87d089de20175a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301489577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6db179c05511cd99f61dba6ced7ca2ab8bea8626a013c4f7d6e0121b52cfdb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 06 Sep 2024 18:48:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
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
	-	`sha256:5e407bf3af905fb1f6edf271f870052697e79b018f921119921615cd25365fdb`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 49.2 MB (49239252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a87f9d67e2d21e2798c86432dad12f7f48ed183498d0975b68916bc4102c1a`  
		Last Modified: Tue, 10 Sep 2024 01:54:50 GMT  
		Size: 40.4 MB (40418113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9285c8120b81c73c125c64f3a20e9459f1cd26ed2dc6b7f5cbee8c6e994e91`  
		Last Modified: Tue, 10 Sep 2024 01:54:52 GMT  
		Size: 211.8 MB (211832212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-14-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:260ac5795c0020d08bf40ce793e13fcd12e28fdb25272dac38f9a2bab029f3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac388db3710a73a9541725631bb7baecbf4019716e3cd2c4d4f70714458fcb3`

```dockerfile
```

-	Layers:
	-	`sha256:6804131feb910f8b3cf8f6d2af1529778b3ee6b4ab6625bd4077021a066adef1`  
		Last Modified: Tue, 10 Sep 2024 01:54:49 GMT  
		Size: 3.7 MB (3670499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b5d8c3c243cea077a1f9f1baa8d2f6aa88f43f52be2d47206e016edbd69d20f`  
		Last Modified: Tue, 10 Sep 2024 01:54:49 GMT  
		Size: 19.7 KB (19711 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-14-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7e4ac73aafbdceded98958093807e138f3cb2d2e1de041ee687c9bc2b79d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b53d67a6b28cd6331c14652cf3e908863b758f86ceebbf1627d4598d5d0a2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Aug 2024 00:40:26 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Fri, 23 Aug 2024 00:40:27 GMT
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
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d43f5ded4088b46b5f902d592d52c2a52fe637a75fa3f5875e873ef3c66794`  
		Last Modified: Fri, 06 Sep 2024 22:24:26 GMT  
		Size: 39.5 MB (39489040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d7fa6da34451efda3c1a92cd10668e1a134ca1405ab43685514606fba6d5db`  
		Last Modified: Fri, 06 Sep 2024 22:24:31 GMT  
		Size: 209.7 MB (209682487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-14-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:936533b61d2992156efad41e06a4ce1caa66d2d45235602ab318d6a52345e28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3662636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f969693b433324783afb49977e3e26de49933ac60d68deb52e126d716b93ca`

```dockerfile
```

-	Layers:
	-	`sha256:2e0f6396590117672fe8bfd5afb11fef6f159c4f42f4165a83bfc2052b8ffd39`  
		Last Modified: Fri, 06 Sep 2024 22:24:25 GMT  
		Size: 3.6 MB (3642634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e10d7a56aa517e82008b3b58f731e128e98cc2cd37faecdff4a90b856e896b`  
		Last Modified: Fri, 06 Sep 2024 22:24:25 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json
