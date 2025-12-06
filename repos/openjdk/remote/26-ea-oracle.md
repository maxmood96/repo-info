## `openjdk:26-ea-oracle`

```console
$ docker pull openjdk@sha256:40e6b02eaa1b6b8eaaf1bf55f7e621af349dd643422ca306270bc84a2ca44289
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:7803308aedc53372df7c8cecee2d6ede9482d4cc8af96aeb59ff2a079f02b728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313430828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8666b31dfea20b99dd84bbc30cc919f34ff9fee6b8f1ea37c6f3a6feb0ecb75`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:33:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:33:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Dec 2025 00:33:55 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:33:55 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:33:55 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:33:55 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:33:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4ff58ab1572230750b4a7fb82dbb75c767faa983eb2b1a4d6af78c78a6271`  
		Last Modified: Sat, 06 Dec 2025 00:34:41 GMT  
		Size: 38.3 MB (38298004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c2ecb57ff10f1e0cdbab7155c062e99458befe51b1408e7b91390cffb84041`  
		Last Modified: Sat, 06 Dec 2025 00:36:08 GMT  
		Size: 227.8 MB (227818076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e84a8d95ecd11ae992f56fc72e754b100a25b25af18d2aa5829146aa38c913c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f1b4e5a198ddc627dd839e302205512f324518b6fed4623ef28ca5be1a7e5c`

```dockerfile
```

-	Layers:
	-	`sha256:4c9e2f716df8d0fadbe87849add970f2646fc7f5b94b6bc93e8576bed3b6df2b`  
		Last Modified: Sat, 06 Dec 2025 01:23:32 GMT  
		Size: 3.7 MB (3655331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbc3668237ef6bbafa8aa107c8b87035c5c77661abba690b02872a5b395705e0`  
		Last Modified: Sat, 06 Dec 2025 01:23:33 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7c1dd0a94111750f906beb74cbb825bce07cb161e2f06f567383c376aed1f69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310332373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b11da68091eca3fbf8d27b0a34e8e86152e1f017a04e8d33da12fb4402dab6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:34:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:35:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Dec 2025 00:35:07 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:07 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:07 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:35:07 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8090318bfe3ef046daf7ec1e15088d12210fd6439a6ea2487afcfe38cd22f7c3`  
		Last Modified: Sat, 06 Dec 2025 00:35:43 GMT  
		Size: 38.7 MB (38700224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921ee30cbbd1ade4361d00a0bb9a1d54ce6d2635e9b602db7412792acf6e7217`  
		Last Modified: Sat, 06 Dec 2025 00:37:42 GMT  
		Size: 225.7 MB (225735117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5618cab5a33beb8194ccf6408189aeb0dc258dd68eb6eb6240a2456d11069fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daaa861c4352a655da4ad9fd7f82cbb2168ad6c051782c9ec25b4e6446261e3a`

```dockerfile
```

-	Layers:
	-	`sha256:5dac55075565d376b2d9dd92da6b22c536b8bf3d6ed62ba7ad1d0552dcde7f23`  
		Last Modified: Sat, 06 Dec 2025 01:23:37 GMT  
		Size: 3.7 MB (3653021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a3e517e38d008e0837d60e65dbcf8784abd5eefc36985eff517867919ed6dd`  
		Last Modified: Sat, 06 Dec 2025 01:23:38 GMT  
		Size: 18.1 KB (18053 bytes)  
		MIME: application/vnd.in-toto+json
