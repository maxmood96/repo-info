## `openjdk:23-oracle`

```console
$ docker pull openjdk@sha256:467ff574d27e3525997bd6644563732d9471896c1131f4c1e715a197d90a3225
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:49818a2152c923d3bc39c9e85b88811b670072124882525a52ab2f621a37b401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298127795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e90bd886e5459565ab4e3252e64add9a37029a369b5efa24f1a9dcbb1ebcda`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9787d2213b963e1cae955cd65939ea8b89bacfeadd00a2b1448f92ed4041a90`  
		Last Modified: Mon, 10 Jun 2024 22:33:16 GMT  
		Size: 37.9 MB (37862443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f2f094118e512b881a0575149f8401afc82ac995d13ff47b3acee139c97db1`  
		Last Modified: Mon, 10 Jun 2024 22:33:20 GMT  
		Size: 211.3 MB (211270474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e27ec83e3790c96cbde86f8c05571a854ff58ce24cd50736281fc5bd5e619646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5d17afe74c9d9aab4d4b76148566997b269a7dc6faac9de4ab4dd49cd31fe8`

```dockerfile
```

-	Layers:
	-	`sha256:d23817e8310fb37b2cf244354b4ec6e50acf028b2ec87b5ede93e2c43b8abe3c`  
		Last Modified: Mon, 10 Jun 2024 22:33:15 GMT  
		Size: 3.3 MB (3333243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304746864fdd5baa6c96e240d503907b7ab6fac692bbcdba03718b497445b3b2`  
		Last Modified: Mon, 10 Jun 2024 22:33:15 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:00fa40f74d0e89b0ddd211db4ffb4410a135f8a0955ebdc4b893e233d4e8567b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295060357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317dfb916d4d2823e645a68d1cfee7894c241f3c51ab02dd6e789e5ab348801f`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4126ceeefbe5a1d06272578a6b6a99a1d422489b25511cbccbaaeb1576551bfd`  
		Last Modified: Sun, 02 Jun 2024 01:54:26 GMT  
		Size: 38.3 MB (38259157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fb23b25b3e556902bd31cdbdbed116bce17105cf25b7af29923e88d7713b04`  
		Last Modified: Tue, 11 Jun 2024 03:36:18 GMT  
		Size: 209.1 MB (209149209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5e0115aa64b633475d9fc70218feee4829a0f3dce5702dce550c8e18a66cb5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad91d616f0611670351fa25f0b79c2fc293485e418e49b0f6cf221d5e8bf88d`

```dockerfile
```

-	Layers:
	-	`sha256:a78b9352de49c23b5710f6e89df1f1acc102d8dd0a8aae87e2c65bb28c71cc1f`  
		Last Modified: Tue, 11 Jun 2024 03:36:13 GMT  
		Size: 3.3 MB (3331626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b14add91a6c0120976f29b14ff9c5e930185750d53fadf5169ef3b635214fd`  
		Last Modified: Tue, 11 Jun 2024 03:36:13 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json
