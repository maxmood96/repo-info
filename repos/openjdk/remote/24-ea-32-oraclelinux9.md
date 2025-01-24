## `openjdk:24-ea-32-oraclelinux9`

```console
$ docker pull openjdk@sha256:6505e5d2257d16ab11f8c93256e00faac871bc47308ae2e7ca99f4f1e40f70aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-32-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:a9fdc8c6f7dae834c6be52f9db3af529c7c96df27d9f24d453e639910ad49549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310649663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671d2909c605cbb15a8dac9d1f9fc529b07a6b39bd5858a695d3ace775bc1c0b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce868e6ebff65cd828251ad179b6c0a331ec470c760695923c4bc38397f7d60e`  
		Last Modified: Thu, 23 Jan 2025 22:27:09 GMT  
		Size: 48.8 MB (48774984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758c4b779b9233353ddef6faaa1d76d82fb3cf05dfb91c46730ddacaa1ca0bfd`  
		Last Modified: Thu, 23 Jan 2025 22:27:11 GMT  
		Size: 212.8 MB (212775977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-32-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:dfdeaea7ab1fcd99251e54617702cfc5dfb5b2a3b5cbd9d1e7efc815bfb36517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68357f61198ced074c0a289db64a3aedc3ee74688cdd0859901e92cff64494f4`

```dockerfile
```

-	Layers:
	-	`sha256:fd09a121c09abf05f432c878c2bad2ea40739a00b88fe244a2e871de38f61fbd`  
		Last Modified: Thu, 23 Jan 2025 22:27:08 GMT  
		Size: 4.9 MB (4907575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e36fa64090994ea8b614b2268605f53316f7d051094288a672d0bb0de0ec75`  
		Last Modified: Thu, 23 Jan 2025 22:27:08 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-32-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:710cbbb73c87615e4116b4925c2bfcc4a8c743841009986d50c4731843bdb4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307600151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5027a8fe98120fedd58fbce396eeebbd04f7e0e624a83090f150e13f9f34b4a8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9527a70a5df0c50a0919b2bbc807b6789f8d6833d49f997079d3ab5dd2e735`  
		Last Modified: Wed, 22 Jan 2025 02:29:30 GMT  
		Size: 49.2 MB (49203729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1044ee2c4fb15e6dcfeeb709b8d122b4f848d38788d91fb9a757c3c4d6a2945`  
		Last Modified: Thu, 23 Jan 2025 22:29:55 GMT  
		Size: 210.7 MB (210729030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-32-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f3871df0c7f960ee8f64e941ea49b282305c0288c8a5dc156bc3c17838437097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ad9a7570c71de645bf6f7a13eba0816ee81ba32c1df3eefbbafb5b2e7faf84`

```dockerfile
```

-	Layers:
	-	`sha256:776bc2f84dbc0ce4a0ceca1eb193e21883ca1bc7f24674cf9fe471f02f90ab4e`  
		Last Modified: Thu, 23 Jan 2025 22:29:49 GMT  
		Size: 4.9 MB (4905337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60e74bb7f6a63d78ce585df0b61a52a6d8992969b11cafe0a1dbbe97168e0e6`  
		Last Modified: Thu, 23 Jan 2025 22:29:48 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
