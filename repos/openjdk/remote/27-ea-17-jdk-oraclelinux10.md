## `openjdk:27-ea-17-jdk-oraclelinux10`

```console
$ docker pull openjdk@sha256:7252474d898ff965e24aed1c8c8f700fb075acce574d74b33d99eb5e1ec9d401
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-17-jdk-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:80499e87c52ba88993d9811bdb3c7fad75e29bd795de84b14daa15ef4662927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309602738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6591c0f24aef5fae583258ae808508a35403e761890d3e2c467cc7b2f41637`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:22 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:16:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:16:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 14 Apr 2026 19:16:29 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 19:16:29 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 19:16:29 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 19:16:29 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 19:16:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:498f1cd31aa47ca32767d1f6fb836be14f8c529c946cbcefb22da887b6176fce`  
		Last Modified: Tue, 14 Apr 2026 18:56:31 GMT  
		Size: 43.1 MB (43074860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f2565491e705c6f70a1ff3c9b989d8270ec37f34c13ffb4859290a2c3bb6a7`  
		Last Modified: Tue, 14 Apr 2026 19:16:52 GMT  
		Size: 37.7 MB (37678752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c29452658dbe133273b1bbda7899b30d82dfb92b714d6307192608a07255d28`  
		Last Modified: Tue, 14 Apr 2026 19:16:56 GMT  
		Size: 228.8 MB (228849126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:95642a1e68ac2fede38b5f525620973421666c900c604113d0bca4acff6e6452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3af716e002142d56dcbbae9ceafcc4260c7ae963ee89f6e27d7344c2389518b`

```dockerfile
```

-	Layers:
	-	`sha256:7febfc03cd125a9a117a59d4dcc751a5e2bbeadb0a8a8027be42f944313661f3`  
		Last Modified: Tue, 14 Apr 2026 19:16:50 GMT  
		Size: 2.4 MB (2369035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64b2ae909b0cac95260fdbd413fd9e7130c194fc94fbc7521eb64ba7f25dafc`  
		Last Modified: Tue, 14 Apr 2026 19:16:49 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-17-jdk-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:75d3329c7d42023b528faf83a35eb8b050eb89e5f8662bc114fa55a932cb4198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305977334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ba399be7d17878d807abbb0b6a2177414b150ee608505a639be3e87d9e0edb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:11 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:17:01 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:17:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 14 Apr 2026 19:17:11 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 19:17:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 19:17:11 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 19:17:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 19:17:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cff1e6245ebd88e4cb56192e615670dfed7647e37ae961c194f005f3e0c4fa4e`  
		Last Modified: Tue, 14 Apr 2026 18:55:20 GMT  
		Size: 41.5 MB (41477251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110e3dca9f62cc6df5ea9a68bb56597a293fccd8b8a5357f2f6d1934047f9b1e`  
		Last Modified: Tue, 14 Apr 2026 19:17:33 GMT  
		Size: 37.7 MB (37691978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5601a8b58555f3bf8be7bfdae7786008d2d1d6357c401d0147cd81472b1b00c4`  
		Last Modified: Tue, 14 Apr 2026 19:17:38 GMT  
		Size: 226.8 MB (226808105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:4b511a451710ab9abcb6f9411cb17a547d85706eb1877e265f0f041f5d103099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd90eb587728cbc191e7a8598ebd90fc62eada961a40501c92734e1a14e9e79`

```dockerfile
```

-	Layers:
	-	`sha256:00ff369f0ecbd191d2e181765d6ba7481e4210f27539e639eca1e5af1eec1cce`  
		Last Modified: Tue, 14 Apr 2026 19:17:32 GMT  
		Size: 2.4 MB (2368563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d89582ea2c71389ffa5610ba5fecdc8ae4db7ef9220aaab41e16af53d20fa01`  
		Last Modified: Tue, 14 Apr 2026 19:17:32 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
