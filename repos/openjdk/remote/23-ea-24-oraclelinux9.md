## `openjdk:23-ea-24-oraclelinux9`

```console
$ docker pull openjdk@sha256:3e51d5de9631daa50975a9db236a0026c7cb90c0ba084d08d988024df9d0fbc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-24-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:56c4c2d2365e4b6bd94b4fbeb684e66af295e362180f36e212aeea5f77086408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297336318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8650a5f924e8e112b602aa12ebc6a561258aa1d70e17f605ed38a05334d5d755`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 May 2024 17:23:46 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 29 May 2024 17:23:46 GMT
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
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8103c94114a3e3f3696bb8a78491c532cc7f329a5aa883c01393308c60ff3a11`  
		Last Modified: Sat, 01 Jun 2024 01:50:11 GMT  
		Size: 37.9 MB (37862519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d250832460928d05745683d8c65777a377a5ec84c39ee500f7d95e4b1a74417f`  
		Last Modified: Sat, 01 Jun 2024 01:50:15 GMT  
		Size: 210.5 MB (210478921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-24-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:7aab1bb8963bbd1e07002c4f8cb312afd1db684c7c421964098d24424efddc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5542fad23c5b89bfac9915c1ccb7081988ce3add5f9eb68c010abff704d02a`

```dockerfile
```

-	Layers:
	-	`sha256:790287e57a1b84916bf251b1b4ab8dc339caa91547f8ae7cf9ba46e84f50fa4a`  
		Last Modified: Sat, 01 Jun 2024 01:50:11 GMT  
		Size: 3.3 MB (3333243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834f6095cca155c538e64e77e29655ff4471ca6f1fd758bd87638500f0c6ec3b`  
		Last Modified: Sat, 01 Jun 2024 01:50:10 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-24-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e57a495caccb43ebd70a29eb2307f97d21ea63fe487d1494d26da15a5e3a984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294284429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7d128081d08e8f7ab34042326eea4d9d514451087aac6506ea38adc3a3f982`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 May 2024 17:23:46 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Wed, 29 May 2024 17:23:46 GMT
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
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4126ceeefbe5a1d06272578a6b6a99a1d422489b25511cbccbaaeb1576551bfd`  
		Last Modified: Sun, 02 Jun 2024 01:54:26 GMT  
		Size: 38.3 MB (38259157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42008cab5fa16551b15c7aa00cc3ed7d8326f13b1bc90362379327d2277cc`  
		Last Modified: Sun, 02 Jun 2024 01:54:29 GMT  
		Size: 208.4 MB (208373281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-24-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:9a14853f66ff60207673b25d04dba6e57650e51a1237ef1c5c5d2a590610d774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95874cbfce7f3eb9e9d739fcbc9e8c162225365c8a78dd0440770ee1bb004926`

```dockerfile
```

-	Layers:
	-	`sha256:fee9bbd78aadf19ccb845531afdb73b993b3bf6396378a88d196c5dea9ec59b5`  
		Last Modified: Sun, 02 Jun 2024 01:54:25 GMT  
		Size: 3.3 MB (3331626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d20ba55a69725b86a122749e51f1dbd2d16670356bca63157fbebae7a3969c`  
		Last Modified: Sun, 02 Jun 2024 01:54:25 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.in-toto+json
