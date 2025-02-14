## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:f6734479d8671e222995836a9cd2db13b1ac7f2bd75ca5fccc9bfa0066043637
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f72b9cf1467b4c62b4ec39e070d0cbf4aeeb4f0a7b5ba242842dfed40216999e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279555486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f86869fc33535eebffdd462ac5f010f150b14d941a912a5b304312eaac582b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:50bd714b8e38d1a822db5498f9fe090cf204274713557d5f5437e40188ac4303`  
		Last Modified: Fri, 14 Feb 2025 01:27:41 GMT  
		Size: 51.3 MB (51283059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dae045c797c2cda0f6233dda51820efa418629b7903bb3c6de463c71b24a94`  
		Last Modified: Fri, 14 Feb 2025 05:09:31 GMT  
		Size: 15.0 MB (14978966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0fb9388a619f05a0ae88884632182b934156eb1f298e7b054324cbc2b0883c`  
		Last Modified: Fri, 14 Feb 2025 05:09:44 GMT  
		Size: 213.3 MB (213293461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a008ec1a2b7755c04fda620d9fc28560790842380f83cc69c4e04de26bc7bd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f1432a05e4da62693471739df58060b8b471ed9cda7fe540d255bac369f218`

```dockerfile
```

-	Layers:
	-	`sha256:d27cf10f10965ae758521347df78f231f1e6dbed419a70d37cb979cc69ea26ef`  
		Last Modified: Fri, 14 Feb 2025 04:23:21 GMT  
		Size: 2.4 MB (2444671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53984f507ee1fff284221380604f9581474ff8e11209a4ffe4f56f5edcc4ca45`  
		Last Modified: Fri, 14 Feb 2025 04:23:21 GMT  
		Size: 15.4 KB (15434 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:aa586c49b720525bd3e81023dbc1c5a6bea4bea59ad48065b8ed9688338b986b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276930810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35032f8590a2a1459e4bbedba0268ea6fde67b05777cafd1d4f7962afe7438f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e8ec99a1e85147c24be8e8ee35b17a7fa5f9a2c30701932a58ae62802e80c54`  
		Last Modified: Fri, 14 Feb 2025 04:52:34 GMT  
		Size: 50.0 MB (49989289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d2291ce00cd6bc0d3bd9e3183640619c1993d713063dbe8f6430762533fbdb`  
		Last Modified: Fri, 14 Feb 2025 04:22:36 GMT  
		Size: 15.7 MB (15675007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40acf5ec5ed8647ec400eef8cb56d5e3442f07f7834074cfdd59d25f4b4b2136`  
		Last Modified: Fri, 14 Feb 2025 04:23:28 GMT  
		Size: 211.3 MB (211266514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2146afcbd431e067cbe7c4a23971f68b6b1113317e502c0c66289586dff692b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4b7614aae9249493b306b85116e30d6d5b0bdc2654fc2c672764d0d3cb66a2`

```dockerfile
```

-	Layers:
	-	`sha256:a004a7f4b57a6695abd4a7889b8617a82d063e44c1a4e9f503cdd48d858e0b7f`  
		Last Modified: Fri, 14 Feb 2025 07:23:22 GMT  
		Size: 2.4 MB (2443493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:817dfc1f487396ee8145c8b01949028bdfd2b26495dd55c69e60ccb9e6c010aa`  
		Last Modified: Fri, 14 Feb 2025 07:23:23 GMT  
		Size: 15.6 KB (15551 bytes)  
		MIME: application/vnd.in-toto+json
