## `openjdk:27-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:cf88293e0d940366dbc90edfb61b1abedd7378d3fcd04c5c53b45e16c8311318
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:1fec68db5af19b49443baddb181069a845d3f9c755e4bbceccc89bb14ad79f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314370208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0706fb08c0128128daa6f9fbe7cd18ce4e20b8f86897754024509cba210a21`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:09:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 26 May 2026 19:09:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 26 May 2026 19:09:26 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:09:26 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:09:26 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:09:26 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:09:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d61308b988b2a37809d7ce211c6afde167ebfb70317db47d77edcbdf658326`  
		Last Modified: Tue, 26 May 2026 19:09:48 GMT  
		Size: 38.3 MB (38267899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3425ad1e33de71881f7a037ce4979fc0677ed4eb81a86bd99c48ea1caba8318a`  
		Last Modified: Tue, 26 May 2026 19:09:52 GMT  
		Size: 228.8 MB (228792736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:1fab1b1158db4e196cc31018d3fdd711ea3b27aab5d625a1d1a1c28337986b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4461fe94ac80d82fb185ecc0fe2c5740f8b5280b584d953f94d86b32640ac012`

```dockerfile
```

-	Layers:
	-	`sha256:b5b8c31401dd26c7d00c953da139e27de1fc1ecfc295c9c675be5cb63571f580`  
		Last Modified: Tue, 26 May 2026 19:09:47 GMT  
		Size: 3.7 MB (3651707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc09a3fd4d31e811be55d44312959852bd70280d4fd0b2f86862a24657858a39`  
		Last Modified: Tue, 26 May 2026 19:09:47 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:79f487a67718fdf60fd5f676bc6b430bb644a4f7fae4bbacfb4748ced7449e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311328206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf46da64a03033ddb3ca95edac61810e50244037685501d90ba1378b69f5995`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:11:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 26 May 2026 19:11:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 26 May 2026 19:11:21 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:11:21 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:11:21 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:11:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:11:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0e929ff3394fce4a2b1d03e5ccdfbc264ca123eb01334e4aba8b78dec52161`  
		Last Modified: Tue, 26 May 2026 19:11:44 GMT  
		Size: 38.7 MB (38665534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfe62819ea11cbce0a0fb49d7e9ac1eb285e5a6f9ab93b19a219e7c9ce18fbe`  
		Last Modified: Tue, 26 May 2026 19:11:49 GMT  
		Size: 226.8 MB (226763582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:50294dc783328a28156023c48ede8d65b6b2879edb58696950b0c884b94b579b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3664763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2a1170adc09c2cda2820e1509f616faefffcb195ecaf22cdf6b7ad40722242`

```dockerfile
```

-	Layers:
	-	`sha256:dd0d92f55403d5605b56c5817c36dd7c33e7003df53c694d90ffb7f4cc2e8407`  
		Last Modified: Tue, 26 May 2026 19:11:43 GMT  
		Size: 3.6 MB (3649301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc180c8d69f362c483ccdba956f02f55d0353c6a69bd04537a0c3b87242291e2`  
		Last Modified: Tue, 26 May 2026 19:11:42 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
