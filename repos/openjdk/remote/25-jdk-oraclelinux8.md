## `openjdk:25-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:04f15166cda820fdb3e7808e966450227c6896875fe06b1b2d64dbba1ed6cc34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:779282fa007b32f2bae66ae0432c7ed83d31822a8e123c8a54e12fd050dabd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279171847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fec0a79dc66dece41efb543e18519ed9e52443454cf08110ff04474ddddf83`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Apr 2025 20:57:19 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 20:57:19 GMT
CMD ["/bin/bash"]
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f3b2ad924e7ca97331fdfa1452577e2714860bf1ca5f6771b23be815f3ec81c`  
		Last Modified: Tue, 15 Apr 2025 21:51:32 GMT  
		Size: 51.3 MB (51312414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1575aff33c7227193dd6ecf95aa4704eae9a37ad86e06901d800156c0f01c39`  
		Last Modified: Fri, 18 Apr 2025 18:38:06 GMT  
		Size: 15.0 MB (15003460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4584ccae95cc531fcc629d3f93b18c044a54e0661d5046ef52d6b71aec73e87f`  
		Last Modified: Fri, 18 Apr 2025 18:38:09 GMT  
		Size: 212.9 MB (212855973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:591941bc5fbd449b12e614dab6fdf597a4e06c5c76ebeecda965be31810e68ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8961551c5ff37e8c9bad521f7538f349e7ea6f4cdcb15f99ae22dff78b2269`

```dockerfile
```

-	Layers:
	-	`sha256:3d74b9a15f76a936c8376c42f54631cdd6b869dd32958e0fbfe126cd97c97c11`  
		Last Modified: Fri, 18 Apr 2025 18:38:06 GMT  
		Size: 2.4 MB (2442869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca85b2e7a6116ed83c02a19ec51cf8e450dcb8e432c798291ec0e725ce791a37`  
		Last Modified: Fri, 18 Apr 2025 18:38:06 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:98cf0debd82bcacc84674941ee2bfe28971858118bb2bdbf4f6439b5425cda6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276373926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef447074a9984fe572e04c750de569fd9abeb62745b4faa68b8011a441f34b9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Apr 2025 20:58:10 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 20:58:10 GMT
CMD ["/bin/bash"]
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:321e78d03edef700126a05493206e74311bcaec7bfcbffcdb1632706eeb5635d`  
		Last Modified: Tue, 15 Apr 2025 21:51:19 GMT  
		Size: 50.0 MB (50020274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd1f69440985768661d39f21920c1138fde7a0693e9d51d5a207dfc34788b6`  
		Last Modified: Tue, 15 Apr 2025 21:58:35 GMT  
		Size: 15.7 MB (15675726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8af96cea364b79e6faa240879cf5865633990b7d16aba68e7970c8f29b70b`  
		Last Modified: Fri, 18 Apr 2025 18:38:25 GMT  
		Size: 210.7 MB (210677926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:548b51f0aa4054b7b76ee18b91111f52e80b128ac8d1e12e0ef905e1c8d39961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4725ed5d5ffef2cbe374ad19d99fb60e28b0ff579e7722ce5f7f5da1f8a964ab`

```dockerfile
```

-	Layers:
	-	`sha256:ca50cdcb613cfa46e0a45e22dd0349f8f22886962b47ed91ef5e0e905c2705e3`  
		Last Modified: Fri, 18 Apr 2025 18:38:20 GMT  
		Size: 2.4 MB (2441715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3340758c836f7a8a2133dd358eabd7f464f72773f1e1127eb5bf5de6af366340`  
		Last Modified: Fri, 18 Apr 2025 18:38:19 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
