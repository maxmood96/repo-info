## `openjdk:27-ea-oracle`

```console
$ docker pull openjdk@sha256:68a7c98fca8de6f365d5566981495ec0eb8ae109d6d5a8ef71cc60604d4eefbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:a8b6e69329feb7614fd5d4b7d54d69dce859e25318254dd90f7fb642cd0128eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313985847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb537604e95672ea3a378d841fdaee8c1aebd4f86507d6fd9a70499de7c56d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Sat, 21 Feb 2026 01:28:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 21 Feb 2026 01:28:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 21 Feb 2026 01:28:38 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:28:38 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:28:38 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:28:38 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:28:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9bd672210818c0c09d6939ec6b7e6ba2ccf3d968391f51fcfeb3c6f1d25379`  
		Last Modified: Sat, 21 Feb 2026 01:29:01 GMT  
		Size: 38.3 MB (38296371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3c388863bce15fb3a9c1a0acd47038c949e0e06fcb56cec112bd139d90f765`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 228.4 MB (228380605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:1bcf43e2c857dfc6a5aa6a3711f96c636eed2ef6056b1a83dffc3ee74e9af9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb3a1384ee8b9b0b93e00fce2da184bb32597f7b0adc68858963f7b80f815de`

```dockerfile
```

-	Layers:
	-	`sha256:5ab77068673b246b6d8630a3d193b8e59d5b6df1689f040b54164a96cacd6ecd`  
		Last Modified: Sat, 21 Feb 2026 01:29:00 GMT  
		Size: 3.7 MB (3655435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda033f5a118409625336a92b40e99951eda8b3857f267925ca8be2cfb3644ce`  
		Last Modified: Sat, 21 Feb 2026 01:28:59 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1a8bbbe4f874c1f959906fc77cc4ad754cb0dcf47da789f427172a4e8614343a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310929206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b4bdac97b2f8e74fc4d08cb20f4cd0bfecf4b5cfc6a63cd10dc40612909ffd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Sat, 21 Feb 2026 01:28:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 21 Feb 2026 01:28:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 21 Feb 2026 01:28:39 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:28:39 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:28:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:28:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8396e6db6b9853e7bf9bec482b6aadd9eea2eea888beec7d439cc8d5476b6fc4`  
		Last Modified: Sat, 21 Feb 2026 01:29:02 GMT  
		Size: 38.7 MB (38693484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f0b5b05b68e6d51eb7cf6f9e2d485ccf5695cf2782eba0a6502e6124d3210f`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 226.3 MB (226333742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5970cf3fb620b21c0df4c2213daa06a8f91dff5926d04ad054a917720d9a1be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec556468ea204a59c3e0f6b382c77ff0e8d676f09d85e368b33351535aec4f1c`

```dockerfile
```

-	Layers:
	-	`sha256:93951b20ab17761be1dc8ec3a60addce6766414cffda0acedadd240b760318f4`  
		Last Modified: Sat, 21 Feb 2026 01:29:00 GMT  
		Size: 3.7 MB (3653125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b444668ecf2896b67c06ecd2f83cd7f1e2bf29cc683ca1a48cac2047f13bd3`  
		Last Modified: Sat, 21 Feb 2026 01:29:00 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
