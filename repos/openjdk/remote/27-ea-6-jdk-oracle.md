## `openjdk:27-ea-6-jdk-oracle`

```console
$ docker pull openjdk@sha256:d817ae82cab50fd8c7098a6448817b1da8b2c004719be848e4b034ca3ea7a7a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-6-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:67e90d5266967d794e7763a14ae6a2af375fceaec0da629d476b74980e5b2e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313834235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8854bf0e351b4ebdb7765691d252648d55a98a746c51b893667f85e400b8af0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:12:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 28 Jan 2026 22:12:36 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 22:12:36 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 22:12:36 GMT
ENV JAVA_VERSION=27-ea+6
# Wed, 28 Jan 2026 22:12:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 28 Jan 2026 22:12:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5d45c47ad951c2691e62302c3f12e58bad39e8efb583c72058c42d774cc7c`  
		Last Modified: Wed, 28 Jan 2026 22:12:58 GMT  
		Size: 38.3 MB (38296127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0caebd8be029d3d5bb1c78c32031d7aae3a6f64a5329ee5e5e6847362dc27c2`  
		Last Modified: Wed, 28 Jan 2026 22:13:04 GMT  
		Size: 228.2 MB (228225394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e5666e848a97816ab4dee78b6880c60cff4ac90c3d395b994ac45863427c68f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e76a7fe0c44fa111c88c0660b8efc005fa88283fed41918787835ca95a98045`

```dockerfile
```

-	Layers:
	-	`sha256:5d5c29f3edcf363dcd6f7cddbef5a5b6799ecb7e8fe5c952b6d9ea9b6e6227a6`  
		Last Modified: Wed, 28 Jan 2026 22:12:56 GMT  
		Size: 3.7 MB (3655375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0455f3b65a4c2aba8b62ee51ce3058b02156af3991d1e8c6b8532137764e32cb`  
		Last Modified: Wed, 28 Jan 2026 22:12:55 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-6-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dce842829244f19760c4cd9c8fab7c9b989c2aa7c57b8614c97b781ee5a4735c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310744085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e937b8556f61c55dfb0b83cccd7e15b6af37ae3abf7e375218bddb56fbaa1114`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:12:02 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 28 Jan 2026 22:12:12 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 22:12:12 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 22:12:12 GMT
ENV JAVA_VERSION=27-ea+6
# Wed, 28 Jan 2026 22:12:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 28 Jan 2026 22:12:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289423e4c58521d9c4ebdb604f7edc16a15b0eec01c87b7bc5d19ddbaab90e18`  
		Last Modified: Wed, 28 Jan 2026 22:12:35 GMT  
		Size: 38.7 MB (38692413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d9de4ec420a20c679fcc9c81d3b8b39fe00352c1da4775cdc24ee05100c478`  
		Last Modified: Wed, 28 Jan 2026 22:12:39 GMT  
		Size: 226.1 MB (226148444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:ecda646ad3c40d2f27d46984896af7c3b58b8b1af49faf63c352f72ae79d2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f5c0bd5ffcd130090e5d56e255e4269578a2d321ad7c2c6c883e9725f3c523`

```dockerfile
```

-	Layers:
	-	`sha256:8f3468a1c6609ec26586023ecc455a2487dba4b9df83314d76ea68481abf836e`  
		Last Modified: Wed, 28 Jan 2026 22:12:34 GMT  
		Size: 3.7 MB (3653065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61521e6555b3b03044ec0bf88db9f24c70de643327d88021d841e535adbd4160`  
		Last Modified: Wed, 28 Jan 2026 22:12:33 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
