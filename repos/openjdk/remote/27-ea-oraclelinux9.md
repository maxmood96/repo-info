## `openjdk:27-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:34cf715f637d3b3e1a47e869662caed9cc144f5b2f604dc1ebb78220aa4bc71e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:517b1ad73fb9ad8236a9ff5c0584108bff608bf2ffda18a4aa8a8fe35f2dfc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314003201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d8342b33934c758848f4481d8169b16943eda0e57ffc23e3b23ecdaebece6d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 23:34:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 28 Apr 2026 23:34:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 28 Apr 2026 23:34:54 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:34:54 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:34:54 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:34:54 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:34:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e66405128a1b0257fcc4362a765eece73bdd898ebaf7a75c0ba364fd20a5d63`  
		Last Modified: Tue, 28 Apr 2026 23:35:15 GMT  
		Size: 38.3 MB (38269977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb3adf1ed2371996db70c09f19dfd8bd205bcce65b410a2540fec8311b46a1b`  
		Last Modified: Tue, 28 Apr 2026 23:35:18 GMT  
		Size: 228.4 MB (228423411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:1b50457e9bb2ef8596ea5b78f488cf26b5804ccef5a3026706bca0785d7d9662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b345863855f8589b17a333e460c1bbe80820714933b388cd01b5e7bb8cded0`

```dockerfile
```

-	Layers:
	-	`sha256:dfc3de4848a408895dd82afc371cf398f4c4587e34ceb8c54ba5b00ae81198f4`  
		Last Modified: Tue, 28 Apr 2026 23:35:13 GMT  
		Size: 3.7 MB (3651695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41664feb81a6600c00b38ffe9b985877557b9845f342165b7fed8f6eaa058607`  
		Last Modified: Tue, 28 Apr 2026 23:35:13 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d8759862278925d9577535e8d5e060e93640103d69836e8b63bbaebddedf63f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310954961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cbd440c9e1569aa3c5e1e1c1ed9cf77a5fc8225610007c2609f5b1ac841591`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 23:36:01 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 28 Apr 2026 23:36:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 28 Apr 2026 23:36:09 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:36:09 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:36:09 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:36:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:36:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2263de15cca1eee7e910c8d6c19bffd1aded98dcea208685bf7c4ade3f89cbf`  
		Last Modified: Tue, 28 Apr 2026 23:36:34 GMT  
		Size: 38.7 MB (38667302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13be594de399c94ef502438d23bfe924664690aaa2e38dad279b013ee3ccf4`  
		Last Modified: Tue, 28 Apr 2026 23:36:37 GMT  
		Size: 226.4 MB (226387872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:fe88947cc18bffea8bb9f67bb97013227d2fbbfa66db53e0e7b3ac14bfaedebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3664751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ca0e22e2956f17ed5f77ea65fd430b529f7d95e61b046737336e3526c4bbb`

```dockerfile
```

-	Layers:
	-	`sha256:28b7a7682712fad37a3f98e7bb767fade50050d6066a82b19c19eaa583606b20`  
		Last Modified: Tue, 28 Apr 2026 23:36:32 GMT  
		Size: 3.6 MB (3649289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab30f8ed59fe5b94ad44f28df5c82434cc9caefe7dedb074f221da9173c8d85d`  
		Last Modified: Tue, 28 Apr 2026 23:36:32 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
