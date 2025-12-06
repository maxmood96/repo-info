## `openjdk:27-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:b22ddf151b7e977b89109669c80a1e5088dfef60f9736cb862f5dc1f53605029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:e40a64cdc763f6e987295375c9ca3092e7754edd7abc2f7f09fbf85921506d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313494419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bec637e7996081ccd489416bfc4c84f8581c7f77f7cf696b65ce63a150513e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:35:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:36:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 06 Dec 2025 00:36:06 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:36:06 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:36:06 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:36:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:36:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766cbc67f5bb9ce37e8c4926095f057824965a6e139b4591e6cfc02e5014c591`  
		Last Modified: Sat, 06 Dec 2025 00:36:42 GMT  
		Size: 38.3 MB (38297697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00aae1514b26cdd1c009890ad7f837eae97744798f19e6b617f607898a445c67`  
		Last Modified: Sat, 06 Dec 2025 00:37:58 GMT  
		Size: 227.9 MB (227881974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:724c9095d89d4e9d63b6519947b8031591037ffe6b761e2dec1bd884ab3fe8c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282695180d16e7edf27c0bc5e7b403dd6f774a875c576606d20a93bbadcd54b7`

```dockerfile
```

-	Layers:
	-	`sha256:c6390c201238763bb7b65866df208d7f65de744c975fb9101657b47cd63eb4d5`  
		Last Modified: Sat, 06 Dec 2025 01:26:02 GMT  
		Size: 3.7 MB (3655311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e691db148ca9131f330b41fe6d423005129c6b4c9a8d511f51443f07b2d4994`  
		Last Modified: Sat, 06 Dec 2025 01:26:03 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0d1eeb3ee1f9eee9707f22f9b205f28da68e4b16acf51fd307758bf1a3e5be4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310390968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dc191b72b5411db8203aef0b4523b0c57df29ed0c8be7976721e9df90036ab`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:33:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:34:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 06 Dec 2025 00:34:18 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:34:18 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:34:18 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:34:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:34:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c02781e6cdec0c19e71a9ab30def63957e34ef0700cbb69e547dc083fe59ea4`  
		Last Modified: Sat, 06 Dec 2025 00:35:06 GMT  
		Size: 38.7 MB (38700425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2eee8e3187dae9fde6620170b719f2de767aaaf177d26371180899a7157b9e`  
		Last Modified: Sat, 06 Dec 2025 00:37:52 GMT  
		Size: 225.8 MB (225793511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:e42320fd91030d9df7b339a0d6019a7a263c0492cf715ce001682b64bdde9203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b995d368097b51e526ba36286c6c4a14c8145a14804a1c4e1914f451fefd0`

```dockerfile
```

-	Layers:
	-	`sha256:7271a53405ec27e0338c980cff116a3513961f4a172946c697b8ed9cf9eea0f4`  
		Last Modified: Sat, 06 Dec 2025 01:26:07 GMT  
		Size: 3.7 MB (3653001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6681105316bc0f415d00656d4b0ccaa6f69a4f1962fe1fb7e29a3efb7b55b45`  
		Last Modified: Sat, 06 Dec 2025 01:26:07 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
