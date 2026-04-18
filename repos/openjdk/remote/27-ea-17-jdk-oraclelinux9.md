## `openjdk:27-ea-17-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:a1cfb462ea039e3d455423e01c4aaccd716dc1b7e847d82949bc0c9620b06a0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-17-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:699bf840ce774ce259158843a61c267f3c7d73432c6c9775b79f33a783d6ec18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314429033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8dd81a87905737e7522d832801dbab087311c025be8e3dae7d05d22077e6bd`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:39:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:39:18 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:13:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:13:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 18 Apr 2026 00:13:25 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Apr 2026 00:13:25 GMT
ENV LANG=C.UTF-8
# Sat, 18 Apr 2026 00:13:25 GMT
ENV JAVA_VERSION=27-ea+17
# Sat, 18 Apr 2026 00:13:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 18 Apr 2026 00:13:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bb5107df7baaf29d90d3f3cd5c8b8d9bb0e9786e901a49be069e0d37e4c07bae`  
		Last Modified: Fri, 17 Apr 2026 23:39:29 GMT  
		Size: 47.3 MB (47309813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293463526afd98c9c1fada4d2245ccd412fce97417e7875182a209d6d3af4680`  
		Last Modified: Sat, 18 Apr 2026 00:13:47 GMT  
		Size: 38.3 MB (38270134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adfd59a02afb9501fc53e956ffd42db9eadee8272b0b50406094d9bba6d9b92`  
		Last Modified: Sat, 18 Apr 2026 00:13:52 GMT  
		Size: 228.8 MB (228849086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:7f406d131d1b89c24d5def6891c5ebf49f9106516a006a31cd4d425885ebadd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c5f9706a59bd585981b4722b682dd5340ac4de669c180e6f0901477ddc3e57`

```dockerfile
```

-	Layers:
	-	`sha256:3458b08601210b8d01c280be86d5111cd3751848d54f6c62e7af18e89c039551`  
		Last Modified: Sat, 18 Apr 2026 00:13:45 GMT  
		Size: 3.7 MB (3652963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:480ac9e689f1d4e61f351b12eea84b83e86438ae746e2b7b578f2b55cc34b7f6`  
		Last Modified: Sat, 18 Apr 2026 00:13:45 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-17-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4d12688e67cc5a0042cbc717354d3c09011b60ee17d6f425a087f6e64aab5778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311375161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f7e4ec0aab37fbe38e8c133f0f9753d61a705dc77dfa080dc1c807c5eca0cf`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:52 GMT
CMD ["/bin/bash"]
# Sat, 18 Apr 2026 00:12:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 18 Apr 2026 00:12:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 18 Apr 2026 00:12:44 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Apr 2026 00:12:44 GMT
ENV LANG=C.UTF-8
# Sat, 18 Apr 2026 00:12:44 GMT
ENV JAVA_VERSION=27-ea+17
# Sat, 18 Apr 2026 00:12:44 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 18 Apr 2026 00:12:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b35b830a608cfc2dcaa5da71abe9012e9157f6732d8d283a866aa979b3d292be`  
		Last Modified: Fri, 17 Apr 2026 23:39:03 GMT  
		Size: 45.9 MB (45899787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4345b2993e1f6dd5a5a8a0ddadf48363ca9b0dbcc8654e3902d5750f4f1619dd`  
		Last Modified: Sat, 18 Apr 2026 00:13:09 GMT  
		Size: 38.7 MB (38667237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c827d1f6fbb471c0b8dd9b1bc1f4c2d3348778b0befd8c4aba6492cca7ce08`  
		Last Modified: Sat, 18 Apr 2026 00:13:14 GMT  
		Size: 226.8 MB (226808137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:083e371974eb186627a9f0ad3a4a730484c1eac174f4b1fd2ffaee924fb7e404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3666019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf1bc8ee011bcf427e7d94ae106eed9549449f6944da8b66c5eb450048288e0`

```dockerfile
```

-	Layers:
	-	`sha256:6045f69ad816785789b13f45ed1c2e86f46e36e82b8be37d37cb52041ba307d0`  
		Last Modified: Sat, 18 Apr 2026 00:13:07 GMT  
		Size: 3.7 MB (3650557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97bae9e115e315f2e3e5cdc3b64976987e87253061bca5109e82c8eae6123b23`  
		Last Modified: Sat, 18 Apr 2026 00:13:06 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
