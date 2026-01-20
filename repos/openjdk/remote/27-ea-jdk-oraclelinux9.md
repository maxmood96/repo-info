## `openjdk:27-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:4b683a01f89e4b025fc793984f0b74941ec6085a32fe77191e84a2758cfb0333
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:3505074074a84c7dbc0012f87f1e09b6329a1ef1bd25708ca21a9286896fbe1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313522870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8de6e0aef7c0b87cdab25b0b9317be42bb52372705d6c752b80f2b23b525ec`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:28:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 16 Jan 2026 23:28:42 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 23:28:42 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 23:28:42 GMT
ENV JAVA_VERSION=27-ea+4
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc6a75e130e02b91d0820ad93a640d7f28f2c23f23528271e3641694330c749`  
		Last Modified: Fri, 16 Jan 2026 23:29:15 GMT  
		Size: 38.3 MB (38295743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b663e32a2b97b41e16bcc868cae73292acd229e41299de4974acc748e85e1ecc`  
		Last Modified: Fri, 16 Jan 2026 23:30:10 GMT  
		Size: 227.9 MB (227912589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:16947f364a18f0dbea4ca24ab3e29483359bfd0cd5247fdce96233fa512472c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a94b742623575e562a9da324df26321e405a7d128885d81cf3d58dcfbe24a99`

```dockerfile
```

-	Layers:
	-	`sha256:fa3d99859f0e522da22063744c2abf00c9e3e261514f27209bb4986196258178`  
		Last Modified: Sat, 17 Jan 2026 01:24:20 GMT  
		Size: 3.7 MB (3655355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcaa7e1607eae2d1f1000eeacf29dadaa8cceb6db73beb751b42c771aaeb9b84`  
		Last Modified: Fri, 16 Jan 2026 23:29:01 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b0408de3ff396d0b49fde7a77083846e877fac2090ec8371c3db1deded45a852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310435838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9eefa553d3100390959b76011ca25423ecdaeee9f50a7d0ceb5a916b295a11`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:31:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:31:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 16 Jan 2026 23:31:50 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 23:31:50 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 23:31:50 GMT
ENV JAVA_VERSION=27-ea+4
# Fri, 16 Jan 2026 23:31:50 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Jan 2026 23:31:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7099d6fad7d14a21ea13db57086b9cd7129cb7c247e916d93f12c415ab3c551`  
		Last Modified: Fri, 16 Jan 2026 23:32:22 GMT  
		Size: 38.7 MB (38697670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5895cb36439eca786b73f203fffd05652abca69df530950daa56e58eb38df063`  
		Last Modified: Fri, 16 Jan 2026 23:32:36 GMT  
		Size: 225.8 MB (225836265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:5fd102b1f2a1aa08e185cd23a078060b9cd3851ed5a76bc28a09b009f876bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8838c32b0a93b7e58211a596462f58a9f0ade110e694a1f363755c084cd5c016`

```dockerfile
```

-	Layers:
	-	`sha256:ff02396afc759f3c0a02db77c716dd898ff449e48ad70058568013d2a908d27e`  
		Last Modified: Sat, 17 Jan 2026 01:24:25 GMT  
		Size: 3.7 MB (3653045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86fddf70be616b0ff1166fa3ee498d2ea40eed418a837573054b417d400f2890`  
		Last Modified: Sat, 17 Jan 2026 01:24:26 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
