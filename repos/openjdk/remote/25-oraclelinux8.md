## `openjdk:25-oraclelinux8`

```console
$ docker pull openjdk@sha256:468c937c026098a4832ab7bce4c93744a4f16e03fcddc257d21dff1e7bdc91c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b7cc49f3d0ed5066a96fceeb58c921b6ec08090093e645efc0cb8b76bdc13548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278405259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6536866aa4496ebb63cb5ec0afd4e19b729b900c8d28d957ef2467f3438d1d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 15 Nov 2024 23:04:32 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ec34616a0686adf2a9a8d4c7f2292021c2f1742b75b6a343f9d936f8f95759`  
		Last Modified: Tue, 28 Jan 2025 23:28:31 GMT  
		Size: 15.0 MB (14975039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9346807325624d438c55f0b073e5d7fe301e8b8b8ee1632bd3d8e60582aa955`  
		Last Modified: Tue, 28 Jan 2025 23:28:34 GMT  
		Size: 212.2 MB (212155228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e044b36c2030bd35aee7e2661e460e366c589f3969435a10da53efdfb302f330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed7a11de82ba0eefdc03d24c472a6eeab66fcde03ad6c57cce49bf46c3cfb5`

```dockerfile
```

-	Layers:
	-	`sha256:94eea9cdb3d0e7bf715e05698bb7966590c0e3a475db3af4fe90887dfd33959f`  
		Last Modified: Tue, 28 Jan 2025 23:28:31 GMT  
		Size: 2.4 MB (2440949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aa472cf09f7dac99cdbad2c9a2aacde34056d9a9e841bb5841326c2e2a64cf1`  
		Last Modified: Tue, 28 Jan 2025 23:28:30 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:14a938e6d65a07d798327eeabc80b2f83e882795c8e3e28e3694a6ed00097e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275763399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe50fa494143bf18632bbe5bb38898c6678cd2e410aaba5358980afab07603b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:54 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad1cd9205a89581b21ab3876711618f2acded12b00d2b5d3a9daefffa65ac7c`  
		Last Modified: Wed, 22 Jan 2025 02:31:00 GMT  
		Size: 15.7 MB (15659984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92a6ebc70c08122265c0c963b8f40bade5217bfbc0f745b9dbee80676d570b8`  
		Last Modified: Tue, 28 Jan 2025 23:33:13 GMT  
		Size: 210.1 MB (210123140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:eb41dc2c2811bffda6f11d6db03e58a5d783c6b2040d3ec90d9c30a60dd0b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6509e0362db0464852abbea8849f4788140bf1f3c150114f915dc6310f09eff`

```dockerfile
```

-	Layers:
	-	`sha256:152e041f1de99fd97f9d7bd5f8c94c6fd5857f25dde6f796aa4d7adb4f3f79e2`  
		Last Modified: Tue, 28 Jan 2025 23:33:09 GMT  
		Size: 2.4 MB (2439795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7619dc4b0aa2429050fe1f601d79d91850ad8fc73c5e22e3956f1d97a2a8f39e`  
		Last Modified: Tue, 28 Jan 2025 23:33:09 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
