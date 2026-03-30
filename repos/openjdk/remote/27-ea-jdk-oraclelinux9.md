## `openjdk:27-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:7df28075c4e7cd4830a1b5cfe689149add06117ee1c72fa72346b2e0acb4f2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:cf835ee80e2aac94d47e5ea731f202a85e4ab7e9197910cc2de5f5dc1458f48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314095119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d763e0d088c8430297a16b1106ce94d8ee6c4bdd2303a39723eb7019233d3d53`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 17:51:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 30 Mar 2026 17:51:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 30 Mar 2026 17:51:31 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:51:31 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:51:31 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:51:31 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:51:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac90a09a3e31c552efa1c9a49908d38f25a3ff08536dc8b148ee673507d520`  
		Last Modified: Mon, 30 Mar 2026 17:51:54 GMT  
		Size: 38.3 MB (38297413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6c5eff714838bf6f70d8a741953f5782cb019474bc52c275ad7e1be4c1dba`  
		Last Modified: Mon, 30 Mar 2026 17:51:58 GMT  
		Size: 228.5 MB (228487437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:aba4b57fe0e653e9f3c3db86e28d9902e7505cfe4839c179808f9bf59e68d042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e3823c04a2ee845a8a074f4939936ead221646b2def7f6aa0c0ac2ab2d56ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce0d993acaf7e3abd6a19880a57144f6b046a805c98a2388fc2df6c0929f74f1`  
		Last Modified: Mon, 30 Mar 2026 17:51:53 GMT  
		Size: 3.7 MB (3652947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013b6dd47a4edfd3a90bbf86094e9d28706f180c0ea4936960df7324cd64bbb2`  
		Last Modified: Mon, 30 Mar 2026 17:51:52 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6c7135d462fe8c6ec8e79189d82728bf1b16d7e10aeee0bd0b659a7cd5dd9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311044413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc7283723caaa6a11ff7097f23b1f00c0191ae9e7c6bda404026d3e04661133`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 17:48:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 30 Mar 2026 17:48:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 30 Mar 2026 17:48:54 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:48:54 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:48:54 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:48:54 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:48:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64196a9ddde48f61502beabcfb82bd24338eb2a7e113121e99d2546feb6fbc7e`  
		Last Modified: Mon, 30 Mar 2026 17:49:17 GMT  
		Size: 38.7 MB (38692359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4e210e5e8787f40c6557b9b92fa7a88940943705789eec0875f230be33d6fd`  
		Last Modified: Mon, 30 Mar 2026 17:49:21 GMT  
		Size: 226.5 MB (226454072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:52d0b984f98cafcf714101e0cb6e1d84617179c6bf80f9693fa91a6f2c3fd4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3666003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0396d05c1c2f52ba5aa6db2cbe27bd786f0b63ea15801f65ded65cf5a2613a`

```dockerfile
```

-	Layers:
	-	`sha256:0ed6570d4b0855e5ef248293e9ce0717d32357df11485d27fac8b6c0d60b4e3d`  
		Last Modified: Mon, 30 Mar 2026 17:49:16 GMT  
		Size: 3.7 MB (3650541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a67d7d787a01806eaecf7b1321b1ba484bac2c02f744f94f15828891604abd69`  
		Last Modified: Mon, 30 Mar 2026 17:49:15 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
