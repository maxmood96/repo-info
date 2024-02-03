## `openjdk:22-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:5a4ce346489f954e7cce2f4ea7e9b5431a25f49bcf23fe80ccc7353f57ca3da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-jdk-oraclelinux8` - linux; amd64

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

### `openjdk:22-ea-jdk-oraclelinux8` - unknown; unknown

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

### `openjdk:22-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0a08067b3d083e1f4722818ce17ec786c47bc097bc5925cc7d99ff96d9d02f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266596692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750a8b28a2238e31383964d821e178577e13503971a90ffd85db60b125432fb6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbecf34c8e1a9b9949041e4c9e805d7ee8c1f00ad6362349a4579d6db495c27`  
		Last Modified: Thu, 18 Jan 2024 10:42:33 GMT  
		Size: 15.7 MB (15702213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e6df84efe45220b0b88a68825ee4ca571893eccc5f99cbb8b179fb8ea39eb`  
		Last Modified: Sat, 27 Jan 2024 20:38:48 GMT  
		Size: 200.8 MB (200819901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1b6e3602be475ff5df204eb8bf83b30e0d0e08a37f14ad2cb0f29d5fc9742732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855a3783344e1aceb5507bdfc40bdec936a2ba50a3a0c55891e9a59b186cc3a`

```dockerfile
```

-	Layers:
	-	`sha256:fae4128886094b364111597edfe3d98bb46793a52b2383f018ddfeb443393d6b`  
		Last Modified: Sat, 27 Jan 2024 20:38:45 GMT  
		Size: 1.9 MB (1914433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78724ab722b7a3afe77d1ab576cda99a0fca72bfc7ec9717c4613ac1c02e89fa`  
		Last Modified: Sat, 27 Jan 2024 20:38:44 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json
