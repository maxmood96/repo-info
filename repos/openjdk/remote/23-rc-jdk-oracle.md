## `openjdk:23-rc-jdk-oracle`

```console
$ docker pull openjdk@sha256:de33fdf7eb3ccdc75a887142cded3c5ba95393a0d61f11afacfe2aa9fbc89aaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-rc-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:d1fce8ca4e2ebe0a3406014083a4501c72ad15f64275418e9d35638172df6ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299346650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2958f3e9743ed36abc48f29997642dd5f4b7559d1370335bc4975873695509`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Aug 2024 18:48:11 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44805694e07581b2c8c35bdee9920a1ae13cd3da26122a2749414997e140538d`  
		Last Modified: Wed, 21 Aug 2024 01:06:29 GMT  
		Size: 39.0 MB (39046995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81e1d33df5bbed75654448fcb7e3279d0f5b0e7a3d4e94282c2dcc58ccdaed0`  
		Last Modified: Wed, 21 Aug 2024 01:06:31 GMT  
		Size: 211.3 MB (211304834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f214d7de953bc96edae04a0df0d96004e35514c7df8f1dbb01da4fe9bcdde0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e826c3382d57bd7a671914532ed213c70a4a15162839da5f38930e78f264dab`

```dockerfile
```

-	Layers:
	-	`sha256:4cf79149ed59e4c322487b0aa22cab88dbcc97b419edfe8ec62d3335350663d1`  
		Last Modified: Wed, 21 Aug 2024 01:06:28 GMT  
		Size: 3.5 MB (3544045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91bcf60e0d5daa504c178e5a98a82bdd447db9fb0f33d1e6b3801a9b0efc6d76`  
		Last Modified: Wed, 21 Aug 2024 01:06:28 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-rc-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e530e99f16bfeeefad70e59fd91edf0521e27f3f5ed3aebac5d334aad29d883f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296314767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7444311a667c650ec8c1ec50ca8487574ebd63d00fb28bdbbbda705f971c13bf`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Aug 2024 18:48:11 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64a371a7ad1ff13a4dded4febe3bd91f6ddf3dac8b18dc7feef6e025c2943f3`  
		Last Modified: Wed, 21 Aug 2024 01:11:51 GMT  
		Size: 39.5 MB (39478981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e63c6e38e8f08cb924dcba8361c22f53e8ec0712e45259605ea6672f361ea7`  
		Last Modified: Wed, 21 Aug 2024 01:12:47 GMT  
		Size: 209.2 MB (209181220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:1ceb403cafcb6b7bf3e3fbc348a92235ec65828c5a06c7497e9dc7edfcbb844a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c66ea7745b2f841f156e17632afcd18f2b7d136e046a0c86b861af8951ef8d`

```dockerfile
```

-	Layers:
	-	`sha256:4459b296fa52f18bb4370954540d0eb79e8abbdd06a6fb3eef90de9f23c16033`  
		Last Modified: Wed, 21 Aug 2024 01:12:38 GMT  
		Size: 3.5 MB (3542356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cd3810976a94e002eca55f6183a72f02e8a1e4df7911427e2200ca3994a210`  
		Last Modified: Wed, 21 Aug 2024 01:12:38 GMT  
		Size: 18.1 KB (18067 bytes)  
		MIME: application/vnd.in-toto+json
