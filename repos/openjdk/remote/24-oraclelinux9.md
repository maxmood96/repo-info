## `openjdk:24-oraclelinux9`

```console
$ docker pull openjdk@sha256:07bdcf70d0053fc9c728d897451bfb4ce4f7ee0b4af5b8e2be9304d3ea5bda4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:7608a0a78acbc5602a991e9ef6dbe186b6adb27f9a4977f58e2feaa1d201619e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310705208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90bec810e1c80c14cee80d53c86e87a76d99651909dd7a2398e28046bdd8412`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Feb 2025 19:48:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c46ec965fc0d0493229ac200d2975b7c89fa91892ea0f2a83327878381a32e`  
		Last Modified: Wed, 05 Feb 2025 21:08:50 GMT  
		Size: 48.8 MB (48767695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a653d7c72fd91d9241eade741ac19fca245803f40f557e73aad38fab842146ad`  
		Last Modified: Wed, 05 Feb 2025 21:08:52 GMT  
		Size: 212.8 MB (212840210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:78bcd58a5793a146ac20d10d14160afbd2a4ff5a780adec8320ef952a03525f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9ba1ebc18152a4ffbfc28f1382c0283f2c7d4ab78b0c68aebf043c376fa604`

```dockerfile
```

-	Layers:
	-	`sha256:61456936950abffae6809e3644a6af9489564603ba15649a2e5084fd25204891`  
		Last Modified: Wed, 05 Feb 2025 21:08:49 GMT  
		Size: 4.9 MB (4911371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20854bfd706524b5737485cf8571306ce23e51041300d7dad0919592e6e9f619`  
		Last Modified: Wed, 05 Feb 2025 21:08:49 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:20d1b805ace29898e7fbfd763e6d7449398d11c79f26d32a2952f407049fa3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307655389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabb183e8ebcd71c8d0c6fb5f9c1c617652a5a567d1521fdaf97e8fb3f45527e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Feb 2025 19:48:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354218c5a9ae45d85db8f8a7c222a5a95ac10891fc8bc4e58bc61dffb50dcd3`  
		Last Modified: Wed, 05 Feb 2025 21:14:50 GMT  
		Size: 49.2 MB (49193687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f747b566d4c3bb74047988ca17f596db62421b8b97e7b8d91e8e4b3bcd8fc567`  
		Last Modified: Wed, 05 Feb 2025 21:15:47 GMT  
		Size: 210.8 MB (210792292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:0204aee70c54ffd197aef648ba4a810d9fbb060eeadc88efbf7065e369a569c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5e7c06e2bb95ee4db52043a49b7d8a6d616cdf8cebb709896ce0e995dac338`

```dockerfile
```

-	Layers:
	-	`sha256:d2f305660408c61811aae3f8c1b8a8665a71f977e6f0b9206a71c972d915c0cd`  
		Last Modified: Wed, 05 Feb 2025 21:15:42 GMT  
		Size: 4.9 MB (4909133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a868400f1d91890d2d14bcb4506c1fe66cd097656347d1c1225f6f78d11a3209`  
		Last Modified: Wed, 05 Feb 2025 21:15:42 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
