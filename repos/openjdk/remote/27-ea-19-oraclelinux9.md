## `openjdk:27-ea-19-oraclelinux9`

```console
$ docker pull openjdk@sha256:dbbcfda1cb2249566f62137831edcf01e6c3b64a899d10860bd74cd1318a88fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-19-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:1f545208a2d260cc2ffd0f48d6b7aafd4c7aa90432a86b1d0012bdc1030af2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314004477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e10e8d2be90fefc9b4c3b6fb910d1a1b5c9364bab323282e36fb9e3a884a82`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 23:00:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 23:00:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 04 May 2026 23:00:23 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 23:00:23 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 23:00:23 GMT
ENV JAVA_VERSION=27-ea+19
# Mon, 04 May 2026 23:00:23 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 04 May 2026 23:00:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ea43a0ab6c41510ea8659361c554de97573ef2ec2c82224b790c734eed5972`  
		Last Modified: Mon, 04 May 2026 23:00:46 GMT  
		Size: 38.3 MB (38271276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa447c21cae0ee290eb44752d53c46b5309c1bf75bd89586ceedd22463a02f97`  
		Last Modified: Mon, 04 May 2026 23:00:50 GMT  
		Size: 228.4 MB (228423345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-19-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:98d08cb00868ec0dbd800e63174486c9feeffd476da467ce03cabde450de3a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1486c28af0ab0a2e93d030dbf43354f251a62c6aa566027c09eda6570e2b8d4f`

```dockerfile
```

-	Layers:
	-	`sha256:363c318b801e1c2ee5747f3c8e42db6272eba96701f3d4e3f2253da91dc59a7a`  
		Last Modified: Mon, 04 May 2026 23:00:44 GMT  
		Size: 3.7 MB (3651703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d80c92ea3c2449877dda1e92ecd2cfe9edc2de6e233003be88141853c6dc4a`  
		Last Modified: Mon, 04 May 2026 23:00:44 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-19-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b9e69f1e4c80c3e9ada85096ac3e7ddea6dd0c8af288fbdadabe9a8fbd3c9653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310949008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64aaab2c5c6e1640a23472d44807f1d867a5b8fe0345e34c213585d113781d1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:09:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 04 May 2026 21:09:42 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 21:09:42 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 21:09:42 GMT
ENV JAVA_VERSION=27-ea+19
# Mon, 04 May 2026 21:09:42 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 04 May 2026 21:09:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2594f8ec8fc5489d664a7bee5859ffce74d52cf8d915cf93ec6cef7c987e25f1`  
		Last Modified: Mon, 04 May 2026 21:10:06 GMT  
		Size: 38.7 MB (38662235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3902a0314d9d773b8f73ea915ea56cc2ec48965918987784c8037e686d40b1db`  
		Last Modified: Mon, 04 May 2026 21:10:10 GMT  
		Size: 226.4 MB (226387851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-19-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f024fda22fcd36c010f3df88574d0ce5826fa7021706d92a5988bfac84efa69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3664759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cc38992d5167d107d13a1c96a381a9559c66e28930219c4695154139ee26c3`

```dockerfile
```

-	Layers:
	-	`sha256:78b101d559d0c2c0ec0225d62085772fb84540225c161a327808487890d3e621`  
		Last Modified: Mon, 04 May 2026 21:10:04 GMT  
		Size: 3.6 MB (3649297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e299e3ac2a68af86519dd0b9c778106738f7db33497cc2a7fd89b2379d7f82`  
		Last Modified: Mon, 04 May 2026 21:10:04 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
