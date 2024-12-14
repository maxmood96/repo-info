## `openjdk:25-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:dd0857040862dcde0ec171602112c83a5b5e35a5b499868f6d9c2c2d682f0440
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:46c7f85d4d8b29490efc8dbfddd94692cb2bdf1cb5fd8f33f7fd4d89bf887709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310724814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b84c5ef9150a545cee1259f523119ceae970ea80975f013837f5ac037b4fad5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68168330634465979a06abb42a03da6095434a7c4500b34556ab865dd75a0b02`  
		Last Modified: Sat, 14 Dec 2024 00:30:37 GMT  
		Size: 48.8 MB (48765837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdbe96bb63e84f123b1ef0ccbff9c72a72c82bcd467112464b2a4148eef317`  
		Last Modified: Sat, 14 Dec 2024 00:30:42 GMT  
		Size: 212.9 MB (212860275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:0ba5f3167a7621246b49b1f75e9cd05d39113974cc254d2b6da48422ff1ec84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4937371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebbed11c4aa87ea5247fbe194755dbae02e21a122c71f6a1aa124be1be5aa41`

```dockerfile
```

-	Layers:
	-	`sha256:f3f7f8a6eebb62c90c5c37e2ad26993f79b9b97c13597b6e52af3803828c6156`  
		Last Modified: Sat, 14 Dec 2024 00:30:36 GMT  
		Size: 4.9 MB (4917650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44052871e42397fe9ef192f93296b6e1d29a0af79601b9040d007ecc2153cc33`  
		Last Modified: Sat, 14 Dec 2024 00:30:36 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:38b9323efbdc56c79b2850cd1544dfa93c7349ac3ad150a59243bffbc98b72a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307683238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7685c8abfe0e34feda3ab6357a22ceec2744d5b8e00aac3c8a31357bf65ccd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50730d7cdebc9dd971fe547b229ac9b36632531d0634a0903681766460bf2cf8`  
		Last Modified: Tue, 10 Dec 2024 01:26:17 GMT  
		Size: 49.2 MB (49196487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c554b7bffec1cb68851059dae1e0588d73acbb39c88c1a9fd21fdd0a56d610cb`  
		Last Modified: Sat, 14 Dec 2024 00:29:48 GMT  
		Size: 210.8 MB (210819359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:4ed45a520a307e751548e038fb315ad1a43be1e4cbb3995c74a5a956cf6025e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d623494d06263fb29b3dce459b6800f237d949dfc40ff781ea054a1db9d9c983`

```dockerfile
```

-	Layers:
	-	`sha256:e3d754ffbea15eeb15aa5b5b3afde572e69411a92205aaa14574793254061c7b`  
		Last Modified: Sat, 14 Dec 2024 00:29:43 GMT  
		Size: 4.9 MB (4915408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6949e6c442731a479869e27be36954dcc22b0d9563742d2578bebfb936cee319`  
		Last Modified: Sat, 14 Dec 2024 00:29:43 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
