## `openjdk:27-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:72edaa2a0f19e66c2a46734a4b9dd6dd0e54e176f397439e42374d9b6bd88e03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:dc05a79018e1001e534235281402d6516656a8483d4b245e382bb5d7bbcf4efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294720937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5063597206648279e398dba6cdcea6fdb5b6c01c6afdba5e3368facaf0ff8c67`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:50:37 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:50:37 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:36:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:36:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 06 Dec 2025 00:36:23 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:36:23 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:36:23 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:36:23 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:36:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b436d89f13c92f9703618820d992b4e1f2b38ba243024b251c81a610f04c67b1`  
		Last Modified: Tue, 25 Nov 2025 23:51:01 GMT  
		Size: 51.4 MB (51378078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f40875005821869ff19e4ae00ae2a2782fc1d8a71906189b46225e664aa638`  
		Last Modified: Sat, 06 Dec 2025 00:37:00 GMT  
		Size: 15.0 MB (14999378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c26591d486c9e0a06a330649fe7354e6864c60204321316a8aa52e6fd3c56a9`  
		Last Modified: Sat, 06 Dec 2025 00:37:01 GMT  
		Size: 228.3 MB (228343481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ac55c13e48cd4571bfa454278ae0983b00c29f9154c43f729ec9485937eb172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ca638f5284b19fc95bbf6a773e8605ba482c0c1e46159d24343a3ca25d0a34`

```dockerfile
```

-	Layers:
	-	`sha256:fd00fd8d49f204f6fa308e2412ae12045b34a35bc3e9daf984da914b0730bb29`  
		Last Modified: Sat, 06 Dec 2025 01:26:33 GMT  
		Size: 2.4 MB (2448001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71f5fedc0b139f692fe1e19296f61d99de6ef606204652bdc7fb4c0434a5ce6`  
		Last Modified: Sat, 06 Dec 2025 01:26:34 GMT  
		Size: 15.3 KB (15325 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bdd42f42208582eed1332e550c0b492a47312b924f7dea19e5c87c29749a31b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292064015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0168b386157bac18189427d133faf2a61788dc9e6a509dc5aeb477cf350a06c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:37:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:37:54 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:36:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:36:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 06 Dec 2025 00:36:22 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:36:22 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:36:22 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:36:22 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:36:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:674388ef21c06396c4d40407ba2af1c3a42c30a5cb162fd4355950be7600edf7`  
		Last Modified: Tue, 25 Nov 2025 23:38:20 GMT  
		Size: 50.1 MB (50103076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0ed787b9ca556e2c3c3fa5dde9ea5a9e0c5f38a71efd36efc20cef33e55b5f`  
		Last Modified: Sat, 06 Dec 2025 00:37:00 GMT  
		Size: 15.7 MB (15691589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e97e4711dc57bae254fce3d94c372dca1837e0c39cbe916f00254fd4b1309de`  
		Last Modified: Sat, 06 Dec 2025 00:37:28 GMT  
		Size: 226.3 MB (226269350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5c465487d4aef991694b9d756fb8a6ef49045e3f6cd5a975ee424e4fc5905c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f55867c69a3665ec86bb095cceb5f6e7350f7f622022655f23b84e3409c5f5d`

```dockerfile
```

-	Layers:
	-	`sha256:1146341b3a1ead0c493d63e685782a9d773ce8b45347a02cf9005e2e46b0c14d`  
		Last Modified: Sat, 06 Dec 2025 01:26:38 GMT  
		Size: 2.4 MB (2446811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6d2a7d8ab733e5b8af4b76bcac31b132da2d0de12bc7e11d91192cabe95ab2`  
		Last Modified: Sat, 06 Dec 2025 01:26:39 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
