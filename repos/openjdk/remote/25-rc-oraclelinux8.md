## `openjdk:25-rc-oraclelinux8`

```console
$ docker pull openjdk@sha256:5c79221451e3790f871539c6d5fa5c98cbcdf0d2054f2cdea6b513d478cbf7ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-rc-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c1647b67c2cbd300d8dc5611eedcd6a57c7088ef778136645a0ee987ad8de010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289831702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09258101817f62efc66e5ed310b4fb0f7444129cfeffab5db4cdf0380e2b1874`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Aug 2025 00:48:25 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8594c04af449ca62935e69e4d836465fc70e191e73c55e9bb0d2ce12b8a09`  
		Last Modified: Thu, 21 Aug 2025 19:09:48 GMT  
		Size: 15.0 MB (14976984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00069efeda640550943fe97734a9afbf5fb5805822ac859877d38d0054273808`  
		Last Modified: Thu, 21 Aug 2025 19:09:28 GMT  
		Size: 223.5 MB (223531155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c9a42a770777ef94a7c9ca8fdcb942fc10f29ac1e3e1935872bf5818b8183be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3852a73a1a25f4d96ddd3ba9521dddef234561d9f78215810b3611bd6f86fc7b`

```dockerfile
```

-	Layers:
	-	`sha256:2a02b0438a0b01bedfb7bb85773b31511faaa5656e033bf5cee572c3bd4dce14`  
		Last Modified: Thu, 21 Aug 2025 21:23:32 GMT  
		Size: 2.5 MB (2451048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af88b8312b547f87a99566c45c38d59d9c2f892a1d6516ea3407de78e62d97e6`  
		Last Modified: Thu, 21 Aug 2025 21:23:32 GMT  
		Size: 15.4 KB (15434 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e82fed4a5744f30fe9cad81399c325a9d44e7f2871bca73e033ff8efa4fd0704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287053850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11efa5a0da679a69b3394ca59778fc06710f0b7e625dfc61e3ab404e5fb6e5e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Aug 2025 00:48:25 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9866c68be293aa81b529074549b7f38395dba71a8ea8fc528f721fbf8543b957`  
		Last Modified: Thu, 21 Aug 2025 18:57:24 GMT  
		Size: 50.0 MB (50039817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a01811484fdc87c21c7358e9f38ab4c42443d4a91eff20c2aa855940ad8b39a`  
		Last Modified: Thu, 21 Aug 2025 20:17:11 GMT  
		Size: 15.7 MB (15672244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805cf5c9abb10190aa65112d559e810b54cb00296f47295be1532fcdcc60f0ad`  
		Last Modified: Thu, 21 Aug 2025 20:18:21 GMT  
		Size: 221.3 MB (221341789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:377d20a652a14718f71e9798f39184e5c359460f5dcd25f3ae19965afd375804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078e5f900963492c58e8dccbb809f9cfdfb182e5175965f638ef229dca5b25b6`

```dockerfile
```

-	Layers:
	-	`sha256:2566003449a1bc27460bbaaa0ebb90e8f6ea7bb7e2103a3cd1775c2f8d33055e`  
		Last Modified: Thu, 21 Aug 2025 21:23:37 GMT  
		Size: 2.4 MB (2449858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43756c5c30b261eb0b5c12cda1ae48eb5af6ffddc36e5b7b3086710c79589c4e`  
		Last Modified: Thu, 21 Aug 2025 21:23:38 GMT  
		Size: 15.6 KB (15552 bytes)  
		MIME: application/vnd.in-toto+json
