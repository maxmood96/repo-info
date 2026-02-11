## `openjdk:26-ea-33-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:91a4d3d642b4f49b50ab5f243542bc5c6be1184c630aea12bfc24115dd167163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-33-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:338099d8fb7a7d5fa89e3e89478f3be202e6e62dd6cab52aed8b47665a143c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294779448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e65d6b016769d5dec05d52d7763a9069a1c3e4e334deb13501a587d5b1eb1ec`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:50 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:50 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 23:10:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 10 Feb 2026 23:10:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 10 Feb 2026 23:10:42 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 23:10:42 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 23:10:42 GMT
ENV JAVA_VERSION=26-ea+33
# Tue, 10 Feb 2026 23:10:42 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 10 Feb 2026 23:10:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df558405081e8d5c6af13745e322e2d270802ff99fe9a1eea2b63615844efa1a`  
		Last Modified: Tue, 10 Feb 2026 23:03:01 GMT  
		Size: 51.5 MB (51464982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22f5df7ea3096a28583fb0932dc662f53498604ecaa8662f0e513238fc5f313`  
		Last Modified: Tue, 10 Feb 2026 23:11:01 GMT  
		Size: 15.0 MB (14991677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd92b1f8f7f9486237e34db38b3a7249a00a8d264f215071f2aeab2a42af259`  
		Last Modified: Tue, 10 Feb 2026 23:11:05 GMT  
		Size: 228.3 MB (228322789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:22ecf566170badfa1e22897cbba22ee6a783ce48315862b009b9c59cb140bfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9830477993970233eba76f0160215785f0a66dc86df06a57d6477a641cb8d4e5`

```dockerfile
```

-	Layers:
	-	`sha256:88a27da254e97f38779e98d5bf19ee8fc19580d6f378f12cc9f46d76e7283d02`  
		Last Modified: Tue, 10 Feb 2026 23:11:00 GMT  
		Size: 2.4 MB (2448694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b657a16d3996b2a1e06fa1cbb549ba4a8d7cc4425ae90d8119cffee5bfb29ae2`  
		Last Modified: Tue, 10 Feb 2026 23:11:00 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-33-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:41a3ff6997e2d240aa388025b3377c9b3dabe33afd5fd9d75ddd4ccdf365f42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292146755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c391c24053e4930cef9517832ae0ad02f09427f449b30f05806af9d37df71cd6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:07 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:07 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 23:10:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 10 Feb 2026 23:11:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 10 Feb 2026 23:11:00 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 23:11:00 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 23:11:00 GMT
ENV JAVA_VERSION=26-ea+33
# Tue, 10 Feb 2026 23:11:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 10 Feb 2026 23:11:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07a1effc9605f90c3e2f6e8e5b85d7de94a80b436a975fd605cfe7f53acd6ca5`  
		Last Modified: Tue, 10 Feb 2026 23:02:19 GMT  
		Size: 50.2 MB (50191339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ceb8831e0da270203511acfa003af3f6ff1ec2905dfd1b73812f9d17b572d2`  
		Last Modified: Tue, 10 Feb 2026 23:11:21 GMT  
		Size: 15.7 MB (15690775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cb1230fa39df8e5643accf02b7a46c8710e30567908b9c3e41b5797f816167`  
		Last Modified: Tue, 10 Feb 2026 23:11:26 GMT  
		Size: 226.3 MB (226264641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:4daa0a6cb8e0b90483051f43639a3570fc71cae9e17e300c2519419bfcdc2c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cdcc99a4738159209e3b45e28e5671cddbebbc0a2709a871bfffaf2f4602fc`

```dockerfile
```

-	Layers:
	-	`sha256:a46e63128d3f2ca7bcd8cc0d4f3ba06e7f52b076223506a1ad895961fe3708ea`  
		Last Modified: Tue, 10 Feb 2026 23:11:21 GMT  
		Size: 2.4 MB (2447504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724a8e9187976339cae147463c8ae82677a6ab233f6b389ee6301acbd3a78e72`  
		Last Modified: Tue, 10 Feb 2026 23:11:20 GMT  
		Size: 15.5 KB (15461 bytes)  
		MIME: application/vnd.in-toto+json
