## `openjdk:27-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:0e0245daf04daa20b31e50a65d5a49f2200c9d2ce8f6791207ebb8c517fb0f9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ebbb0b2f40c2aec7f9483904652b5029cd2ed9f43a357b4c4af279319a3a2dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295291432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe13e6cffe06ae7103e7e5b37d7136f2673cec1760ed267f93f66f34ff384f0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:50 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:50 GMT
CMD ["/bin/bash"]
# Sat, 21 Feb 2026 01:28:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 21 Feb 2026 01:28:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 21 Feb 2026 01:28:58 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:28:58 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:28:58 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:28:58 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:28:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df558405081e8d5c6af13745e322e2d270802ff99fe9a1eea2b63615844efa1a`  
		Last Modified: Tue, 10 Feb 2026 23:03:01 GMT  
		Size: 51.5 MB (51464982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ce5ecb3c03c2e487f51b3c3ad2ae4863a21e485808bff610dba83612327a46`  
		Last Modified: Sat, 21 Feb 2026 01:29:17 GMT  
		Size: 15.0 MB (14991574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a085c12e9715a3baa19b378c6339da63f8d4d93b4a4ef92ef3bccab29438fc0`  
		Last Modified: Sat, 21 Feb 2026 01:29:22 GMT  
		Size: 228.8 MB (228834876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b05ad7ac97baaf859e14e6512b62aadd2bebedb55d16c7a88278e525792efcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df7ff8798279296e59d47e70bb9e18f4a9aae8c90e26635ff7b84ace0b65351`

```dockerfile
```

-	Layers:
	-	`sha256:a48029de7e43b3584bccd993162d440788554469566bee53a3c0299da4c7f4d3`  
		Last Modified: Sat, 21 Feb 2026 01:29:16 GMT  
		Size: 2.4 MB (2448700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01a8e0f75e179efdf46672415c00c7170e93d3ae01a6ad23791c49b457409b10`  
		Last Modified: Sat, 21 Feb 2026 01:29:16 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c0453d1cef3dd2dd4f9e279fc912cc57c2331eb56f3268d93850e458120be705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292696130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41265776435ce1e0a4b3d40d82022bdd29c65a4f5f91214cbb7a05e0b3b65e39`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:07 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:07 GMT
CMD ["/bin/bash"]
# Sat, 21 Feb 2026 01:29:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 21 Feb 2026 01:29:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 21 Feb 2026 01:29:23 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:29:23 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:29:23 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:29:23 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:29:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07a1effc9605f90c3e2f6e8e5b85d7de94a80b436a975fd605cfe7f53acd6ca5`  
		Last Modified: Tue, 10 Feb 2026 23:02:19 GMT  
		Size: 50.2 MB (50191339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd2a5f3fe1d669a26f15123fc518a01680898c3d6f09d72a055a3cce0f08022`  
		Last Modified: Sat, 21 Feb 2026 01:29:45 GMT  
		Size: 15.7 MB (15690735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8ee43d0b852e3d986ad6ea410c8095c6c52f5ddd905e46327e39a6fecac35f`  
		Last Modified: Sat, 21 Feb 2026 01:29:50 GMT  
		Size: 226.8 MB (226814056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ffea5c110b27c9e7ba7ade742fdba08832e08da49c289b81e88c76916d58616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010032a5f18a84fd9e128f1fef45160b9f377597307863459a86e0811961bc52`

```dockerfile
```

-	Layers:
	-	`sha256:7b26c8b583a8ef85a85f5e7c017ef87bf07a3a4086f03278d2ee40e4631747d1`  
		Last Modified: Sat, 21 Feb 2026 01:29:45 GMT  
		Size: 2.4 MB (2447510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b99bbd12cca5cfe08e9dfa5837f4cfff5e453e187809f8d68999d2394ed87899`  
		Last Modified: Sat, 21 Feb 2026 01:29:44 GMT  
		Size: 15.5 KB (15460 bytes)  
		MIME: application/vnd.in-toto+json
