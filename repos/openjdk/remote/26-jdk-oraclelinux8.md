## `openjdk:26-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:a3c1ceee30cdfc604153f8a4a6d776be35171b61c5def3bf1f96195dcde4baee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7a19d429c6575b906aad2907cd8579a7033637b4bea2d6dfbdab075f40f3c503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292427890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1333f42a41c890129e0289c78cadc04b9d7b98da56f606e1fb9c7d066e1b37cb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66700e2b18e01c0550984729a0cbc6c7137d4f5489a563e0fe17c014042a3f6d`  
		Last Modified: Mon, 06 Oct 2025 21:05:30 GMT  
		Size: 15.0 MB (14979318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270e1f494740626563ccae0cc342381da710e8427d48e698295ea4d81f9ff8c5`  
		Last Modified: Mon, 06 Oct 2025 21:53:04 GMT  
		Size: 226.1 MB (226125009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2ef34c04c6baa6797b2be8328dc8a554f165a2bba291a78be97638daf8e39b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fc685a82a04057d93b22a386057bed20df67bf059cd892098c5f489498eab9`

```dockerfile
```

-	Layers:
	-	`sha256:00ba45374ba87e3fdb65d2af010f2d541e0342e2f23ab5c71ff6b03e0b7c668e`  
		Last Modified: Mon, 06 Oct 2025 21:23:52 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77fdf486d0e7bf8b511aba42626882e148d011fd53ddd700ae358416aa91eff`  
		Last Modified: Mon, 06 Oct 2025 21:23:53 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c6f3ec9000bee0e12767aa857dcbbadf058229f22a1d56cf9857396dec1bcc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289724974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0357256a8a9b8d186f06e38c9b44e36784d4c178b5d411884f046fa4b4e33522`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 11 Oct 2025 00:48:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e02731574931ec9bdc32dd8c8318f7852e7941a5505a71857b506b382a97f7e9`  
		Last Modified: Mon, 13 Oct 2025 18:13:14 GMT  
		Size: 50.0 MB (50041880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e752ea6dd57e0a38431dd5e3daca8753f903c06706fa3e36843d8dd2001cf81d`  
		Last Modified: Mon, 13 Oct 2025 18:20:11 GMT  
		Size: 15.7 MB (15659314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80edc187a20cec1ebb639d80bcad40a360fcab08a835d85799051b1bffb5b61`  
		Last Modified: Mon, 13 Oct 2025 18:19:47 GMT  
		Size: 224.0 MB (224023780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b09747b573cd170ad1166d36991eaacbd9fffb34866882b052fccd5026c5ca56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02f44114bf7a9208f9809f97b44599e3b6ebe34a42e77d657a40953c669113f`

```dockerfile
```

-	Layers:
	-	`sha256:72811d52399de227981aba7e783793b960909ffaac82fdb802012d09e0212da8`  
		Last Modified: Mon, 13 Oct 2025 21:24:02 GMT  
		Size: 2.4 MB (2449951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135b138cd682c80181ff90e9412e59c364eae9df8fedc9da165f2f558f5b4dd8`  
		Last Modified: Mon, 13 Oct 2025 21:24:03 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
