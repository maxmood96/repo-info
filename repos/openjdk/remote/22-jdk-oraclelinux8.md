## `openjdk:22-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:74de73d5224b41dc6b95cc1ab0dffb03bc06a00f938fa4260459c715c2423c37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:87f6bc4105fb62574cb2979bf1729ceb4efaad979a98a0d1952ccd18f7116265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269096201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8970b9b2c9dd0f91e8b4703bef46bb038769177c593a6763c424324759157efb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Feb 2024 19:48:12 GMT
ADD file:cbc540158e77b85113e3a0e0ed1e202046cf293cdb8d7cd890b04883493dbf35 in / 
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81badc5f380f1ca21f6c430303f4107b9b5e0af27c59e3725bf731915b457fc8`  
		Last Modified: Wed, 14 Feb 2024 01:49:17 GMT  
		Size: 51.3 MB (51325575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6574a4eb4be0630a44c8540c0b61b8c2f758c50a14435558760db8752e9c4b`  
		Last Modified: Wed, 14 Feb 2024 02:55:45 GMT  
		Size: 15.0 MB (15005931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec4fc6868fa9311a9590ec68a117b0751a74e3f0a730b06542dcec6c138fcb2`  
		Last Modified: Wed, 14 Feb 2024 02:55:48 GMT  
		Size: 202.8 MB (202764695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9273d509bdfa40fbdb90a8363d425cadea13689da41cac2447c9d98e2be8bf42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1931979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736e34780635c67d1b341a65725cbc7b0d1914e8d58e751de6dd247f01d9c067`

```dockerfile
```

-	Layers:
	-	`sha256:8f5ed3f15ee453e415bbc5e772576f9fadddab9e5a2fdcaeca859c299919f42b`  
		Last Modified: Wed, 14 Feb 2024 02:55:45 GMT  
		Size: 1.9 MB (1913954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603ef5b4ae50a82575b6ce3ed92e4eb0a04abeb2e0b08ccef93bfd2f1ad48308`  
		Last Modified: Wed, 14 Feb 2024 02:55:45 GMT  
		Size: 18.0 KB (18025 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:87d7f26a9a13430322797e1ddf787f5593ab8dc36d28e7c6dcc0551647000fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266586876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2a04ab388d407ab1ffdaf4ad755bf799056ba06844d69f85a10c6a3e04abdf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Feb 2024 22:04:58 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Tue, 06 Feb 2024 22:04:58 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04d3eef9c8a6237c8b46c9794501777a8ce3c58a2e3a645da53db98f8e028aa`  
		Last Modified: Tue, 06 Feb 2024 23:32:40 GMT  
		Size: 15.7 MB (15691300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76722c4edacd1fd68218c0562411b0ac7c222a22901c1880f4a489b1351fd0c2`  
		Last Modified: Tue, 13 Feb 2024 00:30:03 GMT  
		Size: 200.8 MB (200818152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:94b0ab1977c65de9b8648d11a20d9910c1d0f0e83efd06e5b97e4f84e93a2174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1931360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18df53ba898ee7a49af885505e0dec9a86aa676dedbdb56cc26b3dad3ce6a983`

```dockerfile
```

-	Layers:
	-	`sha256:71ec43d9e73b8601b8ffc6772d36955c21d08b7f602785331589223c77b6f82c`  
		Last Modified: Tue, 13 Feb 2024 00:29:58 GMT  
		Size: 1.9 MB (1913476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c96bf1d42a1bba24cebd4942cf587b9ec746a227f2ada3c873b56b0a93e2cda`  
		Last Modified: Tue, 13 Feb 2024 00:29:58 GMT  
		Size: 17.9 KB (17884 bytes)  
		MIME: application/vnd.in-toto+json
