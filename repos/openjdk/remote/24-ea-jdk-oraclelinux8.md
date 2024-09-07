## `openjdk:24-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:459297dbccc0b1abc1eb53d59abced3cba94fe35ca73e2615368fd932b00cee3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3b94cca14379264b5b74bee9bafaffdf6e3caef80266f0aca62fa90d9641fd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278642719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57043c4e828731a4d83450fcbddd00a79656b9d96882bfc2d624a93d717f180a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Aug 2024 01:20:57 GMT
ADD file:31fe8501106347a4e3341c03d1b81904a23f97e8744fdf62f24355513658cb72 in / 
# Fri, 23 Aug 2024 01:20:57 GMT
CMD ["/bin/bash"]
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 29 Aug 2024 18:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6ff78227fb6865113ff0e844c0e3dbbd3c3fee0fd03b4a3b3f7134390f785bd4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='21518bb62faf883eff4bfb1e2c69a5b50d6b3e96b30b0a111f1d1f41a4205fae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a4c7d85dbdbfdeab6ad5b1244e378081e17343d003de892c7fee8d9dd53a329f`  
		Last Modified: Fri, 23 Aug 2024 01:22:40 GMT  
		Size: 51.3 MB (51294233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa83650390250ce03fe597433bc5b53a1eb3bdfba20ed0acf5662c8b21650406`  
		Last Modified: Thu, 29 Aug 2024 21:00:03 GMT  
		Size: 15.0 MB (15040789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9a306268b353f4550c65e2e650438eac1f321e670155158a831f738c199323`  
		Last Modified: Thu, 29 Aug 2024 21:00:06 GMT  
		Size: 212.3 MB (212307697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:16cb5479a90fc3ab266a742d9e6458432bb80bf43195ace349e14ad8aeee8f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b2b62350c211862e68dd1a8b7084a5e1f7db17cbd0e3cd4e26f68b1640a9cd`

```dockerfile
```

-	Layers:
	-	`sha256:5824d57250eebf53d7717a72b735028e29fbef532949a18c0b7e38bf9116224c`  
		Last Modified: Thu, 29 Aug 2024 21:00:02 GMT  
		Size: 2.3 MB (2287869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53457b0a810be1c30a5a017ef31396d08efc66a9681aab224f0a36d6fc57609b`  
		Last Modified: Thu, 29 Aug 2024 21:00:02 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:df08456e348c453e43285cf2505b2c1b8420f355ee46f08406ec7e691016cd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275858201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ef53388b577f4f337d864fad5ad6282326b42a83404ca15e3bbee5a45eec05`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Aug 2024 00:40:52 GMT
ADD file:6b13879bf605622e279dbcac5c590af19f2ada3a9a83051585288eac41ef5a5b in / 
# Fri, 23 Aug 2024 00:40:53 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee4bb281b07b90a8d48b631141dbbfe6ee3f5d88680eac4b43c59de36db45ca5`  
		Last Modified: Fri, 23 Aug 2024 00:42:25 GMT  
		Size: 50.0 MB (50007867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c165483eb500b45b6fd4a0a0a8a6f46fbfdc62a2aba4faac778e22aac9005d`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 15.7 MB (15702976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc51607f9b4594225e6b8a2a9948627b64463c1b438c5794e6995a581e46104`  
		Last Modified: Fri, 06 Sep 2024 22:26:55 GMT  
		Size: 210.1 MB (210147358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:84acfe26091493528edcc742ee589577bb1f05cc3cd116c055f42d9382a6e13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb71228d92f092f69c8219979e37cdfee1e4d21e9626a30e7972b553571feef`

```dockerfile
```

-	Layers:
	-	`sha256:745656cf95658b5d9d8fa839b032f2f77cb4b1c9730d0eb19663e5ef00853603`  
		Last Modified: Fri, 06 Sep 2024 22:26:50 GMT  
		Size: 2.3 MB (2287338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62d254168bec24c25935d9f486212ca018aeb289184fced688135e4463fe9e5`  
		Last Modified: Fri, 06 Sep 2024 22:26:50 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
