## `openjdk:27-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:7bbe1f1bb8c414c9ee948a26fd08661d838664f7c86301401df8374e17c0d38e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:585dc64d93c21bdad0d425cdd80a64fc56599ead853609f689d6cd41146f39b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314426929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e7b845a2712e5276d9ac7740b0a76b4341bbd14a32575d05c1121d91d59681`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 00:01:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:01:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 14 Apr 2026 00:01:19 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:19 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:01:19 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:01:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:01:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9c8a933a45c56c3a8824b51f9ffb32a97df7275f1256af9f01cabb75891d2d`  
		Last Modified: Tue, 14 Apr 2026 00:01:44 GMT  
		Size: 38.3 MB (38267581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941b47b6e357ba003619da5d3f5a4bc8f815bef1b16ada020902a25674e9588`  
		Last Modified: Tue, 14 Apr 2026 00:01:48 GMT  
		Size: 228.8 MB (228849079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:2f9074afb874b6ac30b65dacedc97a3e4652cc1e1642abe19106e0a35ac0b7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13823570da08e9825eeb05b94d0b9a26668c3aba73a801907932c3075277db91`

```dockerfile
```

-	Layers:
	-	`sha256:ae9176da1b70bbda1e1f1bc231766786190b3e8c78e4ef2a890372557f8ffde1`  
		Last Modified: Tue, 14 Apr 2026 00:01:42 GMT  
		Size: 3.7 MB (3652947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfc3725b158240e7c6fabcb6250456e05117882fce0e0fea6a68ffa74d1562a4`  
		Last Modified: Tue, 14 Apr 2026 00:01:42 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b3aa5b43861f2020a3587636be2a89bc287003247ab7434e15e24ad74259edeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311374798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e89486581fd4ef887b29e93ef34e6b66a1c03f321ff18503a8c1c0ba29e443`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 00:02:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:02:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 14 Apr 2026 00:02:46 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:46 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:02:46 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:02:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:02:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973f139e6d38a8af210bcd5b588347153f44be38863b8d47916fcb2362c029a8`  
		Last Modified: Tue, 14 Apr 2026 00:03:09 GMT  
		Size: 38.7 MB (38668795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1babc6d2875dc0d712b1e6eff850965ee98e54caaa0357e36f22b73a3d0e812`  
		Last Modified: Tue, 14 Apr 2026 00:03:13 GMT  
		Size: 226.8 MB (226808021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:cdd12ec2040344fee7929bf914d7e751d1cd11919883114305bade72283dfb37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3666003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fff7c79006409567a6854a3cf946fecc253b69ecaf94ff57673743f5dfc51cb`

```dockerfile
```

-	Layers:
	-	`sha256:1e09dddf4943c82b5bf5134353dac8659e348d2f62f0aaf2c9b0b4b401d43029`  
		Last Modified: Tue, 14 Apr 2026 00:03:08 GMT  
		Size: 3.7 MB (3650541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:979b78cf278a1641b03a98d0325679f6603b100156a619390ca2211b81317501`  
		Last Modified: Tue, 14 Apr 2026 00:03:07 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
