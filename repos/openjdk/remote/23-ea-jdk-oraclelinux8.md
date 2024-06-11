## `openjdk:23-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:3d27539b37c1173b498e19fbef72d0abcd7a7fca6509517950b99c24b805e93d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7054870f0da0a188400d6aa2008a29056153f9e2ee8ce7916ac4e5feb7198847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (277991858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d365bc455943a0a6d3a736e35a314a018981cfd3518b3b7327effe6e25ac20`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:53 GMT
ADD file:6f8c3cf297caf3b2a501a32c94a4fc0d2c7024f63d5e4b2215730b56faa6cdfb in / 
# Fri, 07 Jun 2024 03:48:53 GMT
CMD ["/bin/bash"]
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:427bba466fea4df7396a02ec368c5aa24d07ac80d02aa94eb57ba7af7b84b5a3`  
		Last Modified: Fri, 07 Jun 2024 03:50:01 GMT  
		Size: 51.2 MB (51219315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b25a995ada908598bc8d2171c097e362a00b89c535003df3c5de97d0183fd8`  
		Last Modified: Mon, 10 Jun 2024 22:33:35 GMT  
		Size: 15.0 MB (15035416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdfbf6624fbc829dfee2f7e408053493d9c68fdb23a790e21f0a92cff021052`  
		Last Modified: Mon, 10 Jun 2024 22:33:39 GMT  
		Size: 211.7 MB (211737127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5c0cc53dd2ec05ed2b407b19a5db88c6f90b90d4e4dbd8d47cfb2a3e11ac1b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c4effbea6079dc7ffd014bed5fa0ce369dc8899cf403cf237cf63f9ec45ac5`

```dockerfile
```

-	Layers:
	-	`sha256:0b3b7354e6b155d58814c6e2b32271340fd70b9386b51039dde434964cd073a9`  
		Last Modified: Mon, 10 Jun 2024 22:33:34 GMT  
		Size: 2.3 MB (2267558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df70c08022804b3266653667a9f275b4476008b9d07f13369363dcf7bc784d5`  
		Last Modified: Mon, 10 Jun 2024 22:33:34 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b194137569eb95ceac007c92b2f3477e237408866e82996b8b7a3e3deb30ff32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275225069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fa7997ad670cb7f34468057b801444239c9d1f286a5f83872404304d6e05ff`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:11:59 GMT
ADD file:28329ccaf9d0f8718e6c37965272b9ac3d23fdb6d109ca304f4cdc12c515a2eb in / 
# Fri, 07 Jun 2024 03:11:59 GMT
CMD ["/bin/bash"]
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5522c693c44935bd999ae97ef2649e6707ffdfcf11d7d226a3b78066d03f8ac1`  
		Last Modified: Fri, 07 Jun 2024 03:12:59 GMT  
		Size: 49.9 MB (49926502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224c310d8d2c96f49a742c5059029d51003313d8a587e51fed9a9aedb25695b`  
		Last Modified: Fri, 07 Jun 2024 07:39:04 GMT  
		Size: 15.7 MB (15689949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06b0eb90191fa003aa572cc74cab8801e69088e8a47984fc2bb067757ef6590`  
		Last Modified: Tue, 11 Jun 2024 03:37:30 GMT  
		Size: 209.6 MB (209608618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2fd5b10b9a20c12967b21f9265e72a9a81cf4c5cfc6a12f82409701291370b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb5054da043bb27c00962d34b0c575594fc5316b72bc96a6011c36578ef5ea9`

```dockerfile
```

-	Layers:
	-	`sha256:2128c0ad91ab9e122edde5e1a7bf7f35575400404f739b65dd197186c403ff91`  
		Last Modified: Tue, 11 Jun 2024 03:37:26 GMT  
		Size: 2.3 MB (2267027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1253a2fd4e9c88f90673977739d69ecfb2e7325516032307a23ad6ba3421513`  
		Last Modified: Tue, 11 Jun 2024 03:37:25 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
