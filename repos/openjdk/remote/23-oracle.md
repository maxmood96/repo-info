## `openjdk:23-oracle`

```console
$ docker pull openjdk@sha256:6a31f75f8c711ec269c00d0cc85dbfcb811b46b7cbd4b6b0e3d206e1b6d024b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:734d37cc3c4def048db31a335c4485eb6c567803225d825f0d331e1de93a3dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269434431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9894dfe046a2b3cd6cd3d0bcf2090bd2d75ccad639757e143a07051d237ae2cd`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:16 GMT
ADD file:cbc540158e77b85113e3a0e0ed1e202046cf293cdb8d7cd890b04883493dbf35 in / 
# Wed, 14 Feb 2024 01:47:16 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81badc5f380f1ca21f6c430303f4107b9b5e0af27c59e3725bf731915b457fc8`  
		Last Modified: Wed, 14 Feb 2024 01:49:17 GMT  
		Size: 51.3 MB (51325575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b03709e2246c1357321974fa62c948ef62d25defe476e1d3b1d7c8e8cfdc29`  
		Last Modified: Sat, 17 Feb 2024 00:53:38 GMT  
		Size: 15.0 MB (15005910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c5f60bbd5d4caaa3b17c8eae5c606cbc80796e18f10587ac94bd4a256c6d8d`  
		Last Modified: Sat, 17 Feb 2024 00:53:41 GMT  
		Size: 203.1 MB (203102946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:716e087438493269c1b52579cdc0205dc8ed5b60f3dca3133cd17c44ce183920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7647a2158d301e7c8b6d7d80abc8e3477d5cecd739a66144b2a7a03ff51b3642`

```dockerfile
```

-	Layers:
	-	`sha256:b91806e75d81e00b9abfdac76f38869998751abdd4ec80d8ca6fb864e4e9b59c`  
		Last Modified: Sat, 17 Feb 2024 00:53:38 GMT  
		Size: 2.3 MB (2271204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e8fab6dd83acb9b2df889f556fb1ee3a6284aa6c738bbe6ca1f3eeca60b350`  
		Last Modified: Sat, 17 Feb 2024 00:53:38 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e2f1d7abb68004c6ee09e1ba233ccb68a036abdbe0b34bb0efe61bc856ff0e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266748100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da61a15e43c52e5a6b1815bf2c3cc53e7fe48d915f3f3664482d38540dc5e0a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b1d3eb6a012567065354e86eb0bac67a32e425e65bc6fe8b5cd84b95a0643`  
		Last Modified: Wed, 14 Feb 2024 11:04:46 GMT  
		Size: 15.7 MB (15691290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2341b94bef246b9e6b4bbbb98d337a699766145dc1df6a27ea832111912ccb6`  
		Last Modified: Sun, 18 Feb 2024 05:15:34 GMT  
		Size: 201.0 MB (200983896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:2eb06e977078c21414f0a09dd04475fdee51bdcce78f7841a40d7e864883d314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cacc13b106dce4c563c603802f4c107fb019b88c72547a6a7700a61302d5a69`

```dockerfile
```

-	Layers:
	-	`sha256:751b823e4f4829abea98181c7e023c897f74445f8c63a4b338ff9b3f2c8ecef8`  
		Last Modified: Sun, 18 Feb 2024 05:15:29 GMT  
		Size: 2.3 MB (2269674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c35bdb8662de38d5430bb350a319aba1b910afe9fd19e519a36ad08de4f74d`  
		Last Modified: Sun, 18 Feb 2024 05:15:29 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json
