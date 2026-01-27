## `openjdk:27-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:3fd47f0ad5d35940a91680b1f346b41395dff118ddc963ea347130278abe7a0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:6a689b478f5c7f08d81bea060a160d200d581c11d17f613eeffc32973b921f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295139978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24c1bdb1dc97203425621394217c13cab7c471f6422ec967f0367c677d3f1bf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jan 2026 22:04:10 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:04:10 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 22:20:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:21:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 26 Jan 2026 22:21:02 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:21:02 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:21:02 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:21:02 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:21:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70f5c9ee868f124c508277177dfd78acddb8ada1f704dc8be2b2cdd99836131c`  
		Last Modified: Mon, 26 Jan 2026 22:04:22 GMT  
		Size: 51.5 MB (51467065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a89566332abf31ba60fbfa0b6def0444415da099320e609b0953605463eb2e4`  
		Last Modified: Mon, 26 Jan 2026 22:21:23 GMT  
		Size: 15.0 MB (14991052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103305e3deb7322f54e83d80e16b16481a162bd64242a9af240e049c604aed6b`  
		Last Modified: Mon, 26 Jan 2026 22:21:28 GMT  
		Size: 228.7 MB (228681861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1cdcf096f9420baa8e7ad2bf93635913ad31b06a925e4ace68356a08736c9c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee03954d2687b0f3ff2cfc7d8e345ff835c3ce1724034c3324f94a338338bb6f`

```dockerfile
```

-	Layers:
	-	`sha256:f2dd6002b75585fdda06a3fd38e481839d1626d164bdbf4b0d7854768f22f47c`  
		Last Modified: Mon, 26 Jan 2026 22:21:23 GMT  
		Size: 2.4 MB (2448680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb07fe33cb68f31bef95983060605dffcd14ab639caf776bf0d48f4ae7b7d097`  
		Last Modified: Mon, 26 Jan 2026 22:21:23 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f7a808ba141a04ac6059c951cf1df286a754a1374bc11864a911c03e1444a762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292507554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350be3f9e396a716a72ec2a90f2fb4a047317b41f8a7c1305b2d59e62f8e2337`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jan 2026 22:07:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:07:11 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 22:17:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:17:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 26 Jan 2026 22:17:24 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:17:24 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:17:24 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:17:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:17:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e76a047bd66be5e3e8818d893725279bf9a5b8a583db4b258f0d16df8850a42`  
		Last Modified: Mon, 26 Jan 2026 22:07:23 GMT  
		Size: 50.2 MB (50197120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6531c42b37027b5baabec984a3d23dd9a79ca265c03bac534a883849a90759c3`  
		Last Modified: Mon, 26 Jan 2026 22:17:45 GMT  
		Size: 15.7 MB (15687708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0b59fe73ed70bf78b7966f00e6f574365fb4045ff7579d3d1ea5410a2e4f88`  
		Last Modified: Mon, 26 Jan 2026 22:17:49 GMT  
		Size: 226.6 MB (226622726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:76592105604648735a6525fc7d6e44b18fe64614a0105fa5f0b764b126410851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac69f945ea03a8188c96c1edf4651bc35ef1662da8182a0ff302a4863b87273b`

```dockerfile
```

-	Layers:
	-	`sha256:1775a67e8051c9f86e52752c04ae98492529b150b399718bfd5eb97a36ab565c`  
		Last Modified: Mon, 26 Jan 2026 22:17:45 GMT  
		Size: 2.4 MB (2447490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1808a6d47588181918431a42ab9d9ade14f9c542d56c41eb7e46f1ebb6fdf31e`  
		Last Modified: Mon, 26 Jan 2026 22:17:45 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
