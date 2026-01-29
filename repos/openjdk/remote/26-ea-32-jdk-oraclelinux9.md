## `openjdk:26-ea-32-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:a854ef05ccc170199bb7b0599b837564ac0743273b6e513d105b38325de367da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-32-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:1bf96b0382269e91123421097e7cb8abdce6cc44fd7b98a17720bb33dc2b9bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313475776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83395350716c1c4c7ecd08dc85283c025d9a32a023f19aa08af2570ea93d53a0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 21:31:17 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:31:17 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:12:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 28 Jan 2026 22:12:39 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 22:12:39 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 22:12:39 GMT
ENV JAVA_VERSION=26-ea+32
# Wed, 28 Jan 2026 22:12:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 28 Jan 2026 22:12:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:869c24490fd0fbe19ff930bf16fd1c67a7253c63ffb7ba471f8606a272ce29dd`  
		Last Modified: Wed, 28 Jan 2026 21:31:28 GMT  
		Size: 47.3 MB (47312714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17e94958ce11086530cb108a2252cc6445e86fb183d565e3d26ec1f5aab7776`  
		Last Modified: Wed, 28 Jan 2026 22:13:02 GMT  
		Size: 38.3 MB (38295590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb99fb3196ab850058fe4a698e34f84472f7a9556092ab110d1b95816b086d7`  
		Last Modified: Wed, 28 Jan 2026 22:13:06 GMT  
		Size: 227.9 MB (227867472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-32-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:d274f82f25efbeb72ac08b80b33dd456a41b183d981728a3ad29f7b3effa9f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc69af40e19b24630c00ff24fdf3b5568369900120c8ffdb9e739fe5080e5e2`

```dockerfile
```

-	Layers:
	-	`sha256:128a65d6fe6c7da03bb252ea8227a64f4dd93ae33076676fa203496eff73c840`  
		Last Modified: Wed, 28 Jan 2026 22:13:01 GMT  
		Size: 3.7 MB (3655391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d69ce2a9d147a37f7ee0bceec1cfc9c6a4b62d8ce4b7f499bcb2efc11db76c84`  
		Last Modified: Wed, 28 Jan 2026 22:13:00 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-32-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2fadc3ab1c6328db30f2a98696f4713c211ca09091a6ce97237b413b731f2c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310380700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9da70668be6defdea3e70d855fb395289d9176dadd20293fb779b95c1255a7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 21:29:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 28 Jan 2026 21:29:32 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 22:11:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 28 Jan 2026 22:11:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 28 Jan 2026 22:11:40 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 22:11:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 22:11:40 GMT
ENV JAVA_VERSION=26-ea+32
# Wed, 28 Jan 2026 22:11:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 28 Jan 2026 22:11:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:006f7f7ff6e4153965433950879efe455ec6847a503f9a7244723b1b4a79251b`  
		Last Modified: Wed, 28 Jan 2026 21:29:43 GMT  
		Size: 45.9 MB (45903228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7277b006798b7010f7a3c16433d0f4ff67bd919446768330eb3bb26f4c1b8392`  
		Last Modified: Wed, 28 Jan 2026 22:12:04 GMT  
		Size: 38.7 MB (38691925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706597df5c79d02c3cc58f5a91f8c62febfc66958b247eb5b033f5dd1d5eaffb`  
		Last Modified: Wed, 28 Jan 2026 22:12:08 GMT  
		Size: 225.8 MB (225785547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-32-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:ddda5519519f15fe942320627c667b35c6c4b35d53cd7c9b5cdba9f877e13e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166a25a7f99e65ee87ec0e4bc331266763a821ea5715d95af1582a2f60748456`

```dockerfile
```

-	Layers:
	-	`sha256:37d0824284b74e213b42ee1ccc20d22522278862428cee7b7a7109c9e6cefdbd`  
		Last Modified: Wed, 28 Jan 2026 22:12:02 GMT  
		Size: 3.7 MB (3653081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7390ec14679b619022c47eb35e5d8b76905c838bba35491336a105cb7a647dd4`  
		Last Modified: Wed, 28 Jan 2026 22:12:01 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
