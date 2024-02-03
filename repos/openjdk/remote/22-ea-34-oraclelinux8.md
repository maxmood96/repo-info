## `openjdk:22-ea-34-oraclelinux8`

```console
$ docker pull openjdk@sha256:d0bc6ec72af7ca91c5bb523e85ad72fea66915be728e829b0e5893d5fa4a7552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:22-ea-34-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:89771771ae841a63f23a4940c2f6722a2cec0a417f3aa04e7dab28431c0dfb0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269080851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9951f2c7164b318233936cc466e68ce5e5efbb5961188148de8c554c4dcb0bca`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 02 Feb 2024 19:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='170b7192de3e30c796b95d765b12ca457d3f4b05e97bee0bf81709c8b43cd992'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='63460b6a2c4d547d7a8cf4cf86d67a46f5e6a96a62843a787a2aabdbed4df119'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5321363d1f4afdb53dd9623b4c324ff7b6f9e006331aa24d53364131cbfcf719`  
		Last Modified: Fri, 02 Feb 2024 22:53:51 GMT  
		Size: 15.0 MB (14990916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638c9cb5bb1c379ecf3ad742a194f1d83febd499a0ecdfef595f721ee18822d6`  
		Last Modified: Fri, 02 Feb 2024 22:53:53 GMT  
		Size: 202.8 MB (202768204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-34-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:dd4bf964cfca2a4d4ec8522e2398a1318b8ee0232b71b9bd5bb39a803215e043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98f1c7c540bac76e52da31d853675962af70d5507256f860b4d69ee1d0a88f4`

```dockerfile
```

-	Layers:
	-	`sha256:cd1804889dac4e3015a36651d43ac731e14916575e8850b5c39bc5622ba158d6`  
		Last Modified: Fri, 02 Feb 2024 22:53:50 GMT  
		Size: 1.9 MB (1915866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b29b6af58e94efe3b4a2234c2d6062e268fecace7d4bf116fed3c18de0256189`  
		Last Modified: Fri, 02 Feb 2024 22:53:51 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json
