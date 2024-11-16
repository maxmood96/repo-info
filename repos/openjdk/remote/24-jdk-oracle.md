## `openjdk:24-jdk-oracle`

```console
$ docker pull openjdk@sha256:8af6e4c421f833067c1ffcb2eba473b20aab6520b0f26b14b88a4f02b1981c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:3eee0799644397d94d8b24e50c4b045f5a2b9fd025dffd63fb306af897526f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310370619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c03ffcc26fb51bbd1a4d15127c4806982bb4c06aaa452a24bde00dccbae480`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 06 Nov 2024 16:23:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 06 Nov 2024 16:23:18 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faecf1dc429eb2f533abc3954faf4feb0d52697a438dee641a870f62d7d3e6c`  
		Last Modified: Fri, 15 Nov 2024 23:05:07 GMT  
		Size: 39.1 MB (39050410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3311fb8191835db40810f9a06d08298302e92a0babc4433b781d94375b5b44dd`  
		Last Modified: Fri, 15 Nov 2024 23:05:11 GMT  
		Size: 222.1 MB (222102150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:4d524393cf2d69b5b9b5e30963864ad12bdab8395b065488781c364a7538ab90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3820060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64efbce0abb3e3a30b336e39cbe7159ad4fb4b1aeceb4342b37966da981151c7`

```dockerfile
```

-	Layers:
	-	`sha256:351be862e5539dcc4534860ce233f13951ed031cd70c63a846cb2aa31cde36ec`  
		Last Modified: Fri, 15 Nov 2024 23:05:06 GMT  
		Size: 3.8 MB (3800315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08714b3a55d94a711e00f02090b6dd014de2a67a838c77ba4748cde7b6142d09`  
		Last Modified: Fri, 15 Nov 2024 23:05:06 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:24c1647f2362b15c6883384717a3f9dcd2ac5009bd4c5db7bcb8720f622069c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307426191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b5432a60894d733c254931c248e484a81e9295ff4892656f540f1f370132fd`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 06 Nov 2024 16:24:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 06 Nov 2024 16:24:10 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6462210e2d7b7d2ea30c30358ab0d739cc495b4de8d2eca0563575ff695ced2`  
		Last Modified: Wed, 06 Nov 2024 20:56:40 GMT  
		Size: 39.5 MB (39482424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023cde86e525ed3962dc9e5c2e211b3b524b26c6d68199e525954641ab0ee4ba`  
		Last Modified: Fri, 15 Nov 2024 23:09:55 GMT  
		Size: 220.1 MB (220052069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:bfa9babca8d0f4d0776246bdc727042f76500f6624fee1de00795473e26779ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6fa2b7454cd0736e227fe91b271d94953d132f9d49a5cc39aa904cbee8a6a0`

```dockerfile
```

-	Layers:
	-	`sha256:3299112a65cc206b221a38061c0851557028643d91115fa7b46a74617b0c41ae`  
		Last Modified: Fri, 15 Nov 2024 23:09:51 GMT  
		Size: 3.8 MB (3798073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ecf1fb3c7f56abfa1235e853f21a1ece009ecc00ad46132f9668259b326e27`  
		Last Modified: Fri, 15 Nov 2024 23:09:50 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
