## `openjdk:24-ea-26-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:e403225e178b537eb511ea39521e52ba78d39bd29881a5e5e5783196a42f6bef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-26-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:ca2cf9dfc43e8287870a8d1e424cee0750361c51be279146b1fd703f7b53804a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310492530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7005f9ffb2863a5c201a0ea44aaac68b2e7c4b6edf7f91967ce98941b6ada264`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Mon, 02 Dec 2024 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Mon, 02 Dec 2024 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 19:48:14 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 19:48:14 GMT
ENV JAVA_VERSION=24-ea+26
# Mon, 02 Dec 2024 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='5a912c97361c098aaee25aa395745f77456ec2af1541c1aaa707b20f20e50fb8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='fd075f47c3ef0e3e6270244864a33309becf3f2fbdff615d20a86ea15779caf1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf1b8130822be9bf2279a02fc0887a3fda78b2cba75805e44f82419543a8d11`  
		Last Modified: Tue, 03 Dec 2024 16:32:42 GMT  
		Size: 48.8 MB (48764963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93116d5d8910d60b72df1d9d293eb004b082cfec539a3dc1ea8320dccd09a1f9`  
		Last Modified: Tue, 03 Dec 2024 16:32:45 GMT  
		Size: 212.6 MB (212628865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-26-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:5fb7de27a046875816c952ea2d30fd690590bb5a83abd197d19e35e731c4b6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10830eebcf47044b2dc3effa70952e96ad6c04efd3b7d90d95f4dccc4509c978`

```dockerfile
```

-	Layers:
	-	`sha256:e9d25e381fe8de9fef13d6a62753995d8eac23d0b8e67d220bcc859803797571`  
		Last Modified: Tue, 03 Dec 2024 16:32:42 GMT  
		Size: 4.9 MB (4912587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7924aeac007772607eb667765e7adeb526e4697b8bc079c5ff74c03ac02f9202`  
		Last Modified: Tue, 03 Dec 2024 16:32:42 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json
