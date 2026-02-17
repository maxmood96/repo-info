## `openjdk:27-ea-oracle`

```console
$ docker pull openjdk@sha256:62ca52daa2382031751fea41cf7d1e776c67224b6aa856a697454054194cc3c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:8db61366096922d549d6688fed8c56819a09fab35f2d6f073b83be60e10a698e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313975705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bbebbcb986b563c49948123ca8a496747922c850df49d16409286297d110c5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 19:32:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 17 Feb 2026 19:32:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 17 Feb 2026 19:32:21 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:32:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:32:21 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:32:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:32:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296838985401ed2f4d62f8613c39f49db0400fc1ea3e53dd1061c7f545b35c6f`  
		Last Modified: Tue, 17 Feb 2026 19:32:43 GMT  
		Size: 38.3 MB (38300024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330123bab50165a496fcf4439bdb8de0752cc46cc49e3547502e6ea1ce67671b`  
		Last Modified: Tue, 17 Feb 2026 19:32:47 GMT  
		Size: 228.4 MB (228368139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:179f3de9406defbd45dd76af3761c4ea78030b029b6082cc3da63c3b293b8090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a652704fd701cbfbdb5b4a6c3c006ba8e1ba01411667e016fb4d4d54b83a708`

```dockerfile
```

-	Layers:
	-	`sha256:a8a441b6ab6a16fd731c19a478f4c75770b49de5c6c821849cfca3f895d88a7e`  
		Last Modified: Tue, 17 Feb 2026 19:32:42 GMT  
		Size: 3.7 MB (3655411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e69a65c69ade61a45dd48a52094f3ff415253e0972781887231e0a66822bf19`  
		Last Modified: Tue, 17 Feb 2026 19:32:42 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d99e1f56982cb7f7f5f2ebdf3d8732e767df98cfc572e72028a5bda23426e678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310913923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d1abef27804c76c3bb474cec56395714e8919c54a60928c1c235cc5c67199b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 19:31:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 17 Feb 2026 19:31:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 17 Feb 2026 19:31:21 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:31:21 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:31:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:31:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a8b592ead8fe418afa8a35c4541e63d9906fce6a1ecf80cc908378035adee2`  
		Last Modified: Tue, 17 Feb 2026 19:31:44 GMT  
		Size: 38.7 MB (38697313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074b8554ce3381af8fae803ec357f821d6f2eaa57653aed3aa256257f947277`  
		Last Modified: Tue, 17 Feb 2026 19:31:47 GMT  
		Size: 226.3 MB (226313200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:867c38c16ce9e8e4d8660994bfd7ea15226f6a82a514de74a839a327c75cb210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1db1439e1d1b15ca3b01192d1b056d52e80c74acf28986ad5f8400ce253f80`

```dockerfile
```

-	Layers:
	-	`sha256:f8eb6f5a4e5901da17894fdf84d16b11d66781c0feaa9c5d9a388ee4937c3324`  
		Last Modified: Tue, 17 Feb 2026 19:31:42 GMT  
		Size: 3.7 MB (3653101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b26964b448d0ae9adcce25e9c6ff49dacf66987c10ede5401028870c5717dbe`  
		Last Modified: Tue, 17 Feb 2026 19:31:42 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
