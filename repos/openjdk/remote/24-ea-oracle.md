## `openjdk:24-ea-oracle`

```console
$ docker pull openjdk@sha256:c88f062dfd77d078cbac238d7dfbb9e030f3b3a2421007dd2b6d30142699531b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oracle` - linux; amd64

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

### `openjdk:24-ea-oracle` - unknown; unknown

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

### `openjdk:24-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5a4472fdca0885a309c16490756d113d6c1994cfa1b323e887a0ddb71a78121d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307734185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6189d34ae7c7d944c5d19cb6f4b0ca3335e379b3c623697dbd2f3475321266`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 22 Nov 2024 19:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_VERSION=24-ea+25
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='06d2571c8af4948ac1eaad2b912ab59f320f01744bc4152f3476a65512bb3901'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='022d2edea028f26d0aa8cc933429f305abac8f8a74451095a55b1354f0db7966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff9f5494a427d9d8a40a0f42c60afadac361e3515d52601f7d74bf0d09b993`  
		Last Modified: Fri, 22 Nov 2024 05:14:01 GMT  
		Size: 49.2 MB (49188086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981ee1f51758540a106d4ff7d7d1c5015a848f6afcc728729d0d1a8a2267651f`  
		Last Modified: Mon, 25 Nov 2024 23:24:35 GMT  
		Size: 210.9 MB (210878707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:13f822835dad7cb22d2bc37e32865a02f613835ce8895dbf3f8015751b7c16f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cea25c644d7fdbe1ead4a0fe217ada6cc76e8110c4e0ac0b55dbcb7fd61db15`

```dockerfile
```

-	Layers:
	-	`sha256:68e9399bf9598e70aaa7728ac9f1830bcf882d81f3088dced726d43383350feb`  
		Last Modified: Mon, 25 Nov 2024 23:24:31 GMT  
		Size: 4.9 MB (4910341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2607f942e15dbc8d452db9488f584d0dea081161408a602251f95094b240bd4`  
		Last Modified: Mon, 25 Nov 2024 23:24:30 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
