## `openjdk:27-ea-24-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:2f56b91dc4fc489679c25a49a6b42005a1d451501cc466092f9279da90889928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-24-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:d03b80f6339ec9bd80a0ff7d6f775e2eb6af55f9d78095615d7d89f6b68c74db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312458052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d0175d0697f1f113234cc36452e46d93d3c9426b7f09915b913bd021aadc44`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 07:12:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 07:12:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 02 Jun 2026 07:12:26 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:12:26 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:12:26 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:12:26 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:12:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bc5e622d927e9258947beaabbf5a60a4c76cb2134e2771d79639fe591645b2`  
		Last Modified: Tue, 02 Jun 2026 07:12:47 GMT  
		Size: 38.3 MB (38267950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c37727ee92f719bf5ae8bb837793970697b996ca94b334adb20221ba409b7e`  
		Last Modified: Tue, 02 Jun 2026 07:12:51 GMT  
		Size: 226.9 MB (226880529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:e16c8b59d85447ddb20c40d7ffa85c76f40ca6b9566025482c854767b8e288ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c7ebdce9ee0bd8d452d0f4ca4ffcd81386d48afba732dc5054a03d774a872c`

```dockerfile
```

-	Layers:
	-	`sha256:d66a59faadb7c85babcc7e1deb90a73fba3bd63f83a900517c4605224f85a5fb`  
		Last Modified: Tue, 02 Jun 2026 07:12:46 GMT  
		Size: 3.7 MB (3650422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b6b461c51a9b6de4140ccb80a08ce61671abc105c59cff5f4c2ff2a1d5abbdb`  
		Last Modified: Tue, 02 Jun 2026 07:12:45 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-24-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b50af6f430600e0bafb00593ea87b0d956cafea6909342984db3ea4377697723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309459204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c468e99ca1d1ece585cb961b686382c8561c31c8ebc727fca98846e308a7209`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 07:11:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 07:12:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 02 Jun 2026 07:12:09 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:12:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:12:09 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:12:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:12:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d46a677a00822c4fc21ef86a09fbc30bed864f426d1878e067a4da858e163a7`  
		Last Modified: Tue, 02 Jun 2026 07:12:32 GMT  
		Size: 38.7 MB (38665606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ecd22c1b22a424d60457b55658add2788c3fa7c161d67560d6317963f6d8fa`  
		Last Modified: Tue, 02 Jun 2026 07:12:36 GMT  
		Size: 224.9 MB (224894508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ae7609e9acb95b06eb4af50ec9305acd3f86787340d053bf7120053c5a73cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6c53cf250fd081e3de3b7317777d93ac4fd52a21bf605efcec24d1d0f21607`

```dockerfile
```

-	Layers:
	-	`sha256:7d293cb825b7b87ab46ceba1500c85c0d24dc73560bb78dcbdab0be402ef3ce9`  
		Last Modified: Tue, 02 Jun 2026 07:12:30 GMT  
		Size: 3.6 MB (3648016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cca4352c85861c2da7933b048bf3196c80229f3d55c810032e7e3edbe569a3`  
		Last Modified: Tue, 02 Jun 2026 07:12:30 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
