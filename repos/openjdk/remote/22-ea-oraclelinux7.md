## `openjdk:22-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:5519900bf1e07c401ea04b67c29e27334cdef9ded4efd46d40dff2c0c479b0ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:e427bf0af5a9c38bb329fec16d2e282d06beda5caf6f78b49f3140372afa41b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267374075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b701f0ff8be0f8cdf58eb2b47cb68eaadc14bcd5b1b0817870d5a104a11c77f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Jan 2024 01:48:33 GMT
ADD file:bbd183ec68733730893e5ca4bc8673cc42d54ecec8fc30444474122a66c84dab in / 
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5dd0ec2f99109a7ed9268ac1405fb9951743210620437ec13df10714ebe89b00`  
		Last Modified: Wed, 17 Jan 2024 21:37:41 GMT  
		Size: 50.4 MB (50385815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118336218338e0e6cad2084c8b562be583c184474de1d510e7c7337cab2d0a5`  
		Last Modified: Wed, 17 Jan 2024 22:43:57 GMT  
		Size: 14.2 MB (14232272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d2c29e7e563d474a5b697186572cee875121a3a68fc4aa74e7f0d1987a944`  
		Last Modified: Wed, 17 Jan 2024 22:44:02 GMT  
		Size: 202.8 MB (202755988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:2577616815e51390374586eb30acb018a4ad525dbc6d6d715e2ed128ce90bf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c2abae11fd9c7150e0a96cecb10eb8078c74b13ba028fde9266a2510ee0d50`

```dockerfile
```

-	Layers:
	-	`sha256:7d5bb644fd8c74db568134fc828fcb91f41825fecaa5d07b52405268b0d32ad9`  
		Last Modified: Wed, 17 Jan 2024 22:43:57 GMT  
		Size: 3.8 MB (3768690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2cfc268b1225dafc5125318bccb92518303165a5b89c3e94aa526febf07ed`  
		Last Modified: Wed, 17 Jan 2024 22:43:57 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1f2ac70661e637fe1e08db57340365ae5b6a6aac02f23f8974597d23cfa0c4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267074930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac3be3ef489b4ff49f640307d9cea3cd8a272729097a1e3ba6b95686e21a222`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Jan 2024 01:48:33 GMT
ADD file:8e4f54dbc6703a8208e63085c4e5598de223be1f27406807e223bc6ef121c4cf in / 
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:963289c7c202b6b90d04fa4c851434fe886f6eaf9d3f3cd608dd53d3616791ea`  
		Last Modified: Wed, 17 Jan 2024 22:10:14 GMT  
		Size: 51.0 MB (51000317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385c41166173f9457fc478a9d47f500342a45b6725b38dbcfe193311857a8963`  
		Last Modified: Thu, 18 Jan 2024 10:43:55 GMT  
		Size: 15.3 MB (15257951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1feb1075debbde46d8fd3f136a04e4eee5a0f248219bd4c87fa4c19f81b596`  
		Last Modified: Thu, 18 Jan 2024 10:45:36 GMT  
		Size: 200.8 MB (200816662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:91bc2f0be2912333f15f0c64b78e16f3a5d7755b47e4c719dfbcb6040ad57c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8df6a5d571f5da1bbc47cebe1c716ba387874ad7ca5ce66be5d8d3ed4480bf`

```dockerfile
```

-	Layers:
	-	`sha256:fef136fcb14546d415fb49602e92a280e37cd285d0eb087423a33d815a023171`  
		Last Modified: Thu, 18 Jan 2024 10:45:31 GMT  
		Size: 3.8 MB (3764557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5525e637552152338cf1403a993649ba6ec76a26eac27181bd46fffcbd313f28`  
		Last Modified: Thu, 18 Jan 2024 10:45:31 GMT  
		Size: 16.2 KB (16250 bytes)  
		MIME: application/vnd.in-toto+json
