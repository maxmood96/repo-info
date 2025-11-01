## `openjdk:26-ea-22-jdk-oracle`

```console
$ docker pull openjdk@sha256:c91c350af999648da19835b2117f1865cde5c3a4c77b204e0e97a6482317ca95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-22-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:0d5b9570c8894efd1f4177404d20d4d2ba63d8e451847224ee3ae694fe64db32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313387385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79c652f7b9b6d93383f09aa129966cc508732aec99ec3fd7a8bc86244e8d3cb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 20:29:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Oct 2025 20:29:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 31 Oct 2025 20:29:18 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:29:18 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:29:18 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:29:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:29:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f52671d8640f78fb620835252e9bb17ede1f1ffe1d006b52689eccc020a81f9`  
		Last Modified: Fri, 31 Oct 2025 20:29:51 GMT  
		Size: 38.1 MB (38088664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e9256083390a62a4cd490d39471961833a586e8a03335840305f11c7680198`  
		Last Modified: Fri, 31 Oct 2025 21:26:04 GMT  
		Size: 225.8 MB (225802216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:8f9ad98cd841f05c46b832db67a084c7af9566d764fce090ec680cfb3d79f093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20953d97fc19157c86b180501890067983aa83743d965eea3c155f9cd1cd6dbc`

```dockerfile
```

-	Layers:
	-	`sha256:7f989b46ef1730f4dc8e3c9667ae6374cdd4d09c7e9837c26cb227989bd8bc0c`  
		Last Modified: Fri, 31 Oct 2025 21:23:27 GMT  
		Size: 3.6 MB (3638870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8911474527fa2abe19b2b3e33d6734a5639de9c187cc2ea4321cc4a3e6508596`  
		Last Modified: Fri, 31 Oct 2025 21:23:28 GMT  
		Size: 19.7 KB (19703 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-22-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:370113cfafc6796c1bfdb5ee27d86ede54095ef93030660853cb93788d49c8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310219284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b971c8b6443a76930cf758dacdfa55e6979d71a9064afaef392f1b0b4b4ddfe9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 20:09:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Oct 2025 20:09:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 31 Oct 2025 20:09:53 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:09:53 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:09:53 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:09:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:09:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e330f617d80d4f200463c938ad131223d4f568895e3d18972993148c9cd7c8`  
		Last Modified: Fri, 31 Oct 2025 20:10:29 GMT  
		Size: 38.5 MB (38491320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21da5f6ea4336817b8bcb3323204c0a6ae9bf5a30f896762eed7114094f2fdfd`  
		Last Modified: Fri, 31 Oct 2025 21:26:28 GMT  
		Size: 223.6 MB (223641063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d0eea96def5df3b13f675765cd13f4df271981c963a3079db90e9407690410e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3656622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd7ab94463d30ea710ebd75ca89295fe18d6d452be08b5240bd6a94dd7cbcf`

```dockerfile
```

-	Layers:
	-	`sha256:e5dae7e5f4145771ca550b778cc6fdb7d3786533ecccb29eecee0b99f68fa6bd`  
		Last Modified: Fri, 31 Oct 2025 21:23:32 GMT  
		Size: 3.6 MB (3636632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff8b683dd0e12906f196f838cdb537a55fe4b2fe9097f3d43f18120201b4c5a`  
		Last Modified: Fri, 31 Oct 2025 21:23:33 GMT  
		Size: 20.0 KB (19990 bytes)  
		MIME: application/vnd.in-toto+json
