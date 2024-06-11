## `openjdk:23-ea-26-jdk-oracle`

```console
$ docker pull openjdk@sha256:6c3d6ac009f39c53d8307a71a634ffbac70db4788dc6f852b50ade41c08e8ea9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-26-jdk-oracle` - linux; amd64

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

### `openjdk:23-ea-26-jdk-oracle` - unknown; unknown

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
