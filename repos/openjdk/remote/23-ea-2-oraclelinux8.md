## `openjdk:23-ea-2-oraclelinux8`

```console
$ docker pull openjdk@sha256:03cbc8302be6acf7482d104def6e3ef2d3650b7eff10f91c5ed4d5fabeccc335
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-2-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:bfacbf6914020e0074b2ec76f0ffee6aab9700fc6a3a51c7fa8b16d77a856bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269278399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e026b4fea8d97c1a7368b893263669e2d142f3509e2b68694e9836c7a95ac83`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:53:43 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_VERSION=23-ea+2
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='c10168b0639ae5a316fb20444202e82fabe5908be7241f1cd42e34ed9d1eca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='84b416aba4f3578138dd0d27f570dbaee9123528c4d45d13a338278c3d7136c1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b50b646c649fd0100ff8e093760c71fafb17c17ce4db0983c0e19a5cd0af9a`  
		Last Modified: Sat, 16 Dec 2023 01:52:10 GMT  
		Size: 15.0 MB (15003818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401397eb7d249e669ee7e8502f1c7646790132003d9580084c2fa590d9cd4e9f`  
		Last Modified: Sat, 16 Dec 2023 01:52:15 GMT  
		Size: 203.0 MB (202954616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-2-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c9afd03b7dbd00357c815f3b0144a421248f8fbed2328ef15fa217f15f7e6135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8914f5144b57a574c911658b91f974be4d1702abc7fb3a305b597106387471`

```dockerfile
```

-	Layers:
	-	`sha256:7e20e0033e542e5c7a59d0278b5c18a5a287a78c3921806868b48b7db8830f74`  
		Last Modified: Sat, 16 Dec 2023 01:52:10 GMT  
		Size: 1.9 MB (1915813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76d698bb8f1542611cc27191c08f772a777895c17db684344075bdca4b932b0`  
		Last Modified: Sat, 16 Dec 2023 01:52:10 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.in-toto+json
