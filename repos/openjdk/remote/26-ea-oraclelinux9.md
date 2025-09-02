## `openjdk:26-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:dc185726fa454da9c5b711ec516ac873d892954af673ab1f55cf2dc02d10a747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:c85d7e4a9c17b09da7511d646505050dc7211eb40fbf5bfd974c99ba3d2dc546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310683121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8eae1dfbd576738a6976c25494eeca29382947b16b7ff42adbdcdbae2f5f4b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6bfa726944bdde2d3a824591b1bb2c176e79afac3179bc99fb5c0b0f7596c0`  
		Last Modified: Tue, 02 Sep 2025 17:24:43 GMT  
		Size: 38.0 MB (38004417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09033ad10c922f74b3a0005af640ef20c3d3bbc3607b629f53dd4e9ea1814a3`  
		Last Modified: Tue, 02 Sep 2025 18:28:49 GMT  
		Size: 223.2 MB (223181688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:6f8c513d47f7f868fb13965fd823524c55849f63b3240dd9e4dddcf9cadc07db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f849dba6b1544747ac29b9c55316770b1c57794773832db3e342405e0d8fe3`

```dockerfile
```

-	Layers:
	-	`sha256:a77a6ec374b005c2e72bc8071feec8e940d55e611ae4082b4a8593bc913e6b07`  
		Last Modified: Tue, 02 Sep 2025 18:23:53 GMT  
		Size: 3.6 MB (3640729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3004d71fba1f6f30a8fa933d9b4abc3d0a097ed0fd45a496a0217d8980b1b025`  
		Last Modified: Tue, 02 Sep 2025 18:23:54 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d2435216d0d178cdf60e4e3a8965d06c30ebda43b45bc9b2f166881b5da1315a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307538194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bdd38e50e111f1c2d0c346aa7d98805c64e41d294c050e10e6d3d2c1bf3823`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade142e540dfe120fd9911d2c0bb723eebed56196b92ac04851aa01400bf00f1`  
		Last Modified: Tue, 02 Sep 2025 18:22:01 GMT  
		Size: 38.4 MB (38406267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c752317fbbf55bbd525ff7b1ba13cca358cf49f8a01b5f9fd4e7e72535c98104`  
		Last Modified: Tue, 02 Sep 2025 21:53:17 GMT  
		Size: 221.0 MB (221045204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:7c9f982a9f4e7653e335e52b2438d10e8f73dda9bdeda91016d700f4b6e78e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67f6d3ad4e74efd86dbc7bb2ac8a7a54c02536cae956cfb61f668456a6e9e36`

```dockerfile
```

-	Layers:
	-	`sha256:6fd50d1510cd2a80e6688f55e841dce0c00350f938725f63dc998d72d613433c`  
		Last Modified: Tue, 02 Sep 2025 21:23:52 GMT  
		Size: 3.6 MB (3638491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71c73c23be370b1bbb0d5a2f2c3be0fa473b6c8d4aba5db9b300fba0c490a6a`  
		Last Modified: Tue, 02 Sep 2025 21:23:54 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
