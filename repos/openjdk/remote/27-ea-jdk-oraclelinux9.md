## `openjdk:27-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:22d6a9a1f5a20596e10322393bdb1fd7b318f701ea0c2bae9844abdd3b7114e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:f309192d04b75451180cd0de865dbe5a6f74d6659344776cec1497e4ebddb101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314225058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a10159ee56e4916e5fac95e430bec53cbb3611fb1ea2b81df263184dddf09`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 23:50:45 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 11 May 2026 23:50:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 11 May 2026 23:50:54 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:50:54 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:50:54 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:50:54 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:50:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123fc05551d09eb48975eded7e3c4a8c765b6161c48319d281016df35cad0172`  
		Last Modified: Mon, 11 May 2026 23:51:17 GMT  
		Size: 38.3 MB (38272801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9aef6415ce1c3df46b0074e1417980d66dd5dfdad395836d5d1f64035c1362`  
		Last Modified: Mon, 11 May 2026 23:51:21 GMT  
		Size: 228.6 MB (228642401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:fe73421663154a3b6ada78e644fb4d4bfdd97cdc2d802b495d513961bb471b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0195c276a9854af2d7723762409a7252e299ad445a1ff6f7e19c30c7bc18e58`

```dockerfile
```

-	Layers:
	-	`sha256:10620c2793fdd24195cc9218ec446ccb53019df969cdd1d1bb367b49b59d788b`  
		Last Modified: Mon, 11 May 2026 23:51:16 GMT  
		Size: 3.7 MB (3651703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28808e76ac2a057c91d7b98dbd46d896fa010675151a4a9bbc350f54a23ab2e0`  
		Last Modified: Mon, 11 May 2026 23:51:15 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d5031b427035dd85515fb4cfde3e9d5973e754e8069c63738908ed1ac45dee90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.2 MB (311158875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd946b28ae359f494310db3652031a34e2477ea0e643a6323ad35c5d84d30761`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 23:51:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 11 May 2026 23:51:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 11 May 2026 23:51:46 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:51:46 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:51:46 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:51:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:51:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bc6b6dce24ffbfbc5da7dd9eaabff6fb9c69dbd114087377383118e61e3710`  
		Last Modified: Mon, 11 May 2026 23:52:09 GMT  
		Size: 38.7 MB (38662615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a8250a09aefb70292b52b0b07df10eec90eebb43cc355e2f1e7cb908789314`  
		Last Modified: Mon, 11 May 2026 23:52:13 GMT  
		Size: 226.6 MB (226597338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:509108e8f8b7298404dd0fe7b82be47be0c22800ba3a3b92fa57ad4e60a5713e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3664759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e428695952546396f809425253137d843a9daea731afe5f63f62b7cec845037`

```dockerfile
```

-	Layers:
	-	`sha256:e8f0f51124e27b0e6ae63d1abf8cf055e775e50e68e277f7411f02e4018d04d0`  
		Last Modified: Mon, 11 May 2026 23:52:08 GMT  
		Size: 3.6 MB (3649297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf547dc8931b05a30df3cc2f9e6d384e84c5b0503c7152064fa7432a2649b89`  
		Last Modified: Mon, 11 May 2026 23:52:07 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
