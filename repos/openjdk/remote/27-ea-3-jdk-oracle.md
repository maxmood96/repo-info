## `openjdk:27-ea-3-jdk-oracle`

```console
$ docker pull openjdk@sha256:6b6e76fd0cf44365ca052861195927bb90e64fc11b9eda4a3c2045111007efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-3-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:56269533fe433d46f965990297c4b09cd36442c87f077d590c3358f19087d125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313544681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012ca7741fefff5f0e0120099930d9e600939e0615adc9598b0dea82fae7c919`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:12:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:12:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 24 Dec 2025 06:12:18 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:12:18 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 06:12:18 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 06:12:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 06:12:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e10dc21723e990af6ec228f2e759c661e005bf16d67efbfe4826f75eace3ff`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 38.3 MB (38298802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1cfa508b9f805ef56630eacb005be41183ffddc874a6b0561d51c9bc6bf3bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:13 GMT  
		Size: 227.9 MB (227926123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:bf5d5b80f93a6d9704df67067119c1564e1185e30d1945817c6539dfd96f6320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6ec78f4b64c8025f48b1c2f6b2343c038663149cc3813e4536b8f0f3b86b30`

```dockerfile
```

-	Layers:
	-	`sha256:1570c84575616cc9925ffcc5c2692dcdbff0c0ee78488cd8151fce9c25910a3a`  
		Last Modified: Wed, 24 Dec 2025 07:26:05 GMT  
		Size: 3.7 MB (3655339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52f0501f79b1757177d171a1fc11bcf88178abaee8f864e28dfa6b8188132e51`  
		Last Modified: Wed, 24 Dec 2025 07:26:06 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-3-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b73fd40c5a5e9e18ed00e093221dbfe0ae2a2c1b35784bddda360d0e86069ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310458204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65847da335312f58ad540901ecb3762e941faad56d8a95dd31c4084dc8f3ff9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:12:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:12:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 24 Dec 2025 06:12:26 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:12:26 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 06:12:26 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 06:12:26 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 06:12:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edf1ae8686bbde3e30a7a1e695dab68cb3380fb9606189ea3dc93305b5dd900`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 38.7 MB (38699384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0ee4285267179def8b3d3878d2a00ce7d753c84324af488b6984bb9176ad07`  
		Last Modified: Wed, 24 Dec 2025 06:13:42 GMT  
		Size: 225.9 MB (225855827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:70bb61d1ec5b4718f9a34f909828c667735f2fa4102150a67acdfa105c79f7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0b401eecb8306b8040d0e8960128240b1f0b52fbdd9b8a8019f8e1fe13f255`

```dockerfile
```

-	Layers:
	-	`sha256:c28fa740361ecddb904cf09d18aef7a3d1b8b4d1eba6707338dfe7eb26d94e1a`  
		Last Modified: Wed, 24 Dec 2025 07:26:10 GMT  
		Size: 3.7 MB (3653029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61e83db41a41fffa2537a81e1959a035f5a280b64e59e1201a9ddd3bdd7a6fe1`  
		Last Modified: Wed, 24 Dec 2025 07:26:11 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
