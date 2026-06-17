## `openjdk:28-ea-oracle`

```console
$ docker pull openjdk@sha256:b68997054d34dce5b333392a907c28966e986bc1133a226a6679d4c86ecc6e25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:1d91a309dab2c08cd25b015212f978fb387efcacfadf0f6b8cb347646c00cd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308149792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1970dcfafdaa6ac12cfc712f972c7772276b84b4c1612bc9f638f2f6daef26`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:32:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:32:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Tue, 16 Jun 2026 23:32:20 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:20 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:20 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896404133cc1e382d6b3c749ab5b7f2ba53faaed86d789cc099c1fc48a98c725`  
		Last Modified: Tue, 16 Jun 2026 23:32:43 GMT  
		Size: 37.7 MB (37687683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c48ecad05c3698573cf45bb0426cace8803fad1388f63cf0d096454db4e679`  
		Last Modified: Tue, 16 Jun 2026 23:32:47 GMT  
		Size: 227.4 MB (227381527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6c1e28f1fcc46746407897c35a10d238da1f3283aa8e8caa56d7508a3e8548ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6aa19f231352f0780ef92cd5e3a6e9fb820a39b2f22c57bf3648cc9c908e13`

```dockerfile
```

-	Layers:
	-	`sha256:febfa027699384967e7c9242c97f0e187026fe91c31e44cf7cbe1d7fda2562c1`  
		Last Modified: Tue, 16 Jun 2026 23:32:42 GMT  
		Size: 2.4 MB (2366444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ace043fc3ca832a95b57cf2509af082cd05016ec409a09be6cbccaf13567856`  
		Last Modified: Tue, 16 Jun 2026 23:32:41 GMT  
		Size: 17.8 KB (17829 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3be5106ce185a22862756bc04da3db2f10173252d02354f09b63cc74dc9ee5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304597127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7d898a97746ed02243ea830f554d094227f93967898b03e5c8c3564e128fab`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:31:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:32:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Tue, 16 Jun 2026 23:32:13 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:13 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27f3d34c927e746b9b26a64a66424b63c02c12f7b4501bc1455ed826c88775e`  
		Last Modified: Tue, 16 Jun 2026 23:32:36 GMT  
		Size: 37.7 MB (37696036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe45583bf226847dc4e146c13ed42fe86919241985db802d4c5ac6077e55a4e`  
		Last Modified: Tue, 16 Jun 2026 23:32:39 GMT  
		Size: 225.4 MB (225405396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b53d3305e096754989d92c74d26290ef2f7fa2f9694c8636a596a283be5ae9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe84954b1e6043b6af15c4a75f4bd0d8f6ac6749a64738f31f1d96dcc1455a57`

```dockerfile
```

-	Layers:
	-	`sha256:5ff2908729e0193841071a0ee6a76f2718e86163865c84354c3b8d76707c0fd5`  
		Last Modified: Tue, 16 Jun 2026 23:32:35 GMT  
		Size: 2.4 MB (2365972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1732fb09382745910e933ac7fdd5e54ad324857b81efd52d9a44f48957a448d1`  
		Last Modified: Tue, 16 Jun 2026 23:32:34 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json
