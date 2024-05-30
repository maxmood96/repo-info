## `openjdk:23-ea-24-oraclelinux9`

```console
$ docker pull openjdk@sha256:de9b8086fb6f44089a9de3b6b47f7faba1aef578f557de09b55374b14c29bacc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-24-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:f3056a4503c4db9ebe99fcc07ff1e26c7ec4d5078adca84a07596d09350d3eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297340037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044abf4d87595bf58d551c36afe074870682a97381f73292b8d2dc100a275f4b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 22:30:14 GMT
ADD file:95cf7039855dd392d2faa5bb16415fdb79680afe50aecf7c299b8b2dd377328e in / 
# Thu, 09 May 2024 22:30:14 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 29 May 2024 17:23:46 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 29 May 2024 17:23:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fcbdc4090331ae224779b095ccebf7fa4fd896fb807b7d6bdb37776132e9710f`  
		Last Modified: Thu, 09 May 2024 22:31:50 GMT  
		Size: 49.0 MB (48998671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b376214fec0bdd909b74c38e0b0fe9243555cc0224fbf4a0e17c5162b7724ca`  
		Last Modified: Wed, 29 May 2024 23:01:17 GMT  
		Size: 37.9 MB (37862384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b259f4a84e66ca4287e8f6b49ae3c793b41e801996fe54878fd547385ecea5`  
		Last Modified: Wed, 29 May 2024 23:01:21 GMT  
		Size: 210.5 MB (210478982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-24-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:a08cd7c15adcd5eb66828283f7b342a18077014905bf3baab44d7c985ad8b48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a044e50a2e58bdd5f8ebdcc030f7499818af3af68fd23e86ca4db3c32d6bca75`

```dockerfile
```

-	Layers:
	-	`sha256:413a1e8710497e56ce830166df83798e141905515a9dbda14de23e42cabc1b0d`  
		Last Modified: Wed, 29 May 2024 23:01:17 GMT  
		Size: 3.3 MB (3333220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:053198caa794b52e9e7465b56ef57f77ee9bdfdabf3d16c1e1255e226509f04a`  
		Last Modified: Wed, 29 May 2024 23:01:17 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-24-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:39daa99eed01c3b1c61169630e6ac7ccff652be926fe8061ec548182ef77c1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294286362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2896f4886a8f98a9991e0ef046fac390e7bfc5080f33e8c85f009a025cb15c0c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 22:06:19 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Thu, 09 May 2024 22:06:19 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 29 May 2024 17:23:46 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 29 May 2024 17:23:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2299765a7e287b7319b50bb610f011c8eb05c98fd3e650d0863d09fd6470a5ec`  
		Last Modified: Thu, 30 May 2024 12:44:45 GMT  
		Size: 38.3 MB (38259385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5a4d1b7fb06139c80114a656ac06c05e61aaf783ecb07d5da70f46be1916e6`  
		Last Modified: Thu, 30 May 2024 12:44:49 GMT  
		Size: 208.4 MB (208373177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-24-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:336ea63c93dbc7acfcc8d0c80cbb9cb34aee7f6ba3b872570364e596d0e3f73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630fe341154c77f1e7ec4d0c7a276cc8e3637ee98d8e9d04c6938a6c88ba0932`

```dockerfile
```

-	Layers:
	-	`sha256:d53b1a5e6f31bdcf7c69ea2a6dcc55a3dff21148331e462ac3b2f0524e7afc5c`  
		Last Modified: Thu, 30 May 2024 12:44:44 GMT  
		Size: 3.3 MB (3331603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f9bfdf7513e36e51dded19db881074a86f1265bc00b56ddea57ec4d4f3a554`  
		Last Modified: Thu, 30 May 2024 12:44:43 GMT  
		Size: 19.9 KB (19950 bytes)  
		MIME: application/vnd.in-toto+json
