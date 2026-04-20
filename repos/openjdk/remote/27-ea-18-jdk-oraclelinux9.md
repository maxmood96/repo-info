## `openjdk:27-ea-18-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:72576176225766d5735099bd77e4b9a583230d024d7afce9e3c5159360c09016
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-18-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:ad316d140157f966dc29663464df6b37ff6ae7e833a837fdde760eb3e5b1be32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314196154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6a97e274be515869d409efd8ff44b84f4c94e84a3c20c944d0ccecf3a9f1bb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 17:41:03 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 17:41:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 20 Apr 2026 17:41:12 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:12 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 17:41:12 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 17:41:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Apr 2026 17:41:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96c4bc0ff2a4be1c3d33812f5cf82828baa31908a3caebf4f4e0d76ba1e4860`  
		Last Modified: Mon, 20 Apr 2026 17:41:35 GMT  
		Size: 38.3 MB (38269971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b688a29c156910b291eefeee5b792c97932dcd7b923044a18a85a53e55968e`  
		Last Modified: Mon, 20 Apr 2026 17:41:39 GMT  
		Size: 228.6 MB (228616370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:c3d98879039bcf1f4dc1a202447379c9aa33c20c192cf2880b46e886661a0e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f17005c37fda9c8918963de924f1e522b04fc7be1857ce373dad41ebd3ae85`

```dockerfile
```

-	Layers:
	-	`sha256:7fc7c1d4f7e599f64e49a653ab94beb231a673b89260ae2efafee4f834e11adc`  
		Last Modified: Mon, 20 Apr 2026 17:41:33 GMT  
		Size: 3.7 MB (3651695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5047b54f787899d0da122a8a0dceca0da3a3f229d353345897d7124243f2e9e5`  
		Last Modified: Mon, 20 Apr 2026 17:41:33 GMT  
		Size: 15.3 KB (15340 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-18-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7bf01a8774a21463b2df8c633d92cc53848055581bea6fa7326e43e56c15cac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.1 MB (311149473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cc14e4d7eb34d2b53f94e084b0b405f872e5c823ec401d074983b7b5fc40f1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 17:41:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 17:41:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 20 Apr 2026 17:41:15 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:15 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 17:41:15 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 17:41:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Apr 2026 17:41:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2fcc2b2f96aa14ac122e024b965e09d9d9f3dbcc48f1061d4c975f7ef05615`  
		Last Modified: Mon, 20 Apr 2026 17:41:38 GMT  
		Size: 38.7 MB (38667300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d68d2675f97cee03fd5a07206488420fda028d35878202e8a23927a5bbb074`  
		Last Modified: Mon, 20 Apr 2026 17:41:44 GMT  
		Size: 226.6 MB (226582386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:d2de65999e1facaa06aed3b56a16538cf7cfe8b9acf1a4f34b27470bf3441214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3664751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd894084d3f74a72caf5a30470c6dc77c76706e573c6598a4efc80ec6ad0dd6`

```dockerfile
```

-	Layers:
	-	`sha256:05c8a200ba200d70a647ce94ca044f61d89f9a9eaf66173f291fa91ec088df0d`  
		Last Modified: Mon, 20 Apr 2026 17:41:37 GMT  
		Size: 3.6 MB (3649289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c73b89a4cd67e8f436aa76849f14e150860da1ba08c69f22a2b8d9fab1ced9`  
		Last Modified: Mon, 20 Apr 2026 17:41:36 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
