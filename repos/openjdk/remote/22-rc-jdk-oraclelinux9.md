## `openjdk:22-rc-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:4739c72f44d7c0a47712b440e345aa72c47497774e6b2d8b41ed612922a84789
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:22-rc-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:aa232ec30b86617a044994b3898a1a61d7ee739cb6aae7944084c37b0aa1255b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289480248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a271298cf196c7aaa694279395e0c7e10640b40f3071042ffd3a0740c1598f1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:04 GMT
ADD file:9bcef05fa351e2fb72a4b6052a0252eeaa2cff794ed089a482670c67961d2e90 in / 
# Fri, 08 Mar 2024 19:21:04 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 15 Mar 2024 16:08:04 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 16:08:04 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_VERSION=22
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:972029ff9873af36c6c0fcee05b14acbc57a61ecd0b8bf86b167bdf46f973823`  
		Last Modified: Fri, 08 Mar 2024 19:22:31 GMT  
		Size: 49.0 MB (48978454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04e36430406bb6588fe835b6268588b825205320c94fbd96651f340a618da24`  
		Last Modified: Fri, 15 Mar 2024 23:56:11 GMT  
		Size: 37.7 MB (37733618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c9b018c642931f767eff0ee01c56b4805e644ebaff9ba39c4e2ce5d1f174e7`  
		Last Modified: Fri, 15 Mar 2024 23:56:14 GMT  
		Size: 202.8 MB (202768176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:03a821ae7863e1d4fb951c920442a09281960eb7468d43006cfddca019d960ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989f6e5925fb1a36b7a63fc4a063afc841dbdfdf6f52934016dcb3de3a576817`

```dockerfile
```

-	Layers:
	-	`sha256:df3900d63d29682f3a3d17ecaa8de3563b7259cd06a78831d3594cdecff5a87b`  
		Last Modified: Fri, 15 Mar 2024 23:56:11 GMT  
		Size: 3.3 MB (3327582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebbd60a7e7ac1c2b8e00c836cf3306c543d50f09287d94e2aafcad26cb24179`  
		Last Modified: Fri, 15 Mar 2024 23:56:11 GMT  
		Size: 18.0 KB (18025 bytes)  
		MIME: application/vnd.in-toto+json
